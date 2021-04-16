---
description: O método OnDirectRender coleta informações de tempo que controlam a sincronização e o controle de qualidade.
ms.assetid: ed617fac-b2c6-4a3a-ac91-77e2d7cce981
title: Método CBaseVideoRenderer. OnDirectRender (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnDirectRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c117366590c96b63ff4595d4563e92aec542cfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758701"
---
# <a name="cbasevideorendererondirectrender-method"></a><span data-ttu-id="8627e-103">Método CBaseVideoRenderer. OnDirectRender</span><span class="sxs-lookup"><span data-stu-id="8627e-103">CBaseVideoRenderer.OnDirectRender method</span></span>

<span data-ttu-id="8627e-104">O método **OnDirectRender** coleta informações de tempo que controlam a sincronização e o controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="8627e-104">The **OnDirectRender** method collects timing information that controls synchronization and quality control.</span></span>

## <a name="syntax"></a><span data-ttu-id="8627e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8627e-105">Syntax</span></span>


```C++
virtual HRESULT OnDirectRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="8627e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8627e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8627e-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="8627e-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="8627e-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8627e-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8627e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8627e-109">Return value</span></span>

<span data-ttu-id="8627e-110">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8627e-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8627e-111">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8627e-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8627e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8627e-112">Remarks</span></span>

<span data-ttu-id="8627e-113">Chame esse método em vez de [**OnRenderStart**](cbasevideorenderer-onrenderstart.md) e [**OnRenderEnd**](cbasevideorenderer-onrenderend.md).</span><span class="sxs-lookup"><span data-stu-id="8627e-113">Call this method instead of [**OnRenderStart**](cbasevideorenderer-onrenderstart.md) and [**OnRenderEnd**](cbasevideorenderer-onrenderend.md).</span></span> <span data-ttu-id="8627e-114">Esse método é usado pelo renderizador de vídeo do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="8627e-114">This method is used by the DirectDraw video renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8627e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8627e-115">Requirements</span></span>



| <span data-ttu-id="8627e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8627e-116">Requirement</span></span> | <span data-ttu-id="8627e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8627e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8627e-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8627e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8627e-119"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8627e-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8627e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8627e-120">Library</span></span><br/> | <dl> <span data-ttu-id="8627e-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8627e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8627e-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="8627e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8627e-123">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="8627e-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




