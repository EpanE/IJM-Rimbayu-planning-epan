For a high-stakes, township-wide anti-theft project involving 31 street-pole CCTV cameras across a targeted zone in [IJM Rimbayu](https://www.google.com/search?kgmid=/g/11npjdp4fn), relying on standard 2.4 GHz mesh to carry all that video back to a central server will cause the system to crash.
With 31 cameras streaming continuously, you are dealing with a serious data aggregation problem. If each camera is a standard 4MP/1080p smart surveillance unit utilizing modern H.265 compression, it will pull roughly 3 to 4 Mbps of continuous upload bandwidth. For 31 cameras, your network core must reliably sustain a baseline upload throughput of 93 Mbps to 124 Mbps 24/7. If you upgrade to 4K cameras for license plate recognition, that requirement spikes to 250+ Mbps.
Because the data compounds as it travels down the street light poles, you need a resilient, enterprise-grade architecture.
To successfully cover the roads without running miles of expensive fiber-optic cables down every single curb, you should deploy a Point-to-Multipoint (PtMP) wireless topology combined with localized 2.4 GHz/5 GHz client access.

* 
* The Camera Connections (The Access Layer):
Each of your 31 cameras connects to a pole-mounted industrial wireless node. If the camera is hardwired via an Ethernet cable directly down the pole into the node, you bypass 2.4 GHz interference entirely. If some cameras must be wireless (e.g., viewing a blind spot across the street), use 5 GHz Wi-Fi for the camera-to-pole connection to keep the highly congested 2.4 GHz band free.
* The Sector Hubs (The Aggregation Layer):
Instead of daisy-chaining 31 poles in a straight line (which causes massive latency and total failure if one pole loses power), divide the 31 cameras into 3 or 4 geographic clusters. At the center of each cluster, install a high-capacity 90-degree or 120-degree Sector Base Station Antenna on a dominant master pole.
* The Invisible Backbone (The Backhaul Layer):
Each individual street light pole will feature a small, highly directional client dish pointing directly back to its designated cluster Sector Hub using a clean, non-Wi-Fi proprietary frequency like 5 GHz airMAX / LTU or 60 GHz millimeter-wave (such as Ubiquiti UISP hardware). The Sector Hubs then beam the combined data directly back to your central guardhouse or command center.
* 

Since this project targets theft prevention along public township roads, standard security cameras are not enough. The network must be engineered to support the specific demands of crime prevention:

* 
* Zero-Packet-Loss for LPR: To catch thieves or tracing getaway vehicles, you will likely deploy License Plate Recognition (LPR) cameras at key entry/exit road bottlenecks. LPR software requires crystal-clear, uncompressed snapshots. If your wireless network suffers from 2.4 GHz interference or packet drops, the license plates will blur. This makes a dedicated, clean wireless backhaul mandatory.
* Edge Storage Safeguards: If a thief deliberately cuts power to a street light circuit or tampers with a master node, you cannot afford to lose footage. Ensure all 31 cameras are equipped with high-end, endurance-rated MicroSD cards configured for Edge Recording / Automatic Network Replenishment (ANR). If the wireless link drops, the camera records locally and automatically uploads the missing video to the central recorder once the network heals.
* 

Before approving hardware procurement, ensure your engineering team verifies these three critical township constraints:

   1. Continuous Power Authorization: You must secure approval from the local council or IJM Rimbayu’s master developer to tap into the street light mains before the photocell switch. The network nodes and cameras require unswitched 240V power so they do not shut off during the day when the street lights turn off.
   2. Pole Load and Wind Logistics: Hanging a dome camera, a wireless backhaul dish, and a weatherproof industrial enclosure box creates significant wind resistance. Ensure the chosen street light poles are structurally rated to handle the weight and wind load during heavy Malaysian monsoon storms.
   3. The Greenery Obstacle: IJM Rimbayu is famous for its lush, eco-friendly landscaping. A tree branch directly blocking the line of sight between two network poles can degrade a high-frequency wireless signal by up to 80%. Your master poles and sector antennas must be mounted higher than the mature tree canopy line, or positioned carefully to shoot down clear road corridors.

To help select the specific enterprise wireless hardware models, do you know the maximum distance (in meters or kilometers) from the furthest street light pole back to the central guardhouse? Also, are the roads mostly straight lines, or do they involve heavy curves and roundabouts?

