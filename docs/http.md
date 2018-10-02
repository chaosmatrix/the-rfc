### Http Status Code
1. status code && Method
    * 301/302: method "POST" can change into "GET"
    * 307/308: method "POST" must no change into "GET"
        * some lib not support 308 code
2. Lib support status
    * libcurl support clearly disable "POST" to "GET" even use 301/302
        * new version make this as default
    * Go/Java/Python default change "POST" into "GETO" when use 301/302
        * Go support self define redirect handler to overwrite this
