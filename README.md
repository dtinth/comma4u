# comma4u

A little library that helps you insert commas in JavaScript code!


## Rough ideas

- This library should be triggered when inserting text in a blank line, or removing the only non-whitespace character in a line.

- When inserting text into a blank line…

  - The previous line must end with an identifier name, number, or `]`, `)`, `>`, `'`, `"`, `\``.

  - The next line must begin with `]`, `}`, or `)`.
  
  - The inserted character must be an identifier, number, or `[`, `(`, `<`, `'`, `"`, `\``

  - Use a very simple algorithm to determine the current state of code…

  - If the result is “object literal,” “array literal,” or “parens” insert a comma on the previous line.

- When removing the only character from a line…

  - The previous line must end with `,`.

  - The next line must begin with `]`, `}`, or `)`.
  
  - Use a very simple algorithm to determine the current state of code…

  - If the result is “object literal,” “array literal,” or “parens” remove a comma on the previous line.
