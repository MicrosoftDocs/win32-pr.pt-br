---
description: O método DeliverEndFlush solicita o pino de entrada conectado para finalizar uma operação de liberação.
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: Método CBaseOutputPin. DeliverEndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9b92947f2452b8755109c4b83cb21afa119461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758869"
---
# <a name="cbaseoutputpindeliverendflush-method"></a><span data-ttu-id="cf437-103">Método CBaseOutputPin. DeliverEndFlush</span><span class="sxs-lookup"><span data-stu-id="cf437-103">CBaseOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="cf437-104">O `DeliverEndFlush` método solicita o PIN de entrada conectado para finalizar uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="cf437-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf437-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf437-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="cf437-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf437-106">Parameters</span></span>

<span data-ttu-id="cf437-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cf437-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf437-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf437-108">Return value</span></span>

<span data-ttu-id="cf437-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cf437-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cf437-110">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf437-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="cf437-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cf437-111">Return code</span></span>                                                                                           | <span data-ttu-id="cf437-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf437-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cf437-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cf437-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="cf437-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="cf437-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="cf437-115"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="cf437-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="cf437-116">O PIN não está conectado.</span><span class="sxs-lookup"><span data-stu-id="cf437-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cf437-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf437-117">Remarks</span></span>

<span data-ttu-id="cf437-118">Esse método chama o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="cf437-118">This method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf437-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf437-119">Requirements</span></span>



| <span data-ttu-id="cf437-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf437-120">Requirement</span></span> | <span data-ttu-id="cf437-121">Valor</span><span class="sxs-lookup"><span data-stu-id="cf437-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf437-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cf437-122">Header</span></span><br/>  | <dl> <span data-ttu-id="cf437-123"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cf437-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cf437-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf437-124">Library</span></span><br/> | <dl> <span data-ttu-id="cf437-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cf437-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf437-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf437-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf437-127">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="cf437-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




