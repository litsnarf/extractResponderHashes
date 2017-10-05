#Extract Responder Hashes

Extract hashes from `Responder-Session.log`. Select to extract all hashes or filter by
* one hash per user (first occurrence)
* date range
* hash type
* protocol
* user
* domain
* IP and client information

##Usage

```bash
./extractResponderHashes [-i|--input] <Responder-Session.log> [-o|--output,-A,--start,--end,-P "SMB|FTP" -H "NTLMv2|NTLMv2-SSP", 
```
###Options
```
Input/Output options
  -i, --input  <filename>           Responder log file to parse
  -o, --output <filename>           Output results into a file 
  -I, --show-ip                     Print client information for each hash

Filter options
  -A:                               Extract ALL the hashes for every user. By default extraxt the first occurence
  -P, --protocols <protocol_name>   Protocol(s) for which you want the hashes. Separate with pipe (|): -P "SMB|HTTP|SMBv2|FTP"
  -H, --hash-type <HASH_TYPE>       HASH_TYPE for which you want the hashes. Separate with pipe (|): -H "NTLMv2|NTLMv2-SSP"
  -U, --user <username>             Filter hashes for a specific username
  -D, --domain                      Filter hashes for a specific domain

Date and time: the dates must exist in the file
  --start mm/dd/yyyy                Extract hashes starting from the date specified
  --end mm/dd/yyyy                  Extract hashes till the date specified (included)
```

##TODO
* Try to nslookup/ping the machine to check if it alive/true
* print client IP information (IP)
* add IP filter
