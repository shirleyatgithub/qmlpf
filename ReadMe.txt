unzip the train and test.zip
cd MLPTrainScripts
one needs to modify the dataset path in qtrain.py and qtest.py
trainfilepath = 'D://qmlpfpys-s//2xTrainingDataDND21train//'
testfilepath = 'D://qmlpfpys-s//2xTrainingDataDND21test//'

python qtrain.py 0 4
-first parameter 0/1, 0 means quantized training, 1 means float training.
-second parameter, 4 means quantized bits for inputs and activations before the last layer. the last layer have 16 bits.
-key code in function qbuildModel

python qtest.py hotel 4
-first parameter hotel/dri, hotel means using hotel dataset, dri means using driving dataset.
-second parameter, 4 means quantized bits.
