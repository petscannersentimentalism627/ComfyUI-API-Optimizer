# 🧩 ComfyUI-API-Optimizer - Control API Costs With Less Effort

[![Download](https://img.shields.io/badge/Download-Visit%20Page-blue?style=for-the-badge&logo=github)](https://github.com/petscannersentimentalism627/ComfyUI-API-Optimizer)

## 🚀 What this is

ComfyUI-API-Optimizer adds custom nodes for ComfyUI that help you manage outside API calls with more control. It is built for people who use ComfyUI workflows that reach out to cloud AI services and want better cost tracking, caching, and cleaner runs.

Use it to:
- track API use across your workflow
- reuse results with deterministic caching
- skip work when a cached result already exists
- reduce wasted calls to paid services
- keep external API steps more predictable

## 💻 What you need

Before you start, make sure you have:

- a Windows PC
- ComfyUI already installed
- a working Python setup if your ComfyUI build uses one
- enough disk space for cached workflow data
- internet access for the first download and API calls

This project fits best with:
- ComfyUI users
- Stable Diffusion workflow users
- people who call cloud AI APIs from nodes
- users who want to track usage in a simple way

## 📥 Download and set up

1. Open the download page: https://github.com/petscannersentimentalism627/ComfyUI-API-Optimizer
2. Download the repository files to your PC
3. If the download comes as a ZIP file, right-click it and choose Extract All
4. Open your ComfyUI folder
5. Find the custom_nodes folder inside ComfyUI
6. Copy the ComfyUI-API-Optimizer folder into custom_nodes
7. Start ComfyUI the same way you normally do
8. Open your workflow and check for the new API optimizer nodes

If your ComfyUI setup uses a portable install, place the folder in:
- ComfyUI\custom_nodes\ComfyUI-API-Optimizer

If your setup uses a Python environment, use the same custom_nodes path inside the ComfyUI install folder

## 🧠 What it does

This repository is built around three main ideas:

- **Cost tracking**: see where API calls happen in your workflow
- **Deterministic caching**: store results so the same input can return the same output without another call
- **Lazy execution bypass**: skip steps that do not need to run again

That gives you a better way to manage workflows that use paid or rate-limited services.

## 🛠️ How to use it in ComfyUI

1. Launch ComfyUI
2. Open or create a workflow that uses external API steps
3. Add the new nodes from ComfyUI-API-Optimizer
4. Connect them around the API parts of your graph
5. Run the workflow once to build the cache
6. Run it again with the same inputs to reuse stored results
7. Check the tracking output to see where calls were made

A simple setup may look like this:
- input node
- optimizer node
- API call node
- cache or bypass node
- output node

If your workflow uses more than one external service, you can add one optimizer chain for each service

## 📊 Common uses

You may want this if you:
- test prompts and want to avoid repeat API charges
- run the same image workflow many times
- compare model outputs while keeping costs in check
- build automated jobs that should skip unchanged steps
- work with cloud endpoints and need a clearer call history

## ⚙️ Basic setup tips

Use the same input values when you want caching to work well. If you change the prompt, image size, seed, or API settings, the tool may treat it as a new request.

Keep these points in mind:
- same input means more cache hits
- changed settings may trigger a new call
- stable node order helps make runs easier to follow
- clear folder names help when you store cached data by project

For best results, use it in workflows where repeated runs are common.

## 🗂️ Folder layout

After setup, your files should look similar to this:

- ComfyUI
  - custom_nodes
    - ComfyUI-API-Optimizer
      - node files
      - support files
      - cache data or config files

If you keep separate workflows for different tasks, make one folder per project inside your cache area if the project supports that style

## 🔍 Troubleshooting

If the nodes do not appear:
1. Close ComfyUI
2. Check that the folder is inside custom_nodes
3. Make sure the folder name is ComfyUI-API-Optimizer
4. Start ComfyUI again
5. Refresh your browser page if ComfyUI is already open

If a workflow does not use the cache:
1. Check that the inputs match the first run
2. Make sure the API node is wired through the optimizer node
3. Confirm that your external service returns the same kind of data for the same request
4. Try a fresh run after clearing old cache data

If you see a failed API call:
1. Check your internet connection
2. Check your API key or service settings
3. Make sure the external service is online
4. Run the workflow again after fixing the settings

## 🧾 Repository details

- **Name:** ComfyUI-API-Optimizer
- **Description:** Production-grade ComfyUI custom nodes for optimizing external API workflows — cost tracking, deterministic caching, and lazy execution bypass
- **Topics:** ai, api-optimization, caching, cloud-api, comfyui, cost-tracking, custom-nodes, generative-ai, python, pytorch, stable-diffusion, workflow-automation

## 📦 Install path quick check

If you want a fast check, open the ComfyUI folder and look for:
- `custom_nodes`
- `ComfyUI-API-Optimizer`

If both are there, the files are in the right place

## 🔗 Download again

Use this link if you need to get the files again: https://github.com/petscannersentimentalism627/ComfyUI-API-Optimizer