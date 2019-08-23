Cross-Entropy
=============

Cross-entropy loss, or log loss, measures the performance of a classification model whose output is a probability value between 0 and 1. Cross-entropy loss increases as the predicted probability diverges from the actual label. So predicting a probability of .012 when the actual observation label is 1 would be bad and result in a high loss value. A perfect model would have a log loss of 0.

.. image:: images/cross_entropy.png
    :align: center

The graph above shows the range of possible loss values given a true observation (isDog = 1). As the predicted probability approaches 1, log loss slowly decreases. As the predicted probability decreases, however, the log loss increases rapidly. Log loss penalizes both types of errors, but especially those predictions that are confident and wrong!

.. note::

Cross-entropy and log loss are slightly different depending on context, but in machine learning when calculating error rates between 0 and 1 they resolve to the same thing.

.. rubric:: Code

.. literalinclude:: ../code/loss_functions.py
      :pyobject: CrossEntropy

.. rubric:: Math

In binary classification, where the number of classes :math:`M` equals 2, cross-entropy can be calculated as:
