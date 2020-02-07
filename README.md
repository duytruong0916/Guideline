# Guideline
# Frontend Coding Style Guidelines

Programming languages are designed for humans to read, and humans are imperfect. Many bugs are caused by human error, and we simply cannot help it. However, by enforcing strict coding standards, we can ensure that syntax does not get in our way. It lets us focus on what our code does rather than syntax.

Writing clean code is an act of courtesy between developers. Keep in mind that the code you write will be read by another human.

## Git

- One commit should only change one thing or serve one purpose
- Start your commit header with a present-tense verb, followed by a predicate

## Naming Guidelines

### Rules

- **ALWAYS** use PascalCasing for classes, interfaces, and React components.
- **ALWAYS** use camelCasing for functions, fields, parameters, and local declarations.
- **ALWAYS** use UPPER_SNAKE_CASE for global constants
- **NEVER** lead an identifier with an underscore. JavaScript symbols are not exported by default, so leading underscores are redundant.

| Identifier         | Convention       | Example                            | Notes               |
|-------------------|------------------|------------------------------------|---------------------|
| Class             | PascalCase       | `class MyClass`                    |                     |
| Interface         | PascalCase       | `interface MyInterface`            | For TypeScript only |
| Function          | camelCase        | `function myFunction`              |                     |
| Field             | camelCase        | `myField`                          |                     |
| Static Field      | camelCase        | `static myStaticField`             |                     |
| Parameter         | camelCase        | `function myFunction(myParameter)` |                     |
| Local Variable    | camelCase        | `let myVariable = props.value`     |                     |
| Local Constant    | camelCase        | `const myConstant = props.value`   |                     |
| Global Constant   | UPPER_SNAKE_CASE | `const STATE_READY = 0`            |                     |
| *React Component* | PascalCase       | `function MyComponent(props)`      | For React only      |

### Capitalization Rules for Compound Words

- **ALWAYS** capitalize each word in open-form compound words
- **NEVER** capitalize each word in closed-form compound words

Examples:

| Good      | Bad       |
|-----------|-----------|
| Baseball  | BaseBall  |
| FileName  | Filename  |
| MeetUp    | Meetup    |
| Minecraft | MineCraft |
| Workshop  | WorkShop  |

### Word Choice

- Identifiers **MUST** read well out loud. For example, use `earlyBirdPrice` rather than `priceEarlyBird`
- **NEVER** use underscores
- **NEVER** use reserved keywords (e.g. "type")

### Abbreviations and Acronyms

- **NEVER** use abbreviations in a public API. For example, use `profileImage` over `profileImg`
- **ONLY** use well-known acronyms **UNLESS** the identifier becomes too long

## Whitespace

- **Always** use 4 spaces for indentation
- **Always** indent your code consistently
- **Do not** keep indents on empty lines
- One space **must** precede the opening parenthesis of a control statement

```javascript
// OK.
if (foo === bar) {}

// Not OK.
if(foo === bar) {}
```

- One space **must** precede and succeed a binary or ternary operator

```javascript
// OK.
PI * radius * radius

// Not OK.
PI*radius*radius

// Not OK.
PI *radius*radius
```

- There should be **no space** around a unary operator
- One space **must** precede the opening brace of a control block

```javascript
// OK.
if (foo === bar) {
    // ...
}

// Not OK.
if (foo === bar){
    // ...
}
```

- One space **must** succeed a comma

```javascript
// OK.
fetchJson('GET', '/api/me/');

// Not OK.
fetchJson('GET','/api/me/');
```

## Layout

- Write only one statement per line

- Write only one declaration per line

- **Always** leave an empty line between declarations

```javascript
// OK.
import React from 'react';
import {Button, Col, Row} from 'react-bootstrap';
import {FaCalendar, FaUser} from 'react-icons/fa';
import 'styles.scss';

function MyComponent(props) {
    // ...
}

function MyOtherComponent(props) {
    // ...
}

// Not OK.
import React from 'react';
import {Button, Col, Row} from 'react-bootstrap';
import {FaCalendar, FaUser} from 'react-icons/fa';
import 'styles.scss';
function MyComponent(props) {
    // ...
}
function MyOtherComponent(props) {
    // ...
}
```

- There may be **no more than one** consecutive empty lines

```javascript
// OK.
import React from 'react';

function MyComponent(props) {
    // ...
}

// Not OK.
import React from 'react';


function MyComponent(props) {
    // ...
}
```

- **ALWAYS** Place opening braces at the end of a line.

```javascript
// OK.
if (foo === bar) {
    // ...
}

// Not OK.
if (foo === bar)
{
    // ...
}

// OK.
return {
    name: 'John Smith',
    email: 'johnsmith@example.com',
};

// Not OK, and will result in unexpected behavior due to JavaScript's automatic semicolon insertion.
return
{
    name: 'John Smith',
    email: 'johnsmith@example.com',
};
```

- **ALWAYS** place chained block statements on new lines.

```javascript
// OK.
if (foo === bar) {
    // ...
}
else if (bar === tar) {
    // ...
}
else {
    // ...
}

// Not OK.
if (foo === bar) {
    // ...
} else if (bar === tar) {
    // ...
} else {
    // ...
}
```

- **ALWAYS** use brace blocks with statements.

```javascript
// OK.
if (foo === bar) {
    // ...
}
else if (bar === tar) {
    // ...
}
else {
    // ...
}

// Not OK.
if (foo === bar)
    // ...
else if (bar === tar)
    // ...
else
    // ...
```

## Comments

- Place comments on separate lines, not at the end of lines
- Begin the comment with an uppercase letter
- End the comment text with a period
- One space must succeed the comment delimiter. For example, use `// My comment.` over `//My comment`

## Punctuation

- **ALWAYS** use single-quote string literals in JavaScript
- **ALWAYS** use double-quote string literals in JSX tags
- **ALWAYS** add a trailing comma in multiline JSON objects

## Declarations

- **Prefer** nominal function declarations over arrow functions **unless** the function is no more than a single return statement.
- **Avoid** object deconstruction in parameter lists. This can obfuscate otherwise readable code.
