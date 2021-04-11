---
title: Função FreeHelperAttributes (Ndattributils. h)
description: Desaloca a memória alocada internamente a uma matriz de \_ estruturas de atributo auxiliar.
ms.assetid: d973bdb9-c1d1-4cea-bcc6-98671349413f
keywords:
- NDF da função FreeHelperAttributes
topic_type:
- apiref
api_name:
- FreeHelperAttributes
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400addd7d32914cb4e849e4e0bfae76ccc3ddf22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454903"
---
# <a name="freehelperattributes-function"></a><span data-ttu-id="e2466-104">Função FreeHelperAttributes</span><span class="sxs-lookup"><span data-stu-id="e2466-104">FreeHelperAttributes function</span></span>

<span data-ttu-id="e2466-105">A função **FreeHelperAttributes** Desaloca a memória alocada internamente a uma matriz de estruturas de [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) .</span><span class="sxs-lookup"><span data-stu-id="e2466-105">The **FreeHelperAttributes** function deallocates the memory allocated internally to an array of [**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute) structures.</span></span> <span data-ttu-id="e2466-106">Essa função chama [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para desalocar memória.</span><span class="sxs-lookup"><span data-stu-id="e2466-106">This function calls [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to deallocate memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2466-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2466-107">Syntax</span></span>


```C++
VOID FreeHelperAttributes(
  _In_ HELPER_ATTRIBUTE *pInfo,
       ULONG            HelperAttributeCount,
       BOOL             bFreePointer
);
```



## <a name="parameters"></a><span data-ttu-id="e2466-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2466-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2466-109">*pInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e2466-109">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2466-110">Tipo: \**\* [**\_ atributo auxiliar**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)* _</span><span class="sxs-lookup"><span data-stu-id="e2466-110">Type: \**[**HELPER\_ATTRIBUTE**](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)\** _</span></span>

<span data-ttu-id="e2466-111">A matriz de estruturas.</span><span class="sxs-lookup"><span data-stu-id="e2466-111">The array of structures.</span></span> <span data-ttu-id="e2466-112">A memória alocada apontada por essas estruturas será liberada.</span><span class="sxs-lookup"><span data-stu-id="e2466-112">The allocated memory pointed to by these structures will be freed.</span></span>

</dd> <dt>

<span data-ttu-id="e2466-113">_HelperAttributeCount \*</span><span class="sxs-lookup"><span data-stu-id="e2466-113">_HelperAttributeCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="e2466-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="e2466-114">Type: **ULONG**</span></span>

<span data-ttu-id="e2466-115">O número de estruturas na matriz apontada por *pInfo*.</span><span class="sxs-lookup"><span data-stu-id="e2466-115">The number of structures in the array pointed to by *pInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="e2466-116">*bFreePointer*</span><span class="sxs-lookup"><span data-stu-id="e2466-116">*bFreePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="e2466-117">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="e2466-117">Type: **BOOL**</span></span>

<span data-ttu-id="e2466-118">True se a matriz de estruturas também deve ser excluída; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="e2466-118">True if the array of structures should also be deleted; otherwise, false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2466-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2466-119">Return value</span></span>

<span data-ttu-id="e2466-120">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e2466-120">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2466-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2466-121">Requirements</span></span>



| <span data-ttu-id="e2466-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2466-122">Requirement</span></span> | <span data-ttu-id="e2466-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e2466-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2466-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2466-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e2466-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e2466-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="e2466-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2466-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e2466-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e2466-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e2466-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2466-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2466-129"><dt>Ndattributils. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2466-129"><dt>Ndattributils.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2466-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2466-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2466-131">**\_atributo auxiliar**</span><span class="sxs-lookup"><span data-stu-id="e2466-131">**HELPER\_ATTRIBUTE**</span></span>](/windows/win32/api/ndattrib/ns-ndattrib-helper_attribute)
</dt> <dt>

[<span data-ttu-id="e2466-132">**CoTaskMemFree**</span><span class="sxs-lookup"><span data-stu-id="e2466-132">**CoTaskMemFree**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

