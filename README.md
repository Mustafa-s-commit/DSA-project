# Expression Lab

Expression Lab is an interactive data structures and algorithms visualizer for converting mathematical expressions between infix, postfix, and prefix notation. It demonstrates Shunting-Yard and stack-based conversion algorithms step by step.

## Features

- Convert infix expressions to postfix notation with the Shunting-Yard algorithm.
- Convert postfix and prefix expressions to infix notation.
- Visualize stack operations and each conversion step.
- Step backward, step forward, or play through an animation.
- Validate expressions and show helpful parsing errors.
- Choose from built-in example expressions.
- View operator precedence and associativity for infix conversions.
- Responsive interface for desktop and mobile devices.

## Supported Operators

| Operator | Description |
| --- | --- |
| `+` | Addition |
| `-` | Subtraction |
| `*` | Multiplication |
| `/` | Division |
| `^` | Exponentiation |

Exponentiation uses right associativity. Parentheses are supported for infix expressions.

## Getting Started

### Prerequisites

- Node.js 20 or newer
- npm

### Installation

```bash
npm install
```

### Development

```bash
npm run dev
```

Open the local URL printed by Vite, usually `http://localhost:5173`.

### Production Build

```bash
npm run build
npm run preview
```

### Lint

```bash
npm run lint
```

## Example Expressions

| Conversion | Example |
| --- | --- |
| Infix to postfix | `A+B*C` |
| Infix to postfix | `(A+B)*C` |
| Postfix to infix | `AB+C*` |
| Prefix to infix | `*+ABC` |

## Available Routes

| Route | Purpose |
| --- | --- |
| `/` | Landing page |
| `/postfix` | Convert infix expressions to postfix |
| `/infix` | Convert postfix or prefix expressions to infix |
| `/about` | Learn how the conversion algorithms work |

## Project Structure

```text
src/
├── components/
│   ├── landing/       # Landing page visuals
│   ├── layout/        # Navigation and application shell
│   └── workspace/     # Inputs, controls, stack and step visualizations
├── engine/
│   ├── infixToPostfix.ts
│   ├── postfixToInfix.ts
│   ├── prefixToInfix.ts
│   ├── tokenizer.ts
│   ├── validators.ts
│   └── operators.ts
├── hooks/
│   └── useAlgorithmPlayer.ts
├── pages/
│   ├── LandingPage.tsx
│   ├── InfixPage.tsx
│   ├── PostfixPage.tsx
│   └── AboutPage.tsx
├── App.tsx
└── main.tsx
```

## Technology Stack

- React 19
- TypeScript
- Vite
- React Router
- Framer Motion
- Lucide React
- Tailwind CSS
- Oxlint
