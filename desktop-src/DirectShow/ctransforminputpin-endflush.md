---
description: 'O método EndFlush termina uma operação de liberação. Esse método implementa o método IPin:: EndFlush.'
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
ms.openlocfilehash: f0fe6afeaa0ca3d47b278987af494221e8f50340
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750036"
---
# <a name="ctransforminputpinendflush-method"></a><span data-ttu-id="8afa5-104">Método CTransformInputPin. EndFlush</span><span class="sxs-lookup"><span data-stu-id="8afa5-104">CTransformInputPin.EndFlush method</span></span>

<span data-ttu-id="8afa5-105">O `EndFlush` método encerra uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="8afa5-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="8afa5-106">Esse método implementa o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="8afa5-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8afa5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8afa5-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="8afa5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8afa5-108">Parameters</span></span>

<span data-ttu-id="8afa5-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8afa5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8afa5-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8afa5-110">Return value</span></span>

<span data-ttu-id="8afa5-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8afa5-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8afa5-112">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="8afa5-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="8afa5-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="8afa5-113">Return code</span></span>                                                                                           | <span data-ttu-id="8afa5-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="8afa5-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="8afa5-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8afa5-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="8afa5-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="8afa5-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="8afa5-117"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="8afa5-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="8afa5-118">O pino de saída não está conectado.</span><span class="sxs-lookup"><span data-stu-id="8afa5-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8afa5-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="8afa5-119">Remarks</span></span>

<span data-ttu-id="8afa5-120">Esse método chama o método [**CTransformFilter:: EndFlush**](ctransformfilter-endflush.md) do filtro para entregar a chamada downstream.</span><span class="sxs-lookup"><span data-stu-id="8afa5-120">This method calls the filter's [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method to deliver the call downstream.</span></span> <span data-ttu-id="8afa5-121">Em seguida, ele chama o método [**CBaseInputPin:: EndFlush**](cbaseinputpin-endflush.md) do PIN.</span><span class="sxs-lookup"><span data-stu-id="8afa5-121">Then it calls the pin's [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8afa5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8afa5-122">Requirements</span></span>



| <span data-ttu-id="8afa5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8afa5-123">Requirement</span></span> | <span data-ttu-id="8afa5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8afa5-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8afa5-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8afa5-125">Header</span></span><br/>  | <dl> <span data-ttu-id="8afa5-126"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8afa5-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8afa5-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8afa5-127">Library</span></span><br/> | <dl> <span data-ttu-id="8afa5-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8afa5-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




