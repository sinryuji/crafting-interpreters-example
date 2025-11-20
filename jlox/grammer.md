```
expression      → ternary ;
ternary         → equality ( "?" expression ":" ternary )? ;
equality        → comparison ( ( "!=" | "==" ) comparison )* ;
comparsion      → term ( ( ">" | ">=" | "<" | "<=" ) term )* ;
term            → factor ( ( "-" | "+" ) factor )* ;
factor          → unary ( ( "/" | "*" ) unary )* ;
unary           → ( "!" | "-" ) unary
				| primary ;
primary         → NUMBER | STRING | "true" | "false" | "nil"
				| "(" expression ")" ;
```
