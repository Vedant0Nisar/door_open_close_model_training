# Automatic-Number-Plate-Recognition-YOLOv8
## Demo


https://github.com/Muhammad-Zeerak-Khan/Automatic-License-Plate-Recognition-using-YOLOv8/assets/79400407/1af57131-3ada-470a-b798-95fff00254e6



## Data

The video used in the tutorial can be downloaded [here](https://drive.google.com/file/d/1JbwLyqpFCXmftaJY1oap8Sa6KfjoWJta/view?usp=sharing).

## Model

A Yolov8 pre-trained model (YOLOv8n) was used to detect vehicles.

A licensed plate detector was used to detect license plates. The model was trained with Yolov8 using [this dataset](https://universe.roboflow.com/roboflow-universe-projects/license-plate-recognition-rxg4e/dataset/4). 
- The model is available [here](https://drive.google.com/file/d/1Zmf5ynaTFhmln2z7Qvv-tgjkWQYQ9Zdw/view?usp=sharing).

## Dependencies

The sort module needs to be downloaded from [this repository](https://github.com/abewley/sort).

```bash
git clone https://github.com/abewley/sort
```

## Project Setup

* Make an environment with python=3.10 using the following command 
``` bash
conda create --prefix ./env python==3.10 -y
```
* Activate the environment
``` bash
source activate ./env
``` 

* Install the project dependencies using the following command 
```bash
pip install -r requirements.txt
```
* Run main.py with the sample video file to generate the test.csv file 
``` python
python main.py
```
* Run the add_missing_data.py file for interpolation of values to match up for the missing frames and smooth output.
```python
python add_missing_data.py
```

* Finally run the visualize.py passing in the interpolated csv files and hence obtaining a smooth output for license plate detection.
```python
python visualize.py
```

## Real-time / Live visualization

You can run detections and see results in real-time (webcam or a video file) with the included `run_live.py` script.

Examples:

- Run from the default webcam (first camera):

```powershell
python run_live.py --source 0
```

- Run from the sample video file `sample.mp4`:

```powershell
python run_live.py --source sample.mp4
```

Controls:
- Press `q` in the display window to quit.

Notes:
- The script uses the same models in the repository: `yolov8n.pt` and `license_plate_detector.pt`. Make sure both files are present.
- For GPU use, change the `device` argument to the GPU id (for example `--device 0`) and ensure the ultralytics/torch setup supports it.
"# door_open_close_model_training" 
