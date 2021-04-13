---
description: Os primitivos que ficam parcialmente dentro (ou completamente fora) da exibição frustum podem ser recortados para que apenas a parte visível do primitivo seja renderizada.
ms.assetid: 096683a4-2d8f-49d3-b1a0-832150907f11
title: Estado de recorte primitivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5a305118d8db5c71e0e3cfa97132052777be68
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370333"
---
# <a name="primitive-clipping-state-direct3d-9"></a><span data-ttu-id="236fe-103">Estado de recorte primitivo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="236fe-103">Primitive Clipping State (Direct3D 9)</span></span>

<span data-ttu-id="236fe-104">Os primitivos que ficam parcialmente dentro (ou completamente fora) da [exibição frustum](viewports-and-clipping.md) podem ser recortados para que apenas a parte visível do primitivo seja renderizada.</span><span class="sxs-lookup"><span data-stu-id="236fe-104">Primitives that lie partially inside (or completely outside) the [view frustum](viewports-and-clipping.md) can be clipped so that only the visible portion of the primitive will be rendered.</span></span> <span data-ttu-id="236fe-105">O recorte reduz a quantidade de trabalho feita apenas para os primitivos ou partes de um primitivo que ficará visível.</span><span class="sxs-lookup"><span data-stu-id="236fe-105">Clipping reduces the amount of work that is done to only those primitives or portions of a primitive that will be visible.</span></span>

<span data-ttu-id="236fe-106">Para usar o pipeline para recorte, defina o \_ estado de renderização de recorte D3DRS como **true** (o valor padrão) para habilitar o recorte ou **false** para desabilitar o recorte de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="236fe-106">To use the pipeline for clipping, set the D3DRS\_CLIPPING render state to **TRUE** (the default value) to enable clipping, or to **FALSE** to disable Direct3D clipping.</span></span>

## <a name="related-topics"></a><span data-ttu-id="236fe-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="236fe-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="236fe-108">Processar Estados</span><span class="sxs-lookup"><span data-stu-id="236fe-108">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



