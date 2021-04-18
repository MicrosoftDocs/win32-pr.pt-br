---
description: Seu app pode usar o buffer de estêncil para compor imagens 2D ou 3D em uma cena 3D.
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: Composição (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bca61559d2773bd1e4f7dc345e9ad4c1fb6fcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807157"
---
# <a name="compositing-direct3d-9"></a><span data-ttu-id="a75e6-103">Composição (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a75e6-103">Compositing (Direct3D 9)</span></span>

<span data-ttu-id="a75e6-104">Seu app pode usar o buffer de estêncil para compor imagens 2D ou 3D em uma cena 3D.</span><span class="sxs-lookup"><span data-stu-id="a75e6-104">Your application can use the stencil buffer to composite 2D or 3D images onto a 3D scene.</span></span> <span data-ttu-id="a75e6-105">Uma máscara no buffer de estêncil é usada para ocultar uma área da superfície de destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="a75e6-105">A mask in the stencil buffer is used to occlude an area of the rendering target surface.</span></span> <span data-ttu-id="a75e6-106">Informações armazenadas 2D, como texto ou bitmaps, podem então ser escritas na área obstruída.</span><span class="sxs-lookup"><span data-stu-id="a75e6-106">Stored 2D information, such as text or bitmaps, can then be written to the occluded area.</span></span> <span data-ttu-id="a75e6-107">Como alternativa, seu app pode renderizar objetos primitivos 3D adicionais para a região mascarada por estêncil da superfície do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="a75e6-107">Alternately, your application can render additional 3D primitives to the stencil-masked region of the rendering target surface.</span></span> <span data-ttu-id="a75e6-108">Ele pode até mesmo renderizar uma cena inteira.</span><span class="sxs-lookup"><span data-stu-id="a75e6-108">It can even render an entire scene.</span></span>

<span data-ttu-id="a75e6-109">Jogos geralmente são compostos por diversas cenas 3D juntas.</span><span class="sxs-lookup"><span data-stu-id="a75e6-109">Games often composite multiple 3D scenes together.</span></span> <span data-ttu-id="a75e6-110">Por exemplo, jogos de direção normalmente exibem um espelho retrovisor.</span><span class="sxs-lookup"><span data-stu-id="a75e6-110">For instance, driving games typically display a rear-view mirror.</span></span> <span data-ttu-id="a75e6-111">O espelho contém o modo de exibição da cena 3D atrás do condutor.</span><span class="sxs-lookup"><span data-stu-id="a75e6-111">The mirror contains the view of the 3D scene behind the driver.</span></span> <span data-ttu-id="a75e6-112">Ele é essencialmente uma segunda cena 3D composta pela visão frontal do condutor.</span><span class="sxs-lookup"><span data-stu-id="a75e6-112">It is essentially a second 3D scene composited with the driver's forward view.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a75e6-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a75e6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a75e6-114">Técnicas de buffer de estêncil</span><span class="sxs-lookup"><span data-stu-id="a75e6-114">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



