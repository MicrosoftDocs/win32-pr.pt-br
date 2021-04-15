---
title: Escuta IAgentNotifySinkEx
description: Escuta IAgentNotifySinkEx
ms.assetid: e303b299-0dd0-419a-87a9-1490fe6cf54a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fee8f931030cbd68cd148fc57360d8b0ccf7624
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498724"
---
# <a name="iagentnotifysinkexlisteningstate"></a><span data-ttu-id="7fcf5-103">IAgentNotifySinkEx:: Listeningstate</span><span class="sxs-lookup"><span data-stu-id="7fcf5-103">IAgentNotifySinkEx::ListeningState</span></span>

<span data-ttu-id="7fcf5-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7fcf5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ListeningState(
   long dwCharacterID,  // character ID
   long bListening,     // listening mode state
   long dwCause         // cause  
);
```

<span data-ttu-id="7fcf5-105">Notifica um aplicativo cliente quando o modo de escuta é alterado.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-105">Notifies a client application when the Listening mode changes.</span></span>

-   <span data-ttu-id="7fcf5-106">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="7fcf5-107"><span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*</span><span class="sxs-lookup"><span data-stu-id="7fcf5-107"><span id="dwCharacterID"></span><span id="dwcharacterid"></span><span id="DWCHARACTERID"></span>*dwCharacterID*</span></span>
</dt> <dd>

<span data-ttu-id="7fcf5-108">O caractere para o qual o estado de escuta foi alterado.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-108">The character for which the listening state changed.</span></span>

</dd> <dt>

<span data-ttu-id="7fcf5-109"><span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*</span><span class="sxs-lookup"><span data-stu-id="7fcf5-109"><span id="bListening"></span><span id="blistening"></span><span id="BLISTENING"></span>*bListening*</span></span>
</dt> <dd>

<span data-ttu-id="7fcf5-110">O estado do modo de escuta.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-110">The Listening mode state.</span></span> <span data-ttu-id="7fcf5-111">**Verdadeiro** indica que o modo de escuta foi iniciado; **False**, que o modo de escuta terminou.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-111">**True** indicates that Listening mode has started; **False**, that Listening mode has ended.</span></span>

</dd> <dt>

<span data-ttu-id="7fcf5-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="7fcf5-112"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="7fcf5-113">A causa do evento, que pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-113">The cause for the event, which may be one of the following values.</span></span>



| <span data-ttu-id="7fcf5-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7fcf5-114">Value</span></span>                                                                             | <span data-ttu-id="7fcf5-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="7fcf5-115">Description</span></span>                                                                    |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="7fcf5-116">**const LSCOMPLETE Long sem sinal** **\_ causa \_ PROGRAMDISABLED = 1;**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-116">**const unsigned long** **LSCOMPLETE\_CAUSE\_PROGRAMDISABLED = 1;**</span></span><br/>    | <span data-ttu-id="7fcf5-117">O modo de escuta foi desativado pelo código do programa.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-117">Listening mode was turned off by program code.</span></span>                                 |
| <span data-ttu-id="7fcf5-118">**const LSCOMPLETE Long sem sinal** **\_ causa \_ PROGRAMTIMEDOUT = 2;**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-118">**const unsigned long** **LSCOMPLETE\_CAUSE\_PROGRAMTIMEDOUT = 2;**</span></span><br/>    | <span data-ttu-id="7fcf5-119">O modo de escuta (ativado pelo código do programa) atingiu o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-119">Listening mode (turned on by program code) timed out.</span></span>                          |
| <span data-ttu-id="7fcf5-120">**const LSCOMPLETE Long sem sinal** **\_ causa \_ USERTIMEDOUT = 3;**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-120">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERTIMEDOUT = 3;**</span></span><br/>       | <span data-ttu-id="7fcf5-121">O modo de escuta (ativado pela chave de escuta) atingiu o tempo limite.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-121">Listening mode (turned on by the Listening key) timed out.</span></span>                     |
| <span data-ttu-id="7fcf5-122">**const LSCOMPLETE Long sem sinal** **\_ causa \_ USERRELEASEDKEY = 4;**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-122">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERRELEASEDKEY = 4;**</span></span><br/>    | <span data-ttu-id="7fcf5-123">O modo de escuta foi desativado porque o usuário liberou a chave de escuta.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-123">Listening mode was turned off because the user released the Listening key.</span></span>     |
| <span data-ttu-id="7fcf5-124">**const LSCOMPLETE Long sem sinal** **\_ causa \_ USERUTTERANCEENDED = 5;**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-124">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERUTTERANCEENDED = 5;**</span></span><br/> | <span data-ttu-id="7fcf5-125">O modo de escuta foi desativado porque o usuário terminou de falar.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-125">Listening mode was turned off because the user finished speaking.</span></span>              |
| <span data-ttu-id="7fcf5-126">**const LSCOMPLETE Long sem sinal** **\_ causa \_ CLIENTDEACTIVATED = 6;**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-126">**const unsigned long** **LSCOMPLETE\_CAUSE\_CLIENTDEACTIVATED = 6;**</span></span><br/>  | <span data-ttu-id="7fcf5-127">O modo de escuta foi desativado porque o cliente ativo de entrada foi desativado.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-127">Listening mode was turned off because the input active client was deactivated.</span></span> |
| <span data-ttu-id="7fcf5-128">**const LSCOMPLETE Long sem sinal** **\_ causa \_ DEFAULTCHARCHANGE = 7**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-128">**const unsigned long** **LSCOMPLETE\_CAUSE\_DEFAULTCHARCHANGE = 7**</span></span><br/>   | <span data-ttu-id="7fcf5-129">O modo de escuta foi desativado porque o caractere padrão foi alterado.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-129">Listening mode was turned off because the default character was changed.</span></span>       |
| <span data-ttu-id="7fcf5-130">**const LSCOMPLETE longo sem sinal** **\_ causa o \_ userdesabilitoud = 8**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-130">**const unsigned long** **LSCOMPLETE\_CAUSE\_USERDISABLED = 8**</span></span><br/>        | <span data-ttu-id="7fcf5-131">O modo de escuta foi desativado porque o usuário desabilitou a entrada de fala.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-131">Listening mode was turned off because the user disabled speech input.</span></span>          |



 

</dd> </dl>

<span data-ttu-id="7fcf5-132">Esse evento é enviado a todos os clientes quando o modo de escuta começa depois que o usuário pressiona a tecla de escuta ou quando seu tempo limite termina, ou quando o cliente de entrada-ativo chama o método [**IAgentCharacterEx:: Listen**](iagentcharacterex--listen.md) com **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-132">This event is sent to all clients when the Listening mode begins after the user presses the Listening key or when its time-out ends, or when the input-active client calls the [**IAgentCharacterEx::Listen**](iagentcharacterex--listen.md) method with **True** or **False**.</span></span>

<span data-ttu-id="7fcf5-133">O evento retorna valores para os clientes que atualmente têm esse caractere carregado.</span><span class="sxs-lookup"><span data-stu-id="7fcf5-133">The event returns values to the clients that currently have this character loaded.</span></span> <span data-ttu-id="7fcf5-134">Todos os outros clientes recebem um caractere nulo (cadeia de caracteres vazia).</span><span class="sxs-lookup"><span data-stu-id="7fcf5-134">All other clients receive a null character (empty string).</span></span>

## <a name="see-also"></a><span data-ttu-id="7fcf5-135">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="7fcf5-135">See Also</span></span>

[<span data-ttu-id="7fcf5-136">**IAgentCharacterEx:: escutar**</span><span class="sxs-lookup"><span data-stu-id="7fcf5-136">**IAgentCharacterEx::Listen**</span></span>](iagentcharacterex--listen.md)


 

 





