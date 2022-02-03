---
page_type: sample
languages:
- csharp
- .Net 5
products:
- azure
- azure-communication-services
---

Deploy to Azure using instructions [here](./docs/deployment-guides/deploy-and-test-sample-on-azure.md).

# Azure Communication Services Solutions - Authentication Server Sample

[![CI](https://github.com/Azure-Samples/communication-services-authentication-hero-csharp/actions/workflows/ci.yml/badge.svg)](https://github.com/Azure-Samples/communication-services-authentication-hero-csharp/actions/workflows/ci.yml)
[![CodeQL](https://github.com/Azure-Samples/communication-services-authentication-hero-csharp/actions/workflows/codeql-analysis.yml/badge.svg)](https://github.com/Azure-Samples/communication-services-authentication-hero-csharp/actions/workflows/codeql-analysis.yml)
[![C#](https://img.shields.io/badge/%3C%2F%3E-C%23-blue)](https://dotnet.microsoft.com/en-us/languages/csharp)
[![.Net 5.0](https://img.shields.io/badge/%3C%2F%3E-.Net5.0-%230074c1.svg)](https://dotnet.microsoft.com/en-us/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

1. [Overview](#overview)
2. [Getting Started](#getting-started)
3. [Endpoints](#endpoints)
4. [Code Structure](#code-structure)
5. [Troubleshooting](#troubleshooting)
6. [Known Issues](#known-issues)
7. [Contributing](#contributing)
8. [Resources](#resources)
9. [Trademark](#trademark)
10. [License](#license)

## Overview

In order to properly implement a secure Azure Communication Services solutions, developers must start by putting in place the correct infrastructure to properly generate user and access token credentials for Azure Communication Services. Azure Communication Services is identity-agnostic, to learn more check out our [conceptual documentation](https://docs.microsoft.com/azure/communication-services/concepts/identity-model).

This repository provides a sample of a server implementation of an authentication service for Azure Communication Services. It uses best practices to build a trusted backend service that issues Azure Communication Services credentials and maps them to Azure Active Directory identities. 

This sample can help you in the following scenarios:
1. As a developer, you need to enable an authentication flow for joining native Azure Communication Services and/or Teams Interop calling/chat which is done by mapping an Azure Communication Services identity to an Azure Active Directory identity and using this same Azure Communication Services identity for the user to fetch an Azure Communication Services token in every session.
2. As a developer, you need to enable an authentication flow for Custom Teams Endpoint which is done by using an M365 Azure Active Directory identity of a Teams' user to fetch an Azure Communication Services token to be able to join Teams calling/chat.

If you are looking to get started with Azure Communication Services, but are still in learning / prototyping phases, check out our [quickstarts for getting started with azure communication services users and access tokens](https://docs.microsoft.com/en-us/azure/communication-services/quickstarts/access-tokens?pivots=programming-language-csharp).

> :loudspeaker: An Azure Communication Services Solutions - Authentication Sample (NodeJS version) can be found [here](https://github.com/Azure-Samples/communication-services-authentication-hero-nodejs).

![Azure Communication Services Authentication Server Sample Overview Flow](docs/images/ACS-Authentication-Server-Sample_Overview-Flow.png)

Additional documentation for this sample can be found on [Microsoft Docs](https://docs.microsoft.com/azure/communication-services/samples/calling-hero-sample). !!! TODO: change link?

Since this sample only focuses on the server APIs, the client application is not part of it. If you want to add the client application to login user using Azure Active Directory, then please follow the MSAL samples [here](https://github.com/AzureAD/microsoft-authentication-library-for-js).

Before contributing to this sample, please read our [contribution guidelines](./CONTRIBUTING.md).

## Getting Started

If you're wondering where to get started, here are a few scenarios to help you get going:

* "How does the Azure Communication Services Authentication server sample work?"
  * Take a look at our conceptual documentation on:
    - [Azure Communication Services Authentication Server Sample Architecture Design](./docs/design-guides/architecture-overview.md).
    - [Secured Web API Architecture Design](./docs/design-guides/secured-web-api-design.md).
    - [Identity Mapping Architecture Design](./docs/design-guides/identity-mapping-design-graph-open-extensions.md).
    - [Azure Active Directory Token Exchange Architecture Design](). !!! TODO: add link
* "I want to see what this Azure Communication Services Authentication Server sample can do by running it!"
  * Check out our [local deployment guide](<docs/deployment-guides/deploy-locally>) guide.
* "I want to submit a fix or a feature for this project"
  * Check out our [contribution guidelines](CONTRIBUTING.md) first.
  * Check out the following guides in sequence after coding.
    * [Test Your Changes](<docs/contribution-guides/2. test-your-changes.md>)
    * [Write Unit Tests](<docs/contribution-guides/3. write-unit-tests.md>)
    * [Submit a PR](<docs/contribution-guides/4. submit-a-pr.md>)
    * [Publish Your Changes](<docs/contribution-guides/5. publish-your-changes.md>)

## Endpoints

This Azure Communication Services Solutions - Authentication server sample provides responses for **user** and **token** endpoints. For more details, please check our [Endpoints and Responses designe doc](./docs/design-guides/endpoints-and-responses.md).

## Troubleshooting

Coming soon...

!!! TODO

## Known Issues

- ...

## Contributing

Join us by making a contribution. To get you started check out our [contribution guidelines](CONTRIBUTING.md).

We look forward to building an amazing open source Azure Communication Services Authentication server sample with you!

## Resources

- [Azure Communication Services Documentation](https://docs.microsoft.com/en-us/azure/communication-services/) - Find more about how to add voice, video, chat, and telephony on our official documentation.
- [Azure Communication Services Hero Samples](https://docs.microsoft.com/en-us/azure/communication-services/samples/overview) - Find more Azure Communication Services samples and examples on our samples overview page.
- [On-Behalf-Of workflow](https://docs.microsoft.com/en-us/azure/active-directory/develop/v2-oauth2-on-behalf-of-flow) - Find more about the OBO workflow
- [Creating a protected API](https://github.com/Azure-Samples/active-directory-dotnet-native-aspnetcore-v2/tree/master/2.%20Web%20API%20now%20calls%20Microsoft%20Graph) - Detailed example of creating a protected API

## Trademark

**Trademarks** This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft trademarks or logos is subject to and must follow [Microsoft’s Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general). Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship. Any use of third-party trademarks or logos are subject to those third-party’s policies.

## License

[MIT](LICENSE.md)
