---
description: As estruturas a seguir dão suporte às funções de API de DRT (tabela de roteamento distribuído).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Estruturas de tabela de roteamento distribuído
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764635"
---
# <a name="distributed-routing-table-structures"></a><span data-ttu-id="9bfa3-103">Estruturas de tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="9bfa3-103">Distributed Routing Table Structures</span></span>

<span data-ttu-id="9bfa3-104">As estruturas a seguir dão suporte às funções de API de DRT (tabela de roteamento distribuído).</span><span class="sxs-lookup"><span data-stu-id="9bfa3-104">The following structures support the Distributed Routing Table (DRT) API functions.</span></span>



| <span data-ttu-id="9bfa3-105">Estrutura</span><span class="sxs-lookup"><span data-stu-id="9bfa3-105">Structure</span></span>                                                  | <span data-ttu-id="9bfa3-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bfa3-106">Description</span></span>                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bfa3-107">**dados de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="9bfa3-107">**DRT\_DATA**</span></span>](/windows/desktop/api/drt/ns-drt-drt_data)                              | <span data-ttu-id="9bfa3-108">Contém um blob de dados.</span><span class="sxs-lookup"><span data-stu-id="9bfa3-108">Contains a data blob.</span></span> <span data-ttu-id="9bfa3-109">Essa estrutura é usada por várias funções DRT.</span><span class="sxs-lookup"><span data-stu-id="9bfa3-109">This structure is used by several DRT functions.</span></span>                                                                                                                   |
| [<span data-ttu-id="9bfa3-110">**registro de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="9bfa3-110">**DRT\_REGISTRATION**</span></span>](/windows/desktop/api/drt/ns-drt-drt_registration)              | <span data-ttu-id="9bfa3-111">Contém o registro de chave.</span><span class="sxs-lookup"><span data-stu-id="9bfa3-111">Contains the key registration.</span></span> <span data-ttu-id="9bfa3-112">Esse é um membro da estrutura [**de \_ \_ resultados da pesquisa DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) e é um argumento passado para [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey).</span><span class="sxs-lookup"><span data-stu-id="9bfa3-112">This is a member of the [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) structure and is an argument passed to [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey).</span></span> |
| [<span data-ttu-id="9bfa3-113">**\_endereço DRT**</span><span class="sxs-lookup"><span data-stu-id="9bfa3-113">**DRT\_ADDRESS**</span></span>](/windows/desktop/api/drt/ns-drt-drt_address)                        | <span data-ttu-id="9bfa3-114">Contém informações de ponto de extremidade sobre um nó DRT que participou de uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9bfa3-114">Contains endpoint information about a DRT node that participated in a search.</span></span> <span data-ttu-id="9bfa3-115">Essas informações se destinam ao uso na depuração de problemas de conectividade.</span><span class="sxs-lookup"><span data-stu-id="9bfa3-115">This information is intended for use in debugging connectivity problems.</span></span>                                   |
| [<span data-ttu-id="9bfa3-116">**\_lista de endereços DRT \_**</span><span class="sxs-lookup"><span data-stu-id="9bfa3-116">**DRT\_ADDRESS\_LIST**</span></span>](/windows/desktop/api/drt/ns-drt-drt_address_list)             | <span data-ttu-id="9bfa3-117">Contém um conjunto de estruturas de [**\_ endereço DRT**](/windows/desktop/api/drt/ns-drt-drt_address) que representa os nós contatados durante uma pesquisa de uma chave.</span><span class="sxs-lookup"><span data-stu-id="9bfa3-117">Contains a set of [**DRT\_ADDRESS**](/windows/desktop/api/drt/ns-drt-drt_address) structures representing the nodes contacted during a search for a key.</span></span>                                                             |
| [<span data-ttu-id="9bfa3-118">**\_provedor de segurança DRT \_**</span><span class="sxs-lookup"><span data-stu-id="9bfa3-118">**DRT\_SECURITY\_PROVIDER**</span></span>](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | <span data-ttu-id="9bfa3-119">Define a interface que deve ser implementada por um provedor de segurança.</span><span class="sxs-lookup"><span data-stu-id="9bfa3-119">Defines the interface that must be implemented by a security provider.</span></span>                                                                                                                   |
| [<span data-ttu-id="9bfa3-120">**\_provedor de inicialização DRT \_**</span><span class="sxs-lookup"><span data-stu-id="9bfa3-120">**DRT\_BOOTSTRAP\_PROVIDER**</span></span>](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | <span data-ttu-id="9bfa3-121">Define a interface que deve ser implementada por um provedor de inicialização.</span><span class="sxs-lookup"><span data-stu-id="9bfa3-121">Defines the interface that must be implemented by a bootstrap provider.</span></span>                                                                                                                  |
| [<span data-ttu-id="9bfa3-122">**configurações de DRT \_**</span><span class="sxs-lookup"><span data-stu-id="9bfa3-122">**DRT\_SETTINGS**</span></span>](/windows/desktop/api/drt/ns-drt-drt_settings)                      | <span data-ttu-id="9bfa3-123">Define as configurações de DRT na inicialização.</span><span class="sxs-lookup"><span data-stu-id="9bfa3-123">Defines DRT settings at initialization.</span></span> <span data-ttu-id="9bfa3-124">Essa estrutura é passada como um argumento para [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).</span><span class="sxs-lookup"><span data-stu-id="9bfa3-124">This structure is passed as an argument to [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).</span></span>                                                                           |
| [<span data-ttu-id="9bfa3-125">**\_informações de pesquisa DRT \_**</span><span class="sxs-lookup"><span data-stu-id="9bfa3-125">**DRT\_SEARCH\_INFO**</span></span>](/windows/desktop/api/drt/ns-drt-drt_search_info)               | <span data-ttu-id="9bfa3-126">Define uma consulta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9bfa3-126">Defines a search query.</span></span> <span data-ttu-id="9bfa3-127">Essa estrutura é passada como um argumento para [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).</span><span class="sxs-lookup"><span data-stu-id="9bfa3-127">This structure is passed as an argument to [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).</span></span>                                                                             |
| [<span data-ttu-id="9bfa3-128">**\_resultado da pesquisa DRT \_**</span><span class="sxs-lookup"><span data-stu-id="9bfa3-128">**DRT\_SEARCH\_RESULT**</span></span>](/windows/desktop/api/drt/ns-drt-drt_search_result)           | <span data-ttu-id="9bfa3-129">Contém um resultado de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="9bfa3-129">Contains a search result.</span></span> <span data-ttu-id="9bfa3-130">Essa estrutura é retornada por [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).</span><span class="sxs-lookup"><span data-stu-id="9bfa3-130">This structure is returned by [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).</span></span>                                                                                |
| [<span data-ttu-id="9bfa3-131">**\_dados de evento DRT \_**</span><span class="sxs-lookup"><span data-stu-id="9bfa3-131">**DRT\_EVENT\_DATA**</span></span>](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | <span data-ttu-id="9bfa3-132">Contém os dados de evento retornados chamando [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) depois que um aplicativo recebe um sinal de evento.</span><span class="sxs-lookup"><span data-stu-id="9bfa3-132">Contains the event data returned by calling [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) after an application receives an event signal.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="9bfa3-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9bfa3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bfa3-134">Enumerações de tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="9bfa3-134">Distributed Routing Table Enumerations</span></span>](distributed-routing-table-enumerations.md)
</dt> <dt>

[<span data-ttu-id="9bfa3-135">Funções de tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="9bfa3-135">Distributed Routing Table Functions</span></span>](distributed-routing-table-functions.md)
</dt> <dt>

[<span data-ttu-id="9bfa3-136">Referência de API de Tabela de roteamento distribuído</span><span class="sxs-lookup"><span data-stu-id="9bfa3-136">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



