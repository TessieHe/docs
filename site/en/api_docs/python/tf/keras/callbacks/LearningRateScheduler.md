page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.callbacks.LearningRateScheduler


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L1311-L1358">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



## Class `LearningRateScheduler`

Learning rate scheduler.

Inherits From: [`Callback`](../../../tf/keras/callbacks/Callback)

### Aliases:

* Class `tf.compat.v1.keras.callbacks.LearningRateScheduler`
* Class `tf.compat.v2.keras.callbacks.LearningRateScheduler`


### Used in the tutorials:

* [Distributed training with Keras](https://www.tensorflow.org/tutorials/distribute/keras)




#### Arguments:


* <b>`schedule`</b>: a function that takes an epoch index as input
    (integer, indexed from 0) and returns a new
    learning rate as output (float).
* <b>`verbose`</b>: int. 0: quiet, 1: update messages.

```python
# This function keeps the learning rate at 0.001 for the first ten epochs
# and decreases it exponentially after that.
def scheduler(epoch):
  if epoch < 10:
    return 0.001
  else:
    return 0.001 * tf.math.exp(0.1 * (10 - epoch))

callback = tf.keras.callbacks.LearningRateScheduler(scheduler)
model.fit(data, labels, epochs=100, callbacks=[callback],
          validation_data=(val_data, val_labels))
```

<h2 id="__init__"><code>__init__</code></h2>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L1335-L1338">View source</a>

``` python
__init__(
    schedule,
    verbose=0
)
```

Initialize self.  See help(type(self)) for accurate signature.




## Methods

<h3 id="on_batch_begin"><code>on_batch_begin</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L464-L465">View source</a>

``` python
on_batch_begin(
    batch,
    logs=None
)
```

A backwards compatibility alias for `on_train_batch_begin`.


<h3 id="on_batch_end"><code>on_batch_end</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L467-L468">View source</a>

``` python
on_batch_end(
    batch,
    logs=None
)
```

A backwards compatibility alias for `on_train_batch_end`.


<h3 id="on_epoch_begin"><code>on_epoch_begin</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L1340-L1354">View source</a>

``` python
on_epoch_begin(
    epoch,
    logs=None
)
```

Called at the start of an epoch.

Subclasses should override for any actions to run. This function should only
be called during TRAIN mode.

#### Arguments:


* <b>`epoch`</b>: integer, index of epoch.
* <b>`logs`</b>: dict. Currently no data is passed to this argument for this method
  but that may change in the future.

<h3 id="on_epoch_end"><code>on_epoch_end</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L1356-L1358">View source</a>

``` python
on_epoch_end(
    epoch,
    logs=None
)
```

Called at the end of an epoch.

Subclasses should override for any actions to run. This function should only
be called during TRAIN mode.

#### Arguments:


* <b>`epoch`</b>: integer, index of epoch.
* <b>`logs`</b>: dict, metric results for this training epoch, and for the
  validation epoch if validation is performed. Validation result keys
  are prefixed with `val_`.

<h3 id="on_predict_batch_begin"><code>on_predict_batch_begin</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L547-L556">View source</a>

``` python
on_predict_batch_begin(
    batch,
    logs=None
)
```

Called at the beginning of a batch in `predict` methods.

Subclasses should override for any actions to run.

#### Arguments:


* <b>`batch`</b>: integer, index of batch within the current epoch.
* <b>`logs`</b>: dict. Has keys `batch` and `size` representing the current batch
  number and the size of the batch.

<h3 id="on_predict_batch_end"><code>on_predict_batch_end</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L558-L566">View source</a>

``` python
on_predict_batch_end(
    batch,
    logs=None
)
```

Called at the end of a batch in `predict` methods.

Subclasses should override for any actions to run.

#### Arguments:


* <b>`batch`</b>: integer, index of batch within the current epoch.
* <b>`logs`</b>: dict. Metric results for this batch.

<h3 id="on_predict_begin"><code>on_predict_begin</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L608-L616">View source</a>

``` python
on_predict_begin(logs=None)
```

Called at the beginning of prediction.

Subclasses should override for any actions to run.

#### Arguments:


* <b>`logs`</b>: dict. Currently no data is passed to this argument for this method
  but that may change in the future.

<h3 id="on_predict_end"><code>on_predict_end</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L618-L626">View source</a>

``` python
on_predict_end(logs=None)
```

Called at the end of prediction.

Subclasses should override for any actions to run.

#### Arguments:


* <b>`logs`</b>: dict. Currently no data is passed to this argument for this method
  but that may change in the future.

<h3 id="on_test_batch_begin"><code>on_test_batch_begin</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L520-L532">View source</a>

``` python
on_test_batch_begin(
    batch,
    logs=None
)
```

Called at the beginning of a batch in `evaluate` methods.

Also called at the beginning of a validation batch in the `fit`
methods, if validation data is provided.

Subclasses should override for any actions to run.

#### Arguments:


* <b>`batch`</b>: integer, index of batch within the current epoch.
* <b>`logs`</b>: dict. Has keys `batch` and `size` representing the current batch
  number and the size of the batch.

<h3 id="on_test_batch_end"><code>on_test_batch_end</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L534-L545">View source</a>

``` python
on_test_batch_end(
    batch,
    logs=None
)
```

Called at the end of a batch in `evaluate` methods.

Also called at the end of a validation batch in the `fit`
methods, if validation data is provided.

Subclasses should override for any actions to run.

#### Arguments:


* <b>`batch`</b>: integer, index of batch within the current epoch.
* <b>`logs`</b>: dict. Metric results for this batch.

<h3 id="on_test_begin"><code>on_test_begin</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L588-L596">View source</a>

``` python
on_test_begin(logs=None)
```

Called at the beginning of evaluation or validation.

Subclasses should override for any actions to run.

#### Arguments:


* <b>`logs`</b>: dict. Currently no data is passed to this argument for this method
  but that may change in the future.

<h3 id="on_test_end"><code>on_test_end</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L598-L606">View source</a>

``` python
on_test_end(logs=None)
```

Called at the end of evaluation or validation.

Subclasses should override for any actions to run.

#### Arguments:


* <b>`logs`</b>: dict. Currently no data is passed to this argument for this method
  but that may change in the future.

<h3 id="on_train_batch_begin"><code>on_train_batch_begin</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L495-L506">View source</a>

``` python
on_train_batch_begin(
    batch,
    logs=None
)
```

Called at the beginning of a training batch in `fit` methods.

Subclasses should override for any actions to run.

#### Arguments:


* <b>`batch`</b>: integer, index of batch within the current epoch.
* <b>`logs`</b>: dict. Has keys `batch` and `size` representing the current batch
  number and the size of the batch.

<h3 id="on_train_batch_end"><code>on_train_batch_end</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L508-L518">View source</a>

``` python
on_train_batch_end(
    batch,
    logs=None
)
```

Called at the end of a training batch in `fit` methods.

Subclasses should override for any actions to run.

#### Arguments:


* <b>`batch`</b>: integer, index of batch within the current epoch.
* <b>`logs`</b>: dict. Metric results for this batch.

<h3 id="on_train_begin"><code>on_train_begin</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L568-L576">View source</a>

``` python
on_train_begin(logs=None)
```

Called at the beginning of training.

Subclasses should override for any actions to run.

#### Arguments:


* <b>`logs`</b>: dict. Currently no data is passed to this argument for this method
  but that may change in the future.

<h3 id="on_train_end"><code>on_train_end</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L578-L586">View source</a>

``` python
on_train_end(logs=None)
```

Called at the end of training.

Subclasses should override for any actions to run.

#### Arguments:


* <b>`logs`</b>: dict. Currently no data is passed to this argument for this method
  but that may change in the future.

<h3 id="set_model"><code>set_model</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L461-L462">View source</a>

``` python
set_model(model)
```




<h3 id="set_params"><code>set_params</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/callbacks.py#L458-L459">View source</a>

``` python
set_params(params)
```