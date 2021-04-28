---
description: Método CBaseOutputPin. Inactive-o método inativo notifica o PIN de que o filtro não está mais ativo.
ms.assetid: 14a020de-2102-4d49-8a34-d59abe6698d1
title: Método CBaseOutputPin. Inactive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc4901bba7f1e34d49ff5bafb7b291544157bd9c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096134"
---
# <a name="cbaseoutputpininactive-method"></a><span data-ttu-id="a1293-103">Método CBaseOutputPin. Inactive</span><span class="sxs-lookup"><span data-stu-id="a1293-103">CBaseOutputPin.Inactive method</span></span>

<span data-ttu-id="a1293-104">O `Inactive` método notifica o PIN de que o filtro não está mais ativo.</span><span class="sxs-lookup"><span data-stu-id="a1293-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1293-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1293-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="a1293-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1293-106">Parameters</span></span>

<span data-ttu-id="a1293-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="a1293-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a1293-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a1293-108">Return value</span></span>

<span data-ttu-id="a1293-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a1293-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a1293-110">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a1293-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="a1293-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a1293-111">Return code</span></span>                                                                                          | <span data-ttu-id="a1293-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1293-112">Description</span></span>                                  |
|------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="a1293-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a1293-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="a1293-114">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="a1293-114">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="a1293-115"><dt>**VFW \_ E \_ nenhum \_ alocador**</dt></span><span class="sxs-lookup"><span data-stu-id="a1293-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="a1293-116">Não há alocador de memória disponível.</span><span class="sxs-lookup"><span data-stu-id="a1293-116">No memory allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a1293-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1293-117">Remarks</span></span>

<span data-ttu-id="a1293-118">Esse método substitui o método [**CBasePin:: Inactive**](cbasepin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="a1293-118">This method overrides the [**CBasePin::Inactive**](cbasepin-inactive.md) method.</span></span> <span data-ttu-id="a1293-119">Ele chama o método [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) para desconfirmar o alocador de memória.</span><span class="sxs-lookup"><span data-stu-id="a1293-119">It calls the [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit) method to decommit the memory allocator.</span></span>

<span data-ttu-id="a1293-120">Se você substituir esse método, chame o método de classe base do seu método de substituição.</span><span class="sxs-lookup"><span data-stu-id="a1293-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1293-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1293-121">Requirements</span></span>



| <span data-ttu-id="a1293-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1293-122">Requirement</span></span> | <span data-ttu-id="a1293-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a1293-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1293-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a1293-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a1293-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1293-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a1293-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1293-126">Library</span></span><br/> | <dl> <span data-ttu-id="a1293-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a1293-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1293-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a1293-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1293-129">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="a1293-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




