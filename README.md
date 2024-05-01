# OSINT CAT API v2

Our Data Breach Search API provides a powerful interface for searching through various data breaches to find if certain details (email, username, password, IP address) have been compromised. It aggregates data from multiple sources, offering a comprehensive search capability. This document outlines how to interact with the API, including authentication, request formats, endpoints, and examples.

To simplify the documentation we are just gonna provide curl request examples that will work with our API. You can easily convert these to any language you like.

Ensure that you have opened a ticket in our [Discord](https://discord.gg/osintcat) and provided your API key so we can authorize it in our WAF if you run into Cloudflare issues. 
*Please note that not all of the headers in the curl requests are required. You also do not need the `cf_clearance` cookie.*

## Authentication

To use the API, you need a valid API key, which must be included in the request cookies as `API-Key`. Unauthorized requests will be denied.

## Blacklist

The API maintains a blacklist. Blacklisted queries will be denied.

## Response Format

Responses from the API are in JSON format. A successful search will return the relevant data from the breach databases. In case of an error (e.g., invalid API key, blacklisted query, or failed search), the response will include an error message and a status code indicating the nature of the issue.

## Security and Privacy

Ensure your API key is kept secure and not exposed publicly. Avoid sending sensitive personal information unnecessarily. Sharing this key will result in a full blacklist if you haven't gotten prior permission.

## Username Searches
### Our Username Search Engine is used to determine if a username has been exposed in a data breach.

### Maine Coon User Search

```bash
curl 'https://osintcat.com/api/mainecoonusersearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"username":"Query"}'
```
### Persian Username search:
```bash
curl 'https://osintcat.com/api/persianusersearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"username":"Query"}' ;
```
### Ragdoll Username Search:
```bash
curl 'https://osintcat.com/api/ragdollusernamesearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"username":"Query"}' ;
```

### Burmese Username Search:
```bash
curl 'https://osintcat.com/api/burmeseusernamesearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"username":"Query"}' ;
```
### Osint Cat Username Search:
```bash
curl 'https://osintcat.com/api/osintcatusersearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"username":"Query"}'
```

IP Searches:
=============================================================================
### Contains information about an IP Address and if any IP address have been exposed in a Data Breach. 

### Mainecoon IP Search:
```bash
curl 'https://osintcat.com/api/mainecoonipsearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"ip":"Query"}' ;
```
### Osint Cat IP Search: 
```bash
curl 'https://osintcat.com/api/osintcatipsearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"ip":"Query"}'
```

Email Searches:
=============================================================================
### Our Email Search engine shows what Emails have been exposed in a data breach. 

### Mainecoon Email Search: 
```bash
curl 'https://osintcat.com/api/mainecoonemailsearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"email":"Query"}' ;
```
### Persian Email Search: 
```bash
curl 'https://osintcat.com/api/persianemailsearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"email":"Query"}' ;
```
### Ragdoll Email Search:
```bash
curl 'https://osintcat.com/api/ragdollemailsearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"email":"Query"}' ;
```
### Burmese Email Search: 
```bash
curl 'https://osintcat.com/api/burmeseemailsearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"email":"Query"}' ;
```
### Osint Cat Email Search: 
```bash
curl 'https://osintcat.com/api/osintcatemailsearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"email":"Query"}'
  ```

Password searches:
=============================================================================
### Our Password searches are used to find what passwords have been exposed in a data breach. 

### Mainecoon Password Search:
```bash
curl 'https://osintcat.com/api/mainecoonpasswordsearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"password":"Query"}' ;
```
### Persian Password Search:
```bash
curl 'https://osintcat.com/api/persianpasswordsearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"password":"Query"}'
```
Phone Number Searches:
=============================================================================
### Our Phone Number Searches are used to find breaches within Phone Numbers. 

### Persian Phone Number Search: 
```bash
curl 'https://osintcat.com/api/persianphonesearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"phone":"Query"}' ;
```
### Ragdoll Phone Number Search:  
```bash
curl 'https://osintcat.com/api/ragdollphonesearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"phone":"Query"}'
  ```
Gaming Database Searches:
=============================================================================
### Our Gaming Database contains lines from Gaming Platforms and Hangout sources and forums. 

### Our Osint Cat Gaming Database:
```bash
curl 'https://osintcat.com/api/osintcatgamesearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"gaming":"Query"}' ;
```
### Ragdoll Minecraft Database:
```bash
curl 'https://osintcat.com/api/ragdollmcsearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"gaming":"Query"}'
  ```
Hash Lookups:
=============================================================================
### Used to solve and guess hashes. 

### Osint Cat Hash Solver/Guesser:
```bash
curl 'https://osintcat.com/api/hashsearch' \
  -H 'accept: */*' \
  -H 'accept-language: en-GB,en;q=0.5' \
  -H 'content-type: application/json' \
  -H 'cookie: cf_clearance=tSnQQ8pCucJ0fJeGS4VHd3SyT7B6_jhfXbZ_P2HQW50-1714470082-1.0.1.1-zwcF.P.GiuTiQKtAu2PtNDSQqkjn3QJX_2cYfxITrh.3839CDBfJAtbrCtEXrbHddq4QuTx5uFtHdruAfetKAg; API-Key=YOURAPIKEY' \
  -H 'origin: https://osintcat.com' \
  -H 'priority: u=1, i' \
  -H 'referer: https://osintcat.com/search' \
  -H 'sec-ch-ua: "Chromium";v="124", "Brave";v="124", "Not-A.Brand";v="99"' \
  -H 'sec-ch-ua-mobile: ?0' \
  -H 'sec-ch-ua-model: ""' \
  -H 'sec-ch-ua-platform: "Linux"' \
  -H 'sec-ch-ua-platform-version: "6.8.7"' \
  -H 'sec-fetch-dest: empty' \
  -H 'sec-fetch-mode: cors' \
  -H 'sec-fetch-site: same-origin' \
  -H 'sec-gpc: 1' \
  -H 'user-agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36' \
  --data-raw '{"hash":"Query"}'
```


## Support

For issues, questions, or API key requests, please contact the API support team at [ceo@osintcat.com](mailto:ceo@osintcat.com) or via the [Discord server](https://discord.gg/osintcat).

Thanks to [SallyHacks](https://github.com/SallyHacks)  for organizing and creating this Documentation. 
