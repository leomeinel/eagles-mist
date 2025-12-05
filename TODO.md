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

### Window

- [ ] Width view area should stretch infinitely
- [ ] Height view area limited to height of single chunk

### UI

- [ ] Use [bevy_ui_text_input](https://crates.io/crates/bevy_ui_text_input)

### Chunks

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

### Movement

- [ ] Use [bevy_rapier2d](https://crates.io/crates/bevy_rapier2d)

### Graphics

- [ ] Use [Pixelorama](https://pixelorama.org/)
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
- [pixelblog](https://raymond-schlitter.squarespace.com/blog)
- [pixelblog Graphical Projections 1](https://www.slynyrd.com/blog/2018/3/14/pixelblog-3-graphical-projections-1)
- [pixelblog Graphical Projections 2](https://www.slynyrd.com/blog/2018/4/12/pixelblog-4-graphical-projection-part-2)
