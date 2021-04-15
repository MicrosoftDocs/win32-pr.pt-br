---
description: Copia o conteúdo de um bloco de memória de origem para um bloco de memória de destino e dá suporte a blocos de memória de origem e destino sobrepostos.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: Função RtlMoveMemory (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlMoveMemory
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 65f8c8490224213e0bef27fab5239a21eca24344
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753889"
---
# <a name="rtlmovememory-function"></a><span data-ttu-id="22cd8-103">Função RtlMoveMemory</span><span class="sxs-lookup"><span data-stu-id="22cd8-103">RtlMoveMemory function</span></span>

<span data-ttu-id="22cd8-104">Copia o conteúdo de um bloco de memória de origem para um bloco de memória de destino e dá suporte a blocos de memória de origem e destino sobrepostos.</span><span class="sxs-lookup"><span data-stu-id="22cd8-104">Copies the contents of a source memory block to a destination memory block, and supports overlapping source and destination memory blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="22cd8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22cd8-105">Syntax</span></span>


```C++
VOID RtlMoveMemory(
  _Out_       VOID UNALIGNED *Destination,
  _In_  const VOID UNALIGNED *Source,
  _In_        SIZE_T         Length
);
```



## <a name="parameters"></a><span data-ttu-id="22cd8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="22cd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22cd8-107">*Destino* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="22cd8-107">*Destination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22cd8-108">Um ponteiro para o bloco de memória de destino para o qual copiar os bytes.</span><span class="sxs-lookup"><span data-stu-id="22cd8-108">A pointer to the destination memory block to copy the bytes to.</span></span>

</dd> <dt>

<span data-ttu-id="22cd8-109">*Origem* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="22cd8-109">*Source* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22cd8-110">Um ponteiro para o bloco de memória de origem para o qual copiar os bytes.</span><span class="sxs-lookup"><span data-stu-id="22cd8-110">A pointer to the source memory block to copy the bytes from.</span></span>

</dd> <dt>

<span data-ttu-id="22cd8-111">*Comprimento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="22cd8-111">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22cd8-112">O número de bytes a serem copiados da origem para o destino.</span><span class="sxs-lookup"><span data-stu-id="22cd8-112">The number of bytes to copy from the source to the destination.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22cd8-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="22cd8-113">Return value</span></span>

<span data-ttu-id="22cd8-114">Nenhum</span><span class="sxs-lookup"><span data-stu-id="22cd8-114">None</span></span>

## <a name="remarks"></a><span data-ttu-id="22cd8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="22cd8-115">Remarks</span></span>

<span data-ttu-id="22cd8-116">O bloco de memória de origem, que é definido pela *origem* e o *comprimento*, pode se sobrepor ao bloco de memória de destino, que é definido pelo *destino* e pelo *comprimento*.</span><span class="sxs-lookup"><span data-stu-id="22cd8-116">The source memory block, which is defined by *Source* and *Length*, can overlap the destination memory block, which is defined by *Destination* and *Length*.</span></span>

<span data-ttu-id="22cd8-117">A rotina [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) é executada mais rápido que **RtlMoveMemory**, mas o **RtlCopyMemory** requer que os blocos de memória de origem e destino não se sobreponham.</span><span class="sxs-lookup"><span data-stu-id="22cd8-117">The [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) routine runs faster than **RtlMoveMemory**, but **RtlCopyMemory** requires that the source and destination memory blocks do not overlap.</span></span>

<span data-ttu-id="22cd8-118">Os chamadores de **RtlMoveMemory** podem ser executados em qualquer IRQL se os blocos de memória de origem e destino estiverem em memória de sistema não paginável.</span><span class="sxs-lookup"><span data-stu-id="22cd8-118">Callers of **RtlMoveMemory** can be running at any IRQL if the source and destination memory blocks are in nonpaged system memory.</span></span> <span data-ttu-id="22cd8-119">Caso contrário, o chamador deve estar em execução em IRQL <= nível da APC \_ .</span><span class="sxs-lookup"><span data-stu-id="22cd8-119">Otherwise, the caller must be running at IRQL <= APC\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="22cd8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22cd8-120">Requirements</span></span>



| <span data-ttu-id="22cd8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="22cd8-121">Requirement</span></span> | <span data-ttu-id="22cd8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="22cd8-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22cd8-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22cd8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="22cd8-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="22cd8-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="22cd8-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22cd8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="22cd8-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="22cd8-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="22cd8-127">Plataforma de destino</span><span class="sxs-lookup"><span data-stu-id="22cd8-127">Target platform</span></span><br/>          | <dl> <span data-ttu-id="22cd8-128"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="22cd8-128"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="22cd8-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="22cd8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="22cd8-130"><dt>WDM. h (incluindo WDM. h, Ntddk. h ou Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22cd8-130"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="22cd8-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22cd8-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="22cd8-132"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22cd8-132"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="22cd8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="22cd8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22cd8-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22cd8-134"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="22cd8-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="22cd8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22cd8-136">**RtlCopyMemory**</span><span class="sxs-lookup"><span data-stu-id="22cd8-136">**RtlCopyMemory**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
