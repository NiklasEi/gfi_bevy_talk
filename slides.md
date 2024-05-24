---
layout: cover
theme: dracula
background: bistro_masked.jpg
favicon: https://www.nikl.me/favicon.ico
---

# The Open Source Game Engine Bevy

A refreshingly simple data-driven game engine built in Rust
Free and Open Source Forever!

<div class="footnotes-right">
<a href="https://github.com/DGriffin91/bevy_bistro_scene">https://github.com/DGriffin91/bevy_bistro_scene</a>
</div>
---
layout: image-right
image: oicana.png
imageColClass: oicana-image
---

# Niklas Eicker

- Software consultant
- Using Bevy in my free-time for more than 3 years
- Maintaining multiple open source Bevy extensions/projects
<br/>
<br/>

<mdi-github/> https://github.com/NiklasEi

<div class="footnotes-right">
<a href="https://niklme.itch.io/oicana">https://niklme.itch.io/oicana</a>
</div>
---
layout: image-right
image: bevy_github.png
---

# Bevy

- First version August 2020
- 2D and 3D renderer
- 6 officially supported platforms
- Licensed MIT OR Apache 2.0
- Active community [^1]

[^1]: https://discord.gg/bevy
<div class="footnotes-right">
<a href="https://github.com/bevyengine/bevy">https://github.com/bevyengine/bevy</a>
</div>
---
layout: image-right
image: tunnet_steam.png
---

# Projects using Bevy

- hundreds of small games on itch.io [^1]
- some projects on steam and mobile stores
- Usage outside of game dev (e.g. CAD)

<br/>

<img alt="Bevy games on itch.io" src="/bevy_on_itch.png" width="500"/>

[^1]: https://itch.io/games/tag-bevy
<div class="footnotes-right">
<a href="https://store.steampowered.com/app/2286390/Tunnet">https://store.steampowered.com/app/2286390/Tunnet</a>
</div>
---
layout: image-right
image: bevy-logo.png
class: bigger-left
imageColClass: logo
---

# What makes Bevy different?

- Written in Rust
- Everything based on Entity Component System (ECS)
- Very modular (~40 "plugins")

<div class="footnotes-right">
Bevy logo (<a href="http://opensource.org/licenses/MIT">MIT</a>)
</div>
---
layout: image-right
image: rust-logo.png
imageColClass: logo
---

# Rust

- Performance comparable with C and C++
- Automatic memory management without GC
- Nice, modern tooling

<div class="footnotes-right">
Rust logo (<a href="https://creativecommons.org/licenses/by/4.0/">CC-BY</a>)
</div>


---

# Entity Component System (ECS)

- Separation of Data and behaviour
- Can lead to very modular code
- Good performance

--- 

# Short Intro to ECS


*Entity*: Unique identifier for anything in the "world" (e.g. player, tree, camera)

*Component*: Data; components get attached to entities

*System*: Behaviour; can manipulate components

---
layout: image-right
image: bevy_crates.png
---

# Bevy Plugins

- Group systems and related components by domain
- Easy to use from third-party crates
- This is how the whole engine is built up!

<div class="footnotes-right">
<a href="https://github.com/bevyengine/bevy/tree/main/crates">https://github.com/bevyengine/bevy/tree/main/crates</a>
</div>
---

# Bevy - Hello World

```rust
use bevy::prelude::*;

fn main() {
  App::new().add_systems(Startup, hello_world).run();
}

fn hello_world() {
  println!("Hello World");
}
```
---

# Bevy ECS

A system spawning a new entity with a custom component
```rust
fn my_system(mut commands: Commands) {
    commands.spawn(MyComponent {
        data: 42.,
        more_data: "Hello there!".into()
    });
}

#[derive(Component)]
struct MyComponent {
    data: f32,
    more_data: String
}
```
---
# Time to play around with Bevy
---