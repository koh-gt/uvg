# uvg
Universal Vanity Generator to generate vanity address for all Bitcoin/Litecoin forks.

![uvg-matrioshka-banner](https://github.com/koh-gt/uvg/assets/101822992/c8142aca-898c-42aa-b696-2b333f2cc0ea)

# Usage
## List all supported crypto currencies - [See supported coins](https://github.com/koh-gt/uvg/wiki/Supported-coins) - [Add your coin](https://github.com/koh-gt/uvg/wiki/Add-coin):
```
C:\VanitygenPlusPlusSuite\Binaries\x86\Static-Release>vanitygen.exe -C LIST
ETH : Ethereum : 0x
BTC : Bitcoin : 1
LTC : Litecoin : L
FEC : Ferritecoin : F
...... (skip many output)
```

### Generate FEC vanity address (legacy) - [More examples (other coins)](https://github.com/koh-gt/uvg/wiki/Supported-coins):
```
C:\Static-Release>oclvanitygen Fabric
Generating FEC (Ferritecoin) Address
Difficulty: 264104224
[24.39 Mkey/s][total 88080384][Prob 28.4%][50% in 3.9s]
FEC Pattern: Fabric
FEC Address: Fabric58EkXhGLiKSxXNX2J87qsY4i8dQH
FEC Privkey: 6V1rgz9WzaaSLRy84m8AJMsySq2HPwdacBbbqT29Ap1uDEaicYc
```

### Generate ETH vanity address:
>Case insensitive does not work. Use `-i`.
```
C:\Static-Release>oclvanitygen -C ETH -i 0xFACADE
Generating ETH Address
Difficulty: 60492497
[24.85 Mkey/s][total 163577856][Prob 93.3%][95% in 0.7s]
ETH Pattern: 0xFACADE
ETH Address: 0xFACADE12C5a8Aa9Bb19303880f01941b258fE62E
ETH Privkey: 0xe0553449ae2dadeb470f6d1d869ba609196d96f6fad3e2eb44e8b71c51cac87c
```

### Generate ETH vanity contract address (CA):
```
C:\Static-Release>oclvanitygen -C ETH -F contract -i 0xBadBabe
Generating ETH Address
Difficulty: 268435456
[22.47 Mkey/s][total 134217728][Prob 39.3%][50% in 2.3s]
ETH Pattern: 0xBadBabe
ETH Address: 0xbadBabeFaA3bcA1180bbf1C1f85bD4E115891743
ETH Privkey: 0xa610bb9e10aca2509b8d21f967e5673808cdc6323b926baea026dbd4a793f699
```

If you don't have an OpenCL-compatible GPU, please use `vanitygen`. It runs on the CPU but may be up to 1,000x slower.

### [Advanced Features](https://github.com/koh-gt/uvg/wiki/Advanced-Features)

# Original code
https://github.com/samr7/vanitygen  
https://github.com/10gic/vanitygen-plusplus  
https://github.com/kjx98/vanitygen-eth  

## Credits 
1. https://github.com/samr7/vanitygen  
2. https://github.com/exploitagency/vanitygen-plus  
3. https://github.com/10gic/vanitygen-plusplus  
4. https://github.com/AngelTs/vanitygen-plusplus-ported-for-VS2019  
5. https://github.com/kjx98/vanitygen-eth
6. https://www.reddit.com/r/Namecoin/comments/zmp7pu/a_proofofwork_solution_against_impersonation/  
7. https://www.reddit.com/r/Namecoin/comments/vnkmzx/vanity_addresses_and_brute_forcing_private_keys/  

## Images
Cover Image - https://kardashev.fandom.com/wiki/Matrioshka_brain
 
## Known Issues
1. oclvanitygen++ (GPU version) can't find vanity ETH address starting with 0x0.  
2. oclvanitygen++ (GPU version) can't find case sensitive vanity ETH addresses.  
3. ETH vanity address difficulty estimation is **always** for case-insensative searching.  
4. oclcanitygen only works on legacy addresses.  


