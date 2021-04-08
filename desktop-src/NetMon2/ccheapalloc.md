---
description: A função CCHeapAlloc aloca memória em uma base captura por captura.
ms.assetid: 6403c35f-d78f-48dc-90cc-0b76260bbab7
title: Função CCHeapAlloc (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCHeapAlloc
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 14fce9f56103803e575d295799a5c5971ed1c459
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828229"
---
# <a name="ccheapalloc-function"></a><span data-ttu-id="8d7d5-103">Função CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="8d7d5-103">CCHeapAlloc function</span></span>

<span data-ttu-id="8d7d5-104">A função **CCHeapAlloc** aloca memória em uma base captura por captura.</span><span class="sxs-lookup"><span data-stu-id="8d7d5-104">The **CCHeapAlloc** function allocates memory on a capture-by-capture basis.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d7d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8d7d5-105">Syntax</span></span>


```C++
LPVOID WINAPI CCHeapAlloc(
   DWORD dwBytes,
   BOOL  bZeroInit
);
```



## <a name="parameters"></a><span data-ttu-id="8d7d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d7d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d7d5-107">*dwBytes*</span><span class="sxs-lookup"><span data-stu-id="8d7d5-107">*dwBytes*</span></span> 
</dt> <dd>

<span data-ttu-id="8d7d5-108">Comprimento solicitado da memória alocada.</span><span class="sxs-lookup"><span data-stu-id="8d7d5-108">Requested length of memory allocated.</span></span>

</dd> <dt>

<span data-ttu-id="8d7d5-109">*bZeroInit*</span><span class="sxs-lookup"><span data-stu-id="8d7d5-109">*bZeroInit*</span></span> 
</dt> <dd>

<span data-ttu-id="8d7d5-110">Indicador de se a memória alocada foi inicializada.</span><span class="sxs-lookup"><span data-stu-id="8d7d5-110">Indicator of whether allocated memory was initialized.</span></span> <span data-ttu-id="8d7d5-111">Se o valor do parâmetro for **true**, a memória alocada será inicializada para zero.</span><span class="sxs-lookup"><span data-stu-id="8d7d5-111">If the parameter value is **TRUE**, the allocated memory initializes to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d7d5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8d7d5-112">Return value</span></span>

<span data-ttu-id="8d7d5-113">Se a função for bem-sucedida, o valor de retorno será um ponteiro para a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="8d7d5-113">If the function is successful, the return value is a pointer to the allocated memory.</span></span> <span data-ttu-id="8d7d5-114">Quando você terminar de usar a memória alocada, libere a memória chamando a função [**CCHeapFree**](ccheapfree.md) .</span><span class="sxs-lookup"><span data-stu-id="8d7d5-114">When you have finished using the allocated memory, free the memory by calling the [**CCHeapFree**](ccheapfree.md) function.</span></span>

<span data-ttu-id="8d7d5-115">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="8d7d5-115">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d7d5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8d7d5-116">Requirements</span></span>



| <span data-ttu-id="8d7d5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d7d5-117">Requirement</span></span> | <span data-ttu-id="8d7d5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8d7d5-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8d7d5-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d7d5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8d7d5-120">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8d7d5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8d7d5-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8d7d5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8d7d5-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8d7d5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8d7d5-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8d7d5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d7d5-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d7d5-124"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="8d7d5-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8d7d5-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="8d7d5-126"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d7d5-126"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="8d7d5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="8d7d5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d7d5-128"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d7d5-128"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d7d5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d7d5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d7d5-130">**SetCCInstPtr**</span><span class="sxs-lookup"><span data-stu-id="8d7d5-130">**SetCCInstPtr**</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="8d7d5-131">**GetCCInstPtr**</span><span class="sxs-lookup"><span data-stu-id="8d7d5-131">**GetCCInstPtr**</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="8d7d5-132">**CCHeapFree**</span><span class="sxs-lookup"><span data-stu-id="8d7d5-132">**CCHeapFree**</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="8d7d5-133">**CCHeapReAlloc**</span><span class="sxs-lookup"><span data-stu-id="8d7d5-133">**CCHeapReAlloc**</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="8d7d5-134">**CCHeapSize**</span><span class="sxs-lookup"><span data-stu-id="8d7d5-134">**CCHeapSize**</span></span>](ccheapsize.md)
</dt> </dl>

 

 




