# macOS Permissions

macOS requires both **Input Monitoring** and **Local Network** access for the Driver Station to function correctly.

If you declined one of these prompts, first try re-enabling access in **System Settings -> Privacy & Security**.

If the Driver Station still cannot access the local network, you can add macOS local network exceptions from Terminal for both Ethernet and Wi-Fi. The following commands allow access to any `10.x.x.x` address and any `172.16.x.x` through `172.31.x.x` address:

```zsh
sudo defaults write com.apple.network.local-network AllowedEthernetLocalNetworkAddresses -array "10.0.0.0/8"
sudo defaults write com.apple.network.local-network AllowedEthernetLocalNetworkAddresses -array-add "172.16.0.0/12"
sudo defaults write com.apple.network.local-network AllowedWiFiLocalNetworkAddresses -array "10.0.0.0/8"
sudo defaults write com.apple.network.local-network AllowedWiFiLocalNetworkAddresses -array-add "172.16.0.0/12"
```

After running these commands, reboot macOS before starting the Driver Station again.

> [!WARNING]
> These settings allow any app on the Mac to access local networks in those ranges without prompting. If you only need access to one robot network, a narrower CIDR range is more restrictive.

For more information, see Apple's documentation on [understanding local network privacy](https://developer.apple.com/documentation/technotes/tn3179-understanding-local-network-privacy#macOS-considerations).
