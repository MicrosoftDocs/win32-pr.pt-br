---
title: Visão geral do eco de exemplo
description: Visão geral do eco de exemplo
ms.assetid: df9ad8f4-8c17-44b8-b5ee-c86de44788cf
keywords:
- Plug-ins do Windows Media Player, visão geral do eco de exemplo
- plug-ins, visão geral do eco de exemplo
- plug-ins de processamento de sinal digital, visão geral do eco de exemplo
- Plug-ins do DSP, visão geral do eco de exemplo
- Exemplo de plug-in do eco DSP, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1081b6d54ce34581bb6231d5617dd300e392ad71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811117"
---
# <a name="echo-sample-overview"></a><span data-ttu-id="ddf46-108">Visão geral do eco de exemplo</span><span class="sxs-lookup"><span data-stu-id="ddf46-108">Echo Sample Overview</span></span>

<span data-ttu-id="ddf46-109">Este guia cria um plug-in de DSP do Windows Media Player que cria um efeito de eco no áudio PCM durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="ddf46-109">This guide builds a Windows Media Player DSP plug-in that creates an echo effect in PCM audio during playback.</span></span> <span data-ttu-id="ddf46-110">As metas para o plug-in são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="ddf46-110">The goals for the plug-in are as follows:</span></span>

-   <span data-ttu-id="ddf46-111">O plug-in processa apenas áudio PCM de 8 ou 16 bits.</span><span class="sxs-lookup"><span data-stu-id="ddf46-111">The plug-in processes 8-bit or 16-bit PCM audio only.</span></span>
-   <span data-ttu-id="ddf46-112">Ele dá suporte a um tempo de atraso entre 10 milissegundos (MS) e 2000 MS (2 segundos).</span><span class="sxs-lookup"><span data-stu-id="ddf46-112">It supports a delay time between 10 milliseconds (ms) and 2000 ms (2 seconds).</span></span> <span data-ttu-id="ddf46-113">Isso representa um intervalo prático para a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="ddf46-113">This represents a practical range for most applications.</span></span>
-   <span data-ttu-id="ddf46-114">Ele dá suporte à combinação do sinal original com o sinal de atraso.</span><span class="sxs-lookup"><span data-stu-id="ddf46-114">It supports mixing of the original signal with the delay signal.</span></span>
-   <span data-ttu-id="ddf46-115">Ele fornece uma implementação de página de propriedades que permite ao usuário fornecer um valor para o tempo de atraso e um valor para a porcentagem de sinal de atraso em relação ao nível de sinal de áudio geral.</span><span class="sxs-lookup"><span data-stu-id="ddf46-115">It provides a property page implementation that allows the user to provide a value for the delay time and a value for the percentage of delay signal relative to the overall audio signal level.</span></span>
-   <span data-ttu-id="ddf46-116">O código é criado modificando o exemplo de plug-in do assistente de plug-in do DSP do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ddf46-116">The code is created by modifying the Windows Media Player Plug-in Wizard audio DSP plug-in sample.</span></span>

<span data-ttu-id="ddf46-117">O exemplo de eco não está incluído no SDK do Windows Media Player; é um exemplo que você cria.</span><span class="sxs-lookup"><span data-stu-id="ddf46-117">The Echo sample is not included with the Windows Media Player SDK; it is a sample that you create.</span></span> <span data-ttu-id="ddf46-118">Para criar o exemplo de eco, você deve começar com o projeto padrão do assistente de plug-in do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ddf46-118">To create the Echo sample, you must start with the default project from the Windows Media Player Plug-in Wizard.</span></span> <span data-ttu-id="ddf46-119">Você pode nomear o projeto como desejar; Esta documentação pressupõe que o projeto é denominado Echo.</span><span class="sxs-lookup"><span data-stu-id="ddf46-119">You can name the project whatever you like; this documentation assumes the project is named Echo.</span></span> <span data-ttu-id="ddf46-120">Para obter detalhes sobre como usar o assistente, consulte [criando um plug-in do DSP](building-a-dsp-plug-in.md).</span><span class="sxs-lookup"><span data-stu-id="ddf46-120">For details about using the wizard, see [Building a DSP Plug-in](building-a-dsp-plug-in.md).</span></span>

<span data-ttu-id="ddf46-121">A seção a seguir fornece uma visão geral de como o exemplo cria um efeito de eco:</span><span class="sxs-lookup"><span data-stu-id="ddf46-121">The following section provides an overview of how the sample creates an echo effect:</span></span>

-   [<span data-ttu-id="ddf46-122">Como funciona o exemplo de eco</span><span class="sxs-lookup"><span data-stu-id="ddf46-122">How the Echo Sample Works</span></span>](how-the-echo-sample-works.md)

## <a name="related-topics"></a><span data-ttu-id="ddf46-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ddf46-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddf46-124">**O exemplo de eco**</span><span class="sxs-lookup"><span data-stu-id="ddf46-124">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




