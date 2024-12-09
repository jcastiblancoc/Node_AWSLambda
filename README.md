# Node.js AWS Lambda Integration

This project demonstrates how to create and deploy a serverless application using **Node.js** and **AWS Lambda**. It includes a simple API that handles HTTP requests through **API Gateway** and processes them within Lambda functions.

## Features

- Serverless architecture powered by AWS Lambda.
- Integration with **AWS API Gateway** for HTTP endpoints.
- Environment variable management for configuration.
- Sample endpoints to handle basic HTTP methods (`GET`, `POST`, etc.).
- Lightweight and modular structure for scalability.

## Prerequisites

To work with this project, you need:

- [Node.js](https://nodejs.org/) installed on your machine.
- An AWS account with permissions to use **Lambda** and **API Gateway**.
- [AWS CLI](https://aws.amazon.com/cli/) configured with your credentials.
- [Serverless Framework](https://www.serverless.com/) installed globally:
  ```bash
  npm install -g serverless
Installation
Clone the repository:

bash
Copiar código
git clone https://github.com/jcastiblancoc/Node_AWSLambda.git
cd Node_AWSLambda
Install dependencies:

bash
Copiar código
npm install
Set up environment variables: Create a .env file at the root of the project and add the required configuration, such as:

env
Copiar código
AWS_REGION=<your-aws-region>
FUNCTION_NAME=<your-function-name>
Deployment
This project uses the Serverless Framework for deployment.

Deploy to AWS: Run the following command to deploy your application:

bash
Copiar código
serverless deploy
Access the API: After deployment, the API Gateway endpoint will be displayed in the terminal. Use this URL to interact with your Lambda functions.

Project Structure
bash
Copiar código
├── src
│   ├── handlers
│   │   ├── getHandler.js   # Handles GET requests
│   │   ├── postHandler.js  # Handles POST requests
│   └── utils
│       └── helper.js       # Utility functions
├── .env                    # Environment variables
├── serverless.yml          # Serverless Framework configuration
├── package.json            # Project dependencies
├── README.md               # Project documentation
Usage
Local Testing
Install the serverless-offline plugin:

bash
Copiar código
npm install serverless-offline --save-dev
Run the application locally:

bash
Copiar código
serverless offline
Interact with the API on http://localhost:<port>.

Endpoints
GET /items: Retrieves a list of items.
POST /items: Creates a new item in the database.
PUT /items/:id: Updates an item by ID.
DELETE /items/:id: Deletes an item by ID.
Example Request
GET /items
bash
Copiar código
curl https://<your-api-gateway-url>/items
POST /items
bash
Copiar código
curl -X POST -H "Content-Type: application/json" -d '{"name": "Item1", "value": 100}' https://<your-api-gateway-url>/items
Contributing
Contributions are welcome! Please fork this repository and submit a pull request with your changes.

License
This project is licensed under the MIT License. See the LICENSE file for more details.

Resources
AWS Lambda Documentation
Serverless Framework Documentation
