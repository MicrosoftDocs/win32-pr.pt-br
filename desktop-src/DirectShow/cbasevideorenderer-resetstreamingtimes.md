---
description: O método ResetStreamingTimes redefine todos os horários que controlam o streaming.
ms.assetid: 8a596760-a45a-4486-bb91-aab10bbf927f
title: Método CBaseVideoRenderer. ResetStreamingTimes (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ResetStreamingTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d887ca9e246d5e3fb746c119b1ed6784201ec702
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749025"
---
# <a name="cbasevideorendererresetstreamingtimes-method"></a><span data-ttu-id="5141c-103">Método CBaseVideoRenderer. ResetStreamingTimes</span><span class="sxs-lookup"><span data-stu-id="5141c-103">CBaseVideoRenderer.ResetStreamingTimes method</span></span>

<span data-ttu-id="5141c-104">O `ResetStreamingTimes` método redefine todos os horários que controlam o streaming.</span><span class="sxs-lookup"><span data-stu-id="5141c-104">The `ResetStreamingTimes` method resets all times that control the streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="5141c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5141c-105">Syntax</span></span>


```C++
virtual HRESULT ResetStreamingTimes();
```



## <a name="parameters"></a><span data-ttu-id="5141c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5141c-106">Parameters</span></span>

<span data-ttu-id="5141c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5141c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5141c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5141c-108">Return value</span></span>

<span data-ttu-id="5141c-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5141c-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5141c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5141c-110">Remarks</span></span>

<span data-ttu-id="5141c-111">Os horários são definidos de modo que os quadros não serão inicialmente descartados e, portanto, o primeiro quadro será desenhado.</span><span class="sxs-lookup"><span data-stu-id="5141c-111">The times are set so that frames will not be initially dropped and so that the first frame will be drawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="5141c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5141c-112">Requirements</span></span>



| <span data-ttu-id="5141c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5141c-113">Requirement</span></span> | <span data-ttu-id="5141c-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5141c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5141c-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5141c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="5141c-116"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5141c-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5141c-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5141c-117">Library</span></span><br/> | <dl> <span data-ttu-id="5141c-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5141c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5141c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5141c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5141c-120">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="5141c-120">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




