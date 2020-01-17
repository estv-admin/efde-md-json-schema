# efde-md-json-schema

Install go library and cli to validate json

    go get github.com/santhosh-tekuri/jsonschema

Add the following content to a local file called 'create_claim_output_error.json'

```json
{
    "success": false,
    "error": [
       {
          "errorCode": "M0016",
          "errorDescription": "Claim not valid"
       },
       {
          "errorCode": "E0004",
          "errorReferenceID": "B491C9A9-6C16-DA67-5DAB-F8FFAD6CF52C",
          "errorDescription": "Invalid DocumentID. No document found."
       },
       {
          "errorCode": "E0004",
          "errorReferenceID": "B491C9A9-6C16-DA67-5DAB-F8FFAD6CF52C",
          "errorDescription": "Invalid DocumentID. No document found."
       }
    ]
 }
```

Run the cli 'jv' to validate the above json data

    jv https://raw.githubusercontent.com/estv-admin/efde-md-json-schema/master/create_claim_output_schema.json create_claim_output_error.json

