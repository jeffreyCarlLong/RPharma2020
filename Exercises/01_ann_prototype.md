Exercise - Prototyping an Artificial Neural Network in R
================

*Learning Objective: Get an initial intuition for how hyperparameters
affect an ANN model*

You will find a simple Artifical Neural Network implemented in base R
(i.e. no libraries) here:
[R/01\_ann\_prototype.R](../R/01_ann_prototype.R) (This script is also
in the directory `/R` of your RStudio session). You are NOT expected to
follow all the details of the code, but rather an get an impression of
an ANN prototype.

*Your task is to, make the script run and find and tune the
hyperparameters `n_hidden`, `epochs` and `epsilon` to get a working
model*

The model is working, when the `y_pred` values are equal to the `y_true`
values in the right pane of the final plot. Technically, the model is
actually working, when we can set a prediction threshold, which
separates all true negatives `0` from true positives `1`. The left pane
is the training progress and shows the meas squared error for each epoch
(1 epoch = 1 run through all data points)

<details>

<summary>When you have the script running and a working model, click
here to see suggested hyperparameters</summary>

  - `n_hidden = 4` (The number of hidden neurons)
  - `epochs = 200` (The number of training cycles)
  - `epsilon = 0.01` (The learning rate, i.e. size of steps towards a
    better model)

Ok, so this was not particularly straight forward, it doesn’t scale and
writing complicated models this way would be challenging, to say the
least. Let us see if there is a better way.

</details>

When you are looking at the code, it might be a good idea to keep this
visualisation in mind:

![](https://raw.githubusercontent.com/leonjessen/CPHRANNworkshop/master/lectures/figures/ann_04.png)
