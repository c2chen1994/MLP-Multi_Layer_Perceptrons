# Neural-Networks-NN-_Multi-Layer-Perceptrons-MLP-
	Background
		In recent years, neural networks have been one of the most powerful machine learning models. Many toolboxes/platforms
		(e.g., TensorFlow, PyTorch, Torch, Theano, MXNet, Caffe, CNTK) are publicly available
		for efficiently constructing and training neural networks. The core idea of these toolboxes is to treat a neural
		network as a combination of data transformation (or mathematical operation) modules.

		1
			Run script q33.sh. It will output MLP lr0.01 m0.0 w0.0 d0.0.json.
		What it does: q33.sh will run python3 dnn mlp.py with learning rate 0.01, no momentum, no weight
		decay, and dropout rate 0.0. The output file stores the training and validation accuracies over 30 training epochs.

		2	
			Run script q34.sh. It will output MLP lr0.01 m0.0 w0.0 d0.5.json.
		What it does: q34.sh will run python3 dnn mlp.py --dropout rate 0.5 with learning rate 0.01,
		no momentum, no weight decay, and dropout rate 0.5. The output file stores the training and validation
		accuracies over 30 training epochs.

		3
			Run script q35.sh. It will output MLP lr0.01 m0.0 w0.0 d0.95.json.
		What it does: q35.sh will run python3 dnn mlp.py --dropout rate 0.95 with learning rate 0.01,
		no momentum, no weight decay, and dropout rate 0.95. The output file stores the training and validation
		accuracies over 30 training epochs.
			You will observe that the model in 2 will give better validation accuracy (at epoch 30) compared to
		1. Specifically, dropout is widely-used to prevent over-fitting. However, if we use a too large dropout
		rate (like the one in 3), the validation accuracy (together with the training accuracy) will be relatively
		lower, essentially under-fitting the training data.

		4
			Run script q36.sh. It will output LR lr0.01 m0.0 w0.0 d0.0.json.
			What it does: q36.sh will run python3 dnn mlp nononlinear.py with learning rate 0.01, no momentum,
		no weight decay, and dropout rate 0.0. The output file stores the training and validation accuracies
		over 30 training epochs.
			The network has the same structure as the one in 1, except that we remove the relu (nonlinear) layer.
		You will see that the validation accuracies drop significantly (the gap is around 0.03). Essentially, without
		the nonlinear layer, the model is learning multinomial logistic regression.