---
title: Identificadores de peso de filtro (Fwpmu. h)
description: Filtre os identificadores de peso usados pelo BFE (mecanismo de filtragem base) para computar os pesos de filtro gerados automaticamente.
ms.assetid: 73d2e9e0-0d3a-474e-b660-f91675f9000e
topic_type:
- apiref
api_name:
- FWPM_AUTO_WEIGHT_BITS
- FWPM_AUTO_WEIGHT_MAX
- FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS
- FWPM_WEIGHT_RANGE_IPSEC
- FWPM_WEIGHT_RANGE_MAX
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e8ea740c5087151418d50187ee3dc1097baad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761739"
---
# <a name="filter-weight-identifiers"></a><span data-ttu-id="6d61d-103">Identificadores de peso de filtro</span><span class="sxs-lookup"><span data-stu-id="6d61d-103">Filter Weight Identifiers</span></span>

<span data-ttu-id="6d61d-104">Os identificadores de peso de filtro usados pelo BFE (mecanismo de filtragem base) para computar os pesos de filtro gerados automaticamente são listados abaixo.</span><span class="sxs-lookup"><span data-stu-id="6d61d-104">The filter weight identifiers used by the Base Filtering Engine (BFE) to compute auto-generated filter weights are listed below.</span></span>

<span data-ttu-id="6d61d-105">Consulte [atribuição de peso de filtro](filter-weight-assignment.md) para obter mais informações sobre a geração de peso de filtro.</span><span class="sxs-lookup"><span data-stu-id="6d61d-105">See [Filter Weight Assignment](filter-weight-assignment.md) for more information on filter weight generation.</span></span>

<dl> <dt>

<span data-ttu-id="6d61d-106"><span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**\_bits de \_ peso \_ automático FWPM**</span><span class="sxs-lookup"><span data-stu-id="6d61d-106"><span id="FWPM_AUTO_WEIGHT_BITS"></span><span id="fwpm_auto_weight_bits"></span>**FWPM\_AUTO\_WEIGHT\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d61d-107">(60)</span><span class="sxs-lookup"><span data-stu-id="6d61d-107">(60)</span></span>
</dt> <dt>



<span data-ttu-id="6d61d-108">Número de bits usados para pesos de filtro gerados automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6d61d-108">Number of bits used for auto-generated filter weights.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d61d-109"><span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**\_ \_ peso \_ máximo de FWPM**</span><span class="sxs-lookup"><span data-stu-id="6d61d-109"><span id="FWPM_AUTO_WEIGHT_MAX"></span><span id="fwpm_auto_weight_max"></span>**FWPM\_AUTO\_WEIGHT\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d61d-110">(**MAXUINT64** >> 4)</span><span class="sxs-lookup"><span data-stu-id="6d61d-110">(**MAXUINT64** >> 4)</span></span>
</dt> <dt>



<span data-ttu-id="6d61d-111">Peso máximo de filtro gerado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6d61d-111">Maximum auto-generated filter weight.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d61d-112"><span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**\_ \_ isenções Ike de intervalo de peso FWPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6d61d-112"><span id="FWPM_WEIGHT_RANGE_IKE_EXEMPTIONS"></span><span id="fwpm_weight_range_ike_exemptions"></span>**FWPM\_WEIGHT\_RANGE\_IKE\_EXEMPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d61d-113">(0xC)</span><span class="sxs-lookup"><span data-stu-id="6d61d-113">(0xC)</span></span>
</dt> <dt>



<span data-ttu-id="6d61d-114">O BFE atribui um peso com esse valor de intervalo aos filtros IKE e AuthIP.</span><span class="sxs-lookup"><span data-stu-id="6d61d-114">BFE assigns a weight with this range value to IKE and AuthIP filters.</span></span>

<span data-ttu-id="6d61d-115">Consulte [isenções de Ike/AuthIP](ike-exemptions.md) para obter mais informações sobre filtros Ike/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="6d61d-115">See [IKE/AuthIP Exemptions](ike-exemptions.md) for more information on IKE/AuthIP filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d61d-116"><span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**\_IPSec de \_ intervalo de peso FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="6d61d-116"><span id="FWPM_WEIGHT_RANGE_IPSEC"></span><span id="fwpm_weight_range_ipsec"></span>**FWPM\_WEIGHT\_RANGE\_IPSEC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d61d-117">(0x0)</span><span class="sxs-lookup"><span data-stu-id="6d61d-117">(0x0)</span></span>
</dt> <dt>



<span data-ttu-id="6d61d-118">O BFE atribui um peso com esse valor de intervalo aos filtros de política IPsec.</span><span class="sxs-lookup"><span data-stu-id="6d61d-118">BFE assigns a weight with this range value to IPsec policy filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d61d-119"><span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**\_intervalo de peso FWPM \_ \_ máximo**</span><span class="sxs-lookup"><span data-stu-id="6d61d-119"><span id="FWPM_WEIGHT_RANGE_MAX"></span><span id="fwpm_weight_range_max"></span>**FWPM\_WEIGHT\_RANGE\_MAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d61d-120">(**MAXUINT64** >> 60)</span><span class="sxs-lookup"><span data-stu-id="6d61d-120">(**MAXUINT64** >> 60)</span></span>
</dt> <dt>



<span data-ttu-id="6d61d-121">Valor de intervalo de peso de filtro máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="6d61d-121">Maximum allowed filter weight range value.</span></span>


</dt> </dl> </dd> </dl>

> [!Note]  
> <span data-ttu-id="6d61d-122">**MAXUINT64** representa o maior valor possível de **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="6d61d-122">**MAXUINT64** represents the largest possible value of **UINT64**.</span></span> <span data-ttu-id="6d61d-123">O valor dessa constante é 0xFFFFFFFFFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="6d61d-123">The value of this constant is 0xFFFFFFFFFFFFFFFF.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6d61d-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d61d-124">Requirements</span></span>



| <span data-ttu-id="6d61d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d61d-125">Requirement</span></span> | <span data-ttu-id="6d61d-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6d61d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d61d-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d61d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6d61d-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6d61d-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6d61d-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d61d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6d61d-130">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6d61d-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6d61d-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d61d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d61d-132"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d61d-132"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





