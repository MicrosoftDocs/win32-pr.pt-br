---
title: Tensorflow com DirectML no WSL 2
description: Habilitar TensorFlow com DirectML no subsistema do Windows para Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: bfd776013e417760d52134d697439be60c5a1ae8
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "105790657"
---
# <a name="enable-tensorflow-with-directml-in-wsl-2"></a>Habilitar o TensorFlow com o DirectML no WSL 2

Essa visualização fornece aos alunos e iniciantes uma maneira de começar a criar conhecimento no espaço ML em seu hardware existente usando o TensorFlow com o pacote DirectML. Uma vez configurado, os usuários podem começar com os [modelos de tutorial do TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou com nossos exemplos de [DirectML](https://github.com/microsoft/DirectML). 

> [!NOTE]
> Os recursos a seguir estão disponíveis em versões de pré-lançamento do Windows 10 e estão sujeitos a alterações.

## <a name="install-the-latest-windows-insider-dev-channel-build"></a>Instalar a compilação mais recente do canal de desenvolvimento do Windows Insider 

Para usar essa versão prévia, você precisará [se registrar para o programa Windows Insider](https://insider.windows.com/getting-started/#register). Depois de fazer isso, siga [estas instuctions](https://insider.windows.com/getting-started/#install) para instalar a compilação mais recente do insider. Ao escolher suas configurações, verifique se você está selecionando o [canal de desenvolvimento](/windows-insider/flight-hub/#active-development-builds-of-windows-10). 

Para esta versão prévia, você precisa compilar 20150 ou superior. Você pode verificar o número de versão da compilação executando `winver` por meio do comando **executar** (tecla do logotipo do Windows + R).

## <a name="install-the-preview-gpu-driver"></a>Instalar o driver de GPU de visualização 

Antes de instalar o TensorFlow com o pacote DirectML no WSL 2, você precisa instalar drivers de seu fornecedor de hardware de GPU. Esses drivers permitem que a GPU do Windows funcione com o WSL 2.

### <a name="amd"></a>AMD 

[Baixe e instale o driver de visualização da AMD](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) em seu site. Este driver de visualização dá suporte ao seguinte hardware: 

* Série AMD Radeon™ RX e Radeon™ VII Graphics. 
* Gráficos da série AMD Radeon™ pro. 
* Processadores AMD Ryzen™ e Ryzen™ PRO com gráficos Radeon™ Vega. 
* Processadores AMD Ryzen™ e Ryzen™ PRO com placa gráfica Radeon™ Vega. 

Para obter uma lista completa de produtos AMD compatíveis, consulte as notas de versão do AMD. 

### <a name="intel"></a>Intel 

[Baixe e instale o driver de versão prévia da Intel](https://downloadcenter.intel.com/download/29526) para usar com o DirectML em seu site. 

### <a name="nvidia"></a>NVIDIA 

[Baixe e instale o driver de visualização da NVIDIA](https://developer.nvidia.com/cuda/wsl/download) para usar com o DirectML em seu site. Para obter mais informações, consulte [GPU da NVIDIA na página do subsistema do Windows para Linux (WSL)](https://developer.nvidia.com/cuda/wsl) .

## <a name="set-up-the-tensorflow-with-directml-preview"></a>Configurar o TensorFlow com o DirectML Preview 

### <a name="install-wsl-2"></a>Instalar o WSL 2 

Depois de instalar o driver acima, verifique se você [habilitou o WSL 2](/windows/wsl/install-win10) e [Instale uma distribuição baseada em glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (como Ubuntu ou Debian). Para nossos testes, usamos o Ubuntu. Verifique se você tem o kernel mais recente selecionando **verificar atualizações** na seção **Windows Update** do aplicativo configurações. 

> [!NOTE]
> Verifique se você tem as **atualizações recebidas para outros produtos da Microsoft ao atualizar o Windows** habilitado. Você pode encontrá-lo em **Opções avançadas** na seção **Windows Update** do aplicativo configurações. 

Para essa visualização, você precisa de uma versão de kernel do 4.19.121 ou superior. Você pode verificar o número de versão executando o comando a seguir no PowerShell. 

```
wsl cat /proc/version
```

### <a name="set-up-python-environment"></a>Configurar o ambiente do Python 

É recomendável configurar um ambiente Python virtual dentro de sua instância do WSL 2. Há muitas ferramentas que você pode usar para configurar um ambiente virtual Python – para essas instruções, usaremos o [Miniconda da Anaconda](https://docs.conda.io/en/latest/miniconda.html). O restante dessa configuração pressupõe que você use um ambiente miniconda. 

Instale o Miniconda seguindo as [diretrizes no site do Anaconda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)ou executando os comandos a seguir no WSL. 

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh 
```

Depois que o Miniconda for instalado no WSL, crie um ambiente usando o Python chamado "directml" e ative-o por meio dos comandos a seguir. 

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

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library libdirectml.so.ba106a7c621ea741d21598708ee581c11918380 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a>Tensorflow com exemplos e comentários do DirectML 

Agora você está pronto para começar a aprender mais sobre o treinamento de ML. Confira os [tutoriais do TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou [nossos exemplos](https://github.com/microsoft/DirectML). Usamos este conteúdo como validação para este pacote de visualização inicial de TensorFlow com DirectML. 

Se você tiver problemas ou tiver comentários sobre o TensorFlow com o pacote DirectML, [Conecte-se à nossa equipe aqui](https://github.com/microsoft/DirectML/issues).
