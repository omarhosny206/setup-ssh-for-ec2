# Release v1.0.0 - Initial Release

🎉 We are excited to announce the initial release of the "Set up SSH for EC2" GitHub Action! This action simplifies the process of setting up SSH for connecting to an EC2 instance.

## Key Features:
- SSH Configuration:
    - Automatically configures SSH settings based on provided private key and EC2 instance URL.
    
## How to Use:
- In your workflow, use the Set up SSH for EC2 action.
- Provide the required input parameters:
   - EC2_SSH_PRIVATE_KEY: The private key of EC2 instance for SSH connection.
   - EC2_URL: The URL of the EC2 instance.

## Usage:
```yaml
name: SSH Setup Workflow

on:
  push:
    branches:
      - master

jobs:
  setup-ssh:
    runs-on: ubuntu-latest
    steps:
    - name: Setup SSH for EC2
      uses: omarhosny206/setup-ssh-for-ec2@v1.0.0
      with:
        EC2_SSH_PRIVATE_KEY: ${{ secrets.EC2_SSH_PRIVATE_KEY }}
        EC2_URL: ${{ secrets.EC2_URL }}
```
