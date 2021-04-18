---
description: O método GetDeliveryBuffer recupera um exemplo de mídia que contém um buffer vazio.
ms.assetid: 5a20c11b-50f8-443e-a4d5-6bcffde741d5
title: Método CBaseOutputPin. GetDeliveryBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.GetDeliveryBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 332fad740c1ea904feee1a437273f21eb4c1def0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756642"
---
# <a name="cbaseoutputpingetdeliverybuffer-method"></a><span data-ttu-id="b5f1c-103">Método CBaseOutputPin. GetDeliveryBuffer</span><span class="sxs-lookup"><span data-stu-id="b5f1c-103">CBaseOutputPin.GetDeliveryBuffer method</span></span>

<span data-ttu-id="b5f1c-104">O `GetDeliveryBuffer` método recupera um exemplo de mídia que contém um buffer vazio.</span><span class="sxs-lookup"><span data-stu-id="b5f1c-104">The `GetDeliveryBuffer` method retrieves a media sample that contains an empty buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5f1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5f1c-105">Syntax</span></span>


```C++
virtual HRESULT GetDeliveryBuffer(
   IMediaSample   **ppSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="b5f1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5f1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5f1c-107">*ppSample*</span><span class="sxs-lookup"><span data-stu-id="b5f1c-107">*ppSample*</span></span> 
</dt> <dd>

<span data-ttu-id="b5f1c-108">Endereço de uma variável que recebe um ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do buffer.</span><span class="sxs-lookup"><span data-stu-id="b5f1c-108">Address of a variable that receives a pointer to the buffer's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b5f1c-109">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="b5f1c-109">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="b5f1c-110">Ponteiro para a hora de início do exemplo, ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5f1c-110">Pointer to the start time of the sample, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5f1c-111">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="b5f1c-111">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="b5f1c-112">Ponteiro para a hora de término da amostra ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="b5f1c-112">Pointer to the ending time of the sample, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="b5f1c-113">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="b5f1c-113">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="b5f1c-114">Combinação de bits bit a bit de sinalizadores com suporte na interface [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .</span><span class="sxs-lookup"><span data-stu-id="b5f1c-114">Bitwise combination of flags supported by the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5f1c-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5f1c-115">Return value</span></span>

<span data-ttu-id="b5f1c-116">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b5f1c-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b5f1c-117">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b5f1c-117">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="b5f1c-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b5f1c-118">Return code</span></span>                                                                                   | <span data-ttu-id="b5f1c-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5f1c-119">Description</span></span>                        |
|-----------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="b5f1c-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1c-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b5f1c-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="b5f1c-121">Success.</span></span><br/>                |
| <dl> <span data-ttu-id="b5f1c-122"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1c-122"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="b5f1c-123">Nenhum alocador disponível.</span><span class="sxs-lookup"><span data-stu-id="b5f1c-123">No allocator available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b5f1c-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5f1c-124">Remarks</span></span>

<span data-ttu-id="b5f1c-125">Esse método chama o método **IMemAllocator:: GetBuffer** no alocador e passa os parâmetros para esse método.</span><span class="sxs-lookup"><span data-stu-id="b5f1c-125">This method calls the **IMemAllocator::GetBuffer** method on the allocator, and passes the parameters to that method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5f1c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5f1c-126">Requirements</span></span>



| <span data-ttu-id="b5f1c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5f1c-127">Requirement</span></span> | <span data-ttu-id="b5f1c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b5f1c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5f1c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5f1c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b5f1c-130"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1c-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b5f1c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5f1c-131">Library</span></span><br/> | <dl> <span data-ttu-id="b5f1c-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b5f1c-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5f1c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5f1c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5f1c-134">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="b5f1c-134">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




