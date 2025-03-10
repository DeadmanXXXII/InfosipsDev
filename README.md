# InfoSips - SIP Information Stealer

InfoSips is a penetration testing tool designed for ethical hacking and security research on vulnerable sips endpoints.
Use responsibly and report vulnerabilities to affected vendors.

## Installation
```bash
pip install infosips
```

Yes, you can modify the script to request information from each stage dynamically. Instead of sending one request with a wildcard path, the script will iterate through each possible structure and send multiple requests, capturing responses from every stage.


---

How This Works:

1. Iterate Over Each Level: The script will generate different URL structures based on a specified wildcard depth.


2. Send Requests for Each Variation: It will send a request for:

/users/*

/users/*/*

/users/*/*/*

and so on, up to the specified depth.



3. Capture and Store Responses: Each response is logged and optionally saved to a file.





How This Works:

1. Dynamically Generates URL Paths:

The script starts with https://{base_url}/sips/sipsys/users/*

Then https://{base_url}/sips/sipsys/users/*/*

Then https://{base_url}/sips/sipsys/users/*/*/*

This continues up to --wildcard-depth (default: 3)



2. Sends Requests for Each Stage:

Requests data from each level

Stores responses if successful



3. Saves Responses to a File (Optional):

If --output file.txt is used, all responses are stored for later analysis.





---

Example Commands

1. Run with Default 3 Wildcard Depth:
```bash
python infosteal.py https://example.com/sips --wildcard-depth 3 --verbose
```
Sends requests to:

https://example.com/sips/sipsys/users/*
https://example.com/sips/sipsys/users/*/*
https://example.com/sips/sipsys/users/*/*/*



2. Run with 5 Wildcard Depth and Save Output:
```bash
python infosteal.py https://example.com/sips --wildcard-depth 5 --output results.txt
```

Sends requests up to depth 5 and saves all results in results.txt.



3. Use a Proxy and Custom Headers:
```
python infosteal.py https://example.com/sips --proxy http://127.0.0.1# InfoSips - SIP Information Stealer

InfoSips is a penetration testing tool designed for ethical hacking and security research on vulnerable sips endpoints.
Use responsibly and report vulnerabilities to affected vendors.

## Installation
```bash
pip install infosips
```

Yes, you can modify the script to request information from each stage dynamically. Instead of sending one request with a wildcard path, the script will iterate through each possible structure and send multiple requests, capturing responses from every stage.


---

How This Works:

1. Iterate Over Each Level: The script will generate different URL structures based on a specified wildcard depth.


2. Send Requests for Each Variation: It will send a request for:

/users/*

/users/*/*

/users/*/*/*

and so on, up to the specified depth.



3. Capture and Store Responses: Each response is logged and optionally saved to a file.





How This Works:

1. Dynamically Generates URL Paths:

The script starts with https://{base_url}/sips/sipsys/users/*

Then https://{base_url}/sips/sipsys/users/*/*

Then https://{base_url}/sips/sipsys/users/*/*/*

This continues up to --wildcard-depth (default: 3)



2. Sends Requests for Each Stage:

Requests data from each level

Stores responses if successful



3. Saves Responses to a File (Optional):

If --output file.txt is used, all responses are stored for later analysis.





---

Example Commands

1. Run with Default 3 Wildcard Depth:
```bash
python infosteal.py https://example.com/sips --wildcard-depth 3 --verbose
```
Sends requests to:

https://example.com/sips/sipsys/users/*
https://example.com/sips/sipsys/users/*/*
https://example.com/sips/sipsys/users/*/*/*



2. Run with 5 Wildcard Depth and Save Output:
```bash
python infosteal.py https://example.com/sips --wildcard-depth 5 --output results.txt
```

Sends requests up to depth 5 and saves all results in results.txt.



3. Use a Proxy and Custom Headers:
```
python infosteal.py https://example.com/sips --proxy http://127.0.0.1:8080 --headers '{"User-Agent": "Mozilla/5.0"}' --wildcard-depth 4
```



✅ Requests Information from Every Stage
✅ Automatically Iterates Through Depths
✅ Handles Errors Gracefully (404, Timeout, etc.)
✅ Supports Output to File for Offline Analysis
✅ Works with Proxies and Custom Headers


---
:8080 --headers '{"User-Agent": "Mozilla/5.0"}' --wildcard-depth 4
```



✅ Requests Information from Every Stage
✅ Automatically Iterates Through Depths
✅ Handles Errors Gracefully (404, Timeout, etc.)
✅ Supports Output to File for Offline Analysis
✅ Works with Proxies and Custom Headers


---
