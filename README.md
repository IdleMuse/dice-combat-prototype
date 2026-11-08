# Dice Combat Prototype

A barebones browser prototype of a bag-building dice combat system: a party of four (Fighter, Paladin, Wizard, Merchant) against four small enemies, then a second wave with one big monster.

Play it at the GitHub Pages address for this repository.

## How a turn works

1. Enemies roll first. Their cards show what they'll do, and red tags above your party show who each sword is aimed at.
2. You draw dice from the cup and roll them into the tray.
3. Click dice to select them, then click what to spend them on:
   - an enemy, to attack it (swords)
   - a targeted party card, to block (shields)
   - the dice on a party card, to buy one (speech)
   - a card's ability text, to use it (specials)
   - the cup, to draw one more die every turn (speech equal to your current draw)
   - Reroll faces reroll another die. Magic counts as any symbol.
4. End the turn. Unused dice are lost, and enemy swords land. Each unblocked hit rolls that character's health die.

## Editing

Everything is in `index.html`. The dice faces, enemy dice, monster dice and class abilities are defined at the top of the script (`BASE_FACES`, `ENEMY_FACES`, `BOSS_FACES`, `CLASSES`). Fight settings such as enemy health and party level are also adjustable in the page, under Settings.

The dice are drawn by a small canvas renderer in the same file. Icons come from [Lucide](https://lucide.dev) via unpkg.
