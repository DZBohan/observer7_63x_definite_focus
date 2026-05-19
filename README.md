# Observer 7 (63x with Definite Focus) User Guide

**Location:** Furth Building, Room F1114, City of Hope

---

## 1. Start Reservation and Power On

1. Log in to **iLab COH**, navigate to the **Kiosk**, and click **Start** to begin billing. Note: billing must be started within 30 minutes of the reservation start time, otherwise the reservation will be automatically cancelled.
2. Power on the microscope and launch **ZEN pro** software. If the software displays "**Broken Camera x**", close the software, restart the microscope, and relaunch ZEN pro. This usually resolves the issue.

---

## 2. Add Tiles

1. After opening the software, switch the light path to the **eyepiece** by clicking the eyepiece icon at the bottom of the flowchart, so that the image can be observed through the oculars. Start with the **10x objective**.
2. Go to **Acquisition** and select the experiment **"63x-oil-tile"**. Only the following 4 channels are used in this experiment:
   - **AF555** (red)
   - **AFlgG** (green)
   - **DAPI** (blue)
   - **Bright** (brightfield)
3. Open the **Tiles** panel and click the **Show Viewer** button to bring up the tile setup view. Delete the existing tile region and create a new **10 × 10** tile region.
4. Set the channel to **Bright** and click **Live**. The real-time image will appear within the blue capture frame.
5. Use the joystick to navigate the capture frame to the edges of the ROI, then align the tile region with the ROI.
6. Once aligned, rotate the objective turret to the side position and apply oil to the **63x objective**.
   - **Do not remove the slide** when applying oil, otherwise the alignment will need to be redone.
   - Apply **1 drop** of oil — avoid using too much.
7. Switch to the **63x objective**. Use the joystick to make small XY movements so that the oil spreads evenly between the objective and the coverslip, avoiding bubbles.
8. Re-apply oil and repeat the spreading step to ensure sufficient oil coverage. If bubbles appear, wipe the lens with lens paper and reapply.

---

## 3. Focus and Exposure

1. Switch from **Acquisition** to **Locate** (eyepiece mode), select **DAPI** (blue), and observe through the eyepieces. Move to the interior of the ROI and manually focus on the nuclei.
2. Switch back to **Acquisition**. Use the **joystick** to manually navigate to different tile positions across the ROI to check and adjust exposure.

   **Goal:** find an exposure value such that the strongest-signal tiles in the ROI are not overexposed. Sample a few tiles with the brightest signal as the reference, not purely random positions, to avoid missing hotspots.

3. Procedure for each channel (e.g., red):
   1. Click **Live** and select the channel.
   2. Click **Set Exposure** to auto-set the exposure.
   3. Check for overexposure using **both** methods:
      - **Histogram**: inspect the intensity curve.
      - **Range Indicator**: turn it on — overexposed pixels appear **red**, underexposed pixels appear **blue**. This is the most direct way to spot overexposure.
   4. If overexposure is detected, manually set a lower exposure value. Aim for the histogram peak to sit around **70–80%** of the maximum, leaving some headroom.
   5. Close Live, navigate to another tile, and repeat. After checking several tiles, record the final exposure value for that channel.
4. Repeat the procedure for each remaining channel (green, blue, brightfield), recording the final exposure value for each.

---

## 4. Definite Focus

1. Go to the **Focus Strategy** section.
2. Select **"Combine Software Autofocus and Definite Focus"**.
3. Select **"Software Autofocus as Reference for Definite Focus"** and set **DAPI (blue)** as the reference channel.
   - DAPI is used as the reference because its signal is strong, stable, and slow to bleach, making it well suited for focus reference.
4. Select **"Repeat Every 1 tile"** and **uncheck** **"Definite Focus Every 1 tile"**.
5. No changes are needed under the **Software Autofocus** menu.

---

## 5. Acquisition

1. Before starting, make sure **Auto Save** is checked.
2. Move the tile capture frame to the **top-left corner of the ROI** (the starting tile).
3. Click **Live** and manually focus on the starting tile.
4. Right-click on the tile region and select **"Set current Z for selected tile region"** to manually set the Z reference for the starting point.
5. **Estimate acquisition time** before starting. For a 10 × 10 tile region with 4 channels:

   `Total time ≈ 100 tiles × 4 channels × (exposure time per channel) + autofocus time per tile`

   Confirm this fits within the remaining reservation time.
6. Click **Start Experiment** to begin acquisition.
7. During acquisition, monitor exposure and focus periodically to catch issues early.

---

## Notes

- Channel name **"AFlgG"** is recorded as it appears in the experiment configuration. This may correspond to an Alexa Fluor secondary antibody channel (possibly AF488); verify when convenient.
