# GnuCOBOL Extension

This extension contains GnuCOBOL language features that were part of the original bitlang.COBOL Extension.

This extension does not provide support for the COBOL language, so you will be required to use another extension to provide support for this.

This might sound odd but it does allow you to use one of the many COBOL extensions now available and use it with any combination of debuggers or code visualizers.

To summarize, this extension provides:
 - Problem matchers
 - A derived GnuCOBOL language that injects GnuCOBOL keywords into an existing COBOL syntax.

## Task: Single file compile using GnuCOBOL

The example below shows you how you can create a single task to compile one program using the `cobc` command.

This example is for GnuCOBOL 1-2.x, for GnuCOBOL use $gnucobol3-cob

```json
{
    "version": "2.0.0",
    "tasks": [
        {
            "label": "Compile: cobc (single file)",
            "type": "shell",
            "command": "cobc",
            "args": [
                "-fsyntax-only",
                "-I${workspaceFolder}\\CopyBooks",
                "-I${workspaceFolder}\\CopyBooks\\Public",
                "${file}"
            ],
            "problemMatcher" : "$gnucobol-cobc"
        }
    ]
}
```

## Task: Breakdown of problem matchers

| Product and Version                           | Tools                                                            | Problem matcher(s)                                                     |
|-----------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| GnuCOBOL 1-2                                  | *cobc*                                                           | $gnucobol-cobc                                                         |
| GnuCOBOL 3                                    | *cobc*                                                           | $gnucobol3-cobc                                                        |
| GnuCOBOL 3                                    | *cobc* for warnings/errors/notes                                 | $gnucobol3-warning-cobc + $gnucobol3-error-cobc + $gnucobol3-note-cobc |


## Online resources

- Online communities
   - [GnuCOBOL Community](https://sourceforge.net/p/gnucobol/discussion/)
 - Stack Overflow topics/tags:
   - [COBOL](https://stackoverflow.com/questions/tagged/cobol)
   - [GnuCOBOL](https://stackoverflow.com/questions/tagged/gnucobol)
 - [COBOL Programming Language Articles on Reddit](https://www.reddit.com/r/cobol/)
 - [Linkedin Learning COBOL Resources](https://www.linkedin.com/learning/topics/cobol)
- wikipedia
  - [COBOL](https://en.wikipedia.org/wiki/COBOL)
  - [CICS](https://en.wikipedia.org/wiki/CICS)

## Contributors

I would like to thank the follow contributors for providing patches, fixes, kind words of wisdom and enhancements.

 - Kevin Abel of Lincoln, NE, USA
 - Simon Sobisch of Germany
