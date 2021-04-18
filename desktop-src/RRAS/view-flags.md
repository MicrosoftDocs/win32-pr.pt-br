---
title: Exibir sinalizadores
description: Use os sinalizadores de exibição para controlar exibições de tabela de roteamento.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5192bf3e1acaa91412d8ae7e06d035e54af1ece6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105785394"
---
# <a name="view-flags"></a><span data-ttu-id="462f4-103">Exibir sinalizadores</span><span class="sxs-lookup"><span data-stu-id="462f4-103">View Flags</span></span>

<span data-ttu-id="462f4-104">Use os sinalizadores de exibição para controlar exibições de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="462f4-104">Use the View Flags to control routing table views.</span></span>



| <span data-ttu-id="462f4-105">Constante</span><span class="sxs-lookup"><span data-stu-id="462f4-105">Constant</span></span>                 | <span data-ttu-id="462f4-106">Valor</span><span class="sxs-lookup"><span data-stu-id="462f4-106">Value</span></span>      | <span data-ttu-id="462f4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="462f4-107">Description</span></span>                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| <span data-ttu-id="462f4-108">\_tamanho máximo de \_ endereço \_ RTM</span><span class="sxs-lookup"><span data-stu-id="462f4-108">RTM\_MAX \_ADDRESS\_SIZE</span></span> | <span data-ttu-id="462f4-109">16</span><span class="sxs-lookup"><span data-stu-id="462f4-109">16</span></span>         | <span data-ttu-id="462f4-110">Tamanho máximo de endereço para uma família de endereços.</span><span class="sxs-lookup"><span data-stu-id="462f4-110">Max address size for an address family.</span></span>                          |
| <span data-ttu-id="462f4-111">\_máximo de \_ exibições de RTM</span><span class="sxs-lookup"><span data-stu-id="462f4-111">RTM\_MAX\_VIEWS</span></span>          | <span data-ttu-id="462f4-112">32</span><span class="sxs-lookup"><span data-stu-id="462f4-112">32</span></span>         | <span data-ttu-id="462f4-113">Número máximo de exibições que podem estar ativas na tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="462f4-113">Maximum number of views that can be active in the routing table.</span></span> |
| <span data-ttu-id="462f4-114">ID de exibição do RTM \_ \_ \_ UCAST</span><span class="sxs-lookup"><span data-stu-id="462f4-114">RTM\_VIEW\_ID\_UCAST</span></span>     | <span data-ttu-id="462f4-115">0</span><span class="sxs-lookup"><span data-stu-id="462f4-115">0</span></span>          | <span data-ttu-id="462f4-116">Especifica uma exibição unicast.</span><span class="sxs-lookup"><span data-stu-id="462f4-116">Specifies a unicast view.</span></span>                                        |
| <span data-ttu-id="462f4-117">ID de exibição do RTM \_ \_ \_ MCast</span><span class="sxs-lookup"><span data-stu-id="462f4-117">RTM\_VIEW\_ID\_MCAST</span></span>     | <span data-ttu-id="462f4-118">1</span><span class="sxs-lookup"><span data-stu-id="462f4-118">1</span></span>          | <span data-ttu-id="462f4-119">Especifica uma exibição de multicast.</span><span class="sxs-lookup"><span data-stu-id="462f4-119">Specifies a multicast view.</span></span>                                      |
| <span data-ttu-id="462f4-120">\_tamanho da \_ máscara de exibição RTM \_</span><span class="sxs-lookup"><span data-stu-id="462f4-120">RTM\_VIEW\_MASK\_SIZE</span></span>    | <span data-ttu-id="462f4-121">0x20</span><span class="sxs-lookup"><span data-stu-id="462f4-121">0x20</span></span>       | <span data-ttu-id="462f4-122">Especifica o número máximo de exibições que podem ser configuradas.</span><span class="sxs-lookup"><span data-stu-id="462f4-122">Specifies the maximum number of views that can be configured.</span></span>    |
| <span data-ttu-id="462f4-123">\_máscara de exibição RTM \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="462f4-123">RTM\_VIEW\_MASK\_NONE</span></span>    | <span data-ttu-id="462f4-124">0x00000000</span><span class="sxs-lookup"><span data-stu-id="462f4-124">0x00000000</span></span> | <span data-ttu-id="462f4-125">Retorna informações independentemente da exibição.</span><span class="sxs-lookup"><span data-stu-id="462f4-125">Returns information regardless of the view.</span></span>                      |
| <span data-ttu-id="462f4-126">\_ \_ qualquer máscara de exibição RTM \_</span><span class="sxs-lookup"><span data-stu-id="462f4-126">RTM\_VIEW\_MASK\_ANY</span></span>     | <span data-ttu-id="462f4-127">0x00000000</span><span class="sxs-lookup"><span data-stu-id="462f4-127">0x00000000</span></span> | <span data-ttu-id="462f4-128">Retorna os destinos de todas as exibições.</span><span class="sxs-lookup"><span data-stu-id="462f4-128">Returns destinations from all views.</span></span> <span data-ttu-id="462f4-129">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="462f4-129">This is the default value.</span></span>  |
| <span data-ttu-id="462f4-130">\_UCAST de \_ máscara de exibição RTM \_</span><span class="sxs-lookup"><span data-stu-id="462f4-130">RTM\_VIEW\_MASK\_UCAST</span></span>   | <span data-ttu-id="462f4-131">0x00000001</span><span class="sxs-lookup"><span data-stu-id="462f4-131">0x00000001</span></span> | <span data-ttu-id="462f4-132">Retorna os destinos da exibição unicast.</span><span class="sxs-lookup"><span data-stu-id="462f4-132">Returns destinations from the unicast view.</span></span>                      |
| <span data-ttu-id="462f4-133">\_mcast de \_ máscara de exibição RTM \_</span><span class="sxs-lookup"><span data-stu-id="462f4-133">RTM\_VIEW\_MASK\_MCAST</span></span>   | <span data-ttu-id="462f4-134">0x00000002</span><span class="sxs-lookup"><span data-stu-id="462f4-134">0x00000002</span></span> | <span data-ttu-id="462f4-135">Retorna os destinos da exibição multicast.</span><span class="sxs-lookup"><span data-stu-id="462f4-135">Returns destinations from the multicast view.</span></span>                    |
| <span data-ttu-id="462f4-136">\_ \_ todas as máscaras da exibição RTM \_</span><span class="sxs-lookup"><span data-stu-id="462f4-136">RTM\_VIEW\_MASK\_ALL</span></span>     | <span data-ttu-id="462f4-137">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="462f4-137">0xFFFFFFFF</span></span> | <span data-ttu-id="462f4-138">Retorna informações de todas as exibições.</span><span class="sxs-lookup"><span data-stu-id="462f4-138">Returns information from all views.</span></span>                              |



 

 

 




