---
description: O método OnStartStreaming redefine todos os horários que controlam o streaming.
ms.assetid: a2bb07f2-6880-4030-96c5-d146982dfe66
title: Método CBaseVideoRenderer. OnStartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403d465d4ff9fe8ae9101b13e2ec5e6c04bdddf2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751901"
---
# <a name="cbasevideorendereronstartstreaming-method"></a><span data-ttu-id="a8650-103">Método CBaseVideoRenderer. OnStartStreaming</span><span class="sxs-lookup"><span data-stu-id="a8650-103">CBaseVideoRenderer.OnStartStreaming method</span></span>

<span data-ttu-id="a8650-104">O `OnStartStreaming` método redefine todos os horários que controlam o streaming.</span><span class="sxs-lookup"><span data-stu-id="a8650-104">The `OnStartStreaming` method resets all times that control streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8650-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8650-105">Syntax</span></span>


```C++
HRESULT OnStartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="a8650-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8650-106">Parameters</span></span>

<span data-ttu-id="a8650-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a8650-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a8650-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8650-108">Return value</span></span>

<span data-ttu-id="a8650-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a8650-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8650-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8650-110">Remarks</span></span>

<span data-ttu-id="a8650-111">Essa função de membro substitui [**CBaseRenderer:: OnStartStreaming**](cbaserenderer-onstartstreaming.md).</span><span class="sxs-lookup"><span data-stu-id="a8650-111">This member function overrides [**CBaseRenderer::OnStartStreaming**](cbaserenderer-onstartstreaming.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8650-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8650-112">Requirements</span></span>



| <span data-ttu-id="a8650-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8650-113">Requirement</span></span> | <span data-ttu-id="a8650-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a8650-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8650-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8650-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a8650-116"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8650-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a8650-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8650-117">Library</span></span><br/> | <dl> <span data-ttu-id="a8650-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a8650-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8650-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8650-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8650-120">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="a8650-120">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




