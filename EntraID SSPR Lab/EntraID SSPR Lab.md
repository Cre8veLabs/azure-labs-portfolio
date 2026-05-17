# Lab Report: Configure and Deploy Self-Service Password Reset (SSPR)

**Owner:** Marlon Guedes de Wäckerle
**Date:** May 17, 2026  
**Course/Lab:** Microsoft Entra ID - Self-Service Password Reset  
**Estimated Duration:** 15 minutes

## Lab Scenario
The company has decided to empower employees by enabling **Self-Service Password Reset (SSPR)**. This lab configures and tests SSPR in a controlled rollout.

---

## Exercise 1 - Create a Group with SSPR Enabled and Add Users

### Task 1 - Create a Group to Assign SSPR

**Steps Performed:**

1. Opened the **Microsoft Entra admin center**.
2. Navigated to **Identity** > **Groups** > **All groups**.
3. Clicked **New group**.

**Group Configuration:**

| Setting            | Value                  |
|--------------------|------------------------|
| **Group type**     | Security               |
| **Group name**     | SSPRTesters            |
| **Group description** | Testers of SSPR rollout |
| **Membership type**| Assigned               |
| **Members**        | Alex Wilber<br>Allan Deyoung<br>Bianca Pisani |

4. Clicked **Create**.

**Screenshots**

### Task 2 - Enable SSPR for the Test Group

**Steps Performed:**

1. Navigated to **Identity** > **Protection** > **Password reset**.
2. On the **Properties** page:
   - Set **Self service password reset enabled** to **Selected**.
   - Selected the group **SSPRTesers** (replaced the default group).
3. Clicked **Save**.

**Screenshots**

4. Reviewed the default settings under the following sections:
   - **Authentication methods**
   - **Registration**
   - **Notifications**
   - **Customization**

> **Note:** Ensured **Phone** is selected as one of the authentication methods.

--- 

### Task 3 - Register for SSPR with Allan Deyoung

**Steps Performed:**

1. Opened a new InPrivate/Incognito browser session.
2. Navigated to [https://aka.ms/ssprsetup](https://aka.ms/ssprsetup).
3. Signed in as `AllanD@<your-domain>.onmicrosoft.com`.
4. Updated the password if prompted and recorded the new password.
5. Completed the **More information required** setup.
6. Set up **Microsoft Authenticator** app by scanning the QR code.
7. Completed registration and closed the browser.

> **Note:** This process registered the user for both **SSPR** and **MFA**.

---

### Task 4 - Test SSPR

**Steps Performed:**

1. Opened a new InPrivate/Incognito browser.
2. Went to [https://portal.azure.com](https://portal.azure.com).
3. Entered `AlexW@<your-domain>.onmicrosoft.com`.
4. Clicked **Forgot my password**.
5. Followed the SSPR flow:
   - Verified identity using Microsoft Authenticator.
   - Created and confirmed a new password.
6. Signed in successfully with the new password using Allan Deyoung’s account.
7. Closed the browser.

---

## Summary

Successfully completed the following:
- Created a pilot security group (**SSPRTesers**)
- Enabled Self-Service Password Reset for the selected group only
- Registered a user for SSPR + MFA
- Successfully tested password reset

This configuration allows a controlled and secure rollout of Self-Service Password Reset in the organization.

---

**End of Lab Documentation**
