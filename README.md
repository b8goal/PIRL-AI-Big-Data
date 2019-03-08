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

경고창 무시 방법
```
import warnings
warnings.filterwarnings('ignore')
```

텐서플로 GPU 가상환경 설치 [tensorlofw-gpu]
```
conda create --name tf tensorflow-gpu
source activate tf
```

텐서플로 Device 환경 확인
```
from tensorflow.python.client import device_lib
device_lib.list_local_devices()
```

텐서플로 글꼴설정
- User 폴더에서 실행해야합니다.
```
cd .jupyter
mkdir custom
vi custom.css
.CodeMirror pre {font-family: Arial; font-size: 14pt; line-height: 140%;}
```

##원격 데스크톱 가상환경이 세팅된 상황에서 jupyter notebook을 사용하고 싶은데, 가상환경 커널이 추가되지 않았을때##
1) 가상환경 활성화
```
source activate [virtualEnv]
```
2) 가상환경에서 jupyter notebook 설치
```
pip install ipykernel
```
3) jupyter notebook에 가상환경 kernel 추가
```
python -m ipykernel install --user --name [virtualEnv] --display-name "[displayKernelName]"
```
4) jupyter notebook 실행해서 kernel 추가 확인
```
jupyter notebook --ip=[ipAddress]
```