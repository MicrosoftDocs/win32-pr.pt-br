---
description: O método BlockOutputPin bloqueia o PIN.
ms.assetid: 49f6b8da-a8b2-482d-b70d-2c68a1b45a10
title: Método CDynamicOutputPin. BlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.BlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3998774550363b7d22e05ca491f1d76ba7f2ff2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749838"
---
# <a name="cdynamicoutputpinblockoutputpin-method"></a><span data-ttu-id="66f62-103">Método CDynamicOutputPin. BlockOutputPin</span><span class="sxs-lookup"><span data-stu-id="66f62-103">CDynamicOutputPin.BlockOutputPin method</span></span>

<span data-ttu-id="66f62-104">O `BlockOutputPin` método bloqueia o PIN.</span><span class="sxs-lookup"><span data-stu-id="66f62-104">The `BlockOutputPin` method blocks the pin.</span></span> <span data-ttu-id="66f62-105">Enquanto o PIN é bloqueado, o método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) aguarda que o PIN se torne desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="66f62-105">While the pin is blocked, the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method waits for the pin to become unblocked.</span></span> <span data-ttu-id="66f62-106">O estado bloqueado impede que o pino de saída entregue amostras, altere seu formato de saída ou se reconecte a si mesmo.</span><span class="sxs-lookup"><span data-stu-id="66f62-106">The blocked state prevents the output pin from delivering samples, changing its output format, or reconnecting itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f62-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66f62-107">Syntax</span></span>


```C++
void BlockOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="66f62-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66f62-108">Parameters</span></span>

<span data-ttu-id="66f62-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="66f62-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66f62-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="66f62-110">Return value</span></span>

<span data-ttu-id="66f62-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="66f62-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66f62-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="66f62-112">Remarks</span></span>

<span data-ttu-id="66f62-113">Antes de chamar esse método, mantenha a seção crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="66f62-113">Before calling this method, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span> <span data-ttu-id="66f62-114">Não chame esse método se um thread de streaming estiver usando o PIN, seja para entregar dados ou para alterar a conexão.</span><span class="sxs-lookup"><span data-stu-id="66f62-114">Do not call this method if a streaming thread is using the pin, either to deliver data or to change the connection.</span></span> <span data-ttu-id="66f62-115">Para verificar se um thread de streaming está usando o PIN, chame o método [**CDynamicOutputPin:: StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="66f62-115">To check whether a streaming thread is using the pin, call the [**CDynamicOutputPin::StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="66f62-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66f62-116">Requirements</span></span>



| <span data-ttu-id="66f62-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="66f62-117">Requirement</span></span> | <span data-ttu-id="66f62-118">Valor</span><span class="sxs-lookup"><span data-stu-id="66f62-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66f62-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66f62-119">Header</span></span><br/>  | <dl> <span data-ttu-id="66f62-120"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66f62-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="66f62-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66f62-121">Library</span></span><br/> | <dl> <span data-ttu-id="66f62-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="66f62-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66f62-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="66f62-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f62-124">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="66f62-124">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




