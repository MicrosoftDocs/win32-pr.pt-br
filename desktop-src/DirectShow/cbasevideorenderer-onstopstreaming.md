---
description: O método OnStopStreaming é chamado no final do streaming para corrigir os tempos para o relatório da página de propriedades.
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: Método CBaseVideoRenderer. OnStopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08cf23fd2e1a7e854625d8a369d15290591386fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782267"
---
# <a name="cbasevideorendereronstopstreaming-method"></a><span data-ttu-id="a54f5-103">Método CBaseVideoRenderer. OnStopStreaming</span><span class="sxs-lookup"><span data-stu-id="a54f5-103">CBaseVideoRenderer.OnStopStreaming method</span></span>

<span data-ttu-id="a54f5-104">O `OnStopStreaming` método é chamado no final do streaming para corrigir os tempos para o relatório da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="a54f5-104">The `OnStopStreaming` method is called at the end of streaming to fix times for the property page report.</span></span>

## <a name="syntax"></a><span data-ttu-id="a54f5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a54f5-105">Syntax</span></span>


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="a54f5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a54f5-106">Parameters</span></span>

<span data-ttu-id="a54f5-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a54f5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a54f5-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a54f5-108">Return value</span></span>

<span data-ttu-id="a54f5-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a54f5-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a54f5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a54f5-110">Remarks</span></span>

<span data-ttu-id="a54f5-111">Essa função de membro é chamada duas vezes, uma vez ao pausar e novamente quando o fluxo é realmente interrompido.</span><span class="sxs-lookup"><span data-stu-id="a54f5-111">This member function is called twice, once when pausing and again when the stream is actually stopped.</span></span>

<span data-ttu-id="a54f5-112">Essa função de membro substitui [**CBaseRenderer:: OnStopStreaming**](cbaserenderer-onstopstreaming.md).</span><span class="sxs-lookup"><span data-stu-id="a54f5-112">This member function overrides [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a54f5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a54f5-113">Requirements</span></span>



| <span data-ttu-id="a54f5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a54f5-114">Requirement</span></span> | <span data-ttu-id="a54f5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a54f5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a54f5-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a54f5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a54f5-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a54f5-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a54f5-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a54f5-118">Library</span></span><br/> | <dl> <span data-ttu-id="a54f5-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a54f5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a54f5-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="a54f5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a54f5-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="a54f5-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




