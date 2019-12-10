# DL_HW5

I used the ProGAN architecture by Nvidia to generate frog images: https://github.com/tkarras/progressive_growing_of_gans.

The create_dataset notebook chooses a category from cifar10 (in this case frogs) and saves each 32x32 image as a numpy array to a given directory.

I didn't have to change the original code much; added a function (create_from_images_np) to dataset_tool.py that can read numpy arrays and outputs a tfrecord object, changed the batch size and some other hyperparameters in config.py and train.py.

Also added the trained pickled model, which is a tfutil.Network object and has to be run in the same directory as tfutil.py to generate images.

log.txt contains everything that has occured during training time.
