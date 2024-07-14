Vehicle Cut-in detection using IDD

Steps to run the project:

1. Clone or download the repository.
2. Extract downloaded dataset and place it in the "Intel_project\data" folder.
3. While in the Intel_project folder, create a virtual environment named yolov5-env using the following command ```- python -m venv yolov5-env```
4. To activate the environment, type ```yolov5-env\Scripts\activate``` in your terminal.
5. Run the Dataset_modification.py.
6. Move to "models/yolov5" directory and use the command for training the model using ```python train.py --img 640 --batch 8 --epochs 50 --data ../idd.yaml --cfg ../yolov5n.yaml --device cuda:0 --workers 8```
7. Place your custom images in the "\Intel_project\data\own_images" folder and run the ```python detect.py --source ../../data/custom_test_images/test1.jpg --weights runs/train/exp5/weights/best.pt --conf 0.4 command```
   Results can be found at "Intel_project\models\yolov5\runs\detect" folder.
