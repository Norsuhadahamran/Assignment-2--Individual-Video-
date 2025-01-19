# Assignment-2-Individual-Video-

# How to Setup MASM and Irvine Library in Visual Studio | Setup Irvine Library | Visual Studio

# What is Visual Studio
Microsoft's Visual Studio is an integrated development environment (IDE) used for creating computer programs, including websites, web apps, web services, and mobile apps. It uses Microsoft software development platforms like Windows API, Windows Forms, WPF, Microsoft Store, and Silverlight. It includes a code editor, integrated debugger, code profiler, and other built-in tools. Visual Studio supports 36 programming languages, including C, C++, C++/CLI, Visual Basic.NET, C#, F#, JavaScript, TypeScript, XML, XSLT, HTML, and CSS. Additional languages like Python, Ruby, Node.js, and M are available via plug-ins. Visual Studio 2022 is currently production-ready.

# Step by Step to Setup MASM and Irvine Library in Visual Studio | Setup Irvine Library

**1. Download and Prepare the Irvine32 Library**

* **Download:** Get the Irvine32 library from GitHub .
* **Extract:** Unzip the downloaded file. You'll find `Irvine32.inc`, `Irvine32.lib`, and some example code.
* **Organize:** Create a folder (e.g., `C:\Irvine`) and place the `Irvine32.inc` and `Irvine32.lib` files inside.

**2. Set Up a Visual Studio Project**

* **New Project:** Open Visual Studio and create a new "Empty Project". Make sure to select C++ as the language.
* **Add Assembly File:** Right-click on the "Source Files" folder in your project, and add a new item. Name it with the `.asm` extension (e.g., `myProgram.asm`).

**3. Configure Visual Studio for MASM**

* **Build Customization:**
    * Right-click on your project in the Solution Explorer.
    * Go to "Build Dependencies" -> "Build Customizations".
    * Check the box for "masm(.targets,.props)".
* **Set Item Type:**
    * In the Solution Explorer, right-click on your `.asm` file.
    * Select "Properties".
    * Make sure "Item Type" is set to "Microsoft Macro Assembler".

**4. Link the Irvine32 Library**

* **Project Properties:** Right-click on your project in the Solution Explorer and select "Properties".
* **Include Paths (MASM):**
    * Under "Microsoft Macro Assembler" -> "General", find "Include Paths".
    * Add the path to your Irvine folder (e.g., `C:\Irvine`).
* **Additional Library Directories (Linker):**
    * Go to "Linker" -> "General" -> "Additional Library Directories".
    * Add the path to your Irvine folder again.
* **Additional Dependencies (Linker):**
    * Navigate to "Linker" -> "Input" -> "Additional Dependencies".
    * Add `Irvine32.lib` to the list.

**5. Write Your Assembly Code**

* **Include Irvine32.inc:** At the beginning of your `.asm` file, add the following line:

```assembly
INCLUDE Irvine32.inc
```

* **Example Code:**

```assembly
INCLUDE Irvine32.inc

.data
    message BYTE "Hello, world!",0dh,0ah,0

.code
main PROC
    mov edx, OFFSET message
    call WriteString
    exit
main ENDP
END main
```

**6. Build and Run**

* Build your solution (Build -> Build Solution).
* Run your program (Debug -> Start Without Debugging).

You should see "Hello, world!" printed in the console window.

**Important Notes:**

* **Visual Studio Version:** These steps are generally applicable to recent Visual Studio versions. Older versions might have slightly different menu options.
* **32-bit vs. 64-bit:**  The Irvine32 library is designed for 32-bit applications. Make sure your Visual Studio project is configured to target x86 architecture.
* **Troubleshooting:** If you encounter errors, double-check all the paths and settings, and make sure the Irvine32 files are correctly placed.

If you have any more questions, feel free to ask!


