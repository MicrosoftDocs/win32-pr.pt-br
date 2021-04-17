---
description: O método PrepareRender é chamado antes de o filtro renderizar um exemplo.
ms.assetid: 0b137da9-eac0-469f-b457-719a36569c82
title: Método CBaseRenderer. PrepareRender (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.PrepareRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee5739a839222900458ae334de6f97fb6d18876b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754547"
---
# <a name="cbaserendererpreparerender-method"></a><span data-ttu-id="7665d-103">Método CBaseRenderer. PrepareRender</span><span class="sxs-lookup"><span data-stu-id="7665d-103">CBaseRenderer.PrepareRender method</span></span>

<span data-ttu-id="7665d-104">O `PrepareRender` método é chamado antes de o filtro renderizar um exemplo.</span><span class="sxs-lookup"><span data-stu-id="7665d-104">The `PrepareRender` method is called before the filter renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="7665d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7665d-105">Syntax</span></span>


```C++
virtual void PrepareRender();
```



## <a name="parameters"></a><span data-ttu-id="7665d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7665d-106">Parameters</span></span>

<span data-ttu-id="7665d-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7665d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7665d-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7665d-108">Return value</span></span>

<span data-ttu-id="7665d-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7665d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7665d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7665d-110">Remarks</span></span>

<span data-ttu-id="7665d-111">O filtro chama esse método antes de chamar o método [**CBaseRenderer:: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) ou o método [**CBaseRenderer:: render**](cbaserenderer-render.md) .</span><span class="sxs-lookup"><span data-stu-id="7665d-111">The filter calls this method before it calls the [**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) method or the [**CBaseRenderer::Render**](cbaserenderer-render.md) method.</span></span> <span data-ttu-id="7665d-112">`PrepareRender` Não faz nada na classe base.</span><span class="sxs-lookup"><span data-stu-id="7665d-112">`PrepareRender` does not do anything in the base class.</span></span> <span data-ttu-id="7665d-113">A classe derivada pode substituí-la para executar as ações necessárias antes da renderização.</span><span class="sxs-lookup"><span data-stu-id="7665d-113">The derived class can override it to perform any actions required before rendering.</span></span> <span data-ttu-id="7665d-114">Por exemplo, um renderizador de vídeo pode substituir esse método para obter sua paleta.</span><span class="sxs-lookup"><span data-stu-id="7665d-114">For example, a video renderer can override this method to realize its palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="7665d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7665d-115">Requirements</span></span>



| <span data-ttu-id="7665d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7665d-116">Requirement</span></span> | <span data-ttu-id="7665d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="7665d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7665d-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7665d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7665d-119"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7665d-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7665d-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7665d-120">Library</span></span><br/> | <dl> <span data-ttu-id="7665d-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7665d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7665d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="7665d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7665d-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="7665d-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




