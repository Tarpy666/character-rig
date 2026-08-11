# CharacterRig

Skeletal rig: bones, IK two-bone solver, blend trees, walk cycle parameters.

Part of the Counted fleet (character-rig), generated from `seeds/seeds.yaml`.

## Architecture

- `src/modules.ts` — BoneHierarchy, TwoBoneIK, BlendTree
- `src/index.ts` — public API (`SPEC`, `MODULES`, Registry)
- `src/rng.ts` — deterministic seeded PRNG (mulberry32)
- `tests/index.test.ts` — deterministic behavior suite

## Usage

```bash
npm install
npm run typecheck   # strict TS, zero errors
npm test            # deterministic, seeded
npm run build
```

## Determinism

All outputs are seeded; identical inputs produce identical results on any runtime.
