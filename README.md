#Extract Responder Hashes

Extract hashes from `Responder-Session.log`. Select to extract only one hash per user (first occurence) or all the hashes gathered (different HASH_TYPE) per user. Other options can be specified to filter the results.s

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
--start mm/dd/yyyy: [OPTIONAL] Extract hashes starting from the date specified
    **The date must exist in the file
--end mm/dd/yyyy: [OPTIONAL] Extract hashes till the date specified (included)
    **The date must exist in the file
```


##TODO
*  Select the types of hash to extract or All
*  Try to nslookup/ping the machine to check if it alive/true
