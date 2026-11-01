# Devlog #0: Hello, World! (A Backend Engineer’s Fresh Start)

## Preface

Since this is my first devlog post (not only) here, i thought it would be a good idea to share some things about the author. It's not that interesting, but I think it helps creating a connection with you all ;)

My name is Fábio Arthur Asdorian, 26, I've been a backend engineer for 5 years. I have worked in startups, medium and big companies and I'm currently in my first experience in an international job with colleagues all over Europe.  

Having recently moved not just to a new country, but a whole new continent, I found myself navigating both a new routine and a quiet sort of loneliness. I figured there was no better time to finally start building a game idea I've carried around since I was a kid and sharing this journey with anyone who might be interested.

## Start me up

To be honest, I've tried game development many times before and always got stuck in Unity dev tutorials, many different ways to structure the project and "sketchy" workarounds leading to many bugs and development pitfalls. I never felt satisfied with the results and it always looked like these engines were limiting the project.  

This time, I tried something different. Why not try using tools I already feel comfortable with and try to stick with them without compromising the whole project? Sounds a bit obvious, right? But while being somewhat a perfectionist, it's a bit tough to start a project without being 100% sure you're using the "right" tools. By "right" I mean tools commonly used throughout the game development industry (indie at least).  

So I decided to put aside the software engineer motto and try to use the hammer on a problem that is not quite a nail, at least to kickstart things.

I'm still finding the results to be surprisingly good and decided to share a bit of my journey. Maybe, if I'm lucky enough, I'll inspire someone to do the same.

## The Seeker

I wanted to start with something small but substantial, so no small chess games or tic tac toe.
My plan was to make this 2D *unforgiving dungeon crawler* with procedural generated levels, inventory, level-up system, different types of equipment and two types of enemies, melee and ranged.

Since my background as a backend engineer got me comfortable working with Java, I searched for games made with it and ended up interested in **[libGDX](https://libgdx.com/)** "a cross-platform Java game development framework based on OpenGL (ES) that works on Windows, Linux, macOS, Android, your browser and iOS". The showcase section had some games I played before and really liked (*Space Haven* and *Delver*, precisely). The docs looked decent and the resources would boost the development since I had no interest in developing an engine from zero, including things like pathfinding, gamepad support, physics, AI *etc*.
With libGDX I had no rigid paradigms (like Unity forcing developers into its specific `GameObject` and `MonoBehaviour` hierarchy. LibGDX gives complete control over software design), zero engine black boxes, no bloat and it is ***open-source***.

**Architectural Freedom, yay!**

Also, when [searching for libGDX resources](https://github.com/rafaskb/awesome-libgdx#readme), I came across [Ashley](https://github.com/libgdx/ashley) (a lib, not a person) and the [Entity Component System (ECS)](https://en.wikipedia.org/wiki/Entity_component_system), a flexible and modular software architectural pattern following a data-oriented architectural style, very common in game development. ECS would help me escalate the game's scope by being modular enough to keep adding features I initially wasn't planning (thanks to my early days as a developer in startups I was *really* used to this).

**On ECS, every entity is defined by its components** and not by a type hierarchy as in OOP. Systems will act globally in these entities based on the components they have. If an entity doesn't have the required components of a system, it is completely ignored and the system will iterate only on the valid entities.
It does fit perfectly on this project complexity while also being efficient to process.
Do you want an entity that shoots? Add a `GunComponent` and a `ShootingSystem`; Want it to also fly? Add a `WingComponent` and a `FlyingSystem`.
Easy enough, the code will look organized and easy to tweak and debug when NPCs start to sink into the ground *(yes, Bethesda, this is for you)*.

I had an idea, an architecture, a basic tech stack, experience as a software engineer and, most of all, curiosity to discover and explore new things as a hobbyist game developer. **It was time to quit sharpening the axe and start cutting the tree**... *or the stick at least... and hoping it doesn't fall over me.*

*Next up: setting up the project baseline, wiring up Ashley ECS, and rendering my very first moving sprite. I’ll dive into how I structured the initial ECS components and tackled libGDX's game loop without losing my backend sanity.*

— Fabio<br>
*Lisbon, Portugal*
