---
title: Alterações na melhor rota para uma rede
description: Uma alteração em qualquer um dos seguintes valores para a melhor rota para uma determinada rede de destino faz com que o Gerenciador de tabela de roteamento gere uma mensagem de notificação enviada para cada cliente registrado e para os encaminhadores
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8c43483dbd69f5407f9859d5943e515e8825d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105787034"
---
# <a name="changes-to-the-best-route-to-a-network"></a><span data-ttu-id="770c5-103">Alterações na melhor rota para uma rede</span><span class="sxs-lookup"><span data-stu-id="770c5-103">Changes to the Best Route to a Network</span></span>

<span data-ttu-id="770c5-104">**Windows Server 2003:** Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="770c5-104">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="770c5-105">Novos aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="770c5-105">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="770c5-106">Uma alteração em qualquer um dos seguintes valores para a melhor rota para uma determinada rede de destino faz com que o Gerenciador de tabela de roteamento gere uma mensagem de notificação enviada para cada cliente registrado e para os encaminhadores:</span><span class="sxs-lookup"><span data-stu-id="770c5-106">A change in any of the following values for the best route to a given destination network causes the routing table manager to generate a notification message sent to each registered client and to the forwarders:</span></span>

-   <span data-ttu-id="770c5-107">Identificador de protocolo</span><span class="sxs-lookup"><span data-stu-id="770c5-107">Protocol identifier</span></span>
-   <span data-ttu-id="770c5-108">Índice de interface</span><span class="sxs-lookup"><span data-stu-id="770c5-108">Interface index</span></span>
-   <span data-ttu-id="770c5-109">Endereço do roteador do próximo salto</span><span class="sxs-lookup"><span data-stu-id="770c5-109">Address of next-hop router</span></span>
-   <span data-ttu-id="770c5-110">Dados específicos da família de protocolos que incluem métricas de rota</span><span class="sxs-lookup"><span data-stu-id="770c5-110">Protocol family-specific data that includes route metrics</span></span>

<span data-ttu-id="770c5-111">Uma alteração no identificador de protocolo, índice de interface ou endereço de roteador do próximo salto ocorre quando uma nova entrada de rota melhor é adicionada ou quando a entrada de melhor rota atual é excluída ou expirada e deixa outra rota como a nova rota recomendada.</span><span class="sxs-lookup"><span data-stu-id="770c5-111">A change in protocol identifier, interface index, or next-hop router address occurs when a new, better-route entry is added, or when the current best-route entry is deleted or aged out, and leaves another route as the new best route.</span></span>

 

 




