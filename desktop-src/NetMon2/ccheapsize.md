---
description: A função CCHeapSize retorna o tamanho da memória alocada pela função CCHeapAlloc.
ms.assetid: 45d0fd89-bcd1-4298-8cc3-834d86301f93
title: Função CCHeapSize (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapSize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: e184ae196253a66fc68f9066615b39c48f6921e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754624"
---
# <a name="ccheapsize-function"></a><span data-ttu-id="e90d3-103">Função CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="e90d3-103">CCHeapSize function</span></span>

<span data-ttu-id="e90d3-104">A função **CCHeapSize** retorna o tamanho da memória alocada pela função **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="e90d3-104">The **CCHeapSize** function returns the size of the memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e90d3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e90d3-105">Syntax</span></span>


```C++
SIZE_T WINAPI CCHeapSize(
   LPVOID lpMem
);
```



## <a name="parameters"></a><span data-ttu-id="e90d3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e90d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e90d3-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="e90d3-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="e90d3-108">Ponteiro para a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="e90d3-108">Pointer to the allocated memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e90d3-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e90d3-109">Return value</span></span>

<span data-ttu-id="e90d3-110">Se a função for bem-sucedida, o valor de retorno será o tamanho do bloco de memória solicitado medido em bytes.</span><span class="sxs-lookup"><span data-stu-id="e90d3-110">If the function is successful, the return value is the size of the requested memory block   measured in bytes.</span></span>

<span data-ttu-id="e90d3-111">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="e90d3-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e90d3-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e90d3-112">Requirements</span></span>



| <span data-ttu-id="e90d3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e90d3-113">Requirement</span></span> | <span data-ttu-id="e90d3-114">Valor</span><span class="sxs-lookup"><span data-stu-id="e90d3-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e90d3-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e90d3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="e90d3-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e90d3-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e90d3-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e90d3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="e90d3-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e90d3-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e90d3-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e90d3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e90d3-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e90d3-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="e90d3-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e90d3-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="e90d3-122"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e90d3-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="e90d3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e90d3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e90d3-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e90d3-124"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e90d3-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e90d3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e90d3-126">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="e90d3-126">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="e90d3-127">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="e90d3-127">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="e90d3-128">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="e90d3-128">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="e90d3-129">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="e90d3-129">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="e90d3-130">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="e90d3-130">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> </dl>

 

 




