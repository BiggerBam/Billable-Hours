# Billable-Hours

Postman Test Collection README
This README provides an explanation of a Postman test collection named "Bundle." The collection includes three API requests and is intended to demonstrate the process of parsing a CSV file content, retrieving invoice parsing results by ID, and fetching company details from an invoice. The collection is organized in a Postman Collection v2.1.0 format.

API Requests
1. Parse CSV file content
Name: Parse CSV file content
Method: POST
URL: {{baseURL}}/invoice/parse
Description: This request is used to parse a CSV file's content. It sends a JSON payload with CSV data to be parsed.
Request Body: JSON payload with CSV data.
Example Body:
json
Copy code
{
    "payload": "CSV data in base64 encoded format"
}
2. Get Invoice Parsing Result by ID
Name: Get Invoice Parsing Result by ID
Method: GET
URL: {{baseURL}}/invoice/bbd4f48d-30c1-4f90-8377-16614975d46c
Description: This request retrieves the parsing result for an invoice with a specific ID.
Request Parameters: The invoice ID is included in the URL path.
Example URL:
https://csvdemomockappp.bundlewallet.com/invoice/bbd4f48d-30c1-4f90-8377-16614975d46c
3. Get Company details from an Invoice
Name: Get Company details from an Invoice
Method: GET
URL: {{baseURL}}/invoice/bbd4f48d-30c1-4f90-8377-16614975d46c/company?companyName=Google
Description: This request fetches company details from a specific invoice where the company name matches "Google."
Request Parameters: The invoice ID is included in the URL path, and the company name is provided as a query parameter.
Example URL:
https://csvdemomockappp.bundlewallet.com/invoice/bbd4f48d-30c1-4f90-8377-16614975d46c/company?companyName=Google
Environment Variables
The collection utilizes environment variables to make the URLs dynamic. Here are the defined variables:

baseURL: The base URL for the API requests. It is set to https://csvdemomockappp.bundlewallet.com.
companyName: A variable set to "Google."
invoice_id: A variable set to "Google."
Tests and Scripts
The collection includes two event scripts:

Prerequest Script: This script is empty and can be used to run JavaScript code before each request.

Test Script: This script is also empty and can be used to run JavaScript code after each request to validate responses or perform additional actions.

Please note that the actual test logic should be written in the "Test Script" section as required.
