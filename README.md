# UltimateCoins

## Permissions
- ultimatecoins.admin - reload command
- ultimatecoins.percentage.\<number\> - percentage of coins dropped on death
- ultimatecoins.mob.multiplier.\<number\> - mob drop multiplier

## config.yml
```yaml
config-version: 1

############################
#   Integration Settings   #
############################

currency-settings:
  # This is the currency that is used when a coin uses COINENGINE
  coinsengine-currency: "coins"

  # Ddisplay
  vault-uses-whole-numbers: false
  coinsengine-uses-whole-numbers: true

# Should MMOCore party integration be enabled?
# Requires MMOCore & MythicLib installed.
mmocore-integration:
  # Should parties change coin dropping logic
  party:
    enabled: true

    # The amount of coins dropped will be multiplied by
    # this number for each player that's in the party.
    multiplier: 1.2

    # INDIVIDUAL - Only the player gets the coins.
    # SHARED - Each player in the party gets the coins.
    # SPLIT - The coins are split evenly between the party.
    pickup: SPLIT



########################
#   General Settings   #
########################

# Should players drop coins on death?
playersLoseMoneyOnDeath:
  enabled: true
  percentage: 10

# Should players be able to pick up coins dropped by other players?
can-players-pickup-others: false

# Should the victim be able to pick up coins they dropped?
can-player-pickup-own: true



coins:
  # notifies player in chat when they pick up a coin
  notify-player-on-pickup: true

  # Should the drops merge together?
  coin-merging: false

  # Should the drops be dropped with a random offset?
  random-offset: false

  pickup-sound:
    enabled: true
    sound: ENTITY_EXPERIENCE_ORB_PICKUP
    #values from 0-2
    pitch: 1.2
    #values from 0-1
    volume: 0.5

  hologram-animation:
    enabled: true

    hologram-text: "+%currency_symbol%%amount%"

    # In ticks
    duration: 16
    y-offset: 1.5
    distance-from-player: 1

    hologram-rise:
      enabled: true
      amount: 1

messages:
  no-permission: "<red>No Permission."
  usage: "<red>Usage: /<alias> <reload>"
  reloaded: "<green>Reloaded (<time>ms)"
  player-death-message: "<red>You dropped $<amount>."
  coin-pickup-message: "You picked up %currency_symbol%%amount%."
```
