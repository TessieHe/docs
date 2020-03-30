page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.errors.CancelledError


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/framework/errors_impl.py#L213-L229">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



## Class `CancelledError`

Raised when an operation or step is cancelled.

Inherits From: [`OpError`](../../tf/errors/OpError)

### Aliases:

* Class `tf.compat.v1.errors.CancelledError`
* Class `tf.compat.v2.errors.CancelledError`


<!-- Placeholder for "Used in" -->

For example, a long-running operation (e.g.
`tf.QueueBase.enqueue` may be
cancelled by running another operation (e.g.
`tf.QueueBase.close`,
or by `tf.Session.close`.
A step that is running such a long-running operation will fail by raising
`CancelledError`.


<h2 id="__init__"><code>__init__</code></h2>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/tree/r2.0/tensorflow/python/framework/errors_impl.py#L227-L229">View source</a>

``` python
__init__(
    node_def,
    op,
    message
)
```

Creates a `CancelledError`.




## Properties

<h3 id="error_code"><code>error_code</code></h3>

The integer error code that describes the error.


<h3 id="message"><code>message</code></h3>

The error message that describes the error.


<h3 id="node_def"><code>node_def</code></h3>

The `NodeDef` proto representing the op that failed.


<h3 id="op"><code>op</code></h3>

The operation that failed, if known.

*N.B.* If the failed op was synthesized at runtime, e.g. a `Send`
or `Recv` op, there will be no corresponding
<a href="../../tf/Operation"><code>tf.Operation</code></a>
object.  In that case, this will return `None`, and you should
instead use the <a href="../../tf/errors/OpError#node_def"><code>tf.errors.OpError.node_def</code></a> to
discover information about the op.

#### Returns:

The `Operation` that failed, or None.