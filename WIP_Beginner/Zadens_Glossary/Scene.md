[RPG Manager Documentation](../../index.md) >
[Components](0-index.md) >
Scene

# Scene Component

A `scene` is the smallest of the plotting `components` and it identifies a moment in an [Act](Act.md) or a 
[Session](Session.md) in which the player characters must **DO** something.

It is important to understand that, with some rare exclusions, the scene must require some actions from the player
characters, to make sure that the story evolves.

Each `scene` can contain a synopsis (_the goal of the scene_), a trigger (_what starts the scene_) and an action (_what 
the characters should do in the scene_).

If you are using the [Scene Analyser](../analyser/index.md), you can specify the type of a `scene` to help you with the
creation of balanced [acts](Act.md) and [sessions](Session.md).

## Acts or Sessions?
It is important to understand that a `scene` is **plotted** inside an [Act](Act.md), but it is **played** inside a 
[Session](Session.md). The `scene` a hierarchically child of an [Act](Act.md) which can be added to a 
[Session](Session.md).

> **Relevant links**
>
> [Data Structure of a scene](../data/scene/index.md)
