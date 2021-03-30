---
description: A função GetCCInstPtr retorna o ponteiro para os dados da instância adicionados ao contexto de captura.
ms.assetid: 6fb103d3-583b-4460-8b9a-ff921751b0eb
title: Função GetCCInstPtr (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2f078e91829b5324218b901e41e000d37b4cd6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646797"
---
# <a name="getccinstptr-function"></a><span data-ttu-id="42d16-103">Função GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="42d16-103">GetCCInstPtr function</span></span>

<span data-ttu-id="42d16-104">A função **GetCCInstPtr** retorna o ponteiro para os dados da instância adicionados ao contexto de captura.</span><span class="sxs-lookup"><span data-stu-id="42d16-104">The **GetCCInstPtr** function returns the pointer to the instance data added to the capture context.</span></span>

## <a name="syntax"></a><span data-ttu-id="42d16-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42d16-105">Syntax</span></span>


```C++
LPVOID WINAPI GetCCInstPtr(void);
```



## <a name="parameters"></a><span data-ttu-id="42d16-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42d16-106">Parameters</span></span>

<span data-ttu-id="42d16-107">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="42d16-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="42d16-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="42d16-108">Return value</span></span>

<span data-ttu-id="42d16-109">Se a função for bem-sucedida, o valor de retorno será um ponteiro para os dados da instância de uma captura específica.</span><span class="sxs-lookup"><span data-stu-id="42d16-109">If the function is successful, the return value is a pointer to the instance data of a specific capture.</span></span>

<span data-ttu-id="42d16-110">Se a função não for bem-sucedida, o valor de retorno será **nulo**.</span><span class="sxs-lookup"><span data-stu-id="42d16-110">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d16-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42d16-111">Requirements</span></span>



| <span data-ttu-id="42d16-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="42d16-112">Requirement</span></span> | <span data-ttu-id="42d16-113">Valor</span><span class="sxs-lookup"><span data-stu-id="42d16-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="42d16-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42d16-114">Minimum supported client</span></span><br/> | <span data-ttu-id="42d16-115">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="42d16-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="42d16-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="42d16-116">Minimum supported server</span></span><br/> | <span data-ttu-id="42d16-117">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="42d16-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="42d16-118">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="42d16-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="42d16-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="42d16-119"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="42d16-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42d16-120">Library</span></span><br/>                  | <dl> <span data-ttu-id="42d16-121"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42d16-121"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="42d16-122">DLL</span><span class="sxs-lookup"><span data-stu-id="42d16-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42d16-123"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42d16-123"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42d16-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="42d16-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d16-125">SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="42d16-125">SetCCInstPtr</span></span>](setccinstptr.md)
</dt> <dt>

[<span data-ttu-id="42d16-126">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="42d16-126">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="42d16-127">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="42d16-127">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="42d16-128">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="42d16-128">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="42d16-129">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="42d16-129">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




