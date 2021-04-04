---
title: Sinalizadores de consulta de tabela de roteamento
description: Use essas constantes para consultas de tabela de roteador.
ms.assetid: 345a8edc-c2aa-483e-8685-15a692bbfd56
keywords:
- Sinalizadores de consulta de tabela de roteamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b37ab647efb192e29aae421e02bef1dec065e3b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823073"
---
# <a name="routing-table-query-flags"></a><span data-ttu-id="d0e18-104">Sinalizadores de consulta de tabela de roteamento</span><span class="sxs-lookup"><span data-stu-id="d0e18-104">Routing Table Query Flags</span></span>

<span data-ttu-id="d0e18-105">Use essas constantes para consultas de tabela de roteador.</span><span class="sxs-lookup"><span data-stu-id="d0e18-105">Use these constants for router table queries.</span></span>



| <span data-ttu-id="d0e18-106">Constante</span><span class="sxs-lookup"><span data-stu-id="d0e18-106">Constant</span></span>              | <span data-ttu-id="d0e18-107">Valor</span><span class="sxs-lookup"><span data-stu-id="d0e18-107">Value</span></span>      | <span data-ttu-id="d0e18-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d0e18-108">Description</span></span>                                                                |
|-----------------------|------------|----------------------------------------------------------------------------|
| <span data-ttu-id="d0e18-109">correspondência de RTM \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="d0e18-109">RTM\_MATCH\_NONE</span></span>      | <span data-ttu-id="d0e18-110">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0e18-110">0x00000000</span></span> | <span data-ttu-id="d0e18-111">Corresponde a nenhum dos critérios; todas as rotas para o destino são retornadas.</span><span class="sxs-lookup"><span data-stu-id="d0e18-111">Matches none of the criteria; all routes for the destination are returned.</span></span> |
| <span data-ttu-id="d0e18-112">\_proprietário da correspondência RTM \_</span><span class="sxs-lookup"><span data-stu-id="d0e18-112">RTM\_MATCH\_OWNER</span></span>     | <span data-ttu-id="d0e18-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d0e18-113">0x00000001</span></span> | <span data-ttu-id="d0e18-114">Corresponde a rotas com o mesmo proprietário.</span><span class="sxs-lookup"><span data-stu-id="d0e18-114">Matches routes with same owner.</span></span>                                            |
| <span data-ttu-id="d0e18-115">\_vizinho de correspondência RTM \_</span><span class="sxs-lookup"><span data-stu-id="d0e18-115">RTM\_MATCH\_NEIGHBOUR</span></span> | <span data-ttu-id="d0e18-116">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d0e18-116">0x00000002</span></span> | <span data-ttu-id="d0e18-117">Faz a correspondência de rotas com o mesmo vizinho.</span><span class="sxs-lookup"><span data-stu-id="d0e18-117">Matches routes with the same neighbor.</span></span>                                     |
| <span data-ttu-id="d0e18-118">\_correspondência RTM \_ pref</span><span class="sxs-lookup"><span data-stu-id="d0e18-118">RTM\_MATCH\_PREF</span></span>      | <span data-ttu-id="d0e18-119">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d0e18-119">0x00000004</span></span> | <span data-ttu-id="d0e18-120">Faz a correspondência de rotas que têm a mesma preferência.</span><span class="sxs-lookup"><span data-stu-id="d0e18-120">Matches routes that have the same preference.</span></span>                              |
| <span data-ttu-id="d0e18-121">\_NEXTHOP de correspondência RTM \_</span><span class="sxs-lookup"><span data-stu-id="d0e18-121">RTM\_MATCH\_NEXTHOP</span></span>   | <span data-ttu-id="d0e18-122">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d0e18-122">0x00000008</span></span> | <span data-ttu-id="d0e18-123">Faz a correspondência de rotas que têm o mesmo salto seguinte.</span><span class="sxs-lookup"><span data-stu-id="d0e18-123">Matches routes that have the same next hop.</span></span>                                |
| <span data-ttu-id="d0e18-124">\_interface de correspondência RTM \_</span><span class="sxs-lookup"><span data-stu-id="d0e18-124">RTM\_MATCH\_INTERFACE</span></span> | <span data-ttu-id="d0e18-125">0x00000010</span><span class="sxs-lookup"><span data-stu-id="d0e18-125">0x00000010</span></span> | <span data-ttu-id="d0e18-126">Faz a correspondência de rotas que estão na mesma interface.</span><span class="sxs-lookup"><span data-stu-id="d0e18-126">Matches routes that are on the same interface.</span></span>                             |
| <span data-ttu-id="d0e18-127">\_correspondência RTM \_ completa</span><span class="sxs-lookup"><span data-stu-id="d0e18-127">RTM\_MATCH\_FULL</span></span>      | <span data-ttu-id="d0e18-128">0x0000FFFF</span><span class="sxs-lookup"><span data-stu-id="d0e18-128">0x0000FFFF</span></span> | <span data-ttu-id="d0e18-129">Faz a correspondência de rotas com todos os critérios.</span><span class="sxs-lookup"><span data-stu-id="d0e18-129">Matches routes with all criteria.</span></span>                                          |
| <span data-ttu-id="d0e18-130">\_melhor \_ protocolo RTM</span><span class="sxs-lookup"><span data-stu-id="d0e18-130">RTM\_BEST\_PROTOCOL</span></span>   | <span data-ttu-id="d0e18-131">0</span><span class="sxs-lookup"><span data-stu-id="d0e18-131">0</span></span>          | <span data-ttu-id="d0e18-132">Retorna uma rota independentemente de qual protocolo possui.</span><span class="sxs-lookup"><span data-stu-id="d0e18-132">Returns a route regardless of which protocol owns it.</span></span>                      |
| <span data-ttu-id="d0e18-133">RTM \_ este \_ protocolo</span><span class="sxs-lookup"><span data-stu-id="d0e18-133">RTM\_THIS\_PROTOCOL</span></span>   | <span data-ttu-id="d0e18-134">~0</span><span class="sxs-lookup"><span data-stu-id="d0e18-134">~0</span></span>         | <span data-ttu-id="d0e18-135">Retorna a melhor rota para o protocolo de chamada.</span><span class="sxs-lookup"><span data-stu-id="d0e18-135">Returns the best route for the calling protocol.</span></span>                           |



 

 

 




