---
description: 'Método CBaseOutputPin. EndOfStream – o método EndOfStream notifica o PIN de que nenhum dado adicional é esperado. Esse método implementa o método IPin:: EndOfStream.'
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
ms.openlocfilehash: c5f293b8026456618ad1196c491bce58cf481f07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096144"
---
# <a name="cbaseoutputpinendofstream-method"></a><span data-ttu-id="c3a40-104">Método CBaseOutputPin. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="c3a40-104">CBaseOutputPin.EndOfStream method</span></span>

<span data-ttu-id="c3a40-105">O `EndOfStream` método notifica o PIN de que nenhum dado adicional é esperado.</span><span class="sxs-lookup"><span data-stu-id="c3a40-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="c3a40-106">Esse método implementa o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="c3a40-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a40-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3a40-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="c3a40-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3a40-108">Parameters</span></span>

<span data-ttu-id="c3a40-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c3a40-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3a40-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c3a40-110">Return value</span></span>

<span data-ttu-id="c3a40-111">Retorna E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="c3a40-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3a40-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3a40-112">Remarks</span></span>

<span data-ttu-id="c3a40-113">Esse método só deve ser chamado em Pins de entrada, portanto a implementação de **CBaseOutputPin** retorna E \_ inesperada.</span><span class="sxs-lookup"><span data-stu-id="c3a40-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3a40-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3a40-114">Requirements</span></span>



| <span data-ttu-id="c3a40-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3a40-115">Requirement</span></span> | <span data-ttu-id="c3a40-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c3a40-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a40-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3a40-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c3a40-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3a40-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c3a40-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3a40-119">Library</span></span><br/> | <dl> <span data-ttu-id="c3a40-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c3a40-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3a40-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c3a40-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3a40-122">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="c3a40-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




