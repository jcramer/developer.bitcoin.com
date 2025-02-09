---
title: Util
icon: cogs
ordinal: 22
---

### `validateAddress`

Return information about the given bitcoin address.

#### Arguments

- address `string | string[]`

#### Result

- addressDetails `Promise<AddressDetails | AddressDetails[]>`

#### Examples

    (async () => {
      try {
        let validateAddress = await bitbox.Util.validateAddress("bitcoincash:qzc86hrdufhcwlyzk7k82x77kfs2myekn57nv9cw5f");
        console.log(validateAddress);
      } catch(error) {
       console.error(error)
      }
    })()

    // { isvalid: true,
    // address: '17fshh33qUze2yifiJ2sXgijSMzJ2KNEwu',
    // scriptPubKey: '76a914492ae280d70af33acf0ae7cd329b961e65e9cbd888ac',
    // ismine: true,
    // iswatchonly: false,
    // isscript: false,
    // pubkey: '0312eeb9ae5f14c3cf43cece11134af860c2ef7d775060e3a578ceec888acada31',
    // iscompressed: true,
    // account: 'Test' }

    (async () => {
      try {
        let validateAddress = await bitbox.Util.validateAddress(["bitcoincash:qzc86hrdufhcwlyzk7k82x77kfs2myekn57nv9cw5f"]);
        console.log(validateAddress);
      } catch(error) {
       console.error(error)
      }
    })()

    // [{ isvalid: true,
    // address: '17fshh33qUze2yifiJ2sXgijSMzJ2KNEwu',
    // scriptPubKey: '76a914492ae280d70af33acf0ae7cd329b961e65e9cbd888ac',
    // ismine: true,
    // iswatchonly: false,
    // isscript: false,
    // pubkey: '0312eeb9ae5f14c3cf43cece11134af860c2ef7d775060e3a578ceec888acada31',
    // iscompressed: true,
    // account: 'Test' }]

## Interfaces

### AddressDetails

    {
      isvalid: boolean
      address: string
      scriptPubKey: string
      ismine: boolean
      iswatchonly: boolean
      isscript: boolean
      pubkey: string
      iscompressed: boolean
      account: string
    }
