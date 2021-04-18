---
description: O método ReconnectPin quebra uma conexão de PIN existente e a reconecta ao mesmo PIN, usando um tipo de mídia especificado.
ms.assetid: 9e2dea49-a2bd-4abd-b896-54b13b2271bb
title: Método CBaseFilter. ReconnectPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.ReconnectPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22507995621d708e40437175d7004d10f68fedb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749038"
---
# <a name="cbasefilterreconnectpin-method"></a><span data-ttu-id="b63d7-103">Método CBaseFilter. ReconnectPin</span><span class="sxs-lookup"><span data-stu-id="b63d7-103">CBaseFilter.ReconnectPin method</span></span>

<span data-ttu-id="b63d7-104">O `ReconnectPin` método quebra uma conexão de PIN existente e a reconecta ao mesmo PIN, usando um tipo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="b63d7-104">The `ReconnectPin` method breaks an existing pin connection and reconnects it to the same pin, using a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b63d7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b63d7-105">Syntax</span></span>


```C++
HRESULT ReconnectPin(
   IPin                *pPin,
   AM_MEDIA_TYPE const *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="b63d7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b63d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b63d7-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="b63d7-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="b63d7-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do PIN.</span><span class="sxs-lookup"><span data-stu-id="b63d7-108">Pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b63d7-109">*PMT*</span><span class="sxs-lookup"><span data-stu-id="b63d7-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="b63d7-110">Ponteiro para uma estrutura de [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica o tipo de mídia ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="b63d7-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b63d7-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b63d7-111">Return value</span></span>

<span data-ttu-id="b63d7-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b63d7-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b63d7-113">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b63d7-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="b63d7-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b63d7-114">Return code</span></span>                                                                                   | <span data-ttu-id="b63d7-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b63d7-115">Description</span></span>                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b63d7-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b63d7-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b63d7-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="b63d7-117">Success.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="b63d7-118"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="b63d7-118"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="b63d7-119">a variável de membro [**\_ pGraph m**](cbasefilter-m-pgraph.md) é **nula**.</span><span class="sxs-lookup"><span data-stu-id="b63d7-119">[**m\_pGraph**](cbasefilter-m-pgraph.md) member variable is **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b63d7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="b63d7-120">Remarks</span></span>

<span data-ttu-id="b63d7-121">Esse método chama o método [**IFilterGraph2:: ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) no Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="b63d7-121">This method calls the [**IFilterGraph2::ReconnectEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-reconnectex) method on the filter graph manager.</span></span> <span data-ttu-id="b63d7-122">Se a interface [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) não estiver disponível, o método chamará [**IFilterGraph:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).</span><span class="sxs-lookup"><span data-stu-id="b63d7-122">If the [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2) interface is not available, the method calls [**IFilterGraph::Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect).</span></span>

## <a name="requirements"></a><span data-ttu-id="b63d7-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b63d7-123">Requirements</span></span>



| <span data-ttu-id="b63d7-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b63d7-124">Requirement</span></span> | <span data-ttu-id="b63d7-125">Valor</span><span class="sxs-lookup"><span data-stu-id="b63d7-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b63d7-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b63d7-126">Header</span></span><br/>  | <dl> <span data-ttu-id="b63d7-127"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b63d7-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b63d7-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b63d7-128">Library</span></span><br/> | <dl> <span data-ttu-id="b63d7-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b63d7-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b63d7-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b63d7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b63d7-131">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="b63d7-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




