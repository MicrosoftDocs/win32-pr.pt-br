---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f53215591e3d2797c5b57e5586ccb13fc91f5902
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006036"
---
# <a name="iagentnotifysinkdragcomplete"></a><span data-ttu-id="1aafc-103">IAgentNotifySink::D ragComplete</span><span class="sxs-lookup"><span data-stu-id="1aafc-103">IAgentNotifySink::DragComplete</span></span>

<span data-ttu-id="1aafc-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1aafc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="1aafc-105">Notifica um aplicativo cliente quando o usuário para de arrastar um caractere.</span><span class="sxs-lookup"><span data-stu-id="1aafc-105">Notifies a client application when the user stops dragging a character.</span></span>

-   <span data-ttu-id="1aafc-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="1aafc-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="1aafc-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="1aafc-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="1aafc-108">Identificador do caractere arrastado.</span><span class="sxs-lookup"><span data-stu-id="1aafc-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="1aafc-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="1aafc-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="1aafc-110">Um parâmetro que indica o botão do mouse e o estado de chave do modificador.</span><span class="sxs-lookup"><span data-stu-id="1aafc-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="1aafc-111">O parâmetro pode retornar qualquer combinação do seguinte:</span><span class="sxs-lookup"><span data-stu-id="1aafc-111">The parameter can return any combination of the following:</span></span>



|        |                  |
|--------|------------------|
| <span data-ttu-id="1aafc-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="1aafc-112">0x0001</span></span> | <span data-ttu-id="1aafc-113">Botão esquerdo</span><span class="sxs-lookup"><span data-stu-id="1aafc-113">Left Button</span></span>      |
| <span data-ttu-id="1aafc-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="1aafc-114">0x0010</span></span> | <span data-ttu-id="1aafc-115">Botão do meio</span><span class="sxs-lookup"><span data-stu-id="1aafc-115">Middle Button</span></span>    |
| <span data-ttu-id="1aafc-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="1aafc-116">0x0002</span></span> | <span data-ttu-id="1aafc-117">Botão direito</span><span class="sxs-lookup"><span data-stu-id="1aafc-117">Right Button</span></span>     |
| <span data-ttu-id="1aafc-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="1aafc-118">0x0004</span></span> | <span data-ttu-id="1aafc-119">Tecla Shift para baixo</span><span class="sxs-lookup"><span data-stu-id="1aafc-119">Shift Key Down</span></span>   |
| <span data-ttu-id="1aafc-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="1aafc-120">0x0008</span></span> | <span data-ttu-id="1aafc-121">Tecla de controle para baixo</span><span class="sxs-lookup"><span data-stu-id="1aafc-121">Control Key Down</span></span> |
| <span data-ttu-id="1aafc-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="1aafc-122">0x0020</span></span> | <span data-ttu-id="1aafc-123">Tecla Alt para baixo</span><span class="sxs-lookup"><span data-stu-id="1aafc-123">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="1aafc-124"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="1aafc-124"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="1aafc-125">A coordenada x do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="1aafc-125">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="1aafc-126"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="1aafc-126"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="1aafc-127">A coordenada y do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="1aafc-127">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




