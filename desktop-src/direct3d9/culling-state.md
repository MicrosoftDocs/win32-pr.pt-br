---
description: Para melhorar o desempenho de renderização, você pode excluir (ou remover) um primitivo que se rostos da câmera.
ms.assetid: b4b8ff3f-aa20-4422-8f6f-34cae25de0e6
title: Estado de remoção (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86e71fd7c6543f0d232e32a630d73e0ebbadae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089359"
---
# <a name="culling-state-direct3d-9"></a><span data-ttu-id="a659e-103">Estado de remoção (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a659e-103">Culling State (Direct3D 9)</span></span>

<span data-ttu-id="a659e-104">Para melhorar o desempenho de renderização, você pode excluir (ou remover) um primitivo que se rostos da câmera.</span><span class="sxs-lookup"><span data-stu-id="a659e-104">To improve rendering performance, you can cull out (or remove) a primitive that faces away from the camera.</span></span> <span data-ttu-id="a659e-105">Para primitivos de um único lado, isso economiza tempo de renderização porque um back-face não está visível.</span><span class="sxs-lookup"><span data-stu-id="a659e-105">For single-sided primitives, this saves rendering time because a back-face is not visible.</span></span> <span data-ttu-id="a659e-106">Para habilitar a remoção, você precisa saber a ordem de contorno dos vértices (normalmente no sentido anti-horário).</span><span class="sxs-lookup"><span data-stu-id="a659e-106">To enable culling, you need to know the winding order of the vertices (typically counter-clockwise).</span></span> <span data-ttu-id="a659e-107">Este exemplo removerá qualquer primitiva cuja face de fundo esteja voltada para frente (dada uma ordem de enrolamento no sentido anti-horário):</span><span class="sxs-lookup"><span data-stu-id="a659e-107">This example will remove any primitive whose back face is facing forward (given a counter-clockwise winding order):</span></span>


```
SetRenderState(D3DRS_CULLMODE, D3DCULL_CCW);
```



## <a name="related-topics"></a><span data-ttu-id="a659e-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a659e-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a659e-109">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="a659e-109">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



