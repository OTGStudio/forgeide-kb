# ForgeIDE Game Dev Pattern Knowledge Base

**300+ game development patterns** covering game AI, networking, performance, economy,
narrative, accessibility, and more — each with engine-specific implementations for
Unity, Unreal Engine 5, and Godot 4.

This knowledge base powers [ForgeIDE](https://forgeide.com)'s AI assistant, giving it
deep game development context that general-purpose AI tools lack.

## What's in here

Each pattern record includes:
- **Name and domain** (engineering, design, optimization)
- **Summary and when to use**
- **Common pitfalls**
- **Engine implementations** — real code for Unity C#, UE5 C++, and GDScript
- **Related patterns** — graph edges showing conflicts, requirements, and combinations

## Pattern domains (300+ patterns total)

- **Game AI** (25): Behavior trees, GOAP, utility AI, pathfinding, steering, crowd simulation
- **Networking** (20): Rollback netcode, client prediction, lag compensation, interest management
- **Performance** (20): GPU instancing, LOD, draw call batching, ECS layout, frame budgets
- **Game Design** (30+): Genre templates (platformer, RPG, FPS, roguelite, etc.), design-to-code bridges
- **Economy** (20+): Resource loops, pass systems, monetization patterns
- **Narrative** (15): Quest branching, NPC relationships, environmental storytelling
- **Accessibility** (15): Motor, visual, cognitive accessibility patterns
- And more: audio, rendering, physics, testing, UI architecture...

## Using this KB without ForgeIDE

The KB is plain JSON — you can use it directly in any project:

```python
import json

with open("patterns/patterns.json") as f:
    patterns = json.load(f)

# Find all networking patterns
networking = [p for p in patterns if p["domain"] == "engineering"
              and "networking" in p.get("genre_tags", [])]
```

Or integrate with your own AI toolchain by injecting patterns into your system prompt.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). All contributions require signing the CLA.

## License

[CC BY-SA 4.0](LICENSE) — OTG Studio LLC

Attribution: "ForgeIDE Knowledge Base by OTG Studio LLC (forgeide.com)"
