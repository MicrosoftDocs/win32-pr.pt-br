---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 031e78319beb0f62ddb0ea340fca0cd7ed88c0a2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292208"
---
# <a name="iagentnotifysinkdragstart"></a><span data-ttu-id="d9f99-103">IAgentNotifySink::D ragStart</span><span class="sxs-lookup"><span data-stu-id="d9f99-103">IAgentNotifySink::DragStart</span></span>

<span data-ttu-id="d9f99-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d9f99-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="d9f99-105">Notifica um aplicativo cliente quando o usuário começa a arrastar um caractere.</span><span class="sxs-lookup"><span data-stu-id="d9f99-105">Notifies a client application when the user starts dragging a character.</span></span>

-   <span data-ttu-id="d9f99-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d9f99-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="d9f99-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="d9f99-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="d9f99-108">Identificador do caractere arrastado.</span><span class="sxs-lookup"><span data-stu-id="d9f99-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="d9f99-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="d9f99-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="d9f99-110">Um parâmetro que indica o botão do mouse e o estado de chave do modificador.</span><span class="sxs-lookup"><span data-stu-id="d9f99-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="d9f99-111">O parâmetro pode retornar qualquer combinação do seguinte:</span><span class="sxs-lookup"><span data-stu-id="d9f99-111">The parameter can return any combination of the following:</span></span>



|        |                  |
|--------|------------------|
| <span data-ttu-id="d9f99-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="d9f99-112">0x0001</span></span> | <span data-ttu-id="d9f99-113">Botão esquerdo</span><span class="sxs-lookup"><span data-stu-id="d9f99-113">Left Button</span></span>      |
| <span data-ttu-id="d9f99-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="d9f99-114">0x0010</span></span> | <span data-ttu-id="d9f99-115">Botão do meio</span><span class="sxs-lookup"><span data-stu-id="d9f99-115">Middle Button</span></span>    |
| <span data-ttu-id="d9f99-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="d9f99-116">0x0002</span></span> | <span data-ttu-id="d9f99-117">Botão direito</span><span class="sxs-lookup"><span data-stu-id="d9f99-117">Right Button</span></span>     |
| <span data-ttu-id="d9f99-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="d9f99-118">0x0004</span></span> | <span data-ttu-id="d9f99-119">Tecla Shift para baixo</span><span class="sxs-lookup"><span data-stu-id="d9f99-119">Shift Key Down</span></span>   |
| <span data-ttu-id="d9f99-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="d9f99-120">0x0008</span></span> | <span data-ttu-id="d9f99-121">Tecla de controle para baixo</span><span class="sxs-lookup"><span data-stu-id="d9f99-121">Control Key Down</span></span> |
| <span data-ttu-id="d9f99-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="d9f99-122">0x0020</span></span> | <span data-ttu-id="d9f99-123">Tecla Alt para baixo</span><span class="sxs-lookup"><span data-stu-id="d9f99-123">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="d9f99-124"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="d9f99-124"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="d9f99-125">A coordenada x do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="d9f99-125">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="d9f99-126"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="d9f99-126"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="d9f99-127">A coordenada y do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="d9f99-127">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




