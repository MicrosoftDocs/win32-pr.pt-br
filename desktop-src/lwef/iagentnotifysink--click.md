---
title: IAgentNotifySink clique em
description: IAgentNotifySink clique em
ms.assetid: 6587fed8-4651-4c5c-b257-6e3f991cd3a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d1dccd838152503c603d158f043a0279d4b5c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005712"
---
# <a name="iagentnotifysinkclick"></a><span data-ttu-id="a9416-103">IAgentNotifySink:: clique em</span><span class="sxs-lookup"><span data-stu-id="a9416-103">IAgentNotifySink::Click</span></span>

<span data-ttu-id="a9416-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a9416-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Click(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="a9416-105">Notifica um aplicativo cliente quando o usuário clica no ícone da barra de tarefas de um caractere ou caractere.</span><span class="sxs-lookup"><span data-stu-id="a9416-105">Notifies a client application when the user clicks a character or character's taskbar icon.</span></span>

-   <span data-ttu-id="a9416-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a9416-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="a9416-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="a9416-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="a9416-108">Identificador do caractere clicado.</span><span class="sxs-lookup"><span data-stu-id="a9416-108">Identifier of the clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="a9416-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="a9416-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="a9416-110">Um parâmetro que indica o botão do mouse e o estado de chave do modificador.</span><span class="sxs-lookup"><span data-stu-id="a9416-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="a9416-111">O parâmetro pode retornar qualquer combinação do seguinte:</span><span class="sxs-lookup"><span data-stu-id="a9416-111">The parameter can return any combination of the following:</span></span>



|        |                                                |
|--------|------------------------------------------------|
| <span data-ttu-id="a9416-112">0x0001</span><span class="sxs-lookup"><span data-stu-id="a9416-112">0x0001</span></span> | <span data-ttu-id="a9416-113">Botão esquerdo</span><span class="sxs-lookup"><span data-stu-id="a9416-113">Left Button</span></span>                                    |
| <span data-ttu-id="a9416-114">0x0010</span><span class="sxs-lookup"><span data-stu-id="a9416-114">0x0010</span></span> | <span data-ttu-id="a9416-115">Botão do meio</span><span class="sxs-lookup"><span data-stu-id="a9416-115">Middle Button</span></span>                                  |
| <span data-ttu-id="a9416-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="a9416-116">0x0002</span></span> | <span data-ttu-id="a9416-117">Botão direito</span><span class="sxs-lookup"><span data-stu-id="a9416-117">Right Button</span></span>                                   |
| <span data-ttu-id="a9416-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="a9416-118">0x0004</span></span> | <span data-ttu-id="a9416-119">Tecla Shift para baixo</span><span class="sxs-lookup"><span data-stu-id="a9416-119">Shift Key Down</span></span>                                 |
| <span data-ttu-id="a9416-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="a9416-120">0x0008</span></span> | <span data-ttu-id="a9416-121">Tecla de controle para baixo</span><span class="sxs-lookup"><span data-stu-id="a9416-121">Control Key Down</span></span>                               |
| <span data-ttu-id="a9416-122">0x0020</span><span class="sxs-lookup"><span data-stu-id="a9416-122">0x0020</span></span> | <span data-ttu-id="a9416-123">Tecla Alt para baixo</span><span class="sxs-lookup"><span data-stu-id="a9416-123">Alt Key Down</span></span>                                   |
| <span data-ttu-id="a9416-124">0x1000</span><span class="sxs-lookup"><span data-stu-id="a9416-124">0x1000</span></span> | <span data-ttu-id="a9416-125">Ocorreu um evento no ícone da barra de tarefas do caractere</span><span class="sxs-lookup"><span data-stu-id="a9416-125">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="a9416-126"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="a9416-126"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="a9416-127">A coordenada x do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="a9416-127">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="a9416-128"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="a9416-128"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="a9416-129">A coordenada y do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerda).</span><span class="sxs-lookup"><span data-stu-id="a9416-129">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="a9416-130">Esse evento é enviado para o cliente de entrada-ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="a9416-130">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="a9416-131">Se nenhum dos clientes do caractere for entrada-ativo, o servidor notificará o cliente ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="a9416-131">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="a9416-132">Se o caractere estiver visível, o servidor também tornará a entrada do cliente ativa e enviará o [**IAgentNotifySink:: ActivateInputState**](iagentnotifysink--activateinputstate.md).</span><span class="sxs-lookup"><span data-stu-id="a9416-132">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="a9416-133">Se o caractere estiver oculto, o caractere também será mostrado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a9416-133">If the character hidden, the character is also automatically shown.</span></span>

 

 




