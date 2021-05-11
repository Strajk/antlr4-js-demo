## Run

! This repo uses imports/exports for JavaScript modules -> it requires modern version of Node, such as 15 or higher

* `npm install`
* `npm run main` -> should print `(program (sourceElements (sourceElement (statement (variableStatement (variableDeclarationList (varModifier var) (variableDeclaration (assignable (identifier foo)) = (singleExpression (objectLiteral { (propertyAssignment (propertyName (identifierName (identifier bar))) : (singleExpression (literal (numericLiteral 42)))) })))) (eos <EOF>))))) <EOF>)`

## How this repo was initialized

* Install antlr
    * MacOS: `brew install antlr`
* Clone https://github.com/antlr/grammars-v4
* `cd »cloned-dir«/javascript/javascript`
* `antlr -Dlanguage=JavaScript -o gen *.g4` -> should create gen folder with 7 files
* copy 2 files from `»cloned-dir«/javascript/javascript/JavaScript/` to `gen/`
* `gen` folder now should have 9 files:
    * JavaScriptLexer.interp
    * JavaScriptLexer.js
    * JavaScriptLexer.tokens
    * JavaScriptLexerBase.js
    * JavaScriptParser.interp
    * JavaScriptParser.js
    * JavaScriptParser.tokens
    * JavaScriptParserBase.js
    * JavaScriptParserListener.js
* copy them to `grammars` folder in this repo

  

