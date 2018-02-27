## Clear all

```python
tf.reset_default_graph()
```
**Note:** It does not only clear all the variables, but also all the operations.

## Tensorboard
### Save Graph
First, you need to specify a writer.
```python
writer = tf.summary.FileWriter(path/to/save/logdir, sess.graph)
```
 The first para is path to save the logdir, and there are other methods based on the writer (e.g. add the graph). More information can be found [here](https://www.tensorflow.org/api_docs/python/tf/summary/FileWriter).
