---
stepsCompleted: [1, 2]
inputDocuments: []
date: 2026-01-07
author: 1vecera
projectName: leafblossom
workflowStatus: in-progress
---

# Product Brief: leafblossom

<!-- Content will be appended sequentially through collaborative workflow steps -->

## Executive Summary

leafblossom is a modern, beautiful, and highly customizable decision tree visualization library for Python that bridges the gap between complex machine learning models and human understanding. Designed for data scientists who need to explain model behavior to business stakeholders, leafblossom transforms unwieldy decision trees into clear, interactive, and aesthetically pleasing visualizations that reveal the true limits of model predictability.

Unlike existing solutions that are either too simplistic (sklearn.tree.plot), visually overwhelming (dtreeviz), or lack critical customization options, leafblossom provides the perfect balance of beauty, interactivity, and granular control. With seamless integration into scikit-learn and XGBoost workflows, leafblossom empowers data scientists to confidently communicate model decisions, set realistic expectations, and prevent costly misunderstandings in business decision-making.

---

## Core Vision

### Problem Statement

Data scientists working with decision tree-based models (decision trees, Random Forest, XGBoost) face a critical visualization gap: existing tools are either too simplistic, aesthetically unpleasing, or completely unwieldy for trees beyond depth 5-6. This forces data scientists to either abandon visualization entirely, rely on textual outputs, or use global feature importance tools like SHAP that fail to reveal the actual decision logic and limits of predictability.

The impact is profound: business stakeholders misunderstand model capabilities, demand unrealistic performance targets, and make decisions based on incorrect assumptions about how models segment and predict. Data scientists waste time arguing about predictability limits instead of collaborating on actionable insights.

### Problem Impact

- **Model Opacity**: Teams cannot see how models actually make decisions, leading to "black box" distrust
- **Business Misalignment**: Stakeholders expect "magic bullets" (80% precision on tiny segments) that are mathematically impossible
- **Communication Breakdown**: Data scientists struggle to explain WHY certain predictions cannot be made
- **Wasted Effort**: Endless debates about model limits that could be resolved with proper visualization
- **Poor Adoption**: Beautiful, powerful models go unused because stakeholders cannot understand them

### Why Existing Solutions Fall Short

**Current Landscape:**
1. **sklearn.tree.plot** - Not customizable, visually unappealing, rigid output
2. **dtreeviz** - "Crazy out of this world" visual style, unreadable for large trees, limited customization
3. **supertree** (new competitor) - Interactive and promising, but lacks aesthetic polish and deep node customization
4. **SHAP** - Shows global feature importance but NOT decision paths or predictability limits
5. **Textual output** - Painful fallback, inaccessible to non-technical stakeholders
6. **Graphviz** - Rare, clunky, not integrated with ML workflows

**Critical Gaps:**
- **No control over node metrics** - Cannot customize what data appears on each node
- **Aesthetic extremes** - Either ugly or overwhelming, no professional middle ground
- **Large tree unusability** - Depth 6+ becomes unreadable mess
- **Limited interactivity** - Most tools are static or have primitive interaction
- **Outdated feel** - Current tools feel like relics, not modern data science products

### Proposed Solution

leafblossom is a next-generation decision tree visualization library that combines extreme aesthetic polish with deep customization and smart interactivity. Designed for modern data science workflows, leafblossom integrates seamlessly with scikit-learn and XGBoost, transforming complex tree structures into beautiful, navigable visualizations that reveal exactly how models make decisions.

**Core Capabilities:**

1. **Beautiful, Modern Design**
   - Clean, minimalist UI with intelligent information density
   - Professional color schemes that don't "scream" (inspired by proven data visualization palettes)
   - Elegant Lora typography for maximum readability
   - Aesthetic standard that rivals modern web applications, not just "good for a data tool"

2. **Smart Compactness**
   - **Default view: First 4 layers** - Large trees become instantly manageable
   - **Folded nodes show split quality** - Instant insight without expansion
   - **Focus mode** - Highlight single decision paths, fold everything else
   - **Interactive depth control** - Drill down when needed, zoom back out for context

3. **Unmatched Node Customization**
   - **Binary classification**: Show percentage of positive cases per node
   - **Multiclass**: Display percentage distribution for each class
   - **Path clarity**: Variable name and threshold on every decision link
   - **Future extensibility**: User-configurable node templates (planned)

4. **Rich Interactivity**
   - Fold/unfold specific nodes and branches
   - Dynamic depth adjustment (show more/less of tree)
   - Path highlighting to leaves with full decision trace
   - Color customization for different node types/depths
   - Fullscreen mode for Jupyter notebooks
   - Direct links from visualization to actual data samples
   - Search and zoom functionality

5. **ML Library Integration**
   - Native support for scikit-learn decision trees
   - Native support for XGBoost models
   - Handle both standalone trees and ensembles (Random Forest, XGBoost)
   - Surrogate model visualization for complex ensembles

### Key Differentiators

**Three Unfair Advantages:**

1. **Aesthetic Excellence**
   - **Where competitors are ugly or overwhelming, leafblossom is beautiful and professional**
   - Modern UI design standards, not "academic tool" aesthetics
   - Makes data science presentations look polished and credible
   - First visualization tool stakeholders actually enjoy viewing

2. **Deep Node Customization**
   - **Where competitors are rigid, leafblossom gives you complete control**
   - Choose exactly what metrics appear on each node
   - Adapt visualization to your message and audience
   - Show the RIGHT information for the RIGHT decision-making conversation

3. **Smart Information Architecture**
   - **Where competitors overwhelm, leafblossom curates**
   - Default 4-layer view prevents information overload
   - Quality indicators on folded nodes provide insight without expansion
   - Focus mode for deep dives into specific decision paths
   - Designed for both exploration (overview) and explanation (specific paths)

**Why Now?**
- The data science community is hungry for modern, polished tools
- Current visualization tools feel outdated and clunky
- Business demand for model explainability is at an all-time high
- Competitors like supertree validate the market but leave room for a premium option
- Remote work makes visual communication more critical than ever
