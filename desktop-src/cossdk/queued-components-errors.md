---
description: Erros de componentes na fila
ms.assetid: 29a1bf52-7252-4f8a-bdb7-61b152fb907e
title: Erros de componentes na fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 422ea9c7ff77f2d69633d6db8b8d48c63fabc071
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793901"
---
# <a name="queued-components-errors"></a><span data-ttu-id="66c5d-103">Erros de componentes na fila</span><span class="sxs-lookup"><span data-stu-id="66c5d-103">Queued Components Errors</span></span>

<span data-ttu-id="66c5d-104">Quando uma chamada para um componente em fila falha, porque não pôde ser transmitida ao servidor (falha no lado do cliente) ou porque ele não pôde ser executado quando chegou (uma falha no servidor), a mensagem de [enfileiramento de mensagens](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) correspondente é chamada de *mensagem suspeita*.</span><span class="sxs-lookup"><span data-stu-id="66c5d-104">When a call to a queued component fails, either because it could not be transmitted to the server (a client-side failure) or because it failed to execute when it arrived (a server-side failure), the corresponding [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) message is called a *poison message*.</span></span>

<span data-ttu-id="66c5d-105">O serviço de componentes em fila COM+ manipula mensagens suspeitas usando uma série de filas de repetição.</span><span class="sxs-lookup"><span data-stu-id="66c5d-105">The COM+ queued components service handles poison messages by using a series of retry queues.</span></span> <span data-ttu-id="66c5d-106">Após várias tentativas, a mensagem é movida para uma fila de repouso final.</span><span class="sxs-lookup"><span data-stu-id="66c5d-106">After several retries, the message is moved to a final resting queue.</span></span> <span data-ttu-id="66c5d-107">As mensagens permanecem na fila de repouso até que sejam movidas manualmente usando o utilitário enfileiramento de mensagens dos componentes em fila.</span><span class="sxs-lookup"><span data-stu-id="66c5d-107">Messages stay in the resting queue until they are moved manually by using the queued components message mover utility.</span></span> <span data-ttu-id="66c5d-108">Para obter mais informações sobre como usar o movimentador de mensagem, consulte [Manipulando erros](handling-errors-in-queued-components.md).</span><span class="sxs-lookup"><span data-stu-id="66c5d-108">For more information about using the message mover, see [Handling Errors](handling-errors-in-queued-components.md).</span></span>

<span data-ttu-id="66c5d-109">Descrições detalhadas da sequência de eventos que ocorrem para vários tipos de erros podem ser encontradas nos tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="66c5d-109">Detailed descriptions of the sequence of events that occurs for various sorts of errors can be found in the topics described in the following table.</span></span>



| <span data-ttu-id="66c5d-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="66c5d-110">Topic</span></span>                                                                             | <span data-ttu-id="66c5d-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="66c5d-111">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66c5d-112">Erros do lado do servidor</span><span class="sxs-lookup"><span data-stu-id="66c5d-112">Server-Side Errors</span></span>](server-side-errors.md)<br/>                           | <span data-ttu-id="66c5d-113">Descreve em detalhes a resposta do serviço de componentes em fila COM+ para uma falha no servidor.</span><span class="sxs-lookup"><span data-stu-id="66c5d-113">Describes in detail the response of the COM+ queued components service to a server-side failure.</span></span><br/>             |
| [<span data-ttu-id="66c5d-114">Erros do lado do cliente</span><span class="sxs-lookup"><span data-stu-id="66c5d-114">Client-Side Errors</span></span>](client-side-errors.md)<br/>                           | <span data-ttu-id="66c5d-115">Descreve em detalhes a resposta do serviço de componentes em fila COM+ para uma falha do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="66c5d-115">Describes in detail the response of the COM+ queued components service to a client-side failure.</span></span><br/>             |
| [<span data-ttu-id="66c5d-116">Falhas de Client-Side persistentes</span><span class="sxs-lookup"><span data-stu-id="66c5d-116">Persistent Client-Side Failures</span></span>](persistent-client-side-failures.md)<br/> | <span data-ttu-id="66c5d-117">Descreve em detalhes a resposta do serviço de componentes em fila COM+ para falhas repetidas do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="66c5d-117">Describes in the detail the response of the COM+ queued components service to repeated client-side failures.</span></span><br/> |



 

 

 




