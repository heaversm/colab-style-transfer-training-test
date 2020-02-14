# Free Colab Style Transfer Training and Usage in ML5

[This codebase is to be used with this colab notebook](https://colab.research.google.com/drive/1FaxxSKWf4WhcWujYh8MLBfqTYYslr6iE).

### Why Google Colab

It's a way to do all sorts of machine learning related tasks in fast, cloud-hosted computers with a lot of the common dependencies and hardware you'll need, without all the hassle of trying to install them on your own machine, use your potentially slower GPU / CPU, (saving you potentially dozens of hours per training), and prevents you from filling up your hard-drive with training datasets and checkpoint files.

### What does it cost?

You used to be able to use the GPU in Colab notebooks for free, but now it requires a Colab Pro membership. At $10 a month, it is much cheaper than other cloud-hosted training options, which run about $10-15 per training for something like style transfer. 

You will likely need Colab Pro to follow along with this notebook, as Colab supposedly caps machine usage at around 12 hours, therefore the training time required necessitates a runtime environment with a GPU and high-RAM usage. You can [sign up here](https://colab.research.google.com/signup).


### Instructions

Visit [the colab notebook in your browser](https://colab.research.google.com/drive/1FaxxSKWf4WhcWujYh8MLBfqTYYslr6iE) and (if you plan to make changes to any of the code), choose `File > Save a Copy in Drive`.

Before you do anything within the notebook, make sure to read the instructions at the top of it, and make the necessary folders on your drive, and upload your chosen style and content images that you plan on training on. 

Colab notebooks work by pushing play next to each codeblock. While it's possible to just choose `Runtime > Run All`, I would recommend doing things one step at a time, in case you get any errors, so that it's easier to troubleshoot. These steps worked for me at the time of writing - I can't guarantee they will work for you - but please let me know if you see any errors in the notebook.

Once you have successfully finished all the steps in the notebook and downloaded your style folder, you can place it into this repo (overwriting the current `models/mystyle/` folder with your own `mystyle` folder.

Then, assuming you haven't changed any of the naming, run a local web server. On Linux and Mac you can do that with python server. That command (from the directory containing the file you're reading now), is:

Python3:
`python -m http.server`

Python2:
`python -m SimpleHTTPServer`

Now open your browser up to the URL that is started (http://localhost:8000 , by default) click allow camera, and you can see your face rendered in real time in the style of your model-trained style image.