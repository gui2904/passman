<!-- markdownlint-disable MD013 MD033 MD041-->
<div align="center">
  <h1>Passman</h1>
</div>

<div align="center">
  <p>
    Passman is a lightweight command-line password manager written in Python. Unlike many password managers, it does not depend on any external API, network connection, service or any form of external connection. 
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

## Usage

### Add credentials
To add credential with automatic password generation. For the `--username`, I recommend adding either the username you use for the website or the email you use
```bash
passman add github --username myuser or user@mail.com
```
You can add a `--copy` parameter, so the password goes directly to your clipboard
```bash
passman add github --username myuser --copy
```

Prompt for password manually
```bash
passman add github --username myuser --prompt
```

---

### View credentials
```bash
passman view github
```

---

### Edit credentials
To edit credentials, you can use:
```bash
passman edit github --username newuser #only edits the username
passman edit github --prompt #only edits the password
passman edit github --username newuser --prompt #edits the username and password
```

---

### List credentials
```bash
passman list
```

---

### Delete credentials
```bash
passman delete github
```
You can also skip confirmation by using:
```bash
passman delete github --yes
```

---

### Rename credentials
```bash
passman rename github --new-name gh
```

---

### Generate password
To generate a random password, you can use this. But keep in mind that the password will be outputted in the terminal
```bash
passman gen
```

To copy the generated password to your clipboard, and also keeping the password from outputting to the terminal, you can use:
```bash
passman gen --copy
```

If you want to copy the password and also output it, you can use:
```bash
passman gen --copy --print
```

You can also set the lenght of the password by using:
```bash
passman gen --length 20 #can also add the --copy param
```

### Storage Location
Passman stores data locally:
```arduino
~/.config/passman/
├── secret.key
└── credentials.json
```

> [!IMPORTANT]
> If you lose secret.key, your stored passwords cannot be recovered.
> Back it up securely.

## Security notes
- Uses [Fernet] symmetric encryption via cryptography
- Encryption key stored locally with restricted permissions
- Clipboard copies will be stored in your clipboard, keep that in mind
- Intended for personal/local usage
- Backup encryption key safely

## License
This project is licensed under the MIT License. See the LICENSE file for details
