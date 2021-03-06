# Important Shells

This repo contains some important python shells used for basic image/xml operations for custom datasets for deep learning models training.
The code is heavily borrowed from different internet sources. 

Seniors are welcomed for making correction / improvement.

## Important Note:
* It is recommended to always make a copy of your data before using any shell as a little mistake may delete your files/dataset.
* The user is resonsible for any loss/problem caused by these shells. 

## Draw bounding boxes on all images

This program is used to draw bounding boxes on all images in a folder by reading their bounding box values from xml annotations. 
Like coco formate. 

* We suppos you have images and corresponding xml annotations in two separate folder. 
* Download this shell [draw_bounding_box_on_all_images.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/draw_bounding_box_on_all_images.py)

* Now change [imagesPath](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/draw_bounding_box_on_all_images.py#L11) and [xmlPath](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/draw_bounding_box_on_all_images.py#L12) 
in the [draw_bounding_box_on_all_images.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/draw_bounding_box_on_all_images.py) file. 

* Then run using 
```
python draw_bounding_box_on_all_images.py
```
Resulted images with boudning boxes will be saved in `bbimages` folder. 

## Count number of total objects in PASCAL VOC .xml annotation files. 

This program is used to count total number of object in all xml annotations in a folder. 
For example you have coco dataset xml annotations and you want to count total number of objects
then you can use this program. 

* We suppos you have xml annotations in a folder. 
* Download this shell first [countObjects_In_XML.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/countObjects_In_XML.py)

* Nonw change [xmlPath](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/countObjects_In_XML.py#L9) in the in the shell. 
* Then run using 

```
python countObjects_In_XML.py
```
After the calculations , it will display total number of objects. 

specific_ObjectsCounter_in_xmls.py

## Count specific number of objects in PASCAL VOC .xml annotation files. 

This program is used to count total number of object as well as total number of objects for each class in all xml annotations in a folder. 
For example you have coco dataset xml annotations and you want to count how many person, car etc objects are there
then you can use this program. 

* We suppos you have xml annotations in a folder. 
* Download this shell first [specific_ObjectsCounter_in_xmls.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/specific_ObjectsCounter_in_xmls.py)

* Nonw change [xmlPath](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/specific_ObjectsCounter_in_xmls.py#L8) in the in the shell. 
* Currently I use only 7 classes, i.e person ,car , truck , bus , motobikes, bicycle and other, you can add more if conditions to calculate name. 
* Note: The name should be same as name of the objects in the xml file, otherwise it will ignore in counting. 

* Then run using 

```
python specific_ObjectsCounter_in_xmls.py
```
After the calculations , it will display total number of objects , number of objects for each class 
and total number of objects other than these classes. 

## Delete single object from all PASCAL VOC .xml annotations.

This program is used to delete a single object from all xml annotations in a folder. 
For example if xmin is > xmax , that's mean this bounding box value have some problem 
So you want to detelee this kind of all objects, or some similar conditions. 
Then you can use this program. 
* We suppos you have xml annotations in a folder. 
* Download [Delete_single_object.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Delete_single_object.py)
* Change [input](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Delete_single_object.py#L9) and [output](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Delete_single_object.py#L10) xmls path. 
* You can change conditions according to your need. 
* Then run using 
```
python Delete_single_object.py
```
The resulting edited xmls will be saved in the given folder
## Delete specific name objects from all PASCAL VOC .xml annotations.

This program is used to delete a specific objects by name from all xml annotations in a folder.
For example you want to delte all 'person' objects or all 'car' objects from all xmls in a folder

Then you can use this program. 
* We suppos you have xml annotations in a folder. 
* Download [delete_objects_in_xml_by_name.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/delete_objects_in_xml_by_name.py)
* Change [input](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/delete_objects_in_xml_by_name.py#L8) and [output](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/delete_objects_in_xml_by_name.py#L9) folder path. 
* then change object names you want to delte , Note: The name should be same according to the xml. 
* Then run using 
```
python delete_objects_in_xml_by_name.py
```
The resulting edited xmls will be saved in the given folder


## Count and delete PASCAL VOC .xml annotations that do not have objects. 

Sometimes the xml annotations do not have any objects and it create problems during taining AI model. 
So by running this program you can see/delete xmls that do not have any objects. 

* We suppos you have xml annotations in a folder. 
* Download [count&Delete_XML_Dont_Have_objects.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/count%26Delete_XML_Dont_Have_objects.py)
* Change [input path](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/count%26Delete_XML_Dont_Have_objects.py#L9)
* if you only want to print xmls names then run program without uncommenting line [30](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/count%26Delete_XML_Dont_Have_objects.py#L30) if you want also delete the file then uncomment line [30](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/count%26Delete_XML_Dont_Have_objects.py#L30)
* Note: it is recommended to first only print file names, then verify a few and then delete by uncomming line 30. 

* Then run using 
```
python count&Delete_XML_Dont_Have_objects.py
```
The resulting edited xmls will be saved in the given folder

https://github.com/MuhammadAsadJaved/Important-shells/blob/master/rename_objects_in_xml.py

## Rename objects in PASCAL VOC .xml annotations.

This program is used to rename specific objects in xml annotations. 
For example you want to rename `padestrian` to  `person` in xml annotations. 
Then you can use this program. 


* We suppos you have xml annotations in a folder. 
* Download [rename_objects_in_xml.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/rename_objects_in_xml.py)
* Change [input path](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/rename_objects_in_xml.py#L8) and [output_path](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/rename_objects_in_xml.py#L9)

* Chane names you want to rename from line [21](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/rename_objects_in_xml.py#L21) to line [29](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/rename_objects_in_xml.py#L29)

* Then run using 
```
python rename_objects_in_xml.py
```
The resulting edited xmls will be saved in the given folder

Convert_TXT_to_XML.py

## Convert .txt (Darknet) annotations to (PASCAL VOC) .xml annotations. 

This program is used to convert .txt annotations to .xml. 

* We suppos you have txt annotations and corresponding images in two separate folders. 
* Download [Convert_TXT_to_XML.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Convert_TXT_to_XML.py)
* Change [input_txt_path](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Convert_TXT_to_XML.py#L8) and [input_imgages_path](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Convert_TXT_to_XML.py#L9)

* Chane names according to labels in [18](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Convert_TXT_to_XML.py#L18) to line [27](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Convert_TXT_to_XML.py#L27). Note: The generated xmls will be according to these labes
for example the `0` from the txt  will be `person` in the xml, and so on. so use these labels according to your annotations. 

* Then run using 
```
python Convert_TXT_to_XML.py
```
The xmls will be generated in the given output folder.

## Convert .xml (PASCAL VOC) annotations to .txt (Darknet) annotations. 

This program is used to convert .xml annotations to .txt annotations. 

Step 1:

* We suppos you have xml annotations and corresponding images in separate folders according to the follwing structure.

  1) Dataset/VOCdevkit/VOC2007/Annotations/  `Place annotations in this folder`
  2) Dataset/VOCdevkit/VOC2007/JPEGImages/    `Place JPEGImages in this folder`
  3) Dataset/VOCdevkit/VOC2007/ImageSets/Main/ `Empty folder`
  
  Now first we need to create list of images names, for that
* Download [split_voc_train_test_from_imgAndAnnotations.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/2-1-split_voc_train_test_from_imgAndAnnotations.py)
* Change input_images_path on [line 15](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/2-1-split_voc_train_test_from_imgAndAnnotations.py#L15) and list destinateion_path on [line 16 and 17](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/2-1-split_voc_train_test_from_imgAndAnnotations.py#L16)
* Place split_voc_train_test_from_imgAndAnnotations.py in the `Dataset/VOCdevkit/VOC2007/` folder and run using 
```
python split_voc_train_test_from_imgAndAnnotations.py
```
It will create `train.txt` and `val.txt` in the Dataset/VOCdevkit/VOC2007/ImageSets/Main/ directory. 

Step 2:
  
* Download [Convert_xmlToTxt_voc_label.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/2-2-Convert_xmlToTxt_voc_label.py)  
* Place Convert_xmlToTxt_voc_label.py in the `Dataset/` 
* Change [classes](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/2-2-Convert_xmlToTxt_voc_label.py#L18) .
Note: The classes name should be same as in xml, only given names will be converted to .txt.
      In the .txt the labels will be according to the classes position given in L18. for example `person` will be label `0` , `car` will be `1`. You can change according to your need. 
* Then run using 
```
python Convert_xmlToTxt_voc_label.py
```
The .txt annotations will be genreated in the `Dataset/VOCdevkit/VOC2007/labels/` folder. 

## Convert .csv annotations to .txt(Darknet) annotations. 

This program is used to convert annotations from .csv file to .txt. 
It can be used for:
1) Read multiple .csv annotation files and create single .txt file. 
2) Read multiple .csv annotation files and create corresponding multiple .txt files. 
3) Read Multiple inputs from one csv file and generate one txt file containing all multiple outputs in it.
You can change code according to your need. 

* Download [Convert_csv2txt.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Convert_csv2txt.py)  
* Change [input_folder_name](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Convert_csv2txt.py#L6) .
* Then run using 
```
python Convert_csv2txt.py
```
The output .txt files be saved in the same folder with `output.txt` name. 

## Convert .mp3 audio to .pcm. 
This shell is used to convert all .mp3 audio files in a folder to .pcm format.

* Download [Convert_mp3_to_pcm.sh](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Convert_mp3_to_pcm.sh)  
* Then run this program in the same folder which contains .mp3 files. 
```
sh Convert_mp3_to_pcm.sh
```
The output .pcm audios will be saved in the same folder, then you can copy/move .pcm files to another folder. 

## Convert .jpg image to .bgr image.

This program is used to convert .jpg image .bgr.

* Download [Ruyi-convert-jpg2bgr.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Ruyi-convert-jpg2bgr.py) 
* Chnage image input and image output path at [Line 3](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Ruyi-convert-jpg2bgr.py#L3) and [Line 4](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Ruyi-convert-jpg2bgr.py#L4)
* Then run this program using
```
python Ruyi-convert-jpg2bgr.py
```
The output .bgr image will be saved in the given path.
## Convert .jpg/RGB image to .yuv image.

This program is used to convert .jpg image .bgr.

* Download [Ruyi-convert-jpg2yuv.cpp](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Ruyi-convert-jpg2yuv.cpp) 
* Chnage image input and image output path at [Line 13](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Ruyi-convert-jpg2yuv.cpp#L13)
* Then run this program using
```
use any .cpp editor to run this program. this is not a python program.
```
The output .yuv image will be saved in the given path.

## Convert .yuv image to .jpg/RGB image. 

This program is used to convert all .yuv images in a folder to RGB images.
* Download [Yuv2RGB.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Yuv2RGB.py) 
* Chnage input folder and output folder path at [Line 13](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Yuv2RGB.py#L13) and [Line 14](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Yuv2RGB.py#L14)

* Then run this program using
```
python Yuv2RGB.py
```
The output RGB images will be saved in the given path.

## Convert all .png images to .jpg images and vice versa. 

If you want to covnert all images in a folder from one extension i.e .jpg to .png or vice versa then you can use this command.
```
for i in images/*.png ; do convert "$i" "${i%.*}.jpg" ; done
```
The output will be saved in the same folder

## Rename all files in a folder.

This program is used to rename all files in a folder.

* Download [Rename_all_files_in_folder.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Rename_all_files_in_folder.py)
* Change input folder name at [Line 3](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Rename_all_files_in_folder.py#L3)
* Note: you can also change file extension according to your file extensions, the current program is for .jpg images. 
* Then run using
```
python Rename_all_files_in_folder.py
```
The files will be renamed in the same folder. 


## Rename all files in two different folders but keep the same sequence.

This program is used to rename all files in two different folders but keep the same sequence , 
For example if you want to rename images and their corresponding annotations in two different folders and keep the same sequences 
Then you can use this program. 

* Download [Rename_All_Files_And_Keep_Sequence.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Rename_All_Files_And_Keep_Sequence.py)
* Change input folders and output folders at [Line 23](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Rename_All_Files_And_Keep_Sequence.py#L23) to [Line 27](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Rename_All_Files_And_Keep_Sequence.py#L23)

* Then run using
```
python Rename_All_Files_And_Keep_Sequence.py
```
The rename images and xmls will be saved in the given output paths. 


## Combine 2 Images into 1.

This program is used to to combine all images in folder A with corresponding images in folder B.
For example image1 in folder A will be combined with image1 in the folder B.

* Download [Combine2ImagesInto1.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/Combine2ImagesInto1.py)
* Put images in two folders , i.e  A , B.

* Then run using
```
python combineAB.py  --fold_A ./A --fold_B ./B  --fold_AB ./AB
```
Output combined images will be saved in AB folder

## Copy files corresponding to files names from another input folder.

Read some files froma folder and coppy relevent files or images from another folder. </br> 
For example we want to copy images corresponding to 1.xml 2.xml 3.xml ..n.xml from a images folder which contains</br>
thousands of images. so we do not need to search corresponding images manually. 
Note: in this example it read .xml files and copy correspondig images, if you want to use for images to .xml then you </br>
can just replace .xml to .jpg and .jpg to .xml at [Line 20 and 23](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/CopyFiles_or_images.py#L20)
* Download [CopyFiles_or_images.py](https://github.com/MuhammadAsadJaved/Important-shells/blob/master/CopyFiles_or_images.py)
* Change input , output folders.
* Then run using
```
python CopyFiles_or_images.py
```
The coppied files will be saved in the `Coppied` path. 

## Check CUDA and cuDNN version in Ubuntu.
These commands are used to check cuda and cudnn version installed on your ubuntu system. 

Open a terminal with gui or by pressing `Ctrl + Alt + t`

* To check cuda version.
```
cat /usr/local/cuda/version.txt
```
It will show something like this `Cuda compilation tools, release 10.0, V10.0.130`. Here cuda version is `10.0`.
* To check cuDNN version if you installed using .tar file.
```
cat /usr/local/cuda/include/cudnn.h | grep CUDNN_MAJOR -A 2

or

cat /usr/include/cudnn.h | grep CUDNN_MAJOR -A 2
```
It will show something like this</br>
`#define CUDNN_MAJOR 7`</br>
`#define CUDNN_MINOR 4`</br>
`#define CUDNN_PATCHLEVEL 1`</br>
Here your cuDNN version is 7.4.1

* Note: if you are using cuDNN >=8 , they have changed version information in the separate file. so you can check with 
```
cat /usr/local/cuda/include/cudnn_version.h | grep CUDNN_MAJOR -A 2
```
* To check cuDNN version if you installed using .deb file.

```
cat /usr/include/cudnn_version.h | grep CUDNN_MAJOR -A 2
```
## Install cuda , cudnnn and caffe in Ubuntu. 

* These two links </br>

https://github.com/yixindu1573/Caffe-Installation-Ubuntu-16.04-cuda-9.0-cudnn-v7

or 

https://github.com/IraAI/caffe-gpu-installation

http://installing-caffe-the-right-way.wikidot.com/start

## Compile OpenCV in Ubuntu 16.04

https://note.youdao.com/ynoteshare1/index.html?id=0626a4c9f331f1a70e85f355ce410824&type=note
