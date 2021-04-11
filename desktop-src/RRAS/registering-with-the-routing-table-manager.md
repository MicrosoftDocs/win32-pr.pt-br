---
title: Registrando com o Gerenciador de tabela de roteamento
description: Antes que um cliente possa acessar a tabela de roteamento, ele primeiro deve se registrar com o Gerenciador de tabela de roteamento usando a função RtmRegisterEntity.
ms.assetid: 9bdbe138-d31b-42bb-9c51-5f1c5e8a4ca7
keywords:
- Gerenciador de tabela de roteamento versão 2 RRAS, registrando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1ce5a1b350ec5420b3fc32a4e5a68a213a61151
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159739"
---
# <a name="registering-with-the-routing-table-manager"></a><span data-ttu-id="bef98-104">Registrando com o Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="bef98-104">Registering with the Routing Table Manager</span></span>

<span data-ttu-id="bef98-105">Antes que um cliente possa acessar a tabela de roteamento, ele primeiro deve se registrar com o Gerenciador de tabela de roteamento usando a função [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) .</span><span class="sxs-lookup"><span data-stu-id="bef98-105">Before a client can access the routing table, it first must register with the routing table manager using the [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) function.</span></span>

<span data-ttu-id="bef98-106">Quando um cliente é registrado, ele passa para o Gerenciador de tabela de roteamento uma estrutura de [**\_ \_ informações de entidade RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) .</span><span class="sxs-lookup"><span data-stu-id="bef98-106">When a client registers, it passes to the routing table manager an [**RTM\_ENTITY\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) structure.</span></span> <span data-ttu-id="bef98-107">Essa estrutura contém as informações que identificam exclusivamente um cliente, a família de endereços e a instância do Gerenciador de tabelas de roteamento com a qual o cliente está se registrando.</span><span class="sxs-lookup"><span data-stu-id="bef98-107">This structure contains the information that uniquely identifies a client, the address family, and the instance of the routing table manager with which the client is registering.</span></span> <span data-ttu-id="bef98-108">Um cliente também pode estabelecer o retorno de chamada de [**\_ retorno de \_ chamada do evento RTM**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) .</span><span class="sxs-lookup"><span data-stu-id="bef98-108">A client can also establish the [**RTM\_EVENT\_CALLBACK**](/windows/win32/api/rtmv2/nc-rtmv2-_event_callback) callback.</span></span> <span data-ttu-id="bef98-109">O Gerenciador de tabela de roteamento usará esse retorno de chamada para notificar o cliente sobre eventos como notificações de alteração e registros de cliente.</span><span class="sxs-lookup"><span data-stu-id="bef98-109">The routing table manager will use this callback to notify the client of events such as change notifications and client registrations.</span></span>

<span data-ttu-id="bef98-110">O Gerenciador de tabela de roteamento conclui seu processamento de registro e retorna um identificador para o cliente.</span><span class="sxs-lookup"><span data-stu-id="bef98-110">The routing table manager completes its registration processing and returns a handle to the client.</span></span> <span data-ttu-id="bef98-111">O cliente deve usar esse identificador para todas as chamadas subsequentes para as funções RTMv2.</span><span class="sxs-lookup"><span data-stu-id="bef98-111">The client must use this handle for all subsequent calls to RTMv2 functions.</span></span>

<span data-ttu-id="bef98-112">A função [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) que é usada em RTMv2 é análoga à função [**RtmRegisterClient**](rtmregisterclient.md) que é usada em RTMv1.</span><span class="sxs-lookup"><span data-stu-id="bef98-112">The [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity) function that is used in RTMv2 is analogous to the [**RtmRegisterClient**](rtmregisterclient.md) function that is used in RTMv1.</span></span> <span data-ttu-id="bef98-113">A função **RtmRegisterClient** é obsoleta, exceto para clientes que usam IPX.</span><span class="sxs-lookup"><span data-stu-id="bef98-113">The **RtmRegisterClient** function is obsolete, except for clients using IPX.</span></span>

<span data-ttu-id="bef98-114">Depois que um cliente termina de interagir com o Gerenciador de tabela de roteamento, ele deve chamar [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity).</span><span class="sxs-lookup"><span data-stu-id="bef98-114">Once a client has finished interacting with the routing table manager, it must call [**RtmDeregisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmderegisterentity).</span></span> <span data-ttu-id="bef98-115">O Gerenciador de tabela de roteamento destrói o identificador associado ao cliente.</span><span class="sxs-lookup"><span data-stu-id="bef98-115">The routing table manager destroys the handle associated with the client.</span></span> <span data-ttu-id="bef98-116">Para evitar vazamentos de memória, o cliente deve garantir que ele libera todos os identificadores e exclui todas as rotas e os próximos saltos que ele possui antes de chamar **RtmDeregisterEntity**.</span><span class="sxs-lookup"><span data-stu-id="bef98-116">To avoid memory leaks, the client must ensure that it releases all handles and deletes all the routes and next hops that it owns before calling **RtmDeregisterEntity**.</span></span>

<span data-ttu-id="bef98-117">Para obter um exemplo de código que mostra como usar essas funções, consulte [registrar com o Gerenciador de tabela de roteamento](register-with-the-routing-table-manager.md) e [usar o retorno de chamada de notificação de evento](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="bef98-117">For sample code that shows how to use these functions, see [Register with the Routing Table Manager](register-with-the-routing-table-manager.md) and [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




