# Dynamic Price Forecasting 📈💳

Welcome to the Dynamic Price Forecasting project! This repository contains all the necessary information for deploying, utilizing, and understanding a dynamic price forecasting model built using AWS SageMaker, AWS Lambda, API Gateway, and S3 buckets for storage.

## Introduction 👤
Dynamic pricing is a crucial aspect of modern business strategy, allowing companies to adjust prices in response to market demand, competition, and other factors. This project leverages machine learning to forecast prices dynamically, ensuring optimal pricing strategies. This model was trained on a dataset comprising over 2.7 million data instances. After testing more than 8 different regression models, LightGBM emerged as the top performer, achieving an R-squared score of 0.84.

The core components of this project include:
- **AWS SageMaker** for training and deploying the machine learning model.
- **AWS Lambda** for serverless computing and handling API requests.
- **API Gateway** to create, publish, maintain, monitor, and secure APIs.
- **S3 Buckets** for storing data and model artifacts.

## Features
- **Accurate Revenue Forecasting**: Utilizes advanced ML models to predict prices dynamically.
- **Scalable**: Built on AWS infrastructure, ensuring scalability and reliability.
- **API Access**: Easily access the model through a REST API for seamless integration.
- **API Gateway**: Manages API calls, routing them to the appropriate Lambda functions.

## Installation
Follow these steps to set up the Dynamic Price Forecasting project:

1. **Clone this repository**:
```bash
git clone https://github.com/ananya868/Dynamic-Price-Forecasting-end-to-end-Deployed-in-AWS.git
```
```bash
cd dynamic-price-forecasting
```

2. **Set up AWS CLI**: Ensure you have the AWS CLI installed and configured with appropriate permissions.
aws configure


## Usage
You can directly inference the model via Api call using the syntax below.
1. **API Endpoints**
- The model can be accessed via the API endpoints provided by API Gateway. Below is an sample of how to use the API for predicting prices.

Request:
```bash
curl -X POST https://obued9cu2c.execute-api.ap-southeast-2.amazonaws.com/dpf -H "Content-Type: text/csv" -d '{
    "input1": 1.65859528,
    "input2": -1.02586385,
    "input3": -0.69664019,
    "input4": 2.53709666,
    "input5": -1.15203705,
    "input6": -0.45481393,
    "input7": 1.69453,
    "input8": 0.81721406,
    "input9": -0.08265266,
    "input10": 1.02387365,
    "input11": -1.1533949,
    "input12": -0.13231491,
    "input13": -1.51484614,
    "input14": -0.34883264,
    "input15": 1.07586572,
    "input16": -0.42082882
}'
```

Response:
```bash
{
  "predicted_price": 27.18 
}
```


2. **Using Python**
- You can use the following reference Python code to interact with the API:

```python
import requests

url = 'https://obued9cu2c.execute-api.ap-southeast-2.amazonaws.com/dpf'
payload = {
    'input1': value1,
    'input2': value2,
    '......
    # Add more features as needed
}

response = requests.post(url, json=payload)
print(response.json())
```

## Contributing
We welcome contributions from the community! Here’s how you can help:

- Fork the repository.
- Create a new branch (git checkout -b feature-branch).
- Make your changes and commit (git commit -am 'Add new feature').
- Push to the branch (git push origin feature-branch).
- Create a new Pull Request.

## License 🏷️
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact
For any inquiries or feedback, please contact us at:
Email: ananya8154@gmail.com  

### Acknowledgements
We would like to thank the following resources and communities for their support:
- AWS SageMaker for providing a robust platform for model training and deployment.
- [AWS Lambda](https://aws.amazon.com/lambda/) for seamless serverless computing.
- [API Gateway](https://aws.amazon.com/api-gateway/) for managing API integrations.
- [S3 Buckets](https://aws.amazon.com/s3/) for reliable and scalable storage.

Thank you for checking out the Dynamic Price Forecasting project! We hope this solution helps you optimize your pricing strategies effectively. 🌟

Feel free to customize the contact information, repository links, and any other specifics to better fit your project. If you have an architecture diagram, you can also update the placeholder in the Architecture section.
