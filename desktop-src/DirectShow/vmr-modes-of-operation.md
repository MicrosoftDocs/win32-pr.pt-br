---
description: Modos de operação do VMR
ms.assetid: 98244af1-5934-4d1c-b9c3-7a414b065fe7
title: Modos de operação do VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43427c4119bb912d2bc2cf92b1c740b1d22e1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757566"
---
# <a name="vmr-modes-of-operation"></a><span data-ttu-id="eb8cd-103">Modos de operação do VMR</span><span class="sxs-lookup"><span data-stu-id="eb8cd-103">VMR Modes of Operation</span></span>

<span data-ttu-id="eb8cd-104">A arquitetura do componente do VMR permite que os aplicativos o configurem de várias maneiras, dependendo de como a renderização deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-104">The component architecture of the VMR enables applications to configure it in various ways, depending on how rendering is to be performed.</span></span> <span data-ttu-id="eb8cd-105">A tabela a seguir mostra os três modos de apresentação e os dois modos de combinação e os componentes que estão presentes para cada configuração.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-105">The following table shows the three presentation modes and the two mixing modes, and the components that are present for each configuration.</span></span>



| <span data-ttu-id="eb8cd-106">Mode</span><span class="sxs-lookup"><span data-stu-id="eb8cd-106">Mode</span></span>       | <span data-ttu-id="eb8cd-107">Fluxo único</span><span class="sxs-lookup"><span data-stu-id="eb8cd-107">Single Stream</span></span>                                                                     | <span data-ttu-id="eb8cd-108">Vários fluxos (modo de combinação)</span><span class="sxs-lookup"><span data-stu-id="eb8cd-108">Multiple Streams (Mixing Mode)</span></span>                                                                                             |
|------------|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb8cd-109">Em janelas</span><span class="sxs-lookup"><span data-stu-id="eb8cd-109">Windowed</span></span>   | <span data-ttu-id="eb8cd-110">Alocador-unidade de sincronização presenterCore</span><span class="sxs-lookup"><span data-stu-id="eb8cd-110">Allocator-presenterCore Synchronization Unit</span></span><br/> <span data-ttu-id="eb8cd-111">Gerenciador de janelas</span><span class="sxs-lookup"><span data-stu-id="eb8cd-111">Window Manager</span></span><br/> | <span data-ttu-id="eb8cd-112">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="eb8cd-112">MixerCompositor\*</span></span><br/> <span data-ttu-id="eb8cd-113">Alocador-apresentador</span><span class="sxs-lookup"><span data-stu-id="eb8cd-113">Allocator-presenter</span></span><br/> <span data-ttu-id="eb8cd-114">Unidade de sincronização principal</span><span class="sxs-lookup"><span data-stu-id="eb8cd-114">Core Synchronization Unit</span></span><br/> <span data-ttu-id="eb8cd-115">Gerenciador de janelas</span><span class="sxs-lookup"><span data-stu-id="eb8cd-115">Window Manager</span></span><br/> |
| <span data-ttu-id="eb8cd-116">Sem janelas</span><span class="sxs-lookup"><span data-stu-id="eb8cd-116">Windowless</span></span> | <span data-ttu-id="eb8cd-117">Alocador-unidade de sincronização presenterCore</span><span class="sxs-lookup"><span data-stu-id="eb8cd-117">Allocator-presenterCore Synchronization Unit</span></span><br/>                           | <span data-ttu-id="eb8cd-118">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="eb8cd-118">MixerCompositor\*</span></span><br/> <span data-ttu-id="eb8cd-119">Alocador-apresentador</span><span class="sxs-lookup"><span data-stu-id="eb8cd-119">Allocator-presenter</span></span><br/> <span data-ttu-id="eb8cd-120">Unidade de sincronização principal</span><span class="sxs-lookup"><span data-stu-id="eb8cd-120">Core Synchronization Unit</span></span><br/>                           |
| <span data-ttu-id="eb8cd-121">Com renderização</span><span class="sxs-lookup"><span data-stu-id="eb8cd-121">Renderless</span></span> | <span data-ttu-id="eb8cd-122">Unidade de sincronização de núcleo de alocador (fornecido pela aplicação)</span><span class="sxs-lookup"><span data-stu-id="eb8cd-122">Allocator-presenter (provided by application)Core Synchronization Unit</span></span><br/> | <span data-ttu-id="eb8cd-123">MixerCompositor\*</span><span class="sxs-lookup"><span data-stu-id="eb8cd-123">MixerCompositor\*</span></span><br/> <span data-ttu-id="eb8cd-124">Alocador-Presenter (fornecido pelo aplicativo)</span><span class="sxs-lookup"><span data-stu-id="eb8cd-124">Allocator-presenter (provided by application)</span></span><br/> <span data-ttu-id="eb8cd-125">Unidade de sincronização principal</span><span class="sxs-lookup"><span data-stu-id="eb8cd-125">Core Synchronization Unit</span></span><br/> |



 

<span data-ttu-id="eb8cd-126">\* Indica que o aplicativo tem a opção de fornecer um componente personalizado ou usar o componente padrão.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-126">\* Indicates that the application has the option to provide a custom component or use the default component.</span></span>

<span data-ttu-id="eb8cd-127">Em todas as configurações, o ponto principal a ser lembrado quando você cria gráficos de filtro com o VMR é que você deve configurar o VMR antes de conectá-lo.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-127">In all configurations, the main point to remember when you create filter graphs with the VMR is that you must configure the VMR before you connect it.</span></span>

<span data-ttu-id="eb8cd-128">Para todas as configurações, os Pins não podem ser adicionados ou removidos dinamicamente depois que o VMR está conectado ao filtro upstream, mas eles podem ser conectados e desconectados.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-128">For all configurations, pins cannot be dynamically added or removed after the VMR is connected to the upstream filter, but they can be connected and disconnected.</span></span> <span data-ttu-id="eb8cd-129">Se o aplicativo não tiver certeza de quantos Pins serão necessários, ele deverá configurar o VMR para o número máximo que pode ser necessário.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-129">If the application is unsure how many pins will be needed, it should configure the VMR for the maximum number that might be needed.</span></span> <span data-ttu-id="eb8cd-130">A presença de Pins de entrada não utilizados no filtro não degrada o desempenho de renderização.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-130">The presence of unused input pins on the filter does not degrade rendering performance.</span></span> <span data-ttu-id="eb8cd-131">Ao contrário do mixer de sobreposição antigo, o VMR não tem nenhum pino de saída porque não requer um filtro separado para o gerenciamento de janelas.</span><span class="sxs-lookup"><span data-stu-id="eb8cd-131">Unlike the old Overlay Mixer, the VMR has no output pin because it does not require a separate filter for window management.</span></span>

<span data-ttu-id="eb8cd-132">As seções a seguir descrevem como configurar o VMR para um determinado modo:</span><span class="sxs-lookup"><span data-stu-id="eb8cd-132">The following sections describe how to configure the VMR for a given mode:</span></span>

-   [<span data-ttu-id="eb8cd-133">Modo de janela do VMR (compatibilidade)</span><span class="sxs-lookup"><span data-stu-id="eb8cd-133">VMR Windowed (Compatibility) Mode</span></span>](vmr-windowed--compatibility--mode.md)
-   [<span data-ttu-id="eb8cd-134">Modo sem janela do VMR</span><span class="sxs-lookup"><span data-stu-id="eb8cd-134">VMR Windowless Mode</span></span>](vmr-windowless-mode.md)
-   [<span data-ttu-id="eb8cd-135">VMR com vários fluxos (modo de combinação)</span><span class="sxs-lookup"><span data-stu-id="eb8cd-135">VMR with Multiple Streams (Mixing Mode)</span></span>](vmr-with-multiple-streams--mixing-mode.md)
-   [<span data-ttu-id="eb8cd-136">Modo de mixagem YUV</span><span class="sxs-lookup"><span data-stu-id="eb8cd-136">YUV Mixing Mode</span></span>](yuv-mixing-mode.md)
-   [<span data-ttu-id="eb8cd-137">Posicionando e movendo os retângulos de vídeo no espaço de composição</span><span class="sxs-lookup"><span data-stu-id="eb8cd-137">Positioning and Moving Video Rectangles in Composition Space</span></span>](positioning-and-moving-video-rectangles-in-composition-space.md)
-   [<span data-ttu-id="eb8cd-138">Modo de reprodução do VMR (alocador personalizado-apresentadores)</span><span class="sxs-lookup"><span data-stu-id="eb8cd-138">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>](vmr-renderless-playback-mode--custom-allocator-presenters.md)
-   [<span data-ttu-id="eb8cd-139">Modo exclusivo do DirectDraw</span><span class="sxs-lookup"><span data-stu-id="eb8cd-139">DirectDraw Exclusive Mode</span></span>](directdraw-exclusive-mode.md)

 

 




