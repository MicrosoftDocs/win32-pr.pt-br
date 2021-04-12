---
title: IAgentNotifySink DblClick
description: IAgentNotifySink DblClick
ms.assetid: 7e86cc9b-8bc3-405e-9bbf-764cec9c3130
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ec7372d524027588dae5a0a3aafaf07146556e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364004"
---
# <a name="iagentnotifysinkdblclick"></a><span data-ttu-id="db94d-103">IAgentNotifySink::D blClick</span><span class="sxs-lookup"><span data-stu-id="db94d-103">IAgentNotifySink::DblClick</span></span>

<span data-ttu-id="db94d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="db94d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DblClick(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="db94d-105">Notifica um aplicativo cliente quando o usuário clica duas vezes em um caractere.</span><span class="sxs-lookup"><span data-stu-id="db94d-105">Notifies a client application when the user double-clicks a character.</span></span>

-   <span data-ttu-id="db94d-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="db94d-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="db94d-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="db94d-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="db94d-108">Identificador do caractere clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="db94d-108">Identifier of the double-clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="db94d-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="db94d-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="db94d-110">Um parâmetro que indica o botão do mouse e o estado de chave do modificador.</span><span class="sxs-lookup"><span data-stu-id="db94d-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="db94d-111">O parâmetro pode retornar qualquer combinação do seguinte:</span><span class="sxs-lookup"><span data-stu-id="db94d-111">The parameter can return any combination of the following:</span></span>



|        |                                                |
|--------|------------------------------------------------|
| <span data-ttu-id="db94d-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="db94d-112">0x0001</span></span> | <span data-ttu-id="db94d-113">Botão esquerdo</span><span class="sxs-lookup"><span data-stu-id="db94d-113">Left Button</span></span>                                    |
| <span data-ttu-id="db94d-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="db94d-114">0x0010</span></span> | <span data-ttu-id="db94d-115">Botão do meio</span><span class="sxs-lookup"><span data-stu-id="db94d-115">Middle Button</span></span>                                  |
| <span data-ttu-id="db94d-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="db94d-116">0x0002</span></span> | <span data-ttu-id="db94d-117">Botão direito</span><span class="sxs-lookup"><span data-stu-id="db94d-117">Right Button</span></span>                                   |
| <span data-ttu-id="db94d-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="db94d-118">0x0004</span></span> | <span data-ttu-id="db94d-119">Tecla Shift para baixo</span><span class="sxs-lookup"><span data-stu-id="db94d-119">Shift Key Down</span></span>                                 |
| <span data-ttu-id="db94d-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="db94d-120">0x0008</span></span> | <span data-ttu-id="db94d-121">Tecla de controle para baixo</span><span class="sxs-lookup"><span data-stu-id="db94d-121">Control Key Down</span></span>                               |
| <span data-ttu-id="db94d-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="db94d-122">0x0020</span></span> | <span data-ttu-id="db94d-123">Tecla Alt para baixo</span><span class="sxs-lookup"><span data-stu-id="db94d-123">Alt Key Down</span></span>                                   |
| <span data-ttu-id="db94d-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="db94d-124">0x1000</span></span> | <span data-ttu-id="db94d-125">Ocorreu um evento no ícone da barra de tarefas do caractere</span><span class="sxs-lookup"><span data-stu-id="db94d-125">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="db94d-126"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="db94d-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="db94d-127">A coordenada x do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="db94d-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="db94d-128"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="db94d-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="db94d-129">A coordenada y do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="db94d-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="db94d-130">Esse evento é enviado para o cliente de entrada-ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="db94d-130">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="db94d-131">Se nenhum dos clientes do caractere for entrada-ativo, o servidor notificará o cliente ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="db94d-131">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="db94d-132">Se o caractere estiver visível, o servidor também tornará a entrada do cliente ativa e enviará o [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md).</span><span class="sxs-lookup"><span data-stu-id="db94d-132">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="db94d-133">Se o caractere estiver oculto, o caractere também será mostrado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="db94d-133">If the character is hidden, the character is also automatically shown.</span></span>

 

 




