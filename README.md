# iRealm 🌌

![iRealm](https://img.shields.io/badge/iRealm-Automate_Kerberos_Setup-blue.svg)
[![Releases](https://img.shields.io/badge/Download_Releases-brightgreen.svg)](https://github.com/thobanedube/iRealm/releases)

## Overview

Welcome to **iRealm**, a tool designed to streamline the setup of Kerberos and realms for Active Directory (AD) pentesting. This project automates essential tasks such as editing the `/etc/hosts` file, syncing time with the Domain Controller (DC), and configuring the `krb5.conf` file. Whether you are a security professional or a student, iRealm can help simplify your workflow.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Features

- **Automated Configuration**: Automatically updates `/etc/hosts` and `krb5.conf`.
- **Time Synchronization**: Ensures your system clock is in sync with the DC.
- **User-Friendly**: Designed for ease of use, even for those new to AD pentesting.
- **Flexible**: Works in various environments and setups.
- **Open Source**: Contribute to the project and help improve it.

## Installation

To get started with iRealm, you need to download the latest release. You can find the releases [here](https://github.com/thobanedube/iRealm/releases). Download the appropriate file for your system, and execute it to set up the tool.

### Requirements

- A Unix-like operating system (Linux, macOS).
- Administrative privileges to modify system files.
- Basic knowledge of Kerberos and Active Directory.

## Usage

Once you have installed iRealm, you can use it to automate your Kerberos setup. Follow these steps:

1. **Run the Script**: Execute the downloaded file. This will initiate the setup process.
2. **Follow Prompts**: The script will guide you through the necessary configurations.
3. **Verify Configuration**: After completion, check your `/etc/hosts` and `krb5.conf` files to ensure they are correctly configured.

### Example Command

```bash
./iRealm.sh
```

## Configuration

iRealm allows for some customization based on your environment. You can modify the configuration files as needed. Here’s how:

1. **Edit `/etc/hosts`**: Ensure that your DC's hostname and IP address are correctly listed.
2. **Modify `krb5.conf`**: Update the realm and KDC information as required for your setup.

### Sample `krb5.conf`

```ini
[libdefaults]
    default_realm = EXAMPLE.COM
    dns_lookup_realm = false
    dns_lookup_kdc = true

[realms]
    EXAMPLE.COM = {
        kdc = kdc.example.com
        admin_server = kdc.example.com
    }

[domain_realm]
    .example.com = EXAMPLE.COM
    example.com = EXAMPLE.COM
```

## Contributing

We welcome contributions to iRealm! If you want to help improve the tool, follow these steps:

1. **Fork the Repository**: Create your own copy of the project.
2. **Make Changes**: Implement your features or fixes.
3. **Submit a Pull Request**: Share your changes with us for review.

### Issues

If you encounter any issues, please report them in the [Issues](https://github.com/thobanedube/iRealm/issues) section of the repository.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or suggestions, feel free to reach out:

- **Author**: Thobane Dube
- **Email**: thobanedube@example.com
- **GitHub**: [thobanedube](https://github.com/thobanedube)

Thank you for using iRealm! For the latest updates and releases, visit [here](https://github.com/thobanedube/iRealm/releases).