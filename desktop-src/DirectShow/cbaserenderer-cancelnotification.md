---
description: O método CancelNotification cancela o evento de temporizador que agenda a renderização.
ms.assetid: 56ddf692-a2e3-40f2-848f-2d592601ec00
title: Método CBaseRenderer. CancelNotification (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CancelNotification
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3330f369c5fcc45fe051a1964a504d5d40fcd091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769241"
---
# <a name="cbaserenderercancelnotification-method"></a><span data-ttu-id="90ee5-103">Método CBaseRenderer. CancelNotification</span><span class="sxs-lookup"><span data-stu-id="90ee5-103">CBaseRenderer.CancelNotification method</span></span>

<span data-ttu-id="90ee5-104">O `CancelNotification` método cancela o evento de temporizador que agenda a renderização.</span><span class="sxs-lookup"><span data-stu-id="90ee5-104">The `CancelNotification` method cancels the timer event that schedules rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="90ee5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90ee5-105">Syntax</span></span>


```C++
virtual HRESULT CancelNotification();
```



## <a name="parameters"></a><span data-ttu-id="90ee5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90ee5-106">Parameters</span></span>

<span data-ttu-id="90ee5-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="90ee5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="90ee5-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90ee5-108">Return value</span></span>

<span data-ttu-id="90ee5-109">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="90ee5-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="90ee5-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="90ee5-110">Return code</span></span>                                                                             | <span data-ttu-id="90ee5-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="90ee5-111">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="90ee5-112"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="90ee5-112"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="90ee5-113">Não havia nenhum evento de timer pendente.</span><span class="sxs-lookup"><span data-stu-id="90ee5-113">There was no pending timer event.</span></span><br/> |
| <dl> <span data-ttu-id="90ee5-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="90ee5-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="90ee5-115">Êxito.</span><span class="sxs-lookup"><span data-stu-id="90ee5-115">Success.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="90ee5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="90ee5-116">Remarks</span></span>

<span data-ttu-id="90ee5-117">O filtro chama esse método quando o streaming é interrompido.</span><span class="sxs-lookup"><span data-stu-id="90ee5-117">The filter calls this method when streaming stops.</span></span> <span data-ttu-id="90ee5-118">O método cancela qualquer renderização agendada.</span><span class="sxs-lookup"><span data-stu-id="90ee5-118">The method cancels any scheduled rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="90ee5-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90ee5-119">Requirements</span></span>



| <span data-ttu-id="90ee5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="90ee5-120">Requirement</span></span> | <span data-ttu-id="90ee5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="90ee5-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90ee5-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90ee5-122">Header</span></span><br/>  | <dl> <span data-ttu-id="90ee5-123"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90ee5-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="90ee5-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90ee5-124">Library</span></span><br/> | <dl> <span data-ttu-id="90ee5-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="90ee5-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90ee5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="90ee5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90ee5-127">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="90ee5-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




