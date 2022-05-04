Get CLImod to the Launcher
==========================

Once you have your CLImod main directory set up, you'll need to configure a new Minecraft version for the Minecraft Launcher.

| In your `.minecraft/versions` folder, create a new subfolder and call it what you want your version to be named. I'll use "myVersionName"
| Copy your CLImod `.jar` to that folder.
| Copy the `version_name.json` file from the corresponding Minecraft release (like 1.18.2) next to the jar.
| Rename the JSON to your version's name ("myVersionName.json")
| Edit the JSON:
| - find the first occurence of "downloads" and remove the entire block. If you don't do this, Minecraft will redownload the vanilla jar (like 1.18.2.jar) in place of your modded version
| - find "id" and change it to your version's name ("myVersionName")
| - find the game launch arguments (beginning of the file) and add a new argument "--cliModDir" followed by the full path to the CLImod main directory. 
| In the end, the modified parts should look like this:

.. code-block::

   "arguments": {
      "game": [
         "--cliModDir",
         "C:\\Users\\You\\AppData\\Roaming\\.minecraft\\CLImod"
      ]
   },

   "assets": "1.18",
   "complianceLevel": 1,
   "id": "myVersionName"

| Open Minecraft Launcher and add a new profile. "myVersionName" should appear as an available version in the dropdown. Call the profile whatever you want and hit play!