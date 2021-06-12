---
title: Servidores DNS
description: Saiba mais sobre servidores DNS. Um Servidor DNS é um computador que conclui o processo de resolução de nomes no DNS.
ms.assetid: c7ce6e46-491c-482e-8d72-a79b911c3f68
keywords:
- Servidores DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fe2415c50cdd2472b20e8f14123afa2aa919d26
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011249"
---
# <a name="dns-servers"></a><span data-ttu-id="58c52-105">Servidores DNS</span><span class="sxs-lookup"><span data-stu-id="58c52-105">DNS Servers</span></span>

<span data-ttu-id="58c52-106">Um *Servidor DNS* é um computador que conclui o processo de resolução de nomes no DNS.</span><span class="sxs-lookup"><span data-stu-id="58c52-106">A *DNS Server* is a computer that completes the process of name resolution in DNS.</span></span> <span data-ttu-id="58c52-107">Os Servidores DNS [*contêm arquivos de zona*](z-gly.md) que permitem resolver nomes para endereços IP e endereços IP para nomes.</span><span class="sxs-lookup"><span data-stu-id="58c52-107">DNS Servers contain [*zone files*](z-gly.md) that enable them to resolve names to IP addresses and IP addresses to names.</span></span> <span data-ttu-id="58c52-108">Quando consultado, um servidor DNS responderá de uma das três maneiras:</span><span class="sxs-lookup"><span data-stu-id="58c52-108">When queried, a DNS Server will respond in one of three ways:</span></span>

-   <span data-ttu-id="58c52-109">O servidor retorna os dados solicitados de resolução de nome ou resolução de IP.</span><span class="sxs-lookup"><span data-stu-id="58c52-109">The server returns the requested name-resolution or IP-resolution data.</span></span>
-   <span data-ttu-id="58c52-110">O servidor retorna um ponteiro para outro servidor DNS que pode fazer o serviço da solicitação.</span><span class="sxs-lookup"><span data-stu-id="58c52-110">The server returns a pointer to another DNS Server that can service the request.</span></span>
-   <span data-ttu-id="58c52-111">O servidor indica que ele não tem os dados solicitados.</span><span class="sxs-lookup"><span data-stu-id="58c52-111">The server indicates that it does not have the requested data.</span></span>

<span data-ttu-id="58c52-112">Os Servidores DNS podem, durante a preparação para retornar os dados de resolução solicitados, consultar outros Servidores DNS, mas além disso, os Servidores DNS não executam nenhuma outra operação.</span><span class="sxs-lookup"><span data-stu-id="58c52-112">DNS Servers might, during the course of preparing to return the requested resolution data, query other DNS Servers, but beyond that, DNS Servers do not perform any other operations.</span></span>

<span data-ttu-id="58c52-113">Há três tipos principais de servidores DNS : servidores primários, servidores secundários e servidores de cache.</span><span class="sxs-lookup"><span data-stu-id="58c52-113">There are three main kinds of DNS Servers — primary servers, secondary servers, and caching servers.</span></span>

## <a name="primary-server"></a><span data-ttu-id="58c52-114">Servidor Primário</span><span class="sxs-lookup"><span data-stu-id="58c52-114">Primary Server</span></span>

<span data-ttu-id="58c52-115">O *servidor primário* é o servidor autoritativo para a zona.</span><span class="sxs-lookup"><span data-stu-id="58c52-115">The *primary server* is the authoritative server for the zone.</span></span> <span data-ttu-id="58c52-116">Todas as tarefas administrativas associadas à zona (como criar subdomasins dentro da zona ou outras tarefas administrativas semelhantes) devem ser executadas no servidor primário.</span><span class="sxs-lookup"><span data-stu-id="58c52-116">All administrative tasks associated with the zone (such as creating subdomains within the zone, or other similar administrative tasks) must be performed on the primary server.</span></span> <span data-ttu-id="58c52-117">Além disso, todas as alterações associadas à zona ou quaisquer modificações ou adições a RRs nos arquivos de zona devem ser feitas no servidor primário.</span><span class="sxs-lookup"><span data-stu-id="58c52-117">In addition, any changes associated with the zone or any modifications or additions to RRs in the zone files must be made on the primary server.</span></span> <span data-ttu-id="58c52-118">Para qualquer zona, há um servidor primário, exceto quando você integra os serviços do Active Directory e o Servidor DNS da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="58c52-118">For any given zone, there is one primary server, except when you integrate Active Directory services and Microsoft DNS Server.</span></span>

## <a name="secondary-servers"></a><span data-ttu-id="58c52-119">Servidores secundários</span><span class="sxs-lookup"><span data-stu-id="58c52-119">Secondary Servers</span></span>

<span data-ttu-id="58c52-120">*Os servidores secundários* são servidores DNS de backup.</span><span class="sxs-lookup"><span data-stu-id="58c52-120">*Secondary servers* are backup DNS Servers.</span></span> <span data-ttu-id="58c52-121">Os servidores secundários recebem todos os arquivos de zona dos arquivos de zona do servidor primário em uma transferência de zona.</span><span class="sxs-lookup"><span data-stu-id="58c52-121">Secondary servers receive all of their zone files from the primary server zone files in a zone transfer.</span></span> <span data-ttu-id="58c52-122">Vários servidores secundários podem existir para qualquer zona determinada – tantos quantos necessários para fornecer balanceamento de [*carga,*](l-gly.md)tolerância a falhas [*e*](f-gly.md)redução de tráfego.</span><span class="sxs-lookup"><span data-stu-id="58c52-122">Multiple secondary servers can exist for any given zone — as many as necessary to provide [*load balancing*](l-gly.md), [*fault tolerance*](f-gly.md), and traffic reduction.</span></span> <span data-ttu-id="58c52-123">Além disso, qualquer servidor DNS específico pode ser um servidor secundário para várias zonas.</span><span class="sxs-lookup"><span data-stu-id="58c52-123">Additionally, any given DNS Server can be a secondary server for multiple zones.</span></span>

<span data-ttu-id="58c52-124">Além dos Servidores DNS primários e secundários, funções adicionais do Servidor DNS podem ser usadas quando esses servidores são apropriados para uma infraestrutura DNS.</span><span class="sxs-lookup"><span data-stu-id="58c52-124">In addition to primary and secondary DNS Servers, additional DNS Server roles can be used when such servers are appropriate for a DNS infrastructure.</span></span> <span data-ttu-id="58c52-125">Esses servidores adicionais são servidores e encaminhadores [*de cache.*](f-gly.md)</span><span class="sxs-lookup"><span data-stu-id="58c52-125">These additional servers are caching servers and [*forwarders*](f-gly.md).</span></span>

## <a name="caching-servers"></a><span data-ttu-id="58c52-126">Servidores de cache</span><span class="sxs-lookup"><span data-stu-id="58c52-126">Caching Servers</span></span>

<span data-ttu-id="58c52-127">[*Servidores de cache*](c-gly.md), também conhecidos como servidores somente cache, executam como o nome sugere; eles fornecem apenas o serviço de consulta armazenado em cache para respostas DNS.</span><span class="sxs-lookup"><span data-stu-id="58c52-127">[*Caching servers*](c-gly.md), also known as caching-only servers, perform as their name suggests; they provide only cached-query service for DNS responses.</span></span> <span data-ttu-id="58c52-128">Em vez de manter arquivos de zona como outros servidores secundários, o cache de servidores DNS executa consultas, armazena em cache as respostas e retorna os resultados para o cliente de consulta.</span><span class="sxs-lookup"><span data-stu-id="58c52-128">Rather than maintaining zone files like other secondary servers do, caching DNS Servers perform queries, cache the answers, and return the results to the querying client.</span></span> <span data-ttu-id="58c52-129">A principal diferença entre servidores de cache e outros servidores secundários é que outros servidores secundários mantêm arquivos de zona (e fazem transferências de zona quando apropriado, gerando assim o tráfego de rede associado à transferência), os servidores de cache não.</span><span class="sxs-lookup"><span data-stu-id="58c52-129">The primary difference between caching servers and other secondary servers is that other secondary servers maintain zone files (and do zone transfers when appropriate, thereby generating network traffic associated with the transfer), caching servers do not.</span></span>

 

 




