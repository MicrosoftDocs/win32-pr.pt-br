---
description: 'O método Receive recebe o exemplo de próxima mídia no fluxo. Esse método substitui o método CBaseInputPin:: Receive.'
ms.assetid: b09140f0-2e3a-47b1-ace7-954043dd62eb
title: Método CRendererInputPin. Receive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3ddac3f456e1ab24574a4743983d20a828896e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748804"
---
# <a name="crendererinputpinreceive-method"></a><span data-ttu-id="7153e-104">Método CRendererInputPin. Receive</span><span class="sxs-lookup"><span data-stu-id="7153e-104">CRendererInputPin.Receive method</span></span>

<span data-ttu-id="7153e-105">O `Receive` método recebe o próximo exemplo de mídia no fluxo.</span><span class="sxs-lookup"><span data-stu-id="7153e-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="7153e-106">Esse método substitui o método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) .</span><span class="sxs-lookup"><span data-stu-id="7153e-106">This method overrides the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7153e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7153e-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="7153e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7153e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7153e-109">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="7153e-109">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="7153e-110">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="7153e-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7153e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7153e-111">Return value</span></span>

<span data-ttu-id="7153e-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7153e-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7153e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7153e-113">Remarks</span></span>

<span data-ttu-id="7153e-114">Esse método chama o método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) do filtro, que manipula a renderização.</span><span class="sxs-lookup"><span data-stu-id="7153e-114">This method calls the filter's [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method, which handles the rendering.</span></span> <span data-ttu-id="7153e-115">Se esse método falhar, o PIN enviará um \_ evento de ERRORABORT do EC.</span><span class="sxs-lookup"><span data-stu-id="7153e-115">If that method fails, the pin sends an EC\_ERRORABORT event.</span></span>

## <a name="requirements"></a><span data-ttu-id="7153e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7153e-116">Requirements</span></span>



| <span data-ttu-id="7153e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7153e-117">Requirement</span></span> | <span data-ttu-id="7153e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7153e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7153e-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7153e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7153e-120"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7153e-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7153e-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7153e-121">Library</span></span><br/> | <dl> <span data-ttu-id="7153e-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7153e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7153e-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7153e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7153e-124">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="7153e-124">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




