# media-chrome client-side navigation bug

Demonstrates an issue where `<media-theme>` controls work on full page load but break on client-side navigation.

## Bug

- **Works**: Directly visiting `/player` or refreshing on that route
- **Breaks**: Navigating to `/player` from another route (e.g., `/`)

When broken, the media control bar is present in DOM but unresponsive.

## Reproduction

1. `npm install`
2. `npm run dev`
3. Visit `/` then click link to `/player` — controls broken
4. Refresh page on `/player` — controls work

## Dependencies

```bash
npm install media-chrome hls-video-element player.style
```

## Expected vs Actual

**Expected**: Controls initialize correctly regardless of navigation method  
**Actual**: Controls only work on hard navigation / full page load

## Environment

- SvelteKit 2.x
- media-chrome 4.17.2
- hls-video-element 1.5.10
- player.style 0.3.1
