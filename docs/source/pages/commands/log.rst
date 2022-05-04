.log
====

| `.log` writes an arbitrary message using CLImod's `Logger`.
| Logs saved this way have a severity of "Info" and are saved in `climod.log` and output to game chat.

Available overloads (variants)
+---------------+-------------------+--------------------------------+-----------------------------------------------------------------------------+
| Overload name | Argument count    | Syntax                         | Output                                                                      |
+===============+===================+================================+=============================================================================+
| log           | 1                 | .log <message>                 | "Logged", potentially accompanied by `Logger`'s error messages.              |
+---------------+-------------------+--------------------------------+-----------------------------------------------------------------------------+