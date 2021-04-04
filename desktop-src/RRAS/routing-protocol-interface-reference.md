---
title: Referência da interface do protocolo de roteamento
description: Esta documentação descreve as funções e estruturas que são usadas para implementar um protocolo de roteamento como uma DLL de modo de usuário.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- Serviço de roteamento e acesso remoto RRAS, interface do protocolo de roteamento, referência
- Interface do protocolo de roteamento RRAS, referência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9341dd8dbd304da84fd675aee92e378a44271056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822608"
---
# <a name="routing-protocol-interface-reference"></a><span data-ttu-id="1938d-105">Referência da interface do protocolo de roteamento</span><span class="sxs-lookup"><span data-stu-id="1938d-105">Routing Protocol Interface Reference</span></span>

<span data-ttu-id="1938d-106">Esta documentação descreve as funções e estruturas que são usadas para implementar um protocolo de roteamento como uma DLL de modo de usuário.</span><span class="sxs-lookup"><span data-stu-id="1938d-106">This documentation describes the functions and structures that are used to implement a routing protocol as a user-mode DLL.</span></span>

<span data-ttu-id="1938d-107">MPR50 deve ser definido no arquivo Make para o protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="1938d-107">MPR50 should be defined in the make file for the routing protocol.</span></span>

<span data-ttu-id="1938d-108">A macro **sizeof \_ IP \_ Binding (x)** calcula o tamanho, em bytes, de uma estrutura [**de \_ \_ \_ informações de associação de adaptador IP**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) que contém o número de endereços IP.</span><span class="sxs-lookup"><span data-stu-id="1938d-108">The **SIZEOF\_IP\_BINDING(x)** macro computes the size, in bytes, of an [**IP\_ADAPTER\_BINDING\_INFO**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) structure that contains the number of IP addresses.</span></span>

<span data-ttu-id="1938d-109">Esses elementos de referência são descritos nos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="1938d-109">These reference elements are described in the following topics:</span></span>

-   [<span data-ttu-id="1938d-110">Funções da interface do protocolo de roteamento</span><span class="sxs-lookup"><span data-stu-id="1938d-110">Routing Protocol Interface Functions</span></span>](routing-protocol-interface-functions.md)
-   [<span data-ttu-id="1938d-111">Estruturas de interface de protocolo de roteamento</span><span class="sxs-lookup"><span data-stu-id="1938d-111">Routing Protocol Interface Structures</span></span>](routing-protocol-interface-structures.md)
-   [<span data-ttu-id="1938d-112">Gerenciamento de tabela de serviço IPX</span><span class="sxs-lookup"><span data-stu-id="1938d-112">IPX Service Table Management</span></span>](ipx-service-table-management.md)

 

 




