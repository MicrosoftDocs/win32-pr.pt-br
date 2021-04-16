---
description: O método OnReceiveFirstSample é chamado quando o filtro recebe um exemplo enquanto está em pausa.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: Método CBaseRenderer. OnReceiveFirstSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2368b0e2abda3bcdd08872d730f8b9902dad43ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750486"
---
# <a name="cbaserendereronreceivefirstsample-method"></a><span data-ttu-id="7bb6b-103">Método CBaseRenderer. OnReceiveFirstSample</span><span class="sxs-lookup"><span data-stu-id="7bb6b-103">CBaseRenderer.OnReceiveFirstSample method</span></span>

<span data-ttu-id="7bb6b-104">O `OnReceiveFirstSample` método é chamado quando o filtro recebe um exemplo enquanto está em pausa.</span><span class="sxs-lookup"><span data-stu-id="7bb6b-104">The `OnReceiveFirstSample` method is called when the filter receives a sample while paused.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bb6b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7bb6b-105">Syntax</span></span>


```C++
virtual void OnReceiveFirstSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="7bb6b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bb6b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bb6b-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="7bb6b-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="7bb6b-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="7bb6b-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bb6b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7bb6b-109">Return value</span></span>

<span data-ttu-id="7bb6b-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7bb6b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bb6b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bb6b-111">Remarks</span></span>

<span data-ttu-id="7bb6b-112">O método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="7bb6b-112">The [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method calls this method.</span></span> <span data-ttu-id="7bb6b-113">Ele não faz nada na classe base, mas a classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="7bb6b-113">It does nothing in the base class, but the derived class can override it.</span></span> <span data-ttu-id="7bb6b-114">Esse método destina-se principalmente a renderizadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7bb6b-114">This method is intended primarily for video renderers.</span></span> <span data-ttu-id="7bb6b-115">Quando um processador de vídeo é pausado, ele normalmente exibe a primeira amostra como uma imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="7bb6b-115">When a video renderer is paused, it typically displays the first sample as a still image.</span></span>

<span data-ttu-id="7bb6b-116">Procurar o grafo enquanto estiver em pausa também faz com que esse método seja chamado.</span><span class="sxs-lookup"><span data-stu-id="7bb6b-116">Seeking the graph while paused also causes this method to be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bb6b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bb6b-117">Requirements</span></span>



| <span data-ttu-id="7bb6b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bb6b-118">Requirement</span></span> | <span data-ttu-id="7bb6b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7bb6b-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb6b-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7bb6b-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7bb6b-121"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7bb6b-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7bb6b-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7bb6b-122">Library</span></span><br/> | <dl> <span data-ttu-id="7bb6b-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7bb6b-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bb6b-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bb6b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bb6b-125">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="7bb6b-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




