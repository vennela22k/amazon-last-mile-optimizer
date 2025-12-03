# Amazon Last-Mile Delivery Optimizer  

<p align="center">
  <img src="https://github.com/vennela22k/amazon-last-mile-optimizer/blob/main/before.png?raw=true" width="48%"/>
  <img src="https://github.com/vennela22k/amazon-last-mile-optimizer/blob/main/after.png?raw=true" width="48%"/>
  <br>
</p> 
*Left: Unoptimized routes (40,000+ miles) — Right: Optimized with OR-Tools (under 1,600 miles)*

### Results (100 real deliveries)
| Metric                  | Before         | After          | Savings     |
|-------------------------|----------------|----------------|-------------|
| Total Distance          | 41,238 miles   | 1,592 miles    | **96.1%**   |
| Miles Saved             | -              | 39,646 miles   | -           |
| Estimated Annual Savings| -              | **~$2.4 million** | -        |

*Assumptions: $1.20/mile average cost (fuel + driver + wear), 365 days/year*

### How it works
1. Cleaned real Amazon delivery coordinates (removed GPS errors in the Atlantic Ocean)
2. Built distance matrix using `geopy`
3. Solved Vehicle Routing Problem with **Google OR-Tools** (same engine Amazon & UPS use)
4. Visualized before/after with interactive Folium + Google Maps tiles

### How I Built It
Leveraged **Grok (xAI)** to accelerate development and learn advanced OR-Tools routing algorithms in real-time. I handled data cleaning, geographic filtering, map visualization, and business impact calculations myself, AI assisted with syntax and optimization patterns, helping me deliver production-quality code 5× faster while deepening my understanding of constraint-based solvers.

### Tech Stack
- Python · Pandas · Geopy · Folium · Google OR-Tools

_____________________________________________
