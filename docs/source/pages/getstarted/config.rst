Write a CLImod config file
==========================

Creating a CLImod main folder
-----------------------------
| To work properly, CLImod needs a folder for its files (like the configuration, or files that dotcommands use).
| Create a folder anywhere you have write access to on your computer. It's preferable to put it in `.minecraft`, where it won't bother you.

Writing CLImod config
---------------------
| Create a file in your CLImod main folder you created earlier, and call it "config.txt". This is the main file CLImod depends on, and it won't work without it.
| Entries in that file take the form of `keyName valueName`. Lines starting with `#` are ignored by the configuration parser in CLImod (comments)

Definitions of all `config.txt` keys

+----------------+--------------------------------------------------------------+
| Key            | Definition                                                   |
+================+==============================================================+
| prefix         | Single character all dotcommand invocations must start with  |
+----------------+--------------------------------------------------------------+
| logfilename    | The name of the file that Logger writes its logs to          |
+----------------+--------------------------------------------------------------+
| notefilename   | The name of the file .note notes are stored in               |
+----------------+--------------------------------------------------------------+
| coordfilename  | The name of the file .coord coords are stored in             |
+----------------+--------------------------------------------------------------+

Example `config.txt` file:

.. code-block::
   
   # CLImod configuration file
   # CLImod made with <3 Ghostling225

   ## Dotcommands
   prefix .

   # .log
   logfilename climod.log

   # .note
   notefilename notes.txt

   # .coord
   coordfilename coords.txt

That's it! Keep in mind extensions to CLImod might require additional config entries.