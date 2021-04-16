---
description: O método SynchronousBlockOutputPin bloqueia o PIN; Não retorna até que o PIN seja bloqueado.
ms.assetid: 10fdb788-bc72-4eda-b60b-af83f954d689
title: Método CDynamicOutputPin. SynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fff1a0a1f093b97d07c74d7916ef2a7511d0e16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757424"
---
# <a name="cdynamicoutputpinsynchronousblockoutputpin-method"></a><span data-ttu-id="6ceba-103">Método CDynamicOutputPin. SynchronousBlockOutputPin</span><span class="sxs-lookup"><span data-stu-id="6ceba-103">CDynamicOutputPin.SynchronousBlockOutputPin method</span></span>

<span data-ttu-id="6ceba-104">O `SynchronousBlockOutputPin` método bloqueia o PIN; não retorna até que o PIN seja bloqueado.</span><span class="sxs-lookup"><span data-stu-id="6ceba-104">The `SynchronousBlockOutputPin` method blocks the pin; does not return until the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ceba-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ceba-105">Syntax</span></span>


```C++
HRESULT SynchronousBlockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="6ceba-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ceba-106">Parameters</span></span>

<span data-ttu-id="6ceba-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6ceba-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ceba-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6ceba-108">Return value</span></span>

<span data-ttu-id="6ceba-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6ceba-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6ceba-110">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6ceba-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="6ceba-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6ceba-111">Return code</span></span>                                                                                                                    | <span data-ttu-id="6ceba-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6ceba-112">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="6ceba-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6ceba-113"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="6ceba-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="6ceba-114">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="6ceba-115"><dt>**VFW \_ E \_ PIN \_ já \_ bloqueados**</dt></span><span class="sxs-lookup"><span data-stu-id="6ceba-115"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="6ceba-116">O PIN já está bloqueado em outro thread.</span><span class="sxs-lookup"><span data-stu-id="6ceba-116">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="6ceba-117"><dt>**VFW \_ E \_ PIN \_ já \_ bloqueados neste \_ \_ \_ thread**</dt></span><span class="sxs-lookup"><span data-stu-id="6ceba-117"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="6ceba-118">O PIN já está bloqueado no thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="6ceba-118">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6ceba-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ceba-119">Remarks</span></span>

<span data-ttu-id="6ceba-120">Não chame esse método do thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="6ceba-120">Do not call this method from the streaming thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ceba-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ceba-121">Requirements</span></span>



| <span data-ttu-id="6ceba-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ceba-122">Requirement</span></span> | <span data-ttu-id="6ceba-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6ceba-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ceba-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6ceba-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6ceba-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ceba-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6ceba-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ceba-126">Library</span></span><br/> | <dl> <span data-ttu-id="6ceba-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6ceba-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ceba-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ceba-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ceba-129">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="6ceba-129">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




