# Public artifact status and evidence boundaries

## Included evidence

- Source modules and supporting scripts are included.
- Agent YAML, prompts, skills, and configuration variants are included.
- Unit and integration test source files are included.
- Technical documentation records the intended workflow and prior validation steps.

## Claims that are supported by the project documentation

- Official-harness validation and compilation were reported as passing for the documented V1.1 submission package.
- An end-to-end test with a scripted model was reported as passing.
- A limited repository-localization experiment was reported, with its AST and lexical-proxy limitations disclosed.

## Claims that are not supported

- No real Gemma 4 model repair success rate is available.
- No official Kaggle leaderboard score is available for this project.
- The scripted-model pipeline check is not evidence of real-model performance.
- No claim of first place, state-of-the-art performance, or hidden-test success is made.

## Architecture alignment note

The documented V1.1 configuration is a single main agent. Specialist sub-agents are described as off in V1.1 and enabled only in an experimental V2 variant. Any paper description of a read-only analysis agent must therefore be framed as optional/proposed or explicitly tied to the experimental variant, not as an always-active component of V1.1.
