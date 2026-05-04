# ComfyUI Custom Nodes (Meta Repository)

This repository manages a collection of ComfyUI custom nodes using Git submodules.

Each submodule represents a separate custom node repository.

---

## 📁 Structure

After cloning, the repository will look like:

```

custom_nodes/
node_a/
node_b/
node_c/

````

Each folder is a git submodule pointing to an external repository.

---

## 🚀 Setup

Clone with submodules:

```bash
git clone --recurse-submodules http://<gitlab-url>/medlabotx/comfyui/custom_nodes.git
````

If already cloned:

```bash
git submodule update --init --recursive
```

---

## 🔄 Updating nodes

To update all nodes to their configured versions:

```bash
git pull
git submodule update --init --recursive
```

To update submodules to latest remote commits:

```bash
git submodule update --remote --recursive
```

---

## ➕ Adding a new node

```bash
git submodule add http://<gitlab-url>/group/node_repo.git <node_name>
git commit -m "Add new custom node"
```

---

## ⚠️ Notes

* This repository only manages references to node repositories.
* Each node may have its own dependencies and installation requirements.
* Intended for use with ComfyUI startup automation systems.

---
