page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.layers.dot


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/keras/layers/merge.py#L708-L725">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Functional interface to the `Dot` layer.

### Aliases:

* `tf.compat.v1.keras.layers.dot`
* `tf.compat.v2.keras.layers.dot`


``` python
tf.keras.layers.dot(
    inputs,
    axes,
    normalize=False,
    **kwargs
)
```



<!-- Placeholder for "Used in" -->


#### Arguments:


* <b>`inputs`</b>: A list of input tensors (at least 2).
* <b>`axes`</b>: Integer or tuple of integers,
    axis or axes along which to take the dot product.
* <b>`normalize`</b>: Whether to L2-normalize samples along the
    dot product axis before taking the dot product.
    If set to True, then the output of the dot product
    is the cosine proximity between the two samples.
* <b>`**kwargs`</b>: Standard layer keyword arguments.


#### Returns:

A tensor, the dot product of the samples from the inputs.