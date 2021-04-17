---
description: 'O método EndOfStream notifica o PIN de que nenhum dado adicional é esperado. Esse método implementa o método IPin:: EndOfStream.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: Método CBaseOutputPin. EndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e1cd903e811dbcd000ba202fc86c0fcb41bf221b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755365"
---
# <a name="cbaseoutputpinendofstream-method"></a><span data-ttu-id="b831e-104">Método CBaseOutputPin. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="b831e-104">CBaseOutputPin.EndOfStream method</span></span>

<span data-ttu-id="b831e-105">O `EndOfStream` método notifica o PIN de que nenhum dado adicional é esperado.</span><span class="sxs-lookup"><span data-stu-id="b831e-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="b831e-106">Esse método implementa o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="b831e-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b831e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b831e-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="b831e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b831e-108">Parameters</span></span>

<span data-ttu-id="b831e-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b831e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b831e-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b831e-110">Return value</span></span>

<span data-ttu-id="b831e-111">Retorna E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="b831e-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="b831e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b831e-112">Remarks</span></span>

<span data-ttu-id="b831e-113">Esse método só deve ser chamado em Pins de entrada, portanto a implementação de **CBaseOutputPin** retorna E \_ inesperada.</span><span class="sxs-lookup"><span data-stu-id="b831e-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="b831e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b831e-114">Requirements</span></span>



| <span data-ttu-id="b831e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b831e-115">Requirement</span></span> | <span data-ttu-id="b831e-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b831e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b831e-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b831e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b831e-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b831e-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b831e-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b831e-119">Library</span></span><br/> | <dl> <span data-ttu-id="b831e-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b831e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b831e-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="b831e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b831e-122">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="b831e-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




