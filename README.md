# LoraDatasetBuilder

Generate character portrait prompts for LoRA training datasets. Runs locally on Windows — no cloud, no subscription.

---

## What it does

LoraDatasetBuilder creates structured text prompts for LoRA model training. Select your character attributes (gender, body type, age, features), pick which shot types and poses you need, and generate a full prompt set ready for image generation. Output as a ZIP of  files formatted for most training pipelines.

---

## Requirements

- Windows 10 or 11
- Node.js 18+ ([nodejs.org](https://nodejs.org))
- Optional: [ComfyUI](https://github.com/comfyanonymous/ComfyUI) for automated image generation

---

## Install

1. Download the latest  from [Releases](https://github.com/magnetik713/lora-dataset-builder/releases)
2. Extract to any folder
3. Run  — installs Node dependencies and creates a desktop shortcut
4. Run  or use the shortcut — opens the app at 

---

## Usage

### Dataset tab

1. Enter your character name in the **Subject** field
2. Choose **Gender**, **Body Type**, **Age**, and any other attributes
3. Select which **Views** (shot types) to generate prompts for
4. Click **Generate Prompts**
5. Review and edit individual prompts if needed
6. Click **Download ZIP** — get a  file per view, ready for training

### Library tab

Browse and manage previously generated prompt sets.

### Settings tab

Configure LLM and ComfyUI connections.

---

## Settings

### LLM (prompt generation)

LoraDatasetBuilder uses a local or remote LLM to write the prompts. Any OpenAI-compatible API works.

| Setting | Description |
|---------|-------------|
| LLM URL | Base URL of your LLM API (e.g.  for Ollama) |
| API Key | Leave blank for local models; required for hosted APIs |
| Model | Model name (e.g. , ) |

Recommended free options: [Ollama](https://ollama.ai) with  or .

### ComfyUI (image generation)

Optional. Connect to a running ComfyUI instance to generate training images directly from the app.

| Setting | Description |
|---------|-------------|
| Host | ComfyUI server hostname or IP (e.g. ) |
| Port | Default  |
| Workflow | Select a  workflow file — SDXL and SD1.5 workflows included |

If ComfyUI is not configured, you can still export prompts and generate images separately.

---

## Tips for dataset quality

- **One subject only** — prompts are written for a single character. Do not add secondary figures.
- **Consistent attributes** — use the same character settings for all views in a training set.
- **Shot variety** — include a mix of close-up, medium, and full-body views for better LoRA generalization.
- **Negatives** — when generating images, add strong negative prompts to prevent unwanted content from correlated training patterns (e.g. ).

---

## Free to use

LoraDatasetBuilder is free for personal and commercial use. No license key required.

---

## Related

- [SpicyPrompter](https://github.com/magnetik713/spicyprompter) — full-featured prompt builder with scene, act, and role generation
