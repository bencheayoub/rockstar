# **Writeup: Rockstar Cipher Challenge**  
**Category**: Cryptography  
**Points**: 100  
**Solves**: 4/5  

## **Initial Observations**  
The challenge provides a file named `lyrics.txt` and is titled **"Rockstar"**, hinting at a possible connection to Rockstar Games or their encryption methods.  

### **Step 1: Researching Rockstar Encryption**  
A quick search reveals that Rockstar Games uses a proprietary engine called **RAGE (Rockstar Advanced Game Engine)**, primarily written in C++. However, for scripting gameplay elements, they may use embedded languages.  

A more relevant discovery is **[Code with Rockstar](https://codewithrockstar.com/online.html)**, a satirical programming language resembling rock lyrics. This suggests the cipher might involve Rockstar-language encoding.  

### **Step 2: Decoding with Rockstar Interpreter**  
Pasting the contents of `lyrics.txt` into the Rockstar interpreter yields the following numeric output:  
```
114 114 114 111 99 107 110 114 110 48 49 49 51 114
```  
![Image](https://github.com/user-attachments/assets/cb1256f6-cfe6-4204-9007-693623dcb255)

### **Step 3: Decimal to ASCII Conversion**  
Interpreting these numbers as **ASCII decimal values**, we decode them to characters:  

| Decimal | ASCII |
|---------|-------|
| 114     | 'r'   |
| 114     | 'r'   |
| 114     | 'r'   |
| 111     | 'o'   |
| 99      | 'c'   |
| 107     | 'k'   |
| 110     | 'n'   |
| 114     | 'r'   |
| 110     | 'n'   |
| 48      | '0'   |
| 49      | '1'   |
| 49      | '1'   |
| 51      | '3'   |
| 114     | 'r'   |

Combining these gives the string:  
**`rrrocknrn0113r`**  

Or simply we can use cyberchef :
![Image](https://github.com/user-attachments/assets/92fd41df-2a31-4971-9cd2-5d5af0b6e51d)


### **Final Flag**  
Wrapping the decoded string in the competition's flag format:  
**`OMC{rrrocknrn0113r}`**  

---

### **Summary**  
1. **Recognized the "Rockstar" hint** and explored relevant encoding methods.  
2. **Used the Rockstar interpreter** to convert lyrics into decimal values.  
3. **Decoded ASCII** to reveal the flag.  
