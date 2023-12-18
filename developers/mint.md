# Mint

### Requirement

Valid UTF-8 encoded JSON string.

### Example

```
{ 
  "p": "isc-20",
  "op": "mint",
  "tick": "injs",
  "amt": "1000",
  "nonce": "1231006505",
}
```

### Fields

<table><thead><tr><th width="135">Key</th><th width="168">Required</th><th>Description</th></tr></thead><tbody><tr><td>p</td><td>yes</td><td>Protocol name: Helps other systems identify</td></tr><tr><td>op</td><td>yes</td><td>Operation: Type of event (Deploy, Mint, Transfer, List, Unlist, Deal)</td></tr><tr><td>tick</td><td>yes</td><td>Ticker: The identifier of irc-20, unique, not case sensitive.</td></tr><tr><td>amt</td><td>yes</td><td>Amount to mint: States the amount of the irc-20 to mint. Has to be less or equal to "lim"</td></tr><tr><td>nonce</td><td>yes</td><td>unique value, timestamp is recommended.</td></tr></tbody></table>

