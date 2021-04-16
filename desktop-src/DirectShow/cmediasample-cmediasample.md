---
description: Método de construtor.
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
ms.openlocfilehash: e4513af3b01d39f311fd1b8ecc1cea8f086d89c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775635"
---
# <a name="cmediasamplecmediasample-constructor"></a><span data-ttu-id="89b25-103">Construtor CMediaSample. CMediaSample</span><span class="sxs-lookup"><span data-stu-id="89b25-103">CMediaSample.CMediaSample constructor</span></span>

<span data-ttu-id="89b25-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="89b25-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="89b25-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="89b25-105">Syntax</span></span>


```C++
CMediaSample(
   TCHAR          *pName,
   CBaseAllocator *pAllocator,
   HRESULT        *phr,
   LPBYTE         pBuffer = NULL,
   LONG           length = 0
);
```



## <a name="parameters"></a><span data-ttu-id="89b25-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="89b25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89b25-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="89b25-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="89b25-108">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="89b25-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="89b25-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="89b25-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="89b25-110">Ponteiro para o objeto [**CBaseAllocator**](cbaseallocator.md) que criou este exemplo.</span><span class="sxs-lookup"><span data-stu-id="89b25-110">Pointer to the [**CBaseAllocator**](cbaseallocator.md) object that created this sample.</span></span>

</dd> <dt>

<span data-ttu-id="89b25-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="89b25-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="89b25-112">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="89b25-112">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="89b25-113">*pBuffer*</span><span class="sxs-lookup"><span data-stu-id="89b25-113">*pBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="89b25-114">Ponteiro para um buffer de memória alocado pelo chamador, de tamanho *.*</span><span class="sxs-lookup"><span data-stu-id="89b25-114">Pointer to a memory buffer allocated by the caller, of size *length*.</span></span>

</dd> <dt>

<span data-ttu-id="89b25-115">*length*</span><span class="sxs-lookup"><span data-stu-id="89b25-115">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="89b25-116">Comprimento do buffer de memória.</span><span class="sxs-lookup"><span data-stu-id="89b25-116">Length of the memory buffer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89b25-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="89b25-117">Remarks</span></span>

<span data-ttu-id="89b25-118">A classe base não modifica o valor **HRESULT** passado no parâmetro *PHR* .</span><span class="sxs-lookup"><span data-stu-id="89b25-118">The base class does not modify the **HRESULT** value passed in the *phr* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="89b25-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89b25-119">Requirements</span></span>



| <span data-ttu-id="89b25-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="89b25-120">Requirement</span></span> | <span data-ttu-id="89b25-121">Valor</span><span class="sxs-lookup"><span data-stu-id="89b25-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89b25-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="89b25-122">Header</span></span><br/>  | <dl> <span data-ttu-id="89b25-123"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89b25-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="89b25-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89b25-124">Library</span></span><br/> | <dl> <span data-ttu-id="89b25-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="89b25-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89b25-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="89b25-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b25-127">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="89b25-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




