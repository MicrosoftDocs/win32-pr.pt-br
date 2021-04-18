---
title: Habilitar a NVIDIA CUDA no WSL 2
description: Habilitar o NVIDIA CUDA Preview no subsistema do Windows para Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: ea5b460d4b4c71417f8ac9969f58bcebf6d10af9
ms.sourcegitcommit: 85acfd5afdcd30c81e3d2b375e813957f9830e9f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/03/2020
ms.locfileid: "105773935"
---
# <a name="enable-nvidia-cuda-in-wsl-2"></a><span data-ttu-id="ce2c0-103">Habilitar a NVIDIA CUDA no WSL 2</span><span class="sxs-lookup"><span data-stu-id="ce2c0-103">Enable NVIDIA CUDA in WSL 2</span></span>

<span data-ttu-id="ce2c0-104">O SDK do Windows Insider dá suporte à execução de ferramentas de ML, bibliotecas e estruturas populares existentes que usam NVIDIA CUDA para aceleração de hardware de GPU dentro de uma instância do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="ce2c0-104">The Windows Insider SDK supports running existing ML tools, libraries, and popular frameworks that use NVIDIA CUDA for GPU hardware acceleration inside a WSL 2 instance.</span></span> <span data-ttu-id="ce2c0-105">Isso inclui PyTorch e TensorFlow, bem como todos os suporte do Docker e do kit de ferramentas de contêiner NVIDIA disponíveis em um ambiente Linux nativo.</span><span class="sxs-lookup"><span data-stu-id="ce2c0-105">This includes PyTorch and TensorFlow as well as all the Docker and NVIDIA Container Toolkit support available in a native Linux environment.</span></span> 

> [!NOTE]
> <span data-ttu-id="ce2c0-106">Os recursos a seguir estão disponíveis em versões de pré-lançamento do Windows 10 e estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="ce2c0-106">The following features are available in prerelease versions of Windows 10, and are subject to change.</span></span>

## <a name="install-the-latest-windows-insider-dev-channel-build"></a><span data-ttu-id="ce2c0-107">Instalar a compilação mais recente do canal de desenvolvimento do Windows Insider</span><span class="sxs-lookup"><span data-stu-id="ce2c0-107">Install the latest Windows Insider Dev Channel build</span></span> 

<span data-ttu-id="ce2c0-108">Para usar essa versão prévia, você precisará [se registrar para o programa Windows Insider](https://insider.windows.com/getting-started/#register).</span><span class="sxs-lookup"><span data-stu-id="ce2c0-108">To use this preview, you'll need to [register for the Windows Insider Program](https://insider.windows.com/getting-started/#register).</span></span> <span data-ttu-id="ce2c0-109">Depois de fazer isso, siga [estas instuctions](https://insider.windows.com/getting-started/#install) para instalar a compilação mais recente do insider.</span><span class="sxs-lookup"><span data-stu-id="ce2c0-109">Once you do, follow [these instuctions](https://insider.windows.com/getting-started/#install) to install the latest Insider build.</span></span> <span data-ttu-id="ce2c0-110">Ao escolher suas configurações, verifique se você está selecionando o [canal de desenvolvimento](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span><span class="sxs-lookup"><span data-stu-id="ce2c0-110">When choosing your settings, ensure you're selecting the [Dev Channel](/windows-insider/flight-hub/#active-development-builds-of-windows-10).</span></span> 

<span data-ttu-id="ce2c0-111">Para esta versão prévia, você precisa compilar 20150 ou superior.</span><span class="sxs-lookup"><span data-stu-id="ce2c0-111">For this preview, you need Build 20150 or higher.</span></span> <span data-ttu-id="ce2c0-112">Você pode verificar o número de versão da compilação executando `winver` por meio do comando **executar** (tecla do logotipo do Windows + R).</span><span class="sxs-lookup"><span data-stu-id="ce2c0-112">You can check your build version number by running `winver` via the **Run** command (Windows logo key + R).</span></span>

## <a name="install-the-preview-gpu-driver"></a><span data-ttu-id="ce2c0-113">Instalar o driver de GPU de visualização</span><span class="sxs-lookup"><span data-stu-id="ce2c0-113">Install the preview GPU driver</span></span> 

<span data-ttu-id="ce2c0-114">Baixe e instale o [Driver habilitado para NVIDIA CUDA para o WSL](https://developer.nvidia.com/cuda/wsl) para usar com seus fluxos de trabalho existentes do ml CUDA.</span><span class="sxs-lookup"><span data-stu-id="ce2c0-114">Download and install the [NVIDIA CUDA-enabled driver for WSL](https://developer.nvidia.com/cuda/wsl) to use with your existing CUDA ML workflows.</span></span> 

## <a name="set-up-wsl-2-for-the-preview"></a><span data-ttu-id="ce2c0-115">Configurar o WSL 2 para a versão prévia</span><span class="sxs-lookup"><span data-stu-id="ce2c0-115">Set up WSL 2 for the preview</span></span> 

<span data-ttu-id="ce2c0-116">Depois de instalar o driver acima, verifique se você [habilitou o WSL 2](/windows/wsl/install-win10) e [Instale uma distribuição baseada em glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (como Ubuntu ou Debian).</span><span class="sxs-lookup"><span data-stu-id="ce2c0-116">Once you've installed the above driver, ensure you [enable WSL 2](/windows/wsl/install-win10) and [install a glibc-based distribution](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (such as Ubuntu or Debian).</span></span> <span data-ttu-id="ce2c0-117">Verifique se você tem o kernel mais recente selecionando **verificar atualizações** na seção **Windows Update** do aplicativo configurações.</span><span class="sxs-lookup"><span data-stu-id="ce2c0-117">Ensure you have the latest kernel by selecting **Check for updates** in the **Windows Update** section of the Settings app.</span></span> 

> [!NOTE]
> <span data-ttu-id="ce2c0-118">Verifique se você **recebeu atualizações para outros produtos da Microsoft ao atualizar o Windows** habilitado.</span><span class="sxs-lookup"><span data-stu-id="ce2c0-118">Ensure you have **Receive updates for other Microsoft products when you update Windows** enabled.</span></span> <span data-ttu-id="ce2c0-119">Você pode encontrá-lo em **Opções avançadas** na seção **Windows Update** do aplicativo configurações.</span><span class="sxs-lookup"><span data-stu-id="ce2c0-119">You can find it in **Advanced options** within the **Windows Update** section of the Settings app.</span></span> 

<span data-ttu-id="ce2c0-120">Para essa visualização, você precisa de uma versão de kernel do 4.19.121 ou superior.</span><span class="sxs-lookup"><span data-stu-id="ce2c0-120">For this preview, you need a kernel version of 4.19.121 or higher.</span></span> <span data-ttu-id="ce2c0-121">Você pode verificar o número de versão executando o comando a seguir no PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ce2c0-121">You can check the version number by running the following command in PowerShell.</span></span> 

```powershell
wsl cat /proc/version
```

<span data-ttu-id="ce2c0-122">Agora você pode começar a usar seus fluxos de trabalho do Linux existentes por meio do [Docker NVIDIA](https://github.com/NVIDIA/nvidia-docker)ou instalando [PyTorch](https://pytorch.org/get-started/locally/) ou [TensorFlow](https://www.tensorflow.org/install/gpu) dentro do WSL 2.</span><span class="sxs-lookup"><span data-stu-id="ce2c0-122">Now you can start using your exisiting Linux workflows through [NVIDIA Docker](https://github.com/NVIDIA/nvidia-docker), or by installing [PyTorch](https://pytorch.org/get-started/locally/) or [TensorFlow](https://www.tensorflow.org/install/gpu) inside WSL 2.</span></span> <span data-ttu-id="ce2c0-123">Mais informações sobre como obter a configuração são capturadas no [Guia do usuário do CUDA no WSL da NVIDIA](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).</span><span class="sxs-lookup"><span data-stu-id="ce2c0-123">More information on getting set up is captured in [NVIDIA's CUDA on WSL User Guide](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).</span></span>

<span data-ttu-id="ce2c0-124">Compartilhe comentários sobre o suporte da NVIDIA por meio de seu [Fórum da Comunidade para CUDA em WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).</span><span class="sxs-lookup"><span data-stu-id="ce2c0-124">Share feedback on NVIDIA's support via their [Community forum for CUDA on WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).</span></span>
