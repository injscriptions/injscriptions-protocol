# Transfer

The destination address is the black hole address of the inscription, there is no limit to INJ amount, just meet the minimum network requirements. When the inscription is listed, it will not be able to be transferred. Due to the current memo length limit, it is limited to being transferred to two different addresses at most.

### Requirement

Valid UTF-8 encoded JSON string.

### Example

```
{
  "p": "isc-20",
  "op": "transfer",
  "tick": "injs",
  "nonce": "1231006505",
  "to": [ //batch transfer, the sum of amt must equal the previous amt param
    {
      "recv": "inj1tqfz777uyv5wpf60nnqtxyr5q0fgwtazyk67e6", //receiver address
      "amt": "50" //amount
    },
    {
      "recv": "inj1y9vkk3ga59gq96amj9np7l67nuhnwg6rv4a06j",
      "amt": "50"
    }
  ]
}
```

### Fields

<table><thead><tr><th width="152">Key</th><th width="191">Required</th><th>Description</th></tr></thead><tbody><tr><td>p</td><td>yes</td><td>Protocol name: Helps other systems identify</td></tr><tr><td>op</td><td>yes</td><td>Operation: Type of event (Deploy, Mint, Transfer, List, Unlist, Deal)</td></tr><tr><td>tick</td><td>yes</td><td>Ticker: The identifier of irc-20, unique, not case sensitive.</td></tr><tr><td>nonce</td><td>yes</td><td>unique value, timestamp is recommended.</td></tr><tr><td>to</td><td>yes</td><td>array object, "recv" and "amt", "recv" and "amt" fields, recv is the recipient address, amt is the quantity, the recipient address must start with 0x, and the length is appropriate, otherwise the entire transaction is invalid.</td></tr></tbody></table>
