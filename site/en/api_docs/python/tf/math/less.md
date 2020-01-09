page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.math.less


<table class="tfo-notebook-buttons tfo-api" align="left">
</table>

Defined in generated file: `python/ops/gen_math_ops.py`



Returns the truth value of (x < y) element-wise.

### Aliases:

* `tf.RaggedTensor.__lt__`
* `tf.Tensor.__lt__`
* `tf.compat.v1.RaggedTensor.__lt__`
* `tf.compat.v1.Tensor.__lt__`
* `tf.compat.v1.less`
* `tf.compat.v1.math.less`
* `tf.compat.v2.RaggedTensor.__lt__`
* `tf.compat.v2.Tensor.__lt__`
* `tf.compat.v2.less`
* `tf.compat.v2.math.less`
* `tf.less`


``` python
tf.math.less(
    x,
    y,
    name=None
)
```



<!-- Placeholder for "Used in" -->

*NOTE*: <a href="../../tf/math/less"><code>math.less</code></a> supports broadcasting. More about broadcasting
[here](http://docs.scipy.org/doc/numpy/user/basics.broadcasting.html)

#### Args:


* <b>`x`</b>: A `Tensor`. Must be one of the following types: `float32`, `float64`, `int32`, `uint8`, `int16`, `int8`, `int64`, `bfloat16`, `uint16`, `half`, `uint32`, `uint64`.
* <b>`y`</b>: A `Tensor`. Must have the same type as `x`.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A `Tensor` of type `bool`.