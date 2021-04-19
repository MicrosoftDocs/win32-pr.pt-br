---
description: O método StreamingThreadUsingOutputPin determina se algum thread está executando uma operação de streaming no PIN.
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: Método CDynamicOutputPin. StreamingThreadUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 797dcb94e227861642de2a05e6edf24f675bb4e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769221"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a><span data-ttu-id="44b18-103">Método CDynamicOutputPin. StreamingThreadUsingOutputPin</span><span class="sxs-lookup"><span data-stu-id="44b18-103">CDynamicOutputPin.StreamingThreadUsingOutputPin method</span></span>

<span data-ttu-id="44b18-104">O método StreamingThreadUsingOutputPin determina se algum thread está executando uma operação de streaming no PIN.</span><span class="sxs-lookup"><span data-stu-id="44b18-104">The StreamingThreadUsingOutputPin method determines whether any thread is performing a streaming operation on the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="44b18-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44b18-105">Syntax</span></span>


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="44b18-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44b18-106">Parameters</span></span>

<span data-ttu-id="44b18-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="44b18-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44b18-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44b18-108">Return value</span></span>

<span data-ttu-id="44b18-109">Retornará **true** se um thread estiver executando uma operação de streaming no PIN.</span><span class="sxs-lookup"><span data-stu-id="44b18-109">Returns **TRUE** if a thread is performing a streaming operation on the pin.</span></span> <span data-ttu-id="44b18-110">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="44b18-110">Otherwise, returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="44b18-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="44b18-111">Remarks</span></span>

<span data-ttu-id="44b18-112">Se algum thread retornar com êxito do método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) e não tiver feito uma chamada correspondente para o método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , esse método retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="44b18-112">If any threads have successfully returned from the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method and have not made a corresponding call to the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method, this method returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="44b18-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44b18-113">Requirements</span></span>



| <span data-ttu-id="44b18-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="44b18-114">Requirement</span></span> | <span data-ttu-id="44b18-115">Valor</span><span class="sxs-lookup"><span data-stu-id="44b18-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44b18-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44b18-116">Header</span></span><br/>  | <dl> <span data-ttu-id="44b18-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="44b18-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="44b18-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="44b18-118">Library</span></span><br/> | <dl> <span data-ttu-id="44b18-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="44b18-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44b18-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="44b18-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44b18-121">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="44b18-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




