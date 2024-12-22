## Overview

This README describes the various steps and commands to preprocess the data, handle files, and run the program with input data.





## 🔌 Data Preprocessing

#### 📅 Last Update: December 22, 2024

1. **Download the related TSV data**  

2. **Use LibreOffice Calc to process the data and save the result as a HTML file**  

3. **Convert newlines to spaces (Online tool)**  

4. **Save the data as List.txt**  





## ⚙️ Installation


0. **Prerequisites**  

   ```bash
   sudo apt-get install build-essential automake autoconf libtool libgmp3-dev p7zip-full
   cd Bitfi
   ```

1. **Unzipping the Password-Protected File**  

   ```bash
   7z x Bitfi.zip
   ```

2. **Running Make**  

   ```bash
   make
   ```

3. **Concatenating the File to display its contents)**  

   ```bash
   cat List.txt | head -c 100
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
