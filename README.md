# ShiftLeft Scan

ShiftLeft [Scan](https://docs.shiftleft.io/shiftleft/scan/scan) is a free commercial-grade security tool for modern DevOps teams. With an integrated multi-scanner based design, Scan can detect various kinds of security flaws in your application and infrastructure code in a single fast scan. The product supports a range of integration options: from scanning every push via a git hook to scanning every build and pull-request in the CI/CD pipelines such as Azure DevOps Pipelines, GitHub actions and so on.

Use this extension to perform security scans and visualize the scan results without leaving your IDE. Navigate to the source code and remediate the results by interacting with the scan results.

## **Features**

- One-click security scanning (SAST Based scanning)
- Navigation to the source location of the result
- Scan Results shows details about the result:
  - Result info
  - Run info
  - Code flow steps
  - Attachments
  - Fixes
- MacOS touch bar support
- Contributes a dark theme called `ShiftLeft`

## Results Viewer

- Automatically launches after performing a scan or when the workspace contains .sarif files in reports directory
- Updates the Result Details Panel with the currently selected result in the Results List, Problems Panel, or in source code
- Manually open it by typing "ShiftLeft: ShiftLeft Scan Results" in the Command Palette(Ctrl+P or ⌘+P) or using the hotkey (Ctrl+L then Ctrl+E)

# Using

## Install

1. Install or upgrade [Visual Studio Code](https://code.visualstudio.com/). Requires version 1.41.0 or higher.
2. Install the ShiftLeft Scan Extension
3. Reload VS Code
4. Install Docker Desktop for performing ShiftLeft Scan

## Use

1. Perform a ShiftLeft Scan by using the `Perform Security Scan` option in the results window. Or in the Command Palette (Ctrl+Shift+p or ⌘+⇧+p) type "ShiftLeft: Perform Scan" or use the hotkey (Ctrl+l then Ctrl+p)
2. Results will show up on the **Scan Findings** panel
3. Click the result you're investigating. The editor will navigate to the location

## Screenshots

![Extension in Action](resources/readmeImages/vscode.gif?raw=true)

# Support

For help and support installing and using this extension, please use: https://discuss.shiftleft.io

## Known Issues

- VS code version should be 1.41.0 or higher for the extension to install and work
- The user should be part of the `docker` group on linux and mac. Please refer to the [post install](https://docs.docker.com/install/linux/linux-postinstall/) steps for your platform. Example below for linux.

```bash
sudo groupadd docker
sudo usermod -aG docker $USER
```

- Internet connectivity is required while loading the results for the first time. You might see the below error otherwise.

```
Unable to load schema from 'https://raw.githubusercontent.com/oasis-tcs/sarif-spec/master/Schemata/sarif-schema-2.1.0.json': getaddrinfo ENOTFOUND raw.githubusercontent.com.
```

# Credits

The extension uses parts of [SARIF extension](https://github.com/Microsoft/sarif-vscode-extension) with a number of ShiftLeft Scan specific enhancements.