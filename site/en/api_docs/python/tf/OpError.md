


<!-- DO NOT EDIT! Automatically generated file. -->
# tf.OpError

### `class tf.OpError`
### `class tf.errors.OpError`

See the guide: [Running Graphs > Error classes and convenience functions](../../../api_guides/python/client#Error_classes_and_convenience_functions)

A generic error that is raised when TensorFlow execution fails.

Whenever possible, the session will raise a more specific subclass
of `OpError` from the `tf.errors` module.

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
[`tf.Operation`](../tf/Operation)
object.  In that case, this will return `None`, and you should
instead use the [`tf.OpError.node_def`](../tf/OpError#node_def) to
discover information about the op.

#### Returns:

  The `Operation` that failed, or None.



## Methods

<h3 id="__init__"><code>__init__(node_def, op, message, error_code)</code></h3>

Creates a new `OpError` indicating that a particular op failed.

#### Args:

* <b>`node_def`</b>: The `node_def_pb2.NodeDef` proto representing the op that
    failed, if known; otherwise None.
* <b>`op`</b>: The `ops.Operation` that failed, if known; otherwise None.
* <b>`message`</b>: The message string describing the failure.
* <b>`error_code`</b>: The `error_codes_pb2.Code` describing the error.



## Class Members

<h3 id="args"><code>args</code></h3>



Defined in [`tensorflow/python/framework/errors_impl.py`](https://www.tensorflow.org/code/tensorflow/python/framework/errors_impl.py).
