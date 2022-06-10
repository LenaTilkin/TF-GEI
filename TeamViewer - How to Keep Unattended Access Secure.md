## TeamViewer: How to Keep Unattended Access Secure

### The key to secure unattended access is ensuring only authorized people can connect to those devices. How? With these five best practices.

You can describe TeamViewer connections in two ways: attended and unattended. Attended means someone is physically near the device to which you are trying to connect and can accept the connection request. Customers in IT support use attended access a lot because when there’s a problem with an individual device, the affected user is there waiting for a resolution.

But many times, you will want to remotely access devices without having to rely on someone being there to accept your connection request. Sometimes you will access devices that no one uses but you, such as your desktop computer at home or servers at work. Or perhaps you oversee servicing kiosks or terminals all over the world. It saves a lot of time (not to mention travel) being able to access devices from anywhere, whether or not someone else is there.

The key to secure unattended access is ensuring only authorized people can connect to those devices. How? With these five best practices. Let’s dive in…
1. **Disable Random Passwords**

The random password feature is ideal for attended machines that may require remote support from time to time. For example, if you’re having an issue, all the IT support agent needs to remotely access your computer is the random password. But on an unattended device, the random password functionality is just another way someone can gain access to the device.

To disable random passwords, go to Options > Security > Random password (for spontaneous access) and select Disabled (no random password).
Remotely Control Servers
2. **Disable Personal Passwords**

If the host device, the one you’re trying to connect to, is assigned to a particular TeamViewer account or group, eliminate the personal password(s). After all, anyone who knows that password — or can guess it — can access the device.

Disabling this functionality in favor of Easy Access (more on that below) makes sense if you assign the device to an account or group because Easy Access requires a TeamViewer account. You can secure TeamViewer accounts by two-factor authentication and other measures. Taking away the ability for outsiders to guess your personal password adds another layer of security for unattended access.

Check that setting under Options > Advanced > Personal password.
3. **Enable Easy Access**

The newest secure way to access a device with TeamViewer is through Easy Access. When Easy Access is enabled on a device and that device is assigned to your TeamViewer account, no random or personal password is required. You simply need to be logged in to your account. The only way someone else could access that device is with the device ID and password, so if you’ve eliminated passwords, you have limited access to only your device (and your group, if you have assigned the device to a group).

This approach is more secure than those involving passwords due to one powerful feature: two-factor authentication. Securing your TeamViewer account with two-factor authentication significantly reduces the chances of someone other than you is accessing your device(s). For more on how to enable two-factor authentication at the account level, check out our TeamViewer Community article.
Setting up Easy Access is… well, easy.

If someone already assigned the device to your TeamViewer account: Click Extras –> Options –> Security –> under Unattended access, activate the checkbox Grant easy access –> click OK.

If the device is not yet assigned to your TeamViewer account: Click Extras –> Options –> Security –> click the Configure button –> The Assign to account dialog box will open –> Click the Assign button –> Under Personal Password (for unattended access), activate the Grant easy access checkbox –> click OK.
4. **Block and Allowlist**

For a more granular approach to managing who and what can connect to devices with TeamViewer, use your Allowlist and Blocklist.

Blocklist: TeamViewer accounts or device IDs that appear on your device’s Blocklist are blocked from making a TeamViewer connection to that device. If your organization has experienced malicious connection attempts in the past, add those specific IDs or devices to your Blocklist. Also, if you have public-facing devices that live beyond your firewall, such as a web server, block their access to your device.

Allowlist: Only TeamViewer accounts and device IDs that are added to the Allowlist can make connections to your device. Stick to accounts for your Allowlist whenever possible; after all, someone you wouldn’t approve could be using an approved device. This is ideal if you know that only certain people should have remote access to your device. Of course, you can add groups or even your entire company to the Allowlist, if that’s appropriate.

You can configure your lists under Extras –> Options –> Security –> Block and Allowlist –> Click on Configure.
5. **Consider Two-Factor Authentication for Connections**

We’ve recently added two-factor authentication (TFA) at the connection level in addition to the TFA at the account level. This is great for when you need visibility and approval power for every connection attempt made to a particular device.

When someone attempts a connection to the secured device, you can receive a push notification on your phone that includes the device ID that is attempting the connection, as well as a prompt to approve or deny the request. If you have made unattended access available for a device to which only a few connections may be made or should only be accessed by you, like your desktop computer at work, TFA can provide an extra level of security.

Learn more about how to activate TFA for connections in this article on our Community.