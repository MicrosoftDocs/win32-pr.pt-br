---
description: Construtor de CAMMsgEvent. CAMMsgEvent-método de construtor.
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: Construtor CAMMsgEvent. CAMMsgEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dac72ecb97a1ea1fd2594af9c11b8a03078cf2cb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096525"
---
# <a name="cammsgeventcammsgevent-constructor"></a><span data-ttu-id="42e4d-103">Construtor CAMMsgEvent. CAMMsgEvent</span><span class="sxs-lookup"><span data-stu-id="42e4d-103">CAMMsgEvent.CAMMsgEvent constructor</span></span>

<span data-ttu-id="42e4d-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="42e4d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="42e4d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="42e4d-105">Syntax</span></span>


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="42e4d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="42e4d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42e4d-107">*phr*</span><span class="sxs-lookup"><span data-stu-id="42e4d-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="42e4d-108">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="42e4d-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="42e4d-109">Se o Construtor falhar, esse parâmetro receberá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="42e4d-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="42e4d-110">Se isso ocorrer, o objeto não está em um estado válido.</span><span class="sxs-lookup"><span data-stu-id="42e4d-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="42e4d-111">Para compatibilidade com versões anteriores do Strmbase. lib, esse parâmetro assume **nulo** como padrão.</span><span class="sxs-lookup"><span data-stu-id="42e4d-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="42e4d-112">No entanto, a passagem de um valor não **nulo** é preferida, para que o chamador possa verificar o status do objeto.</span><span class="sxs-lookup"><span data-stu-id="42e4d-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42e4d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42e4d-113">Requirements</span></span>



| <span data-ttu-id="42e4d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="42e4d-114">Requirement</span></span> | <span data-ttu-id="42e4d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="42e4d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42e4d-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="42e4d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="42e4d-117"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42e4d-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="42e4d-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42e4d-118">Library</span></span><br/> | <dl> <span data-ttu-id="42e4d-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="42e4d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42e4d-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="42e4d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42e4d-121">**Classe CAMMsgEvent**</span><span class="sxs-lookup"><span data-stu-id="42e4d-121">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




