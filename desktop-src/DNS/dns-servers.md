---
title: Servidores DNS
description: Um servidor DNS é um computador que conclui o processo de resolução de nomes no DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- Servidores DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 509ceeb811f221560540ae60f269c6ee1b05444f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636482"
---
# <a name="dns-servers"></a><span data-ttu-id="f6f4b-104">Servidores DNS</span><span class="sxs-lookup"><span data-stu-id="f6f4b-104">DNS Servers</span></span>

<span data-ttu-id="f6f4b-105">Um *servidor DNS* é um computador que conclui o processo de resolução de nomes no DNS.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-105">A *DNS Server* is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="f6f4b-106">Os servidores DNS contêm [*arquivos de zona*](z-gly.md) que os habilitam a resolver nomes para endereços IP e endereços IP para nomes.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-106">DNS Servers contain [*zone files*](z-gly.md) that enable them to resolve names to IP addresses and IP addresses to names.</span></span> <span data-ttu-id="f6f4b-107">Quando consultado, um servidor DNS responderá de uma das três maneiras a seguir:</span><span class="sxs-lookup"><span data-stu-id="f6f4b-107">When queried, a DNS Server will respond in one of three ways:</span></span>

-   <span data-ttu-id="f6f4b-108">O servidor retorna a resolução de nome ou os dados de resolução de IP solicitados.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-108">The server returns the requested name-resolution or IP-resolution data.</span></span>
-   <span data-ttu-id="f6f4b-109">O servidor retorna um ponteiro para outro servidor DNS que pode atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-109">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="f6f4b-110">O servidor indica que ele não tem os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-110">The server indicates that it does not have the requested data.</span></span>

<span data-ttu-id="f6f4b-111">Os servidores DNS podem, durante o curso de preparação, retornar os dados de resolução solicitados, consultar outros servidores DNS, mas além disso, os servidores DNS não executam nenhuma outra operação.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-111">DNS Servers might, during the course of preparing to return the requested resolution data, query other DNS Servers, but beyond that, DNS Servers do not perform any other operations.</span></span>

<span data-ttu-id="f6f4b-112">Há três tipos principais de servidores DNS – servidores primários, servidores secundários e servidores de cache.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-112">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span>

## <a name="primary-server"></a><span data-ttu-id="f6f4b-113">Servidor Primário</span><span class="sxs-lookup"><span data-stu-id="f6f4b-113">Primary Server</span></span>

<span data-ttu-id="f6f4b-114">O *servidor primário* é o servidor autoritativo para a zona.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-114">The *primary server* is the authoritative server for the zone.</span></span> <span data-ttu-id="f6f4b-115">Todas as tarefas administrativas associadas à zona (como a criação de subdomínios dentro da zona ou outras tarefas administrativas semelhantes) devem ser executadas no servidor primário.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-115">All administrative tasks associated with the zone (such as creating subdomains within the zone, or other similar administrative tasks) must be performed on the primary server.</span></span> <span data-ttu-id="f6f4b-116">Além disso, todas as alterações associadas à zona ou quaisquer modificações ou inclusões em RRs nos arquivos de zona devem ser feitas no servidor primário.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-116">In addition, any changes associated with the zone or any modifications or additions to RRs in the zone files must be made on the primary server.</span></span> <span data-ttu-id="f6f4b-117">Para qualquer zona, há um servidor primário, exceto quando você integra os serviços do Active Directory e o servidor DNS da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-117">For any given zone, there is one primary server, except when you integrate Active Directory services and Microsoft DNS Server.</span></span>

## <a name="secondary-servers"></a><span data-ttu-id="f6f4b-118">Servidores secundários</span><span class="sxs-lookup"><span data-stu-id="f6f4b-118">Secondary Servers</span></span>

<span data-ttu-id="f6f4b-119">Os *servidores secundários* são servidores DNS de backup.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-119">*Secondary servers* are backup DNS Servers.</span></span> <span data-ttu-id="f6f4b-120">Os servidores secundários recebem todos os arquivos de zona dos arquivos de zona do servidor primário em uma transferência de zona.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-120">Secondary servers receive all of their zone files from the primary server zone files in a zone transfer.</span></span> <span data-ttu-id="f6f4b-121">Vários servidores secundários podem existir para qualquer zona específica, tanto quanto necessário para fornecer [*balanceamento de carga*](l-gly.md), [*tolerância a falhas*](f-gly.md)e redução de tráfego.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-121">Multiple secondary servers can exist for any given zone — as many as necessary to provide [*load balancing*](l-gly.md), [*fault tolerance*](f-gly.md), and traffic reduction.</span></span> <span data-ttu-id="f6f4b-122">Além disso, qualquer servidor DNS específico pode ser um servidor secundário para várias zonas.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-122">Additionally, any given DNS Server can be a secondary server for multiple zones.</span></span>

<span data-ttu-id="f6f4b-123">Além dos servidores DNS primários e secundários, outras funções de servidor DNS podem ser usadas quando esses servidores são apropriados para uma infraestrutura de DNS.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-123">In addition to primary and secondary DNS Servers, additional DNS Server roles can be used when such servers are appropriate for a DNS infrastructure.</span></span> <span data-ttu-id="f6f4b-124">Esses servidores adicionais são servidores de cache e [*encaminhadores*](f-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f6f4b-124">These additional servers are caching servers and [*forwarders*](f-gly.md).</span></span>

## <a name="caching-servers"></a><span data-ttu-id="f6f4b-125">Servidores de cache</span><span class="sxs-lookup"><span data-stu-id="f6f4b-125">Caching Servers</span></span>

<span data-ttu-id="f6f4b-126">[*Servidores de cache*](c-gly.md), também conhecidos como servidores somente de cache, são executados como seu nome sugere; Eles fornecem somente o serviço de consulta em cache para respostas DNS.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-126">[*Caching servers*](c-gly.md), also known as caching-only servers, perform as their name suggests; they provide only cached-query service for DNS responses.</span></span> <span data-ttu-id="f6f4b-127">Em vez de manter arquivos de zona como outros servidores secundários, o cache de servidores DNS executa consultas, armazena em cache as respostas e retorna os resultados para o cliente de consulta.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-127">Rather than maintaining zone files like other secondary servers do, caching DNS Servers perform queries, cache the answers, and return the results to the querying client.</span></span> <span data-ttu-id="f6f4b-128">A principal diferença entre servidores de cache e outros servidores secundários é que outros servidores secundários mantêm arquivos de zona (e fazem transferências de zona quando apropriado, gerando assim o tráfego de rede associado à transferência), servidores de cache não.</span><span class="sxs-lookup"><span data-stu-id="f6f4b-128">The primary difference between caching servers and other secondary servers is that other secondary servers maintain zone files (and do zone transfers when appropriate, thereby generating network traffic associated with the transfer), caching servers do not.</span></span>

 

 




