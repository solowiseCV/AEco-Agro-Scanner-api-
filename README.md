

# QR Code Scanner API

## Introduction 
This Api documentation is sub documentation for api that provides functionality for scanning QR codes and fetching product information based on the scanned QR code.



### Route

POST /scan

``route.get("/api/v1/scan/grainId")``

Scan a QR code and retrieve product information.

#### Request Body

json
{
  "qrData": "Base64EncodedQRCodeData"
} 

qrData: Base64 encoded QR code data captured from the device's camera.

 ## Response
 - If the product ID is found in the database
  If the product contains GMO ingredients:

{
  "message": "<Product Name> contains GMO ingredients.",
  "moreDetails": "Link to GMO Information Center for more details"
}

If the product does not contain GMO ingredients
 {
  "name": "<Product Name>",
  "description": "<Product Description>",
  "isGMO": false,
  "ingredients": ["<Ingredient 1>", "<Ingredient 2>", ...],
  "nutritionalFacts": {
    "calories": <Calories>,
    "fat": "<Fat Content>"
  }
}

## Error Responses

If an error occurs during the scanning process or while fetching product information, the API will return an appropriate error response with a corresponding status code.

Example Error Response
{
  "error": "Error message"
}



## Getting Started

### Installation

## Clone the repository: 
- git clone https://github.com/solowiseCV/AEco-Agro-Scanner-api-/

### Install dependencies:

cd qr-code-scanner-api
npm install

Start the server:
  npm start

 The server will be running at http://localhost:5000 by default.

 Dependencies

  express: Fast, unopinionated, minimalist web framework for Node.js.
  body-parser: Node.js body parsing middleware.
  qrcode-reader: QR code reading library for Node.js.
  fs: Node.js file system module.
  base-64: Base64 encoding and decoding for Node.js.
  axios: Promise based HTTP client for Node.js and the browser.

