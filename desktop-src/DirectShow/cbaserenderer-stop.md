---
description: O método Stop interrompe o filtro.
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: Método CBaseRenderer. Stop (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ddd8194bbf76c4a4311aa90335f94d1e7548a356
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748214"
---
# <a name="cbaserendererstop-method"></a><span data-ttu-id="11e74-103">Método CBaseRenderer. Stop</span><span class="sxs-lookup"><span data-stu-id="11e74-103">CBaseRenderer.Stop method</span></span>

<span data-ttu-id="11e74-104">O `Stop` método para o filtro.</span><span class="sxs-lookup"><span data-stu-id="11e74-104">The `Stop` method stops the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="11e74-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11e74-105">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="11e74-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11e74-106">Parameters</span></span>

<span data-ttu-id="11e74-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="11e74-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="11e74-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11e74-108">Return value</span></span>

<span data-ttu-id="11e74-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="11e74-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="11e74-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="11e74-110">Remarks</span></span>

<span data-ttu-id="11e74-111">Esse método substitui o método [**CBaseFilter:: Stop**](cbasefilter-stop.md) .</span><span class="sxs-lookup"><span data-stu-id="11e74-111">This method overrides the [**CBaseFilter::Stop**](cbasefilter-stop.md) method.</span></span> <span data-ttu-id="11e74-112">Ele executa as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="11e74-112">It performs the following actions:</span></span>

-   <span data-ttu-id="11e74-113">Chama [**CBaseFilter:: Stop**](cbasefilter-stop.md).</span><span class="sxs-lookup"><span data-stu-id="11e74-113">Calls [**CBaseFilter::Stop**](cbasefilter-stop.md).</span></span>
-   <span data-ttu-id="11e74-114">O desconfirma o alocador.</span><span class="sxs-lookup"><span data-stu-id="11e74-114">Decommits the allocator.</span></span> <span data-ttu-id="11e74-115">(Consulte [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)</span><span class="sxs-lookup"><span data-stu-id="11e74-115">(See [**IMemAllocator::Decommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)</span></span>
-   <span data-ttu-id="11e74-116">Cancela qualquer renderização agendada e libera o thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="11e74-116">Cancels any scheduled rendering and releases the streaming thread.</span></span>
-   <span data-ttu-id="11e74-117">Aguarda a conclusão de qualquer chamada de **recebimento** pendente.</span><span class="sxs-lookup"><span data-stu-id="11e74-117">Waits for any pending **Receive** call to complete.</span></span>

## <a name="requirements"></a><span data-ttu-id="11e74-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11e74-118">Requirements</span></span>



| <span data-ttu-id="11e74-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="11e74-119">Requirement</span></span> | <span data-ttu-id="11e74-120">Valor</span><span class="sxs-lookup"><span data-stu-id="11e74-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11e74-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11e74-121">Header</span></span><br/>  | <dl> <span data-ttu-id="11e74-122"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11e74-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="11e74-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11e74-123">Library</span></span><br/> | <dl> <span data-ttu-id="11e74-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="11e74-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11e74-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="11e74-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e74-126">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="11e74-126">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




