---
title: Sobre o Gerenciador de tabela de roteamento versão 1
description: O Gerenciador de tabela de roteamento é um repositório central de informações de roteamento para todos os protocolos de roteamento que operam em RRAS (serviço de roteamento e acesso remoto).
ms.assetid: 6d0e7697-5c52-4a69-b2a1-9c893600191b
keywords:
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de tabela de roteamento versão 1
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de tabela de roteamento versão 1, descrito
- Gerenciador de tabela de roteamento versão 1 RRAS
- Gerenciador de tabela de roteamento versão 1 RRAS, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b99f913230db6e6882a36b414914c3924181a221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005641"
---
# <a name="about-routing-table-manager-version-1"></a><span data-ttu-id="7447b-107">Sobre o Gerenciador de tabela de roteamento versão 1</span><span class="sxs-lookup"><span data-stu-id="7447b-107">About Routing Table Manager Version 1</span></span>

<span data-ttu-id="7447b-108">**Windows Server 2003:** Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7447b-108">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="7447b-109">Novos aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="7447b-109">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="7447b-110">O Gerenciador de tabela de roteamento é um repositório central de informações de roteamento para todos os protocolos de roteamento que operam em RRAS (serviço de roteamento e acesso remoto).</span><span class="sxs-lookup"><span data-stu-id="7447b-110">The routing table manager is a central repository of routing information for all routing protocols that operate under Routing and Remote Access Service (RRAS).</span></span> <span data-ttu-id="7447b-111">O Gerenciador de tabela de roteamento fornece informações de roteamento para todos os componentes interessados, como protocolos de roteamento, agentes de gerenciamento e agentes de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="7447b-111">The routing table manager provides routing information to all interested components, such as routing protocols, management agents, and monitoring agents.</span></span> <span data-ttu-id="7447b-112">O Gerenciador de tabela de roteamento também determina a melhor rota para cada rede de destino conhecida pelos protocolos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="7447b-112">The routing table manager also determines the best route to each destination network known to the routing protocols.</span></span> <span data-ttu-id="7447b-113">Ele determina essa rota com base nas prioridades do protocolo de roteamento e nas métricas associadas às rotas.</span><span class="sxs-lookup"><span data-stu-id="7447b-113">It determines this route based on routing protocol priorities and on metrics associated with the routes.</span></span> <span data-ttu-id="7447b-114">Observe que o administrador é capaz de configurar as prioridades do protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="7447b-114">Note that the administrator is able to configure routing protocol priorities.</span></span> <span data-ttu-id="7447b-115">Em seguida, o Gerenciador de tabela de roteamento passa as informações de melhor rota para os encaminhadores e de volta para os protocolos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="7447b-115">The routing table manager then passes the best-route information on to the forwarders and back to the routing protocols.</span></span>

<span data-ttu-id="7447b-116">Cada protocolo de roteamento chama [**RtmRegisterClient**](rtmregisterclient.md) para registrar com o Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="7447b-116">Each routing protocol calls [**RtmRegisterClient**](rtmregisterclient.md) to register with the routing table manager.</span></span> <span data-ttu-id="7447b-117">**RtmRegisterClient** retorna um identificador que é usado pelo protocolo de roteamento para adicionar ou excluir entradas de rota.</span><span class="sxs-lookup"><span data-stu-id="7447b-117">**RtmRegisterClient** returns a handle that is used by the routing protocol to add or delete route entries.</span></span> <span data-ttu-id="7447b-118">O **RtmRegisterClient** também permite que o protocolo de roteamento registre um objeto de evento com o Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="7447b-118">**RtmRegisterClient** also allows the routing protocol to register an event object with the routing table manager.</span></span> <span data-ttu-id="7447b-119">O Gerenciador de tabela de roteamento sinaliza esse objeto de evento para notificar o protocolo de roteamento das alterações nas informações de melhor rota.</span><span class="sxs-lookup"><span data-stu-id="7447b-119">The routing table manager signals this event object to notify the routing protocol of changes in best-route information.</span></span> <span data-ttu-id="7447b-120">Todos os outros componentes podem obter informações armazenadas no Gerenciador de tabela de roteamento por meio de enumeração de rota.</span><span class="sxs-lookup"><span data-stu-id="7447b-120">All other components can obtain information stored in the routing table manager through route enumeration.</span></span>

 

 




