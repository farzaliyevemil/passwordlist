# 🧠 CUpp Usage Guide – Common User Passwords Profiler

**CUpp (Common User Passwords Profiler)** is a Python-based tool that generates personalized wordlists based on information gathered through social engineering.

It is ideal for **CTFs**, **real-world pentests**, and **targeted brute-force attacks** — just like Elliot did in *Mr. Robot*.

---

## ⚙️ Installation

```bash
git clone https://github.com/Mebus/cupp.git
cd cupp
python3 cupp.py -h
```

✅ No extra dependencies required — it’s fully portable and works on Kali, Parrot, Ubuntu, etc.

🚀 Interactive Mode
Use this mode to provide data manually and generate a wordlist:

```bash
python3 cupp.py -i
```

It will ask for the following info:

First name

Surname

Nickname

Birthdate

Partner’s name

Pet’s name

Company name

Favorite color, sports, teams

Additional keywords

➡️ At the end, it generates a personalized wordlist like:

```
sarah1995
bluecat
johnmary123
chelsea2020
...
```

🔍 Example – Mr. Robot Style Attack
Imagine you know the following about your target:

Name: Angela

Birth year: 1988

Pet: Luna

Favorite band: Nirvana

CUpp will combine these values and create realistic password guesses like:
```
angela1988
luna88
nirvana1988
angelaluna
NirvanaLuna
...
```
💡 Other Usage Modes
Generate wordlist from file (keywords):
```
python3 cupp.py -w -l keywords.txt
```
Each line in keywords.txt should contain one word (name, hobby, pet, etc.)

📦 Output
The generated wordlist is saved as:
```
[firstname].txt
```
You can use this with any password cracking tool:
```
hydra -l admin -P angela.txt ftp://192.168.0.10
```

🧪 Tip
CUpp doesn’t generate huge lists — it focuses on realistic, likely combinations, which makes it very effective in practical brute-force attacks.

🔗 GitHub Repository:
https://github.com/Mebus/cupp
