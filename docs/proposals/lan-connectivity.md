# Verify Jellyfin access from the home network

The PC’s DHCP address changed. The current server answered locally at the current Ethernet address, but phone and TV access still need independent verification.

- Reserve the server address in the router and confirm the configured URL on each client.
- Check whether the active Windows network profile matches the existing subnet-scoped firewall rule.
- Test the sign-in page on the phone and TV before troubleshooting the custom app or casting. If the page loads and app sign-in fails, inspect the webOS request and server response.

This proposal makes no network configuration changes.
