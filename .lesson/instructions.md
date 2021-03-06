# Instructions  

Build a Legacy Bitcoin Transaction Parser in Python. You should be able to input any transaction using P2PK, P2PKH, P2SH, or P2MS TXOs and parse it into a python dict of the relevant transaction fields.

For this exercise, we're not doing any validation. You don't need to parse the scriptSig or scriptPubKey fields, or lookup the amounts of the inputs. We're simply parsing out the relevant TX fields of the rawtransaction hex string.

Example:

Input (First Ever Bitcoin Transaction: Satoshi Paying Hal 10BTC): 
0100000001c997a5e56e104102fa209c6a852dd90660a20b2d9c352423edce25857fcd3704000000004847304402204e45e16932b8af514961a1d3a1a25fdf3f4f7732e9d624c6c61548ab5fb8cd410220181522ec8eca07de4860a4acdd12909d831cc56cbbac4622082221a8768d1d0901ffffffff0200ca9a3b00000000434104ae1a62fe09c5f51b13905f07f06b99a2f7159b2225f374cd378d71302fa28414e7aab37397f554a7df5f142c21c1b7303b8a0626f1baded5c72a704f7e6cd84cac00286bee0000000043410411db93e1dcdb8a016b49840f8c53bc1eb68a382e97b1482ecad7b148a6909a5cb2e0eaddfb84ccf9744464f82e160bfa9b8b64f9d4c03f999b8643f656b412a3ac00000000

Output (python dict, you can pretty print it like below by doing print(json.dumps(d, indent=4))):

{

    "version": 1,
    "inputs": [
        {
            "txid": "0437cd7f8525ceed2324359c2d0ba26006d92d856a9c20fa0241106ee5a597c9",
            "vout": 0,
            "scriptSig": "47304402204e45e16932b8af514961a1d3a1a25fdf3f4f7732e9d624c6c61548ab5fb8cd410220181522ec8eca07de4860a4acdd12909d831cc56cbbac4622082221a8768d1d0901",
            "sequence": 4294967295
        }
    ],
    "outputs": [
        {
            "amount": 1000000000,
            "scriptPubKey": "4104ae1a62fe09c5f51b13905f07f06b99a2f7159b2225f374cd378d71302fa28414e7aab37397f554a7df5f142c21c1b7303b8a0626f1baded5c72a704f7e6cd84cac"
        },
        {
            "amount": 4000000000,
            "scriptPubKey": "410411db93e1dcdb8a016b49840f8c53bc1eb68a382e97b1482ecad7b148a6909a5cb2e0eaddfb84ccf9744464f82e160bfa9b8b64f9d4c03f999b8643f656b412a3ac"
        }
    ],
    "locktime": 0
    
}

  
  