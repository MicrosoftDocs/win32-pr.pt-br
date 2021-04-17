---
description: Método de construtor.
ms.assetid: a853813d-cdf6-4cb4-8288-62685a883b56
title: Construtor CBaseInputPin. CBaseInputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 554c768f2cb99fda77aa87cfc916580b948da0ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749035"
---
# <a name="cbaseinputpincbaseinputpin-constructor"></a><span data-ttu-id="8da34-103">Construtor CBaseInputPin. CBaseInputPin</span><span class="sxs-lookup"><span data-stu-id="8da34-103">CBaseInputPin.CBaseInputPin constructor</span></span>

<span data-ttu-id="8da34-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="8da34-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8da34-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8da34-105">Syntax</span></span>


```C++
CBaseInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pPinName
);
```



## <a name="parameters"></a><span data-ttu-id="8da34-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8da34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8da34-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="8da34-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="8da34-108">Cadeia de caracteres que contém o nome de depuração do objeto.</span><span class="sxs-lookup"><span data-stu-id="8da34-108">String containing the debug name of the object.</span></span> <span data-ttu-id="8da34-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="8da34-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="8da34-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="8da34-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="8da34-111">Ponteiro para o filtro que criou este pin.</span><span class="sxs-lookup"><span data-stu-id="8da34-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="8da34-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="8da34-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="8da34-113">Ponteiro para um bloqueio de [**CCritSec**](ccritsec.md) , usado para serializar alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="8da34-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="8da34-114">Essa pode ser a mesma seção crítica que o bloqueio de filtro, [**CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="8da34-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="8da34-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="8da34-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="8da34-116">Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="8da34-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="8da34-117">*pPinName*</span><span class="sxs-lookup"><span data-stu-id="8da34-117">*pPinName*</span></span> 
</dt> <dd>

<span data-ttu-id="8da34-118">Cadeia de caracteres largos contendo o nome do PIN (também usado como o identificador do PIN).</span><span class="sxs-lookup"><span data-stu-id="8da34-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8da34-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="8da34-119">Remarks</span></span>

<span data-ttu-id="8da34-120">Todos os parâmetros são passados diretamente para o construtor [**CBasePin**](cbasepin-cbasepin.md) .</span><span class="sxs-lookup"><span data-stu-id="8da34-120">All of the parameters are passed directly to the [**CBasePin**](cbasepin-cbasepin.md) constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="8da34-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8da34-121">Requirements</span></span>



| <span data-ttu-id="8da34-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8da34-122">Requirement</span></span> | <span data-ttu-id="8da34-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8da34-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8da34-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8da34-124">Header</span></span><br/>  | <dl> <span data-ttu-id="8da34-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8da34-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8da34-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8da34-126">Library</span></span><br/> | <dl> <span data-ttu-id="8da34-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8da34-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8da34-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8da34-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8da34-129">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="8da34-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




