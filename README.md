# ObsidianPy (obsn)

ObsidianPy is a library for Python that provides easier access to Geometry Dash, Encryptions relating to Geometry Dash functions and other utilities. Made mainly for obsidian tools.  
https://sevenworks.eu.org/obsidian

## Installation

You can install the package via pip:

```sh
pip install obsn
```

## Usage

### Importing the Library

```py
import obsidian
```

### Functions

#### Encryption/Decryption and Generation

- `xor_cipher(data, key)`

  Encrypt something with XOR.

  ```python
  x = obsidian.xor_cipher("hello there", "key")
  ```

- `base64_encode(string)`

  Encode a string in Base64.

  ```python
  b64 = obsidian.base64_encode("hello")
  ```

- `base64_decode(encoded_string)`

  Decode a Base64 string.

  ```python
  b64d = obsidian.base64_decode(b64)
  ```

- `gjp_encrypt(data)`

  Encrypt data using GJP (Geometry Jump Password) encryption.

  ```python
  password = obsidian.gjp_encrypt("data")
  ```

- `gjp_decrypt(encrypted_data)`

  Decrypt data using GJP decryption.

  ```python
  passwordyay = obsidian.gjp_decrypt(password)
  ```

- `generate_udid()`

  Generate a UDID for server requests.

  ```python
  udid = obsidian.generate_udid()
  ```

- `generate_rs(n)`

  Generate a random string, RobTops security in a nutshell.

  ```python
  gd_rs = obsidian.generate_rs(8)
  ```

- `generate_uuid(parts=[8, 4, 4, 4, 10])`

  Generate a UUID for server requests.

  ```python
  uuid = obsidian.generate_uuid()
  ```

- `generate_upload_seed(data, chars=50)`

  Generate an upload seed.

  ```python
  upload_seed = obsidian.generate_upload_seed("some data")
  ```

- `generate_leaderboard_seed(jumps, percentage, seconds, has_played=True)`

  Generate a leaderboard seed.

  ```python
  leaderboard_seed = obsidian.generate_leaderboard_seed(10, 80, 120)
  ```

- `generate_chk(values=[], key="", salt="")`

  Generate a fancy CHK.

  ```python
  chk = obsidian.generate_chk([1, 2, 3], key="key", salt="salt")
  ```

#### HTTP Requests

- `gd(endpoint, **data)`

  Send a POST request to the Geometry Dash servers. ("using accounts/registerGJAccount.php" is valid too)

  ```python
  response = obsidian.gd("getGJGirlfriends24", user="Sevenworks")
  ```

- `gdbrowser(endpoint, value, **kwargs)`

  Send a GET request to retrive something from GDBrowser API.

  ```python
  response = obsidian.gdbrowser("search", "*", count=10)
  ```

- `gd2json(response)`

  Convert a Geometry Dash server response (key:value:key:value) to JSON format, for nerds only.

  ```python
  response_json = obsidian.gd_json(response)
  ```

#### Other

- `toast(title, content, timeout=3)`

  Display a toast notification on Windows.

  ```python
  obsidian.toast("My Tool", "yo wassup", timeout=5)
  ```
