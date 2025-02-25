# Bedrock Demo CLI

A simple command-line interface for demonstrating AWS Bedrock capabilities, particularly focused on interacting with Claude 3 Sonnet.

## Prerequisites

- Ruby
- AWS CLI configured with SSO access
- AWS account with Bedrock access

## Installation

1. Clone this repository
2. Install dependencies:

```bash
bundle install
```

## Setup

Ensure you have AWS SSO configured. If you haven't logged in recently, run:

```bash
aws sso login
```

## Usage

The CLI currently supports the following commands:

### Hello Command

Test your Bedrock connection with a simple completion using Claude 3 Sonnet:

```bash
❯ ./bin/bedrock-demo hello
Greetings, terrestrial orb of diverse life forms!
```

This command will:
1. Verify your AWS SSO session
2. Connect to Bedrock
3. Generate an interesting variation of "hello, world!" using Claude 3 Sonnet
4. Stream the response to your terminal

If your SSO session has expired, the tool will automatically attempt to refresh it.

## Error Handling

The tool includes built-in error handling for:
- Expired SSO sessions (with automatic renewal attempt)
- Bedrock service errors

## Dependencies

- thor
- aws-sdk-bedrockruntime
- aws-sdk-bedrock