---
title: IAgentNotifySink
description: IAgentNotifySink
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2ccfd4acf4a64c229379aeea5847fbe044b7d5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007470"
---
# <a name="iagentnotifysink"></a><span data-ttu-id="eb7ae-103">IAgentNotifySink</span><span class="sxs-lookup"><span data-stu-id="eb7ae-103">IAgentNotifySink</span></span>

<span data-ttu-id="eb7ae-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="eb7ae-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="eb7ae-105">O IAgentNotifySink notifica os clientes quando determinadas alterações de estado ocorrem.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-105">IAgentNotifySink notifies clients when certain state changes occur.</span></span> <span data-ttu-id="eb7ae-106">Essas funções também estão disponíveis em [IAgentNotifySinkEx](iagentnotifysinkex.md).</span><span class="sxs-lookup"><span data-stu-id="eb7ae-106">These functions are also available from [IAgentNotifySinkEx](iagentnotifysinkex.md).</span></span>

<span data-ttu-id="eb7ae-107">**Métodos em ordem vtable**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="eb7ae-108">IAgentNotifySink</span><span class="sxs-lookup"><span data-stu-id="eb7ae-108">IAgentNotifySink</span></span>                                                      | <span data-ttu-id="eb7ae-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="eb7ae-109">Description</span></span>                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb7ae-110">**Comando**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-110">**Command**</span></span>](command-method.md)                                     | <span data-ttu-id="eb7ae-111">Ocorre quando o servidor processa um comando definido pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-111">Occurs when the server processes a client-defined command.</span></span>                               |
| [<span data-ttu-id="eb7ae-112">**ActivateInputState**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-112">**ActivateInputState**</span></span>](iagentnotifysink--activateinputstate.md)    | <span data-ttu-id="eb7ae-113">Ocorre quando um caractere se torna ou deixa de ser inserido-ativo.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-113">Occurs when a character becomes or ceases to be input-active.</span></span>                            |
| [<span data-ttu-id="eb7ae-114">**BalloonVisibleState**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-114">**BalloonVisibleState**</span></span>](iagentnotifysink---balloonvisiblestate.md) | <span data-ttu-id="eb7ae-115">Ocorre quando o estado **visível** do caractere é alterado.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-115">Occurs when the character's **Visible** state changes.</span></span>                                   |
| [<span data-ttu-id="eb7ae-116">**Evento Clicar**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-116">**Click Event**</span></span>](click-event.md)                                    | <span data-ttu-id="eb7ae-117">Ocorre quando um caractere é clicado.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-117">Occurs when a character is clicked.</span></span>                                                      |
| [<span data-ttu-id="eb7ae-118">**Evento DblClick**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-118">**DblClick Event**</span></span>](dblclick-event.md)                              | <span data-ttu-id="eb7ae-119">Ocorre quando um caractere é clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-119">Occurs when a character is double-clicked.</span></span>                                               |
| [<span data-ttu-id="eb7ae-120">**DragStart**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-120">**DragStart**</span></span>](/windows/desktop/lwef/dragstart-event)                                | <span data-ttu-id="eb7ae-121">Ocorre quando um usuário começa a arrastar um caractere.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-121">Occurs when a user starts dragging a character.</span></span>                                          |
| [<span data-ttu-id="eb7ae-122">**DragComplete**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-122">**DragComplete**</span></span>](https://www.bing.com/search?q=**DragComplete**)                          | <span data-ttu-id="eb7ae-123">Ocorre quando um usuário para de arrastar um caractere.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-123">Occurs when a user stops dragging a character.</span></span>                                           |
| [<span data-ttu-id="eb7ae-124">**RequestStart**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-124">**RequestStart**</span></span>](iagentnotifysink--requeststart.md)                | <span data-ttu-id="eb7ae-125">Ocorre quando o servidor começa a processar um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="eb7ae-125">Occurs when the server begins processing a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>    |
| [<span data-ttu-id="eb7ae-126">**RequestComplete**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-126">**RequestComplete**</span></span>](iagentnotifysink--requestcomplete.md)          | <span data-ttu-id="eb7ae-127">Ocorre quando o servidor conclui o processamento de um objeto de [**solicitação**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="eb7ae-127">Occurs when the server completes processing a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> |
| [<span data-ttu-id="eb7ae-128">**Indicador**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-128">**Bookmark**</span></span>](iagentnotifysink--bookmark.md)                        | <span data-ttu-id="eb7ae-129">Ocorre quando o servidor processa um indicador.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-129">Occurs when the server processes a bookmark.</span></span>                                             |
| [<span data-ttu-id="eb7ae-130">**Ocioso**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-130">**Idle**</span></span>](iagentnotifysink--idle.md)                                | <span data-ttu-id="eb7ae-131">Ocorre quando o servidor inicia ou termina o processamento ocioso.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-131">Occurs when the server starts or ends idle processing.</span></span>                                   |
| [<span data-ttu-id="eb7ae-132">**Mover**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-132">**Move**</span></span>](iagentnotifysink--move.md)                                | <span data-ttu-id="eb7ae-133">Ocorre quando um caractere é movido.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-133">Occurs when a character has been moved.</span></span>                                                  |
| [<span data-ttu-id="eb7ae-134">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-134">**Size**</span></span>](iagentnotifysink---size.md)                               | <span data-ttu-id="eb7ae-135">Ocorre quando um caractere é redimensionado.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-135">Occurs when a character has been resized.</span></span>                                                |
| [<span data-ttu-id="eb7ae-136">**BalloonVisibleState**</span><span class="sxs-lookup"><span data-stu-id="eb7ae-136">**BalloonVisibleState**</span></span>](iagentnotifysink---balloonvisiblestate.md) | <span data-ttu-id="eb7ae-137">Ocorre quando o estado de visibilidade do balão de palavras de um caractere é alterado.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-137">Occurs when the visibility state of a character's word balloon changes.</span></span>                  |



 

<span data-ttu-id="eb7ae-138">Os eventos IAgentNotifySink:: restart e IAgentNotifySink:: Shutdown, com suporte em versões anteriores do Microsoft Agent, agora estão obsoletos.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-138">The IAgentNotifySink::Restart and IAgentNotifySink::Shutdown events, supported in earlier versions of Microsoft Agent, are now obsolete.</span></span> <span data-ttu-id="eb7ae-139">Embora haja suporte para compatibilidade com versões anteriores, o servidor não envia mais esses eventos.</span><span class="sxs-lookup"><span data-stu-id="eb7ae-139">While supported for backward compatibility, the server no longer sends these events.</span></span>

 

 