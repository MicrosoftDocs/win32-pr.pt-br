---
description: A função SetCCInstPtr captura um ponteiro de instância de contexto.
ms.assetid: 31924608-4aa1-4801-a5de-d8de054e12d9
title: Função SetCCInstPtr (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetCCInstPtr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 323e6334c90358dd8725f3f9092142275cfe491a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501889"
---
# <a name="setccinstptr-function"></a><span data-ttu-id="d1178-103">Função SetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="d1178-103">SetCCInstPtr function</span></span>

<span data-ttu-id="d1178-104">A função **SetCCInstPtr** captura um ponteiro de instância de contexto.</span><span class="sxs-lookup"><span data-stu-id="d1178-104">The **SetCCInstPtr** function captures a context instance pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1178-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1178-105">Syntax</span></span>


```C++
VOID WINAPI SetCCInstPtr(
   LPVOID lpCurCaptureInst
);
```



## <a name="parameters"></a><span data-ttu-id="d1178-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d1178-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1178-107">*lpCurCaptureInst*</span><span class="sxs-lookup"><span data-stu-id="d1178-107">*lpCurCaptureInst*</span></span> 
</dt> <dd>

<span data-ttu-id="d1178-108">Ponteiro para os dados da instância adicionados à captura.</span><span class="sxs-lookup"><span data-stu-id="d1178-108">Pointer to the instance data added to the capture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1178-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d1178-109">Return value</span></span>

<span data-ttu-id="d1178-110">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d1178-110">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1178-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d1178-111">Remarks</span></span>

<span data-ttu-id="d1178-112">Use essa função para armazenar um ponteiro para um bloco que foi alocado com a função **CCHeapAlloc** .</span><span class="sxs-lookup"><span data-stu-id="d1178-112">Use this function to store a pointer to a block that was allocated with the **CCHeapAlloc** function.</span></span> <span data-ttu-id="d1178-113">Cada analisador pode definir uma única instância de dados em uma captura.</span><span class="sxs-lookup"><span data-stu-id="d1178-113">Each parser can set a single instance of data on a capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1178-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1178-114">Requirements</span></span>



| <span data-ttu-id="d1178-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1178-115">Requirement</span></span> | <span data-ttu-id="d1178-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d1178-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d1178-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1178-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d1178-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d1178-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d1178-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1178-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d1178-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d1178-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d1178-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d1178-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1178-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1178-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d1178-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1178-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d1178-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d1178-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d1178-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d1178-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1178-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1178-126"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1178-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1178-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1178-128">GetCCInstPtr</span><span class="sxs-lookup"><span data-stu-id="d1178-128">GetCCInstPtr</span></span>](getccinstptr.md)
</dt> <dt>

[<span data-ttu-id="d1178-129">CCHeapAlloc</span><span class="sxs-lookup"><span data-stu-id="d1178-129">CCHeapAlloc</span></span>](ccheapalloc.md)
</dt> <dt>

[<span data-ttu-id="d1178-130">CCHeapFree</span><span class="sxs-lookup"><span data-stu-id="d1178-130">CCHeapFree</span></span>](ccheapfree.md)
</dt> <dt>

[<span data-ttu-id="d1178-131">CCHeapReAlloc</span><span class="sxs-lookup"><span data-stu-id="d1178-131">CCHeapReAlloc</span></span>](ccheaprealloc.md)
</dt> <dt>

[<span data-ttu-id="d1178-132">CCHeapSize</span><span class="sxs-lookup"><span data-stu-id="d1178-132">CCHeapSize</span></span>](ccheapsize.md)
</dt> </dl>

 

 




