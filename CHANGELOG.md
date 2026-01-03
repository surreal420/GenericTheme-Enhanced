# Changelog

## New Features

### 1. Bomb Classification System
- Bombs are now divided into two types:
  - **Normal Bomb**: Explosion effects for regular notes
  - **LN Bomb**: Dedicated explosion effects for Long Notes
- Resource directory structure:
  - `customize/bomb/normal/` - Normal bombs
  - `customize/bomb/ln/` - LN bombs

### 2. Bomb Scaling Factor
- Added `factor` parameter to control the base scaling of bombs
- **formula**:
  ```
  bomb width = (scratch lane width * 2) * factor + user offset w
  ```

### 3. Frame Time Control
- Added `frame_time` parameter to control the duration of each frame in bomb animations (milliseconds)
- Allows different bombs to have different playback speeds
- Example: `frame_time = 10` means each frame lasts 10ms, resulting in faster animation

### 4. New Custom Bombs
- **cyan**: Cyan ring explosion
- **blueburst**: Blue burst

---

## Configuration Example

```lua
-- customize/bomb/normal/*bomb_name*.lua
return {
    w = 600,            -- Single frame width
    h = 600,            -- Single frame height
    divx = 4,           -- Horizontal division count
    divy = 4,           -- Vertical division count
    factor = 1.5,       -- Scaling factor (new)
    frame_time = 15.625 -- Frame duration in ms (optional)
}
```
