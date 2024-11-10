---
title: 'How SSOBridge works'
layout: '~/layouts/MarkdownLayout.astro'
---

### **SSOBridge Demo**

**SSOBridge** is a service that simplifies Single Sign-On (SSO) integration for scala applications. With SSOBridge, your app can authenticate users across multiple identity providers (e.g., Google, Okta, Microsoft Azure) using standardized protocols like **SAML** or **OAuth2**.
This ensures that users only need one set of login credentials across different platforms, improving security and user experience.

#### **How SSOBridge Works**:

1. **User Login Request**: A user tries to log in to an app using SSO.
2. **SSOBridge Redirection**: The app redirects the user to SSOBridge, which connects with an external Identity Provider (e.g., Google, Okta).
3. **Authentication**: The Identity Provider authenticates the user and returns an authentication token.
4. **Token Validation**: SSOBridge validates the token and sends the user back to the app with secure credentials.
5. **Access Granted**: The user is logged in to the app.

![PlantUML Diagram](https://www.planttext.com/api/plantuml/png/NP3FRi8m38VlUGghTrwWXuco0qAQD4G5To-nm6gN5CS5yVR4bUZeJldZJvz_zZehYew_lKElIU2OITnGljZpW56XQeQX0inGpcMXRRytmk5CKtb-BQ5TeAYi3zXBkd4WcU1Ts3jdhM3rOU8QFdlsNORgAvqvmftrOiRAbQ8nixs60mKMyWgQtfhEDwEBleQMOW0SzM81F2gd24BNaRAw0lopDdyWmMXBM1ZVo1Fs78pIr55SOjCeSq3Jm0_wxZM5JLp3Lcmpw3tbxDownBJrFm40)

---
### **Schema: SSOBridge Flow**

```plaintext
1. User clicks "Login with SSO" in the app
           |
           V
2. App redirects to SSOBridge
           |
           V
3. SSOBridge sends request to Identity Provider (e.g., Okta)
           |
           V
4. Identity Provider authenticates user
           |
           V
5. SSOBridge receives token, validates it
           |
           V
6. SSOBridge redirects user back to the app
           |
           V
7. App grants access to the user