---
title: Enumerando grupos (RRAS)
description: A tabela a seguir resume uma série de etapas em uma interação entre um protocolo de roteamento e o Gerenciador do grupo de multicast.
ms.assetid: 30a81946-fa60-4424-9a16-a9b4dfe1961e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d3860c6876ed6ea5caef4941efcdd949eb9890d
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104453795"
---
# <a name="enumerating-groups"></a><span data-ttu-id="66248-103">Enumerando grupos</span><span class="sxs-lookup"><span data-stu-id="66248-103">Enumerating Groups</span></span>

<span data-ttu-id="66248-104">A tabela a seguir resume uma série de etapas em uma interação entre um protocolo de roteamento e o Gerenciador do grupo de multicast.</span><span class="sxs-lookup"><span data-stu-id="66248-104">The following table summarizes a series of steps in an interaction between a routing protocol and the multicast group manager.</span></span> <span data-ttu-id="66248-105">A primeira coluna descreve as ações que o protocolo de roteamento executa e as respostas do protocolo de roteamento para o Gerenciador do grupo de multicast.</span><span class="sxs-lookup"><span data-stu-id="66248-105">The first column describes the actions that the routing protocol performs and the routing protocol's responses to the multicast group manager.</span></span> <span data-ttu-id="66248-106">A segunda coluna descreve as respostas do Gerenciador do grupo de multicast para o protocolo de roteamento.</span><span class="sxs-lookup"><span data-stu-id="66248-106">The second column describes the multicast group manager's responses to the routing protocol.</span></span> <span data-ttu-id="66248-107">A terceira coluna apresenta informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="66248-107">The third column presents any additional information.</span></span>

<span data-ttu-id="66248-108">Cada linha da tabela representa uma etapa.</span><span class="sxs-lookup"><span data-stu-id="66248-108">Each row of the table represents one step.</span></span>



| <span data-ttu-id="66248-109">Ação do protocolo de roteamento</span><span class="sxs-lookup"><span data-stu-id="66248-109">Routing protocol action</span></span>                                                                                                                                                    | <span data-ttu-id="66248-110">Ação do Gerenciador de grupo multicast</span><span class="sxs-lookup"><span data-stu-id="66248-110">Multicast group manager action</span></span>                                                                                                                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66248-111">Obtenha um identificador para uma enumeração usando a função [**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart) .</span><span class="sxs-lookup"><span data-stu-id="66248-111">Obtain a handle to an enumeration using the [**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart) function.</span></span>                                                         | <span data-ttu-id="66248-112">Retornar um identificador.</span><span class="sxs-lookup"><span data-stu-id="66248-112">Return a handle.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="66248-113">Obtenha um ou mais grupos usando a função [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) .</span><span class="sxs-lookup"><span data-stu-id="66248-113">Obtain one or more groups using the [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) function.</span></span>                                                             | <span data-ttu-id="66248-114">Retornar quantos grupos couberem no buffer fornecido pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="66248-114">Return as many groups as fit in the buffer supplied by the client.</span></span> <span data-ttu-id="66248-115">Se nenhum grupo puder ser retornado no buffer fornecido, \_ \_ o buffer de erro de retorno será insuficiente e o tamanho do buffer necessário para retornar um grupo.</span><span class="sxs-lookup"><span data-stu-id="66248-115">If no groups can be returned in the supplied buffer, return ERROR\_INSUFFICIENT\_BUFFER and the size of the buffer that is needed to return one group.</span></span><br/> <span data-ttu-id="66248-116">Retorne o erro \_ sem \_ mais \_ itens quando não houver mais grupos.</span><span class="sxs-lookup"><span data-stu-id="66248-116">Return ERROR\_NO\_MORE\_ITEMS when there are no more groups.</span></span><br/> |
| <span data-ttu-id="66248-117">Se \_ o buffer insuficiente de erro \_ for recebido, chame a função [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) novamente usando um buffer do tamanho indicado.</span><span class="sxs-lookup"><span data-stu-id="66248-117">If ERROR\_INSUFFICIENT\_BUFFER is received, call the [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) function again using a buffer of the size indicated.</span></span> |                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="66248-118">Continue chamando a função [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) até que o erro \_ nenhum \_ \_ item seja recebido.</span><span class="sxs-lookup"><span data-stu-id="66248-118">Continue calling the [**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext) function until ERROR\_NO\_MORE\_ITEMS is received.</span></span>                                   |                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="66248-119">Finalize o processo de enumeração usando a função [**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend) .</span><span class="sxs-lookup"><span data-stu-id="66248-119">End the enumeration process using the [**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend) function.</span></span>                                                                   | <span data-ttu-id="66248-120">Destrua o identificador.</span><span class="sxs-lookup"><span data-stu-id="66248-120">Destroy the handle.</span></span>                                                                                                                                                                                                                                                                                          |



 

 

 





