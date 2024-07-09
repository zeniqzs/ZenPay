# ZenPay Plugin 💸

Welcome to the ZenPay Plugin, facilitating easy monetary transactions and balance management for your Minecraft server!

## Features 🌟

- **Pay Command:** Transfer funds between players with a simple command.
  
- **BalTop GUI:** View top balances on the server with a convenient graphical interface.
  
- **Customizable Messages and Sounds:** Tailor messages and sounds for various pay-related events.
  
- **Offline Player Payment Control:** Option to enable or disable payments to offline players.
  
- **Cooldown System:** Prevent spamming of pay commands with a configurable cooldown period.

## Configuration Example 📝

### Messages and Sounds Configuration

```yaml
Messages:
  Balance: "&7Balance: &a{balance}"
  OtherBalance: "&7Balance from #0078FF{player} &7is &a{balance}&7."
  OnlyPlayers: "&cOnly players can use this command."
  NotFound: "#FF0000Player not found."
  Bal-Usage: "#FF0000Incorrect usage! Use /balance or /balance <player>."
  Pay-Usage: "#FF0000Usage: /pay <player> <amount>"
  InvalidAmount: "#FF0000Please enter a valid amount."
  Not-Enough-Money: "#FF0000You do not have enough money to complete this transaction."
  CannotPaySelf: "#FF0000You cannot pay yourself."
  CannotPayOfflinePlayers: "#FF0000You cannot pay offline players."
  Received: "&7You have received &a{amount} &7from #0078FF{sender}&7."
  Paid: "&7You have paid &a{amount} &7to #0078FF{recipient}."
  PayNotificationsEnabled: "&aPay notifications have been enabled."
  PayNotificationsDisabled: "&cPay notifications have been disabled."


Sounds:
  Balance: "ENTITY_PLAYER_LEVELUP"
  OtherBalance: "ENTITY_PLAYER_LEVELUP"
  OnlyPlayers: "ENTITY_VILLAGER_NO"
  NotFound: "ENTITY_VILLAGER_NO"
  Bal-Usage: "ENTITY_VILLAGER_NO"
  Pay-Usage: "ENTITY_VILLAGER_NO"
  InvalidAmount: "ENTITY_VILLAGER_NO"
  Not-Enough-Money: "ENTITY_VILLAGER_NO"
  CannotPaySelf: "ENTITY_VILLAGER_NO"
  CannotPayOfflinePlayers: "ENTITY_VILLAGER_NO"
  Received: "ENTITY_PLAYER_LEVELUP"
  Paid: "ENTITY_PLAYER_LEVELUP"
  PayNotificationsEnabled: "ENTITY_PLAYER_LEVELUP"
  PayNotificationsDisabled: "ENTITY_VILLAGER_NO"

Pay:
  PayOfflinePlayers: false #Buggy if its on true
  Cooldown: 60  # Cooldown in seconds

BalTop:
  Title: "&6Top Balances - Page {0}"
  Arrows:
    Left:
      Material: "ARROW"
      Title: "&aPrevious Page"
      Lore:
        - "&7Click to go to the previous page"
    Right:
      Material: "ARROW"
      Title: "&aNext Page"
      Lore:
        - "&7Click to go to the next page"
  BarrierBlock:
    Material: "BARRIER"
    Title: "&cClose"
    Lore:
      - "&7Click to close the menu"
  CloseGlass:
    Enabled: true
    Title: "&cClose Menu"
    Lore:
      - "&7Click to close the menu"
  Heads:
    Lores:
      Title: "&b%player%'s Balance"
      Money: "&aBalance: &e{0}"
      Rank: "&aRank: &e{0}"
    Command: "balance {player}"
```

# Checking Balance:
- Use /balance to check your own balance or /balance <player> to check another player's balance.
# Paying Another Player:
- Use /pay <player> <amount> to transfer funds to another online player.
# Viewing Top Balances:
- Access the BalTop GUI to view the players with the highest balances on the server.
