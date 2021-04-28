---
description: 'Método CTransInPlaceInputPin. EnumMediaTypes – o método EnumMediaTypes enumera os tipos de mídia preferenciais do PIN. Esse método implementa o método IPin:: EnumMediaTypes.'
ms.assetid: 0c28b4b0-a45f-400f-a6d7-7668458f9642
title: Método CTransInPlaceInputPin. EnumMediaTypes (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.EnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f9e05d0e9db50cabc700da7b3803c1606efab78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094754"
---
# <a name="ctransinplaceinputpinenummediatypes-method"></a><span data-ttu-id="1e673-104">Método CTransInPlaceInputPin. EnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="1e673-104">CTransInPlaceInputPin.EnumMediaTypes method</span></span>

<span data-ttu-id="1e673-105">O `EnumMediaTypes` método enumera os tipos de mídia preferenciais do PIN.</span><span class="sxs-lookup"><span data-stu-id="1e673-105">The `EnumMediaTypes` method enumerates the pin's preferred media types.</span></span> <span data-ttu-id="1e673-106">Esse método implementa o método [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="1e673-106">This method implements the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e673-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e673-107">Syntax</span></span>


```C++
HRESULT EnumMediaTypes(
   IEnumMediaTypes **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="1e673-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e673-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e673-109">*ppEnum*</span><span class="sxs-lookup"><span data-stu-id="1e673-109">*ppEnum*</span></span> 
</dt> <dd>

<span data-ttu-id="1e673-110">Recebe um ponteiro para a interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="1e673-110">Receives a pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e673-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1e673-111">Return value</span></span>

<span data-ttu-id="1e673-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e673-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1e673-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1e673-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="1e673-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1e673-114">Return code</span></span>                                                                                           | <span data-ttu-id="1e673-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e673-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="1e673-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1e673-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="1e673-117">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="1e673-117">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="1e673-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1e673-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>         | <span data-ttu-id="1e673-119">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="1e673-119">Insufficient memory.</span></span><br/>             |
| <dl> <span data-ttu-id="1e673-120"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="1e673-120"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="1e673-121">Ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="1e673-121">**NULL** pointer.</span></span><br/>                |
| <dl> <span data-ttu-id="1e673-122"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="1e673-122"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="1e673-123">O pino de saída não está conectado.</span><span class="sxs-lookup"><span data-stu-id="1e673-123">The output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1e673-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e673-124">Remarks</span></span>

<span data-ttu-id="1e673-125">Esse método retorna a interface **IEnumMediaTypes** do pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="1e673-125">This method returns the **IEnumMediaTypes** interface from downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e673-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e673-126">Requirements</span></span>



| <span data-ttu-id="1e673-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e673-127">Requirement</span></span> | <span data-ttu-id="1e673-128">Valor</span><span class="sxs-lookup"><span data-stu-id="1e673-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e673-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e673-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1e673-130"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e673-130"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1e673-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e673-131">Library</span></span><br/> | <dl> <span data-ttu-id="1e673-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1e673-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e673-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="1e673-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e673-134">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="1e673-134">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




