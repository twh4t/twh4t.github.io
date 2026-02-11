# A Fake Courier App Almost Compromised My Friend’s PhonePe

A few weeks ago, a senior friend called me in panic. Her phone was sending SMS messages automatically to unknown numbers. On top of that, her PhonePe account suddenly logged out, and she was worried someone had logged into her account from another phone.

Here’s what happened.

She received a WhatsApp message from an unknown person claiming to be from a courier service. Since she had missed a delivery earlier, she trusted the message and installed the app from the link they sent. The app wasn’t from the Play Store.

<img width="250" height="250" alt="apk" src="https://github.com/user-attachments/assets/fce215e7-a64e-4248-8849-5858c9482234" />

After installing it, she logged into PhonePe inside the app. Soon after, the app disappeared from her home screen, her phone started sending SMS automatically, and her PhonePe logged out. That’s when she realized something was wrong.

<img width="300" height="300" alt="app_interface" src="https://github.com/user-attachments/assets/53bb9f97-4782-4f75-b22e-bc8c51dcb098" />

I connected her phone using ADB and found a hidden, unknown app running in the background. After removing it, the strange SMS activity stopped.

This was a classic mobile phishing attack:

- Social engineering using a fake courier story  
- A malicious app sent via WhatsApp  
- A fake login screen to steal PhonePe credentials  
- Hidden app behavior to avoid detection  

## What We Learned

- Never install apps from WhatsApp or SMS links  
- Always verify courier messages using official apps or websites  
- Don’t log into financial apps through third-party links  
- If an app hides itself, assume it’s malicious  
- Enable transaction alerts and Play Protect  
