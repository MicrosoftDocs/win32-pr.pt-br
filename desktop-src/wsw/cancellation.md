---
title: Cancelamento
description: A maioria das operações no WWSAPI pode ser cancelada durante a execução.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Serviços Web de cancelamento para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e979455e898922dfb7c81381c1f1aafd455274
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294631"
---
# <a name="cancellation"></a><span data-ttu-id="a8659-106">Cancelamento</span><span class="sxs-lookup"><span data-stu-id="a8659-106">Cancellation</span></span>

<span data-ttu-id="a8659-107">A maioria das operações no WWSAPI pode ser cancelada durante a execução.</span><span class="sxs-lookup"><span data-stu-id="a8659-107">Most of operations in the WWSAPI can be canceled during execution.</span></span>

<span data-ttu-id="a8659-108">A função que você usa para cancelar uma operação depende do objeto afetado.</span><span class="sxs-lookup"><span data-stu-id="a8659-108">Which function you use to cancel an operation depends on the object affected.</span></span>

| <span data-ttu-id="a8659-109">Função</span><span class="sxs-lookup"><span data-stu-id="a8659-109">Function</span></span>                                           | <span data-ttu-id="a8659-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8659-110">Description</span></span>                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8659-111">**WsAbortChannel**</span><span class="sxs-lookup"><span data-stu-id="a8659-111">**WsAbortChannel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | <span data-ttu-id="a8659-112">Cancela todas as entradas e saídas pendentes em um canal especificado e define o estado do canal para o estado do WS \_ Channel com \_ \_ falha.</span><span class="sxs-lookup"><span data-stu-id="a8659-112">Cancels all pending input and output on a specified channel and sets the channel state to WS\_CHANNEL\_STATE\_FAULTED.</span></span> |
| [<span data-ttu-id="a8659-113">**WsAbortListener**</span><span class="sxs-lookup"><span data-stu-id="a8659-113">**WsAbortListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | <span data-ttu-id="a8659-114">Cancela todas as entradas e saídas pendentes em um ouvinte especificado.</span><span class="sxs-lookup"><span data-stu-id="a8659-114">Cancels all pending input and output on a specified listener.</span></span>                                                          |
| [<span data-ttu-id="a8659-115">**WsAbortServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="a8659-115">**WsAbortServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | <span data-ttu-id="a8659-116">Cancela todas as entradas e saídas pendentes em um proxy de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="a8659-116">Cancels all pending input and output on a specified service proxy.</span></span>                                                     |
| [<span data-ttu-id="a8659-117">**WsAbortServiceHost**</span><span class="sxs-lookup"><span data-stu-id="a8659-117">**WsAbortServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | <span data-ttu-id="a8659-118">Interrompe e descontinua as operações atuais no host de serviço.</span><span class="sxs-lookup"><span data-stu-id="a8659-118">Interrupts and discontinues current operations on the service host.</span></span>                                                    |
| [<span data-ttu-id="a8659-119">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="a8659-119">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | <span data-ttu-id="a8659-120">Abandona uma chamada, uma chamada especificada em um proxy de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="a8659-120">Abandons a call, a specified call on a specified service proxy.</span></span>                                                        |



 

<span data-ttu-id="a8659-121">Para obter informações sobre cancelamentos que afetam [operações de serviço do servidor](server-side-service-operations.md) e retornos de chamada de modelo de serviço, consulte [cancelamento de chamada](call-cancellation.md).</span><span class="sxs-lookup"><span data-stu-id="a8659-121">For information on cancellations that affect [server side service operations](server-side-service-operations.md) and service-model callbacks, see [Call Cancellation](call-cancellation.md).</span></span>


 

 




