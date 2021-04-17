---
description: O método Ready sinaliza que uma transição de estado foi concluída.
ms.assetid: 01328281-cf25-43fd-9f9c-e55fccbac217
title: Método CBaseRenderer. Ready (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Ready
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a7f70ec258fde7f6208d44c35ca2c284f99e0a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748216"
---
# <a name="cbaserendererready-method"></a><span data-ttu-id="841eb-103">Método CBaseRenderer. Ready</span><span class="sxs-lookup"><span data-stu-id="841eb-103">CBaseRenderer.Ready method</span></span>

<span data-ttu-id="841eb-104">O `Ready` método sinaliza que uma transição de estado foi concluída.</span><span class="sxs-lookup"><span data-stu-id="841eb-104">The `Ready` method signals that a state transition is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="841eb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="841eb-105">Syntax</span></span>


```C++
void Ready();
```



## <a name="parameters"></a><span data-ttu-id="841eb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="841eb-106">Parameters</span></span>

<span data-ttu-id="841eb-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="841eb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="841eb-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="841eb-108">Return value</span></span>

<span data-ttu-id="841eb-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="841eb-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="841eb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="841eb-110">Remarks</span></span>

<span data-ttu-id="841eb-111">Esse método faz com que o método [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) retorne S \_ OK, o que indica que o filtro concluiu a transição para seu estado atual.</span><span class="sxs-lookup"><span data-stu-id="841eb-111">This method causes the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method to return S\_OK, which indicates that the filter has completed the transition to its current state.</span></span> <span data-ttu-id="841eb-112">O filtro chama esse método sempre que ele conclui uma transição de estado.</span><span class="sxs-lookup"><span data-stu-id="841eb-112">The filter calls this method whenever it completes a state transition.</span></span>

## <a name="requirements"></a><span data-ttu-id="841eb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="841eb-113">Requirements</span></span>



| <span data-ttu-id="841eb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="841eb-114">Requirement</span></span> | <span data-ttu-id="841eb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="841eb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="841eb-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="841eb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="841eb-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="841eb-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="841eb-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="841eb-118">Library</span></span><br/> | <dl> <span data-ttu-id="841eb-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="841eb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="841eb-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="841eb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="841eb-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="841eb-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="841eb-122">**CBaseRenderer::CheckReady**</span><span class="sxs-lookup"><span data-stu-id="841eb-122">**CBaseRenderer::CheckReady**</span></span>](cbaserenderer-checkready.md)
</dt> <dt>

[<span data-ttu-id="841eb-123">**CBaseRenderer:: não é possível ler**</span><span class="sxs-lookup"><span data-stu-id="841eb-123">**CBaseRenderer::NotReady**</span></span>](cbaserenderer-notready.md)
</dt> </dl>

 

 




