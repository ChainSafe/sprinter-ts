---
sidebar_position: 1
---

# Introduction

Welcome to the Sprinter SDK documentation! The Sprinter SDK is a powerful tool designed to simplify cross-chain balance aggregation and transaction management, allowing your customers to seamlessly interact with multiple blockchain networks.

## Getting Started

Depending on your needs, you have two main options for using the Sprinter SDK:

1. **Using the SDK (Recommended for TypeScript and Web Framework Developers)**
2. **Calling APIs Directly**

### Using the SDK

Using the Sprinter SDK provides a convenient and unified interface for blockchain interactions, complete with TypeScript support for enhanced type safety and a better development experience. This approach is particularly recommended for developers working with TypeScript or popular web frameworks.

#### Quick Example

Here's a quick example of how to use the SDK in your project:

```typescript
import { Sprinter } from '@chainsafe/sprinter-sdk';

const sprinter = new Sprinter(window.ethereum);

sprinter.getUserBalances().then(console.log);
```

For a more detailed guide on setting up and using the SDK, refer to the [SDK Documentation](sdk/overview.md).

### Calling API Endpoints Directly

If you prefer more control or wish to implement the solution in a different programming language, you can directly interact with the API endpoints provided by Sprinter.

#### Quick Example

Here’s how you can call the API directly using JavaScript's Fetch API:

```javascript
const ownerAddress = "0x3E101Ec02e7A48D16DADE204C96bFF842E7E2519";
const tokenSymbol = "USDC";
const baseUrl = "https://your-api-url.com";  // Replace with your API base URL

fetch(`${baseUrl}/accounts/${ownerAddress}/assets/fungible/${tokenSymbol}`)
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error fetching user fungible tokens:', error));
```

For a comprehensive list of available endpoints and how to use them, check out the [API Documentation](api/get-started.md).

## Next Steps

- If you're new to Sprinter SDK, start with our [Getting Started Guide](get-started.md).
- For an in-depth understanding, read the [Introduction to Sprinter SDK](introduction.md).
- Explore detailed examples and advanced usage in the [SDK Documentation](sdk/overview.md).
- Dive into the specifics of our API in the [API Documentation](api/get-started.md).

We hope you find the Sprinter SDK easy to use and integrate into your projects. Happy coding!