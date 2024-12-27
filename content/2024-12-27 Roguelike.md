+++
title = "Roguelike"
date = 2024-12-27T13:32:15-05:00
authors = ["sarksus"]
[taxonomies]
tags = ["Gamedev", "Writing"]
+++

I have had some open world roguelike ideas percolating in my head these last few years. The world I’m making for my book would also be well suited for a roguelike, particularly in the past when the remnants of the empire and the newer republics were still kicking around fucking up the world. I’ve also been playing a lot of roguelikes lately so I’m just in the mood to try and push forward on this. 

I’ve started demoing both Godot and Bevy for developing the game. Godot would overall be easier to learn and use but Bevy’s ECS would be extremely well suited to the roguelike I want to make. I want to build a lot of dynamic entities and systems that influence the world. But Bevy is a Rust game engine that is still pretty new so I would have to contend with Rust’s barrier of entry and the lack of built-in tools. There are quite a number of third party crates that help fill in gaps but it means learning a number of unrelated crates that don’t necessarily follow the same ergonomics or documentation.

I’m going to try both and see which one I liked using the most. I’ll just implement a really basic roguelike in each, just a level with some enemies and neutrals trying to achieve various personal goals like finding food, avoiding danger, or intentionally finding people to fight. 