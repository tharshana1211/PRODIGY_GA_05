🎨 **Neural Style Transfer using TensorFlow & VGG19**

This project implements Neural Style Transfer (NST) using a pre-trained VGG19 model in TensorFlow.
It combines the content of one image with the style of another image to generate an artistic output.

📌 **Project Overview**

Neural Style Transfer is a deep learning technique that:

Preserves the content structure of an image

Transfers the artistic style (texture, colors, brush strokes) from another image

Produces a stylized, artistic output

This implementation uses:

✅ TensorFlow 2.x

✅ Pretrained VGG19 (ImageNet weights)

✅ Gram Matrix for style representation

✅ Content + Style + Total Variation Loss

✅ Adam Optimizer

🧠 **How It Works**

1️⃣ **Feature Extraction**

We use selected layers from VGG19:

Content Layer : block5_conv2

Style Layers :

block1_conv1

block2_conv1

block3_conv1

block4_conv1

block5_conv1

2️⃣ **Loss Function**

The total loss consists of:

🎨 Style Loss (Gram Matrix comparison)

🖼 Content Loss (Feature difference)

🌊 Total Variation Loss (Smoothness regularization)

Total Loss = Style Loss + Content Loss + TV Loss

⚙️ **Key Parameters**

You can tune artistic strength here:

style_loss *= 1e-3
content_loss *= 1e2
epochs = 300
learning_rate = 0.02

**To Increase Artistic Effect:**

Increase style_loss weight

Increase number of epochs

**To Preserve Content More:**

Increase content_loss weight

🖼 **Example Output**

Content Image:
Dog image

Style Image:
Art painting

Generated Image:
Stylized artistic version of the dog image

🎯 **Features**

Fully customizable style intensity

Total variation loss for smoother results

Works with any content and style images

GPU compatible

Clean TensorFlow implementation

💡 **Future Improvements**

Add live progress visualization

Add multi-style blending

Convert into Streamlit web app

Use Faster Style Transfer with pretrained feed-forward networks
