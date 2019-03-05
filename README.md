# AI · Big Data 5기

### Posco & Postech AI & Big Data Academy

API문서는 자주 확인하자
- https://www.tensorflow.org/api_docs/python/tf
- 예전에는 activation=**Relu**로 되어있었는데 **None**으로 변경되었다.<br> 확인하는 습관을 기르자.
```python
tf.layers.dense(
    inputs,
    units,
    activation=None,
    use_bias=True,
    kernel_initializer=None,
    bias_initializer=tf.zeros_initializer(),
    kernel_regularizer=None,
    bias_regularizer=None,
    activity_regularizer=None,
    kernel_constraint=None,
    bias_constraint=None,
    trainable=True,
    name=None,
    reuse=None
)
```

참고 사이트
- [TensorFlow-Examples] https://github.com/aymericdamien/TensorFlow-Examples
- [다양한 예제] https://www.github.com/aymericdamien