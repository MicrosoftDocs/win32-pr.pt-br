---
description: 'Método CTransformInputPin. EndOfStream – o método EndOfStream notifica o PIN de que nenhum dado adicional é esperado. Esse método implementa o método IPin:: EndOfStream.'
ms.assetid: db9896eb-3db2-4d58-a787-4d80ce8f0d0e
title: Método CTransformInputPin. EndOfStream (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2035d0261447826098162f480ddc959544b101b7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084974"
---
# <a name="ctransforminputpinendofstream-method"></a><span data-ttu-id="a31e5-104">Método CTransformInputPin. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="a31e5-104">CTransformInputPin.EndOfStream method</span></span>

<span data-ttu-id="a31e5-105">O `EndOfStream` método notifica o PIN de que nenhum dado adicional é esperado.</span><span class="sxs-lookup"><span data-stu-id="a31e5-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="a31e5-106">Esse método implementa o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="a31e5-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a31e5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a31e5-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="a31e5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a31e5-108">Parameters</span></span>

<span data-ttu-id="a31e5-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a31e5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a31e5-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a31e5-110">Return value</span></span>

<span data-ttu-id="a31e5-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a31e5-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a31e5-112">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a31e5-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="a31e5-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a31e5-113">Return code</span></span>                                                                                           | <span data-ttu-id="a31e5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a31e5-114">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="a31e5-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a31e5-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="a31e5-116">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="a31e5-116">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="a31e5-117"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="a31e5-117"><dt>**S\_FALSE**</dt></span></span> </dl>               | <span data-ttu-id="a31e5-118">O PIN está sendo liberado no momento.</span><span class="sxs-lookup"><span data-stu-id="a31e5-118">Pin is currently flushing.</span></span><br/>       |
| <dl> <span data-ttu-id="a31e5-119"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="a31e5-119"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a31e5-120">O pino de saída não está conectado.</span><span class="sxs-lookup"><span data-stu-id="a31e5-120">The output pin is not connected.</span></span><br/> |
| <dl> <span data-ttu-id="a31e5-121"><dt>**VFW \_ E \_ erro de tempo de execução \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a31e5-121"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="a31e5-122">Ocorreu um erro em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a31e5-122">A run-time error occurred.</span></span><br/>       |
| <dl> <span data-ttu-id="a31e5-123"><dt>**VFW \_ E \_ estado incorreto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a31e5-123"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>   | <span data-ttu-id="a31e5-124">O PIN foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="a31e5-124">The pin is stopped.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="a31e5-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a31e5-125">Remarks</span></span>

<span data-ttu-id="a31e5-126">Esse método chama o método [**CTransformFilter:: EndOfStream**](ctransformfilter-endofstream.md) do filtro para entregar o downstream de notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a31e5-126">This method calls the filter's [**CTransformFilter::EndOfStream**](ctransformfilter-endofstream.md) method to deliver the end-of-stream notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="a31e5-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a31e5-127">Requirements</span></span>



| <span data-ttu-id="a31e5-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a31e5-128">Requirement</span></span> | <span data-ttu-id="a31e5-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a31e5-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a31e5-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a31e5-130">Header</span></span><br/>  | <dl> <span data-ttu-id="a31e5-131"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a31e5-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a31e5-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a31e5-132">Library</span></span><br/> | <dl> <span data-ttu-id="a31e5-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a31e5-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




