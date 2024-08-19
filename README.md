# OpenBullet xoxo.anom Configuration

## Overview

This repository contains the `xoxo.anom` configuration file for the OpenBullet anomaly tool. This configuration is designed to automate validation of user identities on the `stores.xoxoday.com` platform.

## Configuration Details

The `xoxo.anom` configuration includes the following components:

- **Settings**:
  - **Name**: `store xoxo`
  - **Version**: `1.4.1 [Anomaly]`
  - **Max Redirects**: 8
  - **Needs Proxies**: True

- **Script**:
  - **Request Type**: POST
  - **Endpoint**: `https://stores.xoxoday.com/chef/api/public/validateUserIdentity`
  - **Headers**: Custom headers to mimic a browser request
  - **Key Checks**: Validates responses to determine login success or failure

## Installation

To use this configuration with OpenBullet:

1. **Download OpenBullet**:
   - Follow the instructions on the [OpenBullet GitHub page](https://github.com/OpenBulletAnomaly/OpenBullet-Anomaly).

2. **Add Configuration**:
   - Place the `xoxo.anom` file in the appropriate configurations directory of OpenBullet.

3. **Setup Proxies**:
   - Ensure you have configured proxies if needed in OpenBullet settings.

## Usage

1. **Open OpenBullet**:
   - Launch OpenBullet and load the `xoxo.anom` configuration.

2. **Run the Script**:
   - Execute the script using OpenBullet's interface to test user credentials.

## Key Checks

The configuration uses specific key checks to handle responses:

- **Failure**: Detects if the email address or password is incorrect.
- **Success**: Detects successful login.
- **Retry**: Handles access denial due to Cloudflare restrictions.

## Legal

This configuration is provided for educational and testing purposes only. Use it responsibly and ensure that you comply with all applicable laws and terms of service for the target website. Unauthorized use of this tool to access accounts or systems without permission may be illegal and unethical. The authors of this configuration are not responsible for any misuse or legal consequences arising from its use.
