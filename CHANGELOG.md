# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [x.x.x] - 2025-xx-xx

### Added

- Initial release of @vecrea/aws-helpers
- **DynamoDB Module**: Simplified DynamoDB operations
  - `DynamoDB` class with basic CRUD operations (get, put, delete)
  - Cloudflare Workers compatibility
  - TTL (Time To Live) support
- **TypeScript Support**: Full TypeScript support with comprehensive type definitions
- **Modular Design**: Subpath exports for selective imports
  - Main export: `@vecrea/aws-helpers`
  - DynamoDB: `@vecrea/aws-helpers/dynamodb`
- **Build System**: Vite-based build with ES modules and CommonJS support
- **Testing**: Vitest-based test suite

### Technical Details

- ES Module and CommonJS dual package support
- TypeScript declaration files (.d.ts) for all modules
- External dependency on @aws-sdk/lib-dynamodb
- Node.js polyfills for Cloudflare Workers compatibility
