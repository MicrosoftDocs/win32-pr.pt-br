---
title: Sinalizadores do próximo salto
description: Sinalizadores do próximo salto
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Avançar
- Sinalizadores do próximo salto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd672c9b083e47c3d0a7419d03ab890c1037ce5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006004"
---
# <a name="next-hop-flags"></a><span data-ttu-id="3a0ca-105">Sinalizadores do próximo salto</span><span class="sxs-lookup"><span data-stu-id="3a0ca-105">Next Hop Flags</span></span>

## <a name="next-hop-state-flags"></a><span data-ttu-id="3a0ca-106">Sinalizadores de estado do próximo salto</span><span class="sxs-lookup"><span data-stu-id="3a0ca-106">Next Hop State Flags</span></span>



| <span data-ttu-id="3a0ca-107">Constante</span><span class="sxs-lookup"><span data-stu-id="3a0ca-107">Constant</span></span>                     | <span data-ttu-id="3a0ca-108">Valor</span><span class="sxs-lookup"><span data-stu-id="3a0ca-108">Value</span></span> | <span data-ttu-id="3a0ca-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a0ca-109">Description</span></span>                              |
|------------------------------|-------|------------------------------------------|
| <span data-ttu-id="3a0ca-110">Estado de NEXTHOP do RTM \_ \_ \_ criado</span><span class="sxs-lookup"><span data-stu-id="3a0ca-110">RTM\_NEXTHOP\_STATE\_CREATED</span></span> | <span data-ttu-id="3a0ca-111">0</span><span class="sxs-lookup"><span data-stu-id="3a0ca-111">0</span></span>     | <span data-ttu-id="3a0ca-112">Indica que o próximo salto foi criado.</span><span class="sxs-lookup"><span data-stu-id="3a0ca-112">Indicates that the next hop was created.</span></span> |
| <span data-ttu-id="3a0ca-113">Estado de NEXTHOP do RTM \_ \_ \_ excluído</span><span class="sxs-lookup"><span data-stu-id="3a0ca-113">RTM\_NEXTHOP\_STATE\_DELETED</span></span> | <span data-ttu-id="3a0ca-114">1</span><span class="sxs-lookup"><span data-stu-id="3a0ca-114">1</span></span>     | <span data-ttu-id="3a0ca-115">Indica que o próximo salto foi excluído.</span><span class="sxs-lookup"><span data-stu-id="3a0ca-115">Indicates that the next hop was deleted.</span></span> |



 

## <a name="next-hop-flags"></a><span data-ttu-id="3a0ca-116">Sinalizadores do próximo salto</span><span class="sxs-lookup"><span data-stu-id="3a0ca-116">Next Hop Flags</span></span>



| <span data-ttu-id="3a0ca-117">Constante</span><span class="sxs-lookup"><span data-stu-id="3a0ca-117">Constant</span></span>                    | <span data-ttu-id="3a0ca-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3a0ca-118">Value</span></span>  | <span data-ttu-id="3a0ca-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a0ca-119">Description</span></span>                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0ca-120">sinalizadores de NEXTHOP do RTM \_ \_ \_ remotos</span><span class="sxs-lookup"><span data-stu-id="3a0ca-120">RTM\_NEXTHOP\_FLAGS\_REMOTE</span></span> | <span data-ttu-id="3a0ca-121">0x0001</span><span class="sxs-lookup"><span data-stu-id="3a0ca-121">0x0001</span></span> | <span data-ttu-id="3a0ca-122">Este próximo salto aponta para um destino remoto que não está acessível diretamente.</span><span class="sxs-lookup"><span data-stu-id="3a0ca-122">This next hop points to a remote destination that is not directly reachable.</span></span> <span data-ttu-id="3a0ca-123">Para obter o caminho completo, o cliente deve executar uma pesquisa recursiva.</span><span class="sxs-lookup"><span data-stu-id="3a0ca-123">To obtain the complete path, the client must perform a recursive lookup.</span></span> |
| <span data-ttu-id="3a0ca-124">sinalizadores de NEXTHOP do RTM \_ \_ \_ inativos</span><span class="sxs-lookup"><span data-stu-id="3a0ca-124">RTM\_NEXTHOP\_FLAGS\_DOWN</span></span>   | <span data-ttu-id="3a0ca-125">0x0002</span><span class="sxs-lookup"><span data-stu-id="3a0ca-125">0x0002</span></span> | <span data-ttu-id="3a0ca-126">Esse sinalizador é reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="3a0ca-126">This flag is reserved for future use.</span></span>                                                                                                                 |



 

## <a name="next-hop-added"></a><span data-ttu-id="3a0ca-127">Próximo salto adicionado</span><span class="sxs-lookup"><span data-stu-id="3a0ca-127">Next Hop Added</span></span>



| <span data-ttu-id="3a0ca-128">Constante</span><span class="sxs-lookup"><span data-stu-id="3a0ca-128">Constant</span></span>                  | <span data-ttu-id="3a0ca-129">Valor</span><span class="sxs-lookup"><span data-stu-id="3a0ca-129">Value</span></span> | <span data-ttu-id="3a0ca-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a0ca-130">Description</span></span>                 |
|---------------------------|-------|-----------------------------|
| <span data-ttu-id="3a0ca-131">\_ \_ nova alteração de NEXTHOP do RTM \_</span><span class="sxs-lookup"><span data-stu-id="3a0ca-131">RTM\_NEXTHOP\_CHANGE\_NEW</span></span> | <span data-ttu-id="3a0ca-132">0x01</span><span class="sxs-lookup"><span data-stu-id="3a0ca-132">0x01</span></span>  | <span data-ttu-id="3a0ca-133">Um novo salto seguinte foi criado.</span><span class="sxs-lookup"><span data-stu-id="3a0ca-133">A new next hop was created.</span></span> |



 

 

 




