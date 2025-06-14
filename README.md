![image](https://github.com/user-attachments/assets/d4c36444-1662-4b7b-86c2-df2f69ed0b36)




# Soccer Cross-Camera Player Mapping

This project performs player detection, tracking, and cross-camera player ID mapping between two soccer videos (broadcast and tacticam) using a YOLO-based model and spatial matching.

Videos link : https://drive.google.com/drive/folders/1Agv-a7yv6GLwsD5bzI8_D-R98FxtG658?usp=drive_link
Model link  : https://drive.google.com/file/d/1BccOHbeJbkN8Z4SvTSztdFG9uUdK3sYY/view?usp=sharing

## Folder Structure & Setup

Your Google Drive should look like this:

SoccerAssignment/
├── models/
│   └── best.pt
├── videos/
│   ├── broadcast.mp4
│   └── tacticam.mp4
├── outputs/
│   ├── broadcast_tracks.csv
│   ├── tacticam_tracks.csv
│   └── mapping.csv
├── soccer_notebook.ipynb


**Instructions:**
- Mount your Google Drive at the start of the notebook.
- Set the working directory to `/content/drive/My Drive/SoccerAssignment`.
- Place all files in the folders as shown above.



## How to Run

1. Install Dependencies
    - Python 3.8+
    - Install required packages:
        ```
        pip install ultralytics opencv-python pandas matplotlib
        ```

2. Prepare Files
    Create a folder named `SoccerAssignment` in your Google Drive.
    Place your YOLO model in `/models/best.pt`
    Place videos in `/videos/broadcast.mp4` and `/videos/tacticam.mp4` 
    Create `/outputs/` folder for results

3. Run the Notebook
    - Open `Soccer_notebook.ipynb` in Google Colab or Jupyter
    - Run all cells in order
    - Outputs (CSVs, visualizations) will be saved in `/outputs/`

## Notes

- Only the last 5 seconds of the tacticam video are mapped to the 5-second broadcast video.
- "Unmatched" labels mean the player was not visible or not confidently matched in both views.
- The mapping uses a spatial distance threshold for robust matching.




