---
description: 'O método Stop interrompe o filtro. Esse método implementa o método IMediaFilter:: Stop.'
ms.assetid: 68d77f9a-95a2-4a71-bbe1-28be76fbc538
title: Método CBaseFilter. Stop (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b4c4893edcf02fa18da3dc207a49f87c91b2a9ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752105"
---
# <a name="cbasefilterstop-method"></a><span data-ttu-id="f874d-104">Método CBaseFilter. Stop</span><span class="sxs-lookup"><span data-stu-id="f874d-104">CBaseFilter.Stop method</span></span>

<span data-ttu-id="f874d-105">O `Stop` método para o filtro.</span><span class="sxs-lookup"><span data-stu-id="f874d-105">The `Stop` method stops the filter.</span></span> <span data-ttu-id="f874d-106">Esse método implementa o método [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="f874d-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f874d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f874d-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="f874d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f874d-108">Parameters</span></span>

<span data-ttu-id="f874d-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="f874d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f874d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f874d-110">Return value</span></span>

<span data-ttu-id="f874d-111">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="f874d-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="f874d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f874d-112">Remarks</span></span>

<span data-ttu-id="f874d-113">Esse método chama o método [**CBasePin:: Inactive**](cbasepin-inactive.md) em cada um dos Pins conectados do filtro.</span><span class="sxs-lookup"><span data-stu-id="f874d-113">This method calls the [**CBasePin::Inactive**](cbasepin-inactive.md) method on each of the filter's connected pins.</span></span> <span data-ttu-id="f874d-114">Ele também define o estado do filtro como estado \_ parado.</span><span class="sxs-lookup"><span data-stu-id="f874d-114">It also sets the filter's state to State\_Stopped.</span></span>

<span data-ttu-id="f874d-115">Quando o filtro é interrompido, ele deve rejeitar amostras de upstream, parar de entregar amostras downstream, desligar threads de trabalho e liberar todos os recursos usados para streaming.</span><span class="sxs-lookup"><span data-stu-id="f874d-115">When the filter stops, it should reject samples from upstream, stop delivering samples downstream, shut down worker threads, and free any resources that it used for streaming.</span></span>

## <a name="requirements"></a><span data-ttu-id="f874d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f874d-116">Requirements</span></span>



| <span data-ttu-id="f874d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f874d-117">Requirement</span></span> | <span data-ttu-id="f874d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f874d-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f874d-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f874d-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f874d-120"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f874d-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f874d-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f874d-121">Library</span></span><br/> | <dl> <span data-ttu-id="f874d-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f874d-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f874d-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f874d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f874d-124">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="f874d-124">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




