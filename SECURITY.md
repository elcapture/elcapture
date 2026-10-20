# Security

elcapture installs a root certificate and sees decrypted traffic, so we take security reports seriously.

Please report vulnerabilities privately to **hello@elcapture.com** with "Security" in the subject, not in a public issue. Include the elcapture version, your macOS version and the steps to reproduce.

We'll reply within a few days and tell you when a fix is out.

## How the certificate works

elcapture creates its own root certificate on your Mac the first time it runs. The private key never leaves `~/Library/Application Support/elcapture`. Each Mac gets a different certificate, so one install can't be used to read traffic on another machine.

To remove it: turn off **System proxy** in elcapture, open **Keychain Access**, search for **elcapture Root CA** and delete it.
