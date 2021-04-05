---
title: Enumerando entidades registradas
description: Depois que um cliente é registrado, o cliente pode obter uma lista de todos os outros clientes que se registraram com o Gerenciador de tabela de roteamento. Alguns clientes devem executar determinadas operações se a presença de um determinado tipo de cliente for detectada.
ms.assetid: d94de573-7c1e-4179-a41f-5836d2c5d44a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac92ccf89336d3fbca378209b9e79877d9b426a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005569"
---
# <a name="enumerating-registered-entities"></a><span data-ttu-id="34ae5-104">Enumerando entidades registradas</span><span class="sxs-lookup"><span data-stu-id="34ae5-104">Enumerating Registered Entities</span></span>

<span data-ttu-id="34ae5-105">Depois que um cliente é registrado, o cliente pode obter uma lista de todos os outros clientes que se registraram com o Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="34ae5-105">After a client has registered, the client can obtain a list of all the other clients that have registered with the routing table manager.</span></span> <span data-ttu-id="34ae5-106">Alguns clientes devem executar determinadas operações se a presença de um determinado tipo de cliente for detectada.</span><span class="sxs-lookup"><span data-stu-id="34ae5-106">Some clients must perform certain operations if the presence of a particular type of client is detected.</span></span>

<span data-ttu-id="34ae5-107">O cliente pode chamar a função [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) .</span><span class="sxs-lookup"><span data-stu-id="34ae5-107">The client can call the [**RtmGetRegisteredEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetregisteredentities) function.</span></span> <span data-ttu-id="34ae5-108">Um buffer de estruturas de [**\_ \_ informações de entidade RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) é retornado.</span><span class="sxs-lookup"><span data-stu-id="34ae5-108">A buffer of [**RTM\_ENTITY\_INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_entity_info) structures is returned.</span></span> <span data-ttu-id="34ae5-109">Depois que o cliente tiver processado essas informações, o cliente deverá chamar [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) para liberar os identificadores nas estruturas de **\_ \_ informações da entidade RTM** .</span><span class="sxs-lookup"><span data-stu-id="34ae5-109">After the client has processed this information, the client should call [**RtmReleaseEntities**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentities) to release the handles in the **RTM\_ENTITY\_INFO** structures.</span></span>

<span data-ttu-id="34ae5-110">Se o cliente do Gerenciador de tabela de roteamento forneceu uma função de retorno de chamada em chamar [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), o cliente será notificado quando qualquer outro cliente registrar ou cancelar o registro.</span><span class="sxs-lookup"><span data-stu-id="34ae5-110">If the routing table manager client supplied a callback function in the call to [**RtmRegisterEntity**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmregisterentity), the client is notified when any other clients register or unregister.</span></span>

<span data-ttu-id="34ae5-111">Para obter um exemplo de código que mostra como usar essas funções, consulte [enumerar as entidades registradas](enumerate-the-registered-entities.md) e [usar o retorno de chamada de notificação de evento](use-the-event-notification-callback.md).</span><span class="sxs-lookup"><span data-stu-id="34ae5-111">For sample code that shows how to use these functions, see [Enumerate the Registered Entities](enumerate-the-registered-entities.md) and [Use the Event Notification Callback](use-the-event-notification-callback.md).</span></span>

 

 




