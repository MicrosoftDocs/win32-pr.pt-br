---
title: Tipos de informações de IPX para blocos de informações do roteador
description: Os tipos de informações a seguir são listados em Ipxrtdef. h. Use esses tipos de informações com as funções de bloco de informações do roteador ao executar o transporte IPX.
ms.assetid: 6cbc8415-f5ba-4f84-a23f-dd4f4a54d118
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab4494da951c04433da2cf9b1da20db7ea5f3119
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007913"
---
# <a name="ipx-information-types-for-router-information-blocks"></a><span data-ttu-id="b1bfc-104">Tipos de informações de IPX para blocos de informações do roteador</span><span class="sxs-lookup"><span data-stu-id="b1bfc-104">IPX Information Types for Router Information Blocks</span></span>

<span data-ttu-id="b1bfc-105">Os tipos de informações a seguir são listados em Ipxrtdef. h.</span><span class="sxs-lookup"><span data-stu-id="b1bfc-105">The following information types are listed in Ipxrtdef.h.</span></span> <span data-ttu-id="b1bfc-106">Use esses tipos de informações com as funções de bloco de informações do roteador ao executar o transporte IPX.</span><span class="sxs-lookup"><span data-stu-id="b1bfc-106">Use these information types with the router information block functions when running the IPX transport.</span></span>



| <span data-ttu-id="b1bfc-107">Tipo de informação</span><span class="sxs-lookup"><span data-stu-id="b1bfc-107">Information type</span></span>                              | <span data-ttu-id="b1bfc-108">Estrutura de informações</span><span class="sxs-lookup"><span data-stu-id="b1bfc-108">Information structure</span></span>                                          |
|-----------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b1bfc-109">\_tipo de \_ informações do adaptador IPX \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-109">IPX\_ADAPTER\_INFO\_TYPE</span></span>                      | <span data-ttu-id="b1bfc-110">\_informações do adaptador IPX \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-110">IPX\_ADAPTER\_INFO</span></span>                                             |
| <span data-ttu-id="b1bfc-111">\_tipo de \_ informação \_ global IPX</span><span class="sxs-lookup"><span data-stu-id="b1bfc-111">IPX\_GLOBAL\_INFO\_TYPE</span></span>                       | <span data-ttu-id="b1bfc-112">\_informações globais de IPX \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-112">IPX\_GLOBAL\_INFO</span></span>                                              |
| <span data-ttu-id="b1bfc-113">\_tipo de \_ informações da interface IPX \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-113">IPX\_INTERFACE\_INFO\_TYPE</span></span>                    | [<span data-ttu-id="b1bfc-114">**IPX \_ se \_ informações**</span><span class="sxs-lookup"><span data-stu-id="b1bfc-114">**IPX\_IF\_INFO**</span></span>](/windows/desktop/api/Ipxrtdef/ns-ipxrtdef-ipx_if_info)                           |
| <span data-ttu-id="b1bfc-115">IPX \_ no \_ filtro de tráfego \_ \_ \_ tipo de informações globais \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-115">IPX\_IN\_TRAFFIC\_FILTER\_GLOBAL\_INFO\_TYPE</span></span>  | <span data-ttu-id="b1bfc-116">\_ \_ informações globais do filtro de tráfego IPX \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-116">IPX\_TRAFFIC\_FILTER\_GLOBAL\_INFO</span></span>                             |
| <span data-ttu-id="b1bfc-117">\_tipo de \_ \_ \_ informação global do filtro de \_ tráfego \_ IPX out</span><span class="sxs-lookup"><span data-stu-id="b1bfc-117">IPX\_OUT\_TRAFFIC\_FILTER\_GLOBAL\_INFO\_TYPE</span></span> | <span data-ttu-id="b1bfc-118">\_ \_ informações globais do filtro de tráfego IPX \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-118">IPX\_TRAFFIC\_FILTER\_GLOBAL\_INFO</span></span>                             |
| <span data-ttu-id="b1bfc-119">IPX \_ no \_ \_ tipo de informação do filtro de tráfego \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-119">IPX\_IN\_TRAFFIC\_FILTER\_INFO\_TYPE</span></span>          | <span data-ttu-id="b1bfc-120">\_informações de \_ filtro de tráfego IPX \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-120">IPX\_TRAFFIC\_FILTER\_INFO</span></span>                                     |
| <span data-ttu-id="b1bfc-121">\_tipo de \_ informação do filtro de tráfego IPX out \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-121">IPX\_OUT\_TRAFFIC\_FILTER\_INFO\_TYPE</span></span>         | <span data-ttu-id="b1bfc-122">\_informações de \_ filtro de tráfego IPX \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-122">IPX\_TRAFFIC\_FILTER\_INFO</span></span>                                     |
| <span data-ttu-id="b1bfc-123">\_tipo de \_ \_ informação de nome NetBIOS estático \_ de IPX \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-123">IPX\_STATIC\_NETBIOS\_NAME\_INFO\_TYPE</span></span>        | <span data-ttu-id="b1bfc-124">\_informações de \_ \_ nome NetBIOS estático de \_ IPX</span><span class="sxs-lookup"><span data-stu-id="b1bfc-124">IPX\_STATIC\_NETBIOS\_NAME\_INFO</span></span>                               |
| <span data-ttu-id="b1bfc-125">\_tipo de \_ informação de rota estática \_ IPX \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-125">IPX\_STATIC\_ROUTE\_INFO\_TYPE</span></span>                | <span data-ttu-id="b1bfc-126">\_informações de \_ rota \_ estática IPX</span><span class="sxs-lookup"><span data-stu-id="b1bfc-126">IPX\_STATIC\_ROUTE\_INFO</span></span>                                       |
| <span data-ttu-id="b1bfc-127">\_tipo de \_ informações do serviço IPX estático \_ \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-127">IPX\_STATIC\_SERVICE\_INFO\_TYPE</span></span>              | <span data-ttu-id="b1bfc-128">[**\_informações de \_ serviço \_ estático IPX**](/previous-versions/windows/desktop/legacy/aa374456(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b1bfc-128">[**IPX\_STATIC\_SERVICE\_INFO**](/previous-versions/windows/desktop/legacy/aa374456(v=vs.85))</span></span> |
| <span data-ttu-id="b1bfc-129">\_tipo de \_ informações da interface IPXWAN \_</span><span class="sxs-lookup"><span data-stu-id="b1bfc-129">IPXWAN\_INTERFACE\_INFO\_TYPE</span></span>                 | [<span data-ttu-id="b1bfc-130">**IPXWAN \_ se houver \_ informações**</span><span class="sxs-lookup"><span data-stu-id="b1bfc-130">**IPXWAN\_IF\_INFO**</span></span>](/windows/desktop/api/Ipxrtdef/ns-ipxrtdef-ipxwan_if_info)                     |



 

 

 