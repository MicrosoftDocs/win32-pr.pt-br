---
description: 'O método ConnectionMediaType recupera o tipo de mídia para a conexão do PIN atual, se houver. Esse método implementa o método IPin:: ConnectionMediaType.'
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: Método CBasePin. ConnectionMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectionMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62bd211b6c93e44c571d822ccc86104a5a6fdcab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771865"
---
# <a name="cbasepinconnectionmediatype-method"></a><span data-ttu-id="f4705-104">Método CBasePin. ConnectionMediaType</span><span class="sxs-lookup"><span data-stu-id="f4705-104">CBasePin.ConnectionMediaType method</span></span>

<span data-ttu-id="f4705-105">O método **ConnectionMediaType** recupera o tipo de mídia para a conexão do PIN atual, se houver.</span><span class="sxs-lookup"><span data-stu-id="f4705-105">The **ConnectionMediaType** method retrieves the media type for the current pin connection, if any.</span></span> <span data-ttu-id="f4705-106">Esse método implementa o método [**IPin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) .</span><span class="sxs-lookup"><span data-stu-id="f4705-106">This method implements the [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4705-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f4705-107">Syntax</span></span>


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="f4705-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4705-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4705-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="f4705-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="f4705-110">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que recebe o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="f4705-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4705-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4705-111">Return value</span></span>

<span data-ttu-id="f4705-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f4705-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f4705-113">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="f4705-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="f4705-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f4705-114">Return code</span></span>                                                                                           | <span data-ttu-id="f4705-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4705-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f4705-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f4705-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="f4705-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="f4705-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="f4705-118"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="f4705-118"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="f4705-119">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="f4705-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="f4705-120"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="f4705-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="f4705-121">O PIN não está conectado.</span><span class="sxs-lookup"><span data-stu-id="f4705-121">Pin is not connected.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="f4705-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4705-122">Remarks</span></span>

<span data-ttu-id="f4705-123">Se o PIN estiver conectado, esse método copiará o tipo de mídia para a estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) especificada por *PGTO*. O chamador deve liberar o bloco de formato do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="f4705-123">If the pin is connected, this method copies the media type into the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure specified by *pmt*. The caller must free the media type's format block.</span></span> <span data-ttu-id="f4705-124">Você pode usar a função [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ou a função auxiliar [**FreeMediaType**](freemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="f4705-124">You can use the [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function, or the [**FreeMediaType**](freemediatype.md) helper function.</span></span>

<span data-ttu-id="f4705-125">Se o PIN não estiver conectado, esse método zerará o bloco de memória especificado por *PGTO* e retornará um código de erro.</span><span class="sxs-lookup"><span data-stu-id="f4705-125">If the pin is not connected, this method zeroes the memory block specified by *pmt* and returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4705-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4705-126">Requirements</span></span>



| <span data-ttu-id="f4705-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4705-127">Requirement</span></span> | <span data-ttu-id="f4705-128">Valor</span><span class="sxs-lookup"><span data-stu-id="f4705-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4705-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4705-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f4705-130"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4705-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f4705-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4705-131">Library</span></span><br/> | <dl> <span data-ttu-id="f4705-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f4705-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4705-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4705-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4705-134">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="f4705-134">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

