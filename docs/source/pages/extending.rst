Extending CLImod
================

While not designed with modding in mind, CLImod can be extended to add new dotcommands with relative ease.

Procedure
---------
| 1. Decompile and deobfuscate Minecraft (for example with `MCP-Reborn <https://github.com/Hexeption/MCP-Reborn>`_)
| 2. Create a new class extending `DotCommand` from `mod.ghostling.climod.dotcli`. It has to have a constructor with no arguments settings its name and argument counts, and a `RunCommand(Object[] args)` method returning a `String`.
| 3. Somewhere in your code, you should call `mod.ghostling.climod.dotcli.ModManager.nameCommandMap.put(new YourClass().name, new YourClass())`.
| 4. Done! After the code from step 3 is executed, your command will be recognized for use!

More detailed guide
-------------------
| To add a new dotCLI dotcommand to CLImod, you'll need a decompiled version of the client first.
| You can achieve this by decompiling the CLImod `.jar` and using something like the `MCP-Reborn project <https://github.com/Hexeption/MCP-Reborn>`_ to get Minecraft's deobfuscated source code.
| Then, you'll want to create a Java class for your command. Create a package for your commands to live in and create a class for your command inside it.
| All dotcommands must extend the base `DotCommand` class defined in CLImod. All dotcommands need to have a constructor where they define their name (`String`) and their allowed argument counts. They should also have a public method `RunCommand(Object[] args)` returning a `String`.
| When you're finished, it should look something like this:

.. code-block::

   public class MyDotCommand extends mod.ghostling.climod.dotcli.DotCommand {
       public MyDotCommand() {
           this.name = "mydotcommand"; // Will be called as .mydotcommand
           this.argCounts = new int[]{0, 1, 2}; // Will accept either 0, 1, or 2 arguments
       }
       
       public String RunCommand(Object[] args) {
           // This gets executed when the command is called.
       }
   }

| Somewhere in your code, you should then call `mod.ghostling.climod.dotcli.ModManager.nameCommandMap.put(new MyDotCommand().name, new MyDotCommand())`. This makes CLImod recognize your new dotcommand.
| Done! Compile your game into a jar (MCP-Reborn has steps for this in their README) and enjoy your new command!