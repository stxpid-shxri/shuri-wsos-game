# shuri-wsos-game

This is a simple guessing number game from 1-5 between player and the owner. I applied everything ive learned from WSOS - Ackeeblock chain.

# Back-end  anchor/rust

I've use beta.solpg.io for my program development. Tested it and deployed on devnet. After that ive exported it on my local anchor development.

![image](https://user-images.githubusercontent.com/110050848/230229193-d7cad8d3-900c-4089-8230-fe3f4eee8312.png)

Programs, Accounts and process.
1. Initialize fn - this will create a PDA that will hold the prize pool for the guessing game (only owner can use this)
2. Deposit fn - this will be use for refilling the prize pool.
3. Create fn - this will create a PDA that will be use for the bet/play fn, this holds the following, the user  who will guess, the random number to be guess.
4. Play fn - this will run the program to check if who won between the owner and player. this will accept the selected number of player and the bet amount.
              - if user guess right, the bet amount will be automatically sent to his wallet and deducted from the pool.
               -if user guess wrong, the bet amount will be deducted from his wallet and be sent to the pool.
5. Reset fn (not yet done) - this will reset the PDA that was created from Create Fn.

# Front-end next.js

So currently this is how it looks, ive encountered an issue on useeffect/setState that is not updating my data.(still working/testing on this).

![image](https://user-images.githubusercontent.com/110050848/230230281-cb770553-1997-4e7d-830b-fc414145323d.png)

Still not finish, but will try my best to accomplish it.
