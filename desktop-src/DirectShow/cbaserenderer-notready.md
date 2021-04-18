---
description: O método não Ready sinaliza que uma transição de estado ainda não foi concluída.
ms.assetid: 85529a22-5343-4c22-b282-31c0e7ff0f5f
title: Método CBaseRenderer. não Ready (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff07303f9aa8f68ae702ed09bc3a2fd544373f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778629"
---
# <a name="cbaserenderernotready-method"></a><span data-ttu-id="082d5-103">Método CBaseRenderer. não Ready</span><span class="sxs-lookup"><span data-stu-id="082d5-103">CBaseRenderer.NotReady method</span></span>

<span data-ttu-id="082d5-104">O `NotReady` método sinaliza que uma transição de estado ainda não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="082d5-104">The `NotReady` method signals that a state transition is not yet complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="082d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="082d5-105">Syntax</span></span>


```C++
void NotReady();
```



## <a name="parameters"></a><span data-ttu-id="082d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="082d5-106">Parameters</span></span>

<span data-ttu-id="082d5-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="082d5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="082d5-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="082d5-108">Return value</span></span>

<span data-ttu-id="082d5-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="082d5-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="082d5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="082d5-110">Remarks</span></span>

<span data-ttu-id="082d5-111">Esse método faz com que o método [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) retorne o VFW \_ S \_ State \_ intermediário, que indica que o filtro ainda está em transição para seu estado atual.</span><span class="sxs-lookup"><span data-stu-id="082d5-111">This method causes the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method to return VFW\_S\_STATE\_INTERMEDIATE, which indicates that the filter is still transitioning to its current state.</span></span> <span data-ttu-id="082d5-112">O filtro chama esse método sempre que uma transição de estado está pendente.</span><span class="sxs-lookup"><span data-stu-id="082d5-112">The filter calls this method whenever a state transition is pending.</span></span> <span data-ttu-id="082d5-113">(Isso ocorre quando o filtro é pausado, até receber um exemplo.)</span><span class="sxs-lookup"><span data-stu-id="082d5-113">(This occurs when the filter pauses, until it receives a sample.)</span></span>

## <a name="requirements"></a><span data-ttu-id="082d5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="082d5-114">Requirements</span></span>



| <span data-ttu-id="082d5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="082d5-115">Requirement</span></span> | <span data-ttu-id="082d5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="082d5-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="082d5-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="082d5-117">Header</span></span><br/>  | <dl> <span data-ttu-id="082d5-118"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="082d5-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="082d5-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="082d5-119">Library</span></span><br/> | <dl> <span data-ttu-id="082d5-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="082d5-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="082d5-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="082d5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="082d5-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="082d5-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="082d5-123">**CheckReady**</span><span class="sxs-lookup"><span data-stu-id="082d5-123">**CheckReady**</span></span>](cbaserenderer-checkready.md)
</dt> <dt>

[<span data-ttu-id="082d5-124">**Ready**</span><span class="sxs-lookup"><span data-stu-id="082d5-124">**Ready**</span></span>](cbaserenderer-ready.md)
</dt> </dl>

 

 




