# Lab Report: Implement and Test a Conditional Access Policy

**Owner:** Marlon Guedes de Wäckerle 
**Date:** May 17, 2026  
**Course/Lab:** Microsoft Entra ID - Conditional Access Policy  
**Estimated Duration:** 20 minutes  
**Login Type:** Microsoft Entra ID Admin

## Lab Scenario
The organization needs to limit user access to internal applications using Microsoft Entra ID Conditional Access policies.

---

## Exercise 1 - Set a Conditional Access Policy to Block DebraB from Accessing Sway

### Task 1 – Confirm DebraB Has Access to Sway (Before Policy)

**Steps Performed:**

1. Opened a new **InPrivate** browser window.
2. Navigated to [https://www.office.com](https://www.office.com).
3. Signed in as:  
   **Username:** `DebraB@marlonozlive843.onmicrosoft.com`  
   **Password:** (Provided lab password)
4. Skipped welcome/introduction screens.
5. Opened the **Apps** page and successfully launched **Sway**.
6. Logged out and closed the browser.

---

### Task 2 - Create a Conditional Access Policy

**Updated Navigation (2026):**

1. Go to **[https://entra.microsoft.com](https://entra.microsoft.com)**.
2. In the **search bar at the top**, type `Conditional Access` and select it.

**Policy Creation Steps:**

1. Click **+ Create new policy**.
2. In the **Name** box, enter:  
   **`Block Sway for DebraB`**

   **Screenshots**

#### Assignments

**Users and Groups:**
- Under **Include**, select **Users and groups** → Check **Users and groups**.
- Search and select **DebraB** → Click **Select**.

**Target Resources:**
- Click **No target resources selected**.
- Ensure **Cloud apps** is selected.
- Click **Select apps** → Click **None**.
- Search for `Sway`, check the box, and click **Select**.

#### Access Controls

- Under **Grant**, click **0 controls selected**.
- Select **Block access** → Click **Select**.

#### Enable Policy

- Set **Enable policy** to **On**.
- Click **Create**.

---

### Task 3 - Test the Conditional Access Policy

**Steps Performed:**

1. Opened a new **InPrivate** browser window.
2. Navigated to [https://sway.cloud.microsoft](https://sway.cloud.microsoft).
3. Attempted to sign in as:  
   **Username:** `DebraB@marlonozlive843.onmicrosoft.com`
4. Verified that access to **Sway** was **blocked** by the Conditional Access policy.

> **Note:** If still signed in, log out completely, wait 1 minute, and try again.

---

## Exercise 2 - Test Conditional Access Policies with “What If” Tool

**Steps Performed:**

1. Returned to the **Conditional Access** page in Entra admin center.
2. In the left menu, selected **Policies** → Clicked **What If**.
3. Under **User or Workload identity**, selected **DebraB**.
4. Under **Cloud apps, actions, or authentication context**, selected **Sway**.
5. Clicked **What if**.
6. Reviewed the report showing:
   - **Policies that will apply** → `Block Sway for DebraB`
   - **Policies that will not apply**

---

## Final Cleanup

1. Returned to the **Block Sway for DebraB** policy.
2. Changed **Enable policy** to **Off**.
3. Clicked **Save**.

---

## Summary

Successfully completed:
- Confirmed DebraB had access to Sway before the policy
- Created a Conditional Access policy to **block DebraB** from **Sway**
- Tested the policy (access denied)
- Used the **What If** tool to simulate policy behavior

**Key Learning:** Conditional Access policies allow granular control over application access based on users, apps, and other signals.

---

**End of Lab Documentation**

*Document generated for lab submission / personal record.*