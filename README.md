#Extract Responder Hashes

Extract hashes from `Responder-Session.log`. You can choose to extract all hashes or filter the results
* one hash per user (first occurrence)
* date range
* hash type
* protocol
* more - check Usage section

##Usage

```bash
./extractResponderHashes [-i|--input] <Responder-Session.log> [-o|--output] [-A,--start,--end, -P "SMB|FTP", -H "NTLMv2" ]
```
###Options
```
-o, --output <filename>:  [OPTIONAL] Output results into a file.
      If not specified, the results are printed in the stdout
-i, --input  <filename>:  [OPTIONAL] Responder log file to parse
-A: [OPTIONAL] Extract all the hashes for every user (useful to check against john pot).
    If not specified, it prints only the first occurence per user
--start mm/dd/yyyy: [OPTIONAL] Extract hashes starting from the date specified
      **The date must exist in the file
--end mm/dd/yyyy: [OPTIONAL] Extract hashes till the date specified (included)
      **The date must exist in the file
-P, --protocols <protocol_name>: [OPTIONAL] Select the protocol for which you want the hashes
      If more than, one separate with | : -P "SMB|HTTP|SMBv2|FTP"
-H, --hash-type <HASH_TYPE>: [OPTIONAL] Select the HASH_TYPE for which you want the hashes
      If more than one, separate with | : -H "NTLMv2|NTLMv2-SSP"
```


##TODO
* Try to nslookup/ping the machine to check if it alive/true
* Extract specif user hashes
* Extract specific domain hashes
