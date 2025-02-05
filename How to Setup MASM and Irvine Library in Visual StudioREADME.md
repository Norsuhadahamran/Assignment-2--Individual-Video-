# Step by Step to Setup MASM and Irvine Library in Visual Studio | Setup Irvine Library

**1. Download Visual Studio 2019**

* **Download:** Get the Visual Studio from GitHub https://github.com/Norsuhadahamran/Visual-Studio-2019 .

**2. Set Up a Visual Studio Project**

New Project: Open Visual Studio and create a new "Empty Project". Make sure to select C++ as the language.

Add Assembly File: Right-click on the "Source Files" folder in your project, and add a new item. Name it with e.g., Assembly Project and click button OK.

**3. Configure Visual Studio for MASM**

1 ) Delete unrelated folder such as Header Files, Resource Files & Sources Files (Right Click and click delete)
![image](https://github.com/user-attachments/assets/8e6bbb14-136b-493f-a367-8210033b2d3a)

2) Click "OK" for the selected items will be removed from 'Assembly Project Github'
![image](https://github.com/user-attachments/assets/214f5393-492e-40aa-a93c-668be61f565e)

3) Right Click in 'Assembly Project Github' choose 'Build Dependencies' and Click 'Build Customizations..'
![image](https://github.com/user-attachments/assets/945c0db6-dccc-4390-9908-2ff0ddd0c1ac)

4) For 'Available Build Customization Files', Click "masm(.target,.props)" and click "OK"
   ![image](https://github.com/user-attachments/assets/821b2deb-e0db-4bf6-a946-1383f7f5a59e)

   
**4. Download Irvine.zip**

1) Go to Repository https://github.com/Norsuhadahamran/Visual-Studio-2019 and download folder "Irvine.Zip"
![image](https://github.com/user-attachments/assets/f9825c1b-0f87-4437-981f-a251dcb1e124)
![image](https://github.com/user-attachments/assets/e15c6f16-9093-40ad-86c2-717ee3f55a9a)

2) In folder download for Irvine folder, click "Extract all" and save at folder C:\
![image](https://github.com/user-attachments/assets/d4dfefc7-efcd-4b39-a1b0-5f5f6c61e833)

3) Go to folder C:\, click folder Irvine and the contain folder should be like this:
![image](https://github.com/user-attachments/assets/565979fc-f723-4651-a3c5-66164d57d222


**5. Link the Irvine32 Library**

1) In 'Assembly Project Github', go to "add" and click "New item"
![image](https://github.com/user-attachments/assets/cf73ce06-f67a-483d-86a4-53f39e98a274)

2) Change name Source.cpp to Source.asm and click "add"
![image](https://github.com/user-attachments/assets/03b7a734-74b9-4463-8065-85c609892903)

3) Download Code Structure in https://github.com/Norsuhadahamran/Visual-Studio-2019/blob/main/Code%20Structure.
   Copy code structure and paste at Source.asm.
   ![image](https://github.com/user-attachments/assets/5eef6cac-3eec-4925-8eb7-05bd06a1e57f)

   

   **Code Structure:**

   ![image](https://github.com/user-attachments/assets/946406b7-00e6-4a13-aae8-c1e398d9567c)

4) Assembly Project Github : Right-click on your project in the Solution Explorer and select "Properties".
Include Paths (MASM):
Under "Microsoft Macro Assembler" -> "General", find "Include Paths".
![image](https://github.com/user-attachments/assets/857f1645-aa9c-4585-9f82-48dd6ad6bfac)

5) Additional Library Directories (Linker):
   . Go to 'Assembly Project Github' under properties in Linker General at Additional Library Directories.
   Copy folder C:\Irvine and paste at Additional Library Directories.
   
   ![image](https://github.com/user-attachments/assets/e7e65a71-fd79-48da-a974-d3f96d106d2b)
   ![image](https://github.com/user-attachments/assets/637e0ee0-334c-4fb2-b973-737d6c859923)
   ![image](https://github.com/user-attachments/assets/f62b1ea1-fe71-4c7a-a4ee-bf5665e4cc02)

   . Go to Linker under input in 'Additional Dependencies'add "irvine32.lib;"
   ![image](https://github.com/user-attachments/assets/aac29254-40aa-45e2-8b56-b13cd3cf138a)

   ' Under Micsoft Macro Assembler in Include Paths add "C:\Irvine "
   ![image](https://github.com/user-attachments/assets/b03de7bb-f224-4bc6-8d19-eb10726512be)

   . Under Linker in System at SubSystem choose "Console (/SUBSYSTEM:CONSOLE)"
   ![image](https://github.com/user-attachments/assets/495c526a-615f-47dc-8faa-9dec39384186)



**6. Export templete**
 For making tempelete go to 'search' and find 'export templete'
 ![image](https://github.com/user-attachments/assets/f88738b8-cebd-47a8-b6e0-97dc7156fe52)

 Click "Next"
 
 ![image](https://github.com/user-attachments/assets/01741e2a-2edc-4fb8-9061-688cc5c07f41)

 

 Click "Finish"
 
 ![image](https://github.com/user-attachments/assets/27ae310b-2b7a-4230-a0d4-64fb44c81cd8)

 

 Open 'Create a new project', in searching find "Assembly Project Github" and click "Next"
 
 ![image](https://github.com/user-attachments/assets/ffeee6a9-3c2c-4d38-b455-62d18a47cd74)

 

Create your project name and click "Create"

![image](https://github.com/user-attachments/assets/ae3b9829-f9c5-4e42-8849-0159b04d228c)



**6. Write Assembler Code**
' Create simple program to run test the program

![image](https://github.com/user-attachments/assets/c124ea8b-9145-432e-a70c-359f2f917cf0)



. Under Build, click "Compile"

![image](https://github.com/user-attachments/assets/6a973a63-c91e-4c92-8a44-30530ffa92bc)



. The result Output should be success without failed

![image](https://github.com/user-attachments/assets/d2b1a595-5099-4edb-99fd-66a73ed8dca9)



. Next, Under 'Debug' click "Start Debugging"

![image](https://github.com/user-attachments/assets/8e98ac34-159b-49ed-93b8-37c2050548b5)



Final the program must be succesful and can display the command without any failed.

![image](https://github.com/user-attachments/assets/0e3ad02b-7e54-4222-bdd7-1c906985298a)
