---
description: O método AddPin adiciona um novo pino de saída ao filtro.
ms.assetid: 48850a1f-ecb7-460c-9bfc-ce1d1103a00b
title: Método CSource. AddPin (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.AddPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 224550756f5935ce26c106ba01c9ef64f0767140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754528"
---
# <a name="csourceaddpin-method"></a><span data-ttu-id="51fa1-103">Método CSource. AddPin</span><span class="sxs-lookup"><span data-stu-id="51fa1-103">CSource.AddPin method</span></span>

<span data-ttu-id="51fa1-104">O `AddPin` método adiciona um novo pino de saída ao filtro.</span><span class="sxs-lookup"><span data-stu-id="51fa1-104">The `AddPin` method adds a new output pin to the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="51fa1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51fa1-105">Syntax</span></span>


```C++
HRESULT AddPin(
   CSourceStream *pStream
);
```



## <a name="parameters"></a><span data-ttu-id="51fa1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51fa1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51fa1-107">*pStream*</span><span class="sxs-lookup"><span data-stu-id="51fa1-107">*pStream*</span></span> 
</dt> <dd>

<span data-ttu-id="51fa1-108">Ponteiro para o objeto [**CSourceStream**](csourcestream.md) que implementa o PIN.</span><span class="sxs-lookup"><span data-stu-id="51fa1-108">Pointer to the [**CSourceStream**](csourcestream.md) object that implements the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51fa1-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="51fa1-109">Return value</span></span>

<span data-ttu-id="51fa1-110">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="51fa1-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="51fa1-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="51fa1-111">Return code</span></span>                                                                                   | <span data-ttu-id="51fa1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="51fa1-112">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="51fa1-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="51fa1-113"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="51fa1-114">Êxito</span><span class="sxs-lookup"><span data-stu-id="51fa1-114">Success</span></span><br/>             |
| <dl> <span data-ttu-id="51fa1-115"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="51fa1-115"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="51fa1-116">Memória insuficiente</span><span class="sxs-lookup"><span data-stu-id="51fa1-116">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="51fa1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="51fa1-117">Remarks</span></span>

<span data-ttu-id="51fa1-118">Quando você cria um novo PIN derivado de **CSourceStream**, o construtor **CSourceStream** chama esse método automaticamente para adicionar o pino de saída ao filtro.</span><span class="sxs-lookup"><span data-stu-id="51fa1-118">When you create a new pin derived from **CSourceStream**, the **CSourceStream** constructor automatically calls this method, to add the output pin to the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="51fa1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51fa1-119">Requirements</span></span>



| <span data-ttu-id="51fa1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="51fa1-120">Requirement</span></span> | <span data-ttu-id="51fa1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="51fa1-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fa1-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51fa1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="51fa1-123"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51fa1-123"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="51fa1-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="51fa1-124">Library</span></span><br/> | <dl> <span data-ttu-id="51fa1-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="51fa1-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51fa1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="51fa1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51fa1-127">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="51fa1-127">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




