# 🧰 Crunch Examples – Custom Wordlist Generator

`crunch` is a tool used to generate wordlists based on user-defined rules such as character sets, patterns, and word lengths. It is extremely useful for creating tailored lists for password attacks, PIN testing, or specific fuzzing cases.

---

## 📘 Basic Syntax

```bash
crunch <min> <max> [characters] [options]

    
* <min>: Minimum length of generated words

* <max>: Maximum length of generated words

* [characters]: Character set to use (e.g., abc, 123, ABCabc123!@#)

* [options]: Additional arguments (like patterns, output files, compression)

🔹 Examples
1️⃣ Generate 4-digit PIN codes (0000 to 9999)

crunch 4 4 0123456789 -o pin-4digit.txt
➡️ Output will contain every combination from 0000 to 9999

2️⃣ Generate lowercase words (3 to 5 letters)
crunch 3 5 abcdefghijklmnopqrstuvwxyz -o lower.txt
➡️ Useful for username or password guessing

3️⃣ Generate numbers in phone number format (e.g., Azerbaijani numbers: 050xxxxxxx)
crunch 9 9 0123456789 -t 050%%%%%%%
% means a wildcard number

Output: 0501234567, 0509999999, etc.

4️⃣ Generate words with mixed characters (e.g., letters and digits)
crunch 6 6 abc123 -o alphanumeric.txt
➡️ Will produce all 6-character combos using letters a, b, c and digits 1, 2, 3

5️⃣ Compress output with gzip
crunch 6 6 abc123 -o compressed.lst.gz -z gzip
➡️ Saves disk space; output will be in .gz format

6️⃣ Use a custom pattern (e.g., P@ssw0rd format)
crunch 8 8 -t @@ss%%rd
@ → lowercase letters

, → uppercase letters

% → numbers

^ → symbols

➡️ Will generate passwords like: abss12rd, zqss99rd, etc.

🛠️ Tips
Use --help to view all options:

crunch --help
You can pipe output directly into cracking tools:

crunch 6 6 abc123 | john --stdin hashfile
🧪 Note: Be careful — crunch can generate extremely large files. Always check estimated size before outputting to file.
