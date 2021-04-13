---
title: Enumeração DODownloadCostPolicy
description: Especifica a ID das opções de políticas de custo associadas à propriedade **DODownloadProperty_CostPolicy** .
keywords:
- Enumeração DODownloadCostPolicy, DODownloadCostPolicy
topic_type:
- apiref
api_name:
- DODownloadCostPolicy
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: c70384f7c7da1633b910db36c42a335d1c463bae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369286"
---
# <a name="dodownloadcostpolicy-enumeration"></a><span data-ttu-id="de501-104">Enumeração DODownloadCostPolicy</span><span class="sxs-lookup"><span data-stu-id="de501-104">DODownloadCostPolicy enumeration</span></span>

<span data-ttu-id="de501-105">A enumeração **DODownloadCostPolicy** especifica a ID das opções de políticas de custo associadas à propriedade **DODownloadProperty_CostPolicy** .</span><span class="sxs-lookup"><span data-stu-id="de501-105">The **DODownloadCostPolicy** enumeration specifies the ID of cost policies options associated with the **DODownloadProperty_CostPolicy** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="de501-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="de501-106">Syntax</span></span>

```cpp
typedef enum _DODownloadCostPolicy
{
  DODownloadCostPolicy_Always = 0,
  DODownloadCostPolicy_Unrestricted,
  DODownloadCostPolicy_Standard,    
  DODownloadCostPolicy_NoRoaming,   
  DODownloadCostPolicy_NoSurcharge, 
  DODownloadCostPolicy_NoCellular
} DODownloadCostPolicy;
```

## <a name="constants"></a><span data-ttu-id="de501-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="de501-107">Constants</span></span>

| <span data-ttu-id="de501-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="de501-108">Requirement</span></span> | <span data-ttu-id="de501-109">Valor</span><span class="sxs-lookup"><span data-stu-id="de501-109">Value</span></span> |
|-|-|
| <span data-ttu-id="de501-110">DODownloadCostPolicy_Always</span><span class="sxs-lookup"><span data-stu-id="de501-110">DODownloadCostPolicy_Always</span></span> | <span data-ttu-id="de501-111">O download é executado independentemente do custo.</span><span class="sxs-lookup"><span data-stu-id="de501-111">Download runs regardless of the cost.</span></span> |
| <span data-ttu-id="de501-112">DODownloadCostPolicy_Unrestricted</span><span class="sxs-lookup"><span data-stu-id="de501-112">DODownloadCostPolicy_Unrestricted</span></span> | <span data-ttu-id="de501-113">O download é executado, a menos que o impõe custos ou limites de tráfego.</span><span class="sxs-lookup"><span data-stu-id="de501-113">Download runs unless imposes costs or traffic limits.</span></span> |
| <span data-ttu-id="de501-114">DODownloadCostPolicy_Standard</span><span class="sxs-lookup"><span data-stu-id="de501-114">DODownloadCostPolicy_Standard</span></span> | <span data-ttu-id="de501-115">O download é executado, a menos que não esteja sujeito a uma sobretaxa ou ao próximo esgotamento.</span><span class="sxs-lookup"><span data-stu-id="de501-115">Download runs unless neither subject to a surcharge nor near exhaustion.</span></span> |
| <span data-ttu-id="de501-116">DODownloadCostPolicy_NoRoaming</span><span class="sxs-lookup"><span data-stu-id="de501-116">DODownloadCostPolicy_NoRoaming</span></span> | <span data-ttu-id="de501-117">O download é executado, a menos que a conectividade esteja sujeita a sobretaxas de roaming.</span><span class="sxs-lookup"><span data-stu-id="de501-117">Download runs unless that connectivity is subject to roaming surcharges.</span></span> |
| <span data-ttu-id="de501-118">DODownloadCostPolicy_NoSurcharge</span><span class="sxs-lookup"><span data-stu-id="de501-118">DODownloadCostPolicy_NoSurcharge</span></span> | <span data-ttu-id="de501-119">O download é executado, a menos que sujeito a uma sobretaxa.</span><span class="sxs-lookup"><span data-stu-id="de501-119">Download runs unless subject to a surcharge.</span></span> |
| <span data-ttu-id="de501-120">DODownloadCostPolicy_NoCellular</span><span class="sxs-lookup"><span data-stu-id="de501-120">DODownloadCostPolicy_NoCellular</span></span> | <span data-ttu-id="de501-121">O download é executado, a menos que a rede esteja em celular.</span><span class="sxs-lookup"><span data-stu-id="de501-121">Download runs unless network is on cellular.</span></span> |

## <a name="requirements"></a><span data-ttu-id="de501-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de501-122">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="de501-123">**Cliente mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="de501-123">**Minimum supported client**</span></span> | <span data-ttu-id="de501-124">Somente aplicativos do Windows 10, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="de501-124">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="de501-125">**Servidor mínimo com suporte**</span><span class="sxs-lookup"><span data-stu-id="de501-125">**Minimum supported server**</span></span> | <span data-ttu-id="de501-126">Somente aplicativos do Windows Server, versão 1809 \[ Win32\]</span><span class="sxs-lookup"><span data-stu-id="de501-126">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="de501-127">**Cabeçalho**</span><span class="sxs-lookup"><span data-stu-id="de501-127">**Header**</span></span> | <span data-ttu-id="de501-128">DeliveryOptimizationDownloadTypes. h</span><span class="sxs-lookup"><span data-stu-id="de501-128">DeliveryOptimizationDownloadTypes.h</span></span> |
