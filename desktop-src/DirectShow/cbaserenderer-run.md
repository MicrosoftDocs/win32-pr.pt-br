---
description: O método Run executa o filtro.
ms.assetid: 83251137-83f8-45a3-b3f2-d7b45f43f7f8
title: Método CBaseRenderer. Run (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc298cbe3f2a0b8063caaa3bdb69fd0d8a88f556
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754994"
---
# <a name="cbaserendererrun-method"></a><span data-ttu-id="59138-103">Método CBaseRenderer. Run</span><span class="sxs-lookup"><span data-stu-id="59138-103">CBaseRenderer.Run method</span></span>

<span data-ttu-id="59138-104">O `Run` método executa o filtro.</span><span class="sxs-lookup"><span data-stu-id="59138-104">The `Run` method runs the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="59138-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59138-105">Syntax</span></span>


```C++
HRESULT Run();
```



## <a name="parameters"></a><span data-ttu-id="59138-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59138-106">Parameters</span></span>

<span data-ttu-id="59138-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="59138-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59138-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59138-108">Return value</span></span>

<span data-ttu-id="59138-109">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="59138-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="59138-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="59138-110">Remarks</span></span>

<span data-ttu-id="59138-111">Esse método substitui o método [**CBaseFilter:: Run**](cbasefilter-run.md) .</span><span class="sxs-lookup"><span data-stu-id="59138-111">This method overrides the [**CBaseFilter::Run**](cbasefilter-run.md) method.</span></span> <span data-ttu-id="59138-112">Ele executa as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="59138-112">It performs the following actions:</span></span>

-   <span data-ttu-id="59138-113">Chama o método **CBaseFilter:: Run** .</span><span class="sxs-lookup"><span data-stu-id="59138-113">Calls the **CBaseFilter::Run** method.</span></span>
-   <span data-ttu-id="59138-114">Confirma o alocador.</span><span class="sxs-lookup"><span data-stu-id="59138-114">Commits the allocator.</span></span> <span data-ttu-id="59138-115">(Consulte [**IMemAllocator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span><span class="sxs-lookup"><span data-stu-id="59138-115">(See [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span></span>
-   <span data-ttu-id="59138-116">Se o estado anterior foi interrompido, o filtro libera qualquer amostra que está segurando.</span><span class="sxs-lookup"><span data-stu-id="59138-116">If the previous state was stopped, the filter releases any sample it is holding.</span></span> <span data-ttu-id="59138-117">(O exemplo não é mais válido.)</span><span class="sxs-lookup"><span data-stu-id="59138-117">(The sample is no longer valid.)</span></span>
-   <span data-ttu-id="59138-118">Chama o método [**CBaseRenderer:: StartStreaming**](cbaserenderer-startstreaming.md) e retorna o resultado.</span><span class="sxs-lookup"><span data-stu-id="59138-118">Calls the [**CBaseRenderer::StartStreaming**](cbaserenderer-startstreaming.md) method and returns the result.</span></span> <span data-ttu-id="59138-119">Se um exemplo estiver pendente, o método **StartStreaming** o agendará para renderização.</span><span class="sxs-lookup"><span data-stu-id="59138-119">If a sample is pending, the **StartStreaming** method schedules it for rendering.</span></span>

<span data-ttu-id="59138-120">Se o filtro não estiver conectado, ele lançará um evento de [**\_ conclusão do EC**](ec-complete.md) imediatamente.</span><span class="sxs-lookup"><span data-stu-id="59138-120">If the filter is not connected, it posts an [**EC\_COMPLETE**](ec-complete.md) event immediately.</span></span>

## <a name="requirements"></a><span data-ttu-id="59138-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59138-121">Requirements</span></span>



| <span data-ttu-id="59138-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="59138-122">Requirement</span></span> | <span data-ttu-id="59138-123">Valor</span><span class="sxs-lookup"><span data-stu-id="59138-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59138-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59138-124">Header</span></span><br/>  | <dl> <span data-ttu-id="59138-125"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59138-125"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="59138-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59138-126">Library</span></span><br/> | <dl> <span data-ttu-id="59138-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="59138-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59138-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="59138-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59138-129">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="59138-129">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




