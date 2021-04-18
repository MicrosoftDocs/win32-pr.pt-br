---
description: O método SetPopEvent especifica um evento que é sinalizado sempre que o objeto remove um exemplo da fila.
ms.assetid: 147a09b9-14d3-4739-843a-1bfb19d2d052
title: Método COutputQueue. SetPopEvent (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.SetPopEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 764abf76265fce66c5798923ca1fa522edd682af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758692"
---
# <a name="coutputqueuesetpopevent-method"></a><span data-ttu-id="2de4d-103">Método COutputQueue. SetPopEvent</span><span class="sxs-lookup"><span data-stu-id="2de4d-103">COutputQueue.SetPopEvent method</span></span>

<span data-ttu-id="2de4d-104">O `SetPopEvent` método especifica um evento que é sinalizado sempre que o objeto remove um exemplo da fila.</span><span class="sxs-lookup"><span data-stu-id="2de4d-104">The `SetPopEvent` method specifies an event that is signaled whenever the object removes a sample from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="2de4d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2de4d-105">Syntax</span></span>


```C++
void SetPopEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a><span data-ttu-id="2de4d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2de4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2de4d-107">*hEvent*</span><span class="sxs-lookup"><span data-stu-id="2de4d-107">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="2de4d-108">Identificador para um evento criado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="2de4d-108">Handle to an event created by the caller.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2de4d-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2de4d-109">Return value</span></span>

<span data-ttu-id="2de4d-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2de4d-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2de4d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2de4d-111">Requirements</span></span>



| <span data-ttu-id="2de4d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2de4d-112">Requirement</span></span> | <span data-ttu-id="2de4d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="2de4d-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2de4d-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2de4d-114">Header</span></span><br/>  | <dl> <span data-ttu-id="2de4d-115"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2de4d-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2de4d-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2de4d-116">Library</span></span><br/> | <dl> <span data-ttu-id="2de4d-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2de4d-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2de4d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="2de4d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2de4d-119">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="2de4d-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




