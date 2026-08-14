# Proserpina Security Policy

These recommendations are intended to reduce privacy and security risks when using Proserpina in untrusted or restricted network environments, including when interacting with online services.

**Important:** These recommendations do not make the user completely anonymous or invulnerable. They are intended to reduce the amount of exposed data, limit trust in third-party services, and mitigate the consequences of a potential system compromise. Choose security measures according to your own threat model.

## Security recommendations

1. **Use full-disk encryption.**
   Enable disk encryption with LUKS during system installation. This protects your data from unauthorized access when the computer is powered off or locked.

2. **Use additional encryption for sensitive data.**
   Encrypt files and directories containing personal, work-related, or otherwise sensitive information with `encrypt-decrypt` (AES-256), even if the system disk is already encrypted.

3. **Use only trusted repositories for system updates.**
   Whenever possible, use official and trusted software sources. Avoid unknown third-party repositories and unverified mirrors. If a third-party mirror is necessary, verify package and repository cryptographic signatures.

4. **Minimize the amount of sensitive information provided to search engines and voice assistants.**
   Do not provide personal, professional, or otherwise sensitive information to third-party search engines, voice assistants, or similar services unless necessary.

5. **Use Censor to filter unwanted content.**
   Configure Censor to block potentially harmful, unwanted, or toxic resources. Keep in mind that content filtering is not an anonymity mechanism.

6. **Use secure network connections when working in an untrusted network environment, if required by your threat model.**
   Proserpina provides various tools for establishing secure network connections. Choose the appropriate technology according to your threat model.

7. **Keep personal and work-related digital identities separate.**
   Whenever possible, use separate accounts, browser profiles, or dedicated working environments for different categories of services. Avoid unnecessarily sharing cookies, browsing history, saved passwords, and other identifiers between environments.

8. **Minimize your presence on services you do not trust.**
   Do not publish personal, professional, or sensitive information there. Whenever possible, avoid using the same accounts or identifiers across unrelated services.

9. **If you are required to use the MAX messenger, run it inside MaxContainer.**
   `MaxContainer` isolates MAX and restricts its interaction with the host system, including access to devices, audio/video, DBus, and the filesystem.

   **Do not consider the container a guarantee of complete anonymity or security of MAX itself.** Its primary purpose is to reduce the application's potential impact on the host system and user data.

10. **Do not grant applications unnecessary permissions.**
    Access to the camera, microphone, contacts, files, location, and other resources should only be granted when actually required.

11. **Do not use third-party services to store sensitive data unless necessary.**
    Avoid synchronizing documents, photos, contacts, passwords, browser history, and other sensitive data with external services unless there is a specific need to do so.

12. **Do not install untrusted software.**
    Do not run RPM packages, scripts, browsers, network clients, or other software obtained from unverified sources, including social networks, messengers, forums, and random file-sharing sites.

13. **Do not install unknown root certificates.**
    If a website or application asks you to install an additional CA certificate, determine who issued it and why it is required. Installing an unknown root certificate adds a new trusted certificate authority to your system.

14. **Use unique passwords and multi-factor authentication.**
    Do not reuse the same password across different services. Use MFA, passkeys, or hardware security keys for important accounts whenever available.

15. **Do not store passwords, tokens, or cryptographic keys in plain text.**
    SSH keys, API tokens, cookies, MFA recovery codes, and other secrets should not be stored in ordinary text files, publicly accessible directories, or scripts.

16. **Do not open suspicious links or attachments.**
    Be particularly careful with documents and executable files received via email, messengers, and social networks.

17. **Do not respond to suspicious messages.**
    Even a simple reply can confirm that an email address or account is active. If in doubt, verify the sender through an independent communication channel.

18. **Create regular backups.**
    Keep backups of important data separately from the primary system. Ideally, maintain at least one backup that is not permanently connected to the computer.

19. **Use a separate user account for everyday work.**
    Do not operate as `root` on a regular basis, and do not run ordinary applications with administrative privileges.

20. **Monitor network activity.**
    Pay attention to unexpected network connections made by applications. An unknown application that establishes persistent connections to external servers should be investigated.

21. **Use secure DNS.**
    When appropriate, configure `DNSCrypt-GUI` or another trusted secure DNS mechanism. This can protect DNS queries against certain types of interception and manipulation, but **does not provide complete anonymity**.

22. **Limit telemetry and automatic synchronization.**
    Disable unnecessary diagnostic data collection and automatic synchronization with external services, especially when it involves personal or sensitive information.

23. **Be careful when connecting external devices.**
    Do not connect unknown USB storage devices or other untrusted hardware to your working system. Grant ADB access to Android devices only when necessary.

24. **Do not treat VPNs, encryption, or containers as absolute protection.**
    LUKS protects data on a powered-off disk; `encrypt-decrypt` protects individual files; secure network connections protect a particular part of the network path; MaxContainer restricts MAX's interaction with the host system. None of these mechanisms protects against every possible threat.

25. **Follow the principle of minimum necessary trust.**
    Before using any third-party service, ask yourself three questions: **What data am I providing? What permissions am I granting? Do I actually need to use this service?**

---

## Security principle

Security is not provided by a single application or technology. Proserpina combines several layers of protection, but the overall security of the system also depends on user behavior, software sources, system configuration, and the specific threat model.

Use only the protection mechanisms that are appropriate for your situation, understand their limitations, and avoid relying on any single security mechanism.


