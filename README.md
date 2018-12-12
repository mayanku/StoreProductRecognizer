# StoreProductRecognizer
<center><h2> ABSTRACT </h2></center>
<p>Grocery item image classification is a well-researched problem. However, until the recent announcements form Amazon regarding their “Just walk out” technology used in Amazon Go, most Computer Vision and Machine Learning techniques used in the state-of-the-art research did not involve neural network</p>
<p>The aim of this project is to recognize products in a store shelves using Convolution Neural Network (CNN). This helps to provide more accuracy in categorizing the products to help the owners to avoid problems like product misplacement, product availability in the shelves. The results of the detection are stored in a database to make in much easier and faster to process this information later in order to create a custom service as required by the owners.</p>
<br/>
<b>Keywords:</b>CNN, Computer Vision, Machine Learning, Product Recognition
<br/>
<center><h2> INTRODUCTION </h2></center>
<p>The recent emphasis on using computer vision and machine learning to assist store’s owners is facing many reliability and performance issues. In this study, we demonstrate a system that recognizes the products in shelf images. The results of the detection process are stored in a database for faster processing when required. Two of the most important situations that store owners need to avoid are out of stock, misplaced products and percentage of a product in a specific section of the shelves. To avoid these situations, for example, it is possible to set up an alarm that counts the number of products in the produced database to notify the owner when it is below a preset limit, or, set up an alarm when a specific product is found in an image that is not supposed to be in.</p>
<p>The products are detected using CNN in which image is passed through a series of convolutional, non-linear layer, pooling layers and fully connected layers and then generates the output. The computer sees the image as an array of pixels. For example, if image size is 300 x 300. In this case, the size of the array will be 300x300x3. Where 300 is width, next 300 is height and 3 is RGB channel values. The computer is assigned a value from 0 to 255 to each of these numbers. This value describes the intensity of the pixel at each point. To solve this problem the computer looks for the characteristics of the base level. In human understanding such characteristics are for example logo or shape or size of the product. For the computer, these characteristics are boundaries or curvatures. And then through the groups of convolutional layers the computer constructs more abstract concepts</p>
<p>The ambition of this project is to automate the system and provide a user-friendly application which can be used to detect products on the store shelves and the problem of high cost of human power, out of stock and product misplacement situations can be reduced. </p>


  
 
