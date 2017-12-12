To identify and validate correctly Operator and/or User an http header needs to be added to all requests:

    Header: Authorization
    Value: Bearer {JWT Token}

For development and testing, we will provide a token with a very long lifetime that can be used also with common tools such as Swagger. In real production, the token needs to be obtained and signed using a dedicated service which will be provided and documented separately.
 
JWT stands for JSON Web Token. This is an open standard that defines a compact way for transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. The JWT Token is encrypted to provide confidentiality. It consists of three parts separated by dots (.), which are:

* Header
* Payload
* Signature

The JWT token is added to the header for the request sent to the API.