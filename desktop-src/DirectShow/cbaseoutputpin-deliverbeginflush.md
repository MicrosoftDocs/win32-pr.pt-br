---
description: O método DeliverBeginFlush solicita o pino de entrada conectado para iniciar uma operação de liberação.
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: Método CBaseOutputPin. DeliverBeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dad764ceaa6cc57c8c5b7ee288859926b6c63f02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749032"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a><span data-ttu-id="14042-103">Método CBaseOutputPin. DeliverBeginFlush</span><span class="sxs-lookup"><span data-stu-id="14042-103">CBaseOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="14042-104">O `DeliverBeginFlush` método solicita o PIN de entrada conectado para iniciar uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="14042-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="14042-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="14042-105">Syntax</span></span>


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="14042-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14042-106">Parameters</span></span>

<span data-ttu-id="14042-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="14042-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="14042-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14042-108">Return value</span></span>

<span data-ttu-id="14042-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="14042-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="14042-110">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="14042-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="14042-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="14042-111">Return code</span></span>                                                                                           | <span data-ttu-id="14042-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="14042-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="14042-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="14042-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="14042-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="14042-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="14042-115"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="14042-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="14042-116">O PIN não está conectado.</span><span class="sxs-lookup"><span data-stu-id="14042-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="14042-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="14042-117">Remarks</span></span>

<span data-ttu-id="14042-118">Esse método chama o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="14042-118">This method calls the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="14042-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14042-119">Requirements</span></span>



| <span data-ttu-id="14042-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="14042-120">Requirement</span></span> | <span data-ttu-id="14042-121">Valor</span><span class="sxs-lookup"><span data-stu-id="14042-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14042-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14042-122">Header</span></span><br/>  | <dl> <span data-ttu-id="14042-123"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14042-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="14042-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="14042-124">Library</span></span><br/> | <dl> <span data-ttu-id="14042-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="14042-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14042-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="14042-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14042-127">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="14042-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




