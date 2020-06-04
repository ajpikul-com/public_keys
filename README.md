# Public Keys

This is a list of staff public keys- for the computers you use to access devices.

If you want to give someone access to a server or otherwise, create a user for them (their folder name) and copy all of their public key's into `/home/[USERNAME]/.ssh/authorized_keys`.

Example:
```sh
git clone https://github.com/osoximeter/public_keys
cd public_keys/ajp
cat * >> /home/ajp/.ssh/authorized_keys
```
## DO NOT PUSH YOUR PRIVATE KEYS
## Basic assymetric encryption explanation:

One key is private, one is public. Encrypted with either one, decrypted with the opposite. This allows you to

a) verify the speaker
- They encrypt with private key, no way anyone else could have encrypted it if it can be decrypted by their public key!

b) communicate privately TO the speaker (not from!).
- You encrypt with their public keys, only they can decrypt with their private key.
