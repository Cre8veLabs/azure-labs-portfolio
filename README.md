# 02 - User Creation in Entra ID

**Date:** 15 May 2026  
**Tenant Name:** marlonozlive843.onmicrosoft.com  
**Student Name:** Marlon Guedes de Waeckerle

## Objective
Create a single user manually and then perform a bulk user creation using a CSV file.

---

## Part 1: Create a Single User (Manual)

### Steps Performed

1. Logged into the [Azure Portal](https://portal.azure.com)
2. Navigated to **Microsoft Entra ID**
3. In the left menu, clicked on **Users** → **New user**

4. Filled in the following information:

   - **User principal name (UPN)**: Bhogeswar Kalita
   - **Mail nickname**: `bhogeswar.kalita`
   - **Display name**: `Bhogeswar Kalita`
   - **First name**: Bhogeswar
   - **Last name**: Kalita
   - **Password**: Qugo196098 (Auto-generated)
   - **Account enabled**: Yes

5. Clicked **Review + create** → **Create**

### Verification
- User appeared in the Users list
- Could successfully sign in with the temporary password

**Folder Entra ID Lab documentation - Screenshot:**

![User Creation and Details](screenshots/Single-User-Creation.png)

---

## Part 2: Bulk User Creation using CSV File

### Steps Performed

1. In **Microsoft Entra ID** → **Users** → clicked **Bulk operations** → **Bulk create**

2. Downloaded the sample CSV template

3. Prepared the CSV file with the following columns and data:

**CSV File: **
![CSV File APL0501-BilkUser] (APL0501-BulkUser)


4. Uploaded the completed CSV file
5. Clicked **Create** and waited for the processing to finish

6. **Folder Entra ID Lab documentation - Screenshot:**

![BulkUser Creation and Details](screenshots/BulkUser-Creation.png)

### Verification

- All 10 users were successfully created
- All users have the domain `@marlonozlive843.onmicrosoft.com`
- Users appear in the **Users** list with status **Enabled**

**Screenshots:**
![User Creation and Details](screenshots/Single-User-Creation.png)

![Bulk Operation Result](screenshots/02-05-result-success.png)

---

Basic Powershel Script Create User
# 1. Connect to Microsoft Graph
Connect-MgGraph -Scopes "User.ReadWrite.All", "Directory.ReadWrite.All"

# 2. Create the user
New-MgUser `
    -DisplayName "Bhogeswar Kalita" `
    -UserPrincipalName "bhogeswar.kalita@marlonozlive843.onmicrosoft.com" `
    -MailNickname "bhogeswar.kalita" `
    -GivenName "Bhogeswar" `
    -Surname "Kalita" `
    -PasswordProfile @{
        Password = "Qugo196098"
        ForceChangePasswordNextSignIn = $false
    } `
    -AccountEnabled $true `
    -UsageLocation "CH"          # Switzerland
