# @esmkit/identifier-keyword-validator

a utility package for parsing JavaScript keywords and identifiers. It provides several helper functions for identifying valid identifier names and detecting reserved words and keywords.

## Installation

```bash
bun add @esmkit/identifier-keyword-validator
```

## Usage

```ts
import {
  isIdentifierName,
  isIdentifierStart,
  isIdentifierChar,
  isReservedWord,
  isStrictBindOnlyReservedWord,
  isStrictBindReservedWord,
  isStrictReservedWord,
  isKeyword,
} from "@esmkit/identifier-keyword-validator";
```

### isIdentifierName

```ts
function isIdentifierName(name: string): boolean
```

The isIdentifierName function checks whether a given string can be a valid identifier name. Note that it doesn't handle unicode escape sequences. For example, isIdentifierName("\\u0061") returns false while \u0061 could be an JavaScript identifier name (a).

## isIdentifierStart

```ts
function isIdentifierStart(codepoint: number): boolean
```

The isIdentifierStart function checks whether a given Unicode code point can start an identifier, as defined by the IdentifierStartChar.

## isIdentifierChar

```ts
function isIdentifierChar(codepoint: number): boolean
```

The isIdentifierChar function checks whether a given Unicode code point can be part of an identifier, as defined by the IdentifierPartChar.

## Keywords and Reserved words helpers

These helpers detect keyword and reserved words. For more information, see the implementation.

```ts
function isReservedWord(word: string, inModule: boolean): boolean
function isStrictReservedWord(word: string, inModule: boolean): boolean
function isStrictBindOnlyReservedWord(word: string): boolean
function isStrictBindReservedWord(word: string, inModule: boolean): boolean
function isKeyword(word: string): boolean
```

## License

MIT © BILLGO. See LICENSE for details.
