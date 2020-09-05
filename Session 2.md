```python
import dates
```

Cargar datos


```python
dates.user
```




    'Juancxh'




```python
# DATOS LOCALES
import os
os.name
```




    'posix'




```python
# RUTA EN QUE SE TRABAJA
os.getcwd()
```




    '/home/ubuntu/Documents/projects/python/statistic'




```python
# LISTA DE ARCHIVOS DEL DIRECTORIO
os.listdir()
```




    ['dates.py',
     'Session 2.ipynb',
     'dates.ipynb',
     'bicicletas-compartidas.csv',
     '.ipynb_checkpoints',
     '__pycache__']




```python
# INSTALAR PAQUETES PIP EN JUPYTER NOTEBOOK
import sys
!{sys.executable} -m pip install pandas
```

    Collecting pandas
      Downloading pandas-1.1.1-cp38-cp38-manylinux1_x86_64.whl (10.4 MB)
    [K     |████████████████████████████████| 10.4 MB 13.1 MB/s eta 0:00:01
    [?25hRequirement already satisfied: pytz>=2017.2 in /usr/lib/python3/dist-packages (from pandas) (2019.3)
    Collecting numpy>=1.15.4
      Downloading numpy-1.19.1-cp38-cp38-manylinux2010_x86_64.whl (14.5 MB)
    [K     |████████████████████████████████| 14.5 MB 12.0 MB/s eta 0:00:01
    [?25hRequirement already satisfied: python-dateutil>=2.7.3 in /usr/lib/python3/dist-packages (from pandas) (2.7.3)
    Installing collected packages: numpy, pandas
    Successfully installed numpy-1.19.1 pandas-1.1.1



```python
# VISUALIZAR ARCHIVOS CSV
import pandas as pd
archivo = pd.read_csv('bicicletas-compartidas.csv')
```


```python
"""
"head()" es una funcion implícita de panda
permite ver elementos del csv
"""
archivo.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>fecha</th>
      <th>bicis-compartidas</th>
      <th>temp-obs</th>
      <th>sens-temp</th>
      <th>hum</th>
      <th>viento</th>
      <th>codigo-clima</th>
      <th>festivo</th>
      <th>findesemana</th>
      <th>cuartil-ano</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2015-01-04 00:00:00</td>
      <td>182</td>
      <td>3.0</td>
      <td>2.0</td>
      <td>93.0</td>
      <td>6.0</td>
      <td>3.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2015-01-04 01:00:00</td>
      <td>138</td>
      <td>3.0</td>
      <td>2.5</td>
      <td>93.0</td>
      <td>5.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2015-01-04 02:00:00</td>
      <td>134</td>
      <td>2.5</td>
      <td>2.5</td>
      <td>96.5</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2015-01-04 03:00:00</td>
      <td>72</td>
      <td>2.0</td>
      <td>2.0</td>
      <td>100.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2015-01-04 04:00:00</td>
      <td>47</td>
      <td>2.0</td>
      <td>0.0</td>
      <td>93.0</td>
      <td>6.5</td>
      <td>1.0</td>
      <td>0.0</td>
      <td>1.0</td>
      <td>3.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
"""
"columns" ayuda a ver las variables de las columnas
"""
archivo.columns
```




    Index(['fecha', 'bicis-compartidas', 'temp-obs', 'sens-temp', 'hum', 'viento',
           'codigo-clima', 'festivo', 'findesemana', 'cuartil-ano'],
          dtype='object')




```python
"""
"shape" muestra el número de filas y columnas
"""
archivo.shape
```




    (17414, 10)




```python
# INSTALAR PAQUETES PIP EN JUPYTER NOTEBOOK
import sys
!{sys.executable} -m pip install tensorflow
```

    Collecting tensorflow
      Downloading tensorflow-2.3.0-cp38-cp38-manylinux2010_x86_64.whl (320.5 MB)
    [K     |████████████████████████████████| 320.5 MB 3.9 kB/s  eta 0:00:01   |█▌                              | 14.7 MB 8.0 MB/s eta 0:00:39     |███████████████████████████▋    | 276.5 MB 14.3 MB/s eta 0:00:04
    [?25hRequirement already satisfied: wrapt>=1.11.1 in /home/ubuntu/.local/lib/python3.8/site-packages (from tensorflow) (1.12.1)
    Collecting h5py<2.11.0,>=2.10.0
      Downloading h5py-2.10.0-cp38-cp38-manylinux1_x86_64.whl (2.9 MB)
    [K     |████████████████████████████████| 2.9 MB 9.3 MB/s eta 0:00:01
    [?25hCollecting scipy==1.4.1
      Downloading scipy-1.4.1-cp38-cp38-manylinux1_x86_64.whl (26.0 MB)
    [K     |████████████████████████████████| 26.0 MB 12.2 MB/s eta 0:00:01
    [?25hRequirement already satisfied: wheel>=0.26 in /usr/lib/python3/dist-packages (from tensorflow) (0.34.2)
    Requirement already satisfied: six>=1.12.0 in /usr/lib/python3/dist-packages (from tensorflow) (1.14.0)
    Collecting termcolor>=1.1.0
      Downloading termcolor-1.1.0.tar.gz (3.9 kB)
    Collecting numpy<1.19.0,>=1.16.0
      Downloading numpy-1.18.5-cp38-cp38-manylinux1_x86_64.whl (20.6 MB)
    [K     |████████████████████████████████| 20.6 MB 14.8 MB/s eta 0:00:01
    [?25hCollecting tensorflow-estimator<2.4.0,>=2.3.0
      Downloading tensorflow_estimator-2.3.0-py2.py3-none-any.whl (459 kB)
    [K     |████████████████████████████████| 459 kB 21.5 MB/s eta 0:00:01
    [?25hCollecting tensorboard<3,>=2.3.0
      Downloading tensorboard-2.3.0-py3-none-any.whl (6.8 MB)
    [K     |████████████████████████████████| 6.8 MB 27.5 MB/s eta 0:00:01
    [?25hCollecting protobuf>=3.9.2
      Downloading protobuf-3.13.0-cp38-cp38-manylinux1_x86_64.whl (1.3 MB)
    [K     |████████████████████████████████| 1.3 MB 19.6 MB/s eta 0:00:01
    [?25hCollecting opt-einsum>=2.3.2
      Downloading opt_einsum-3.3.0-py3-none-any.whl (65 kB)
    [K     |████████████████████████████████| 65 kB 3.4 MB/s  eta 0:00:01
    [?25hCollecting grpcio>=1.8.6
      Downloading grpcio-1.31.0-cp38-cp38-manylinux2014_x86_64.whl (3.4 MB)
    [K     |████████████████████████████████| 3.4 MB 17.3 MB/s eta 0:00:01
    [?25hCollecting keras-preprocessing<1.2,>=1.1.1
      Downloading Keras_Preprocessing-1.1.2-py2.py3-none-any.whl (42 kB)
    [K     |████████████████████████████████| 42 kB 1.3 MB/s  eta 0:00:01
    [?25hCollecting gast==0.3.3
      Downloading gast-0.3.3-py2.py3-none-any.whl (9.7 kB)
    Collecting astunparse==1.6.3
      Downloading astunparse-1.6.3-py2.py3-none-any.whl (12 kB)
    Collecting absl-py>=0.7.0
      Downloading absl_py-0.10.0-py3-none-any.whl (127 kB)
    [K     |████████████████████████████████| 127 kB 18.4 MB/s eta 0:00:01
    [?25hCollecting google-pasta>=0.1.8
      Downloading google_pasta-0.2.0-py3-none-any.whl (57 kB)
    [K     |████████████████████████████████| 57 kB 4.5 MB/s  eta 0:00:01
    [?25hCollecting tensorboard-plugin-wit>=1.6.0
      Downloading tensorboard_plugin_wit-1.7.0-py3-none-any.whl (779 kB)
    [K     |████████████████████████████████| 779 kB 42.7 MB/s eta 0:00:01
    [?25hCollecting google-auth-oauthlib<0.5,>=0.4.1
      Downloading google_auth_oauthlib-0.4.1-py2.py3-none-any.whl (18 kB)
    Collecting markdown>=2.6.8
      Downloading Markdown-3.2.2-py3-none-any.whl (88 kB)
    [K     |████████████████████████████████| 88 kB 4.7 MB/s  eta 0:00:01
    [?25hCollecting google-auth<2,>=1.6.3
      Downloading google_auth-1.21.1-py2.py3-none-any.whl (93 kB)
    [K     |████████████████████████████████| 93 kB 615 kB/s  eta 0:00:01
    [?25hRequirement already satisfied: setuptools>=41.0.0 in /usr/lib/python3/dist-packages (from tensorboard<3,>=2.3.0->tensorflow) (45.2.0)
    Requirement already satisfied: requests<3,>=2.21.0 in /usr/lib/python3/dist-packages (from tensorboard<3,>=2.3.0->tensorflow) (2.22.0)
    Collecting werkzeug>=0.11.15
      Using cached Werkzeug-1.0.1-py2.py3-none-any.whl (298 kB)
    Collecting requests-oauthlib>=0.7.0
      Downloading requests_oauthlib-1.3.0-py2.py3-none-any.whl (23 kB)
    Collecting rsa<5,>=3.1.4; python_version >= "3.5"
      Downloading rsa-4.6-py3-none-any.whl (47 kB)
    [K     |████████████████████████████████| 47 kB 4.9 MB/s  eta 0:00:01
    [?25hCollecting pyasn1-modules>=0.2.1
      Downloading pyasn1_modules-0.2.8-py2.py3-none-any.whl (155 kB)
    [K     |████████████████████████████████| 155 kB 23.0 MB/s eta 0:00:01
    [?25hCollecting cachetools<5.0,>=2.0.0
      Downloading cachetools-4.1.1-py3-none-any.whl (10 kB)
    Requirement already satisfied: oauthlib>=3.0.0 in /usr/lib/python3/dist-packages (from requests-oauthlib>=0.7.0->google-auth-oauthlib<0.5,>=0.4.1->tensorboard<3,>=2.3.0->tensorflow) (3.1.0)
    Collecting pyasn1>=0.1.3
      Downloading pyasn1-0.4.8-py2.py3-none-any.whl (77 kB)
    [K     |████████████████████████████████| 77 kB 4.3 MB/s  eta 0:00:01
    [?25hBuilding wheels for collected packages: termcolor
      Building wheel for termcolor (setup.py) ... [?25ldone
    [?25h  Created wheel for termcolor: filename=termcolor-1.1.0-py3-none-any.whl size=4830 sha256=181d505e8a93662305d5b408ed32179ab0e696b92ab6d21b86218a8f500ce3be
      Stored in directory: /home/ubuntu/.cache/pip/wheels/a0/16/9c/5473df82468f958445479c59e784896fa24f4a5fc024b0f501
    Successfully built termcolor
    Installing collected packages: numpy, h5py, scipy, termcolor, tensorflow-estimator, tensorboard-plugin-wit, pyasn1, rsa, pyasn1-modules, cachetools, google-auth, requests-oauthlib, google-auth-oauthlib, markdown, absl-py, grpcio, protobuf, werkzeug, tensorboard, opt-einsum, keras-preprocessing, gast, astunparse, google-pasta, tensorflow
      Attempting uninstall: numpy
        Found existing installation: numpy 1.19.1
        Uninstalling numpy-1.19.1:
          Successfully uninstalled numpy-1.19.1
    Successfully installed absl-py-0.10.0 astunparse-1.6.3 cachetools-4.1.1 gast-0.3.3 google-auth-1.21.1 google-auth-oauthlib-0.4.1 google-pasta-0.2.0 grpcio-1.31.0 h5py-2.10.0 keras-preprocessing-1.1.2 markdown-3.2.2 numpy-1.18.5 opt-einsum-3.3.0 protobuf-3.13.0 pyasn1-0.4.8 pyasn1-modules-0.2.8 requests-oauthlib-1.3.0 rsa-4.6 scipy-1.4.1 tensorboard-2.3.0 tensorboard-plugin-wit-1.7.0 tensorflow-2.3.0 tensorflow-estimator-2.3.0 termcolor-1.1.0 werkzeug-1.0.1



```python

```
