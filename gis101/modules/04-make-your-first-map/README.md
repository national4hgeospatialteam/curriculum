# Module 4: Make Your First Map 🛠️  
> *“The best way to learn GIS is to make maps!”*

📝 **Tip:** For guided practice and reflection, use the companion [`worksheet.md`](./worksheet.md) or [`worksheet.docx`](./worksheet.docx) as you go.

---

## 🌍 Welcome to Your First Build

You’ve explored what GIS is, thought like a cartographer, and sharpened your spatial reasoning. Now it’s time to **create your own digital map** using **ArcGIS Online (AGOL)**, preview **QGIS**, and learn where to find trusted **data**.  
By the end, you’ll be able to open AGOL and know *what each step does, why it matters,* and *how it connects to GIS fundamentals.*

> 💡 *Think of this as your “Hello, World” for mapping.*

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

### 1) Sign In & Roles
- Sign in at **arcgis.com** using your **school/4-H credentials**.  
- Access may vary by **role** (Viewer, Editor, Publisher, etc.). Some analysis tools require elevated privileges and **credits**. If a tool is disabled, check with your admin/lead.

---

### 2) The Map Viewer: Your Workbench

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

> 🧭 **Tip:** Start with the big three: **Add → Style → Share**. Then refine with pop-ups, labels, filters, and analysis.

---

### 3) Adding Data (Three Main Ways)

| Method | Use It When | Steps |
|---|---|---|
| **Living Atlas** | You want vetted, ready-to-use layers | `Add → Browse layers → Living Atlas` |
| **Your Files** | You have a CSV/GeoJSON/zipped shapefile | `Add → Add layer → Your device` |
| **From URL** | You have a Feature/Map Service (REST) | `Add → Add layer from URL` |

**File tips**
- **CSV** must include *Lat/Long* or a geocodable field (address/city/state).  
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

---

## 🧮 Analysis in ArcGIS Online (The “Why” Engine)

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

**Credit-aware habits**
- Prefer **buffers, summarize, overlay, and joins** first (often no credits).  
- Use **Drive-Time** and **Enrich** selectively; document why they’re worth the credits.  
- Keep input layers small (filter to your area of interest).

---

### B) Quick Analysis Wins (No/Low Credits)

1. **Proximity (Buffer)**: Schools within ½ mile of parks  
2. **Summarize Within**: Count farmers markets per county  
3. **Overlay (Intersect)**: Parcels inside flood zones  
4. **Join Features (Spatial)**: Attach nearest transit stop ID to each school

> 🧪 **Mini-Lab Idea:**  
> - Buffer bus stops at ¼ mile → Summarize Within census tracts → Identify tracts with low stop coverage.

---

### C) Measurement & Query Tools (Zero Credits)

- **Measure** distance/area for quick checks.  
- **Select by rectangle/lasso** for ad-hoc queries.  
- **Filter** before exporting or sharing to focus viewers.

---

## 🧪 Guided Map Lab (Population Choropleth + Analysis)

**Goal:** Build a clean choropleth and answer one analytic question.

1. **Add** → Living Atlas → **World Countries (Generalized)**  
2. **Style** → `POP_EST` (or equivalent) with **Counts & Amounts (Color)** → 5 classes  
3. **Basemap** → Light Gray Canvas; **Legend** on; **Labels** off (for now)  
4. **Pop-up** → Show Country + Population (formatted)  
5. **Save** (clear title, tags, summary)  
6. **Analysis** (pick one):  
   - **Summarize Within**: How many people live inside your drawn region (Sketch layer → polygon)?  
   - **Join Features**: Attach continent names (from a lookup table) to countries; restyle by continent.  
   - **Overlay**: Intersect countries with a climate zone layer (Living Atlas) to compare population by zone.  
7. **Share** → Organization or Public (as allowed) → copy link

> ✅ **Deliverable:** Map link + 2–3 sentences answering your analysis question.

---

## 🧭 Freestyle Challenge (2 Layers + 1 Analysis)

Pick a theme you care about and combine **one Living Atlas layer** with **one local/open data layer**. Then run **one** analysis tool.

Examples:
- **Food Access**: Farmers markets (points) + census tracts → *Aggregate Points* (# markets per tract)  
- **Parks & People**: Park polygons + buffer of ½ mile → *Summarize Within* (population within buffers)  
- **Transit**: Bus lines + schools → *Find Nearest* (closest stop to each school; be mindful of credits)

**Checklist**
- Clear **title**, **legend**, **credits** (with dates)  
- **Symbology** matches your story  
- **Pop-ups** show the key fields  
- **Share** works; **link** opens without errors

---

## 🛠 Troubleshooting & Best Practices

| Issue | Likely Cause | Fix |
|---|---|---|
| Points in the ocean | Lat/Long swapped or wrong units | Ensure `Latitude` = −90..+90, `Longitude` = −180..+180; swap if needed |
| Layer won’t draw | Filter excludes all / scale range too tight | Clear filters; widen visibility range |
| Colors feel muddy | Basemap conflicts / too many classes | Use Light Gray; 5–7 classes max |
| Pop-ups blank | Fields not selected | Configure pop-up; pick fields and formatting |
| Public share blocked | Org policy | Share to **Organization**; ask admin about public sharing |
| Long tool run | Big inputs / unnecessary fields | Filter AOI smaller; remove unused fields; dissolve |

**Data hygiene**
- Name layers clearly; avoid “Layer 1 copy.”  
- Add **metadata** (source, date updated).  
- Keep a **CHANGELOG** in your item description for classroom projects.  
- Export a snapshot (GeoJSON) before heavy analysis.

---

## 🌍 Real-World Example

**Youth Food Access Map (Class Project → City Briefing)**  
Students combined a Living Atlas demographic layer with a local CSV of markets (SNAP yes/no). They buffered transit stops, summarized households within ½ mile, and highlighted neighborhoods with poor overlap between markets and bus access. The city used the map to propose **extended market hours** near two corridors.

**Key Takeaways**
- Start with a clear **question**.  
- Use **analysis** to move beyond “dots on a map.”  
- **Document** sources, dates, and methods so others can trust and reuse your work.

---

## ✏️ Reflection (Choose 3)

1. Which analysis tool did you try, and what did it reveal that styling alone did not?  
2. How did your symbology and basemap choices support (or distract from) the story?  
3. What assumptions did your data make (time, accuracy, coverage)?  
4. If you had credits and time, which tool would you run next — and why?  
5. What will you map next, and who needs to see it?

> 📝 **UDL Tip:** Reflect via text, 60-sec video/audio, or a one-slide mini poster.

---

## 🧰 Exit Artifact

Submit one of the following:
- 🌐 **Map link** (org/public) + 2–4 sentence findings  
- 🖼 **Screenshot** with captions of key symbology/analysis choices  
- 📝 **Short brief** (150–250 words) describing your workflow and result

📬 Send to: onboarding@national4hgeospatialteam.us

---

## 🔗 Additional Resources

- 🎥 **AGOL: Getting Started (2–5 min each)**  
  https://www.youtube.com/watch?v=LQlWLKRmAQ8&list=PLGZUzt4E4O2IJt1O_OTDFR-3dUpiCZGKf  
- 🌐 **ArcGIS Living Atlas** — curated, trustworthy layers  
  https://livingatlas.arcgis.com/  
- 🧰 **ArcGIS Learn** — step-by-step projects and tutorials  
  https://learn.arcgis.com/  
- 🏛 **data.gov** — U.S. open data portal  
  https://www.data.gov/

---

## 🎉 You Did It!

You built, styled, **analyzed**, and shared your first web map. That loop — **question → data → design → analysis → share → feedback** — is the backbone of real GIS work.

---

## 🚀 What’s Next? (StoryMaps)  

**Module 5: Tell Your Story** — turn your map into a compelling narrative with **ArcGIS StoryMaps**:
- Structure a story (title → lead → sections)  
- Embed live maps and media  
- Design for accessibility and impact  
- Publish for real audiences

🔗 [Next Module → Tell Your Story](../05-tell-your-story/README.md)

---

## 🙌 Bonus Shout-Out: QGIS (Open-Source Power)

Curious to go deeper or work offline? Explore **QGIS** — a free, open-source desktop GIS used globally.

- **Why QGIS?** Powerful geoprocessing (Processing Toolbox), flexible **GeoPackage** workflows, rich **plugins** (QuickOSM, DataPlotly), and **Print Layout** for publication-quality maps.  
- **How it fits:** Build skills in AGOL for web maps and collaboration; use QGIS for advanced analysis, offline projects, or open-data pipelines.  
- 🎥 **QGIS Playlist (Beginner → Intermediate):**  
  https://www.youtube.com/watch?v=WmobNBnN1lc&list=PLLxyyob7YmEHFg5xvwszKIo_sNZbczlNC

*Most 4-H programs have free access to Esri tools — that’s our course default. QGIS is a powerful complementary path once you’re comfortable with the basics.*
