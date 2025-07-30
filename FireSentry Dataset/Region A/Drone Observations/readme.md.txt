# Drone Video Modalities

## Infrared Video
> Location: `./Infrared video`

### Key Characteristics
- **Temporal Processing**:  
  Videos are temporally downsampled with a **5-second interval** between consecutive frames to clearly visualize wildfire progression dynamics.
  
- **Advantages over Visible Light**:
  - Resistant to smoke occlusion
  - Unaffected by vegetation cover interference
  - Provides clear thermal signatures of active fire fronts
  - Effective for night operations and low-visibility conditions

### Scientific Value
Infrared imaging captures critical thermal dynamics that are essential for:
1. Accurate fire intensity mapping
2. Subsurface fire detection
3. Heat flux quantification
4. Burn severity assessment

---

## Visible Light Video
> Location: `./Visible light video`

### Key Characteristics
- **Native Frame Rate**:  
  Maintains original temporal resolution with **1/30-second interval** between consecutive frames.
  
- **Complementary Information**:
  - Visual documentation of smoke plume diffusion
  - Detailed vegetation status monitoring
  - Terrain feature visualization
  - Fire-atmosphere interaction patterns
  - Flame color and structure analysis

### Scientific Value
RGB imaging provides unique visual context crucial for:
1. Smoke dispersion modeling
2. Fuel moisture estimation
3. Firebrand spotting analysis
4. Topographic influence studies
5. Fire behavior documentation

---

## Comparative Analysis
| Feature | Infrared Video | Visible Light Video |
|---------|----------------|---------------------|
| **Frame Interval** | 5 seconds | 1/30 second |
| **Smoke Penetration** | Excellent | Limited |
| **Vegetation Occlusion** | Minimal | Significant |
| **Night Operation** | Effective | Ineffective |
| **Flame Structure** | Thermal profile only | Visual details |
| **Smoke Analysis** | Indirect heat signature | Direct visualization |
| **Primary Use Case** | Fire front tracking | Environmental impact assessment |

> **Technical Note**: The temporal downsampling in infrared videos is applied **only** for visualization enhancement. Raw high-frequency thermal data is available upon request for research purposes.