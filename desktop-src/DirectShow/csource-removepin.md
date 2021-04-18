---
description: O método RemovePin remove um PIN especificado do filtro. O método não exclui o PIN.
ms.assetid: 104eccfa-3fff-4f47-ba1b-3206eab9eef8
title: Método CSource. RemovePin (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.RemovePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b71ced14a6f92a3056ac4f42e55bc3858c578ff6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752889"
---
# <a name="csourceremovepin-method"></a><span data-ttu-id="2968f-104">Método CSource. RemovePin</span><span class="sxs-lookup"><span data-stu-id="2968f-104">CSource.RemovePin method</span></span>

<span data-ttu-id="2968f-105">O `RemovePin` método Remove um PIN especificado do filtro.</span><span class="sxs-lookup"><span data-stu-id="2968f-105">The `RemovePin` method removes a specified pin from the filter.</span></span> <span data-ttu-id="2968f-106">O método não exclui o PIN.</span><span class="sxs-lookup"><span data-stu-id="2968f-106">The method does not delete the pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="2968f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2968f-107">Syntax</span></span>


```C++
HRESULT RemovePin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="2968f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2968f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2968f-109">*pStream*</span><span class="sxs-lookup"><span data-stu-id="2968f-109">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="2968f-110">Ponteiro para o objeto [**CSourceStream**](csourcestream.md) que implementa o PIN.</span><span class="sxs-lookup"><span data-stu-id="2968f-110">Pointer to the [**CSourceStream**](csourcestream.md) object that implements the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2968f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2968f-111">Return value</span></span>

<span data-ttu-id="2968f-112">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2968f-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="2968f-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2968f-113">Return code</span></span>                                                                             | <span data-ttu-id="2968f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2968f-114">Description</span></span>                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="2968f-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2968f-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="2968f-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="2968f-116">Success.</span></span><br/>                              |
| <dl> <span data-ttu-id="2968f-117"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="2968f-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="2968f-118">O filtro não contém esse PIN.</span><span class="sxs-lookup"><span data-stu-id="2968f-118">The filter does not contain this pin.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2968f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2968f-119">Remarks</span></span>

<span data-ttu-id="2968f-120">O método destruidor chama esse método para remover o pino de saída do filtro.</span><span class="sxs-lookup"><span data-stu-id="2968f-120">The destructor method calls this method, to remove the output pin from the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2968f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2968f-121">Requirements</span></span>



| <span data-ttu-id="2968f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2968f-122">Requirement</span></span> | <span data-ttu-id="2968f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2968f-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2968f-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2968f-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2968f-125"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2968f-125"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2968f-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2968f-126">Library</span></span><br/> | <dl> <span data-ttu-id="2968f-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2968f-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2968f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2968f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2968f-129">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="2968f-129">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




