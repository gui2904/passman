<!-- markdownlint-disable MD013 MD033 MD041-->
<div align="center">
  <h1>Passman</h1>
</div>

<div align="center">
  <p>
    Passman is a lightweight command-line password manager written in Python. Unlike many password managers, it does not depend on any external API, network connection, service or any form of external connection. 
    <br>
    It securely stores credentials using encryption, generates strong passwords, and provides a simple CLI workflow for managing logins locally.
    <br>
    Designed for developers, terminal users, and anyone who prefers a minimal, private password solution.
  </p>
</div>


---

<div align="center"><p>

[Features]: #features
[Get Started]: #get-started
[Usage]: #usage
[Security]: #security-notes

**[<kbd><br> Features <br></kbd>][Features]**
**[<kbd><br> Get Started <br></kbd>][Get Started]**
**[<kbd><br> Usage <br></kbd>][Usage]**
**[<kbd><br> Security <br></kbd>][Security]**

</p></div>

---

## Features

[Fernet]: https://pypi.org/project/cryptography/

- **Local encrypted** password storage using [Fernet] encryption (Python library)
- **Fast** CLI workflow. No GUI required
- **Strong** secure password generator
- **Clipboard** support (Wayland / X11)
- No **cloud**, **API**, or any form of **external** dependencies
- **Options** for edit, rename, list, and delete credentials
- **Automatic** secure file permissions
- **Simple** JSON storage with encryption layer

## Get Started
### Requirements

- Python **3.8+**
- `cryptography` package:
  ```bash
  pip install cryptography
  ```

- Optional clipboard tools:
  - Wayland
  ```bash
  sudo apt install wl-clipboard #For Ubuntu/Debian
  sudo pacman -S wl-clipboard #For ArchLinux
  ```

  - X11
  ```bash
  sudo apt install xclip #For Ubuntu/Debian
  sudo pacman -S xclip #For ArchLinux
  ```

### Clone the repository
```bash
git clone https://github.com/gui2904/passman.git
cd passman
chmod +x passman
```
Optional: You can move it to your local bin directory for easier user
```bash
sudo mv passman /usr/local/bin
```

### Usage
To add credential with automatic password generation, for the user I recommend adding either the username of the website or the email you use
```bash
passman add github --username myuser or user@mail.com
```
You can add a --copy parameter, so the password goes directly to your clipboard
```bash
passman add github --username myuser --copy
```

Prompt for password manually
```bash
passman add github --username myuser --prompt
```

