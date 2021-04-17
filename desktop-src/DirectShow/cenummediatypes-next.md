---
description: 'O método Next recupera um número especificado de tipos de mídia. Esse método implementa o método IEnumMediaTypes:: Next.'
ms.assetid: d59dea48-e36c-4ee6-9935-5a47e8a12a9e
title: Método CEnumMediaTypes. Next (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5eaa75a52f88539438cec58f024919577518e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751246"
---
# <a name="cenummediatypesnext-method"></a><span data-ttu-id="c0fa5-104">Método CEnumMediaTypes. Next</span><span class="sxs-lookup"><span data-stu-id="c0fa5-104">CEnumMediaTypes.Next method</span></span>

<span data-ttu-id="c0fa5-105">O `Next` método recupera um número especificado de tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="c0fa5-105">The `Next` method retrieves a specified number of media types.</span></span> <span data-ttu-id="c0fa5-106">Esse método implementa o método [**IEnumMediaTypes:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) .</span><span class="sxs-lookup"><span data-stu-id="c0fa5-106">This method implements the [**IEnumMediaTypes::Next**](/windows/desktop/api/Strmif/nf-strmif-ienummediatypes-next) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0fa5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0fa5-107">Syntax</span></span>


```C++
HRESULT Next(
   ULONG         cMediaTypes,
   AM_MEDIA_TYPE **ppMediaTypes,
   ULONG         *pcFetched
);
```



## <a name="parameters"></a><span data-ttu-id="c0fa5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0fa5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0fa5-109">*cMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="c0fa5-109">*cMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="c0fa5-110">Número de tipos de mídia a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="c0fa5-110">Number of media types to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="c0fa5-111">*ppMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="c0fa5-111">*ppMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="c0fa5-112">Matriz de ponteiros para as estruturas de [**\_ \_ tipo de mídia**](/windows/win32/api/strmif/ns-strmif-am_media_type) , de tamanho *cPins*.</span><span class="sxs-lookup"><span data-stu-id="c0fa5-112">Array of pointers to [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structures, of size *cPins*.</span></span>

</dd> <dt>

<span data-ttu-id="c0fa5-113">*pcFetched*</span><span class="sxs-lookup"><span data-stu-id="c0fa5-113">*pcFetched*</span></span> 
</dt> <dd>

<span data-ttu-id="c0fa5-114">Ponteiro para uma variável que recebe o número de tipos de mídia que o método retornou.</span><span class="sxs-lookup"><span data-stu-id="c0fa5-114">Pointer to a variable that receives the number of media types the method returned.</span></span> <span data-ttu-id="c0fa5-115">Pode ser **NULL** se *cMediaTypes* for 1.</span><span class="sxs-lookup"><span data-stu-id="c0fa5-115">Can be **NULL** if *cMediaTypes* is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0fa5-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0fa5-116">Return value</span></span>

<span data-ttu-id="c0fa5-117">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0fa5-117">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="c0fa5-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c0fa5-118">Return code</span></span>                                                                                                | <span data-ttu-id="c0fa5-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="c0fa5-119">Description</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0fa5-120"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="c0fa5-120"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="c0fa5-121">Não foi possível recuperar quantos tipos de mídia solicitados.</span><span class="sxs-lookup"><span data-stu-id="c0fa5-121">Did not retrieve as many media types as requested.</span></span><br/>                       |
| <dl> <span data-ttu-id="c0fa5-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c0fa5-122"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="c0fa5-123">Êxito.</span><span class="sxs-lookup"><span data-stu-id="c0fa5-123">Success.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="c0fa5-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c0fa5-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="c0fa5-125">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="c0fa5-125">Invalid argument.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="c0fa5-126"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="c0fa5-126"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="c0fa5-127">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="c0fa5-127">**NULL** pointer argument.</span></span><br/>                                               |
| <dl> <span data-ttu-id="c0fa5-128"><dt>**VFW \_ E \_ enum \_ fora \_ de \_ sincronia**</dt></span><span class="sxs-lookup"><span data-stu-id="c0fa5-128"><dt>**VFW\_E\_ENUM\_OUT\_OF\_SYNC**</dt></span></span> </dl> | <span data-ttu-id="c0fa5-129">O estado do PIN foi alterado e agora está inconsistente com o enumerador.</span><span class="sxs-lookup"><span data-stu-id="c0fa5-129">The pin's state has changed and is now inconsistent with the enumerator.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c0fa5-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0fa5-130">Remarks</span></span>

<span data-ttu-id="c0fa5-131">Se o método tiver sucesso, a matriz especificada por *ppMediaTypes* conterá ponteiros para \_ estruturas de tipo de mídia am \_ .</span><span class="sxs-lookup"><span data-stu-id="c0fa5-131">If the method succeeds, the array specified by *ppMediaTypes* contains pointers to AM\_MEDIA\_TYPE structures.</span></span> <span data-ttu-id="c0fa5-132">O número de estruturas é igual a *\* pcFetched*.</span><span class="sxs-lookup"><span data-stu-id="c0fa5-132">The number of structures is equal to *\*pcFetched*.</span></span> <span data-ttu-id="c0fa5-133">Libere cada tipo de mídia chamando a função [**DeleteMediaType**](deletemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="c0fa5-133">Free each media type by calling the [**DeleteMediaType**](deletemediatype.md) function.</span></span>

<span data-ttu-id="c0fa5-134">Esse método chama o método [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) do PIN para recuperar os tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="c0fa5-134">This method calls the pin's [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) method to retrieve the media types.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0fa5-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0fa5-135">Requirements</span></span>



| <span data-ttu-id="c0fa5-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0fa5-136">Requirement</span></span> | <span data-ttu-id="c0fa5-137">Valor</span><span class="sxs-lookup"><span data-stu-id="c0fa5-137">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0fa5-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0fa5-138">Header</span></span><br/>  | <dl> <span data-ttu-id="c0fa5-139"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0fa5-139"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c0fa5-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0fa5-140">Library</span></span><br/> | <dl> <span data-ttu-id="c0fa5-141"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c0fa5-141"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0fa5-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0fa5-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0fa5-143">**Classe CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="c0fa5-143">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




