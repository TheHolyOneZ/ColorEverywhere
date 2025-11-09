# ColorEverywhere
**ColorEverywhere** is a powerful and intuitive Discord Extension/Addon designed to give you complete control over the embed colors in your server. Instead of having random or default embed colors, you can assign a specific hex color to each channel, ensuring a clean, consistent, and customized look.
> 💡 **Built for the Zygnal Ecosystem — to download and use this extension, you must be part of the Zygnal Ecosystem.**  
> This extension (cog) is part of the **Zygnal Ecosystem** and is only available through its supported platforms.  
> You can use it with:  
> - The **[Discord Bot Framework](https://github.com/TheHolyOneZ/discord-bot-framework)** — ideal for developers who want full control and flexibility *(includes an integrated extension marketplace)*, or  
> - The **[ZygnalBot](https://zygnalbot.de)** — a prebuilt, plug-and-play Discord bot *(also includes an integrated extension marketplace)*.  
>
> Browse and install extensions at [zygnalbot.com/extension](https://zygnalbot.com/extension).  
> For help or community discussions, join us on Discord: [discord.gg/sgZnXca5ts](https://discord.gg/sgZnXca5ts)
# 🎨 ColorEverywhere Discord Extension/Addon

**ColorEverywhere** is a powerful and intuitive Discord Extension/Addon designed to give you complete control over the embed colors in your server. Instead of having random or default embed colors, you can assign a specific hex color to each channel, ensuring a clean, consistent, and customized look.

This extension is perfect for servers that want to maintain a specific theme or simply organize information with color-coded embeds.

> **Credits:** The original source code was created by **lqwn** and has been significantly modified and enhanced by **TheHolyOneZ**.

***

## Features

* **Custom Color Per Channel**: Assign a unique hex color to embeds in any channel you choose.
* **Easy Admin Panel**: A simple, button-based control panel for all settings. No complex commands to remember.
* **Bulk Management**: Add, edit, or remove multiple channel configurations at once with a simple message format.
* **Detailed Status View**: Instantly see which channels are being monitored and what color is assigned to each.
* **Persistent Settings**: The bot saves your configuration, so your settings are safe even after a restart.
* **Dual Command Support**: Works with both modern slash commands (`/colors`) and traditional prefix commands (`!colors`).
* **Smart Color Validation**: Automatically checks for valid hex color codes and even supports shorthand (e.g., `#FFF`).

***

## How to Use

The extension is controlled entirely through one simple command, which is only available to server administrators.

### The Command: `/colors` (or `!colors`)

Using this command will bring up the main control panel with three buttons.

* **Add/Edit Channels**:
    1.  Click this button.
    2.  The bot will ask you to send a message listing the channels and the hex colors you want to assign.
    3.  Reply with each channel and color on a new line. If a channel is already configured, this will update its color.
        ```
        #announcements, #FFD700
        #rules, #C0C0C0
        #general, #7289DA
        ```
    4.  The bot will confirm which channels were added or updated.

* **Remove Channels**:
    1.  Click this button.
    2.  The bot will ask which channels you want to stop monitoring.
    3.  Mention the channels you want to remove in a reply, separated by commas.
        ```
        #general, #bot-commands
        ```
    4.  The bot will confirm the channels are no longer being monitored.

* **View Settings**:
    * Click this button to get a clean, organized overview of all channels currently managed by ColorEverywhere and their assigned colors.

***

### ⚠️ Very Important Note

For the extension to work, it must have the **Manage Messages** permission in the channels you want it to monitor. More importantly, **the bot can only change the embed color of messages that it sends itself**. It cannot edit messages sent by other users or other bots.





# 🎨 ColorEverywhere - Changelog

This document outlines the major changes between the original version of the extension and the heavily modified version.

***

## Version 1.0 - "The Original" (by lqwn)

This was the initial release, focused on a single, simple goal: making all embeds in specified channels a uniform color.

### Key Features:
* **Uniform Color:** Automatically changed all embeds in monitored channels to a single, hard-coded color (`#FFFFFF`).
* **Channel Monitoring:** Admins could add or remove channels from a monitoring list.
* **Simple Setup:** Required only a list of channels to start working.
* **Basic Controls:** Provided a simple admin panel with "Add," "Remove," and "Status" buttons.

***

## Version 2.0 - "The Customizer" (Modified by TheHolyOneZ)

This version represents a complete overhaul of the original concept, shifting from uniformity to full customization and control.

### ✨ Added
* **Custom Color Per Channel:** The core feature change. Admins can now assign any valid hex color to any specific channel.
* **Bulk Editing:** Added the ability to add, edit, and update multiple channels and their colors in a single command.
* **Hex Color Validation:** The bot now intelligently checks if a provided color is a valid 3-digit or 6-digit hex code.
* **Detailed Status Panel:** The status view was redesigned to group channels by their assigned color, giving a much clearer overview of the server's configuration.

### 🔄 Changed
* **Functionality Shift:** Moved from a "one-color-for-all" system to a "unique-color-per-channel" system.
* **Admin Workflow:** The process for adding channels now requires both a channel mention and a hex color code (e.g., `#channel, #hexcolor`).
* **UI Text:** All bot messages and instructions were updated to reflect the new, more advanced functionality.
* **Backend Logic:** The data storage and message processing logic were completely rewritten to handle a dictionary of channels and their unique colors instead of a simple list.

### Key Differences at a Glance:

| Feature              | Version 1.0 (lqwn)             | Version 2.0 (TheHolyOneZ)                               |
| -------------------- | ------------------------------ | ------------------------------------------------------- |
| **Color System** | One color for all channels     | Unique color for each channel                           |
| **Admin Input** | Just provide channel names     | Provide channel name AND a hex color                    |
| **Customization** | None (always white)            | Full hex color customization                            |
| **Status View** | Simple list of channels        | Detailed, color-grouped list of channels                |
| **Core Logic** | Simple list management         | Complex dictionary management with color validation     |
