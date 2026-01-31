<style>
img {
  image-rendering: pixelated;
}
</style>

<!-- omit in toc -->
# Pixel Art

**This is not complete!**

<!-- omit in toc -->
# Table of contents

1. [Guidelines](#guidelines)
   1. [Naming](#naming)
   2. [Pixelorama](#pixelorama)
2. [Animations](#animations)
3. [Guides](#guides)
4. [Planned sprites](#planned-sprites)
   1. [Humans](#humans)
      1. [Clothing](#clothing)
   2. [Bosses](#bosses)
   3. [Animals](#animals)
   4. [Weapons](#weapons)
      1. [Weapon Tiers](#weapon-tiers)
   5. [Particles](#particles)

<div style="page-break-after: always;"></div>

## Guidelines

### Naming

| Style                     | Usage                                       |
| ------------------------- | ------------------------------------------- |
| `kebab-case`<sup>A1</sup> | files, pixelorama timeline, everything else |

- <sup>A1</sup>: `kebab-case` means separating lower case words with hyphens just like in `kebab-case`.

<figure>
  <img src="./pixelorama-timeline.webp" height="300">
  <figcaption>Pixelorama timeline</figcaption>
</figure>

<div style="page-break-after: always;"></div>

### Pixelorama

**There is a very good guide available for Pixelorama [here](https://pixelorama.org/introduction).**

| Category                                        | Usage                                                                                                             |
| ----------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| Color palette                                   | Use file `apollo.gpl`<sup>B1</sup>                                                                                |
| [Layers](https://pixelorama.org/concepts/layer) | Use layering similar to the example<sup>B2</sup>                                                                  |
| Cels                                            | [Use `Link cels to` instead of duplicating pixels](https://pixelorama.org/concepts/cel/#linked-cels)<sup>B3</sup> |

<figure>
  <img src="./pixelorama-palette-apollo.webp" height="50">
  <figcaption>Apollo color palette<sup>B1</sup></figcaption>
</figure>

<figure>
  <img src="./pixelorama-layers.webp" height="300">
  <figcaption>Layering example<sup>B2</sup></figcaption>
</figure>

- <sup>B3</sup>: This makes working on the project in the future a lot easier since by editing a single linked cel, you can edit all.

<div style="page-break-after: always;"></div>

## Animations

The following examples are meant as a general guideline of how to implement animations.

<a href ="https://www.slynyrd.com/blog/2019/10/21/pixelblog-22-top-down-character-sprites">
  <figure>
    <img src="https://web.archive.org/web/20251202105638im_/https://images.squarespace-cdn.com/content/v1/551a19f8e4b0e8322a93850a/1571764518933-O01PQBVQIMKN8V1C8O7D/55-Walk_Run_2.gif" height="300">
    <figcaption>
      Walk/Run animation example<sup>C1</sup>
    </figcaption>
  </figure>
</a>

- <sup>C1</sup>: The numbers in yellow/red above/below the images are the target frames. The walking animation is 4 frames and the running animation 8 frames.
- <sup>C1</sup>: Since some of these frames are repeated, only what is shown in this image needs to be drawn. Repeating the frames can be done in code.
- <sup>C1</sup>: The perspective of this character is slightly different, it uses a `3/4 perspective` and a `32x16 sprite`.

<figure>
  <img src="./human-male.webp" height="300">
  <figcaption>Unfinished example with main character<sup>C2</sup></figcaption>
</figure>

- <sup>C2</sup>: The first row contains an example idle animation.
- <sup>C2</sup>: The second row contains an example walk/run animation.

<div style="page-break-after: always;"></div>

## Guides

Here are a few different guides that might be helpful.

- [Pixelorama](https://pixelorama.org/introduction)
- [pixelblog](https://raymond-schlitter.squarespace.com/blog)
- [pixelblog Graphical Projections 1](https://www.slynyrd.com/blog/2018/3/14/pixelblog-3-graphical-projections-1)
- [pixelblog Graphical Projections 2](https://www.slynyrd.com/blog/2018/4/12/pixelblog-4-graphical-projection-part-2)
- [pixelblog Top down tiles](https://www.slynyrd.com/blog/2019/8/27/pixelblog-20-top-down-tiles)
- [pixelblog Top down character animation](https://www.slynyrd.com/blog/2025/3/24/pixelblog-55-top-down-character-animation)
- [pixelblog Top down character sprites with 4 directional walking animation](https://www.slynyrd.com/blog/2019/10/21/pixelblog-22-top-down-character-sprites)
- [Pixel art animation](https://www.sandromaglione.com/articles/pixel-art-character-animations-guide)
- [Youtube Pixelorama guide](https://youtu.be/6srsqLhGhKk)
- [Youtube JuniperDev - Beginner to Advanced guide](https://youtu.be/DKmrBUpd0yw)

<div style="page-break-after: always;"></div>

## Planned sprites

### Humans

**SPRITE SIZE:** `16x16`

<table>
  <tr>
    <th>Category</th>
    <th>TODO</th>
  </tr>
  <tr>
    <td>
      Genders
    </td>
    <td>
      <ul>
        <li>male</li>
        <li>female</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>
      Body Shapes
    </td>
    <td>
      <ul>
        <li>thin</li>
        <li>regular</li>
        <li>large</li>
        <li>strong</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>
      Animations
    </td>
    <td>
      <ul>
        <li>idle - 2 frames</li>
        <li>walk-down - 4 frames<sup>D1</sup></li>
        <li>walk-up - 4 frames<sup>D1</sup></li>
        <li>walk-horizontal - 4 frames<sup>D1</sup></li>
        <li>jump-down - 2 frames</li>
        <li>fall-down - 2 frames</li>
        <li>jump-up - 2 frames</li>
        <li>fall-up - 2 frames</li>
        <li>jump-horizontal - 2 frames</li>
        <li>fall-horizontal - 2 frames</li>
      </ul>
    </td>
  </tr>
</table>

- <sup>D1</sup>: The walk in this case includes the run animation, therefore all 4 unique frames need to be drawn.

<div style="page-break-after: always;"></div>

#### Clothing

<table>
  <tr>
    <th>Category</th>
    <th>TODO</th>
  </tr>
  <tr>
    <td>
      Armor (can cover whole body)<sup>D2</sup>
    </td>
    <td>
      <ul>
        <li>light cloth armor, fex. dress, cloak, cape</li>
        <li>light leather armor</li>
        <li>medium chainmail armor</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>
      Clothing<sup>D2</sup>
    </td>
    <td>
      Upper
      <ul>
      <li>hood</li>
      <li>hat</li>
      </ul>
      Arms/Chest
      <ul>
        <li>shirt</li>
        <li>dress</li>
        <li>cape</li>
      </ul>
      Legs
      <ul>
        <li>jeans</li>
        <li>leather pants</li>
        <li>leggings</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>
      Accessories<sup>D2</sup>
    </td>
    <td>
      upper
      <ul>
        <li>glasses</li>
        <li>eye patch</li>
      </ul>
      lower
      <ul>
        <li>belt</li>
        <li><a href="https://en.wikipedia.org/wiki/Girdle">girdle</a></li>
        <li>chain</li>
        <li>ring</li>
        <li>book</li>
      </ul>
    </td>
  </tr>
</table>

- <sup>D2</sup>: This is just meant as an inspiration. Other styles are possible and these styles can come in different variations.
- <sup>D2</sup>: Also see: [Wikipedia - English medieval clothing](https://en.wikipedia.org/wiki/English_medieval_clothing)

<div style="page-break-after: always;"></div>

### Bosses

**SPRITE SIZE:** `16x16`-`64x64`

- [ ] TODO!

<div style="page-break-after: always;"></div>

### Animals

**SPRITE SIZE:** `16x16`-`64x64`

- [ ] Friendly Eagle
- [ ] Evil Vulture
- [ ] TODO!

### Weapons

**SPRITE SIZE:** `16x16`

- [ ] Bows
- [ ] Polearms
- [ ] Swords
- [ ] Maces

#### Weapon Tiers

I'm not sure yet whether we should differentiate each tier only by an outline or if we should use special drawings for each. Either is a viable option.

- [ ] Low
- [ ] Medium
- [ ] High
- [ ] Legendary

<div style="page-break-after: always;"></div>

### Particles

Only a single particle is ever needed, scaling of that particle and arrangement is done in code.

- [ ] Walking/Jump dust; **SPRITE SIZE:** `4x4`
- [ ] Attack dust; **SPRITE SIZE:** `4x4`
- [ ] Attack slash; **SPRITE SIZE:** `8x8` - NEEDS SPECIAL ANIMATION
- [ ] TODO!

<div style="page-break-after: always;"></div>
