## Tensorboard
### Visualize Graph
First, you need to specify a writer.
```python
writer = tf.summary.FileWriter(path/to/save/logdir, sess.graph)
writer.close()
```
 The first para is path to save the logdir, and there are other methods based on the writer (e.g. add the graph). More information can be found [here](https://www.tensorflow.org/api_docs/python/tf/summary/FileWriter). Don't forget to close the writer to make sure you write all the log file completely.
 
 ### Visualize Tensor
 To keep track of the metric, you can use tf.summary.scalar/histogram/image based on the types of needs. For weights, you can use histogram method. Official docu can be found [here](https://www.tensorflow.org/api_docs/python/tf/summary)
 ```python
with tf.name_scope("accuracy"):
    correct_prediction = tf.equal(tf.argmax(logits, 1), tf.argmax(y, 1))
    accuracy = tf.reduce_mean(tf.cast(correct_prediction, tf.float32))
    tf.summary.scalar("accuracy", accuracy)
 ```
 
 Instead of call sess.run(...) each time you want to visualize tensor, you can simply call the following function
 ```python
 sum = tf.summary.merge_all()
 ```
Then run the sum within the session. It will generate a 'event?' file in the path you specify. Then run the following code to show on the tensorboard.

```python
tensorboard --logdir path/to/logdir 
```

## Save and restore the model
In order to save the model for later use, you can first define a trainer as follows:
```python
saver = tf.train.Saver()

```




## Clear all

```python
tf.reset_default_graph()
```
**Note:** It does not only clear all the variables, but also all the operations.




