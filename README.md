It looks like you're creating a module that handles response formatting for success and error cases in a JSON format. To create documentation for this package named response-json-format, you can outline the purpose of the module, describe its functions, and provide examples of usage. Here's an example structure for your documentation:

**response-json-format Package**

**Overview**

The response-json-format package is designed to standardize the formatting of JSON responses for success and error scenarios in JavaScript applications.

**Installation**

You can install the response-json-format package via npm:

npm install response-json-format

**Usage**

Importing the Module

const { sendOkResponce, sendErrorResponce } = require("response-json-format");

“sendOkResponce(data, message) “ Creates a standardized success response object.

**Parameters:**

data (optional): Data payload to be included in the response.

message (optional): Custom success message.

**Returns:**

An object containing:

status: true

message: The provided message or a default "Success" message.

data: The provided data or null if not specified.

“sendErrorResponce(error, message)” Creates a standardized error response object.

**Parameters:**

error (optional): Error details to be included in the response.

message (optional): Custom error message.

**Returns:**

An object containing:

status: false

message: The provided message or a default "Error" message.

error: The provided error or null if not specified.

**Example**
```javascript
const { sendOkResponce, sendErrorResponce } = require("response-json-format");
const my_function = async (req, res) => {
    try {
        let data = { "name": "no name", "email": "example@email.com" };
        res.status(200).json(sendOkResponce(data, "SUCCESS"));
    } catch (error) {
        res.status(400).json(sendErrorResponce(error, "Error"));
    }
}
```

This package facilitates consistent JSON response formatting for success and error cases, enhancing the readability and standardization of your application's API responses.

