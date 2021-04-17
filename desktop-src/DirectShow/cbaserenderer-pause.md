---
description: O método pause pausa o filtro.
ms.assetid: 9dfd23d1-bf07-424b-9952-13719358d0a5
title: Método CBaseRenderer. PAUSE (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e0b422882c07808f560f5256f67d01054d097726
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769238"
---
# <a name="cbaserendererpause-method"></a><span data-ttu-id="4b57c-103">Método CBaseRenderer. Pause</span><span class="sxs-lookup"><span data-stu-id="4b57c-103">CBaseRenderer.Pause method</span></span>

<span data-ttu-id="4b57c-104">O `Pause` método pausa o filtro.</span><span class="sxs-lookup"><span data-stu-id="4b57c-104">The `Pause` method pauses the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b57c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b57c-105">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="4b57c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4b57c-106">Parameters</span></span>

<span data-ttu-id="4b57c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="4b57c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b57c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4b57c-108">Return value</span></span>

<span data-ttu-id="4b57c-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4b57c-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4b57c-110">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4b57c-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="4b57c-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4b57c-111">Return code</span></span>                                                                             | <span data-ttu-id="4b57c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="4b57c-112">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="4b57c-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4b57c-113"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="4b57c-114">A transição foi concluída.</span><span class="sxs-lookup"><span data-stu-id="4b57c-114">The transition is complete.</span></span><br/> |
| <dl> <span data-ttu-id="4b57c-115"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="4b57c-115"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="4b57c-116">A transição não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="4b57c-116">Transition is not complete.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4b57c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b57c-117">Remarks</span></span>

<span data-ttu-id="4b57c-118">Esse método substitui o método [**CBaseFilter::P ause**](cbasefilter-pause.md) .</span><span class="sxs-lookup"><span data-stu-id="4b57c-118">This method overrides the [**CBaseFilter::Pause**](cbasefilter-pause.md) method.</span></span> <span data-ttu-id="4b57c-119">Ele executa as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="4b57c-119">It performs the following steps:</span></span>

-   <span data-ttu-id="4b57c-120">Chama o método **CBaseFilter::P ause** .</span><span class="sxs-lookup"><span data-stu-id="4b57c-120">Calls the **CBaseFilter::Pause** method.</span></span>
-   <span data-ttu-id="4b57c-121">Confirma o alocador.</span><span class="sxs-lookup"><span data-stu-id="4b57c-121">Commits the allocator.</span></span> <span data-ttu-id="4b57c-122">(Consulte [**IMemAllocator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span><span class="sxs-lookup"><span data-stu-id="4b57c-122">(See [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit).)</span></span>
-   <span data-ttu-id="4b57c-123">Se o estado anterior foi interrompido, o filtro libera qualquer amostra que está segurando.</span><span class="sxs-lookup"><span data-stu-id="4b57c-123">If the previous state was stopped, the filter releases any sample it is holding.</span></span> <span data-ttu-id="4b57c-124">(O exemplo não é mais válido.)</span><span class="sxs-lookup"><span data-stu-id="4b57c-124">(The sample is no longer valid.)</span></span>
-   <span data-ttu-id="4b57c-125">Chama o método [**CBaseRenderer:: CompleteStateChange**](cbaserenderer-completestatechange.md) e retorna o valor.</span><span class="sxs-lookup"><span data-stu-id="4b57c-125">Calls the [**CBaseRenderer::CompleteStateChange**](cbaserenderer-completestatechange.md) method and returns the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b57c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b57c-126">Requirements</span></span>



| <span data-ttu-id="4b57c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b57c-127">Requirement</span></span> | <span data-ttu-id="4b57c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="4b57c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b57c-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b57c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="4b57c-130"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b57c-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4b57c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4b57c-131">Library</span></span><br/> | <dl> <span data-ttu-id="4b57c-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4b57c-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b57c-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b57c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b57c-134">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="4b57c-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




