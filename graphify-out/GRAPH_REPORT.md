# Graph Report - SIH  (2026-10-22)

## Corpus Check
- 24 files · ~29,703 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 53 nodes · 68 edges · 17 communities (16 shown, 1 thin omitted)
- Extraction: 79% EXTRACTED · 21% INFERRED · 0% AMBIGUOUS · INFERRED: 14 edges (avg confidence: 0.8)
- Token cost: 0 input · 0 output

## Community Hubs (Navigation)
- [[_COMMUNITY_Community 0|Community 0]]
- [[_COMMUNITY_Community 1|Community 1]]
- [[_COMMUNITY_Community 2|Community 2]]
- [[_COMMUNITY_Community 3|Community 3]]
- [[_COMMUNITY_Community 4|Community 4]]
- [[_COMMUNITY_Community 5|Community 5]]

## God Nodes (most connected - your core abstractions)
1. `createAutonomousBuoy()` - 7 edges
2. `generateBrushedMetalMap()` - 7 edges
3. `createBharatiStation()` - 5 edges
4. `generateIceFractureMap()` - 5 edges
5. `createOceanSurface()` - 4 edges
6. `createBiologgerSeal()` - 3 edges
7. `createCTDSonde()` - 3 edges
8. `createPolarGlaciers()` - 3 edges
9. `generateHDPEBumpMap()` - 3 edges
10. `generateSealSkinBumpMap()` - 3 edges

## Surprising Connections (you probably didn't know these)
- `createAutonomousBuoy()` --calls--> `generateBrushedMetalMap()`  [INFERRED]
  src/components/3d/AutonomousBuoyVFX.js → src/components/3d/ProceduralTextures.js
- `createAutonomousBuoy()` --calls--> `generateHDPEBumpMap()`  [INFERRED]
  src/components/3d/AutonomousBuoyVFX.js → src/components/3d/ProceduralTextures.js
- `createAutonomousBuoy()` --calls--> `generateSolarCellTexture()`  [INFERRED]
  src/components/3d/AutonomousBuoyVFX.js → src/components/3d/ProceduralTextures.js
- `createAutonomousBuoy()` --calls--> `generatePCBTexture()`  [INFERRED]
  src/components/3d/AutonomousBuoyVFX.js → src/components/3d/ProceduralTextures.js
- `createAutonomousBuoy()` --calls--> `generateBenthicBiofoulingMap()`  [INFERRED]
  src/components/3d/AutonomousBuoyVFX.js → src/components/3d/ProceduralTextures.js

## Communities (17 total, 1 thin omitted)

### Community 0 - "Community 0"
Cohesion: 0.2
Nodes (4): createAtmosphere(), setupPostProcessing(), createSplashSystem(), createUnderwaterVFX()

### Community 1 - "Community 1"
Cohesion: 0.62
Nodes (5): createAutonomousBuoy(), generateBenthicBiofoulingMap(), generateHDPEBumpMap(), generatePCBTexture(), generateSolarCellTexture()

### Community 2 - "Community 2"
Cohesion: 0.48
Nodes (5): createBharatiStation(), createCTDSonde(), generateBrushedMetalMap(), generateHelipadTexture(), generateIndianFlagTexture()

### Community 3 - "Community 3"
Cohesion: 0.6
Nodes (3): createPolarGlaciers(), generateIceFractureMap(), createSeaIceFloes()

### Community 4 - "Community 4"
Cohesion: 0.83
Nodes (3): createOceanSurface(), generateOceanFoamMap(), generateWaterNormalMap()

## Knowledge Gaps
- **1 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `createAutonomousBuoy()` connect `Community 1` to `Community 0`, `Community 2`?**
  _High betweenness centrality (0.059) - this node is a cross-community bridge._
- **Why does `createBharatiStation()` connect `Community 2` to `Community 0`?**
  _High betweenness centrality (0.037) - this node is a cross-community bridge._
- **Why does `generateBrushedMetalMap()` connect `Community 2` to `Community 1`?**
  _High betweenness centrality (0.034) - this node is a cross-community bridge._
- **Are the 5 inferred relationships involving `createAutonomousBuoy()` (e.g. with `generateHDPEBumpMap()` and `generateSolarCellTexture()`) actually correct?**
  _`createAutonomousBuoy()` has 5 INFERRED edges - model-reasoned connections that need verification._
- **Are the 3 inferred relationships involving `generateBrushedMetalMap()` (e.g. with `createAutonomousBuoy()` and `createBharatiStation()`) actually correct?**
  _`generateBrushedMetalMap()` has 3 INFERRED edges - model-reasoned connections that need verification._
- **Are the 3 inferred relationships involving `createBharatiStation()` (e.g. with `generateIndianFlagTexture()` and `generateHelipadTexture()`) actually correct?**
  _`createBharatiStation()` has 3 INFERRED edges - model-reasoned connections that need verification._
- **Are the 2 inferred relationships involving `generateIceFractureMap()` (e.g. with `createPolarGlaciers()` and `createSeaIceFloes()`) actually correct?**
  _`generateIceFractureMap()` has 2 INFERRED edges - model-reasoned connections that need verification._