---
description: A função CCHeapReAlloc realoca a memória alocada pela função CCHeapAlloc.
ms.assetid: 82365ce2-3980-44ff-be0f-062a65f676fc
title: Função CCHeapReAlloc (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapReAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e1619e2e6e81e8a265600f8437a6633e18065f10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662139"
---
# <a name="ccheaprealloc-function"></a><span data-ttu-id="a21c4-103">Função CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="a21c4-103">CCHeapReAlloc function</span></span>

<span data-ttu-id="a21c4-104">A função **CCHeapReAlloc** realoca a memória alocada pela função **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="a21c4-104">The **CCHeapReAlloc** function reallocates memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="a21c4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a21c4-105">Syntax</span></span>


```C++
LPVOID WINAPI CCHeapReAlloc(
   LPVOID lpMem,
   DWORD  dwBytes,
   BOOL   bZeroInit
);
```



## <a name="parameters"></a><span data-ttu-id="a21c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a21c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a21c4-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="a21c4-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="a21c4-108">Ponteiro para a memória alocada original.</span><span class="sxs-lookup"><span data-stu-id="a21c4-108">Pointer to the original allocated memory.</span></span>

</dd> <dt>

<span data-ttu-id="a21c4-109">*dwBytes*</span><span class="sxs-lookup"><span data-stu-id="a21c4-109">*dwBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="a21c4-110">Tamanho da memória realocada, medida em bytes.</span><span class="sxs-lookup"><span data-stu-id="a21c4-110">Size of the reallocated memory, measured in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a21c4-111">*bZeroInit*</span><span class="sxs-lookup"><span data-stu-id="a21c4-111">*bZeroInit*</span></span> 
</dt> <dd>

<span data-ttu-id="a21c4-112">Indicador de se a memória realocada foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="a21c4-112">Indicator of whether reallocated memory was initialized.</span></span> <span data-ttu-id="a21c4-113">Se o valor do parâmetro for **true**, a memória realocada recentemente será inicializada para zero.</span><span class="sxs-lookup"><span data-stu-id="a21c4-113">If the parameter value is **TRUE**, the newly reallocated memory initializes to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a21c4-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a21c4-114">Return value</span></span>

<span data-ttu-id="a21c4-115">Se a função for bem-sucedida, o valor de retorno será um ponteiro para a memória realocada.</span><span class="sxs-lookup"><span data-stu-id="a21c4-115">If the function is successful, the return value is a pointer to the reallocated memory.</span></span>

<span data-ttu-id="a21c4-116">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a21c4-116">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a21c4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a21c4-117">Requirements</span></span>



| <span data-ttu-id="a21c4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a21c4-118">Requirement</span></span> | <span data-ttu-id="a21c4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a21c4-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a21c4-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a21c4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a21c4-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a21c4-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a21c4-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a21c4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a21c4-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a21c4-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a21c4-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a21c4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a21c4-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a21c4-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a21c4-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a21c4-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a21c4-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a21c4-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a21c4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a21c4-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a21c4-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a21c4-129"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a21c4-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a21c4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a21c4-131">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="a21c4-131">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="a21c4-132">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="a21c4-132">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="a21c4-133">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="a21c4-133">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="a21c4-134">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="a21c4-134">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="a21c4-135">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="a21c4-135">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




