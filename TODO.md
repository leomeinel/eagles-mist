# To Do

## Game mechanics

- [ ] 2d top-down RPG
- [ ] Theme is exploring the unknown
- [ ] Somewhat realistic
- [ ] Should only use things that humans invented before the middle ages
- [ ] Build up a character over a long time
- [ ] Uses mist, fire and darkness to create specific atmosphere and change game mechanics
  - [ ] Some enemies use fire, which is ineffective with mist
  - [ ] Player can use fire to defend base but this also increases visibility and lures more enemies over time, maybe forcing player to abandon base
- [ ] No magic or potions
- [ ] Random world
- [ ] Random enemies

### Story

#### Opening scene

- [ ] Burned down house
- [ ] Still has low quality bow, polearm and sword
- [ ] Family is gone but unknown where they have gone
- [ ] Arrived after hunting and harvesting
- [ ] House and items never despawn
- [ ] Some parts of the house have survived because of mist

### Enemies

- [ ] Enemy raids on established bases
- [ ] Random enemies scattered across the map
- [ ] Rarely drop heads
- [ ] Area scaling depending on biome and distance from start point

### Crops/Animals

- [ ] Crops are a good food source but farming is quite hard to maintain
- [ ] Berries scattered across the map
- [ ] Fishing and animals provide food and ingredients for traps
  - [ ] Oil obtained from fish or animals needed for fire traps
- [ ] Different animals in each biome

### Player

- [ ] Name
- [ ] Customize colors and addons
- [ ] Fight enemies to gain experience in skills and choose perks or gain achievements
- [ ] Separate parts as layers
  - [ ] Headwear
  - [ ] Eyes
  - [ ] Head
  - [ ] Body
  - [ ] Feet

### NPCs

#### Trading

- [ ] Repair weapons at smith
- [ ] Higher tier weapons can only be exchanged for enemy heads at a towns prison
- [ ] More weapons available and cheaper than with gold

#### Bosses

- [ ] Mainly spawn in dungeons
- [ ] On defeating player can gain perk
- [ ] More like bandit leaders in Skyrim but with interesting mechanics, nothing magical
- [ ] Well defended by their soldiers and traps
- [ ] Always drop a boss head

### Base

- [ ] Player can choose to establish or abandon a base
- [ ] Raids will appear even if not there
- [ ] Only place where farming and ranching is possible

#### Defense

- [ ] Traps that player can use to defend their base
- [ ] NPCs that player can hire to defend their base or stay there for easy access

#### Farming/Ranching

- [ ] Farming and ranching provides food
- [ ] Modifiers for biome determine which animal/crop is good to plant there

### Weapons

- [ ] Will lose sharpness over time. This reduces modifiers until below a lower tier.
  - [ ] Will never be destroyed
- [ ] Certain weapons needed for certain traps, thus allowing player to recycle weapons
- [ ] Random stones and other objects can be thrown as a backup weapon

#### Categories

- [ ] Bows
  - [ ] Only ranged option
- [ ] Polearms
  - [ ] Long reach
- [ ] Swords
  - [ ] Short reach, good against unarmored
- [ ] Maces
  - [ ] Short reach, good against armored

#### Tiers

- [ ] Low
- [ ] Medium
- [ ] High
- [ ] Legendary
  - [ ] Does not lose any sharpness but always has some drawback (fex. weight) compared to other weapons but also some benefit associated with it (fex. armor)

### Dungeons

- [ ] Loot gold from chests and killed bosses


## Technical

- [ ] [bevy_rand](https://crates.io/crates/bevy_rand) and [bevy_prng](https://crates.io/crates/bevy_prng) for determinism and portability of random numbers with feature wyrand
- [ ] [rand](https://crates.io/crates/rand) for pseudo random numbers
- [ ] [bevy_yarnspinner](https://crates.io/crates/bevy_yarnspinner) for dialogue
- [ ] [bevy_asset_loader](https://crates.io/crates/bevy_asset_loader) for asset loading
- [ ] [bevy_light_2d](https://crates.io/crates/bevy_light_2d) for lighting. It is also possible to move a point light with the camera for a sun light, but I'm not sure if that is desired.
- [ ] [bevy_enoki](https://crates.io/crates/bevy_enoki) for particles.
- [ ] [bevy_ecs_tilemap](https://crates.io/crates/bevy_ecs_tilemap) for tilemap.

### Window

- [ ] Width view area should stretch infinitely
- [ ] Height view area limited to height of single chunk

### UI

- [ ] Use [bevy_ui_text_input](https://crates.io/crates/bevy_ui_text_input)
- [ ] Use [bevy_fluent](https://crates.io/crates/bevy_fluent) for translation

### World

- [ ] Use [noisy_bevy](https://crates.io/crates/noisy_bevy) for terrain generation
  - [ ] Use `fbm_simplex_2d_seeded` for continuous, smooth elevation
  - [ ] Use `worley_2d` to define biome regions, cluster resources, or add structural variation (rocks, plants, forests, lakes, mountains)
  - [ ] Modify `fbm_simplex_2d_seeded` output with `worley_2d` output
- [ ] Sorrounding chunks is a dark gray outside plane
- [ ] Save chunks with [bevy_save](https://crates.io/crates/bevy_save/0.9.1) and load on demand
- [ ] One chunk is one canvas size

#### Outside

- [ ] Load current chunk + (2 sorrounding chunks on X-Axis || 1 sorrounding chunk on Y-Axis)
- [ ] Ensure that transition is always possible on at least 2 sides

#### Indoors

- [ ] Only single chunk
- [ ] Ensure that transition is always possible on at least 2 sides
- [ ] Outside plane visible

#### Dungeon

- [ ] Load current chunk + (2 sorrounding chunks on X-Axis || 1 sorrounding chunk on Y-Axis) except if reaching ending chunk
- [ ] Ensure that transition is always possible on at least 2 sides except for ending chunk

### Movement/Physics

- [ ] Use [bevy_rapier2d](https://crates.io/crates/bevy_rapier2d) for physics
- [ ] Use [bevy_enhanced_input](https://crates.io/crates/bevy_enhanced_input) for movement

### Graphics

- [ ] Use [Pixelorama](https://pixelorama.org/)
- [ ] Use [bevy_spritesheet_animation](https://crates.io/crates/bevy_spritesheet_animation)
- [ ] Sprite sizes for pixel art
  - [ ] 8x8: TODO
  - [ ] 16x16: character, TODO
  - [ ] 24x24: TODO
  - [ ] 32x32: TODO
- [ ] Canvas size: 320x180
- [ ] Export as webp
- [ ] Use tilemap
- [ ] Add outline effect with black color in diamond pattern
- [ ] Use shading tool with color replace for shadows
- [ ] Light casts from top right corner
- [ ] 2:1 pixel ratio -> isometric

### Camera

- [ ] Top down
- [ ] Follows player with delay

### Layers

- [ ] UI layer
- [ ] Character layer
- [ ] Effect layer
- [ ] Map layer

### Resources

- [bevy_new_2d](https://github.com/TheBevyFlock/bevy_new_2d)
- [Bevy Upstreaming text input issue](https://github.com/bevyengine/bevy/issues/19752)
- [Testing apps](https://github.com/bevyengine/bevy/blob/main/tests/how_to_test_apps.rs)
- [Testing systems](https://github.com/bevyengine/bevy/blob/main/tests/how_to_test_systems.rs)
- [Rapier](https://rapier.rs/docs/user_guides/bevy_plugin/getting_started_bevy/)
- [Unofficial guide for bevy](https://taintedcoders.com/)
- [Bevy sprites](https://taintedcoders.com/bevy/sprites)
- [bevy_save pipeline](https://github.com/hankjordan/bevy_save/blob/main/examples/pipeline.rs)
- [kenney.nl](https://kenney.nl/)
- [pixelblog](https://raymond-schlitter.squarespace.com/blog)
- [pixelblog Graphical Projections 1](https://www.slynyrd.com/blog/2018/3/14/pixelblog-3-graphical-projections-1)
- [pixelblog Graphical Projections 2](https://www.slynyrd.com/blog/2018/4/12/pixelblog-4-graphical-projection-part-2)
- [pixelblog Top down tiles](https://www.slynyrd.com/blog/2019/8/27/pixelblog-20-top-down-tiles)
- [Pixel art animation](https://www.sandromaglione.com/articles/pixel-art-character-animations-guide)
- [Youtube - How to Implement Worley Biomes in Voxel Games with RUST](https://www.youtube.com/watch?v=m0BCrB_iRiA)
- [noisy_bevy - Basic](https://github.com/johanhelsing/noisy_bevy/blob/main/examples/basic.rs)
- [noisy_bevy - Seeded](https://github.com/johanhelsing/noisy_bevy/blob/main/examples/asteroids.rs)
- [noisy_bevy - Worley](https://github.com/johanhelsing/noisy_bevy/blob/main/examples/worley.rs)
- [freepd.com](https://freepd.com/)
- [sonniss.com](https://sonniss.com/gameaudiogdc/)
- [freesound.org](https://freesound.org/)
- [opengameart.org](https://opengameart.org)
- [punchy](https://github.com/fishfolk/punchy)
