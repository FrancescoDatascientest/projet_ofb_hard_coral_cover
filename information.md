
| Variable | Type | Description |
|-----------|------|-------------|
| `REEF_ID` | String | Unique identifier of the reef. Stable across years. |
| `REEF_NAME` | String | Name of the reef. |
| `A_SECTOR` | Categorical | Geographic management sector of the reef within the GBR. |
| `SHELF` | Categorical | Shelf position of the reef: Inner-shelf, Mid-shelf, or Outer-shelf. Reflects exposure and oceanographic conditions. |
| `LAT` | Float | Latitude of the reef centroid (decimal degrees). |
| `LON` | Float | Longitude of the reef centroid (decimal degrees). |
| `SITE_LAT` | Float | Latitude of the monitored site within the reef. |
| `SITE_LON` | Float | Longitude of the monitored site within the reef. |
| `SITE_NO` | Integer | Numeric identifier of the site within a reef. |
| `TRANSECT_NO` | Integer | Numeric identifier of the transect within a site. Permanent monitoring transects are repeatedly surveyed over time. |

---

### 📅 Temporal Variables

| Variable | Type | Description |
|-----------|------|-------------|
| `REPORT_YEAR` | Integer | Year in which the survey was conducted. |
| `RST` | String | Unique identifier for Reef–Site–Transect combination. Constant over time. |
| `RSTY` | String | Unique identifier for Reef–Site–Transect–Year combination. Fully unique row identifier. |

---

### 🪸 Ecological Response Variables

| Variable | Type | Description |
|-----------|------|-------------|
| `COVER` | Float | Percentage (%) of live hard coral cover measured along the transect. |
| `HC` | Float | Coral health / coral cover condition metric used as the main response variable in this project (**prediction target**). |
| `HC_1` | Float | Lagged value of `HC` from the previous year (t-1). Captures temporal dependency and ecological inertia. |

---

### ⚠️ Disturbance Variables

| Variable | Type | Description |
|-----------|------|-------------|
| `DISTURBANCE` | Categorical | Dominant disturbance category observed during the survey year (e.g., None, COTS, Storm, etc.). |
| `COTS` | Binary (0/1) | Presence (1) or absence (0) of Crown-of-Thorns starfish outbreak. |
| `STORM` | Binary (0/1) | Indicator of cyclone or severe storm impact during the year. |
| `BLEACHING` | Binary (0/1) | Indicator of coral bleaching event. |
| `DISEASE` | Binary (0/1) | Indicator of coral disease presence. |
| `C` | Float | Intensity or proportional metric associated with COTS disturbance. |
| `S` | Float | Intensity or proportional metric associated with storm disturbance. |
| `B` | Float | Intensity or proportional metric associated with bleaching disturbance. |
| `D` | Float | Intensity or proportional metric associated with disease disturbance. |

---

### Ecological Metrics

| Variable | Type | Description |
|-----------|------|-------------|
| `BENT_CLUST` | Categorical | Benthic community cluster classification based on substrate composition. |
| `CLUSTER` | Categorical | Ecological cluster grouping reefs with similar structural or functional characteristics. |
| `CONNECTEDNESS` | Float | Connectivity index representing potential larval exchange or spatial linkage with other reefs. |
| `AREA` | Float | Total reef area (km² or standardized unit). |
| `HERB` | Numeric | Metric related to herbivorous fish biomass or grazing pressure. |
| `HERB2` | Numeric | Alternative or derived herbivore metric. |
| `iZONE` | Integer/Categorical | Inner ecological zone classification. |
| `sZONE` | Integer/Categorical | Shelf zone classification. |
| `PFp` | Float | Probability or proportion of a specific functional group (p-type). |
| `PFs` | Float | Probability or proportion of a specific functional group (s-type). |
| `PFt` | Float | Probability or proportion of a specific functional group (t-type). |
| `PFsum` | Float | Sum of functional group proportions (PFp + PFs + PFt). Should theoretically be ≤ 1. |



