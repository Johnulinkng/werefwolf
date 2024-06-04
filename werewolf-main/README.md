In Johns Hopkins University we developed a project about:
# Werewolf on Chain

This project implements a blockchain-based Werewolf game using Aleo. We have created a 12-player configuration that includes the Seer, Witch, Hunter, Guard, 4 Villagers, and 4 Werewolves. The project includes detailed explanations of each game role's functionality based on the rules of Werewolf. The operations are performed off-chain and then the results are packaged and uploaded on-chain, enabling the scalability feature of blockchain rollup while maintaining a low footprint.

## Project Overview

Werewolf is a popular social deduction game where players are assigned roles secretly, and the goal of the game is to eliminate the opposing team. In this blockchain implementation, we utilize Aleo's capabilities to bring this traditional game into a decentralized environment.

## Game Configuration

The game configuration consists of 12 players with the following roles:
- **Seer**: Can check the identity of one player each night.
- **Witch**: Has two potions, one to save a player and one to poison a player.
- **Hunter**: If killed, can shoot another player.
- **Guard**: Can protect one player each night from being killed.
- **4 Villagers**: Regular players with no special abilities.
- **4 Werewolves**: Work together to eliminate other players.

## Role Explanations

- **Seer**: Each night, the Seer can select one player to check their identity. This information is crucial for identifying werewolves.
- **Witch**: The Witch has two potions - a healing potion and a poison potion. The healing potion can save a player who was attacked by werewolves, while the poison potion can kill a player.
- **Hunter**: If the Hunter is killed, they can immediately take a final shot to eliminate another player.
- **Guard**: The Guard can choose one player to protect each night. The protected player cannot be killed that night.
- **Villagers**: The Villagers aim to identify and eliminate the werewolves based on their deductions and discussions.
- **Werewolves**: The Werewolves aim to eliminate the villagers and other special roles by secretly voting to kill one player each night.

## Implementation Details

- **Off-Chain Operations**: The game logic and player interactions are handled off-chain to ensure efficiency and reduce blockchain congestion.
- **On-Chain Rollup**: The final results of each game phase are packaged and uploaded to the blockchain, leveraging the scalability of rollups to maintain a small on-chain footprint.
- **Aleo Integration**: This project utilizes Aleo's advanced cryptographic and privacy features to ensure a secure and fair gameplay experience.

## How to Play

1. **Setup**: Initialize the game with 12 players, assigning roles randomly.
2. **Night Phase**: Special roles (Seer, Witch, Guard) perform their actions secretly.
3. **Day Phase**: All players discuss and vote to eliminate a suspect.
4. **Repeat**: The game alternates between night and day phases until one team wins.

## How to Run

1. Install Aleo v1.9.4
2. We modified the `run_leo` package to adapt it to Aleo updated in August, 2023.
3. Run the game using:
   ```bash
   python3 game.py
