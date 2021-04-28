---
description: Construtor de CDynamicOutputPin. CDynamicOutputPin-método de construtor.
ms.assetid: 996adc69-8727-431e-a7f5-8fbcc0e305ae
title: Construtor CDynamicOutputPin. CDynamicOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fe6dad14399b5b124b0146ea8b7ca101c8fa817
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099304"
---
# <a name="cdynamicoutputpincdynamicoutputpin-constructor"></a><span data-ttu-id="98dee-103">Construtor CDynamicOutputPin. CDynamicOutputPin</span><span class="sxs-lookup"><span data-stu-id="98dee-103">CDynamicOutputPin.CDynamicOutputPin constructor</span></span>

<span data-ttu-id="98dee-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="98dee-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="98dee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98dee-105">Syntax</span></span>


```C++
CDynamicOutputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="98dee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="98dee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98dee-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="98dee-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="98dee-108">Ponteiro para uma cadeia de caracteres que contém o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="98dee-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="98dee-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="98dee-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="98dee-110">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="98dee-110">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="98dee-111">Ponteiro para o filtro que criou este pin.</span><span class="sxs-lookup"><span data-stu-id="98dee-111">Pointer to the filter that created this pin.</span></span>

</dd> <dt>

<span data-ttu-id="98dee-112">*pLock*</span><span class="sxs-lookup"><span data-stu-id="98dee-112">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="98dee-113">Ponteiro para um bloqueio de [**CCritSec**](ccritsec.md) , usado para serializar alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="98dee-113">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span> <span data-ttu-id="98dee-114">Use a mesma seção crítica que o bloqueio de filtro, [ **CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md)</span><span class="sxs-lookup"><span data-stu-id="98dee-114">Use the same critical section as the filter lock, [**CBaseFilter::m\_pLock**](cbasefilter-m-plock.md)</span></span>

</dd> <dt>

<span data-ttu-id="98dee-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="98dee-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="98dee-116">Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método.</span><span class="sxs-lookup"><span data-stu-id="98dee-116">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="98dee-117">Inicialize o valor para S \_ OK antes de criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="98dee-117">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="98dee-118">O valor será alterado somente se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="98dee-118">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="98dee-119">*pName*</span><span class="sxs-lookup"><span data-stu-id="98dee-119">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="98dee-120">Ponteiro para uma cadeia de caracteres largos contendo o identificador de PIN.</span><span class="sxs-lookup"><span data-stu-id="98dee-120">Pointer to a wide-character string containing the pin identifier.</span></span> <span data-ttu-id="98dee-121">Para obter mais informações, consulte [**IPin:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span><span class="sxs-lookup"><span data-stu-id="98dee-121">For more information, see [**IPin::QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98dee-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98dee-122">Requirements</span></span>



| <span data-ttu-id="98dee-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="98dee-123">Requirement</span></span> | <span data-ttu-id="98dee-124">Valor</span><span class="sxs-lookup"><span data-stu-id="98dee-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98dee-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98dee-125">Header</span></span><br/>  | <dl> <span data-ttu-id="98dee-126"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98dee-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="98dee-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98dee-127">Library</span></span><br/> | <dl> <span data-ttu-id="98dee-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="98dee-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98dee-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="98dee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98dee-130">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="98dee-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




