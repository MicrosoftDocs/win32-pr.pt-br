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
# <a name="enable-tensorflow-with-directml-on-windows"></a><span data-ttu-id="c7cba-103">Habilitar o TensorFlow com o DirectML no Windows</span><span class="sxs-lookup"><span data-stu-id="c7cba-103">Enable TensorFlow with DirectML on Windows</span></span>

<span data-ttu-id="c7cba-104">Essa visualização fornece aos alunos e iniciantes uma maneira de começar a criar seu conhecimento no espaço ML em seu hardware existente usando o pacote TensorFlow com DirectML.</span><span class="sxs-lookup"><span data-stu-id="c7cba-104">This preview provides students and beginners a way to start building their knowledge in the ML space on their existing hardware by using the the TensorFlow with DirectML package.</span></span> <span data-ttu-id="c7cba-105">Uma vez configurado, os usuários podem começar com os [modelos de tutorial do TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou com [nossos exemplos de DirectML](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="c7cba-105">Once set up, users can start with the [TensorFlow tutorial models](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our DirectML samples](https://github.com/microsoft/DirectML).</span></span> 

> [!NOTE]
> <span data-ttu-id="c7cba-106">O recurso a seguir está em versão prévia e está sujeito a alterações.</span><span class="sxs-lookup"><span data-stu-id="c7cba-106">The following feature is in preview, and are subject to change.</span></span>

## <a name="check-your-version-of-windows"></a><span data-ttu-id="c7cba-107">Verifique sua versão do Windows</span><span class="sxs-lookup"><span data-stu-id="c7cba-107">Check your version of Windows</span></span> 

<span data-ttu-id="c7cba-108">O TensorFlow com o pacote DirectML no Windows Works nativo a partir do Windows 10 versão 1709 (Build 16299 ou superior).</span><span class="sxs-lookup"><span data-stu-id="c7cba-108">The TensorFlow with DirectML package on native Windows works starting with Windows 10 Version 1709 (Build 16299 or higher).</span></span> <span data-ttu-id="c7cba-109">Você pode verificar o número de versão da compilação executando `winver` por meio do comando **executar** (tecla do logotipo do Windows + R).</span><span class="sxs-lookup"><span data-stu-id="c7cba-109">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="check-for-gpu-driver-updates"></a><span data-ttu-id="c7cba-110">Verificar atualizações de driver de GPU</span><span class="sxs-lookup"><span data-stu-id="c7cba-110">Check for GPU driver updates</span></span> 

<span data-ttu-id="c7cba-111">Verifique se você tem o driver de GPU mais recente instalado.</span><span class="sxs-lookup"><span data-stu-id="c7cba-111">Ensure you have the latest GPU driver installed.</span></span> <span data-ttu-id="c7cba-112">Selecione **verificar se há atualizações** na seção **Windows Update** do aplicativo configurações.</span><span class="sxs-lookup"><span data-stu-id="c7cba-112">Select **Check for updates** in the **Windows Update** section of the Settings app.</span></span>

## <a name="set-up-the-tensorflow-with-directml-preview"></a><span data-ttu-id="c7cba-113">Configurar o TensorFlow com o DirectML Preview</span><span class="sxs-lookup"><span data-stu-id="c7cba-113">Set up the TensorFlow with DirectML preview</span></span> 

<span data-ttu-id="c7cba-114">É recomendável configurar um ambiente Python virtual dentro do Windows.</span><span class="sxs-lookup"><span data-stu-id="c7cba-114">We recommend setting up a virtual Python environment inside Windows.</span></span> <span data-ttu-id="c7cba-115">Há muitas ferramentas que você pode usar para configurar um ambiente virtual Python – para essas instruções, usaremos o [Miniconda da Anaconda](https://docs.conda.io/en/latest/miniconda.html).</span><span class="sxs-lookup"><span data-stu-id="c7cba-115">There are many tools you can use to setup a virtual Python environment — for these instructions, we'll use [Anaconda’s Miniconda](https://docs.conda.io/en/latest/miniconda.html).</span></span> <span data-ttu-id="c7cba-116">O restante dessa configuração pressupõe que você use um ambiente miniconda.</span><span class="sxs-lookup"><span data-stu-id="c7cba-116">The rest of this setup assumes you use a miniconda environment.</span></span> 

### <a name="set-up-python-environment"></a><span data-ttu-id="c7cba-117">Configurar o ambiente do Python</span><span class="sxs-lookup"><span data-stu-id="c7cba-117">Set up Python environment</span></span> 

<span data-ttu-id="c7cba-118">Baixe e instale o [Windows Installer do Miniconda](https://docs.conda.io/en/latest/miniconda.html#windows-installers) em seu sistema.</span><span class="sxs-lookup"><span data-stu-id="c7cba-118">Download and install the [Miniconda Windows installer](https://docs.conda.io/en/latest/miniconda.html#windows-installers) on your system.</span></span> <span data-ttu-id="c7cba-119">Há [diretrizes adicionais para a instalação](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) no site do Anaconda.</span><span class="sxs-lookup"><span data-stu-id="c7cba-119">There is [additional guidance for setup](https://conda.io/projects/conda/en/latest/user-guide/install/windows.html) on Anaconda’s site.</span></span> <span data-ttu-id="c7cba-120">Quando o Miniconda estiver instalado, crie um ambiente usando o Python chamado **directml** e ative-o por meio dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c7cba-120">Once Miniconda is installed, create an environment using Python named **directml** and activate it through the following commands.</span></span> 

> [!NOTE]
> <span data-ttu-id="c7cba-121">Nos comandos abaixo, usamos o Python 3,6.</span><span class="sxs-lookup"><span data-stu-id="c7cba-121">In the commands below, we use Python 3.6.</span></span> <span data-ttu-id="c7cba-122">No entanto, o pacote tensorflow-directml funciona em um ambiente Python 3,5, 3,6 ou 3,7.</span><span class="sxs-lookup"><span data-stu-id="c7cba-122">However, the tensorflow-directml package works in a Python 3.5, 3.6 or 3.7 environment.</span></span> 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a><span data-ttu-id="c7cba-123">Instalar o Tensorflow com o pacote DirectML</span><span class="sxs-lookup"><span data-stu-id="c7cba-123">Install the Tensorflow with DirectML package</span></span> 

<span data-ttu-id="c7cba-124">Instale o pacote de TensorFlow com um back-end DirectML por meio de Pip executando o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="c7cba-124">Install the package of TensorFlow with a DirectML backend through pip by running the following command.</span></span>

> [!NOTE]
> <span data-ttu-id="c7cba-125">O pacote tensorflow-directml só dá suporte a TensorFlow 1,15.</span><span class="sxs-lookup"><span data-stu-id="c7cba-125">The tensorflow-directml package only supports TensorFlow 1.15.</span></span> 

```
pip install tensorflow-directml
```

<span data-ttu-id="c7cba-126">Depois de instalar o pacote tensorflow-directml, você pode verificar se ele é executado corretamente adicionando dois dezenases.</span><span class="sxs-lookup"><span data-stu-id="c7cba-126">Once you’ve installed the tensorflow-directml package, you can verify that it runs correctly by adding two tensors.</span></span> <span data-ttu-id="c7cba-127">Copie as linhas a seguir em uma sessão interativa do Python.</span><span class="sxs-lookup"><span data-stu-id="c7cba-127">Copy the following lines into an interactive Python session.</span></span> 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

<span data-ttu-id="c7cba-128">Você deverá ver uma saída semelhante à seguinte, com o operador Add colocado no dispositivo DML.</span><span class="sxs-lookup"><span data-stu-id="c7cba-128">You should see output similar to the following, with the add operator placed on the DML device.</span></span> 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library DirectMLba106a7c621ea741d2159d8708ee581c11918380.dll 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a><span data-ttu-id="c7cba-129">Tensorflow com exemplos e comentários do DirectML</span><span class="sxs-lookup"><span data-stu-id="c7cba-129">Tensorflow with DirectML samples and feedback</span></span> 

<span data-ttu-id="c7cba-130">Agora você está pronto para começar a aprender mais sobre o treinamento de ML.</span><span class="sxs-lookup"><span data-stu-id="c7cba-130">Now you’re ready to start learning more about ML training.</span></span> <span data-ttu-id="c7cba-131">Confira os [tutoriais do TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou [nossos exemplos](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="c7cba-131">Check out the [TensorFlow tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our samples](https://github.com/microsoft/DirectML).</span></span> <span data-ttu-id="c7cba-132">Usamos esse conteúdo como validação para esse pacote de visualização inicial de TensorFlow com um back-end DirectML.</span><span class="sxs-lookup"><span data-stu-id="c7cba-132">We used this content as validation for this initial preview package of TensorFlow with a DirectML backend.</span></span> 

<span data-ttu-id="c7cba-133">Se você tiver problemas ou tiver comentários sobre o TensorFlow com o pacote DirectML, [Conecte-se à nossa equipe aqui](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="c7cba-133">If you run into issues or have feedback on the TensorFlow with DirectML package, please [connect with our team here](https://github.com/microsoft/DirectML/issues).</span></span> 
