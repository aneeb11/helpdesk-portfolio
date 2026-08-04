# Ticket Resolution: INC0012847 — Cannot Access Shared Drive

**Assignee:** aneeb11
**Reported by:** Sarah Mitchell (smitchell@servicedesk-simulator.com)
**Department:** Marketing | Remote (Working from home) | x4892
**Priority:** High
**Date Resolved:** 2026-08-04

## Issue Description

User could not access the Marketing shared drive while working from home, receiving "The network path was not found" when trying to open it. Internet and email worked normally. Mapped drives showed as disconnected. User had already restarted her computer with no change.

## Business Impact

Q1 campaign materials deadline is EOD tomorrow. Unable to access marketing campaign files without shared drive access.

## Root Cause

User's VPN client was disconnected. The Marketing shared drive lives on an internal company file server that is only reachable through the VPN tunnel when working remotely. Without VPN, there is no network route to the file server, so the mapped drive showed disconnected and any attempt to open it failed with "network path not found."

## Resolution Steps Taken

1. Connected to the user's PC via Tools → Remote Support.
2. Opened the VPN Client app, found it showing DISCONNECTED, and clicked Connect.
3. Retrieved the Marketing UNC path from Tools → Documentation → File Server.
4. Opened File Explorer → This PC → Map network drive.
5. Mapped drive letter D: to the Marketing UNC path and clicked Map Drive.
6. Opened the drive and confirmed folder contents loaded successfully for the user.

## Outcome

Resolved — VPN reconnected, Marketing drive remapped to D: and confirmed accessible.

## Screenshots

![Solved ticket](screenshots/solved-ticket.png)

![Chat confirmation](screenshots/chat-confirmation.png)
