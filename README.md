## Overview

This README describes the various commands used to handle files and run programs with input files. Below is an explanation of each command.





## 🔌 Data Preprocessing

#### 📅 Last Updated Date: December 22, 2024

1. **Download the TSV data**  

2. **Use LibreOffice Calc to process the data and save the result as html file**  

3. **Conver newlines to spaces**  

4. **Save the data as List-{Date}.txt**  





## ⚙️ Installation

1. **Unzipping the Password-Protected File**  

   ```bash
   unzip -P password Bitfi.zip
   ```

2. **Running Make**  

   ```bash
   make
   ```

3. **Concatenating the File to display its contents)**  

   ```bash
   cat List.txt
   ```

4. **Displaying the File in Hexadecimal Format**  

   ```bash
   hexdump -C List.txt | head
   ```

5. **Removing Byte Order Mark (BOM) from the File**  

   ```bash
   sed -i '1s/^\xEF\xBB\xBF//' List.txt
   ```

6. **Verifying BOM Removal (Hexadecimal Display)** 

   ```bash
   hexdump -C List.txt | head
   ```

7. **Passing File Content as Arguments**  

   ```bash
   xargs ./Bitfi -t 3 < List.txt
   ```
