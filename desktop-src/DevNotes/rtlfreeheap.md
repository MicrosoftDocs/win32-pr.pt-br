---
description: Libera um bloco de memória que foi alocado a partir de um heap por RtlAllocateHeap.
ms.assetid: 0A08FB6B-23A3-450B-8745-AEB927CEB7BB
title: Função RtlFreeHeap (Ntifs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlFreeHeap
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: e51994c4bcd941bc96575eb3fdbb45d4111c1aeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500934"
---
# <a name="rtlfreeheap-function"></a><span data-ttu-id="0d897-103">Função RtlFreeHeap</span><span class="sxs-lookup"><span data-stu-id="0d897-103">RtlFreeHeap function</span></span>

<span data-ttu-id="0d897-104">Libera um bloco de memória que foi alocado a partir de um heap por [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span><span class="sxs-lookup"><span data-stu-id="0d897-104">Frees a memory block that was allocated from a heap by [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d897-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d897-105">Syntax</span></span>


```C++
BOOLEAN RtlFreeHeap(
  _In_     PVOID HeapHandle,
  _In_opt_ ULONG Flags,
  _In_     PVOID HeapBase
);
```



## <a name="parameters"></a><span data-ttu-id="0d897-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d897-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d897-107">*HeapHandle* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d897-107">*HeapHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d897-108">Um identificador para o heap cujo bloco de memória deve ser liberado.</span><span class="sxs-lookup"><span data-stu-id="0d897-108">A handle for the heap whose memory block is to be freed.</span></span> <span data-ttu-id="0d897-109">Esse parâmetro é um identificador retornado por [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span><span class="sxs-lookup"><span data-stu-id="0d897-109">This parameter is a handle returned by [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span></span>

</dd> <dt>

<span data-ttu-id="0d897-110">*Sinalizadores* \[ de em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="0d897-110">*Flags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0d897-111">Um conjunto de sinalizadores que controla aspectos de liberação de um bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="0d897-111">A set of flags that controls aspects of freeing a memory block.</span></span> <span data-ttu-id="0d897-112">Especificar o valor a seguir substitui o valor correspondente que foi especificado no parâmetro *flags* quando o heap foi criado por [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span><span class="sxs-lookup"><span data-stu-id="0d897-112">Specifying the following value overrides the corresponding value that was specified in the *Flags* parameter when the heap was created by [**RtlCreateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap).</span></span>



| <span data-ttu-id="0d897-113">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="0d897-113">Flag</span></span>                           | <span data-ttu-id="0d897-114">Significado</span><span class="sxs-lookup"><span data-stu-id="0d897-114">Meaning</span></span>                                                                                   |
|--------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d897-115">HEAP \_ sem \_ serialização</span><span class="sxs-lookup"><span data-stu-id="0d897-115">HEAP\_NO\_SERIALIZE</span></span><br/> | <span data-ttu-id="0d897-116">A exclusão mútua não será usada quando o **RtlFreeHeap** estiver acessando o heap.</span><span class="sxs-lookup"><span data-stu-id="0d897-116">Mutual exclusion will not be used when **RtlFreeHeap** is accessing the heap.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="0d897-117">*HeapBase* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0d897-117">*HeapBase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d897-118">Um ponteiro para o bloco de memória para gratuito.</span><span class="sxs-lookup"><span data-stu-id="0d897-118">A pointer to the memory block to free.</span></span> <span data-ttu-id="0d897-119">Esse ponteiro é retornado por [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span><span class="sxs-lookup"><span data-stu-id="0d897-119">This pointer is returned by [**RtlAllocateHeap**](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d897-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d897-120">Return value</span></span>

<span data-ttu-id="0d897-121">Retorna **true** se o bloco foi liberado com êxito; Caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="0d897-121">Returns **TRUE** if the block was freed successfully; **FALSE** otherwise.</span></span>

> [!Note]  
> <span data-ttu-id="0d897-122">A partir do Windows 8, o valor de retorno é digitado como **lógico**, que tem um tamanho diferente de **booliano**.</span><span class="sxs-lookup"><span data-stu-id="0d897-122">Starting with Windows 8 the return value is typed as **LOGICAL**, which has a different size than **BOOLEAN**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="0d897-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d897-123">Requirements</span></span>



| <span data-ttu-id="0d897-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d897-124">Requirement</span></span> | <span data-ttu-id="0d897-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0d897-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d897-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d897-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0d897-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0d897-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="0d897-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d897-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0d897-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0d897-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="0d897-130">Plataforma de destino</span><span class="sxs-lookup"><span data-stu-id="0d897-130">Target platform</span></span><br/>          | <dl> <span data-ttu-id="0d897-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="0d897-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="0d897-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d897-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d897-133"><dt>Ntifs. h (incluir Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d897-133"><dt>Ntifs.h (include Ntifs.h)</dt></span></span> </dl>                                    |
| <span data-ttu-id="0d897-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d897-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="0d897-135"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d897-135"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0d897-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0d897-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d897-137"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d897-137"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="0d897-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d897-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d897-139">**RtlAllocateHeap**</span><span class="sxs-lookup"><span data-stu-id="0d897-139">**RtlAllocateHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlallocateheap)
</dt> <dt>

[<span data-ttu-id="0d897-140">**RtlCreateHeap**</span><span class="sxs-lookup"><span data-stu-id="0d897-140">**RtlCreateHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtlcreateheap)
</dt> <dt>

[<span data-ttu-id="0d897-141">**RtlDestroyHeap**</span><span class="sxs-lookup"><span data-stu-id="0d897-141">**RtlDestroyHeap**</span></span>](/windows-hardware/drivers/ddi/ntifs/nf-ntifs-rtldestroyheap)
</dt> </dl>

 

 
