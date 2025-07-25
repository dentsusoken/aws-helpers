# @vecrea/aws-helpers

A TypeScript library providing aws helper modules for OID4VC (OpenID for Verifiable Credentials) implementations.

## Features

- **DynamoDB Integration**: Simplified DynamoDB operations with Cloudflare Workers compatibility
- **TypeScript Support**: Full TypeScript support with comprehensive type definitions
- **Modular Design**: Import only what you need with subpath exports

## Installation

```bash
npm install @vecrea/aws-helpers
```

## Usage

### DynamoDB Module

Simplified DynamoDB operations with Cloudflare Workers compatibility.

```typescript
import { DynamoDB } from '@vecrea/aws-helpers/dynamodb';
import { DynamoDBDocumentClient } from '@aws-sdk/lib-dynamodb';

// Initialize
const client = new DynamoDBDocumentClient({ region: 'us-east-1' });
const dynamodb = new DynamoDB(client, 'your-table-name');

// Basic operations
await dynamodb.put('user:123', JSON.stringify({ name: 'John', age: 30 }));
const userData = await dynamodb.get('user:123');
await dynamodb.delete('user:123');
```

## API Reference

### DynamoDB

A class for simplified DynamoDB operations.

#### Constructor

```typescript
constructor(client: DynamoDBDocumentClient, tableName: string)
```

#### Methods

- `get(key: string): Promise<string | null>` - Retrieves a value by key
- `put(key: string, value: string, options?: PutOptions): Promise<void>` - Stores a value
- `delete(key: string): Promise<void>` - Deletes an item by key

#### Types

- `DynamoDBItem` - Interface for DynamoDB items
- `PutOptions` - Options for put operations, extending KVNamespacePutOptions

## Development

### Prerequisites

- Node.js 18+
- npm or yarn

### Setup

```bash
git clone <repository-url>
cd aws-helpers
npm install
```

### Scripts

- `npm run build` - Build the library
- `npm test` - Run tests

### Testing

The library uses Vitest for testing. Test files are located in `__tests__` directories alongside the source files.

```bash
npm test
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Run the test suite
6. Submit a pull request

## Support

For issues and questions, please use the GitHub issue tracker.
