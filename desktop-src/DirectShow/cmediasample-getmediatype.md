---
description: 'O método GetMediaType recupera o tipo de mídia, se o tipo de mídia for diferente do exemplo anterior. Esse método implementa o método IMediaSample:: GetMediaType.'
ms.assetid: a7850381-d448-4bf6-b059-d734fb3e8e22
title: Método CMediaSample. GetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a067494d6236b824ef8fbbcb583ad50503297b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778623"
---
# <a name="cmediasamplegetmediatype-method"></a><span data-ttu-id="11407-104">Método CMediaSample. GetMediaType</span><span class="sxs-lookup"><span data-stu-id="11407-104">CMediaSample.GetMediaType method</span></span>

<span data-ttu-id="11407-105">O `GetMediaType` método recuperará o tipo de mídia se o tipo de mídia for diferente do exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="11407-105">The `GetMediaType` method retrieves the media type, if the media type differs from the previous sample.</span></span> <span data-ttu-id="11407-106">Esse método implementa o método [**IMediaSample:: GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) .</span><span class="sxs-lookup"><span data-stu-id="11407-106">This method implements the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="11407-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11407-107">Syntax</span></span>


```C++
HRESULT GetMediaType(
   AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="11407-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11407-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11407-109">*ppMediaType*</span><span class="sxs-lookup"><span data-stu-id="11407-109">*ppMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="11407-110">Endereço de uma variável que recebe um ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="11407-110">Address of a variable that receives a pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="11407-111">Se o tipo de mídia não tiver sido alterado do exemplo anterior, *\* ppMediaType* será definido como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="11407-111">If the media type has not changed from the previous sample, *\*ppMediaType* is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11407-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11407-112">Return value</span></span>

<span data-ttu-id="11407-113">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="11407-113">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="11407-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="11407-114">Return code</span></span>                                                                                   | <span data-ttu-id="11407-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="11407-115">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="11407-116"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="11407-116"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="11407-117">O tipo de mídia não foi alterado do exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="11407-117">The media type has not changed from the previous sample.</span></span><br/> |
| <dl> <span data-ttu-id="11407-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="11407-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="11407-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="11407-119">Success.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="11407-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="11407-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="11407-121">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="11407-121">Insufficient memory.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="11407-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="11407-122">Remarks</span></span>

<span data-ttu-id="11407-123">Quando terminar o tipo de mídia, libere o bloco de memória chamando a função do utilitário [**DeleteMediaType**](deletemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="11407-123">When you are done with the media type, free the memory block by calling the [**DeleteMediaType**](deletemediatype.md) utility function.</span></span>

<span data-ttu-id="11407-124">A variável de membro [**CMediaSample:: m \_ pMediaType**](cmediasample-m-pmediatype.md) especifica o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="11407-124">The [**CMediaSample::m\_pMediaType**](cmediasample-m-pmediatype.md) member variable specifies the media type.</span></span> <span data-ttu-id="11407-125">A variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) especifica se o tipo de mídia foi alterado.</span><span class="sxs-lookup"><span data-stu-id="11407-125">The [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable specifies whether the media type has changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="11407-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11407-126">Requirements</span></span>



| <span data-ttu-id="11407-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="11407-127">Requirement</span></span> | <span data-ttu-id="11407-128">Valor</span><span class="sxs-lookup"><span data-stu-id="11407-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11407-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11407-129">Header</span></span><br/>  | <dl> <span data-ttu-id="11407-130"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11407-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="11407-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11407-131">Library</span></span><br/> | <dl> <span data-ttu-id="11407-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="11407-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11407-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="11407-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11407-134">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="11407-134">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




