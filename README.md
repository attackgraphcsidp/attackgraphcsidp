# Attack Graph Model PBI Report

## Overview

This repository contains the Power BI file for the Crowdstrike Attack Graphs visualisation. To implement the report in your environent, follow the steps below.

## Table of Contents

- [Overview](#overview)
- [Getting Started](#getting-started)
- [Prerequisites](#prerequisites)
- [API Token](#api-token)

## Getting Started

To get started with the Power BI report, follow these steps:

1. Clone/Download the repository:
    ```bash
    git clone https://github.com/attackgraphcsidp/attackgraphcsidp.git
    ```
2. Open the `Crowdstrike IDP Attack Graph.pbit` file located in the repository.

## Prerequisites

Ensure you have the following tools installed:

- [Power BI Desktop](https://powerbi.microsoft.com/desktop/): For viewing and editing the `Crowdstrike IDP Attack Graph.pbit` report file.
- Crowdstrike API Token: You will need to create a new API Token to allow access to the attack path data.

## API Token

Create a new API token in your Falcon Platform with the following permissions:

- Identity Protection Entities (Read)
- Identity Protection GraphQL (Write)

## Storing the secret

Since Power Bi doesn't provide an easy way to store API Credentials for custom API calls (Web.Content), to make the report easy to share and quickly use the API credentials are stored in a parameter in the report. As this leaves the credentials in plain text in the PBIX file, its not recommended to publish the report while using this method. Some other ways the secret could be stored are:

- Locked down Azure Storage Container
- Azure KeyVault (see: https://www.bibb.pro/post/securing-your-api-power-bi-data-with-azure-key-vault#:~:text=Using%20Azure%20Key%20Vault%20in,via%20Power%20BI%20M%20Code) ~ Requires On-Prem Gateway
- Locked down sharepoint file containing the secret

