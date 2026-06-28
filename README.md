<h2>TensorFlow-FlexUNet-Image-Segmentation-Foveal-Avascular-Zone (2025/06/28)</h2>

This is the first experiment of Image Segmentation for Foveal-Avascular-Zone (FAZ)
 based on 
our <a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model">TensorFlow FlexUNet Model</a>
 (<b>TensorFlow Flexible UNet Image Segmentation Model for Multiclass</b>) and a 512x512 pixels PNG
 <a href="https://drive.google.com/file/d/1Q3Ds-EvpiTWQCExFzcY3DE-kciSLswX1/view?usp=sharing">
Foveal-Avascular-Zone-ImageMask-Dataset.zip</a> with colorized masks 
(<a href="https://creativecommons.org/licenses/by/4.0/legalcode">Creative Commons Attribution 4.0 International</a>
), which was derived by us from:<br><br>
<a href="https://zenodo.org/records/5075194">
<b>OCTA imsges dataset with pixel-level mask annotaion for FAZ segmentation</b></a>
<br><br>
<hr>
<b>Actual Image Segmentation for Foveal-Avascular-Zone Images of 512x512 pixels</b><br>
As shown below, the inferred masks look similar to the ground truth masks. <br><br>
<b>class_color_map = {Deep:yellow, Superficial:mazenta} </b>.<br>
<br>
<table>
<tr>
<th>Input: image</th>
<th>Mask (ground_truth)</th>
<th>Prediction: inferred_mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/images/deep_66.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/masks/deep_66.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test_output/deep_66.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/images/superficial_26.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/masks/superficial_26.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test_output/superficial_26.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/images/superficial_279.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/masks/superficial_279.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test_output/superficial_279.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>1. Dataset Citation</h3>
The dataset used here was derived from:<br><br> 
<a href="https://zenodo.org/records/5075194">
<b>OCTA imsges dataset with pixel-level mask annotaion for FAZ segmentation</b></a>
<br><br>
The following explanation was taken from the above web site.<br><br>
This dataset is the affiliated data for the reaserch "A Deep Learning-based Quality 
Assessment and Segmentation System and A Large Benchmark Datatset for Optical Coherence Tomographic Angiography Image"
<br><br>
<b>Detail</b><br>
This dataset is the pixel-level mask annotaion for FAZ segmentation. 1,101 3 × 3 mm2 sOCTA images chosen from gradable and best OCTA images randomly in 
subset sOCTA-3x3-10k, and 1,143 3 × 3 mm2dOCTA images were annotated by an experienced ophthalmologist.
<br>
<br>
<b>Citation</b><br>
Yufei Wang, Yiqing Shen, Meng Yuan, Jing Xu, Wei Wang, & Weijing Cheng. (2021).<br>
OCTA imsges dataset with pixel-level mask annotaion for FAZ segmentation (1.0)<br>
[Data set]. Zenodo. https://doi.org/10.5281/zenodo.5075194
<br><br>
<b>License</b><br>
<a href="https://creativecommons.org/licenses/by/4.0/legalcode">Creative Commons Attribution 4.0 International</a>
<br><br>
<h3>
2 Foveal-Avascular-Zone-Images ImageMask Dataset
</h3>
 If you would like to train this Foveal-Avascular-Zone-Images Segmentation model by yourself,
 please download the dataset from the google drive  
 <a href="https://drive.google.com/file/d/1Q3Ds-EvpiTWQCExFzcY3DE-kciSLswX1/view?usp=sharing">
Foveal-Avascular-Zone-ImageMask-Dataset.zip</a> with colorized masks 
(<a href="https://creativecommons.org/licenses/by/4.0/legalcode">Creative Commons Attribution 4.0 International</a>
)
, expand the downloaded ImageMaskDataset and put it under <b>./dataset</b> folder to be
<br>
<pre>
./dataset
└─Foveal-Avascular-Zone
    ├─test
    │   ├─images
    │   └─masks
    ├─train
    │   ├─images
    │   └─masks
    └─valid
        ├─images
        └─masks
</pre>
<br>
<b>Foveal-Avascular-Zone-Images Statistics</b><br>
<img src ="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/Foveal-Avascular-Zone_Statistics.png" width="512" height="auto"><br>
<br>
As shown above, the number of images of train and valid datasets is not so large to use for the
 training set of our segmentation model.
<br>
<br>
<b>Train_images_sample</b><br>
<img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/asset/train_images_sample.png" width="1024" height="auto">
<br>
<b>Train_masks_sample</b><br>
<img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/asset/train_masks_sample.png" width="1024" height="auto">
<br>

<h3>
3 Train TensorFlowFlexUNet Model
</h3>
 We trained Foveal-Avascular-Zone-Images TensorFlowFlexUNet Model by using the following
<a href="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/train_eval_infer.config"> <b>train_eval_infer.config</b></a> file. <br>
Please move to ./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone-Images and run the following bat file.<br>
<pre>
>1.train.bat
</pre>
, which simply runs the following command.<br>
<pre>
>python ../../../src/TensorFlowFlexUNetTrainer.py ./train_eval_infer.config
</pre>
<hr>

<b>Model parameters</b><br>
Defined a small <b>base_filters=16 </b> and large <b>base_kernels=(11,11)</b> for the first Conv Layer of Encoder Block of 
<a href="./src/TensorFlowFlexUNet.py">TensorFlowFlexUNet.py</a> 
and a large <b>num_layers=8</b> (including a bridge between Encoder and Decoder Blocks).
<pre>
[model]
;You may specify your own UNet class derived from our TensorFlowFlexModel
model         = "TensorFlowFlexUNet"
generator     =  False
image_width    = 512
image_height   = 512
image_channels = 3
input_normalize = True
normalization  = False
num_classes    = 3
base_filters   = 16
base_kernels   = (11,11)
num_layers     = 8
dropout_rate   = 0.04
dilation       = (1,1)
</pre>
<b>Learning rate</b><br>
Defined a small learning rate.  
<pre>
[model]
learning_rate  = 0.00007
</pre>
<b>Loss and metrics functions</b><br>
Specified "categorical_crossentropy" and <a href="./src/dice_coef_multiclass.py">"dice_coef_multiclass"</a>.<br>
<pre>
[model]
loss           = "categorical_crossentropy"
metrics        = ["dice_coef_multiclass"]
</pre>
<b>Dataset class</b><br>
Specifed <a href="./src/ImageCategorizedMaskDataset.py">ImageCategorizedMaskDataset</a> class.<br>
<pre>
[dataset]
class_name    = "ImageCategorizedMaskDataset"
</pre>
<br>
<b>Learning rate reducer callback</b><br>
Enabled learing_rate_reducer callback, and a small reducer_patience.
<pre> 
[train]
learning_rate_reducer = True
reducer_factor     = 0.4
reducer_patience   = 4
</pre>
<b>Early stopping callback</b><br>
Enabled early stopping callback with patience parameter.
<pre>
[train]
patience      = 10
</pre>

<b>RGB Color map</b><br>
Specifed rgb color map dict for Foveal-Avascular-Zone-Images 3 classes.<br>
<pre>
[mask]
mask_datatype= "categorized"
mask_file_format = ".png"
mask_datatyoe    = "categorized"
;Foveal-Avascular-Zone-Images rgb color map dict for 1+2 classes.
;                    Deep:yellow, Superficial:mazenta 
rgb_map = {(0,0,0):0,(255,255,0):1,(255,0,255):2}
</pre>

<b>Epoch change inference callback</b><br>
Enabled <a href="./src/EpochChangeInferencer.py">epoch_change_infer callback</a></b>.<br>
<pre>
[train]
epoch_change_infer       = True
epoch_change_infer_dir   =  "./epoch_change_infer"
num_infer_images         = 6
</pre>

By using this callback, on every epoch_change, the inference procedure can be called
 for 6 images in <b>mini_test</b> folder. This will help you confirm how the predicted mask changes 
 at each epoch during your training process.<br> 
<br> 
As shown below, early in the model training, the predicted masks from our UNet segmentation model showed 
discouraging results.
 However, as training progressed through the epochs, the predictions gradually improved. 
 <br> 
<br>
<b>Epoch_change_inference output at starting (epoch 1,2,3)</b><br>
<img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/asset/epoch_change_infer_at_start.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at middlepoint (epoch 16,17,18)</b><br>
<img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/asset/epoch_change_infer_at_middle.png" width="1024" height="auto"><br>
<br>
<b>Epoch_change_inference output at ending (epoch 34,35,36)</b><br>
<img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/asset/epoch_change_infer_at_end.png" width="1024" height="auto"><br>
<br>

In this experiment, the training process was stopped at epoch 36 by EarlyStopping callback.<br><br>
<img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/asset/train_console_output_at_epoch36.png" width="920" height="auto"><br>
<br>

<a href="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/eval/train_metrics.csv">train_metrics.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/eval/train_metrics.png" width="520" height="auto"><br>

<br>
<a href="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/eval/train_losses.csv">train_losses.csv</a><br>
<img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/eval/train_losses.png" width="520" height="auto"><br>

<br>

<h3>
4 Evaluation
</h3>
Please move to <b>./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone-Images</b> folder,<br>
and run the following bat file to evaluate TensorFlowUNet model for Foveal-Avascular-Zone-Images.<br>
<pre>
./2.evaluate.bat
</pre>
This bat file simply runs the following command.
<pre>
python ../../../src/TensorFlowFlexUNetEvaluator.py ./train_eval_infer_aug.config
</pre>

Evaluation console output:<br>
<img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/asset/evaluate_console_output_at_epoch36.png" width="920" height="auto">
<br><br>Image-Segmentation-Foveal-Avascular-Zone-Images

<a href="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/evaluation.csv">evaluation.csv</a><br>
The loss (categorical_crossentropy) to this Foveal-Avascular-Zone-Images/test was low, and dice_coef_multiclass 
was high as shown below.
<br>
<pre>
categorical_crossentropy,0.0142
dice_coef_multiclass,0.9929
</pre>
<br>

<h3>
5 Inference
</h3>
Please move to a <b>./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone-Images</b> folder<br>
,and run the following bat file to infer segmentation regions for images by the Trained-TensorFlowUNet model for Foveal-Avascular-Zone-Images.<br>
<pre>
./3.infer.bat
</pre>
This simply runs the following command.
<pre>
python ../../../src/TensorFlowFlexUNetInferencer.py ./train_eval_infer_aug.config
</pre>
<hr>
<b>mini_test_images</b><br>
<img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/asset/mini_test_images.png" width="1024" height="auto"><br>
<b>mini_test_mask(ground_truth)</b><br>
<img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/asset/mini_test_masks.png" width="1024" height="auto"><br>

<hr>
<b>Inferred test masks</b><br>
<img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/asset/mini_test_output.png" width="1024" height="auto"><br>
<br>
<hr>
<b>Enlarged images and masks of Foveal-Avascular-Zone Images of 512x512 pixels</b><br><br>
<b>class_color_map = {Deep:yellow, Superficial:mazenta} </b>.<br><br>
<table>
<tr>
<th>Image</th>
<th>Mask (ground_truth)</th>
<th>Inferred-mask</th>
</tr>
<tr>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/images/deep_82.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/masks/deep_82.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test_output/deep_82.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/images/deep_432.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/masks/deep_432.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test_output/deep_432.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/images/deep_1005.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/masks/deep_1005.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test_output/deep_1005.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/images/superficial_271.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/masks/superficial_271.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test_output/superficial_271.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/images/superficial_279.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/masks/superficial_279.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test_output/superficial_279.png" width="320" height="auto"></td>
</tr>

<tr>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/images/superficial_941.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test/masks/superficial_941.png" width="320" height="auto"></td>
<td><img src="./projects/TensorFlowFlexUNet/Foveal-Avascular-Zone/mini_test_output/superficial_941.png" width="320" height="auto"></td>
</tr>
</table>
<hr>
<br>
<h3>
References
</h3>
<b>1. Application of Improved U-Net Convolutional Neural Network 
for Automatic Quantification of the Foveal Avascular Zone in Diabetic Macular Ischemia</b><br>
Yongan Meng, Hailei Lan, Yuqian Hu, Zailiang Chen, Pingbo Ouyang, Jing Luo<br>
<a href="https://pmc.ncbi.nlm.nih.gov/articles/PMC8898103/">https://pmc.ncbi.nlm.nih.gov/articles/PMC8898103/</a>
<br><br>
<b>2. TensorFlow-FlexUNet-Image-Segmentation-Model</b><br>
Toshiyuki Arai @antillia.com<br>
<a href="https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model">
https://github.com/sarah-antillia/TensorFlow-FlexUNet-Image-Segmentation-Model</a>
<br>
<br>
