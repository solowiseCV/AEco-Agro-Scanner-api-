

# QR Code Scanner API

This API provides functionality for scanning QR codes and fetching product information based on the scanned QR code.

## Usage

### Scan QR Code

POST /scan

Scan a QR code and retrieve product information.

#### Request Body

```json
{
  "qrData": "Base64EncodedQRCodeData"
} ```

qrData: Base64 encoded QR code data captured from the device's camera.

## Response
{
  "productId": "123456",
  "productName": "Product Name",
  "description": "Product Description",
  "price": 29.99
}


productId: Unique identifier of the scanned product.
productName: Name of the product.
description: Description of the product.
price: Price of the product.

Error Responses

If an error occurs during the scanning process or while fetching product information, the API will return an appropriate error response with a corresponding status code.

Example Error Response
{
  "error": "Error message"
}


# QR Code Scanner API

This API provides functionality for scanning QR codes and fetching product information based on the scanned QR code.

## Usage

### Scan QR Code
POST /scan


Scan a QR code and retrieve product information.

#### Request Body
```json
{
  "qrData": "Base64EncodedQRCodeData"
}
qrData: Base64 encoded QR code data captured from the device's camera.
Response
json

{
  "productId": "123456",
  "productName": "Product Name",
  "description": "Product Description",
  "price": 29.99
}
productId: Unique identifier of the scanned product.
productName: Name of the product.
description: Description of the product.
price: Price of the product.

Error Responses
If an error occurs during the scanning process or while fetching product information, the API will return an appropriate error response with a corresponding status code.

Example Error Response
json

{
  "error": "Error message"
}

Getting Started

Installation

Clone the repository: 
git clone https://github.com/solowiseCV/Eco-Agro

Install dependencies:

cd qr-code-scanner-api
npm install

Start the server:
  npm start

 The server will be running at http://localhost:5000 by default.

 Dependencies
express: ^4.17.1
body-parser: ^1.19.0
qrcode-reader: ^0.6.3
axios: ^0.21.1

