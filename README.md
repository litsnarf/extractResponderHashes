#Extract Responder Hashes

Extract hashes from `Responder-Session.log`. Select to extract only one hash per user (first occurence) or all the hashes gathered (different HASH_TYPE) per user.

##Usage

```bash
./extractResponderHashes [-i|--input] <Responder-Session.log> [-o|--output] [-A]
```
###Options
```
-o, --output <filename>:  [OPTIONAL] Output results into a file.
    If not specified, the results are printed in the stdout
-i, --input  <filename>:  [OPTIONAL]responder log file to parse
-A: [OPTIONAL] Extract all the hashes for every user. If not specified,
    it prints only the first occurence in the file (per user)
```


##TODO
*  Select the time frame to parse
*  Select the types of hash to extract or All
