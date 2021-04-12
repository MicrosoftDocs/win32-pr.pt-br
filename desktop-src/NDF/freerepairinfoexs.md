---
title: Função FreeRepairInfoExs (Ndattributils. h)
description: Desaloca a memória alocada internamente a uma matriz de estruturas RepairInfoEx.
ms.assetid: b4e3e758-88cd-4ce2-b1a4-5b47889aae9b
keywords:
- NDF da função FreeRepairInfoExs
topic_type:
- apiref
api_name:
- FreeRepairInfoExs
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 094c745486526caa870a500019de3aa819b6fe5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499424"
---
# <a name="freerepairinfoexs-function"></a><span data-ttu-id="71918-104">Função FreeRepairInfoExs</span><span class="sxs-lookup"><span data-stu-id="71918-104">FreeRepairInfoExs function</span></span>

<span data-ttu-id="71918-105">A função **FreeRepairInfoExs** Desaloca a memória alocada internamente a uma matriz de estruturas [**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) .</span><span class="sxs-lookup"><span data-stu-id="71918-105">The **FreeRepairInfoExs** function deallocates the memory allocated internally to an array of [**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) structures.</span></span> <span data-ttu-id="71918-106">Essa função chama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desalocar memória.</span><span class="sxs-lookup"><span data-stu-id="71918-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="71918-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71918-107">Syntax</span></span>


```C++
VOID FreeRepairInfoExs(
  _In_ RepairInfoEx *pInfo,
       ULONG        RepairCount,
       BOOL         bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="71918-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71918-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71918-109">*pInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71918-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71918-110">Tipo: \**[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex) \** _</span><span class="sxs-lookup"><span data-stu-id="71918-110">Type: \**[**RepairInfoEx**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)\** _</span></span>

<span data-ttu-id="71918-111">A matriz de estruturas.</span><span class="sxs-lookup"><span data-stu-id="71918-111">The array of structures.</span></span> <span data-ttu-id="71918-112">A memória alocada apontada por essas estruturas será liberada.</span><span class="sxs-lookup"><span data-stu-id="71918-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="71918-113">_RepairCount \*</span><span class="sxs-lookup"><span data-stu-id="71918-113">_RepairCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="71918-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="71918-114">Type: **ULONG**</span></span>

<span data-ttu-id="71918-115">O número de estruturas na matriz apontada por *pInfo*.</span><span class="sxs-lookup"><span data-stu-id="71918-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="71918-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="71918-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="71918-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="71918-117">Type: **BOOL**</span></span>

<span data-ttu-id="71918-118">True se a matriz de estruturas também deve ser excluída; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="71918-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71918-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71918-119">Return value</span></span>

<span data-ttu-id="71918-120">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="71918-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="71918-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71918-121">Requirements</span></span>



| <span data-ttu-id="71918-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="71918-122">Requirement</span></span> | <span data-ttu-id="71918-123">Valor</span><span class="sxs-lookup"><span data-stu-id="71918-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="71918-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71918-124">Minimum supported client</span></span><br/> | <span data-ttu-id="71918-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="71918-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="71918-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71918-126">Minimum supported server</span></span><br/> | <span data-ttu-id="71918-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="71918-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="71918-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71918-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="71918-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="71918-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71918-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="71918-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71918-131">**RepairInfoEx**</span><span class="sxs-lookup"><span data-stu-id="71918-131">**RepairInfoEx**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-repairinfoex)
</dt> <dt>

[<span data-ttu-id="71918-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="71918-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

