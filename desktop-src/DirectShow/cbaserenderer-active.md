---
description: O método ativo é chamado quando o estado é alternado para em pausa ou em execução.
ms.assetid: 2913bc81-572d-4ee1-a1b6-9e1638e04c9d
title: Método CBaseRenderer. Active (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 11593ffb25a953f4269d84ee2b9c9d884a23e5fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758242"
---
# <a name="cbaserendereractive-method"></a><span data-ttu-id="ea6b5-103">Método CBaseRenderer. active</span><span class="sxs-lookup"><span data-stu-id="ea6b5-103">CBaseRenderer.Active method</span></span>

<span data-ttu-id="ea6b5-104">O `Active` método é chamado quando o estado é alternado para em pausa ou em execução.</span><span class="sxs-lookup"><span data-stu-id="ea6b5-104">The `Active` method is called when the state is switched to paused or running.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea6b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea6b5-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="ea6b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea6b5-106">Parameters</span></span>

<span data-ttu-id="ea6b5-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ea6b5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea6b5-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea6b5-108">Return value</span></span>

<span data-ttu-id="ea6b5-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea6b5-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea6b5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea6b5-110">Remarks</span></span>

<span data-ttu-id="ea6b5-111">O pino de entrada chama esse método de seu próprio método [**CRendererInputPin:: active**](crendererinputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="ea6b5-111">The input pin calls this method from its own [**CRendererInputPin::Active**](crendererinputpin-active.md) method.</span></span> <span data-ttu-id="ea6b5-112">Esse método não faz nada na classe base.</span><span class="sxs-lookup"><span data-stu-id="ea6b5-112">This method does nothing in the base class.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea6b5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea6b5-113">Requirements</span></span>



| <span data-ttu-id="ea6b5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea6b5-114">Requirement</span></span> | <span data-ttu-id="ea6b5-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ea6b5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea6b5-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea6b5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ea6b5-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea6b5-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ea6b5-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea6b5-118">Library</span></span><br/> | <dl> <span data-ttu-id="ea6b5-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ea6b5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea6b5-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea6b5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea6b5-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="ea6b5-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




