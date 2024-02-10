# Integration of Google Auth's Less Secure App Password for Login



Our app uses Google auth for login and registration, you don't need to register in our app, you can directly login in our application using your Google third party (aka less secure app) passwords.



To integrate Google Auth's less secure app password for login without requiring users to register, follow these steps:

## 1. Enable 2-Step Verification

- Go to your Google Account settings.
- Select "Security."
- Under "Signing in to Google," choose "2-Step Verification."

## 2. Generate an App Password

- In the "Security" settings, navigate to "App passwords."
- Enter a name to identify where you'll use the app password.
- Select "Generate" to create a 16-character app password.
- Follow the on-screen instructions to use this password for authentication.
- Once done, you can proceed with login using the app password.

## 3. Troubleshooting

## If you can't find the option to add an app password, ensure:

- 2-Step Verification isn't set up only for security keys.
- You're not logged into a work, school, or organizational account.
- Your Google Account doesn't have Advanced Protection enabled.



Remember, users typically need to enter an app password once per app or device in one session, **make sure to save your password somewhere - once lost - you may need to create new**, this process ensures secure access to your app while maintaining user convenience.

For further assistance or troubleshooting, refer to [Google's support documentation](https://support.google.com/accounts/answer/185833).



# Additional Links:
- [Understanding Api Responses](https://github.com/Untoldhacker-Dev/mailapp-docs/blob/main/understaning%20api%20responses.md)
- [Playing with the Api](https://github.com/Untoldhacker-Dev/mailapp-docs/blob/main/cubeton%20mailapp.md)
- Some users - if they've done this before, can [click on this link](https://accounts.google.com/signin/v2/challenge/pk/presend?TL=AHNYTISyxZxdow8C2FbLUMXAFKJq8Kho3poCRyNprsLT3kNYqQe7GdmuR9-nGGzH&cid=1&continue=https%3A%2F%2Fmyaccount.google.com%2Fapppasswords&ifkv=ASKXGp0Kv3PQhjhZVzHn1TCnjbSWzSgcbN0LWyAf1AmKvUlGSCEmfZlf3qWt22cSssEJN8RakQesJw&rart=ANgoxcfCVAk3qaLNBRSmm-zzJGc8ij147P1HsZj9DceWu_hKb8v_3IsACE2_clmN6F_WKu7-r4tj4DqMIbyj8bWZh3Nxbwaam2jGJLs7CQDG9qR0uqtum-Y&rpbg=1&sarp=1&scc=1&service=accountsettings&theme=glif&flowName=GlifWebSignIn&flowEntry=ServiceLogin) to be directly redirected to the page for generating app password (make sure to choose the correct account on Google's login page).
- [This page](https://security.google.com/settings/security/apppasswords?utm_source=OGB&pli=1) is direct access to the app passwords page for Google account (compatible only for some users)
