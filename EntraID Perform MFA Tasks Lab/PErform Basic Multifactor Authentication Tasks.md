# Lab Report: Perform Basic Multifactor Authentication Tasks

**Owner:** Marlon guedes de Wäckerle 
**Date:** May 17, 2026  
**Course/Lab:** Microsoft Entra ID - Multifactor Authentication (MFA)  
**Estimated Duration:** 10 minutes

## Objective
Explore the MFA setup process and configure a basic MFA deployment using **Per-user MFA** settings in Microsoft Entra ID.

---

## Task 1 - Enable / Disable Per-user MFA Settings

**Steps Performed:**

1. Opened the **Microsoft Entra admin center** at [https://entra.microsoft.com](https://entra.microsoft.com).
2. Logged in using the tenant credentials.
3. From the left menu, navigated to **Identity** > **Users** > **All users**.
4. In the top menu, selected **Per-user MFA**.
5. Selected the checkbox next to **Bhogeswar Kalita**.
6. Clicked **Enable MFA** from the top menu.
7. Reviewed the information message box (contains the MFA registration URL that can be sent to the user).
8. Clicked **Enable** to confirm.

**Result:**  
After a few seconds, the status for **Bhogeswar Kalita** changed to **Enforced**.

**Screenshots**

## Task 2 - Review the Service Settings for MFA

**Steps Performed:**

1. Returned to **Identity** > **Users** > **All users**.
1. Returned to **Identity** > **Users** > **All users**.
2. Clicked **Per-user MFA** again.
3. Selected **Service settings**.

### Settings Reviewed:

| Setting                                      | Purpose |
|----------------------------------------------|---------|
| **App passwords**                            | Allows users to generate app passwords for legacy applications that do not support modern MFA. |
| **Trusted IPs**                              | Define IP address ranges that are considered safe, allowing users to bypass MFA when logging in from these locations. |
| **Verification options**                     | Choose which second-factor authentication methods users can use (e.g., phone call, SMS, authenticator app, etc.). |
| **Remember multifactor authentication on trusted devices** | Allows users to skip MFA for a specified number of days on trusted devices. |

- If any changes were made during review, clicked **Discard** to keep default settings.

**Screenshots**

## Summary

In this lab, the following was successfully completed:

- Enabled **Per-user MFA** for **Bhogeswar Kalita** (Status changed to **Enforced**)
- Reviewed key **Service settings** for MFA configuration
- Understood legacy app support, trusted IPs, verification methods, and remember MFA options

This exercise demonstrated the classic **Per-user MFA** management method in Microsoft Entra ID.

> **Note:** Per-user MFA is the legacy method. Modern recommended approach uses Conditional Access policies for better security and flexibility.

---

**End of Lab Documentation**