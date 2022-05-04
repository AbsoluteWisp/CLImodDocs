Commands
========

| **dotcommands** are the commands invoked when using dotCLI.  
| They take the form of `.commandName <arg1> <arg2> [...]`  
| Arguments can be one of 3 types:  
| - Integers: If something starts with a number or the minus (-) sign, it's considered an integer and parsed as such.
| - Multi-word string: If something starts with the double quote (\") sign, it's considered a string and parsed as such.
| - Single-word string: If something doesn't match any of the criteria above, it's considered a one-word string (word) and parsed as such
| Each dotcommand declares its allowed argument counts. This allows for command overloading (one command doing different things with different arguments)

.. toctree::
   :caption: Dotcommands list
   
   commands/ping
   commands/dist2
   commands/dist3
   commands/coord
   commands/note
   commands/log