---
title: Usando ponteiros opacos
description: Geralmente, os clientes devem armazenar informações adicionais específicas do cliente sobre os destinos.
ms.assetid: e96805b0-680f-411c-a02c-2c3fda7276ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9893b3a8b8e8a69ab78f33156efbe872b86d83ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822826"
---
# <a name="using-opaque-pointers"></a><span data-ttu-id="6d49c-103">Usando ponteiros opacos</span><span class="sxs-lookup"><span data-stu-id="6d49c-103">Using Opaque Pointers</span></span>

<span data-ttu-id="6d49c-104">Geralmente, os clientes devem armazenar informações adicionais específicas do cliente sobre os destinos.</span><span class="sxs-lookup"><span data-stu-id="6d49c-104">Clients often must store additional, client-specific information about destinations.</span></span> <span data-ttu-id="6d49c-105">O Gerenciador de tabela de roteamento permite que os clientes armazenem essas informações em estruturas de destino na tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="6d49c-105">The routing table manager enables clients to store this information in destination structures in the routing table.</span></span> <span data-ttu-id="6d49c-106">As informações são armazenadas e recuperadas usando *ponteiros opacos*.</span><span class="sxs-lookup"><span data-stu-id="6d49c-106">The information is stored and retrieved by using *opaque pointers*.</span></span> <span data-ttu-id="6d49c-107">As informações armazenadas são privadas e acessíveis somente para o cliente que possui o ponteiro opaco.</span><span class="sxs-lookup"><span data-stu-id="6d49c-107">The information stored is private, and accessible only to the client that owns the opaque pointer.</span></span>

<span data-ttu-id="6d49c-108">Por exemplo, o Gerenciador de grupos de multicast mantém uma lista de entradas de encaminhamento de multicast que dependem de um destino específico.</span><span class="sxs-lookup"><span data-stu-id="6d49c-108">For example, the multicast group manager keeps a list of multicast forwarding entries that are dependent on a particular destination.</span></span> <span data-ttu-id="6d49c-109">O Gerenciador do grupo de multicast usa um ponteiro opaco nesse destino.</span><span class="sxs-lookup"><span data-stu-id="6d49c-109">The multicast group manager uses an opaque pointer in that destination.</span></span> <span data-ttu-id="6d49c-110">Em outro exemplo, um protocolo de roteamento que anuncia um destino específico pode manter informações relacionadas ao seu próprio anúncio de rota do destino usando um ponteiro opaco, mesmo que ele não tenha a melhor rota.</span><span class="sxs-lookup"><span data-stu-id="6d49c-110">In another example, a routing protocol that advertises a particular destination can keep information related to its own route advertisement of the destination using an opaque pointer, even though it does not own the best route.</span></span>

<span data-ttu-id="6d49c-111">O número de ponteiros opacos é limitado; Esses ponteiros são alocados aos clientes de acordo com a primeira vez que são atendidos.</span><span class="sxs-lookup"><span data-stu-id="6d49c-111">The number of opaque pointers is limited; these pointers are allocated to clients on a first-come, first-served basis.</span></span> <span data-ttu-id="6d49c-112">O administrador do roteador deve alocar o número correto de ponteiros durante a configuração do roteador; Portanto, os protocolos de roteamento e outros clientes devem documentar o uso de ponteiros opacos.</span><span class="sxs-lookup"><span data-stu-id="6d49c-112">The router administrator must allocate the correct number of pointers during the router configuration; therefore, routing protocols and other clients must document their use of opaque pointers.</span></span>

 

 




