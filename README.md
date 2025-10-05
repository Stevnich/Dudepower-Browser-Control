# Dudepower-Browser-Control
A Browser you're using for Examination

## **Dudepower Browser Control: Feature Set**

This document outlines the key features, usage instructions, advantages, and limitations of **Dudepower Browser Control**, an application built with WPF and CefSharp.

### **Features**

#### **🔒 Security & Web Control**
* **Block Fullscreen Requests:** Prevents web pages from forcing the application into fullscreen mode.
* **Keybind Lock:** Blocks critical key combinations while the application is active, including:
    * $\text{Ctrl} + \text{W}$
    * $\text{Ctrl} + \text{R}$
    * $\text{Alt} + \text{F4}$
    * $\text{Alt} + \text{Tab}$
    * $\text{Windows Key}$
* **Toggle Page Preloading:** Allows users to enable/disable page preloading for performance control.

#### **🌐 Navigation & Page Control**
* **Navigate Page:** Displays a URL input dialog with $\text{OK}/\text{Cancel}$ buttons to load a new page.
* **Reload Page:** Functions similarly to the standard Chrome reload button.
* **Chromium Settings:** Opens the internal Chromium settings window ($\text{chrome://settings}$).

#### **🎨 UI & Branding**
* **Splash Screen / Branding Overlay:** A logo and text display while the Chromium Embedded Framework (CEF) initializes.
* **Loading Overlay:** A circular progress bar appears when a page is loading.
* **Dynamic Window Icon:** Fetches the **favicon** from the loaded webpage, falling back to a default icon if unavailable.

#### **🛠 Developer Tools**
* **Developer Console:** Accessible directly from the "Tools" menu.

#### **🧩 App Instance Management**
* **Single Instance Enforcement:** Prevents multiple instances of the application from running simultaneously, unless launched with the $\text{--open-settings}$ argument.

#### **⚙ Utility**
* **Toggle Taskbar Visibility:** Hides or shows the Windows taskbar.
* **Kill Background Process:** Terminates any dormant $\text{dpBroCon}$ processes that may be running without a visible window.

---

## **Shortcut Keys**

| Shortcut | Function | Note |
| :--- | :--- | :--- |
| $\text{Ctrl} + \text{W}$ | **Blocked** | Prevents accidental application closure. |
| $\text{Ctrl} + \text{R}$ | **Blocked** | Use the "Reload Page" menu option instead. |
| $\text{Alt} + \text{F4}$ | **Blocked** | Use the standard window close button. |
| $\text{Alt} + \text{Tab}$ | **Blocked** | Blocked when the app is active. |
| $\text{Windows Key}$ | **Blocked** | Blocked when the app is active. |

---

## **How to Use**

1.  Execute $\text{Dudepower Browser Control.exe}$.
2.  Wait for the splash screen; the browser will initialize automatically.
3.  Use the **Page** menu to navigate, toggle page preloading, or manage fullscreen security.
4.  Use the **Tools** menu to access the **Developer Console** or **Chromium Settings**.
5.  Use the **Help** menu for version and build information.
6.  Use the **Reload Page** button to refresh the current page.

---

## **Pros & Cons**

### **✅ Advantages**
* **High Security Control:** Features robust security measures, including comprehensive **keybind lock** and fullscreen request blocking.
* **Modern UI:** Offers a modern user experience with a splash screen, loading overlay, and dynamic favicon.
* **Integrated Controls:** Navigation, reload, and access to Chromium settings are available directly within the application menu.
* **Stability:** **Single instance enforcement** minimizes errors and instability caused by multiple parallel instances.
* **Lightweight & Efficient:** Built with $\text{WPF} + \text{CefSharp}$, making it a feature-rich yet lightweight application.

### **❌ Limitations**
* **Settings Access:** Chrome/Chromium settings access is limited; not all configuration options are available.
* **Favicon Reliability:** Favicon retrieval may occasionally fail depending on the webpage's format.
* **No Tab Management:** The application supports a single active page per window (no tab functionality).
* **Platform Restriction:** The Taskbar toggle feature is available only on **Windows**.
* **Security Scope:** Security is limited (e.g., no built-in JavaScript sandboxing).
* **Detection Method:** Single instance detection relies solely on the process name.

---

## **Build & Release Information**

* **Build Environment:** Developed with $\text{Visual Studio 2022}$, utilizing $\text{WPF}$ and $\text{CefSharp 107+}$.
* **Distribution:** Installer package is available via GitHub Releases.
* **System Requirements:** Requires **Windows 10/11**, $\text{.NET 6/7}$, and $\text{CefSharp}$ dependencies.

### **Notes**
* Always use the **Menu > Reload Page** option instead of $\text{Ctrl} + \text{R}$.
* For maximum security features, run the application as **Administrator**.
* To open the Chromium settings without closing the main application, launch the executable with the $\text{--open-settings}$ argument.
