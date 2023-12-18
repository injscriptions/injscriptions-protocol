# Deploy

The destination address is the black hole address, 1 INJ transferred to the black hole address.

### Requirement

Valid UTF-8 encoded JSON string.

### Example

```
{ 
  "p": "isc-20",
  "op": "deploy",
  "tick": "injs",
  "max": "210000000",
  "lim": "1000",
  "tax": "0.1",   //1 inj
  "nonce": "1231006505",
}
```

### Fields

<table><thead><tr><th width="158">Key</th><th width="146">Required</th><th>Description</th></tr></thead><tbody><tr><td>p</td><td>yes</td><td>Protocol name: Helps other systems identify</td></tr><tr><td>op</td><td>yes</td><td>Operation: Type of event (Deploy, Mint, Transfer, List, Unlist, Deal)</td></tr><tr><td>tick</td><td>yes</td><td>Ticker: The identifier of irc-20, unique. If there are duplicates, the first one shall prevail, not case sensitive.</td></tr><tr><td>max</td><td>yes</td><td>Max supply: set max supply of the asc-20</td></tr><tr><td>lim</td><td>yes</td><td>Mint limit: limit per inscription</td></tr><tr><td>tax</td><td>yes</td><td>Tax Value: INJ needs to be sent when casting inscriptions. Only when the amount sent matches the amount of the deployed inscription, it can be parsed as a normal transaction. (The amount that needs to be sent when casting each inscription is defined here)</td></tr><tr><td>nonce</td><td>yes</td><td>unique value, timestamp is recommended.</td></tr></tbody></table>

