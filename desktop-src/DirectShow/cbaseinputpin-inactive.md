---
description: O método inativo notifica o PIN de que o filtro não está mais ativo.
ms.assetid: e00e1562-54bb-4968-8a86-b29e1077d7a5
title: Método CBaseInputPin. Inactive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 52bf7efa352e8a73d562c61c3833a051ee860d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748648"
---
# <a name="cbaseinputpininactive-method"></a><span data-ttu-id="3545d-103">Método CBaseInputPin. Inactive</span><span class="sxs-lookup"><span data-stu-id="3545d-103">CBaseInputPin.Inactive method</span></span>

<span data-ttu-id="3545d-104">O `Inactive` método notifica o PIN de que o filtro não está mais ativo.</span><span class="sxs-lookup"><span data-stu-id="3545d-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="3545d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3545d-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="3545d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3545d-106">Parameters</span></span>

<span data-ttu-id="3545d-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3545d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3545d-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3545d-108">Return value</span></span>

<span data-ttu-id="3545d-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3545d-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="3545d-110">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="3545d-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="3545d-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="3545d-111">Return code</span></span>                                                                                          | <span data-ttu-id="3545d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="3545d-112">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3545d-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3545d-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="3545d-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="3545d-114">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="3545d-115"><dt>**VFW \_ E \_ nenhum \_ alocador**</dt></span><span class="sxs-lookup"><span data-stu-id="3545d-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="3545d-116">Não há alocador de memória disponível.</span><span class="sxs-lookup"><span data-stu-id="3545d-116">No memory allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3545d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3545d-117">Remarks</span></span>

<span data-ttu-id="3545d-118">Esse método substitui o método [**CBasePin:: Inactive**](cbasepin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="3545d-118">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="3545d-119">Ele chama o método [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) para desconfirmar o alocador de memória.</span><span class="sxs-lookup"><span data-stu-id="3545d-119">It calls the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method to decommit the memory allocator.</span></span>

<span data-ttu-id="3545d-120">Se você substituir esse método, chame o método de classe base do seu método de substituição.</span><span class="sxs-lookup"><span data-stu-id="3545d-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3545d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3545d-121">Requirements</span></span>



| <span data-ttu-id="3545d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3545d-122">Requirement</span></span> | <span data-ttu-id="3545d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="3545d-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3545d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3545d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3545d-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3545d-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3545d-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3545d-126">Library</span></span><br/> | <dl> <span data-ttu-id="3545d-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3545d-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3545d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3545d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3545d-129">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="3545d-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




