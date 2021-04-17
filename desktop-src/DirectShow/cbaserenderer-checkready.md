---
description: O método CheckReady consulta se uma transição de estado foi concluída.
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: Método CBaseRenderer. CheckReady (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28c0c8bcb6efb0e3cbd648c1e45d36e8b18d4b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748639"
---
# <a name="cbaserenderercheckready-method"></a><span data-ttu-id="3492c-103">Método CBaseRenderer. CheckReady</span><span class="sxs-lookup"><span data-stu-id="3492c-103">CBaseRenderer.CheckReady method</span></span>

<span data-ttu-id="3492c-104">O `CheckReady` método consulta se uma transição de estado foi concluída.</span><span class="sxs-lookup"><span data-stu-id="3492c-104">The `CheckReady` method queries whether a state transition is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="3492c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3492c-105">Syntax</span></span>


```C++
BOOL CheckReady();
```



## <a name="parameters"></a><span data-ttu-id="3492c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3492c-106">Parameters</span></span>

<span data-ttu-id="3492c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3492c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3492c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3492c-108">Return value</span></span>

<span data-ttu-id="3492c-109">Retornará **true** se a transição de estado estiver concluída ou **false** se o filtro ainda estiver em transição para um novo estado.</span><span class="sxs-lookup"><span data-stu-id="3492c-109">Returns **TRUE** if the state transition is complete, or **FALSE** if the filter is still transitioning to a new state.</span></span>

## <a name="requirements"></a><span data-ttu-id="3492c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3492c-110">Requirements</span></span>



| <span data-ttu-id="3492c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3492c-111">Requirement</span></span> | <span data-ttu-id="3492c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="3492c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3492c-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3492c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="3492c-114"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3492c-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3492c-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3492c-115">Library</span></span><br/> | <dl> <span data-ttu-id="3492c-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3492c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3492c-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="3492c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3492c-118">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="3492c-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="3492c-119">**CBaseRenderer:: não é possível ler**</span><span class="sxs-lookup"><span data-stu-id="3492c-119">**CBaseRenderer::NotReady**</span></span>](cbaserenderer-notready.md)
</dt> <dt>

[<span data-ttu-id="3492c-120">**CBaseRenderer:: pronto**</span><span class="sxs-lookup"><span data-stu-id="3492c-120">**CBaseRenderer::Ready**</span></span>](cbaserenderer-ready.md)
</dt> </dl>

 

 




