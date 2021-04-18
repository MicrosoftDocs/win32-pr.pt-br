---
title: Aceleração de GPU no WSL
description: O Direct Machine Learning (DirectML) alimenta a GPU-accelleration no subsistema do Windows para Linux
ms.topic: article
ms.date: 06/17/2020
ms.openlocfilehash: 217a1763c0030a856e10a822cbd9f2642480c056
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105792891"
---
# <a name="gpu-accelerated-ml-training"></a><span data-ttu-id="8ce89-103">Treinamento de ML acelerado por GPU</span><span class="sxs-lookup"><span data-stu-id="8ce89-103">GPU accelerated ML training</span></span>

![Gráfico do Windows ML](images/winml-graphic.png)

<span data-ttu-id="8ce89-105">Esta documentação aborda o que atualmente tem suporte na visualização de treinamento do ML (aprendizado de máquina acelerada por GPU) para o [subsistema do Windows para Linux](/windows/wsl/about) (WSL) e o Windows nativo.</span><span class="sxs-lookup"><span data-stu-id="8ce89-105">This documentation covers what is currently supported by the GPU accelerated machine learning (ML) training preview for the [Windows Subsystem for Linux](/windows/wsl/about) (WSL) and native Windows.</span></span>  

<span data-ttu-id="8ce89-106">Essa versão prévia dá suporte a cenários profissionais e iniciantes.</span><span class="sxs-lookup"><span data-stu-id="8ce89-106">This preview supports both professional and beginner scenarios.</span></span> <span data-ttu-id="8ce89-107">Abaixo você encontrará ponteiros para guias passo a passo sobre como obter a configuração do sistema dependendo do seu nível de experiência em ML, fornecedor de GPU e a biblioteca de software que você pretende usar.</span><span class="sxs-lookup"><span data-stu-id="8ce89-107">Below you will find pointers to step-by-step guides on how to get your system setup depending on your level of expertise in ML, GPU vendor, and the software library you intend to use.</span></span> 

> [!NOTE]
> <span data-ttu-id="8ce89-108">Os recursos a seguir estão em versão prévia e estão sujeitos a alterações.</span><span class="sxs-lookup"><span data-stu-id="8ce89-108">The following features are in preview, and are subject to change.</span></span>


## <a name="professionals"></a><span data-ttu-id="8ce89-109">Alista</span><span class="sxs-lookup"><span data-stu-id="8ce89-109">Professionals</span></span>

<span data-ttu-id="8ce89-110">Se você for um cientista de dados profissional que usa um ambiente Linux nativo de desenvolvimento e experimentação de ML de loop interno e tiver uma GPU NVIDIA, é recomendável configurar a [Visualização NVIDIA CUDA no WSL 2.](gpu-cuda-in-wsl.md)</span><span class="sxs-lookup"><span data-stu-id="8ce89-110">If you’re a professional data scientist that uses a native Linux environment day-to-day for inner-loop ML development and experimentation, and you have an NVIDIA GPU, we recommend setting up the [NVIDIA CUDA preview in WSL 2.](gpu-cuda-in-wsl.md)</span></span>

## <a name="students-and-beginners"></a><span data-ttu-id="8ce89-111">Estudantes e iniciantes</span><span class="sxs-lookup"><span data-stu-id="8ce89-111">Students and beginners</span></span> 

<span data-ttu-id="8ce89-112">Se você for um aluno ou iniciante procurando começar a criar seu conhecimento no espaço ML, recomendamos configurar o TensorFlow com o pacote de back-end DirectML.</span><span class="sxs-lookup"><span data-stu-id="8ce89-112">If you’re a student or beginner looking to start building your knowledge in the ML space, we recommend setting up the TensorFlow with DirectML backend package.</span></span> <span data-ttu-id="8ce89-113">Esse pacote atualmente acelera fluxos de trabalho em GPUs AMD e Intel.</span><span class="sxs-lookup"><span data-stu-id="8ce89-113">This package currently accelerates workflows on AMD and Intel GPUs.</span></span> <span data-ttu-id="8ce89-114">O suporte para GPUs NVIDIA estará disponível em breve.</span><span class="sxs-lookup"><span data-stu-id="8ce89-114">Support for NVIDIA GPUs is coming soon.</span></span> 

<span data-ttu-id="8ce89-115">Para aqueles mais familiarizados com um ambiente Linux nativo que estão começando com fluxos de trabalho ML, recomendamos executar o [TensorFlow com o pacote DirectML dentro do WSL 2](gpu-tensorflow-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="8ce89-115">For those more familiar with a native Linux environment that are getting started with ML workflows, we recommend running the [TensorFlow with DirectML package inside WSL 2](gpu-tensorflow-wsl.md).</span></span> 

<span data-ttu-id="8ce89-116">Para aqueles mais familiarizados com o Windows que estão começando com fluxos de trabalho ML, é recomendável configurar o [TensorFlow com o pacote DirectML no Windows nativo](gpu-tensorflow-windows.md).</span><span class="sxs-lookup"><span data-stu-id="8ce89-116">For those more familiar with Windows that are getting started with ML workflows, we recommend setting up the [TensorFlow with DirectML package on native Windows](gpu-tensorflow-windows.md).</span></span> 

## <a name="next-steps"></a><span data-ttu-id="8ce89-117">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="8ce89-117">Next steps</span></span>

* <span data-ttu-id="8ce89-118">[Habilite a visualização NVIDIA CUDA no WSL 2](gpu-cuda-in-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="8ce89-118">[Enable NVIDIA CUDA preview in WSL 2](gpu-cuda-in-wsl.md).</span></span>
* <span data-ttu-id="8ce89-119">[Habilite o TensorFlow com o pacote DirectML dentro do WSL 2](gpu-tensorflow-wsl.md).</span><span class="sxs-lookup"><span data-stu-id="8ce89-119">[Enable TensorFlow with DirectML package inside WSL 2](gpu-tensorflow-wsl.md).</span></span>
* <span data-ttu-id="8ce89-120">[Habilite o TensorFlow com o pacote DirectML no Windows nativo](gpu-tensorflow-windows.md).</span><span class="sxs-lookup"><span data-stu-id="8ce89-120">[Enable TensorFlow with DirectML package on native Windows](gpu-tensorflow-windows.md).</span></span>