---
title: IAgentNotifySink DragStart
description: IAgentNotifySink DragStart
ms.assetid: b3905b99-69e4-4046-aab9-2322618935aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33ae89f9e24c6c7b0ec69fba1a98b3a64a18620
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120820"
---
# <a name="iagentnotifysinkdragstart"></a><span data-ttu-id="2631f-103">IAgentNotifySink::D ragStart</span><span class="sxs-lookup"><span data-stu-id="2631f-103">IAgentNotifySink::DragStart</span></span>

<span data-ttu-id="2631f-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2631f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragStart(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="2631f-105">Notifica um aplicativo cliente quando o usuário começa a arrastar um caractere.</span><span class="sxs-lookup"><span data-stu-id="2631f-105">Notifies a client application when the user starts dragging a character.</span></span>

-   <span data-ttu-id="2631f-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="2631f-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="2631f-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="2631f-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="2631f-108">Identificador do caractere arrastado.</span><span class="sxs-lookup"><span data-stu-id="2631f-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="2631f-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="2631f-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="2631f-110">Um parâmetro que indica o botão do mouse e o estado de chave do modificador.</span><span class="sxs-lookup"><span data-stu-id="2631f-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="2631f-111">O parâmetro pode retornar qualquer combinação do seguinte:</span><span class="sxs-lookup"><span data-stu-id="2631f-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="2631f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="2631f-112">Value</span></span>  | <span data-ttu-id="2631f-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="2631f-113">Description</span></span>      |
|--------|------------------|
| <span data-ttu-id="2631f-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="2631f-114">0x0001</span></span> | <span data-ttu-id="2631f-115">Botão esquerdo</span><span class="sxs-lookup"><span data-stu-id="2631f-115">Left Button</span></span>      |
| <span data-ttu-id="2631f-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="2631f-116">0x0010</span></span> | <span data-ttu-id="2631f-117">Botão do meio</span><span class="sxs-lookup"><span data-stu-id="2631f-117">Middle Button</span></span>    |
| <span data-ttu-id="2631f-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="2631f-118">0x0002</span></span> | <span data-ttu-id="2631f-119">Botão direito</span><span class="sxs-lookup"><span data-stu-id="2631f-119">Right Button</span></span>     |
| <span data-ttu-id="2631f-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="2631f-120">0x0004</span></span> | <span data-ttu-id="2631f-121">Tecla Shift para baixo</span><span class="sxs-lookup"><span data-stu-id="2631f-121">Shift Key Down</span></span>   |
| <span data-ttu-id="2631f-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="2631f-122">0x0008</span></span> | <span data-ttu-id="2631f-123">Tecla de controle para baixo</span><span class="sxs-lookup"><span data-stu-id="2631f-123">Control Key Down</span></span> |
| <span data-ttu-id="2631f-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="2631f-124">0x0020</span></span> | <span data-ttu-id="2631f-125">Tecla Alt para baixo</span><span class="sxs-lookup"><span data-stu-id="2631f-125">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="2631f-126"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="2631f-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="2631f-127">A coordenada x do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="2631f-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="2631f-128"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="2631f-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="2631f-129">A coordenada y do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="2631f-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




