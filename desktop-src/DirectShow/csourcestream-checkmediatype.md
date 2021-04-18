---
description: 'O método CheckMediaType determina se o PIN aceita um tipo de mídia específico. Esse método implementa o método puramente virtual CBasePin:: CheckMediaType.'
ms.assetid: 3db7c74c-a6aa-4b49-b2a5-9bf8db35fd7e
title: Método CSourceStream. CheckMediaType (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62f8b6c18613f5c187fc637febd08b74260a1e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751681"
---
# <a name="csourcestreamcheckmediatype-method"></a><span data-ttu-id="e709c-104">Método CSourceStream. CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="e709c-104">CSourceStream.CheckMediaType method</span></span>

<span data-ttu-id="e709c-105">O `CheckMediaType` método determina se o PIN aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="e709c-105">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="e709c-106">Esse método implementa o método puramente virtual [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="e709c-106">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e709c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e709c-107">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="e709c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e709c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e709c-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="e709c-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="e709c-110">Ponteiro para um objeto [**CMediaType**](cmediatype.md) que contém o tipo de mídia proposto.</span><span class="sxs-lookup"><span data-stu-id="e709c-110">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e709c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e709c-111">Return value</span></span>

<span data-ttu-id="e709c-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e709c-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e709c-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e709c-113">Return code</span></span>                                                                            | <span data-ttu-id="e709c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e709c-114">Description</span></span>                                          |
|----------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="e709c-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e709c-115"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="e709c-116">Este PIN dá suporte a este tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e709c-116">This pin supports this media type.</span></span><br/>        |
| <dl> <span data-ttu-id="e709c-117"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="e709c-117"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="e709c-118">O PIN não oferece suporte a esse tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e709c-118">The pin does not support this media type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e709c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="e709c-119">Remarks</span></span>

<span data-ttu-id="e709c-120">Por padrão, o PIN dá suporte a um único tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e709c-120">By default, the pin supports a single media type.</span></span> <span data-ttu-id="e709c-121">Esse método recupera o tipo com suporte chamando a versão de parâmetro único do método [**CSourceStream:: GetMediaType**](csourcestream-getmediatype.md) e o compara com o tipo proposto.</span><span class="sxs-lookup"><span data-stu-id="e709c-121">This method retrieves the supported type by calling the single-parameter version of the [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) method, and compares it to the proposed type.</span></span> <span data-ttu-id="e709c-122">Se o PIN der suporte a mais de um tipo de mídia, substitua esse método.</span><span class="sxs-lookup"><span data-stu-id="e709c-122">If your pin supports more than one media type, override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e709c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e709c-123">Requirements</span></span>



| <span data-ttu-id="e709c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e709c-124">Requirement</span></span> | <span data-ttu-id="e709c-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e709c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e709c-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e709c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e709c-127"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e709c-127"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e709c-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e709c-128">Library</span></span><br/> | <dl> <span data-ttu-id="e709c-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e709c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e709c-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e709c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e709c-131">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="e709c-131">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




