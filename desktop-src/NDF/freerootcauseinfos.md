---
title: Função FreeRootCauseInfos (Ndattributils. h)
description: Desaloca a memória alocada internamente a uma matriz de estruturas RootCauseInfo.
ms.assetid: b45fa432-0db4-470b-80ce-ae25c33f88d6
keywords:
- NDF da função FreeRootCauseInfos
topic_type:
- apiref
api_name:
- FreeRootCauseInfos
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97d302a1c58f1a77aafa7611f437f3d445f29f9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644498"
---
# <a name="freerootcauseinfos-function"></a><span data-ttu-id="9cd0b-104">Função FreeRootCauseInfos</span><span class="sxs-lookup"><span data-stu-id="9cd0b-104">FreeRootCauseInfos function</span></span>

<span data-ttu-id="9cd0b-105">A função **FreeRootCauseInfos** Desaloca a memória alocada internamente a uma matriz de estruturas [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) .</span><span class="sxs-lookup"><span data-stu-id="9cd0b-105">The **FreeRootCauseInfos** function deallocates the memory allocated internally to an array of [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) structures.</span></span> <span data-ttu-id="9cd0b-106">Essa função chama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desalocar memória.</span><span class="sxs-lookup"><span data-stu-id="9cd0b-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cd0b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9cd0b-107">Syntax</span></span>


```C++
VOID FreeRootCauseInfos(
  _In_ RootCauseInfo *pInfo,
       ULONG         RootCauseCount,
       BOOL          bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="9cd0b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9cd0b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cd0b-109">*pInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9cd0b-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cd0b-110">Tipo: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _</span><span class="sxs-lookup"><span data-stu-id="9cd0b-110">Type: \**[**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\** _</span></span>

<span data-ttu-id="9cd0b-111">A matriz de estruturas.</span><span class="sxs-lookup"><span data-stu-id="9cd0b-111">The array of structures.</span></span> <span data-ttu-id="9cd0b-112">A memória alocada apontada por essas estruturas será liberada.</span><span class="sxs-lookup"><span data-stu-id="9cd0b-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="9cd0b-113">_RootCauseCount \*</span><span class="sxs-lookup"><span data-stu-id="9cd0b-113">_RootCauseCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="9cd0b-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="9cd0b-114">Type: **ULONG**</span></span>

<span data-ttu-id="9cd0b-115">O número de estruturas na matriz apontada por *pInfo*.</span><span class="sxs-lookup"><span data-stu-id="9cd0b-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="9cd0b-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="9cd0b-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="9cd0b-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="9cd0b-117">Type: **BOOL**</span></span>

<span data-ttu-id="9cd0b-118">True se a matriz de estruturas também deve ser excluída; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="9cd0b-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cd0b-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9cd0b-119">Return value</span></span>

<span data-ttu-id="9cd0b-120">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="9cd0b-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cd0b-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cd0b-121">Requirements</span></span>



| <span data-ttu-id="9cd0b-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cd0b-122">Requirement</span></span> | <span data-ttu-id="9cd0b-123">Valor</span><span class="sxs-lookup"><span data-stu-id="9cd0b-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd0b-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cd0b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9cd0b-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9cd0b-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9cd0b-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9cd0b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9cd0b-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9cd0b-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9cd0b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9cd0b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cd0b-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cd0b-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cd0b-130">Consulte também</span><span class="sxs-lookup"><span data-stu-id="9cd0b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cd0b-131">**RootCauseInfo**</span><span class="sxs-lookup"><span data-stu-id="9cd0b-131">**RootCauseInfo**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> <dt>

[<span data-ttu-id="9cd0b-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="9cd0b-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

