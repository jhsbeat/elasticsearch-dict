elasticsearch-dict
===========================================================
**A web front end for management of elasticsearch dictionaries such as synonyms and stopwords.**

**This code is just for being test**

## Example

```
PUT /my_index
{
  "index" : {
    "analysis" : {
      "analyzer" : {
        "synonym" : {
          "tokenizer" : "whitespace",
            "filter" : ["synonym"]
          }
        },
      "filter" : {
        "synonym" : {
          "type" : "synonym",
          "synonyms_path" : "../plugins/dict/_site/dictionaries/synonyms.txt"
        }
      }
    }
  }
}
```

## License

Copyright 2016 jhsbeat.

Licensed under the Apache License, Version 2.0: http://www.apache.org/licenses/LICENSE-2.0