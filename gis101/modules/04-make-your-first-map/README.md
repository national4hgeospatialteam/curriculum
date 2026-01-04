# Module 4: Make Your First Map 🛠️  
> *“The best way to learn GIS is to make maps!”*

📝 **Tip:** For guided practice and reflection, use the companion [`worksheet.md`](./worksheet.md) or [`worksheet.docx`](./worksheet.docx) as you go.

---

## 🌍 Welcome to Your First Build

You’ve explored what GIS is, thought like a cartographer, and sharpened your spatial reasoning. Now it’s time to **create your own digital map** using **ArcGIS Online (AGOL)**, preview **QGIS**, and learn where to find trusted **data**.  
By the end, you’ll be able to open AGOL and know *what each step does, why it matters,* and *how it connects to GIS fundamentals.*

> 💡 *Think of this as your “Hello, World” moment for mapping.*

---

## 🎯 Learning Goals

By the end of this module, you’ll be able to:

- **Navigate** AGOL’s Map Viewer (interface, panels, save/share)  
- **Add** data from Living Atlas, files, and URLs  
- **Style** layers with meaningful symbology + basemaps  
- **Configure** pop-ups, labels, filters, and layer visibility  
- **Analyze** spatial relationships (buffer, summarize, overlay, join)  
- **Share** a clean, documented, and working web map  
- **Locate** reliable datasets and understand data credit/permission basics  
- **Preview** how QGIS fits into a broader GIS toolkit

✅ *Success check:* you can build, style, analyze, and share a map link that others can open.

---

## ⏱️ Warm-Up: Map Inspiration (5 min)

Find any online map (Living Atlas, news article, StoryMap, city open data). Answer:

- What story is it telling, and who’s the audience?  
- What data is shown, and how is it styled?  
- What choices (basemap, color, labels) help or hurt clarity?  
- How might you recreate a simple version?

> 🎨 **UDL Tip:** Respond with text, a sketch, or a 30–60 sec audio/video note.

---

## 🧠 Before You Click: GIS Essentials (Quick Refresher)

- **Layer** = one dataset (points/lines/polygons/rasters). Your map stacks layers.  
- **Geometry** (where) + **Attributes** (what) = meaningful symbology & analysis.  
- **Projection** = how the curved Earth is drawn flat. AGOL handles most web projections automatically, but local accuracy can vary.  
- **Metadata** = who created the data, when, how; trust starts here.

---

## 🛰 ArcGIS Online (AGOL) Deep Dive

🎥 **Get started with Esri's series..:** [Get Started with ArcGIS Online](https://www.youtube.com/watch?v=LQlWLKRmAQ8&list=PLGZUzt4E4O2IJt1O_OTDFR-3dUpiCZGKf&index=1) *(~3 min)*

🎥 **Brandon's tutorial on how to use ArcGIS Online:** [ArcGIS Online Tutorial](https://www.youtube.com/watch?v=iz9eurz0uC8)

---

### 1) Sign In & Roles
- Sign in at **arcgis.com** using your **school/4-H credentials**.  
- Access may vary by **role** (Viewer, Editor, Publisher, etc.). Some analysis tools require elevated privileges and **credits**. If a tool is disabled, check with your admin/lead.

---

### 2) The Map Viewer: Your Workbench

🎥 **Quick Overview:** [Mapping Basics](https://www.youtube.com/watch?v=toawx4D-htc&list=PLGZUzt4E4O2IJt1O_OTDFR-3dUpiCZGKf&index=2) *(~3 min)*

When you click **Map**, you’ll open Map Viewer.

| Area | What It’s For |
|---|---|
| **Add** | Add data (Living Atlas, your files, URLs/Services) |
| **Basemap** | Pick contextual background; neutral = better readability |
| **Layers Panel** | Toggle visibility, reorder, group, filter, labeling |
| **Styles** | Choose field + visualization (color, size, type, charts) |
| **Pop-ups** | Configure what users see on click (fields, media, charts) |
| **Analysis** | Spatial tools: buffer, overlay, summarize, join, enrich |
| **Search/Geocode** | Find places/addresses; can add to map |
| **Settings (⚙️)** | Units, blending, measure, capture, performance |
| **Save / Share** | Name, tags, summary; org/shared/public access |

<details>
  <summary>🎥 Optional: Explore 3D Scenes (Scene Basics)</summary>

  [Scene Basics](VIDEO_LINK_HERE) *(~2 min)*  
  *Curious about 3D mapping? Learn how Scene Viewer brings elevation and buildings to life.*
</details>

> 🧭 **Tip:** Start with the big three: **Add → Style → Share**. Then refine with pop-ups, labels, filters, and analysis.

---

### 3) Adding Data (Three Main Ways)

🎥 **Brandon's tutorial on how to make your own data!** [Video](https://youtu.be/gLR2hbRbx40) 

🎥 **Reference:** [Content Basics](https://www.youtube.com/watch?v=vSNcUq_eFwg&list=PLGZUzt4E4O2IJt1O_OTDFR-3dUpiCZGKf&index=4) *(~3 min)*  
🎥 **Reference:** [Data Basics](https://www.youtube.com/watch?v=N2DypYUBYzk&list=PLGZUzt4E4O2IJt1O_OTDFR-3dUpiCZGKf&index=5) *(~5 min)*

| Method | Use It When | Steps |
|---|---|---|
| **Living Atlas** | You want vetted, ready-to-use layers | `Add → Browse layers → Living Atlas` |
| **Your Files** | You have a CSV/GeoJSON/zipped shapefile | `Add → Add layer → Your device` |
| **From URL** | You have a Feature/Map Service (REST) | `Add → Add layer from URL` |

**File tips**
- **CSV or Excel** must include *Lat/Long* or a geocodable field (address/city/state).  
- **Shapefile** = upload as a **.zip** (all component files included).  
- **GeoJSON** imports cleanly and preserves attributes.  
- **Services** ideally end with `/FeatureServer` (editable/queryable) or `/MapServer`.

---

### 4) Symbology & Design (Make Data Speak)

1. Select layer → **Styles** → choose an **attribute field**.  
2. Pick visualization:
   - **Counts & Amounts (Color)**: choropleth for numeric ranges  
   - **Types (Unique Symbols)**: categories/classes  
   - **Size**: proportional/graduated symbols  
   - **Relationship/Charts**: compare two fields (advanced)
3. **Basemap**: prefer neutral (Light Gray Canvas) to keep focus on data.  
4. **Legend**: enable and check class breaks; adjust to match your story.  
5. **Labels**: only where useful; keep legible at target scale.  
6. **Accessibility**: use color-blind-safe ramps; rely on more than color (size, shape, text) when possible.

> 📏 **Visibility Range:** show dense layers only when zoomed in (reduces clutter).

---

### 5) Layer Controls You’ll Use Constantly

- **Reorder layers** (drag): points above polygons above rasters.  
- **Transparency**: soften polygons to reveal basemap context.  
- **Filter**: include only features that meet your criteria (e.g., parks ≥ 5 acres).  
- **Blend modes**: visually combine layers (multiply, overlay) to see overlaps.  
- **Group layers**: keep related layers together (e.g., transit lines + stops).  
- **Calculate field** (where allowed): derive new attributes.  
- **Time enable** (if supported): animate changes over time.

---

### 6) Pop-Ups: Tell a Micro-Story on Click

- Turn on **Pop-ups** → choose fields to display.  
- **Format** numbers (commas, decimals, units).  
- Add **media** (image from URL, small chart) when it clarifies the story.  
- Keep it short—less is more. Link out for details if needed.

> Want to see a real use case of this? Check out this YouTube video of pop ups being used to elevate a StoryMap used by students in a Model UN conference [here!](example.com)

---

## 🧮 Analysis in ArcGIS Online (The “Why” Engine)

🎥 **Watch:** [Analysis Basics](https://www.youtube.com/watch?v=pEFqVebemq8&list=PLGZUzt4E4O2IJt1O_OTDFR-3dUpiCZGKf&index=8) *(~3 min)*

> Some tools **consume credits** and require **Publisher/Creator**-level privileges. Start with low-volume tests; check with your org admin.

### A) Core Vector Analysis Tools (Map Viewer → **Analysis**)

| Tool Group | Tool | What It Answers |
|---|---|---|
| **Use Proximity** | **Create Buffers** | What’s within X miles/minutes? |
|  | **Drive-Time Areas** *(credits)* | What’s reachable in 5/10/20 minutes by road? |
|  | **Find Nearest** *(credits)* | Which facility is closest to each location? |
| **Summarize Data** | **Aggregate Points** | How many points fall inside each area? |
|  | **Summarize Within** | Sum/avg fields of features within polygons |
|  | **Join Features** | Attribute or spatial join across layers |
| **Overlay Layers** | **Intersect/Union/Erase** | Where do features overlap? What’s common/different? |
| **Find Locations** | **Find Existing/Derive New** | Select features meeting multi-criteria rules |
| **Manage Data** | **Dissolve/Clip/Merge/Extract** | Clean up, cut out, and combine datasets |
| **Analyze Patterns** | **Hot Spot / Outlier** *(credits)* | Are there statistically significant clusters? |
| **Enrich Data** | **Enrich Layer** *(credits)* | Append demographics, spending, etc. to features |

---

### B) Quick Analysis Wins (No/Low Credits)

| 🎯 **Question** | 🧰 **Tool** | 🗺️ **Example Workflow** |
|---------------|------------|--------------------------|
| “What’s nearby?” | **Create Buffers** | Buffer park polygons by ½ mile to visualize walkable catchments around green spaces. |
| “How many are inside?” | **Summarize Within** | Count farmers markets (points) inside each county polygon to compare access regionally. |
| “What overlaps?” | **Overlay (Intersect)** | Identify parcels that fall inside flood zones by intersecting two polygon layers. |
| “Which is closest?” | **Find Nearest** *(may use credits)* | For each school, find the nearest bus stop to measure transit accessibility. |
| “What attributes match spatially?” | **Join Features (Spatial)** | Attach census tract population data to farmers market points based on location, then style by tract population served. |

---

## 🧪 Guided Map Lab (Population Choropleth + Analysis)

🎥 **Optional Support:**  
<details>
  <summary>🧠 Playlist Reference: Data + Sharing Basics</summary>

  - [Data Basics](https://www.youtube.com/watch?v=N2DypYUBYzk&list=PLGZUzt4E4O2IJt1O_OTDFR-3dUpiCZGKf&index=5)
  - [Sharing Basics](https://www.youtube.com/watch?v=aEcXNVXLLbU&list=PLGZUzt4E4O2IJt1O_OTDFR-3dUpiCZGKf&index=6)
</details>

...

---

## 🛠 Troubleshooting & Best Practices

<details>
  <summary>🎥 Optional: Group & App Basics (Collaboration + Publishing)</summary>

  - [Group Basics](https://www.youtube.com/watch?v=L2BT2C07RHc&list=PLGZUzt4E4O2IJt1O_OTDFR-3dUpiCZGKf&index=8)
  - [App Basics](https://www.youtube.com/watch?v=rbUNtd_71X8&list=PLGZUzt4E4O2IJt1O_OTDFR-3dUpiCZGKf&index=10)
</details>

---

## 🔗 Additional Resources

<details>
  <summary>🎥 Full ArcGIS Online “Getting Started” Playlist</summary>

  [YouTube Playlist]((https://www.youtube.com/watch?v=LQlWLKRmAQ8&list=PLGZUzt4E4O2IJt1O_OTDFR-3dUpiCZGKf)
</details>

---

## 🙌 Bonus: QGIS (Open-Source Power)

Curious to go deeper or work offline? Explore [**QGIS**](https://qgis.org) — a free, open-source desktop GIS used globally.

🎥 **QGIS Beginner Playlist:** [YouTube](https://www.youtube.com/watch?v=WmobNBnN1lc&list=PLLxyyob7YmEHFg5xvwszKIo_sNZbczlNC)

---

**Ready to continue your journey?**

[**Next Module: Tell Your Story** →](../05-tell-your-story/README.md)
