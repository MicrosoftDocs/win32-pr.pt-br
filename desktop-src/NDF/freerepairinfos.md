---
title: Função FreeRepairInfos (Ndattributils. h)
description: Desaloca a memória alocada internamente a uma matriz de estruturas RepairInfo.
ms.assetid: c40f9d10-8d9e-4c79-ac0b-fa88608888f1
keywords:
- NDF da função FreeRepairInfos
topic_type:
- apiref
api_name:
- FreeRepairInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63bf6ab2154376302e4c9dd076ccaf83a0c565c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085367"
---
# <a name="freerepairinfos-function"></a><span data-ttu-id="8218d-104">Função FreeRepairInfos</span><span class="sxs-lookup"><span data-stu-id="8218d-104">FreeRepairInfos function</span></span>

<span data-ttu-id="8218d-105">A função **FreeRepairInfos** Desaloca a memória alocada internamente a uma matriz de estruturas [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) .</span><span class="sxs-lookup"><span data-stu-id="8218d-105">The **FreeRepairInfos** function deallocates the memory allocated internally to an array of [**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) structures.</span></span> <span data-ttu-id="8218d-106">Essa função chama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desalocar memória.</span><span class="sxs-lookup"><span data-stu-id="8218d-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="8218d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8218d-107">Syntax</span></span>


```C++
VOID FreeRepairInfos(
  _In_ RepairInfo *pInfo,
       ULONG      RepairCount,
       BOOL       bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="8218d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8218d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8218d-109">*pInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8218d-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8218d-110">Tipo: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="8218d-110">Type: \**[**RepairInfo**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\** _</span></span>

<span data-ttu-id="8218d-111">A matriz de estruturas.</span><span class="sxs-lookup"><span data-stu-id="8218d-111">The array of structures.</span></span> <span data-ttu-id="8218d-112">A memória alocada apontada por essas estruturas será liberada.</span><span class="sxs-lookup"><span data-stu-id="8218d-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="8218d-113">_RepairCount \*</span><span class="sxs-lookup"><span data-stu-id="8218d-113">_RepairCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="8218d-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="8218d-114">Type: **ULONG**</span></span>

<span data-ttu-id="8218d-115">O número de estruturas na matriz apontada por *pInfo*.</span><span class="sxs-lookup"><span data-stu-id="8218d-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="8218d-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="8218d-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="8218d-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="8218d-117">Type: **BOOL**</span></span>

<span data-ttu-id="8218d-118">True se a matriz de estruturas também deve ser excluída; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="8218d-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8218d-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8218d-119">Return value</span></span>

<span data-ttu-id="8218d-120">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8218d-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8218d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8218d-121">Requirements</span></span>



| <span data-ttu-id="8218d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8218d-122">Requirement</span></span> | <span data-ttu-id="8218d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8218d-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8218d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8218d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8218d-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8218d-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8218d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8218d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8218d-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8218d-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8218d-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8218d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8218d-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="8218d-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8218d-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="8218d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8218d-131">**RepairInfo**</span><span class="sxs-lookup"><span data-stu-id="8218d-131">**RepairInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> <dt>

[<span data-ttu-id="8218d-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="8218d-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

