---
description: 'Método CTransformInputPin. EndFlush – o método EndFlush termina uma operação de liberação. Esse método implementa o método IPin:: EndFlush.'
ms.assetid: ebc70df3-e99d-4292-990b-99b79ff06461
title: Método CTransformInputPin. EndFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5e080b4531d05160bebd42a68145842c4783bea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095054"
---
# <a name="ctransforminputpinendflush-method"></a><span data-ttu-id="7eb76-104">Método CTransformInputPin. EndFlush</span><span class="sxs-lookup"><span data-stu-id="7eb76-104">CTransformInputPin.EndFlush method</span></span>

<span data-ttu-id="7eb76-105">O `EndFlush` método encerra uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="7eb76-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="7eb76-106">Esse método implementa o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="7eb76-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7eb76-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7eb76-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="7eb76-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7eb76-108">Parameters</span></span>

<span data-ttu-id="7eb76-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7eb76-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7eb76-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7eb76-110">Return value</span></span>

<span data-ttu-id="7eb76-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7eb76-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7eb76-112">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7eb76-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="7eb76-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7eb76-113">Return code</span></span>                                                                                           | <span data-ttu-id="7eb76-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="7eb76-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="7eb76-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7eb76-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="7eb76-116">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="7eb76-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="7eb76-117"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="7eb76-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="7eb76-118">O pino de saída não está conectado.</span><span class="sxs-lookup"><span data-stu-id="7eb76-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7eb76-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7eb76-119">Remarks</span></span>

<span data-ttu-id="7eb76-120">Esse método chama o método [**CTransformFilter:: EndFlush**](ctransformfilter-endflush.md) do filtro para entregar a chamada downstream.</span><span class="sxs-lookup"><span data-stu-id="7eb76-120">This method calls the filter's [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method to deliver the call downstream.</span></span> <span data-ttu-id="7eb76-121">Em seguida, ele chama o método [**CBaseInputPin:: EndFlush**](cbaseinputpin-endflush.md) do PIN.</span><span class="sxs-lookup"><span data-stu-id="7eb76-121">Then it calls the pin's [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eb76-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eb76-122">Requirements</span></span>



| <span data-ttu-id="7eb76-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7eb76-123">Requirement</span></span> | <span data-ttu-id="7eb76-124">Valor</span><span class="sxs-lookup"><span data-stu-id="7eb76-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eb76-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7eb76-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7eb76-126"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7eb76-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7eb76-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7eb76-127">Library</span></span><br/> | <dl> <span data-ttu-id="7eb76-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7eb76-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




