---
description: A função CCHeapFree libera a memória alocada pela função CCHeapAlloc.
ms.assetid: 4e1f3332-b0cb-4c21-8c36-59e14c9686cd
title: Função CCHeapFree (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapFree
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e89ca9a7d00559724edc6679a0ed99e4bdf9c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091726"
---
# <a name="ccheapfree-function"></a><span data-ttu-id="b8be4-103">Função CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="b8be4-103">CCHeapFree function</span></span>

<span data-ttu-id="b8be4-104">A função **CCHeapFree** libera a memória alocada pela função **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="b8be4-104">The **CCHeapFree** function releases the memory allocated by the **CCHeapAlloc** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8be4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8be4-105">Syntax</span></span>


```C++
BOOL WINAPI CCHeapFree(
   LPVOID lpMem
);
```



## <a name="parameters"></a><span data-ttu-id="b8be4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8be4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8be4-107">*lpMem*</span><span class="sxs-lookup"><span data-stu-id="b8be4-107">*lpMem*</span></span> 
</dt> <dd>

<span data-ttu-id="b8be4-108">Ponteiro para a memória que esta função libera.</span><span class="sxs-lookup"><span data-stu-id="b8be4-108">Pointer to the memory that this function releases.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8be4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b8be4-109">Return value</span></span>

<span data-ttu-id="b8be4-110">Se a função **CCHeapFree** for bem-sucedida, o valor de retorno será **true**.</span><span class="sxs-lookup"><span data-stu-id="b8be4-110">If the **CCHeapFree** function is successful, the return value is **TRUE**.</span></span>

<span data-ttu-id="b8be4-111">Se a função não for bem-sucedida, o valor de retorno será **false**.</span><span class="sxs-lookup"><span data-stu-id="b8be4-111">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8be4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8be4-112">Requirements</span></span>



| <span data-ttu-id="b8be4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8be4-113">Requirement</span></span> | <span data-ttu-id="b8be4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="b8be4-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b8be4-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8be4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b8be4-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b8be4-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b8be4-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b8be4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b8be4-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b8be4-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b8be4-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b8be4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8be4-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8be4-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b8be4-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8be4-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8be4-122"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8be4-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b8be4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b8be4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8be4-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8be4-124"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8be4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8be4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8be4-126">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="b8be4-126">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="b8be4-127">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="b8be4-127">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="b8be4-128">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="b8be4-128">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="b8be4-129">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="b8be4-129">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="b8be4-130">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="b8be4-130">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




