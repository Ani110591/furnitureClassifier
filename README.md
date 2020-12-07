# furnitureClassifier
This is a repo to classify identify and classify furniture categories: chairs, sofa, tables, wardrobes

Steps to activate this model:

Step1: Go to the root folder of the project

Step2: Run the existing model:
python scripts/label_image.py --image <local_image_path>

Step3: Retrain the model:
Update the folders chairs, tables, wardrobes or sofas with new images and run
python scripts/retrain.py --output_graph=tf_files/retrained_graph.pb --output_labels=tf_files/retrained_labels.txt --image_dir=tf_files/furniture_photos --architecture mobilenet_1.0_224 --summaries_dir=tf_files/training_summaries/--architecture mobilenet_1.0_224 --bottleneck_dir=tf_files/bottlenecks --how_many_training_steps=500
