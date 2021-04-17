---
description: As seguintes enumerações dão suporte à API de DRT (tabela de roteamento distribuído).
ms.assetid: 38ce95a0-1603-42c2-8a5e-4370f52c8fc9
title: Enumerações de tabela de roteamento distribuído
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c432b156a9299a9f70026a394a6fd97f06528a25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754517"
---
# <a name="distributed-routing-table-enumerations"></a><span data-ttu-id="67965-103">Enumerações de tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="67965-103">Distributed Routing Table Enumerations</span></span>

<span data-ttu-id="67965-104">As seguintes enumerações dão suporte à API de DRT (tabela de roteamento distribuído).</span><span class="sxs-lookup"><span data-stu-id="67965-104">The following enumerations support the Distributed Routing Table (DRT) API.</span></span>



| <span data-ttu-id="67965-105">Enumeração</span><span class="sxs-lookup"><span data-stu-id="67965-105">Enumeration</span></span>                                                            | <span data-ttu-id="67965-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="67965-106">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="67965-107">**escopo de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="67965-107">**DRT\_SCOPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_scope)                                        | <span data-ttu-id="67965-108">Define o conjunto de escopos IPv6 no qual a DRT operará ao usar o transporte UDP IPv6 criado pelo [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport).</span><span class="sxs-lookup"><span data-stu-id="67965-108">Defines the set of IPv6 scopes in which DRT will operate when using the IPv6 UDP transport created by [**DrtCreateIpv6UdpTransport**](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport).</span></span> |
| [<span data-ttu-id="67965-109">**\_sinalizadores de endereço DRT \_**</span><span class="sxs-lookup"><span data-stu-id="67965-109">**DRT\_ADDRESS\_FLAGS**</span></span>](/windows/desktop/api/drt/ne-drt-drt_address_flags)                       | <span data-ttu-id="67965-110">Define o conjunto de respostas que podem ser retornadas por um nó intermediário ao executar uma pesquisa de uma chave.</span><span class="sxs-lookup"><span data-stu-id="67965-110">Defines the set of responses that may be returned by an intermediate node when performing a search for a key.</span></span>                                                         |
| [<span data-ttu-id="67965-111">**STATUS de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="67965-111">**DRT\_STATUS**</span></span>](/windows/desktop/api/drt/ne-drt-drt_status)                                      | <span data-ttu-id="67965-112">Define a possível conectividade e os Estados de erro de um nó local.</span><span class="sxs-lookup"><span data-stu-id="67965-112">Defines the possible connectivity and error states of a local node.</span></span>                                                                                                   |
| [<span data-ttu-id="67965-113">**\_tipo de correspondência DRT \_**</span><span class="sxs-lookup"><span data-stu-id="67965-113">**DRT\_MATCH\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_match_type)                             | <span data-ttu-id="67965-114">Define a exata dos resultados retornados quando uma pesquisa é executada.</span><span class="sxs-lookup"><span data-stu-id="67965-114">Defines the exactness of results returned when a search is performed.</span></span>                                                                                                 |
| [<span data-ttu-id="67965-115">**\_tipo de alteração de chave de folha de \_ \_ \_ tipos DRT**</span><span class="sxs-lookup"><span data-stu-id="67965-115">**DRT\_LEAFSET\_KEY\_CHANGE\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_leafset_key_change_type) | <span data-ttu-id="67965-116">Define o conjunto de tipos de alteração que podem ser executados em um nó de conjunto de folha local no cache DRT local.</span><span class="sxs-lookup"><span data-stu-id="67965-116">Defines the set of change types that can be performed on a local leaf set node in the local DRT cache.</span></span>                                                                |
| [<span data-ttu-id="67965-117">**\_tipo de evento DRT \_**</span><span class="sxs-lookup"><span data-stu-id="67965-117">**DRT\_EVENT\_TYPE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_event_type)                             | <span data-ttu-id="67965-118">Define o conjunto de eventos que podem ser gerados pelo DRT.</span><span class="sxs-lookup"><span data-stu-id="67965-118">Defines the set of events that can be raised by the DRT.</span></span>                                                                                                              |
| [<span data-ttu-id="67965-119">**\_modo de segurança DRT \_**</span><span class="sxs-lookup"><span data-stu-id="67965-119">**DRT\_SECURITY\_MODE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_security_mode)                       | <span data-ttu-id="67965-120">Define os possíveis modos de segurança do DRT.</span><span class="sxs-lookup"><span data-stu-id="67965-120">Defines the possible security modes of the DRT.</span></span> <span data-ttu-id="67965-121">Essa enumeração é um campo da estrutura [**de \_ configurações de DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .</span><span class="sxs-lookup"><span data-stu-id="67965-121">This enumeration is a field of the [**DRT\_SETTINGS**](/windows/desktop/api/drt/ns-drt-drt_settings) structure.</span></span>                                   |
| [<span data-ttu-id="67965-122">**\_estado de registro DRT \_**</span><span class="sxs-lookup"><span data-stu-id="67965-122">**DRT\_REGISTRATION\_STATE**</span></span>](/windows/desktop/api/drt/ne-drt-drt_registration_state)             | <span data-ttu-id="67965-123">Define o estado de uma chave registrada.</span><span class="sxs-lookup"><span data-stu-id="67965-123">Defines the state of a registered key.</span></span>                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="67965-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67965-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67965-125">Estruturas de tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="67965-125">Distributed Routing Table Structures</span></span>](distributed-routing-table-structures.md)
</dt> <dt>

[<span data-ttu-id="67965-126">Funções de tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="67965-126">Distributed Routing Table Functions</span></span>](distributed-routing-table-functions.md)
</dt> <dt>

[<span data-ttu-id="67965-127">Referência de API de Tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="67965-127">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



