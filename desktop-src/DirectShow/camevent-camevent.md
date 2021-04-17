---
description: Método de construtor.
ms.assetid: 35c9ac07-8756-42b1-beeb-5f0e79466742
title: Construtor CAMEvent. CAMEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.CAMEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a01d9d1f592675f58d19e81b800c966dddaca1c3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756212"
---
# <a name="cameventcamevent-constructor"></a><span data-ttu-id="732e1-103">Construtor CAMEvent. CAMEvent</span><span class="sxs-lookup"><span data-stu-id="732e1-103">CAMEvent.CAMEvent constructor</span></span>

<span data-ttu-id="732e1-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="732e1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="732e1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="732e1-105">Syntax</span></span>


```C++
CAMEvent(
   BOOL    fManualReset,
   HRESULT *phr
);
```



## <a name="parameters"></a><span data-ttu-id="732e1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="732e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="732e1-107">*fManualReset*</span><span class="sxs-lookup"><span data-stu-id="732e1-107">*fManualReset*</span></span> 
</dt> <dd>

<span data-ttu-id="732e1-108">Valor booliano que especifica se o objeto é um evento de redefinição manual ou um evento de redefinição automática.</span><span class="sxs-lookup"><span data-stu-id="732e1-108">Boolean value that specifies whether the object is a manual-reset event or an auto-reset event.</span></span> <span data-ttu-id="732e1-109">Se for **true**, o objeto será um evento de redefinição manual.</span><span class="sxs-lookup"><span data-stu-id="732e1-109">If **TRUE**, the object is a manual-reset event.</span></span> <span data-ttu-id="732e1-110">Caso contrário, é um evento de redefinição automática.</span><span class="sxs-lookup"><span data-stu-id="732e1-110">Otherwise, it is an auto-reset event.</span></span>

</dd> <dt>

<span data-ttu-id="732e1-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="732e1-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="732e1-112">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="732e1-112">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="732e1-113">Se o Construtor falhar, esse parâmetro receberá um código de erro.</span><span class="sxs-lookup"><span data-stu-id="732e1-113">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="732e1-114">Se isso ocorrer, o objeto não está em um estado válido.</span><span class="sxs-lookup"><span data-stu-id="732e1-114">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="732e1-115">Para compatibilidade com versões anteriores do Strmbase. lib, esse parâmetro assume **nulo** como padrão.</span><span class="sxs-lookup"><span data-stu-id="732e1-115">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="732e1-116">No entanto, a passagem de um valor não **nulo** é preferida, para que o chamador possa verificar o status do objeto.</span><span class="sxs-lookup"><span data-stu-id="732e1-116">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="732e1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="732e1-117">Remarks</span></span>

<span data-ttu-id="732e1-118">O evento começa em um estado não sinalizado.</span><span class="sxs-lookup"><span data-stu-id="732e1-118">The event begins in a nonsignaled state.</span></span>

<span data-ttu-id="732e1-119">Com um evento de redefinição automática, o método [**CAMEvent:: Wait**](camevent-wait.md) redefine o evento para não sinalizado quando o método retorna.</span><span class="sxs-lookup"><span data-stu-id="732e1-119">With an auto-reset event, the [**CAMEvent::Wait**](camevent-wait.md) method resets the event to nonsignaled when the method returns.</span></span> <span data-ttu-id="732e1-120">Com um evento de redefinição manual, o evento permanece sinalizado até que você chame o método [**CAMEvent:: Reset**](camevent-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="732e1-120">With a manual-reset event, the event remains signaled until you call the [**CAMEvent::Reset**](camevent-reset.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="732e1-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="732e1-121">Requirements</span></span>



| <span data-ttu-id="732e1-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="732e1-122">Requirement</span></span> | <span data-ttu-id="732e1-123">Valor</span><span class="sxs-lookup"><span data-stu-id="732e1-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="732e1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="732e1-124">Header</span></span><br/>  | <dl> <span data-ttu-id="732e1-125"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="732e1-125"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="732e1-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="732e1-126">Library</span></span><br/> | <dl> <span data-ttu-id="732e1-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="732e1-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="732e1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="732e1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="732e1-129">**Classe CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="732e1-129">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




