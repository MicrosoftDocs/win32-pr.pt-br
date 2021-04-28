---
description: Construtor de CMediaSample. CMediaSample-método de construtor.
ms.assetid: 3ee67cfd-a968-4b7c-9c7b-1c28ddb9c343
title: Construtor CMediaSample. CMediaSample (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.CMediaSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd2601b9f53e8f79d9231dd34054932bec4e671
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095434"
---
# <a name="cmediasamplecmediasample-constructor"></a><span data-ttu-id="143f4-103">Construtor CMediaSample. CMediaSample</span><span class="sxs-lookup"><span data-stu-id="143f4-103">CMediaSample.CMediaSample constructor</span></span>

<span data-ttu-id="143f4-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="143f4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="143f4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="143f4-105">Syntax</span></span>


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a><span data-ttu-id="143f4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="143f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="143f4-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="143f4-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="143f4-108">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="143f4-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="143f4-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="143f4-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="143f4-110">Ponteiro para o objeto [**CBaseAllocator**](cbaseallocator.md) que criou este exemplo.</span><span class="sxs-lookup"><span data-stu-id="143f4-110">Pointer to the [**CBaseAllocator**](cbaseallocator.md) object that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="143f4-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="143f4-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="143f4-112">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="143f4-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="143f4-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="143f4-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="143f4-114">Ponteiro para um buffer de memória alocado pelo chamador, de tamanho *.*</span><span class="sxs-lookup"><span data-stu-id="143f4-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span>

</dd> <dt>

<span data-ttu-id="143f4-115">*length*</span><span class="sxs-lookup"><span data-stu-id="143f4-115">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="143f4-116">Comprimento do buffer de memória.</span><span class="sxs-lookup"><span data-stu-id="143f4-116">Length of the memory buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="143f4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="143f4-117">Remarks</span></span>

<span data-ttu-id="143f4-118">A classe base não modifica o valor **HRESULT** passado no parâmetro *PHR* .</span><span class="sxs-lookup"><span data-stu-id="143f4-118">The base class does not modify the **HRESULT** value passed in the *phr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="143f4-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="143f4-119">Requirements</span></span>



| <span data-ttu-id="143f4-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="143f4-120">Requirement</span></span> | <span data-ttu-id="143f4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="143f4-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="143f4-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="143f4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="143f4-123"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="143f4-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="143f4-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="143f4-124">Library</span></span><br/> | <dl> <span data-ttu-id="143f4-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="143f4-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="143f4-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="143f4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="143f4-127">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="143f4-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




