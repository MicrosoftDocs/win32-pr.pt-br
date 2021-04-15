---
description: O método DoRenderSample renderiza um exemplo.
ms.assetid: cf06192c-44c0-4d88-a20e-6501ea48cbfd
title: Método CBaseRenderer. DoRenderSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.DoRenderSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935fd7b92cef5d51056b2eb2daa9d2fb775647b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747603"
---
# <a name="cbaserendererdorendersample-method"></a><span data-ttu-id="4f218-103">Método CBaseRenderer. DoRenderSample</span><span class="sxs-lookup"><span data-stu-id="4f218-103">CBaseRenderer.DoRenderSample method</span></span>

<span data-ttu-id="4f218-104">O `DoRenderSample` método renderiza um exemplo.</span><span class="sxs-lookup"><span data-stu-id="4f218-104">The `DoRenderSample` method renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f218-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f218-105">Syntax</span></span>


```C++
virtual HRESULT DoRenderSample(
   IMediaSample *pMediaSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="4f218-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f218-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f218-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="4f218-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="4f218-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="4f218-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f218-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f218-109">Return value</span></span>

<span data-ttu-id="4f218-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4f218-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f218-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f218-111">Remarks</span></span>

<span data-ttu-id="4f218-112">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="4f218-112">The derived class must implement this method.</span></span> <span data-ttu-id="4f218-113">O comportamento depende totalmente do tipo de filtro que está sendo implementado.</span><span class="sxs-lookup"><span data-stu-id="4f218-113">The behavior depends entirely on the type of filter being implemented.</span></span> <span data-ttu-id="4f218-114">Um processador de vídeo, por exemplo, desenharia a imagem de vídeo contida no exemplo.</span><span class="sxs-lookup"><span data-stu-id="4f218-114">A video renderer, for example, would draw the video image contained in the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f218-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f218-115">Requirements</span></span>



| <span data-ttu-id="4f218-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f218-116">Requirement</span></span> | <span data-ttu-id="4f218-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4f218-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f218-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f218-118">Header</span></span><br/>  | <dl> <span data-ttu-id="4f218-119"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f218-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4f218-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f218-120">Library</span></span><br/> | <dl> <span data-ttu-id="4f218-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4f218-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f218-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f218-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f218-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="4f218-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




