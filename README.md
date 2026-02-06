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

---

## Get Started
### Requirements

- Python **3.8+**
- `cryptography` package:

```bash
pip install cryptography

- Optional clipboard tools:
  - Wayland
  ```bash
  sudo pacman -S wl-clipboard
  or
  sudo apt install wl-clipboard

  - X11
  ```bash
  sudo apt install xclip


