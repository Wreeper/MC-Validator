# MC-Validator by Wreeper
Client-side validator for Minecraft skins and capes signatures.

Available to use right now at https://mc-validator.wreeper.com/

## How does it work?
You want to know how it actually validates the signature.

First, Mojang releases a set of public keys at https://api.minecraftservices.com/publickeys . These keys are RSA public keys encoded in PEM.

Second, Mojang releases signed skin data at sessionserver.mojang.com (below is an example of signed data of my account):

https://sessionserver.mojang.com/session/minecraft/profile/86430f67bdef42789ab8b3df15a02b0d?unsigned=false

Once we have these, we can use libraries such as OpenSSL to match the signature to the public keys. On my testing, it seems like values are signed through profilePropertyKeys from the public keys. The script uses ALL public keys provided by Mojang to check for the signature.

## How can I trust it?
Well, the website's code can be audited on GitHub: https://github.com/Wreeper/MC-Validator/

Actually, wait, you're on GitHub now. nvm

You can download the project.html file and run it locally.



Good luck!
