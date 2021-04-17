---
description: O método FreeSamples libera Todas as amostras pendentes.
ms.assetid: 61b7fe6e-41cc-4d5e-b083-bbc400d04e39
title: Método COutputQueue. FreeSamples (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.FreeSamples
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70d0680d2a1a3ac020be84f244e1cc02bb6efad0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748436"
---
# <a name="coutputqueuefreesamples-method"></a><span data-ttu-id="a09f2-103">Método COutputQueue. FreeSamples</span><span class="sxs-lookup"><span data-stu-id="a09f2-103">COutputQueue.FreeSamples method</span></span>

<span data-ttu-id="a09f2-104">O `FreeSamples` método libera Todas as amostras pendentes.</span><span class="sxs-lookup"><span data-stu-id="a09f2-104">The `FreeSamples` method frees all pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="a09f2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a09f2-105">Syntax</span></span>


```C++
void FreeSamples();
```



## <a name="parameters"></a><span data-ttu-id="a09f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a09f2-106">Parameters</span></span>

<span data-ttu-id="a09f2-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a09f2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a09f2-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a09f2-108">Return value</span></span>

<span data-ttu-id="a09f2-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a09f2-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a09f2-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a09f2-110">Remarks</span></span>

<span data-ttu-id="a09f2-111">Esse método remove todas as amostras pendentes da fila e da matriz de exemplo.</span><span class="sxs-lookup"><span data-stu-id="a09f2-111">This method removes any pending samples from the queue and from the sample array.</span></span>

## <a name="requirements"></a><span data-ttu-id="a09f2-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a09f2-112">Requirements</span></span>



| <span data-ttu-id="a09f2-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a09f2-113">Requirement</span></span> | <span data-ttu-id="a09f2-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a09f2-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a09f2-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a09f2-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a09f2-116"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a09f2-116"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a09f2-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a09f2-117">Library</span></span><br/> | <dl> <span data-ttu-id="a09f2-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a09f2-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a09f2-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a09f2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a09f2-120">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="a09f2-120">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




