# Active Directory Home Lab

A portable Active Directory lab built in VirtualBox using Windows Server 2025 and a Windows 10 client. I built it to get hands-on practice with core Active Directory administration: setting up a domain, managing users and groups, applying Group Policy and automating user creation with PowerShell.

The lab is stored on an external drive so it can be run on different machines.

## Lab Environment

| Component | Details |
|---|---|
| Hypervisor | VirtualBox |
| Domain Controller | Windows Server 2025 |
| Client | Windows 10 |
| Storage | External drive (portable across machines) |

## What I Built

- **Domain setup:** Installed and configured Active Directory Domain Services on Windows Server 2025 and promoted it to a domain controller
- **DNS and DHCP:** Configured DNS and DHCP on the server so the client could resolve the domain and receive an address automatically
- **Domain join:** Joined the Windows 10 client to the domain and signed in with domain accounts
- **Organisational structure:** Created Organisational Units (OUs), users and security groups
- **Group Policy:** Created and applied Group Policy Objects to the domain
- **Automation:** Wrote a PowerShell script to create users in bulk instead of adding them one by one

## Repository Contents

```
.
├── README.md
├── scripts/        # PowerShell scripts (e.g. user creation)
└── screenshots/    # Screenshots of the lab configuration
```

## Screenshots

<!-- Replace these with your own screenshots once uploaded to the screenshots/ folder -->

| Description | Screenshot |
|---|---|
| Active Directory Users and Computers (OU structure) | `screenshots/ou-structure.png` |
| Group Policy Management | `screenshots/group-policy.png` |
| Windows 10 client joined to the domain | `screenshots/domain-join.png` |
| PowerShell user creation script running | `screenshots/powershell-script.png` |

To display an image in this README, use:

```
![OU structure](screenshots/ou-structure.png)
```

## Running the User Creation Script

1. Open PowerShell as Administrator on the domain controller
2. Navigate to the `scripts/` folder
3. Run the script:

```powershell
.\New-BulkUsers.ps1
```

> Replace `New-BulkUsers.ps1` with the actual filename of your script. The script does not contain any real credentials or personal data.

## Skills Demonstrated

- Active Directory Domain Services administration
- User, group and OU management
- Group Policy
- DNS and DHCP configuration
- PowerShell scripting and automation
- Virtualisation with VirtualBox
- Windows Server and Windows client administration

## What I Learned

Building the lab end to end showed me how the pieces of a Windows domain depend on each other: the client cannot join the domain without working DNS, Group Policy only applies once users and computers sit in the right OUs, and repetitive tasks like account creation are much faster and less error-prone when scripted.

## Author

**Bilal Tariq**
GitHub: [Bilal05Tariq](https://github.com/Bilal05Tariq)
