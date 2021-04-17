---
title: Gerenciador de tabela de roteamento
description: O Gerenciador de tabela de roteamento é o repositório central de informações de roteamento para todos os protocolos de roteamento que operam no RRAS (serviço de roteamento e acesso remoto).
ms.assetid: 7b01704e-c1fb-40e3-89cf-1206fdf9fd75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98094eb34c8575e0c24854813fc7458c98749568
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105759601"
---
# <a name="routing-table-manager"></a><span data-ttu-id="80209-103">Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="80209-103">Routing Table Manager</span></span>

<span data-ttu-id="80209-104">O Gerenciador de tabela de roteamento é o repositório central de informações de roteamento para todos os protocolos de roteamento que operam no RRAS (serviço de roteamento e acesso remoto).</span><span class="sxs-lookup"><span data-stu-id="80209-104">The routing table manager is the central repository of routing information for all routing protocols that operate under the Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="80209-105">Ele notifica os clientes quando as alterações ocorreram e permite que os clientes troquem informações particulares.</span><span class="sxs-lookup"><span data-stu-id="80209-105">It notifies clients when changes have occurred, and allows clients to exchange private information.</span></span>

<span data-ttu-id="80209-106">O Gerenciador de tabela de roteamento fornece informações de roteamento para todos os clientes interessados, como protocolos de roteamento, programas de gerenciamento e programas de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="80209-106">The routing table manager provides routing information to all interested clients, such as routing protocols, management programs, and monitoring programs.</span></span> <span data-ttu-id="80209-107">O Gerenciador de tabela de roteamento também determina a melhor rota para cada rede de destino conhecida pelos protocolos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="80209-107">The routing table manager also determines the best route to each destination network that is known to the routing protocols.</span></span> <span data-ttu-id="80209-108">O Gerenciador de tabela de roteamento determina essa rota com base nas prioridades do protocolo de roteamento e nas métricas associadas às rotas.</span><span class="sxs-lookup"><span data-stu-id="80209-108">The routing table manager determines this route based on routing protocol priorities and on the metrics associated with the routes.</span></span> <span data-ttu-id="80209-109">A pessoa que administra o roteador pode configurar as prioridades do protocolo de roteamento usando o console de gerenciamento do RRAS.</span><span class="sxs-lookup"><span data-stu-id="80209-109">The person administering the router can configure routing protocol priorities using the RRAS management console.</span></span>

<span data-ttu-id="80209-110">O Gerenciador de tabela de roteamento passa as informações de melhor rota para os encaminhadores (uma por família de endereços ou uma por interface) e para todos os clientes interessados.</span><span class="sxs-lookup"><span data-stu-id="80209-110">The routing table manager passes the best-route information to the forwarders (one per address family, or one per interface) and to all interested clients.</span></span>

<span data-ttu-id="80209-111">Cada cliente é registrado com o Gerenciador de tabela de roteamento e, em retorno, recebe um identificador que o cliente usa para adicionar ou excluir rotas.</span><span class="sxs-lookup"><span data-stu-id="80209-111">Each client registers with the routing table manager, and in return receives a handle that the client uses to add or delete routes.</span></span> <span data-ttu-id="80209-112">Os clientes podem recuperar informações armazenadas na tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="80209-112">Clients can retrieve information stored in the routing table.</span></span> <span data-ttu-id="80209-113">Além disso, os clientes podem se registrar no Gerenciador de tabelas de roteamento para receber notificações de alterações na melhor rota para um destino.</span><span class="sxs-lookup"><span data-stu-id="80209-113">Additionally, clients can register with the routing table manager to receive notification of changes to the best route to a destination.</span></span>

 

 




