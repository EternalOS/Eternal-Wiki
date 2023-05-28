---
description: 'To Get Started With Building Eternal OS:'
---

# 🛠 Setting Up Environments

<details>

<summary>Step1: Setup Linux, Get Enough, Storage &#x26; RAM (A better than decent computer is preferred)</summary>

You Need to Setup Linux higher than 18.0.0, Have a minimum dedicated 350GB+ storage to build for one device or more if you are interested in conducting multiple builds, 16GB RAM or higher (Very low-possibilities that lower configurations might work)

**Note : You Might want to dual-boot Windows and Ubuntu running Ubuntu terminal/shell from Windows won't work the same applies for WSL (Windows Subsystem for Linux).**&#x20;

</details>

<details>

<summary>Step 2: Install Necessary Packages</summary>

```
sudo apt-get install git-core gnupg flex bison build-essential zip curl zlib1g-dev gcc-multilib g++-multilib libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev lib32z1-dev libgl1-mesa-dev libxml2-utils xsltproc unzip fontconfig
```

then,

```
sudo apt update
```

&

```
sudo apt upgrade
```

</details>

<details>

<summary>Step 3: Initialize Repository &#x26; Sync The Code</summary>

This is where **a Reliable and Fast Internet Connection is Required**

In Terminal:

```
# Create and Enter Eternal Folder
mkdir eternal && cd eternal
```

then,

```
# Initialize Repository Locally
repo init -u https://github.com/EternalOS/manifest -b tiramisu
```

Finally,

_**Note : This Command Might Take up to 12 hours depending on your Internet Connection also this will finally take about 20-30gigs of storage...**_

<pre><code><strong># Download and Sync the Source Code
</strong><strong>repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
</strong></code></pre>

</details>
