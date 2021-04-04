# Project ANNsWTF
<h1>Final Project Artistic Style Transfer </h1>

<p  align="justify">This is a Tensorflow implementation of Artistic Style Transfer mainly based on Gaty et. al. <a href="https://arxiv.org/abs/1508.06576"> paper </a>(For further datails regarding the sources used please refer to the report that accompanies this project)

Our algorithm synthesizes the style of an image S and the content of an image C into a new image G. </p>




<h3> Setup</h3>
<div>
 
The development and testing of the algorithm was done in Colab.
 
<ol>
 <li> Open the noteboook MasterANNsWTF.ipynb in Colab. </li>
 <li>Create a folder in your Google Drive named ANNs StyleTransfer.</li>
 <li>Save the source images to the folder created in step 2. The images can be found <a href="https://github.com/yesidc/ProjectANNsWTF/tree/main/source_img"> here </a></li>
 <li> Run the notebook and mount your Google Drive when asked to do so. </li>
</ol>
</div>


<h3>Running the Model:</h3>

<p  align="justify">You can either run MasterANNsWTF.ipynb with the default parameters or you can customize it as you wish 
in order to conduct your own experiments. </p>


<h4>Conducting your own Experiments: </h4>
<ol>
         <li> Go to the section 'Where stuff happens'. </li>
         <li>Either uncomment any of the already set up experiments or set up a new one by creating a Python list like so: </li>
</ol>
runList=[

         runConfig(1,optimizer= desired optimizer(learning_rate= desired learning rate, beta_1=desired beta value, epsilon=desired epsilon value)),
         runConfig(2, style_weight = desired value, content_weight= desired cotent weight value),
      
]

<p  align="justify">In example above we set up two experiments. The first one, identified with id = 1, sets a desired optimizer, learning rate, beta and epsison values. 
In the second experiment with id = 2, we modified the value of the style weight and content weight to the values we wanted to try out. 
Besides the parameters exemplified above, the following can also be modified: </p>

<ul>
         <li>number </li>

<li> initImageMode </li>

<li> img_content_name </li>

<li> img_style_name </li>

<li> imgwidth </li>

<li> color_preservation_method </li>

<li> content_weight </li>

<li> style_weight </li>

<li> style_layer_weights_modifiers </li>

<li> optimizer </li>
</ul>                

<p align= "justify"> All of the above are attributes of the class runConfig(). To have a better understing as to what value each attribute
takes, we suggest taking a look at the comments that go with their definitions. This can be found in the section
'A helper class to enable parallel trainings' of the notebook MasterANNsWTF.ipynb</p>

<h3>Images </h3>
<p align= "justify"> Inside the folder Images there are four directories that contain the the images obtained after having trained the
model with specific set of parameters. In what follows we detail the content of each of them.</p>
<ul>
 <li><p align= "justify"> <h4>color_preservation:</h4> <ul><li><strong>gatys_no_color</strong>: an example of style image S' obtained using Gaty's et al. color preservation method </li>
  <li><strong>yuv_no_color</strong>: an example of style image S' obtained using YUV method</li>
  <li><strong>generated_40_LR=0.01_1000epo_512_color_pres_method_PAPER</strong>: Image generated using Gaty's et al. color preservation method, learning rate 0.01
   and 1000 epochs</li><li> <strong>generated_41_LR=0.01_1000epo_512_color_pres_method_YUV_FUNCT</strong>: Image generated using YUV method, learning rate 0.01 and
  1000 epochs</li></ul></li>
 <li><h4>content_layer_modifications</h4><ul>
  <li><strong>block3_conv1_5000:</strong> Image obtained after 5000 and epoches and switching content layer to block3_conv1. </li>
  <li><strong>block5_conv4_5000: </strong>Image obtained after 5000 and epoches switching content layer to block5_conv4.</li>
  <li><strong>block_4_conv2: </strong>Image obtained after 5000 epoches and switching content layer to block4_conv2.</li>
  <li><strong>block_5_conv3_5000: </strong>Image obtained after 5000 epoches and switching content layer to block5_conv3.</li></ul></li>
 <li><h4>style_layers_modifications:</h4>
  <ul><li><strong>style_two_more_layers_5000: </strong>Image obtained after 5000 epochs and a total of 7 style layers.</li>
   <li><strong>style_three_more_layers_5000: </strong>Image obtained after 5000 epochs and a total of 8 style layers.</li>
   <li><strong>style_sub_2__last_layers_5000: </strong>Image obtained after 5000 epochs and a total of 3 style layers.</li>
   <li><strong>style_sub_2__first_layers_5000: </strong>Image obtained after 5000 epochs and a total of 3 style layers.</li></ul></li>
 <li><h4>different_parameters: </h4>The images stored in this folder correspond to the ones obtained after having modified a hyperparemeter. 
 To have a clear picture as to what exactly was changed, please refer to the name of the image.</li>
 
