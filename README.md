# Repro guide

```
git clone https://github.com/sorgloomer/prepair-require-extension-vue-report.git
cd prepair-require-extension-vue-report
npm ci
npm test
```


# Error stack

```
$ npm test

> test
> node src/index.js

C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\core\lib\parser\index.js:74
    throw err;
    ^

SyntaxError: C:\workspace\prepair-require-extension-vue-report\src\component.vue: Missing semicolon. (12:2)

  10 | }
  11 |
> 12 | }));
     |   ^
    at toParseError (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\parse-error.ts:95:45)
    at TypeScriptParserMixin.raise (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\tokenizer\index.ts:1496:19)
    at TypeScriptParserMixin.semicolon (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\parser\util.ts:149:10)
    at TypeScriptParserMixin.parseExportDefaultExpression (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\parser\statement.ts:2553:10)
    at TypeScriptParserMixin.parseExportDefaultExpression (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\plugins\typescript\index.ts:2859:20)
    at TypeScriptParserMixin.parseExport (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\parser\statement.ts:2396:25)
    at TypeScriptParserMixin.parseExport (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\plugins\typescript\index.ts:2829:22)
    at TypeScriptParserMixin.parseStatementContent (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\parser\statement.ts:596:25)
    at TypeScriptParserMixin.parseStatementContent (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\plugins\typescript\index.ts:2917:20)
    at TypeScriptParserMixin.parseStatementLike (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\parser\statement.ts:426:17)
    at TypeScriptParserMixin.parseModuleItem (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\parser\statement.ts:363:17)
    at TypeScriptParserMixin.parseBlockOrModuleBlockBody (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\parser\statement.ts:1395:16)
    at TypeScriptParserMixin.parseBlockBody (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\parser\statement.ts:1369:10)
    at TypeScriptParserMixin.parseProgram (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\parser\statement.ts:217:10)
    at TypeScriptParserMixin.parseTopLevel (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\parser\statement.ts:199:25)
    at TypeScriptParserMixin.parse (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\parser\index.ts:46:10)
    at TypeScriptParserMixin.parse (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\plugins\typescript\index.ts:4036:20)
    at parse (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\parser\src\index.ts:65:38)
    at parser (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\core\src\parser\index.ts:28:19)
    at parser.next (<anonymous>)
    at normalizeFile (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\core\src\transformation\normalize-file.ts:50:24)
    at normalizeFile.next (<anonymous>)
    at run (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\core\src\transformation\index.ts:39:36)
    at run.next (<anonymous>)
    at transform (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\core\src\transform.ts:29:20)
    at transform.next (<anonymous>)
    at evaluateSync (C:\workspace\prepair-require-extension-vue-report\node_modules\gensync\index.js:251:28)
    at fn (C:\workspace\prepair-require-extension-vue-report\node_modules\gensync\index.js:89:14)
    at stopHiding - secret - don't use this - v1 (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\core\src\errors\rewrite-stack-trace.ts:99:14)
    at transformSync (C:\workspace\prepair-require-extension-vue-report\node_modules\@babel\core\src\transform.ts:66:52)
    at babelTransform (C:\workspace\prepair-require-extension-vue-report\node_modules\@prepair\require-extension-vue\src\vue2\compile.js:314:10)
    at processScriptBlock (C:\workspace\prepair-require-extension-vue-report\node_modules\@prepair\require-extension-vue\src\vue2\compile.js:160:23)
    at compile (C:\workspace\prepair-require-extension-vue-report\node_modules\@prepair\require-extension-vue\src\vue2\compile.js:82:58)
    at compileHook (C:\workspace\prepair-require-extension-vue-report\node_modules\@prepair\require-extension-vue\src\compile-hook.js:45:9)
    at Module._compile (C:\workspace\prepair-require-extension-vue-report\node_modules\pirates\lib\index.js:113:29)
    at Module._extensions..js (node:internal/modules/cjs/loader:1548:10)
    at Object.newLoader [as .vue] (C:\workspace\prepair-require-extension-vue-report\node_modules\pirates\lib\index.js:121:7)
    at Module.load (node:internal/modules/cjs/loader:1288:32)
    at Function.Module._load (node:internal/modules/cjs/loader:1104:12)
    at Module.require (node:internal/modules/cjs/loader:1311:19)
    at require (node:internal/modules/helpers:179:18)
    at Object.<anonymous> (C:\workspace\prepair-require-extension-vue-report\src\index.js:5:1)
    at Module._compile (node:internal/modules/cjs/loader:1469:14)
    at Object.Module._extensions..js (node:internal/modules/cjs/loader:1548:10)
    at Module.load (node:internal/modules/cjs/loader:1288:32)
    at Function.Module._load (node:internal/modules/cjs/loader:1104:12)
    at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:174:12)
    at node:internal/main/run_main_module:28:49 {
  code: 'BABEL_PARSE_ERROR',
  reasonCode: 'MissingSemicolon',
  loc: Position { line: 12, column: 2, index: 232 },
  pos: 232,
  syntaxPlugin: undefined
}

Node.js v20.17.0
```
