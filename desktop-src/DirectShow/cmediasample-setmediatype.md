---
description: 'O método SetMediaType define o tipo de mídia para o exemplo. Esse método implementa o método IMediaSample:: SetMediaType.'
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: Método CMediaSample. SetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f46fc4e8c348b1d03d19e815f658e0f637b8f880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789970"
---
# <a name="cmediasamplesetmediatype-method"></a><span data-ttu-id="5b4ec-104">Método CMediaSample. SetMediaType</span><span class="sxs-lookup"><span data-stu-id="5b4ec-104">CMediaSample.SetMediaType method</span></span>

<span data-ttu-id="5b4ec-105">O `SetMediaType` método define o tipo de mídia para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="5b4ec-105">The `SetMediaType` method sets the media type for the sample.</span></span> <span data-ttu-id="5b4ec-106">Esse método implementa o método [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) .</span><span class="sxs-lookup"><span data-stu-id="5b4ec-106">This method implements the [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b4ec-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5b4ec-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="5b4ec-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b4ec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b4ec-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="5b4ec-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="5b4ec-110">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="5b4ec-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b4ec-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5b4ec-111">Return value</span></span>

<span data-ttu-id="5b4ec-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5b4ec-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="5b4ec-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5b4ec-113">Return code</span></span>                                                                                   | <span data-ttu-id="5b4ec-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b4ec-114">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="5b4ec-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5b4ec-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="5b4ec-116">Êxito</span><span class="sxs-lookup"><span data-stu-id="5b4ec-116">Success</span></span><br/>             |
| <dl> <span data-ttu-id="5b4ec-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5b4ec-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="5b4ec-118">Memória insuficiente</span><span class="sxs-lookup"><span data-stu-id="5b4ec-118">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5b4ec-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b4ec-119">Remarks</span></span>

<span data-ttu-id="5b4ec-120">Esse método define a variável de membro [**CMediaSample:: m \_ pMediaType**](cmediasample-m-pmediatype.md) , que especifica o tipo de mídia e a variável de membro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica se o tipo de mídia foi alterado.</span><span class="sxs-lookup"><span data-stu-id="5b4ec-120">This method sets the [**CMediaSample::m\_pMediaType**](cmediasample-m-pmediatype.md) member variable, which specifies the media type, and the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies whether the media type has changed.</span></span>

<span data-ttu-id="5b4ec-121">Esse método faz uma cópia da estrutura do \_ tipo de mídia am \_ .</span><span class="sxs-lookup"><span data-stu-id="5b4ec-121">This method makes a copy of the AM\_MEDIA\_TYPE structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b4ec-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b4ec-122">Requirements</span></span>



| <span data-ttu-id="5b4ec-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b4ec-123">Requirement</span></span> | <span data-ttu-id="5b4ec-124">Valor</span><span class="sxs-lookup"><span data-stu-id="5b4ec-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b4ec-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b4ec-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5b4ec-126"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5b4ec-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5b4ec-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b4ec-127">Library</span></span><br/> | <dl> <span data-ttu-id="5b4ec-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5b4ec-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b4ec-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b4ec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b4ec-130">**Classe CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="5b4ec-130">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




