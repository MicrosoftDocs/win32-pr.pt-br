---
title: Sinalizadores de enumeração
description: Sinalizadores de enumeração
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Enumeração
- Sinalizadores de enumeração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1cbec08496ccd6338de77ebdddf76547a48258
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916281"
---
# <a name="enumeration-flags"></a><span data-ttu-id="7087c-105">Sinalizadores de enumeração</span><span class="sxs-lookup"><span data-stu-id="7087c-105">Enumeration Flags</span></span>



| <span data-ttu-id="7087c-106">Constante</span><span class="sxs-lookup"><span data-stu-id="7087c-106">Constant</span></span>               | <span data-ttu-id="7087c-107">Valor</span><span class="sxs-lookup"><span data-stu-id="7087c-107">Value</span></span>      | <span data-ttu-id="7087c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="7087c-108">Description</span></span>                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7087c-109">\_início da enumeração do RTM \_</span><span class="sxs-lookup"><span data-stu-id="7087c-109">RTM\_ENUM\_START</span></span>       | <span data-ttu-id="7087c-110">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7087c-110">0x00000000</span></span> | <span data-ttu-id="7087c-111">Enumere rotas ou destinos começando em 0/0.</span><span class="sxs-lookup"><span data-stu-id="7087c-111">Enumerate routes or destinations starting at 0/0.</span></span>                                                                                                         |
| <span data-ttu-id="7087c-112">\_Enumeração RTM \_ Next</span><span class="sxs-lookup"><span data-stu-id="7087c-112">RTM\_ENUM\_NEXT</span></span>        | <span data-ttu-id="7087c-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="7087c-113">0x00000001</span></span> | <span data-ttu-id="7087c-114">Enumere rotas ou destinos começando no comprimento de endereço/máscara especificado (como 10/8).</span><span class="sxs-lookup"><span data-stu-id="7087c-114">Enumerate routes or destinations starting at the specified address/mask length (such as 10/8).</span></span> <span data-ttu-id="7087c-115">A enumeração continua no final da tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="7087c-115">The enumeration continues to the end of the routing table.</span></span> |
| <span data-ttu-id="7087c-116">\_intervalo de enumeração de RTM \_</span><span class="sxs-lookup"><span data-stu-id="7087c-116">RTM\_ENUM\_RANGE</span></span>       | <span data-ttu-id="7087c-117">0x00000002</span><span class="sxs-lookup"><span data-stu-id="7087c-117">0x00000002</span></span> | <span data-ttu-id="7087c-118">Enumere rotas ou destinos na subárvore especificada especificada pelo comprimento de endereço/máscara (como 10/8).</span><span class="sxs-lookup"><span data-stu-id="7087c-118">Enumerate routes or destinations in the specified subtree specified by the address/mask length (such as 10/8).</span></span>                                            |
| <span data-ttu-id="7087c-119">\_ \_ todos os \_ dests enum de RTM</span><span class="sxs-lookup"><span data-stu-id="7087c-119">RTM\_ENUM\_ALL\_DESTS</span></span>  | <span data-ttu-id="7087c-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7087c-120">0x00000000</span></span> | <span data-ttu-id="7087c-121">Retornar todos os destinos.</span><span class="sxs-lookup"><span data-stu-id="7087c-121">Return all destinations.</span></span>                                                                                                                                  |
| <span data-ttu-id="7087c-122">todos \_ os \_ dests de enumeração do RTM \_</span><span class="sxs-lookup"><span data-stu-id="7087c-122">RTM\_ENUM\_OWN\_DESTS</span></span>  | <span data-ttu-id="7087c-123">0x01000000</span><span class="sxs-lookup"><span data-stu-id="7087c-123">0x01000000</span></span> | <span data-ttu-id="7087c-124">Retornar somente os destinos que o cliente possui.</span><span class="sxs-lookup"><span data-stu-id="7087c-124">Return only those destinations that the client owns.</span></span>                                                                                                      |
| <span data-ttu-id="7087c-125">\_ \_ todas as rotas de enumeração do RTM \_</span><span class="sxs-lookup"><span data-stu-id="7087c-125">RTM\_ENUM\_ALL\_ROUTES</span></span> | <span data-ttu-id="7087c-126">0x00000000</span><span class="sxs-lookup"><span data-stu-id="7087c-126">0x00000000</span></span> | <span data-ttu-id="7087c-127">Retornar todas as rotas.</span><span class="sxs-lookup"><span data-stu-id="7087c-127">Return all routes.</span></span>                                                                                                                                        |
| <span data-ttu-id="7087c-128">\_rotas de enumeração do RTM \_ \_</span><span class="sxs-lookup"><span data-stu-id="7087c-128">RTM\_ENUM\_OWN\_ROUTES</span></span> | <span data-ttu-id="7087c-129">0x00010000</span><span class="sxs-lookup"><span data-stu-id="7087c-129">0x00010000</span></span> | <span data-ttu-id="7087c-130">Retornar somente as rotas que o cliente possui.</span><span class="sxs-lookup"><span data-stu-id="7087c-130">Return only those routes that the client owns.</span></span>                                                                                                            |



 

 

 




