---
description: Método CBaseOutputPin. active – o método ativo notifica o PIN de que o filtro está ativo agora.
ms.assetid: 35df4305-0e2c-4ee1-bc63-db5aec864c46
title: Método CBaseOutputPin. Active (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f282f45bb895a941c44cb70cf5d9d3d373bf8649
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096204"
---
# <a name="cbaseoutputpinactive-method"></a><span data-ttu-id="e5353-103">Método CBaseOutputPin. active</span><span class="sxs-lookup"><span data-stu-id="e5353-103">CBaseOutputPin.Active method</span></span>

<span data-ttu-id="e5353-104">O `Active` método notifica o PIN de que o filtro está ativo agora.</span><span class="sxs-lookup"><span data-stu-id="e5353-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5353-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5353-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="e5353-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5353-106">Parameters</span></span>

<span data-ttu-id="e5353-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e5353-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e5353-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e5353-108">Return value</span></span>

<span data-ttu-id="e5353-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e5353-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e5353-110">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e5353-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="e5353-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e5353-111">Return code</span></span>                                                                                          | <span data-ttu-id="e5353-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5353-112">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e5353-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e5353-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="e5353-114">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="e5353-114">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="e5353-115"><dt>**VFW \_ E \_ nenhum \_ alocador**</dt></span><span class="sxs-lookup"><span data-stu-id="e5353-115"><dt>**VFW\_E\_NO\_ALLOCATOR**</dt></span></span> </dl> | <span data-ttu-id="e5353-116">Nenhum alocador disponível.</span><span class="sxs-lookup"><span data-stu-id="e5353-116">No allocator is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e5353-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5353-117">Remarks</span></span>

<span data-ttu-id="e5353-118">Esse método substitui o método [**CBasePin:: active**](cbasepin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="e5353-118">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span> <span data-ttu-id="e5353-119">Ele chama o método [**IMemAllocator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) no alocador para alocar memória para buffers.</span><span class="sxs-lookup"><span data-stu-id="e5353-119">It calls the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method on the allocator, to allocate memory for buffers.</span></span>

<span data-ttu-id="e5353-120">Se você substituir esse método, chame o método de classe base do seu método de substituição.</span><span class="sxs-lookup"><span data-stu-id="e5353-120">If you override this method, call the base-class method from your overriding method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5353-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5353-121">Requirements</span></span>



| <span data-ttu-id="e5353-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5353-122">Requirement</span></span> | <span data-ttu-id="e5353-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e5353-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5353-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5353-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e5353-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5353-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e5353-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e5353-126">Library</span></span><br/> | <dl> <span data-ttu-id="e5353-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e5353-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5353-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e5353-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5353-129">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="e5353-129">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




