---
description: Método de construtor.
ms.assetid: bf335750-b776-47bc-978d-e84e8b5259f7
title: Construtor CRenderedInputPin. CRenderedInputPin (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ee1ec8944d56d2aa6f46e59ac5034969ca77ea19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749616"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a><span data-ttu-id="09be2-103">Construtor CRenderedInputPin. CRenderedInputPin</span><span class="sxs-lookup"><span data-stu-id="09be2-103">CRenderedInputPin.CRenderedInputPin constructor</span></span>

<span data-ttu-id="09be2-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="09be2-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="09be2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09be2-105">Syntax</span></span>


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="09be2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09be2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09be2-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="09be2-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="09be2-108">Cadeia de caracteres que contém o nome de depuração do objeto.</span><span class="sxs-lookup"><span data-stu-id="09be2-108">String containing the debug name of the object.</span></span> <span data-ttu-id="09be2-109">Para obter mais informações, consulte [**classe CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="09be2-109">For more information, see [**CBaseObject Class**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="09be2-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="09be2-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="09be2-111">Ponteiro para o filtro que criou este pin.</span><span class="sxs-lookup"><span data-stu-id="09be2-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="09be2-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="09be2-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="09be2-113">Ponteiro para um bloqueio de [**CCritSec**](ccritsec.md) , usado para serializar alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="09be2-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="09be2-114">Essa pode ser a mesma seção crítica que o bloqueio de filtro, [**CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="09be2-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="09be2-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="09be2-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="09be2-116">Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="09be2-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="09be2-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="09be2-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="09be2-118">Cadeia de caracteres largos contendo o nome do PIN (também usado como o identificador do PIN).</span><span class="sxs-lookup"><span data-stu-id="09be2-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09be2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09be2-119">Requirements</span></span>



| <span data-ttu-id="09be2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="09be2-120">Requirement</span></span> | <span data-ttu-id="09be2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="09be2-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09be2-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09be2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="09be2-123"><dt>Amextra. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09be2-123"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="09be2-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09be2-124">Library</span></span><br/> | <dl> <span data-ttu-id="09be2-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="09be2-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09be2-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="09be2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09be2-127">**Classe CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="09be2-127">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




