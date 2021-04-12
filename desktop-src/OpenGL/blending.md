---
title: Mesclagem
description: A mesclagem combina os valores R, G, B e A dos fragmentos com aqueles armazenados no framebuffer no local correspondente.
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- Pipeline de processamento OpenGL, mesclagem
- combinação de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0fe7cd2893700d8015148fcc5c25707d19676c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292174"
---
# <a name="blending"></a><span data-ttu-id="8f414-105">Mesclagem</span><span class="sxs-lookup"><span data-stu-id="8f414-105">Blending</span></span>

<span data-ttu-id="8f414-106">A mesclagem combina os valores R, G, B e A dos fragmentos com aqueles armazenados no framebuffer no local correspondente.</span><span class="sxs-lookup"><span data-stu-id="8f414-106">Blending combines a fragment's R, G, B, and A values with those stored in the framebuffer at the corresponding location.</span></span> <span data-ttu-id="8f414-107">A mesclagem, que é executada somente no modo RGBA, depende do valor alfa do fragmento e do pixel armazenado atualmente correspondente; Ele também pode depender dos valores RGB.</span><span class="sxs-lookup"><span data-stu-id="8f414-107">The blending, which is performed only in RGBA mode, depends on the alpha value of the fragment and that of the corresponding currently stored pixel; it may also depend on the RGB values.</span></span> <span data-ttu-id="8f414-108">Você controla a mesclagem com o [**glBlendFunc**](glblendfunc.md), com o qual você indica os fatores de mesclagem de origem e destino.</span><span class="sxs-lookup"><span data-stu-id="8f414-108">You control blending with [**glBlendFunc**](glblendfunc.md), with which you indicate the source and destination blending factors.</span></span>

 

 




