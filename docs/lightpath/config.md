# Config

``` yaml title="config.yml" linenums="1"
# The material that spawns under the player.
material: GLOWSTONE # (1)

# Particles when the light block appears. Set 'none' to deactivate particles.
appear-particle: SMOKE_NORMAL # (2)

# Particles when the light block disappears. Set 'none' to deactivate particles.
disappear-particle: SMOKE_NORMAL # (3)

# Lifetime of the light block in ticks (20 ticks = 1 second).
block-lifetime: 60 # (4)
```

1. See Minecraft [Minecraft Block IDs](https://minecraft-ids.grahamedgecombe.com) for all Block IDs
2. See [Valid Particles](/plugin/lightpath/particles/)
3. See [Valid Particles](/plugin/lightpath/particles/)
4. !!! info "Ticks"
      20 Ticks = 1 second  
      60 Ticks = 3 seconds  
      600 Ticks = 30 seconds

# Light Material

The material that spawns under the player.

``` yaml
material: stone
```

!!! tip "Minecraft Block IDs"

    See Minecraft [Minecraft Block IDs](https://minecraft-ids.grahamedgecombe.com) for all Block ID

# Particle

## Appear Particle

Particles when the light block appears. Set 'none' to deactivate particles.

``` yaml
appear-particle: SMOKE_NORMAL
```

## Dissappear Particle 
Particles when the light block disappears. Set 'none' to deactivate particles.

``` yaml
disappear-particle: SMOKE_NORMAL
```

!!! info "Valid Particles"

    See [Valid Particles](/docs/lightpath/particles/)

# Block Lifetime

Lifetime of the light block in ticks (20 ticks = 1 second).

``` yaml
block-lifetime: 600
```

!!! info "Ticks"

    20 Ticks = 1 Second
