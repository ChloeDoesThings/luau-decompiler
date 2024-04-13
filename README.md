# luau-decompiler
## About
This repository holds files for ChloeRT's new Luau decompiler. This is made specifically for bytecode used by Roblox scripts.

## How does it work
It works by taking an input of Roblox Luau bytecode, and reading all of the information (such as instructions, constants, bytecode version, upvalues, etc.). Afterwards it is turned into readable Lua pcsedocode, which is close to what the actual source code would have looked like.

## How do I use it?
You may use the CLI (which is practically the same as Unluau's) to decompile bytecode. Here are some steps you could use to decompile a Roblox script using the CLI.

1. Write all the script bytecode to a file, you can do it like so:
`writefile(".\\", getscriptbytecode(SCRIPT_INSTANCE))`

2. Now that the file has been written to your workspace folder, now you can use the CLI. The encoding option is not required since it is automatically set to the 'Client' encoding. This is the command I personally use:
`LuauDecompiler.exe -o OUTPUT_FILE_PATH INPUT_FILE_PATH`

3. If the decompilation finished successfully, you should have your really cool looking decompiled results. Feel free to do whatever you want with it :D!
