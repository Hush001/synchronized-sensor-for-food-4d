

# Food-4D: A Spatiotemporal Multimodal Dataset for Dynamic Food Processing Analysis

**Food-4D** is a spatiotemporal four-dimensional multimodal dataset designed to analyze dynamic food preparation processes. unlike traditional static food datasets, Food-4D captures the continuous morphological changes of food (e.g., cutting, peeling, plating) and the synchronous human operational behaviors involved in making homemade bentos.

This dataset serves as a benchmark for automated dietary assessment, food processing analysis, and cross-modal representation learning, enabling precise evaluations of food volume, mass, and nutrition.

## 📅 Dataset Overview

Food-4D systematically records the preparation processes of **20 types of homemade bento** from both first-person and third-person perspectives.



* 
**Objects:** 23 common food ingredients and 4 kitchen tools.


* 
**Scenarios:** Real-life home kitchen simulation with dynamic environmental characteristics.


* 
**Data Scale:** 20 complete construction tasks, fully annotated with dense semantic and measurement labels.


* 
**Annotations:** High-precision measurements of food volume (mL) and mass (g), alongside ingredient attributes.



## 📡 Multimodal Sensor Setup

We collected synchronized data across **6 modalities** using a multi-process parallel system. The data collection platform covers:

1. **Global Vision (RGB-D):**
* **Azure Kinect DK:** Top-down view capturing RGB, Depth, and Point Cloud data.
* **Intel RealSense D405:** Close-range view focused on hand-centric operations.


2. **Ego-Centric Vision & Eye Tracking:**
* **Tobii Pro Glasses 3:** First-person RGB stream and gaze fixation hotspots (attention data).


3. **Hand Motion & Tactile:**
* **WISEGLOVE:** Captures 19-DoF finger joint angles and tactile force feedback.


4. **Physiological Signals:**
* **DELSYS EMG:** Surface electromyography signals to record muscle usage and coordination.



## 📂 Data Structure

The dataset is organized by task index (`n1` to `n20`) and divided into three processing stages:

* **Stage 1 (Making):** Dynamic recording of the cutting, peeling, and arranging process. Contains synchronized raw data streams (RGB, Depth, EMG, Glove, Tobii).


* 
**Stage 2 (Modeling):** 3D scanning of the finished bento using a depth camera trajectory covering a 40cm hemisphere.


* **Stage 3 (Measuring):** Ground truth recording. Contains `.xlsx` files with precise mass and volume measurements for every ingredient.



## 🛠️ Code & Acquisition

This repository provides the Python code used for the **synchronized multimodal sensor acquisition** during the experiment.

* 
**Synchronization:** The code handles timestamp alignment across all 6 sensors.


* 
**Device Drivers:** Includes acquisition scripts for Azure Kinect, RealSense, Tobii, WISEGLOVE, and DELSYS EMG.


* 
**Data Processing:** `.bat` scripts and Python tools are provided to extract RGB frames and Depth maps from the recorded MKV files.



**Repository Link:** [https://github.com/Hush001/synchronized-sensor-for-food-4d](https://github.com/Hush001/synchronized-sensor-for-food-4d) 

## 📝 Citation

If you use the Food-4D dataset or code in your research, please cite our paper:

```bibtex
@article{jiang2024food4d,
  title={Food-4D: A Spatiotemporal Multimodal Dataset for Dynamic Food Processing Analysis},
  author={Jiang, Shuo and Li, Zihan and Lu, Yuxi and Qiu, Jianing and Lo, Frank P.-W. and Su, Xiu and He, Bin},
  journal={IEEE Transactions on Multimedia (Submitted)},
  year={2025}
}

```

---

Based on the manuscript: "Food-4D: A Spatiotemporal Multimodal Dataset for Dynamic Food Processing Analysis"