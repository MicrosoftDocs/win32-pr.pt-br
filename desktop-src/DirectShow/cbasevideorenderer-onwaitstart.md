---
description: O método OnWaitStart atualiza o tempo gasto aguardando e não aguardando.
ms.assetid: 3f2e2bf2-f205-4b59-b969-cf8c2136437d
title: Método CBaseVideoRenderer. OnWaitStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4fab7e1a1f24c3d00f46018db9478990be71666
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770107"
---
# <a name="cbasevideorendereronwaitstart-method"></a><span data-ttu-id="e6846-103">Método CBaseVideoRenderer. OnWaitStart</span><span class="sxs-lookup"><span data-stu-id="e6846-103">CBaseVideoRenderer.OnWaitStart method</span></span>

<span data-ttu-id="e6846-104">O `OnWaitStart` método atualiza os tempos gasto aguardando e não aguardando.</span><span class="sxs-lookup"><span data-stu-id="e6846-104">The `OnWaitStart` method updates times spent waiting and not waiting.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6846-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6846-105">Syntax</span></span>


```C++
void OnWaitStart();
```



## <a name="parameters"></a><span data-ttu-id="e6846-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6846-106">Parameters</span></span>

<span data-ttu-id="e6846-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e6846-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6846-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6846-108">Return value</span></span>

<span data-ttu-id="e6846-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e6846-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6846-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6846-110">Remarks</span></span>

<span data-ttu-id="e6846-111">Essa função de membro é chamada ao começar a aguardar um evento de renderização.</span><span class="sxs-lookup"><span data-stu-id="e6846-111">This member function is called when starting to wait for a rendering event.</span></span> <span data-ttu-id="e6846-112">Ele é usado apenas para medições de desempenho.</span><span class="sxs-lookup"><span data-stu-id="e6846-112">It is used only for performance measurements.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6846-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6846-113">Requirements</span></span>



| <span data-ttu-id="e6846-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6846-114">Requirement</span></span> | <span data-ttu-id="e6846-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e6846-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6846-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6846-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e6846-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6846-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6846-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6846-118">Library</span></span><br/> | <dl> <span data-ttu-id="e6846-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e6846-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6846-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6846-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6846-121">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="e6846-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




