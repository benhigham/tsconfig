# @benhigham/tsconfig

[![npm version](https://img.shields.io/npm/v/@benhigham/tsconfig.svg)](https://www.npmjs.com/package/@benhigham/tsconfig)
[![npm downloads](https://img.shields.io/npm/dm/@benhigham/tsconfig.svg)](https://www.npmjs.com/package/@benhigham/tsconfig)
[![License](https://img.shields.io/github/license/benhigham/tsconfig)](LICENSE.md)

My personal [TypeScript configurations](https://www.typescriptlang.org/docs/handbook/tsconfig-json.html) designed to provide consistent, strict, and production-ready settings across different project types. These opinionated configs balance type safety with developer experience, helping you avoid common pitfalls while maintaining compatibility with modern frameworks and libraries.

## Features

- Ready-to-use TypeScript configurations:
  - `@benhigham/tsconfig`: Base configuration for TypeScript projects
  - `@benhigham/tsconfig/browser`: Configuration optimized for browser environments
  - `@benhigham/tsconfig/astro`: Configuration for Astro framework projects
  - `@benhigham/tsconfig/next`: Configuration for Next.js projects
  - `@benhigham/tsconfig/react-app`: Configuration for React applications
  - `@benhigham/tsconfig/react-library`: Configuration for React libraries
  - `@benhigham/tsconfig/vite`: Configuration for Vite-based projects
- Sensible defaults to ensure type safety and consistent code quality
- Regularly updated to support the latest TypeScript features

## Installation

```bash
# npm
npm install --save-dev @benhigham/tsconfig

# yarn
yarn add --dev @benhigham/tsconfig

# pnpm
pnpm add --save-dev @benhigham/tsconfig
```

## Usage

### Basic Usage

Use in `tsconfig.json` by extending the desired configuration:

```jsonc
{
  "extends": "@benhigham/tsconfig",
  "compilerOptions": {
    "outDir": "dist",
    // your overrides here
  },
  "include": ["src"],
}
```

### Configuration Examples

#### Base Configuration

```jsonc
{
  "extends": "@benhigham/tsconfig",
  "compilerOptions": {
    "outDir": "dist",
  },
  "include": ["src"],
}
```

#### Browser Projects

```jsonc
{
  "extends": "@benhigham/tsconfig/browser",
  "compilerOptions": {
    "outDir": "dist",
  },
  "include": ["src"],
}
```

#### Astro Projects

```jsonc
{
  "extends": "@benhigham/tsconfig/astro",
  "include": ["src", ".astro/types.d.ts"],
}
```

#### Next.js Projects

```jsonc
{
  "extends": "@benhigham/tsconfig/next",
  "include": ["src", "next-env.d.ts"],
}
```

#### React Applications

```jsonc
{
  "extends": "@benhigham/tsconfig/react-app",
  "compilerOptions": {
    "outDir": "dist",
  },
  "include": ["src"],
}
```

#### React Libraries

```jsonc
{
  "extends": "@benhigham/tsconfig/react-library",
  "compilerOptions": {
    "outDir": "dist",
  },
  "include": ["src"],
}
```

#### Vite Projects

```jsonc
{
  "extends": "@benhigham/tsconfig/vite",
  "compilerOptions": {
    "types": ["vite/client"],
  },
  "include": ["src"],
}
```

## Requirements

- TypeScript 5.5.x or higher

## License

This project is licensed under the [MIT License](LICENSE.md).
