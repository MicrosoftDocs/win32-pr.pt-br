---
title: 'Aceleração de GPU no WSL – Perguntas frequentes '
description: Perguntas frequentes sobre a aceleração de GPU no subsistema do Windows para Linux
ms.topic: article
ms.date: 09/28/2020
ms.openlocfilehash: 7c55a8c06bd2b62c670cbf532bc3aa65ddd919d7
ms.sourcegitcommit: f58718691e8b989650108b8c70aaa471d17bf3aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "105793759"
---
# <a name="faq"></a>Perguntas frequentes

### <a name="how-do-i-enable-directml-acceleration"></a>Como fazer habilitar a aceleração DirectML? 

 
O dispositivo DirectML está habilitado por padrão, supondo que você tenha uma GPU apropriada do DirectX 12 disponível. As operações TensorFlow serão automaticamente atribuídas ao dispositivo DirectML, se possível. 

Se você tiver problemas para determinar se seu modelo está sendo executado usando a aceleração DirectML ou não, você pode colocar `tf.debugging.set_log_device_placement(True)` como a primeira instrução do programa e o TensorFlow imprimirá as informações de posicionamento do dispositivo no console.

### <a name="how-do-i-control-device-placement-of-specific-operations"></a>Como fazer controlar o posicionamento de dispositivos de operações específicas? 
 

Como com qualquer outro dispositivo (consulte [o guia do TensorFlow: usar uma GPU](https://www.tensorflow.org/guide/gpu)), você pode usar o `tf.device()` para controlar em qual dispositivo executar. 
 

A cadeia de caracteres do dispositivo DirectML é `'DML'` . 


```python 

import tensorflow as tf 

tf.debugging.set_log_device_placement(True) 

tf.enable_eager_execution() 

 

# Explicitly place tensors on the DirectML device 

with tf.device('/DML:0'): 

  a = tf.constant([1.0, 2.0, 3.0]) 

  b = tf.constant([4.0, 5.0, 6.0]) 

 

c = tf.add(a, b) 

print(c) 

``` 


``` 

Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([5. 7. 9.], shape=(3,), dtype=float32) 

```

### <a name="i-have-multiple-gpus-how-do-i-select-which-one-is-used-by-directml"></a>Tenho várias GPUs. Como fazer selecionar qual delas é usada pelo DirectML?

Há algumas maneiras diferentes de fazer isso, dependendo se você deseja controlar todo o processo de ti ou por sessão (ou ambos).

Se você quiser controlar quais dispositivos estão visíveis para TensorFlow todo o processo, use a `DML_VISIBLE_DEVICES` variável de ambiente. Se você quiser controlá-lo por sessão, use `tf.GPUOptions.visible_device_list` .

### <a name="how-do-i-use-the-dml_visible_devices-environment-variable-to-control-which-gpus-get-used-by-directml"></a>Como fazer usar a `DML_VISIBLE_DEVICES` variável de ambiente para controlar quais GPU (s) são usadas pelo DirectML?

TensorFlow com DirectML dá suporte a uma `DML_VISIBLE_DEVICES` variável de ambiente, que assume a forma de uma lista separada por vírgulas de IDs de dispositivo (também conhecido como "índices de adaptador".) Quando definido, somente as IDs de dispositivo nessa lista ficarão visíveis para TensorFlow todo o processo. Os dispositivos excluídos usando `DML_VISIBLE_DEVICES` o não serão exibidos na lista de dispositivos físicos disponíveis para TensorFlow.

```python
import tensorflow as tf
tf.debugging.set_log_device_placement(True)
tf.enable_eager_execution()

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)
print(c)
```

Aqui está um exemplo de saída **sem** o `DML_VISIBLE_DEVICES` conjunto:

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (NVIDIA TITAN V)
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Com `DML_VISIBLE_DEVICES="1"`:

```
DirectML device enumeration: found 1 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Observe que, ao restringir os dispositivos visíveis somente para o índice 1 (AMD Radeon RX 5700 XT), TensorFlow agora atribui uma ID de 0 a esse dispositivo e o torna o padrão.

Você também pode reordenar os dispositivos usando essa variável de ambiente. Por exemplo, configuração `DML_VISIBLE_DEVICES="1,0"` :

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
DirectML: creating device on adapter 1 (NVIDIA TITAN V)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

Observe que as duas GPUs (NVIDIA TITAN V e AMD Radeon RX 5700 XT) agora têm locais alternados.

Para impedir que dispositivos específicos fiquem visíveis, você pode fornecer uma ID inválida (por exemplo, `-1` ) na lista separada por vírgulas. Todas as IDs de dispositivo após a entrada inválida são ignoradas. Você também pode usar isso para desabilitar totalmente a aceleração de DirectML.

`DML_VISIBLE_DEVICES="-1"`:

```
DirectML device enumeration: found 0 compatible adapters.
Executing op Add in device /job:localhost/replica:0/task:0/device:CPU:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

### <a name="how-do-i-use-the-visible_device_list-session-option-to-control-which-gpus-directml-uses-to-run-the-session"></a>Como fazer usar a `visible_device_list` opção de sessão para controlar quais GPU (s) o DirectML usa para executar a sessão?

Semelhante a `DML_VISIBLE_DEVICES` , você também pode definir uma cadeia de caracteres semelhante para controlar os dispositivos visíveis em um nível de sessão. O `visible_device_list` atributo está disponível na `GPUOptions` classe ao criar sua sessão TensorFlow.

```python
import tensorflow as tf

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)

gpu_config = tf.GPUOptions()
gpu_config.visible_device_list = "1"

session = tf.Session(config=tf.ConfigProto(gpu_options=gpu_config))
print(session.run(c))
```

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
[3.]
```

Você pode ler a [referência de API do TensorFlow GPUOptions](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) para obter mais detalhes.