---
title: Copiando um CD
description: Copiando um CD
ms.assetid: f5c1b5bf-d616-48cb-8690-e0237c56e402
keywords:
- Windows Media Player, CD de CDs
- Modelo de objeto do Windows Media Player, cópia de CD
- modelo de objeto, cópia de CD
- Controle ActiveX do Windows Media Player, cópia de CD
- Controle ActiveX, cópia de CD
- Controle ActiveX móvel do Windows Media Player, cópia de CD
- Windows Media Player Mobile, CD-CDs
- CD de CDs, sobre
- copiando CDs, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767734b3449fd0a64b31c8f351406bbf9f6c805b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822846"
---
# <a name="ripping-a-cd"></a><span data-ttu-id="92b96-112">Copiando um CD</span><span class="sxs-lookup"><span data-stu-id="92b96-112">Ripping a CD</span></span>

<span data-ttu-id="92b96-113">Há duas maneiras de copiar um CD usando o controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="92b96-113">There are two ways to rip a CD by using the Windows Media Player control.</span></span> <span data-ttu-id="92b96-114">O Windows Media Player 9 pode copiar CDs usando **IWMPPlayerServices:: setTaskPane**.</span><span class="sxs-lookup"><span data-stu-id="92b96-114">Windows Media Player 9 can rip CDs by using **IWMPPlayerServices::setTaskPane**.</span></span> <span data-ttu-id="92b96-115">O Windows Media Player 11 apresenta a interface **IWMPCdromRip** para copiar CDs.</span><span class="sxs-lookup"><span data-stu-id="92b96-115">Windows Media Player 11 introduces the **IWMPCdromRip** interface for ripping CDs.</span></span> <span data-ttu-id="92b96-116">Essa interface fornece mais funcionalidade do que **IWMPPlayerServices:: setTaskPane**, e é recomendável que você use o **IWMPCdromRip** se ele estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="92b96-116">This interface provides more functionality than **IWMPPlayerServices::setTaskPane**, and it is recommended that you use **IWMPCdromRip** if it is available.</span></span>

<span data-ttu-id="92b96-117">As seções a seguir descrevem como copiar um CD usando o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="92b96-117">The following sections describe how to rip a CD by using Windows Media Player.</span></span>

-   [<span data-ttu-id="92b96-118">Copiando usando a interface IWMPCdromRip</span><span class="sxs-lookup"><span data-stu-id="92b96-118">Ripping by Using the IWMPCdromRip Interface</span></span>](ripping-by-using-the-iwmpcdromrip-interface.md)
-   [<span data-ttu-id="92b96-119">Copiando por meio de IWMPPlayerServices:: setTaskPane</span><span class="sxs-lookup"><span data-stu-id="92b96-119">Ripping by Using IWMPPlayerServices::setTaskPane</span></span>](ripping-by-using-iwmpplayerservices--settaskpane.md)

## <a name="related-topics"></a><span data-ttu-id="92b96-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="92b96-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="92b96-121">**Guia de controle do Player**</span><span class="sxs-lookup"><span data-stu-id="92b96-121">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




