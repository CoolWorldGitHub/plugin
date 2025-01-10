# Config

``` yaml title="config.yml" linenums="1"
# The material that spawns under the player.
material: GLOWSTONE (1)

# Particles when the light block appears. Set 'none' to deactivate particles.
appear-particle: SMOKE_NORMAL

# Particles when the light block disappears. Set 'none' to deactivate particles.
disappear-particle: SMOKE_NORMAL

# Lifetime of the light block in ticks (20 ticks = 1 second).
block-lifetime: 60
```

1. See [https://minecraft-ids.grahamedgecombe.com/](Valid Block IDs) for more info.

# asd

``` yaml
# (1)!
```

1.  Look ma, less line noise!

# Light Material

The material that spawns under the player.

```yml
material: stone
```

!!! tip "Minecraft Block IDs"

    See Minecraft [Minecraft Block IDs](https://minecraft-ids.grahamedgecombe.com) for all Block ID

# Particle

## Appear Particle

Particles when the light block appears. Set 'none' to deactivate particles.

```yml
appear-particle: SMOKE_NORMAL
```

## Dissappear Particle 
Particles when the light block disappears. Set 'none' to deactivate particles.

```yml
disappear-particle: SMOKE_NORMAL
```

!!! info "Valid Particles"

    See [Valid Particles](https://coolworldgithub.github.io/plugin/lightpath/particles/)

# Block Lifetime

Lifetime of the light block in ticks (20 ticks = 1 second).

```yml
block-lifetime: 600
```

!!! info "Ticks"

    20 Ticks = 1 Second
