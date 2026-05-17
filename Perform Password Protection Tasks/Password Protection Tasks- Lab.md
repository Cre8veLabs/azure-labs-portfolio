# Lab Report: Exercise - Perform Password Protection Tasks

**Owener:** Marlon Guedes de Wäckerle 
**Date:** May 17, 2026  
**Course/Lab:** Microsoft Entra ID - Password Protection  
**Estimated Duration:** 5 minutes

## Objective
Explore the capabilities Microsoft Entra ID offers for protecting passwords. Automate and enforce strong passwords and use login restrictions to prevent password attacks.

## Task 1 - View Lock Settings and Review Duration and Threshold Values

### Steps Performed:

1. Opened the **Microsoft Entra admin center** at [https://entra.microsoft.com](https://entra.microsoft.com).
2. Logged in using the tenant credentials.
3. From the left menu, navigated to **Protection** > **Authentication methods**.

   *(Alternative: Used the search bar at the top and searched for "Password protection")*

4. Selected **Password protection** from the list.

### Configuration Applied:

#### Custom Smart Lockout Settings

| Field                | Value | Description |
|----------------------|-------|-------------|
| **Lockout threshold** | 10     | Number of failed login attempts before the account is locked. |
| **Lockout duration**  | 60    | Duration (in seconds) the account remains locked after reaching the threshold. |

**Screenshots**

#### Custom Banned Password List

- **Enforce custom list**: Set to **Yes**
- **Banned passwords added**:
  - `Could not proceed by account limitations 

  **Screenshots**

- **Mode**: Set to **Enforced**
- Clicked **Save** at the top of the screen.

## Summary
Successfully configured Microsoft Entra ID Password Protection with:
- Smart Lockout (threshold: 10 attempts, duration: 60 seconds)
- Custom banned password list in **Enforced** mode 

This setup helps prevent brute-force attacks and blocks common/weak passwords related to the organization.

---

**End of Lab Documentation**
