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
# <a name="faq"></a><span data-ttu-id="5d8b9-103">Perguntas frequentes</span><span class="sxs-lookup"><span data-stu-id="5d8b9-103">FAQ</span></span>

### <a name="how-do-i-enable-directml-acceleration"></a><span data-ttu-id="5d8b9-104">Como fazer habilitar a aceleração DirectML?</span><span class="sxs-lookup"><span data-stu-id="5d8b9-104">How do I enable DirectML acceleration?</span></span> 

 
<span data-ttu-id="5d8b9-105">O dispositivo DirectML está habilitado por padrão, supondo que você tenha uma GPU apropriada do DirectX 12 disponível.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-105">The DirectML device is enabled by default, assuming you have an appropriate DirectX 12 GPU available.</span></span> <span data-ttu-id="5d8b9-106">As operações TensorFlow serão automaticamente atribuídas ao dispositivo DirectML, se possível.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-106">TensorFlow operations will automatically be assigned to the DirectML device if possible.</span></span> 

<span data-ttu-id="5d8b9-107">Se você tiver problemas para determinar se seu modelo está sendo executado usando a aceleração DirectML ou não, você pode colocar `tf.debugging.set_log_device_placement(True)` como a primeira instrução do programa e o TensorFlow imprimirá as informações de posicionamento do dispositivo no console.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-107">If you're having trouble determining whether your model is running using DirectML acceleration or not, you can put `tf.debugging.set_log_device_placement(True)` as the first statement of your program and TensorFlow will print device placement information to the console.</span></span>

### <a name="how-do-i-control-device-placement-of-specific-operations"></a><span data-ttu-id="5d8b9-108">Como fazer controlar o posicionamento de dispositivos de operações específicas?</span><span class="sxs-lookup"><span data-stu-id="5d8b9-108">How do I control device placement of specific operations?</span></span> 
 

<span data-ttu-id="5d8b9-109">Como com qualquer outro dispositivo (consulte [o guia do TensorFlow: usar uma GPU](https://www.tensorflow.org/guide/gpu)), você pode usar o `tf.device()` para controlar em qual dispositivo executar.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-109">As with any other device (see [TensorFlow Guide: Use a GPU](https://www.tensorflow.org/guide/gpu)), you can use `tf.device()` to control which device to run on.</span></span> 
 

<span data-ttu-id="5d8b9-110">A cadeia de caracteres do dispositivo DirectML é `'DML'` .</span><span class="sxs-lookup"><span data-stu-id="5d8b9-110">The DirectML device string is `'DML'`.</span></span> 


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

### <a name="i-have-multiple-gpus-how-do-i-select-which-one-is-used-by-directml"></a><span data-ttu-id="5d8b9-111">Tenho várias GPUs.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-111">I have multiple GPUs.</span></span> <span data-ttu-id="5d8b9-112">Como fazer selecionar qual delas é usada pelo DirectML?</span><span class="sxs-lookup"><span data-stu-id="5d8b9-112">How do I select which one is used by DirectML?</span></span>

<span data-ttu-id="5d8b9-113">Há algumas maneiras diferentes de fazer isso, dependendo se você deseja controlar todo o processo de ti ou por sessão (ou ambos).</span><span class="sxs-lookup"><span data-stu-id="5d8b9-113">There are a couple of different ways to do this, depending on whether you want to control it process-wide or per-session (or both).</span></span>

<span data-ttu-id="5d8b9-114">Se você quiser controlar quais dispositivos estão visíveis para TensorFlow todo o processo, use a `DML_VISIBLE_DEVICES` variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-114">If you want to control which devices are visible to TensorFlow process-wide, use the `DML_VISIBLE_DEVICES` environment variable.</span></span> <span data-ttu-id="5d8b9-115">Se você quiser controlá-lo por sessão, use `tf.GPUOptions.visible_device_list` .</span><span class="sxs-lookup"><span data-stu-id="5d8b9-115">If you want to control it on a per-session basis, use `tf.GPUOptions.visible_device_list`.</span></span>

### <a name="how-do-i-use-the-dml_visible_devices-environment-variable-to-control-which-gpus-get-used-by-directml"></a><span data-ttu-id="5d8b9-116">Como fazer usar a `DML_VISIBLE_DEVICES` variável de ambiente para controlar quais GPU (s) são usadas pelo DirectML?</span><span class="sxs-lookup"><span data-stu-id="5d8b9-116">How do I use the `DML_VISIBLE_DEVICES` environment variable to control which GPU(s) get used by DirectML?</span></span>

<span data-ttu-id="5d8b9-117">TensorFlow com DirectML dá suporte a uma `DML_VISIBLE_DEVICES` variável de ambiente, que assume a forma de uma lista separada por vírgulas de IDs de dispositivo (também conhecido como "índices de adaptador".) Quando definido, somente as IDs de dispositivo nessa lista ficarão visíveis para TensorFlow todo o processo.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-117">TensorFlow with DirectML supports a `DML_VISIBLE_DEVICES` environment variable, which takes the form of a comma-separated list of device IDs (also known as "adapter indices".) When set, only the device IDs in that list will be visible to TensorFlow process-wide.</span></span> <span data-ttu-id="5d8b9-118">Os dispositivos excluídos usando `DML_VISIBLE_DEVICES` o não serão exibidos na lista de dispositivos físicos disponíveis para TensorFlow.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-118">Devices excluded using `DML_VISIBLE_DEVICES` will not appear in the list of physical devices available to TensorFlow.</span></span>

```python
import tensorflow as tf
tf.debugging.set_log_device_placement(True)
tf.enable_eager_execution()

a = tf.constant([1.])
b = tf.constant([2.])
c = tf.add(a, b)
print(c)
```

<span data-ttu-id="5d8b9-119">Aqui está um exemplo de saída **sem** o `DML_VISIBLE_DEVICES` conjunto:</span><span class="sxs-lookup"><span data-stu-id="5d8b9-119">Here is example output **without** `DML_VISIBLE_DEVICES` set:</span></span>

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (NVIDIA TITAN V)
DirectML: creating device on adapter 1 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="5d8b9-120">Com `DML_VISIBLE_DEVICES="1"`:</span><span class="sxs-lookup"><span data-stu-id="5d8b9-120">With `DML_VISIBLE_DEVICES="1"`:</span></span>

```
DirectML device enumeration: found 1 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="5d8b9-121">Observe que, ao restringir os dispositivos visíveis somente para o índice 1 (AMD Radeon RX 5700 XT), TensorFlow agora atribui uma ID de 0 a esse dispositivo e o torna o padrão.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-121">Note that by restricting the visible devices to only index 1 (AMD Radeon RX 5700 XT), TensorFlow now assigns an ID of 0 to this device, and makes it the default.</span></span>

<span data-ttu-id="5d8b9-122">Você também pode reordenar os dispositivos usando essa variável de ambiente.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-122">You may also re-order devices using this environment variable.</span></span> <span data-ttu-id="5d8b9-123">Por exemplo, configuração `DML_VISIBLE_DEVICES="1,0"` :</span><span class="sxs-lookup"><span data-stu-id="5d8b9-123">For example, setting `DML_VISIBLE_DEVICES="1,0"`:</span></span>

```
DirectML device enumeration: found 2 compatible adapters.
DirectML: creating device on adapter 0 (AMD Radeon RX 5700 XT)
DirectML: creating device on adapter 1 (NVIDIA TITAN V)
Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

<span data-ttu-id="5d8b9-124">Observe que as duas GPUs (NVIDIA TITAN V e AMD Radeon RX 5700 XT) agora têm locais alternados.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-124">Notice that the two GPUs (NVIDIA TITAN V and AMD Radeon RX 5700 XT) have now switched places.</span></span>

<span data-ttu-id="5d8b9-125">Para impedir que dispositivos específicos fiquem visíveis, você pode fornecer uma ID inválida (por exemplo, `-1` ) na lista separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-125">To prevent specific devices from being visible, you can supply an invalid ID (e.g. `-1`) in the comma-separated list.</span></span> <span data-ttu-id="5d8b9-126">Todas as IDs de dispositivo após a entrada inválida são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-126">All device IDs after the invalid entry are ignored.</span></span> <span data-ttu-id="5d8b9-127">Você também pode usar isso para desabilitar totalmente a aceleração de DirectML.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-127">You can also use this to disable DirectML acceleration altogether.</span></span>

<span data-ttu-id="5d8b9-128">`DML_VISIBLE_DEVICES="-1"`:</span><span class="sxs-lookup"><span data-stu-id="5d8b9-128">`DML_VISIBLE_DEVICES="-1"`:</span></span>

```
DirectML device enumeration: found 0 compatible adapters.
Executing op Add in device /job:localhost/replica:0/task:0/device:CPU:0
tf.Tensor([3.], shape=(1,), dtype=float32)
```

### <a name="how-do-i-use-the-visible_device_list-session-option-to-control-which-gpus-directml-uses-to-run-the-session"></a><span data-ttu-id="5d8b9-129">Como fazer usar a `visible_device_list` opção de sessão para controlar quais GPU (s) o DirectML usa para executar a sessão?</span><span class="sxs-lookup"><span data-stu-id="5d8b9-129">How do I use the `visible_device_list` session option to control which GPU(s) DirectML uses to run the session?</span></span>

<span data-ttu-id="5d8b9-130">Semelhante a `DML_VISIBLE_DEVICES` , você também pode definir uma cadeia de caracteres semelhante para controlar os dispositivos visíveis em um nível de sessão.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-130">Similar to `DML_VISIBLE_DEVICES`, you can also set a similar string to control visible devices at a session level.</span></span> <span data-ttu-id="5d8b9-131">O `visible_device_list` atributo está disponível na `GPUOptions` classe ao criar sua sessão TensorFlow.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-131">The `visible_device_list` attribute is available on the `GPUOptions` class when creating your TensorFlow session.</span></span>

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

<span data-ttu-id="5d8b9-132">Você pode ler a [referência de API do TensorFlow GPUOptions](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) para obter mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="5d8b9-132">You can read the [TensorFlow GPUOptions API reference](https://www.tensorflow.org/versions/r1.15/api_docs/python/tf/GPUOptions#visible_device_list) for more details.</span></span>