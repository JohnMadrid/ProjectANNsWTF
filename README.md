# ProjectANNsWTF
Final Project Artistic Style Transfer

This is a Tensorflow implementation of Artistic Style Transfer mainly based on Gaty et. al. paper https://arxiv.org/abs/1508.06576 (For further 
datails regarding the sources used please refer to the report that accompanies this project)

Our algorithm synthesizes the style of an image S and the content of an image C into a new image G. 


Setup

The development and testing of the algorithm was done in Colab.

1. Open the noteboook MasterWTF.ipynb in Colab.
2. Create a folder in your Google Drive named ANNs StyleTransfer.
3. Save the source images to the folder created in step 2. The images can be found here: https://github.com/yesidc/ProjectANNsWTF/tree/main/source_img
4. Run the notebook and mount your Google Drive when asked to do so. 


Running the Model:

You can either run MasterWTF.ipynb with the default parameters or you can customize it as you wish 
to conduct your own experiments. 

Conducting your own Experiments:
1. Go to the section 'Where stuff happens'.
2. Either uncomment any of the already set up experiments or set up a new one by creating a list like so:

runList=[

         runConfig(1,optimizer= desired optimizer(learning_rate= desired learning rate, beta_1=desired beta value, epsilon=desired epsilon value)),
         
         runConfig(2, style_weight = desired value, content_weight= desired cotent weight value),
      
]

In example above we set up two experiments. The first one, identified with id=1, sets a desired optimizer, learning rate, beta and epsison values. 
In the second experiment with id=2, we modified the values of the style weight and content weight to the values we wanted to try out. 
The following parameters can be modified: 

number # id

initImageMode

img_content_name 

img_style_name 

imgwidth 

color_preservation_method 

content_weight

style_weight 

style_layer_weights_modifiers 

optimizer
                     




