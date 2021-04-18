---
title: Tensorflow com DirectML no Windows
description: Habilitar TensorFlow com DirectML diretamente no Windows
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 665ba456d59f09f27a435135468cf71cb6f6f014
ms.sourcegitcommit: 8f3fb56ebad4615389dec5c74d965dec84ad4123
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/22/2020
ms.locfileid: "105762234"
---
# <a name="enable-tensorflow-with-directml-on-windows"></a>Habilitar o TensorFlow com o DirectML no Windows

Essa visualização fornece aos alunos e iniciantes uma maneira de começar a criar seu conhecimento no espaço ML em seu hardware existente usando o pacote TensorFlow com DirectML. Uma vez configurado, os usuários podem começar com os [modelos de tutorial do TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou com [nossos exemplos de DirectML](https://github.com/microsoft/DirectML). 

> [!NOTE]
> O recurso a seguir está em versão prévia e está sujeito a alterações.

## <a name="check-your-version-of-windows"></a>Verifique sua versão do Windows 

O TensorFlow com o pacote DirectML no Windows Works nativo a partir do Windows 10 versão 1709 (Build 16299 ou superior). Você pode verificar o número de versão da compilação executando `winver` por meio do comando **executar** (tecla do logotipo do Windows + R).

## <a name="check-for-gpu-driver-updates"></a>Verificar atualizações de driver de GPU 

Verifique se você tem o driver de GPU mais recente instalado. Selecione **verificar se há atualizações** na seção **Windows Update** do aplicativo configurações.

## <a name="set-up-the-tensorflow-with-directml-preview"></a>Configurar o TensorFlow com o DirectML Preview 

É recomendável configurar um ambiente Python virtual dentro do Windows. Há muitas ferramentas que você pode usar para configurar um ambiente virtual Python – para essas instruções, usaremos o [Miniconda da Anaconda](https://docs.conda.io/en/latest/miniconda.html). O restante dessa configuração pressupõe que você use um ambiente miniconda. 

### <a name="set-up-python-environment"></a>Configurar o ambiente do Python 

Baixe e instale o [Windows Installer do Miniconda](https://docs.conda.io/en/latest/miniconda.html#windows-installers) em seu sistema. Há [diretrizes adicionais para a instalação](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) no site do Anaconda. Quando o Miniconda estiver instalado, crie um ambiente usando o Python chamado **directml** e ative-o por meio dos comandos a seguir. 

> [!NOTE]
> Nos comandos abaixo, usamos o Python 3,6. No entanto, o pacote tensorflow-directml funciona em um ambiente Python 3,5, 3,6 ou 3,7. 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a>Instalar o Tensorflow com o pacote DirectML 

Instale o pacote de TensorFlow com um back-end DirectML por meio de Pip executando o comando a seguir.

> [!NOTE]
> O pacote tensorflow-directml só dá suporte a TensorFlow 1,15. 

```
pip install tensorflow-directml
```

Depois de instalar o pacote tensorflow-directml, você pode verificar se ele é executado corretamente adicionando dois dezenases. Copie as linhas a seguir em uma sessão interativa do Python. 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

Você deverá ver uma saída semelhante à seguinte, com o operador Add colocado no dispositivo DML. 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library DirectMLba106a7c621ea741d2159d8708ee581c11918380.dll 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a>Tensorflow com exemplos e comentários do DirectML 

Agora você está pronto para começar a aprender mais sobre o treinamento de ML. Confira os [tutoriais do TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou [nossos exemplos](https://github.com/microsoft/DirectML). Usamos esse conteúdo como validação para esse pacote de visualização inicial de TensorFlow com um back-end DirectML. 

Se você tiver problemas ou tiver comentários sobre o TensorFlow com o pacote DirectML, [Conecte-se à nossa equipe aqui](https://github.com/microsoft/DirectML/issues). 
