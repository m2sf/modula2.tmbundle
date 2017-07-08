## Supported Modula-2 Dialects ##

This TextMate bundle supports separate dialect modes for the following Modula-2 dialects:

* PIM Modula-2
* ISO Modula-2
* Modula-2 R10


## Dialect Tags ##

Thebundle auto-selects the dialect mode by recognising Modula-2 dialect tags. A Modula-2 dialect tag is a comment with embedded dialect information.
Such Modula-2 dialect tags are supported across multiple utilities and frameworks, for example the Pygments rendering framework. 

However, the bundle will only recognise a Modula-2 dialect tag in the first line of a Modula-2 source file.

The general syntax of a Modula-2 dialect tags is as follows:

```
dialectTag :=
  '(*!' dialectIdent langExtensionIdent? '*)'
  ;

dialectIdent :=
  'm2pim' | 'm2iso' | 'm2r10'
  ;

langExtensionIdent :=
  '+' letter ( letter | digit )*
  ;
```

The bundle will ignore any language extension info.

For best results, put one of the following tags at the very beginning of your Modula-2 source file:

* `(*!m2pim*)` for source files written for PIM Modula-2
* `(*!m2iso*)` for source files written for ISO Modula-2
* `(*!m2r10*)` for source files written for Modula-2 R10
