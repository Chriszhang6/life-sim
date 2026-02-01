# Quiet Life

A cozy, interactive daily routine simulator that plays out entirely inside the browser. Quiet Life renders a home interior with a handful of rooms, detailed furniture, and a single player avatar whose needs ebb and flow over the course of each day. Tap furniture to move there, then watch the character settle in to actions like sleeping, cooking, or gardening while energy, hunger, mood, and focus react to the choices you make.

## How to experience it

1. Open `index.html` in a browser that supports Canvas (any modern browser works).
2. The game boots immediately—no build step or server required.
3. Click on visible furniture to have the character walk there and start the associated activity. If you click empty floor space, the character simply walks to that spot.

## What the game tracks

- **Stats:** Energy, hunger, mood, and focus are displayed next to the canvas. Stats decay slowly over time, so the routine is about balancing rest, nourishment, and small pleasures.
- **Time:** Each action advances time. The display shows Day/Hour:Minute, and a gentle ambient tint hints at dawn/dusk/night.
- **Actions:** Dozens of interactions exist: sleep in bedrooms, work at desks, cook in the kitchen, shower in the bathrooms, garden in the yard, pet the dog, relax on the sofa, etc. Every activity has its own duration, pose, description, and stat effects.

## Controls & interactions

- Click furniture to initiate walking + interaction.
- Click empty areas to move the avatar freely.
- Watch the action banner for what the character is doing.
- During an action, try to plan the next move while the stats update in the sidebar.

## Visual & design notes

- Rooms are rendered with painted floors, subtle patterns, and walls.
- Furniture is hand-drawn with contextual cues (shelves, pillows, plants, etc.) and layering keeps the character in front of or behind objects as required.
- Action progress shows as a small ring above the character while performing a task.
- The ambient lighting adjusts slightly for late evening / night.

## Customizing or extending

- Furniture, rooms, and actions are defined in `index.html` via the `state.world` and `ACTIONS` data structures. You can add new furniture by giving it `type`, `label`, `action`, and optional `isPrimary`/`facing` hints plus a matching drawing routine.
- Stat decay, time scale, and move speed are configurable inside the `CONFIG` object.
- Rendering sits inside the `render` function—feel free to swap palettes, add effects, or plug in new UI overlays.

Enjoy letting the Quiet Life unfold at your own pace.