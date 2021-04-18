---
description: 'O método getalocador recupera o alocador de memória proposto por esse PIN. Esse método implementa o método IMemInputPin:: getalocator.'
ms.assetid: e9db4aa0-4f53-4ca4-babb-5e0215c7c284
title: Método CTransInPlaceInputPin. getalocador (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7798640297539a8fa8f6349c799e61e7e22a453d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780642"
---
# <a name="ctransinplaceinputpingetallocator-method"></a><span data-ttu-id="ee278-104">Método CTransInPlaceInputPin. getalocador</span><span class="sxs-lookup"><span data-stu-id="ee278-104">CTransInPlaceInputPin.GetAllocator method</span></span>

<span data-ttu-id="ee278-105">O `GetAllocator` método recupera o alocador de memória proposto por esse PIN.</span><span class="sxs-lookup"><span data-stu-id="ee278-105">The `GetAllocator` method retrieves the memory allocator proposed by this pin.</span></span> <span data-ttu-id="ee278-106">Esse método implementa o método [**IMemInputPin:: Getalocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) .</span><span class="sxs-lookup"><span data-stu-id="ee278-106">This method implements the [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee278-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee278-107">Syntax</span></span>


```C++
HRESULT GetAllocator(
   IMemAllocator **ppAllocator
);
```



## <a name="parameters"></a><span data-ttu-id="ee278-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee278-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee278-109">*ppAllocator*</span><span class="sxs-lookup"><span data-stu-id="ee278-109">*ppAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="ee278-110">Recebe um ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.</span><span class="sxs-lookup"><span data-stu-id="ee278-110">Receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee278-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee278-111">Return value</span></span>

<span data-ttu-id="ee278-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ee278-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ee278-113">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ee278-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="ee278-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ee278-114">Return code</span></span>                                                                                          | <span data-ttu-id="ee278-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee278-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ee278-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ee278-116"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="ee278-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="ee278-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="ee278-118"><dt>**VFW \_ E \_ nenhum \_ alocador**</dt></span><span class="sxs-lookup"><span data-stu-id="ee278-118"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="ee278-119">Nenhum alocador disponível.</span><span class="sxs-lookup"><span data-stu-id="ee278-119">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ee278-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee278-120">Remarks</span></span>

<span data-ttu-id="ee278-121">Se o pino de saída do filtro estiver conectado, esse método solicitará um alocador do PIN de entrada do filtro downstream.</span><span class="sxs-lookup"><span data-stu-id="ee278-121">If the filter's output pin is connected, this method requests an allocator from the downstream filter's input pin.</span></span>

<span data-ttu-id="ee278-122">Se o pino de saída do filtro não estiver conectado, esse método criará um alocador temporário.</span><span class="sxs-lookup"><span data-stu-id="ee278-122">If the filter's output pin is not connected, this method creates a temporary allocator.</span></span> <span data-ttu-id="ee278-123">Posteriormente, quando o pino de saída estiver conectado, o filtro reconectará o PIN de entrada e renegociará o alocador.</span><span class="sxs-lookup"><span data-stu-id="ee278-123">Later, when the output pin is connected, the filter will reconnect the input pin and renegotiate the allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee278-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee278-124">Requirements</span></span>



| <span data-ttu-id="ee278-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee278-125">Requirement</span></span> | <span data-ttu-id="ee278-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ee278-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee278-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee278-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ee278-128"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee278-128"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ee278-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee278-129">Library</span></span><br/> | <dl> <span data-ttu-id="ee278-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ee278-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee278-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee278-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee278-132">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="ee278-132">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




