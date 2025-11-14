# SMS Forge: The Swiss Army Knife of SMS

![SMSForge](https://github.com/user-attachments/assets/a72b7290-a991-48ab-bab8-23e8075b5031)

First, we need to talk about what SMS Forge is (and isn't).

SMS Forge isn't a conventional SMS application; it wasn't designed as an SMS manager, nor to be used as a replacement for system SMS applications, nor even to receive SMS (with a few exceptions). SMS Forge is a project I've had in mind since the pre-Android era, strongly inspired by the old management software "floAt's Mobile Agent," where I first learned how complex and rich SMS really was, and how extremely limited current SMS applications are. Today, IM has largely replaced the old SMS system, but for many enthusiasts, like myself, we can say that better late than never.

Throughout Android's history, we've been fortunate enough to see a few developers explore the feasibility of creating "advanced" SMS applications, most notably the well-known Class 0 SMS (also known as Flash SMS). Unfortunately, while Google's original APIs allowed developers to create applications for this, they were removed long time ago. This is the case with older apps like FlashSMS, which could work on a very limited number of devices. Somewhat later, and thanks primarily to rooted devices and the EdXposed framework, apps like HushSMS or GAT-App emerged, using EdXposed to intercept internal Android calls that were still available. Unfortunately, again, this was limited not only to having a rooted device, but also to using EdXposed (sometimes a headache for those who use banking apps) and only for older Android versions.

This is where SMS Forge was born, thanks, as I say, to the vision that the FMA developers had many years ago. The goal of SMS Forge is to have a simple tool on our devices capable of sending a wide range of different SMS messages, taking advantage of the richness of GSM standards, and supporting up to day Android devices. All of this breaks down some of the barriers that existed years ago, like limiting its use to a "few" devices. This doesn't mean that SMS Forge can be used on any device (I wish it were). The bad news is that SMS Forge will still require a rooted device for now. The good news, on the other hand, is that it won't require EdXposed or any Magisk Module, only root permissions. Of course, it's compatible with modern versions of Android (tested up to A15). It was initially designed for Android 9 and later, although this shouldn't be a problem if there's significant interest in using older Android versions.

As will be explained later in the FAQ, each manufacturer/device may have different peculiarities that may cause SMS Forge to have some limitations, or be completely incompatible. The idea in the future is to explore different ways to try to maximize compatibility, possibly even including some devices without root. Similarly, when we send an SMS from SMS Forge, we can never guarantee or ensure how the receiving device will interpret it. For example, a Class 0 SMS on a Samsung/Xiaomi device with an A15 will be displayed directly on the screen, allowing us to see both the sender and the option to save it; on iOS, neither the name nor the option appears. Other types of SMS may be directly discarded by the device or have no effect.

The project is far from being finalized; the idea is to continue implementing features, greater control over sending options, and seeking viable alternatives to some existing limitations. Initially, the project will likely be licensed commercially and published on Google Play (there's always the option to ban it). Depending on various factors, I may eventually change my mind and publish it completely openly.
<p> </p>


## Download SMS Forge

Experience the true power of your device's modem.

<div align="left">
    <!-- Insignia oficial de Google Play -->
    <a href="https://play.google.com/store/apps/details?id=es.theliel.smsforge">
        <img alt='Disponible en Google Play' src='https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png' width="200"/>
    </a>
    <p style="margin-top: 10px; font-size: 14px; color: #888;">*Available coming soon</p>
</div>
<p> </p>

# Implemented Features and To-Do

Already Implemented:

+ All SMS Class: 0(Flash)/1(ME)/2(SIM)/3(Reserved)
+ Replace SMS
+ Auto-Delete SMS
+ Message Waiting Indicator: DCS or UDH
+ Silent/Ping SMS: Type 0, MWI, or MMS Notification
+ SMS WAP Push SI / SL
+ SMS for MMS Notification
+ RAW SMS (PDU)
+ Additional settings: SMSC, Valid-Period (Relative/Absolute/Enhanced), PID Selector,
  Message Reference, Reply-Path, Status Report (See FAQ), Reject Duplicate
+ National/International Number Support
+ Automatic charset detection (GSM7/160ch. UCS2/70ch)
+ Light/Dark Theme Support
+ Qualcomm / Mediatek Support (probably other SoCs too)
+ Interface redesign
+ English / Spanish translations


To-Do

- Translation into other languages
- Perhaps a permanent way to work around the limitations of current status reports
- Long SMS (Concatenation)
- Manual Encoding Enforcing (7Bit/8Bit/UCS2)
- More WAP SMS
- SMS Compression?
- More to come...

<p> </p>

# Limitations

As explained, there are some limitations that may prevent partial or complete use of SMS Forge. Some of these are easily remedied and are due to the inability to individually check the compatibility/behavior between the different devices currently on the market, different SoCs, and Basebands. Originally, the idea was to release a testing app to check if the device would be compatible, but I think in the end it was a much better idea to release only one app, where the user can still test the basic functionality before getting the full version, if they so choose. If your device dont seem to work, you always can attach a report to see if it can be implemented. Please visit the Wiki for more information about it.

Currently, it has been tested on several devices with Qualcomm SoCs of different generations, and some MediaTek devices. MediaTek devices are a bit more complex, and although it's fully functional in our tests, you may encounter some bugs. Please feel free to open a bug report if you find any issues.
<p> </p>


<h2>🗺️ Wiki Navigation</h2>
<table style="width:100%; border-collapse: collapse; border: 1px solid #ddd;">
    <thead>
        <tr style="background-color: #f2f2f2;">
            <th style="padding: 10px; border: 1px solid #ddd; text-align: left; width: 30%;">Section</th>
            <th style="padding: 10px; border: 1px solid #ddd; text-align: left;">Description</th>
        </tr>
    </thead>
    <tbody>
         <tr>
            <td style="padding: 10px; border: 1px solid #ddd;"><strong><a href="https://github.com/Theliel/SMSForge/wiki">Wiki Home</a></strong></td>
            <td style="padding: 10px; border: 1px solid #ddd;">The starting point for all documentation relating to SMS Forge, feel free to report any errors you may find in it.</td>
        </tr>
        <tr>
            <td style="padding: 10px; border: 1px solid #ddd;"><strong><a href="https://github.com/Theliel/SMSForge/wiki/01.-User-Guide">User Guide</a></strong></td>
            <td style="padding: 10px; border: 1px solid #ddd;">Step-by-step instructions for using the application's interface and features.</td>
        </tr>
        <tr>
            <td style="padding: 10px; border: 1px solid #ddd;"><strong><a href="https://github.com/Theliel/SMSForge/wiki/02.-Core-Concepts">Core Concepts</a></strong></td>
            <td style="padding: 10px; border: 1px solid #ddd;">Simple explanations of key terms like PDU, AT Commands, TP-PID, MWI, and SMS Classes.</td>
        </tr>
        <tr>
            <td style="padding: 10px; border: 1px solid #ddd;"><strong><a href="https://github.com/Theliel/SMSForge/wiki/03.-Compatibility">Compatibility</a></strong></td>
            <td style="padding: 10px; border: 1px solid #ddd;">Detailed guide on selecting the correct modem device and troubleshooting compatibility issues. <strong>(Critical for first-time setup)</strong></td>
        </tr>
        <tr>
            <td style="padding: 10px; border: 1px solid #ddd;"><strong><a href="https://github.com/Theliel/SMSForge/wiki/04.-FAQ-&-Known-Issues">FAQ & Known Issues</a></strong></td>
            <td style="padding: 10px; border: 1px solid #ddd;">Answers to frequently asked questions about licensing, usage, and known issues.</td>
        </tr>
        <tr>
            <td style="padding: 10px; border: 1px solid #ddd;"><strong><a href="https://github.com/Theliel/SMSForge/wiki/05.-Privacy-Policy,-Data-and-Permissions">Privacy Policy, Data and Permissions</a></strong></td>
            <td style="padding: 10px; border: 1px solid #ddd;">Everything about privacy policy, data collection and retention, and permissions exposed</td>
        </tr>
        <tr>
            <td style="padding: 10px; border: 1px solid #ddd;"><strong><a href="https://github.com/Theliel/SMSForge/wiki/06.--Terms-of-Service-and-EULA">Terms of Service and EULA</a></strong></td>
            <td style="padding: 10px; border: 1px solid #ddd;">ToS and EULA, as the section itself specifies</td>
        </tr>
    </tbody>
</table>
