---
title: Habilitando a sobreposição de vídeo
description: Habilitando a sobreposição de vídeo
ms.assetid: f0b4f24c-3e35-4a18-ac77-8cae7083b0fe
keywords:
- macro capDriverGetCaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce51a3b7c77fbb161007ddde7dfe91c36152121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636937"
---
# <a name="enabling-video-overlay"></a><span data-ttu-id="0e63a-104">Habilitando a sobreposição de vídeo</span><span class="sxs-lookup"><span data-stu-id="0e63a-104">Enabling Video Overlay</span></span>

<span data-ttu-id="0e63a-105">O exemplo a seguir usa a macro [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) para determinar se um driver de captura tem recursos de sobreposição; Se tiver, a macro permitirá a sobreposição.</span><span class="sxs-lookup"><span data-stu-id="0e63a-105">The following example uses the [**capDriverGetCaps**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetcaps) macro to determine whether a capture driver has overlay capabilities; if it does, the macro enables the overlay.</span></span>


```C++
CAPDRIVERCAPS CapDrvCaps; 

capDriverGetCaps(hWndC, &CapDrvCaps, sizeof (CAPDRIVERCAPS)); 

if (CapDrvCaps.fHasOverlay) 
    capOverlay(hWndC, TRUE);
 
```



## <a name="related-topics"></a><span data-ttu-id="0e63a-106">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e63a-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e63a-107">Usando a captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="0e63a-107">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




