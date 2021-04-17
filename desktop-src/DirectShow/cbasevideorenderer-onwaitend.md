---
description: O método OnWaitEnd é chamado quando um tempo de espera termina.
ms.assetid: 283627bb-599c-4711-abc4-b5f92dfd29a5
title: Método CBaseVideoRenderer. OnWaitEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnWaitEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36377565556a759c9268ef1bf31ff7774933ccc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748818"
---
# <a name="cbasevideorendereronwaitend-method"></a><span data-ttu-id="e6785-103">Método CBaseVideoRenderer. OnWaitEnd</span><span class="sxs-lookup"><span data-stu-id="e6785-103">CBaseVideoRenderer.OnWaitEnd method</span></span>

<span data-ttu-id="e6785-104">O método OnWaitEnd é chamado quando um tempo de espera termina.</span><span class="sxs-lookup"><span data-stu-id="e6785-104">The OnWaitEnd method is called when a wait time ends.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6785-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6785-105">Syntax</span></span>


```C++
void OnWaitEnd();
```



## <a name="parameters"></a><span data-ttu-id="e6785-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e6785-106">Parameters</span></span>

<span data-ttu-id="e6785-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e6785-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6785-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e6785-108">Return value</span></span>

<span data-ttu-id="e6785-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e6785-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6785-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6785-110">Remarks</span></span>

<span data-ttu-id="e6785-111">Essa função de membro só faz o registro em log de desempenho.</span><span class="sxs-lookup"><span data-stu-id="e6785-111">This member function does only performance logging.</span></span> <span data-ttu-id="e6785-112">Ele é chamado quando o thread está acordado aguardando na janela ou quando o próximo exemplo é devido a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="e6785-112">It is called when the thread is awoken from waiting in the window, or when the next sample is due to be rendered.</span></span> <span data-ttu-id="e6785-113">Ele pode, eventualmente, ser usado para reunir informações que controlam a sincronização.</span><span class="sxs-lookup"><span data-stu-id="e6785-113">It could eventually be used to gather information that controls synchronization.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6785-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6785-114">Requirements</span></span>



| <span data-ttu-id="e6785-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6785-115">Requirement</span></span> | <span data-ttu-id="e6785-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e6785-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6785-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6785-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e6785-118"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6785-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6785-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6785-119">Library</span></span><br/> | <dl> <span data-ttu-id="e6785-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e6785-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6785-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6785-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6785-122">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="e6785-122">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




