---
description: Método CBaseOutputPin. DeliverEndFlush – o método DeliverEndFlush solicita o pino de entrada conectado para finalizar uma operação de liberação.
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
ms.openlocfilehash: 5f3fd5c1bc686ee5c0b4ff0cd1285a5114b93049
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096174"
---
# <a name="cbaseoutputpindeliverendflush-method"></a><span data-ttu-id="b4571-103">Método CBaseOutputPin. DeliverEndFlush</span><span class="sxs-lookup"><span data-stu-id="b4571-103">CBaseOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="b4571-104">O `DeliverEndFlush` método solicita o PIN de entrada conectado para finalizar uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="b4571-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4571-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4571-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="b4571-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4571-106">Parameters</span></span>

<span data-ttu-id="b4571-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b4571-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b4571-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b4571-108">Return value</span></span>

<span data-ttu-id="b4571-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b4571-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="b4571-110">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b4571-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="b4571-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b4571-111">Return code</span></span>                                                                                           | <span data-ttu-id="b4571-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4571-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b4571-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b4571-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="b4571-114">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="b4571-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="b4571-115"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="b4571-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b4571-116">O PIN não está conectado.</span><span class="sxs-lookup"><span data-stu-id="b4571-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4571-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4571-117">Remarks</span></span>

<span data-ttu-id="b4571-118">Esse método chama o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="b4571-118">This method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4571-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4571-119">Requirements</span></span>



| <span data-ttu-id="b4571-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4571-120">Requirement</span></span> | <span data-ttu-id="b4571-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b4571-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4571-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4571-122">Header</span></span><br/>  | <dl> <span data-ttu-id="b4571-123"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4571-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b4571-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4571-124">Library</span></span><br/> | <dl> <span data-ttu-id="b4571-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b4571-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4571-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b4571-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4571-127">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="b4571-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




