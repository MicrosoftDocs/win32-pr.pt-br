---
description: O método inativo é chamado quando o estado é alternado para parado.
ms.assetid: 2bad81ef-d2a4-4c20-a49b-e40e5097b430
title: Método CBaseRenderer. Inactive (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9ac328c772b740a0d7ab05be4c6ea9f2a24f852e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753345"
---
# <a name="cbaserendererinactive-method"></a><span data-ttu-id="d5f6d-103">Método CBaseRenderer. Inactive</span><span class="sxs-lookup"><span data-stu-id="d5f6d-103">CBaseRenderer.Inactive method</span></span>

<span data-ttu-id="d5f6d-104">O `Inactive` método é chamado quando o estado é alternado para parado.</span><span class="sxs-lookup"><span data-stu-id="d5f6d-104">The `Inactive` method is called when the state is switched to stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f6d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5f6d-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="d5f6d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5f6d-106">Parameters</span></span>

<span data-ttu-id="d5f6d-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d5f6d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d5f6d-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5f6d-108">Return value</span></span>

<span data-ttu-id="d5f6d-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d5f6d-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5f6d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d5f6d-110">Remarks</span></span>

<span data-ttu-id="d5f6d-111">O pino de entrada chama esse método de seu próprio método [**CRendererInputPin:: Inactive**](crendererinputpin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="d5f6d-111">The input pin calls this method from its own [**CRendererInputPin::Inactive**](crendererinputpin-inactive.md) method.</span></span> <span data-ttu-id="d5f6d-112">O filtro chama o método [**CBaseRenderer:: ClearPendingSample**](cbaserenderer-clearpendingsample.md) para liberar o exemplo mais recente.</span><span class="sxs-lookup"><span data-stu-id="d5f6d-112">The filter calls the [**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md) method to release the most recent sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5f6d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5f6d-113">Requirements</span></span>



| <span data-ttu-id="d5f6d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5f6d-114">Requirement</span></span> | <span data-ttu-id="d5f6d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d5f6d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f6d-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d5f6d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d5f6d-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5f6d-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d5f6d-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5f6d-118">Library</span></span><br/> | <dl> <span data-ttu-id="d5f6d-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d5f6d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f6d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5f6d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f6d-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="d5f6d-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




