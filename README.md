# ProjectANNsWTF
<h1>Final Project Artistic Style Transfer </h1>

<p  align="justify">This is a Tensorflow implementation of Artistic Style Transfer mainly based on Gaty et. al. paper https://arxiv.org/abs/1508.06576 (For further 
datails regarding the sources used please refer to the report that accompanies this project)

Our algorithm synthesizes the style of an image S and the content of an image C into a new image G. </p>




<h3> Setup</h3>
<div  align="justify">
The development and testing of the algorithm was done in Colab.
<ol>
 <li> Open the noteboook MasterWTF.ipynb in Colab. </li>
 <li>Create a folder in your Google Drive named ANNs StyleTransfer.</li>
 <li>Save the source images to the folder created in step 2. The images can be found here: https://github.com/yesidc/ProjectANNsWTF/tree/main/source_img </li>
 <li> Run the notebook and mount your Google Drive when asked to do so. </li>
</ol>
</div>


<h3>Running the Model:</h3>

<p  align="justify">You can either run MasterWTF.ipynb with the default parameters or you can customize it as you wish 
to conduct your own experiments. </p>


<h4>Conducting your own Experiments: </h4>
<ol>
         <li> Go to the section 'Where stuff happens'. </li>
         <li>Either uncomment any of the already set up experiments or set up a new one by creating a list like so: </li>
</ol>
runList=[

         runConfig(1,optimizer= desired optimizer(learning_rate= desired learning rate, beta_1=desired beta value, epsilon=desired epsilon value)),
         runConfig(2, style_weight = desired value, content_weight= desired cotent weight value),
      
]

<p  align="justify">In example above we set up two experiments. The first one, identified with id = 1, sets a desired optimizer, learning rate, beta and epsison values. 
In the second experiment with id = 2, we modified the values of the style weight and content weight to the values we wanted to try out. 
The following parameters can be modified: </p>

<ul>
         <li>number # id </li>

<li> initImageMode</li>

<li> img_content_name </li>

<li> img_style_name </li>

<li> imgwidth </li>

<li> color_preservation_method </li>

<li> content_weight </li>

<li> style_weight </li>

<li> style_layer_weights_modifiers </li>

<li> optimizer </li>
</ul>                




