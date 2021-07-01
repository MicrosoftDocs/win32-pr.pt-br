---
title: IAgentNotifySink DragComplete
description: IAgentNotifySink DragComplete
ms.assetid: b2d9b9c2-709e-4988-aa92-f129e3836fc7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb93fbc7bae1ac43d534962659b850561bd50a6d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120801"
---
# <a name="iagentnotifysinkdragcomplete"></a><span data-ttu-id="d244c-103">IAgentNotifySink::D ragComplete</span><span class="sxs-lookup"><span data-stu-id="d244c-103">IAgentNotifySink::DragComplete</span></span>

<span data-ttu-id="d244c-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d244c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DragComplete(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x-coordinate of mouse pointer
   long y          // y-coordinate of mouse pointer
);                          
```

<span data-ttu-id="d244c-105">Notifica um aplicativo cliente quando o usuário para de arrastar um caractere.</span><span class="sxs-lookup"><span data-stu-id="d244c-105">Notifies a client application when the user stops dragging a character.</span></span>

-   <span data-ttu-id="d244c-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="d244c-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="d244c-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="d244c-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="d244c-108">Identificador do caractere arrastado.</span><span class="sxs-lookup"><span data-stu-id="d244c-108">Identifier of the dragged character.</span></span>

</dd> <dt>

<span data-ttu-id="d244c-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="d244c-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="d244c-110">Um parâmetro que indica o botão do mouse e o estado da chave modificadora.</span><span class="sxs-lookup"><span data-stu-id="d244c-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="d244c-111">O parâmetro pode retornar qualquer combinação do seguinte:</span><span class="sxs-lookup"><span data-stu-id="d244c-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="d244c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="d244c-112">Value</span></span>  | <span data-ttu-id="d244c-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="d244c-113">Description</span></span>      |
|--------|------------------|
| <span data-ttu-id="d244c-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="d244c-114">0x0001</span></span> | <span data-ttu-id="d244c-115">Botão Esquerdo</span><span class="sxs-lookup"><span data-stu-id="d244c-115">Left Button</span></span>      |
| <span data-ttu-id="d244c-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="d244c-116">0x0010</span></span> | <span data-ttu-id="d244c-117">Botão Central</span><span class="sxs-lookup"><span data-stu-id="d244c-117">Middle Button</span></span>    |
| <span data-ttu-id="d244c-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="d244c-118">0x0002</span></span> | <span data-ttu-id="d244c-119">Botão Direito</span><span class="sxs-lookup"><span data-stu-id="d244c-119">Right Button</span></span>     |
| <span data-ttu-id="d244c-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="d244c-120">0x0004</span></span> | <span data-ttu-id="d244c-121">Tecla shift para baixo</span><span class="sxs-lookup"><span data-stu-id="d244c-121">Shift Key Down</span></span>   |
| <span data-ttu-id="d244c-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="d244c-122">0x0008</span></span> | <span data-ttu-id="d244c-123">Tecla de controle para baixo</span><span class="sxs-lookup"><span data-stu-id="d244c-123">Control Key Down</span></span> |
| <span data-ttu-id="d244c-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="d244c-124">0x0020</span></span> | <span data-ttu-id="d244c-125">Tecla Alt para baixo</span><span class="sxs-lookup"><span data-stu-id="d244c-125">Alt Key Down</span></span>     |



 

</dd> <dt>

<span data-ttu-id="d244c-126"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="d244c-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="d244c-127">A coordenada X do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerdo).</span><span class="sxs-lookup"><span data-stu-id="d244c-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="d244c-128"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="d244c-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="d244c-129">A coordenada Y do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerdo).</span><span class="sxs-lookup"><span data-stu-id="d244c-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

 

 




