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
# <a name="enable-nvidia-cuda-in-wsl-2"></a>Habilitar a NVIDIA CUDA no WSL 2

O SDK do Windows Insider dá suporte à execução de ferramentas de ML, bibliotecas e estruturas populares existentes que usam NVIDIA CUDA para aceleração de hardware de GPU dentro de uma instância do WSL 2. Isso inclui PyTorch e TensorFlow, bem como todos os suporte do Docker e do kit de ferramentas de contêiner NVIDIA disponíveis em um ambiente Linux nativo. 

> [!NOTE]
> Os recursos a seguir estão disponíveis em versões de pré-lançamento do Windows 10 e estão sujeitos a alterações.

## <a name="install-the-latest-windows-insider-dev-channel-build"></a>Instalar a compilação mais recente do canal de desenvolvimento do Windows Insider 

Para usar essa versão prévia, você precisará [se registrar para o programa Windows Insider](https://insider.windows.com/getting-started/#register). Depois de fazer isso, siga [estas instuctions](https://insider.windows.com/getting-started/#install) para instalar a compilação mais recente do insider. Ao escolher suas configurações, verifique se você está selecionando o [canal de desenvolvimento](/windows-insider/flight-hub/#active-development-builds-of-windows-10). 

Para esta versão prévia, você precisa compilar 20150 ou superior. Você pode verificar o número de versão da compilação executando `winver` por meio do comando **executar** (tecla do logotipo do Windows + R).

## <a name="install-the-preview-gpu-driver"></a>Instalar o driver de GPU de visualização 

Baixe e instale o [Driver habilitado para NVIDIA CUDA para o WSL](https://developer.nvidia.com/cuda/wsl) para usar com seus fluxos de trabalho existentes do ml CUDA. 

## <a name="set-up-wsl-2-for-the-preview"></a>Configurar o WSL 2 para a versão prévia 

Depois de instalar o driver acima, verifique se você [habilitou o WSL 2](/windows/wsl/install-win10) e [Instale uma distribuição baseada em glibc](/windows/wsl/install-win10#install-your-linux-distribution-of-choice) (como Ubuntu ou Debian). Verifique se você tem o kernel mais recente selecionando **verificar atualizações** na seção **Windows Update** do aplicativo configurações. 

> [!NOTE]
> Verifique se você **recebeu atualizações para outros produtos da Microsoft ao atualizar o Windows** habilitado. Você pode encontrá-lo em **Opções avançadas** na seção **Windows Update** do aplicativo configurações. 

Para essa visualização, você precisa de uma versão de kernel do 4.19.121 ou superior. Você pode verificar o número de versão executando o comando a seguir no PowerShell. 

```powershell
wsl cat /proc/version
```

Agora você pode começar a usar seus fluxos de trabalho do Linux existentes por meio do [Docker NVIDIA](https://github.com/NVIDIA/nvidia-docker)ou instalando [PyTorch](https://pytorch.org/get-started/locally/) ou [TensorFlow](https://www.tensorflow.org/install/gpu) dentro do WSL 2. Mais informações sobre como obter a configuração são capturadas no [Guia do usuário do CUDA no WSL da NVIDIA](https://docs.nvidia.com/cuda/wsl-user-guide/index.html).

Compartilhe comentários sobre o suporte da NVIDIA por meio de seu [Fórum da Comunidade para CUDA em WSL](https://forums.developer.nvidia.com/c/accelerated-computing/cuda/cuda-on-windows-subsystem-for-linux-wsl-2/303).
