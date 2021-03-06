# StoreProductRecognizer
<b>The ipynb notebbok cnn_multiplayers-copy2.ipynb contains the entire code with comments the framework used is pytorch </b> 
<center><h2> ABSTRACT </h2></center>
<p>Grocery item image classification is a well-researched problem. However, until the recent announcements form Amazon regarding their “Just walk out” technology used in Amazon Go, most Computer Vision and Machine Learning techniques used in the state-of-the-art research did not involve neural network</p>
<p>The aim of this project is to recognize products in a store shelves using Convolution Neural Network (CNN). This helps to provide more accuracy in categorizing the products to help the owners to avoid problems like product misplacement, product availability in the shelves. The results of the detection are stored in a database to make in much easier and faster to process this information later in order to create a custom service as required by the owners.</p>
<br/>
<b>Keywords:</b>CNN, Computer Vision, Machine Learning, Product Recognition
<br/>
<center><h2> INTRODUCTION </h2></center>
<p>The recent emphasis on using computer vision and machine learning to assist store’s owners is facing many reliability and performance issues. In this study, we demonstrate a system that recognizes the products in shelf images. The results of the detection process are stored in a database for faster processing when required. Two of the most important situations that store owners need to avoid are out of stock, misplaced products and percentage of a product in a specific section of the shelves. To avoid these situations, for example, it is possible to set up an alarm that counts the number of products in the produced database to notify the owner when it is below a preset limit, or, set up an alarm when a specific product is found in an image that is not supposed to be in.</p>
<p>The products are detected using CNN in which image is passed through a series of convolutional, non-linear layer, pooling layers and fully connected layers and then generates the output. The computer sees the image as an array of pixels. For example, if image size is 300 x 300. In this case, the size of the array will be 300x300x3. Where 300 is width, next 300 is height and 3 is RGB channel values. The computer is assigned a value from 0 to 255 to each of these numbers. This value describes the intensity of the pixel at each point. To solve this problem the computer looks for the characteristics of the base level. In human understanding such characteristics are for example logo or shape or size of the product. For the computer, these characteristics are boundaries or curvatures. And then through the groups of convolutional layers the computer constructs more abstract concepts</p>
<p><b>The ambition of this project is to automate the system and provide a user-friendly application which can be used to detect products on the store shelves and the problem of high cost of human power, out of stock and product misplacement situations can be reduced.</b> </p>
<center><h2> DATASET </h2></center>
https://github.com/gulvarol/grocerydataset/blob/master/README.md
<br>
<p>The image grocery dataset consists of 4947 images of 10 grocery classes, with 97 to 370 images per class. We considered common categories of groceries that exists in the most homes such as pasta, spices, coffee, etc. The images of the dataset are captured using smartphone cameras at various grocery stores. The images vary in the degree of clutter and real-world lightning conditions, ranging from well-lit stores to kitchen cupboards. Each image in the dataset contains one or multiple instances of one of the 10 classes. Moreover, for each class, we considered a rich variety of brands, flavors, and packaging designs. The images in the dataset are down-scaled into 256 × 256 pixels. Due to different aspect ratios of the cameras, the images are padded with gray borders as needed.</p> 
<img src="https://github.com/mayanku/StoreProductRecognizer/blob/master/Capture.PNG"><br>
<b>We demonstrate the use of our dataset by training a deep neural network classifier using the images in the dataset. We trained this model which consists of 5 convolutional layers and 2 fully connected layers, using the PyTorch framework<b><br>
<h2> Our Network architecture</h2><br>
<p>The neural network which we designed in this project consists of 5 convolutional layers with 8, 16, 32, 64 and 128 filters in layer 1, 2, 3, 4 and 5 respectively. The kernel size of the filter used in convolutional layer is 2 × 2 with stride = 1 and padding = 0. To reduce the features from the convolve feature map we used max pooling with a filter of kernel size 2 × 2, stride = 2 and padding = 0. The network consists of 2 fully connected layer with 128*8*8 = 8192 neurons in the layer 1 and 64 neurons in layer 2. Finally, we have a Relu activation function which classify the image into different classes like Tea, Cereals, Honey, etc</p><br>
<img src="https://github.com/mayanku/StoreProductRecognizer/blob/master/Capture1.PNG"><br>
<h2>Network Description</h2>
<p>1. The input image is of the 3 × 256 × 256. After the first convolutional layer with 8 filter (kernel size(k) = 3, stride(s) = 1, padding(p) = 0), its size get changed into 8 × 256 × 256. After the pooling (kernel size =2, stride =2, p = 0), the size gets reduced to 8 × 128 × 128.</p><br>
<p>2. In the second conv. layer the size changes from 8 × 128 × 128 to 16 × 128 × 128 (16 filters used) and after the pooling, the size becomes 16 × 64 × 64</p><br>
<p>3. In the third conv. layer the size changes from 16 × 64 × 64 to 32 × 64 × 64 (32 filters used) and after the pooling, the size becomes 32 × 32 × 32.</p><br>
<p>4. In the fourth conv. layer, the size changes from 32 × 32 × 32 to 64 × 32 × 32 (64 filter used) and after the pooling, the size becomes 64 × 16 × 16.</p><br>
<p>5. In the fifth and final layer, the size change from 64 × 16 × 16 to 128 × 16 × 16 (128 filters used) and after the pooling, the size becomes 128 × 8 × 8.</p><br>
<p>6. Finally, the feature map produced after 5 layers of convolutional and pooling is flatten in 1 dimensional vector of size 128*8*8 = 8192.</p><br>
<p>7. The first fully connected layers contain 8192 number of neurons which are further passed into the hidden layer and finally Relu functions outputs the results and classify the image into 10 different classes.</p><br>   

  
  
  
  
 
