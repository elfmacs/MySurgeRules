# MySurgeRules

Public Surge rule sets maintained for use by personal Surge profiles.

Changes should be made on a branch and merged through pull requests.

## T-Mobile

Two separate rule sets are maintained so ordinary website/application routing can be kept distinct from carrier-network / Wi-Fi Calling traffic.

### Web and application domains

```ini
RULE-SET,https://raw.githubusercontent.com/elfmacs/MySurgeRules/main/rules/T-Mobile.list,"📱 T-Mobile",extended-matching
```

### IMS / ePDG / Wi-Fi Calling network traffic

```ini
RULE-SET,https://raw.githubusercontent.com/elfmacs/MySurgeRules/main/rules/T-Mobile-Network.list,"📱 T-Mobile",extended-matching
```

The network rules include T-Mobile US ePDG discovery names and the destination ranges documented for Wi-Fi Calling. They intentionally do not enable the much broader `IP-ASN,21928` catch-all.

The selected `📱 T-Mobile` Surge policy must support UDP if Wi-Fi Calling is expected to work, particularly UDP 500 and UDP 4500.
