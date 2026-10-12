# Natural Visuals

A Fabric client-side mod for Minecraft 26.2 that aims to recreate Bedrock Edition's *Vibrant Visuals*, with additional visual enhancements.

**Authors:** ImGatsu, Seo.

**Join our Discord community:** https://discord.gg/S7pRNSxSd

It runs directly on **Blaze3D (OpenGL backend)** and **Sodium 0.9.2**, without Iris or a shader pack.

## Building

Requirements: JDK 25 and an internet connection (Loom downloads Minecraft, Fabric, and Sodium).

```bash
./gradlew build        # -> build/libs/naturalvisuals-0.32.70.jar
./gradlew runClient    # Development client with Sodium
```

Place the following in your `mods` folder: the Natural Visuals JAR, Sodium 0.9.2 for Minecraft 26.2, and Fabric API.

**Iris must not be installed.** Set the graphics backend to **OpenGL** in the video settings.

In `logs/latest.log`, the following message should appear:

`[naturalvisuals] Active on OpenGL ...`

If a warning appears (Iris or Vulkan) or a shader error occurs, the mod—or the affected feature—will remain disabled.

## Current Features

- **Terrain shading and shadows:** Custom terrain shaders, sunlight and moonlight, pixelated shadows, and shadows cast by terrain and entities.
- **Sky and atmosphere:** Bedrock-inspired sky colors, sun and moon glow, atmospheric fog, and smooth lighting transitions.
- **Water rendering:** Reflections, refraction, depth-based coloring, caustics, underwater light rays, and animated waves.
- **Colored lighting:** Different light colors for torches, soul torches, redstone torches, lava, and other light sources.
- **Dynamic lighting:** Held and dropped light sources illuminate their surroundings, including light emitted by burning entities.
- **Enhanced materials:** LabPBR resource pack support, emissive textures, metallic reflections, surface highlights, and improved leaf translucency.
- **Environmental effects:** Wind-driven foliage, falling leaves, drifting petals, blowing dust, swaying lanterns and chains, rain, wet surfaces, and optional rain puddles.
- **Water interactions:** Shoreline foam, breaking waves, water spray, boat wakes, and splashes.
- **Lighting effects:** Volumetric fog, god rays, bloom, automatic exposure, and HDR-inspired tone mapping.
- **Biome-specific visuals:** Bedrock-inspired atmospheric colors, fog, lighting, and colored lava.
- **Nether and End enhancements:** Custom particles, atmospheric fog, and improved sky effects.

## Configuration

Open the Sodium video settings menu and select **Natural Visuals** to customize visual effects, lighting, shadows, water, weather, foliage, and materials.

Alternatively, edit `config/naturalvisuals.json` and press **F3 + T** to reload the configuration, Bedrock settings, and shaders.

## Known Limitations

- Iris and Vulkan rendering backends are not supported.
- Some entity and particle shadow features remain incomplete.
- Certain effects have rendering limitations involving HDR, reflections, and first-person rendering.
- Some Bedrock visual effects are approximations rather than exact reproductions.

## License

- Original code: LGPL-3.0.
- Sodium is used as a dependency.
- Bedrock sample pack assets and textures originate from Mojang's official Bedrock sample resource pack; its licensing terms must be reviewed before distribution.

## Credits

Special thanks to the creators of LumaLight, LambDynamicLights, PomPom, Fancy World Animations, and Better End Sky for ideas and references that helped inspire various features. Implementations have been adapted or independently developed as described in the original documentation.
