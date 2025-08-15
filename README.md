Scene Localization in Dense Images via Natural Language Queries

The goal is to build a system that can understand a dense, complex image and pinpoint a specific sub-scene based on a simple text description, like finding "multiple people talking" in a busy street photo.

My approach was to start with a working prototype and then plan a more advanced solution.

To get a system up and running quickly, I built a pipeline that combines two powerful, pre-trained models:

1 YOLOS (You Only Look at One Sequence): An object detection model that scans the image and identifies all the objects, giving me a starting point.
2 CLIP (Contrastive Language-Image Pre-training): A vision-language model that acts as the "brain." It compares the cropped image regions with the user's text query to find the best match.

Looking ahead, I have a plan for a more accurate and robust system. This pipeline would involve:

1 Fine-tuning Faster R-CNN: Instead of using a general-purpose object detector, I would fine-tune a more precise model to be an expert in the specific scenes of my project.
2 Leveraging BLIP-2: A more advanced vision-language model that can handle more complex reasoning, helping to understand nuanced queries.
