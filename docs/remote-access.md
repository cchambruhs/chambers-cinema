# Private remote access

The TV client accepts HTTP or HTTPS server addresses. On your home network, keep using the PC’s local address. For travel, use a private Tailscale network with HTTPS. Start with the PC and your phone; an off-site TV needs a way to reach that private network.

1. Install Tailscale on the Windows Jellyfin PC and the phone. Sign in to the same tailnet on both.
2. On the PC, confirm `http://127.0.0.1:8096/web/` opens. Enable MagicDNS and HTTPS certificates in the Tailscale admin console if prompted.
3. From an administrator terminal on the PC, run `tailscale serve --bg http://127.0.0.1:8096` and copy the HTTPS address shown. Use Serve, which is private to your tailnet.
4. On the phone, turn off Wi-Fi, connect Tailscale, open the HTTPS address, and sign in to Jellyfin using your regular account. Play an episode and verify captions and seeking. Test home playback separately using the LAN address.
5. If access is granted to other tailnet members, review the tailnet access policy so only intended users can connect. To stop serving, run `tailscale serve reset` after checking that Serve has no other routes in use.

No router port forwarding is needed. The Windows PC must be awake and Jellyfin must be running. Complete the cellular test before considering remote access ready.

[Tailscale Serve documentation](https://tailscale.com/kb/1242/tailscale-serve)
