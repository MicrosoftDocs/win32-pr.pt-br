---
description: Construtor de CRenderedInputPin. CRenderedInputPin-método de construtor.
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
ms.openlocfilehash: 4bd8e864531604fb36c2abe0bcd57ac5b3a9c869
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085394"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a><span data-ttu-id="01166-103">Construtor CRenderedInputPin. CRenderedInputPin</span><span class="sxs-lookup"><span data-stu-id="01166-103">CRenderedInputPin.CRenderedInputPin constructor</span></span>

<span data-ttu-id="01166-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="01166-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="01166-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01166-105">Syntax</span></span>


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="01166-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01166-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01166-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="01166-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="01166-108">Cadeia de caracteres que contém o nome de depuração do objeto.</span><span class="sxs-lookup"><span data-stu-id="01166-108">String containing the debug name of the object.</span></span> <span data-ttu-id="01166-109">Para obter mais informações, consulte [**classe CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="01166-109">For more information, see [**CBaseObject Class**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="01166-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="01166-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="01166-111">Ponteiro para o filtro que criou este pin.</span><span class="sxs-lookup"><span data-stu-id="01166-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="01166-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="01166-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="01166-113">Ponteiro para um bloqueio de [**CCritSec**](ccritsec.md) , usado para serializar alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="01166-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="01166-114">Essa pode ser a mesma seção crítica que o bloqueio de filtro, [**CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md).</span><span class="sxs-lookup"><span data-stu-id="01166-114">This can be the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md).</span></span>

</dd> <dt>

<span data-ttu-id="01166-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="01166-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="01166-116">Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="01166-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="01166-117">*pName*</span><span class="sxs-lookup"><span data-stu-id="01166-117">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="01166-118">Cadeia de caracteres largos contendo o nome do PIN (também usado como o identificador do PIN).</span><span class="sxs-lookup"><span data-stu-id="01166-118">Wide-character string containing the pin name (also used as the pin identifier).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="01166-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01166-119">Requirements</span></span>



| <span data-ttu-id="01166-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="01166-120">Requirement</span></span> | <span data-ttu-id="01166-121">Valor</span><span class="sxs-lookup"><span data-stu-id="01166-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01166-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01166-122">Header</span></span><br/>  | <dl> <span data-ttu-id="01166-123"><dt>Amextra. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01166-123"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="01166-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01166-124">Library</span></span><br/> | <dl> <span data-ttu-id="01166-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="01166-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01166-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="01166-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01166-127">**Classe CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="01166-127">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




