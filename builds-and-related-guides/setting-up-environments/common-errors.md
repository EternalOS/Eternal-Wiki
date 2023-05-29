---
description: >-
  Building Eternal OS can be an exciting endeavor, allowing you to create your
  own build. Like any complex process, building Eternal OS you might encounter
  errors.
---

# ❌ Common Errors

In this one, we will explore the errors and their solutions :

### 1. "make: \*\*\* No rule to make target 'target'" or similar messages.



This error typically occurs when the build system cannot find the specified target or makefile. To resolve this issue, ensure that you have selected the correct target for your device by running the following command:

```bash
lunch <device_codename>-<build_variant>
```

### 2. "Java heap space" or "Out of memory" errors during the build.

When building Eternal OS, Java heap space errors may occur due to insufficient memory allocated to the Java Virtual Machine (JVM). While, the best resolution for this is to increase ram of your PC but one might try this one:

To address this issue, increase the amount of memory allocated to the JVM by setting the `JAVA_OPTS` environment variable before starting the build, as shown below:

```bash
export JAVA_OPTS="-Xmx4g"
```

This example sets the maximum heap size to 4GB. Adjust the value according to your system's available memory.

### 3. "Missing required modules" or "missing dependency" messages.

If you encounter missing module or dependency errors during the build process, it often indicates that the necessary packages or libraries are not installed on your system. Ensure that you have installed all the required dependencies by following the AOSP documentation or build guides specific to your version and distribution. Additionally, make sure to update your system packages and development tools to their latest versions.

### 4. "permission denied" when executing build scripts or running make commands.&#x20;

Permission denied errors occur when the user executing the build process lacks sufficient permissions. To resolve this issue, ensure that you have the necessary read, write, and execute permissions for the AOSP source code and build directories. You can use the `chmod` command to modify file permissions. For example:

```
chmod +x build/envsetup.sh
```

This command grants execute permission to the specified script.

### 5. "Failed to fetch URL... Connection timed out" during repo sync.

During the "repo sync" command, you may encounter a "Failed to fetch URL... Connection timed out" error. This error suggests a problem with accessing the necessary Eternal OS source code repositories.

To resolve this error, you can try the following steps:

1. Check your internet connection: Ensure that you have a stable internet connection and that you can access other websites or online resources without issues.
2. Retry the repo sync: The error may occur due to a temporary network issue or server problem. Try running the "repo sync" command again to see if the error resolves itself.
3. Use a different network or mirror: Sometimes, certain networks or repositories may experience connectivity issues. Try switching to a different network or using a mirror closer to your location. You can modify the manifest file (`default.xml`) to use a different mirror by replacing the URL with an alternative mirror URL.
4. Configure a proxy (if applicable): If you are behind a proxy, ensure that the necessary proxy settings are correctly configured in the Eternal OS build environment. Modify the Git configuration to include proxy settings using the following commands:

```git
git config --global http.proxy <proxy_url>
git config --global https.proxy <proxy_url>
```

Replace `<proxy_url>` with the appropriate proxy URL and port number.

5. Check firewall and security settings: In some cases, firewall or security settings on your system or network may block the necessary connections. Ensure that any firewall or security software is not interfering with the AOSP build process.

## Conclusion

Building Eternal OD can be a rewarding experience, but encountering errors during the process is not uncommon. By understanding and troubleshooting common errors, you can overcome these hurdles and successfully build Eternal OS. Remember to consult the official AOSP documentation, relevant forums, and developer communities for additional support and guidance when facing specific errors. Happy building!
