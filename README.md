# NppStripIpAndHost

A fast, customizable Notepad++ plugin designed to safely sanitize text files, server logs, and configurations by stripping out sensitive IP addresses (IPv4 & IPv6) and hostnames.

## ✨ Features

* **Smart IPv4 Stripping:** Granular control over IPv4 replacements. You can choose exactly which octets to replace and specify custom placeholder text for each individual octet.
* **IPv6 & Hostname Sanitization:** Quickly toggle and replace entire IPv6 addresses or hostnames/URLs with your own custom strings (e.g., `2001:db8::1` or `hostname.com`).
* **Native Settings UI:** A built-in, easy-to-use configuration window to manage all your replacement strings and toggles on the fly.
* **Document-Safe Undo:** Features a custom, memory-safe "Undo" engine that tracks changes per-document. If you strip the wrong file, you can safely undo it without affecting your other open tabs.
* **Visual Feedback:** Integrates seamlessly with the Notepad++ UI, providing wait cursors for large files and status bar updates to let you know when stripping is complete.

## 🚀 Installation

### Automatic (If added to Plugin Admin later)
* Open Notepad++ -> `Plugins` -> `Plugins Admin...`
* Search for **NppStripIpAndHost**, check the box, and click **Install**.

### Manual Installation
1. Download the latest `NppStripIpAndHost_x64.zip` from the [Releases](../../releases) page.
2. Extract the `.zip` archive.
3. You will see a folder named `NppStripIpAndHost` (containing the `.dll` file). 
4. Copy this entire folder into your Notepad++ plugins directory.
   * *Usually located at:* `C:\Program Files\Notepad++\plugins\`
5. Restart Notepad++.

*(Note: The plugin folder name must exactly match the `.dll` name inside it for Notepad++ to load it properly).*

## 💡 Usage

1. Open the file you want to sanitize in Notepad++.
2. Navigate to **Plugins** -> **NppStripIpAndHost** in the top menu bar.
3. Click **Replace Settings...** to open the configuration menu. Set your custom replacement strings and check the boxes for the items you want to strip.
4. Click **Strip IPs and Hostnames** to execute the replacement.
5. If you need to revert the changes in your current tab, click **Undo Last Strip**.

## 🛠️ Building from Source

If you want to compile this plugin yourself:
1. Clone the repository.
2. Open `NppStripIpAndHost.sln` in **Visual Studio**.
3. Select your target architecture (`x64` for modern 64-bit Notepad++, or `x86` for 32-bit).
4. Go to **Build** -> **Build Solution**.
5. The compiled `.dll` will be output to the `vs.proj\x64\Debug` or `Release` folder.
