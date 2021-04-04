---
title: Usando o Gerenciador de tabela de roteamento versão 2
description: Antes de começar a desenvolver clientes que usam as APIs do RTMv2, examine os problemas de programação do RTMv2.
ms.assetid: c0187b65-3cb2-4ab0-8d5f-ca37e8bc0ad7
keywords:
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de tabelas de roteamento versão 2, tarefas
- Gerenciador de tabelas de roteamento versão 2 RRAS, tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29bc7acab213325a0683de215995eeb2f635b102
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916376"
---
# <a name="using-routing-table-manager-version-2"></a><span data-ttu-id="7ef55-105">Usando o Gerenciador de tabela de roteamento versão 2</span><span class="sxs-lookup"><span data-stu-id="7ef55-105">Using Routing Table Manager Version 2</span></span>

<span data-ttu-id="7ef55-106">Antes de começar a desenvolver clientes que usam as APIs do RTMv2, examine os [problemas de programação do RTMv2](rtmv2-programming-issues.md).</span><span class="sxs-lookup"><span data-stu-id="7ef55-106">Before you begin developing clients that use the RTMv2 APIs, review the [RTMv2 Programming Issues](rtmv2-programming-issues.md).</span></span>

<span data-ttu-id="7ef55-107">Esta seção contém um código de exemplo que pode ser usado ao desenvolver clientes como protocolos de roteamento.</span><span class="sxs-lookup"><span data-stu-id="7ef55-107">This section contains sample code that can be used when developing clients such as routing protocols.</span></span>

-   [<span data-ttu-id="7ef55-108">Problemas de programação do RTMv2</span><span class="sxs-lookup"><span data-stu-id="7ef55-108">RTMv2 Programming Issues</span></span>](rtmv2-programming-issues.md)
-   [<span data-ttu-id="7ef55-109">Registrar com o Gerenciador de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="7ef55-109">Register with the Routing Table Manager</span></span>](register-with-the-routing-table-manager.md)
-   [<span data-ttu-id="7ef55-110">Enumerar as entidades registradas</span><span class="sxs-lookup"><span data-stu-id="7ef55-110">Enumerate the Registered Entities</span></span>](enumerate-the-registered-entities.md)
-   [<span data-ttu-id="7ef55-111">Obter e chamar os métodos exportados para um cliente</span><span class="sxs-lookup"><span data-stu-id="7ef55-111">Obtain and Call the Exported Methods for a Client</span></span>](obtain-and-call-the-exported-methods-for-a-client.md)
-   [<span data-ttu-id="7ef55-112">Registrar para notificação de alteração</span><span class="sxs-lookup"><span data-stu-id="7ef55-112">Register for Change Notification</span></span>](register-for-change-notification.md)
-   [<span data-ttu-id="7ef55-113">Adicionar e atualizar rotas usando RtmAddRouteToDest</span><span class="sxs-lookup"><span data-stu-id="7ef55-113">Add and Update Routes Using RtmAddRouteToDest</span></span>](add-and-update-routes-using-rtmaddroutetodest.md)
-   [<span data-ttu-id="7ef55-114">Atualizar uma rota no local usando o RtmUpdateAndUnlockRoute</span><span class="sxs-lookup"><span data-stu-id="7ef55-114">Update a Route In Place Using RtmUpdateAndUnlockRoute</span></span>](update-a-route-in-place-using-rtmupdateandunlockroute.md)
-   [<span data-ttu-id="7ef55-115">Usar o estado de Hold-Down de rota</span><span class="sxs-lookup"><span data-stu-id="7ef55-115">Use the Route Hold-Down State</span></span>](use-the-route-hold-down-state.md)
-   [<span data-ttu-id="7ef55-116">Enumerar todos os destinos</span><span class="sxs-lookup"><span data-stu-id="7ef55-116">Enumerate All Destinations</span></span>](enumerate-all-destinations.md)
-   [<span data-ttu-id="7ef55-117">Enumerar todas as rotas</span><span class="sxs-lookup"><span data-stu-id="7ef55-117">Enumerate All Routes</span></span>](enumerate-all-routes.md)
-   [<span data-ttu-id="7ef55-118">Pesquisar a melhor rota</span><span class="sxs-lookup"><span data-stu-id="7ef55-118">Search for the Best Route</span></span>](search-for-the-best-route.md)
-   [<span data-ttu-id="7ef55-119">Pesquisar rotas usando uma árvore de prefixo</span><span class="sxs-lookup"><span data-stu-id="7ef55-119">Search for Routes Using a Prefix Tree</span></span>](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md)
-   [<span data-ttu-id="7ef55-120">Acessar o ponteiro opaco em um destino</span><span class="sxs-lookup"><span data-stu-id="7ef55-120">Access the Opaque Pointer in a Destination</span></span>](access-the-opaque-pointer-in-a-destination.md)
-   [<span data-ttu-id="7ef55-121">Usar uma lista de rotas Client-Specific</span><span class="sxs-lookup"><span data-stu-id="7ef55-121">Use a Client-Specific Route List</span></span>](use-a-client-specific-route-list.md)
-   [<span data-ttu-id="7ef55-122">Usar o retorno de chamada de notificação de evento</span><span class="sxs-lookup"><span data-stu-id="7ef55-122">Use the Event Notification Callback</span></span>](use-the-event-notification-callback.md)

 

 




