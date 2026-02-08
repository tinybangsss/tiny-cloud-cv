#AWS ARCHITECTURE DOCUMENTATION 

Architecture Diagram – Sentence-Long Notes (Per Icon)
👤 End User (Web Browser)

The end user accesses the resume website through a standard web browser using a custom domain name.

🌐 Amazon Route 53 (DNS)

Amazon Route 53 routes the custom domain name to the CloudFront distribution using DNS resolution.

☁️ Amazon CloudFront (CDN & HTTPS)

Amazon CloudFront securely delivers the website over HTTPS and caches static content for low-latency access.

🪣 Amazon S3 (Static Website Hosting)

Amazon S3 hosts the static resume website files, including HTML, CSS, and JavaScript.

📄 HTML (Resume Content)

HTML defines the structure and content of the resume displayed on the website.

🎨 CSS (Styling)

CSS styles the resume to improve layout, readability, and visual presentation.

📜 JavaScript (Visitor Counter Logic)

JavaScript runs in the browser and calls the backend API to retrieve and display the visitor count.

🚪 Amazon API Gateway (REST API)

Amazon API Gateway exposes a REST endpoint that receives requests from the frontend JavaScript code.

⚙️ AWS Lambda (Python Backend)

AWS Lambda runs a Python function that processes API requests and updates the visitor count.

🐍 Python (boto3)

Python with the boto3 SDK is used in the Lambda function to interact with AWS services programmatically.

🗄️ Amazon DynamoDB (Database)

Amazon DynamoDB stores and retrieves the visitor count using a serverless, on-demand NoSQL table.

🔐 AWS IAM Role

An IAM role grants the Lambda function least-privilege permissions to access DynamoDB securely.

📊 Amazon CloudWatch (Monitoring & Logs)

Amazon CloudWatch captures logs and metrics for monitoring the Lambda function and troubleshooting issues.

🧱 AWS SAM (Infrastructure as Code)

AWS Serverless Application Model defines and deploys the backend infrastructure as code.

🗂️ GitHub Repository – Backend

The backend GitHub repository stores the Python code, SAM template, and automated tests.

🔁 GitHub Actions – Backend CI/CD

GitHub Actions automatically runs tests and deploys the serverless backend when code is pushed.

🗂️ GitHub Repository – Frontend

The frontend GitHub repository stores the HTML, CSS, and JavaScript source files for the website.

🔁 GitHub Actions – Frontend CI/CD

GitHub Actions automatically deploys updated frontend files to S3 and invalidates the CloudFront cache.

📝 Blog Post

A blog post linked from the resume explains key lessons learned while completing the Cloud Resume Challenge.
