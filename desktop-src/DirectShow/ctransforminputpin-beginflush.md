---
description: 'O método BeginFlush inicia uma operação de liberação. Esse método implementa o método IPin:: BeginFlush.'
ms.assetid: 7c76ca06-dc3c-4f9a-9761-32aea7db4c7e
title: Método CTransformInputPin. BeginFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4d028634364ca59ae293d9ebb60a464974ccd74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749825"
---
# <a name="ctransforminputpinbeginflush-method"></a><span data-ttu-id="cc8e9-104">Método CTransformInputPin. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="cc8e9-104">CTransformInputPin.BeginFlush method</span></span>

<span data-ttu-id="cc8e9-105">O `BeginFlush` método inicia uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-105">The `BeginFlush` method begins a flush operation.</span></span> <span data-ttu-id="cc8e9-106">Esse método implementa o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="cc8e9-106">This method implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc8e9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc8e9-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="cc8e9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc8e9-108">Parameters</span></span>

<span data-ttu-id="cc8e9-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cc8e9-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc8e9-110">Return value</span></span>

<span data-ttu-id="cc8e9-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cc8e9-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="cc8e9-112">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-112">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="cc8e9-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="cc8e9-113">Return code</span></span>                                                                                           | <span data-ttu-id="cc8e9-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="cc8e9-114">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="cc8e9-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e9-115"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="cc8e9-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-116">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="cc8e9-117"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e9-117"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="cc8e9-118">O pino de saída não está conectado.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-118">Output pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cc8e9-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc8e9-119">Remarks</span></span>

<span data-ttu-id="cc8e9-120">Esse método chama o método [**CBaseInputPin:: BeginFlush**](cbaseinputpin-beginflush.md) do PIN.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-120">This method calls the pin's [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md) method.</span></span> <span data-ttu-id="cc8e9-121">Em seguida, ele chama o método [**CTransformFilter:: BeginFlush**](ctransformfilter-beginflush.md) do filtro para entregar a chamada downstream.</span><span class="sxs-lookup"><span data-stu-id="cc8e9-121">Then it calls the filter's [**CTransformFilter::BeginFlush**](ctransformfilter-beginflush.md) method to deliver the call downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc8e9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc8e9-122">Requirements</span></span>



| <span data-ttu-id="cc8e9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc8e9-123">Requirement</span></span> | <span data-ttu-id="cc8e9-124">Valor</span><span class="sxs-lookup"><span data-stu-id="cc8e9-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc8e9-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc8e9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cc8e9-126"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e9-126"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cc8e9-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc8e9-127">Library</span></span><br/> | <dl> <span data-ttu-id="cc8e9-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cc8e9-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




