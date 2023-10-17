# google-calendar-proxy-lambda

## Requirements
- `node` 18

## Variables
- `aws_region`: AWS Region to deploy in
- `client_email`: Google Calendar API Client Email
- `private_key`: Private Key for accessing Google Calendar API
- `proxy_lambda_access_token`: Access Token required to invoke the Lambda
- `hash_secret`: Secret for hashing data
- `allowed_email_domains`: Email domains allowed that will not be hashed

## Output
- `google_calendar_proxy_lambda_id`: ID of Google Calendar Lambda Created
- `google_calendar_proxy_lambda_api_endpoint`: API Endpoint to Invoke Google Calendar Lambda

## Usage
```terraform
module "attuned_google_calendar_proxy_lambda" {
  source = "git@github.com:Attuned-Corp/google-calendar-proxy-lambda.git?ref=(ref)"

  aws_region                = "us-west-2"
  client_email              = "example@example.com"
  private_key               = "-----BEGIN PRIVATE KEY-----..."
  proxy_lambda_access_token = "mP8er6zziP"
  hash_secret               = "Q7ApA0hNOP"
  allowed_email_domains     = ["example.com"]
}
```
