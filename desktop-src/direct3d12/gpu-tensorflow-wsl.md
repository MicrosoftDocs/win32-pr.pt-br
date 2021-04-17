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
# <a name="enable-tensorflow-with-directml-in-wsl-2"></a><span data-ttu-id="b9061-103">Habilitar o TensorFlow com o DirectML no WSL 2</span><span class="sxs-lookup"><span data-stu-id="b9061-103">Enable TensorFlow with DirectML in WSL 2</span></span>

<span data-ttu-id="b9061-104">Essa visualização fornece aos alunos e iniciantes uma maneira de começar a criar conhecimento no espaço ML em seu hardware existente usando o TensorFlow com o pacote DirectML.</span><span class="sxs-lookup"><span data-stu-id="b9061-104">This preview provides students and beginners a way to start building knowledge in the ML space on their existing hardware by using the TensorFlow with DirectML package.</span></span> <span data-ttu-id="b9061-105">Uma vez configurado, os usuários podem começar com os [modelos de tutorial do TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou com nossos exemplos de [DirectML](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="b9061-105">Once set up, users can start with the [TensorFlow tutorial models](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or our [DirectML samples](https://github.com/microsoft/DirectML).</span></span> 

> [!NOTE]
> <span data-ttu-id="b9061-106">Os recursos a seguir estão disponíveis em versões de pré-lançamento do Windows 10 e estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="b9061-106">The following features are available in prerelease versions of Windows 10, and are subject to change.</span></span>

## <a name="install-the-latest-windows-insider-dev-channel-build"></a><span data-ttu-id="b9061-107">Instalar a compilação mais recente do canal de desenvolvimento do Windows Insider</span><span class="sxs-lookup"><span data-stu-id="b9061-107">Install the latest Windows Insider Dev Channel build</span></span> 

<span data-ttu-id="b9061-108">Para usar essa versão prévia, você precisará [se registrar para o programa Windows Insider](https://insider.windows.com/getting-started/#register).</span><span class="sxs-lookup"><span data-stu-id="b9061-108">To use this preview, you'll need to [register for the Windows Insider Program](https://insider.windows.com/getting-started/#register).</span></span> <span data-ttu-id="b9061-109">Depois de fazer isso, siga [estas instuctions](https://insider.windows.com/getting-started/#install) para instalar a compilação mais recente do insider.</span><span class="sxs-lookup"><span data-stu-id="b9061-109">Once you do, follow [these instuctions](https://insider.windows.com/getting-started/#install) to install the latest insider build.</span></span> <span data-ttu-id="b9061-110">Ao escolher suas configurações, verifique se você está selecionando o [canal de desenvolvimento](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span><span class="sxs-lookup"><span data-stu-id="b9061-110">When choosing your settings, ensure you're selecting the [Dev Channel](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span></span> 

<span data-ttu-id="b9061-111">Para esta versão prévia, você precisa compilar 20150 ou superior.</span><span class="sxs-lookup"><span data-stu-id="b9061-111">For this preview, you need Build 20150 or higher.</span></span> <span data-ttu-id="b9061-112">Você pode verificar o número de versão da compilação executando `winver` por meio do comando **executar** (tecla do logotipo do Windows + R).</span><span class="sxs-lookup"><span data-stu-id="b9061-112">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="install-the-preview-gpu-driver"></a><span data-ttu-id="b9061-113">Instalar o driver de GPU de visualização</span><span class="sxs-lookup"><span data-stu-id="b9061-113">Install the preview GPU driver</span></span> 

<span data-ttu-id="b9061-114">Antes de instalar o TensorFlow com o pacote DirectML no WSL 2, você precisa instalar drivers de seu fornecedor de hardware de GPU.</span><span class="sxs-lookup"><span data-stu-id="b9061-114">Before installing the TensorFlow with DirectML package inside WSL 2, you need to install drivers from your GPU hardware vendor.</span></span> <span data-ttu-id="b9061-115">Esses drivers permitem que a GPU do Windows funcione com o WSL 2.</span><span class="sxs-lookup"><span data-stu-id="b9061-115">These drivers enable the Windows GPU to work with WSL 2.</span></span>

### <a name="amd"></a><span data-ttu-id="b9061-116">AMD</span><span class="sxs-lookup"><span data-stu-id="b9061-116">AMD</span></span> 

<span data-ttu-id="b9061-117">[Baixe e instale o driver de visualização da AMD](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) em seu site.</span><span class="sxs-lookup"><span data-stu-id="b9061-117">[Download and install AMD’s preview driver](https://www.amd.com/en/support/kb/release-notes/rn-rad-win-wsl-support) from their website.</span></span> <span data-ttu-id="b9061-118">Este driver de visualização dá suporte ao seguinte hardware:</span><span class="sxs-lookup"><span data-stu-id="b9061-118">This preview driver supports the following hardware:</span></span> 

* <span data-ttu-id="b9061-119">Série AMD Radeon™ RX e Radeon™ VII Graphics.</span><span class="sxs-lookup"><span data-stu-id="b9061-119">AMD Radeon™ RX series and Radeon™ VII graphics.</span></span> 
* <span data-ttu-id="b9061-120">Gráficos da série AMD Radeon™ pro.</span><span class="sxs-lookup"><span data-stu-id="b9061-120">AMD Radeon™ Pro series graphics.</span></span> 
* <span data-ttu-id="b9061-121">Processadores AMD Ryzen™ e Ryzen™ PRO com gráficos Radeon™ Vega.</span><span class="sxs-lookup"><span data-stu-id="b9061-121">AMD Ryzen™ and Ryzen™ PRO Processors with Radeon™ Vega graphics.</span></span> 
* <span data-ttu-id="b9061-122">Processadores AMD Ryzen™ e Ryzen™ PRO com placa gráfica Radeon™ Vega.</span><span class="sxs-lookup"><span data-stu-id="b9061-122">AMD Ryzen™ and Ryzen™ PRO Mobile Processors with Radeon™ Vega graphics.</span></span> 

<span data-ttu-id="b9061-123">Para obter uma lista completa de produtos AMD compatíveis, consulte as notas de versão do AMD.</span><span class="sxs-lookup"><span data-stu-id="b9061-123">For a complete list of compatible AMD products, please refer to the AMD Release Notes.</span></span> 

### <a name="intel"></a><span data-ttu-id="b9061-124">Intel</span><span class="sxs-lookup"><span data-stu-id="b9061-124">Intel</span></span> 

<span data-ttu-id="b9061-125">[Baixe e instale o driver de versão prévia da Intel](https://downloadcenter.intel.com/download/29526) para usar com o DirectML em seu site.</span><span class="sxs-lookup"><span data-stu-id="b9061-125">[Download and install Intel’s preview driver](https://downloadcenter.intel.com/download/29526) to use with DirectML from their website.</span></span> 

### <a name="nvidia"></a><span data-ttu-id="b9061-126">NVIDIA</span><span class="sxs-lookup"><span data-stu-id="b9061-126">NVIDIA</span></span> 

<span data-ttu-id="b9061-127">[Baixe e instale o driver de visualização da NVIDIA](https://developer.nvidia.com/cuda/wsl/download) para usar com o DirectML em seu site.</span><span class="sxs-lookup"><span data-stu-id="b9061-127">[Download and install NVIDIA's preview driver](https://developer.nvidia.com/cuda/wsl/download) to use with DirectML from their website.</span></span> <span data-ttu-id="b9061-128">Para obter mais informações, consulte [GPU da NVIDIA na página do subsistema do Windows para Linux (WSL)](https://developer.nvidia.com/cuda/wsl) .</span><span class="sxs-lookup"><span data-stu-id="b9061-128">For more information, see [NVIDIA's GPU in Windows Subsystem for Linux (WSL)](https://developer.nvidia.com/cuda/wsl) page.</span></span>

## <a name="set-up-the-tensorflow-with-directml-preview"></a><span data-ttu-id="b9061-129">Configurar o TensorFlow com o DirectML Preview</span><span class="sxs-lookup"><span data-stu-id="b9061-129">Set up the TensorFlow with DirectML preview</span></span> 

### <a name="install-wsl-2"></a><span data-ttu-id="b9061-130">Instalar o WSL 2</span><span class="sxs-lookup"><span data-stu-id="b9061-130">Install WSL 2</span></span> 

<span data-ttu-id="b9061-131">Depois de instalar o driver acima, verifique se você [habilitou o WSL 2](/windows/wsl/install-win10) e [Instale uma distribuição baseada em glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (como Ubuntu ou Debian).</span><span class="sxs-lookup"><span data-stu-id="b9061-131">Once you've installed the above driver, ensure you [enable WSL 2](/windows/wsl/install-win10) and [install a glibc-based distribution](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (like Ubuntu or Debian).</span></span> <span data-ttu-id="b9061-132">Para nossos testes, usamos o Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="b9061-132">For our testing, we used Ubuntu.</span></span> <span data-ttu-id="b9061-133">Verifique se você tem o kernel mais recente selecionando **verificar atualizações** na seção **Windows Update** do aplicativo configurações.</span><span class="sxs-lookup"><span data-stu-id="b9061-133">Ensure you have the latest kernel by selecting **Check for updates** in the **Windows Update** section of the Settings app.</span></span> 

> [!NOTE]
> <span data-ttu-id="b9061-134">Verifique se você tem as **atualizações recebidas para outros produtos da Microsoft ao atualizar o Windows** habilitado.</span><span class="sxs-lookup"><span data-stu-id="b9061-134">Ensure you have the **Receive updates for other Microsoft products when you update Windows** enabled.</span></span> <span data-ttu-id="b9061-135">Você pode encontrá-lo em **Opções avançadas** na seção **Windows Update** do aplicativo configurações.</span><span class="sxs-lookup"><span data-stu-id="b9061-135">You can find it in **Advanced options** within the **Windows Update** section of the Settings app.</span></span> 

<span data-ttu-id="b9061-136">Para essa visualização, você precisa de uma versão de kernel do 4.19.121 ou superior.</span><span class="sxs-lookup"><span data-stu-id="b9061-136">For this preview, you need a kernel version of 4.19.121 or higher.</span></span> <span data-ttu-id="b9061-137">Você pode verificar o número de versão executando o comando a seguir no PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b9061-137">You can check the version number by running the following command in PowerShell.</span></span> 

```
wsl cat /proc/version
```

### <a name="set-up-python-environment"></a><span data-ttu-id="b9061-138">Configurar o ambiente do Python</span><span class="sxs-lookup"><span data-stu-id="b9061-138">Set up Python environment</span></span> 

<span data-ttu-id="b9061-139">É recomendável configurar um ambiente Python virtual dentro de sua instância do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="b9061-139">We recommend setting up a virtual Python environment inside your WSL 2 instance.</span></span> <span data-ttu-id="b9061-140">Há muitas ferramentas que você pode usar para configurar um ambiente virtual Python – para essas instruções, usaremos o [Miniconda da Anaconda](https://docs.conda.io/en/latest/miniconda.html).</span><span class="sxs-lookup"><span data-stu-id="b9061-140">There are many tools you can use to setup a virtual Python environment — for these instructions, we'll use [Anaconda’s Miniconda](https://docs.conda.io/en/latest/miniconda.html).</span></span> <span data-ttu-id="b9061-141">O restante dessa configuração pressupõe que você use um ambiente miniconda.</span><span class="sxs-lookup"><span data-stu-id="b9061-141">The rest of this setup assumes you use a miniconda environment.</span></span> 

<span data-ttu-id="b9061-142">Instale o Miniconda seguindo as [diretrizes no site do Anaconda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html)ou executando os comandos a seguir no WSL.</span><span class="sxs-lookup"><span data-stu-id="b9061-142">Install Miniconda by following the [guidance on Anaconda’s site](https://conda.io/projects/conda/en/latest/user-guide/install/index.html), or by running the following commands in WSL.</span></span> 

```
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh 
bash Miniconda3-latest-Linux-x86_64.sh 
```

<span data-ttu-id="b9061-143">Depois que o Miniconda for instalado no WSL, crie um ambiente usando o Python chamado "directml" e ative-o por meio dos comandos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9061-143">Once Miniconda is installed in WSL, create an environment using Python named “directml” and activate it through the following commands.</span></span> 

> [!NOTE]
> <span data-ttu-id="b9061-144">Nos comandos abaixo, usamos o Python 3,6.</span><span class="sxs-lookup"><span data-stu-id="b9061-144">In the commands below, we use Python 3.6.</span></span> <span data-ttu-id="b9061-145">No entanto, o pacote tensorflow-directml funciona em um ambiente Python 3,5, 3,6 ou 3,7.</span><span class="sxs-lookup"><span data-stu-id="b9061-145">However, the tensorflow-directml package works in a Python 3.5, 3.6 or 3.7 environment.</span></span> 

```
conda create --name directml python=3.6 

conda activate directml 
```

### <a name="install-the-tensorflow-with-directml-package"></a><span data-ttu-id="b9061-146">Instalar o Tensorflow com o pacote DirectML</span><span class="sxs-lookup"><span data-stu-id="b9061-146">Install the Tensorflow with DirectML package</span></span> 

<span data-ttu-id="b9061-147">Instale o pacote de TensorFlow com um back-end DirectML por meio de Pip executando o comando a seguir.</span><span class="sxs-lookup"><span data-stu-id="b9061-147">Install the package of TensorFlow with a DirectML backend through pip by running the following command.</span></span>

> [!NOTE]
> <span data-ttu-id="b9061-148">O pacote tensorflow-directml só dá suporte a TensorFlow 1,15.</span><span class="sxs-lookup"><span data-stu-id="b9061-148">The tensorflow-directml package only supports TensorFlow 1.15.</span></span> 

```
pip install tensorflow-directml
```

<span data-ttu-id="b9061-149">Depois de instalar o pacote tensorflow-directml, você pode verificar se ele é executado corretamente adicionando dois dezenases.</span><span class="sxs-lookup"><span data-stu-id="b9061-149">Once you’ve installed the tensorflow-directml package, you can verify that it runs correctly by adding two tensors.</span></span> <span data-ttu-id="b9061-150">Copie as linhas a seguir em uma sessão interativa do Python.</span><span class="sxs-lookup"><span data-stu-id="b9061-150">Copy the following lines into an interactive Python session.</span></span> 

```
import tensorflow.compat.v1 as tf 

tf.enable_eager_execution(tf.ConfigProto(log_device_placement=True)) 

print(tf.add([1.0, 2.0], [3.0, 4.0])) 
```

<span data-ttu-id="b9061-151">Você deverá ver uma saída semelhante à seguinte, com o operador Add colocado no dispositivo DML.</span><span class="sxs-lookup"><span data-stu-id="b9061-151">You should see output similar to the following, with the add operator placed on the DML device.</span></span> 

```
2020-06-15 11:27:18.235973: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:45] DirectML device enumeration: found 1 compatible adapters. 

2020-06-15 11:27:18.240065: I tensorflow/core/common_runtime/dml/dml_device_factory.cc:32] DirectML: creating device on adapter 0 (AMD Radeon VII) 

2020-06-15 11:27:18.323949: I tensorflow/stream_executor/platform/default/dso_loader.cc:60] Successfully opened dynamic library libdirectml.so.ba106a7c621ea741d21598708ee581c11918380 

2020-06-15 11:27:18.337830: I tensorflow/core/common_runtime/eager/execute.cc:571] Executing op Add in device /job:localhost/replica:0/task:0/device:DML:0 

tf.Tensor([4. 6.], shape=(2,), dtype=float32) 
```

## <a name="tensorflow-with-directml-samples-and-feedback"></a><span data-ttu-id="b9061-152">Tensorflow com exemplos e comentários do DirectML</span><span class="sxs-lookup"><span data-stu-id="b9061-152">Tensorflow with DirectML samples and feedback</span></span> 

<span data-ttu-id="b9061-153">Agora você está pronto para começar a aprender mais sobre o treinamento de ML.</span><span class="sxs-lookup"><span data-stu-id="b9061-153">Now you’re ready to start learning more about ML training.</span></span> <span data-ttu-id="b9061-154">Confira os [tutoriais do TensorFlow](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) ou [nossos exemplos](https://github.com/microsoft/DirectML).</span><span class="sxs-lookup"><span data-stu-id="b9061-154">Check out the [TensorFlow tutorials](https://github.com/tensorflow/docs/tree/master/site/en/r1/tutorials) or [our samples](https://github.com/microsoft/DirectML).</span></span> <span data-ttu-id="b9061-155">Usamos este conteúdo como validação para este pacote de visualização inicial de TensorFlow com DirectML.</span><span class="sxs-lookup"><span data-stu-id="b9061-155">We used this content as validation for this initial preview package of TensorFlow with DirectML.</span></span> 

<span data-ttu-id="b9061-156">Se você tiver problemas ou tiver comentários sobre o TensorFlow com o pacote DirectML, [Conecte-se à nossa equipe aqui](https://github.com/microsoft/DirectML/issues).</span><span class="sxs-lookup"><span data-stu-id="b9061-156">If you run into issues or have feedback on the TensorFlow with DirectML package, please [connect with our team here](https://github.com/microsoft/DirectML/issues).</span></span>
