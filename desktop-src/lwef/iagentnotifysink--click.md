---
title: Clique em IAgentNotifySink
description: Clique em IAgentNotifySink
ms.assetid: 6587fed8-4651-4c5c-b257-6e3f991cd3a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0e63244a89467225a7bfd045af6dc112431d12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120899"
---
# <a name="iagentnotifysinkclick"></a><span data-ttu-id="60ec9-103">IAgentNotifySink::Click</span><span class="sxs-lookup"><span data-stu-id="60ec9-103">IAgentNotifySink::Click</span></span>

<span data-ttu-id="60ec9-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="60ec9-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Click(
   long dwCharID,  // character ID
   short fwKeys,   // mouse button and modifier key state
   long x,         // x coordinate of mouse pointer
   long y          // y coordinate of mouse pointer
);                          
```

<span data-ttu-id="60ec9-105">Notifica um aplicativo cliente quando o usuário clica no ícone de barra de tarefas de um caractere ou caractere.</span><span class="sxs-lookup"><span data-stu-id="60ec9-105">Notifies a client application when the user clicks a character or character's taskbar icon.</span></span>

-   <span data-ttu-id="60ec9-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="60ec9-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="60ec9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="60ec9-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="60ec9-108">Identificador do caractere clicado.</span><span class="sxs-lookup"><span data-stu-id="60ec9-108">Identifier of the clicked character.</span></span>

</dd> <dt>

<span data-ttu-id="60ec9-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span><span class="sxs-lookup"><span data-stu-id="60ec9-109"><span id="fwKeys"></span><span id="fwkeys"></span><span id="FWKEYS"></span>*fwKeys*</span></span>
</dt> <dd>

<span data-ttu-id="60ec9-110">Um parâmetro que indica o botão do mouse e o estado da chave modificadora.</span><span class="sxs-lookup"><span data-stu-id="60ec9-110">A parameter that indicates the mouse button and modifier key state.</span></span> <span data-ttu-id="60ec9-111">O parâmetro pode retornar qualquer combinação do seguinte:</span><span class="sxs-lookup"><span data-stu-id="60ec9-111">The parameter can return any combination of the following:</span></span>



| <span data-ttu-id="60ec9-112">Valor</span><span class="sxs-lookup"><span data-stu-id="60ec9-112">Value</span></span>  | <span data-ttu-id="60ec9-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="60ec9-113">Description</span></span>                                    |
|--------|------------------------------------------------|
| <span data-ttu-id="60ec9-114">0x0001</span><span class="sxs-lookup"><span data-stu-id="60ec9-114">0x0001</span></span> | <span data-ttu-id="60ec9-115">Botão Esquerdo</span><span class="sxs-lookup"><span data-stu-id="60ec9-115">Left Button</span></span>                                    |
| <span data-ttu-id="60ec9-116">0x0010</span><span class="sxs-lookup"><span data-stu-id="60ec9-116">0x0010</span></span> | <span data-ttu-id="60ec9-117">Botão Central</span><span class="sxs-lookup"><span data-stu-id="60ec9-117">Middle Button</span></span>                                  |
| <span data-ttu-id="60ec9-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="60ec9-118">0x0002</span></span> | <span data-ttu-id="60ec9-119">Botão Direito</span><span class="sxs-lookup"><span data-stu-id="60ec9-119">Right Button</span></span>                                   |
| <span data-ttu-id="60ec9-120">0x0004</span><span class="sxs-lookup"><span data-stu-id="60ec9-120">0x0004</span></span> | <span data-ttu-id="60ec9-121">Tecla shift para baixo</span><span class="sxs-lookup"><span data-stu-id="60ec9-121">Shift Key Down</span></span>                                 |
| <span data-ttu-id="60ec9-122">0x0008</span><span class="sxs-lookup"><span data-stu-id="60ec9-122">0x0008</span></span> | <span data-ttu-id="60ec9-123">Tecla de controle para baixo</span><span class="sxs-lookup"><span data-stu-id="60ec9-123">Control Key Down</span></span>                               |
| <span data-ttu-id="60ec9-124">0x0020</span><span class="sxs-lookup"><span data-stu-id="60ec9-124">0x0020</span></span> | <span data-ttu-id="60ec9-125">Tecla Alt para baixo</span><span class="sxs-lookup"><span data-stu-id="60ec9-125">Alt Key Down</span></span>                                   |
| <span data-ttu-id="60ec9-126">0x1000</span><span class="sxs-lookup"><span data-stu-id="60ec9-126">0x1000</span></span> | <span data-ttu-id="60ec9-127">Evento ocorrido no ícone da barra de tarefas do caractere</span><span class="sxs-lookup"><span data-stu-id="60ec9-127">Event occurred on the character's taskbar icon</span></span> |



 

</dd> <dt>

<span data-ttu-id="60ec9-128"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="60ec9-128"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="60ec9-129">A coordenada X do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerdo).</span><span class="sxs-lookup"><span data-stu-id="60ec9-129">The x-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="60ec9-130"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="60ec9-130"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="60ec9-131">A coordenada Y do ponteiro do mouse em pixels, em relação à origem da tela (superior esquerdo).</span><span class="sxs-lookup"><span data-stu-id="60ec9-131">The y-coordinate of the mouse pointer in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="60ec9-132">Esse evento é enviado para o cliente ativo de entrada do caractere.</span><span class="sxs-lookup"><span data-stu-id="60ec9-132">This event is sent to the input-active client of the character.</span></span> <span data-ttu-id="60ec9-133">Se nenhum dos clientes do caractere estiver ativo de entrada, o servidor notifica o cliente ativo do caractere.</span><span class="sxs-lookup"><span data-stu-id="60ec9-133">If none of the character's clients are input-active, the server notifies the character's active client.</span></span> <span data-ttu-id="60ec9-134">Se o caractere estiver visível, o servidor também torna esse cliente ativo de entrada e envia [**o IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span><span class="sxs-lookup"><span data-stu-id="60ec9-134">If the character is visible, the server also makes that client input-active and sends the [**IAgentNotifySink::ActivateInputState**](iagentnotifysink--activateinputstate.md).</span></span> <span data-ttu-id="60ec9-135">Se o caractere estiver oculto, o caractere também será mostrado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="60ec9-135">If the character hidden, the character is also automatically shown.</span></span>

 

 




