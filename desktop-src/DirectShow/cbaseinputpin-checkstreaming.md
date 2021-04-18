---
description: Determina se o PIN pode aceitar amostras.
ms.assetid: bc66ab4c-99de-4031-bdac-b1430f736e20
title: Método CBaseInputPin. CheckStreaming (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba07d28ac93f7dc511390a851d3c737a833ef3f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751274"
---
# <a name="cbaseinputpincheckstreaming-method"></a><span data-ttu-id="3a1d7-103">Método CBaseInputPin. CheckStreaming</span><span class="sxs-lookup"><span data-stu-id="3a1d7-103">CBaseInputPin.CheckStreaming method</span></span>

<span data-ttu-id="3a1d7-104">Determina se o PIN pode aceitar amostras.</span><span class="sxs-lookup"><span data-stu-id="3a1d7-104">Determines whether the pin can accept samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a1d7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a1d7-105">Syntax</span></span>


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a><span data-ttu-id="3a1d7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a1d7-106">Parameters</span></span>

<span data-ttu-id="3a1d7-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3a1d7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a1d7-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a1d7-108">Return value</span></span>

<span data-ttu-id="3a1d7-109">Retorna um dos valores **HRESULT** listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3a1d7-109">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="3a1d7-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3a1d7-110">Return code</span></span>                                                                                           | <span data-ttu-id="3a1d7-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="3a1d7-111">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="3a1d7-112"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3a1d7-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="3a1d7-113">Êxito.</span><span class="sxs-lookup"><span data-stu-id="3a1d7-113">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="3a1d7-114"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="3a1d7-114"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="3a1d7-115">O PIN está sendo liberado no momento.</span><span class="sxs-lookup"><span data-stu-id="3a1d7-115">Pin is currently flushing.</span></span><br/> |
| <dl> <span data-ttu-id="3a1d7-116"><dt>**VFW \_ E \_ erro de tempo de execução \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3a1d7-116"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="3a1d7-117">Ocorreu um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="3a1d7-117">A run-time error occurred.</span></span><br/> |
| <dl> <span data-ttu-id="3a1d7-118"><dt>**VFW \_ E \_ estado incorreto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3a1d7-118"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="3a1d7-119">O PIN foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="3a1d7-119">The pin is stopped.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="3a1d7-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="3a1d7-120">Remarks</span></span>

<span data-ttu-id="3a1d7-121">A classe derivada pode substituir esse método para executar verificações adicionais.</span><span class="sxs-lookup"><span data-stu-id="3a1d7-121">The derived class can override this method to perform further checks.</span></span> <span data-ttu-id="3a1d7-122">No método de substituição, também chame a implementação da classe base.</span><span class="sxs-lookup"><span data-stu-id="3a1d7-122">In the overriding method, also call the base class implementation.</span></span>

<span data-ttu-id="3a1d7-123">O método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="3a1d7-123">The [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method calls this method.</span></span> <span data-ttu-id="3a1d7-124">Você deve substituir o método [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) para chamar esse método também.</span><span class="sxs-lookup"><span data-stu-id="3a1d7-124">You should override the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method to call this method as well.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a1d7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a1d7-125">Requirements</span></span>



| <span data-ttu-id="3a1d7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a1d7-126">Requirement</span></span> | <span data-ttu-id="3a1d7-127">Valor</span><span class="sxs-lookup"><span data-stu-id="3a1d7-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a1d7-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a1d7-128">Header</span></span><br/>  | <dl> <span data-ttu-id="3a1d7-129"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a1d7-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3a1d7-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a1d7-130">Library</span></span><br/> | <dl> <span data-ttu-id="3a1d7-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3a1d7-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a1d7-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a1d7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a1d7-133">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="3a1d7-133">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




