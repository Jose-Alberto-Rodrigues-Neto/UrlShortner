# URL Shortener Application

<p align="center"> <img src="https://cdn-icons-png.flaticon.com/512/5968/5968282.png" alt="Java" width="100" height="100"/> <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5c/Amazon_Lambda_architecture_logo.svg/800px-Amazon_Lambda_architecture_logo.svg.png" alt="AWS Lambda" width="100" height="100"/> <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQ-DgaVlN8dTlh9pQuxPEUFaN1hl8ukuPUolQ&s" alt="AWS S3" width="100" height="100"/> <img src="https://seeklogo.com/images/A/aws-api-gateway-logo-368082D845-seeklogo.com.png" alt="AWS API Gateway" width="100" height="100"/> </p>

This project is a **simple URL shortener application** built using **Java** and **AWS services**, including **AWS S3**, **AWS Lambda**, and **API Gateway**. It allows users to create shortened URLs that redirect to their original destinations.

## Features

- **Short URL Generation**: Easily generate shortened URLs for long links.
- **Redirection**: Shortened URLs redirect users to their original links.
- **Serverless Architecture**: Built using AWS Lambda for scalability and cost efficiency.
- **Data Storage**: Links and metadata are securely stored in AWS S3.
- **API Gateway Integration**: Provides RESTful endpoints for URL creation and redirection.

## Technologies Used

- **Java**: The core programming language for the application logic.
- **AWS S3**: For storing mapping data between shortened and original URLs.
- **AWS Lambda**: Serverless backend for processing API requests.
- **AWS API Gateway**: Exposes RESTful APIs for client interaction.

## Getting Started

### Prerequisites

- AWS account with access to S3, Lambda, and API Gateway.
- Java Development Kit (JDK 17).
- AWS CLI configured with appropriate permissions.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/url-shortener.git
   ```
2. Navigate to the project directory:
   ```bash
   cd url-shortener
   ```
3. Create your .env with your AWS S3 Bucket:
   ```bash
   #.env
   S3_BUCKET=your-bucket
   ```
4. Build your .zip file to use:
   ```bash
   mvn clean package
   ```

### Deployment

1. Create an S3 bucket to store URL mappings.
2. Deploy the Lambda function using the provided AWS SAM template or manually upload the package.
3. Configure API Gateway to trigger the Lambda function for specific endpoints.
4. Test the application by sending requests to the API Gateway endpoint.

## Usage

1. Send a POST request to the API with the original URL to generate a shortened link.
2. Use the shortened link to redirect to the original URL.
