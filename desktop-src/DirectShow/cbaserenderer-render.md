---
description: O método Render renderiza um exemplo.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: Método CBaseRenderer. Render (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Render
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fefd44fe1b913fbba0e3ebfaa6f750b88d40813
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751905"
---
# <a name="cbaserendererrender-method"></a><span data-ttu-id="4f3a4-103">Método CBaseRenderer. render</span><span class="sxs-lookup"><span data-stu-id="4f3a4-103">CBaseRenderer.Render method</span></span>

<span data-ttu-id="4f3a4-104">O `Render` método renderiza um exemplo.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-104">The `Render` method renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f3a4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f3a4-105">Syntax</span></span>


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="4f3a4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f3a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f3a4-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="4f3a4-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="4f3a4-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f3a4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4f3a4-109">Return value</span></span>

<span data-ttu-id="4f3a4-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4f3a4-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4f3a4-111">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-111">Possible values include those in the following table.</span></span>



| <span data-ttu-id="4f3a4-112">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="4f3a4-112">Return code</span></span>                                                                             | <span data-ttu-id="4f3a4-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f3a4-113">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f3a4-114"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="4f3a4-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="4f3a4-115">O filtro está parado ou *pMediaSample* é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-115">The filter is stopped, or *pMediaSample* is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="4f3a4-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4f3a4-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="4f3a4-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-117">Success.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="4f3a4-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f3a4-118">Remarks</span></span>

<span data-ttu-id="4f3a4-119">Esse método chama o método virtual puro [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md), que faz o trabalho real.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-119">This method calls the pure virtual method [**CBaseRenderer::DoRenderSample**](cbaserenderer-dorendersample.md), which does the real work.</span></span> <span data-ttu-id="4f3a4-120">A classe derivada deve implementar **DoRenderSample**.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-120">The derived class must implement **DoRenderSample**.</span></span>

<span data-ttu-id="4f3a4-121">Imediatamente antes de chamar **DoRenderSample**, esse método chama o método [**CBaseRenderer:: OnRenderStart**](cbaserenderer-onrenderstart.md) .</span><span class="sxs-lookup"><span data-stu-id="4f3a4-121">Immediately before calling **DoRenderSample**, this method calls the [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md) method.</span></span> <span data-ttu-id="4f3a4-122">Imediatamente depois, ele chama o método [**CBaseRenderer:: OnRenderEnd**](cbaserenderer-onrenderend.md) .</span><span class="sxs-lookup"><span data-stu-id="4f3a4-122">Immediately after, it calls the [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md) method.</span></span> <span data-ttu-id="4f3a4-123">A classe derivada pode substituir esses dois métodos conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="4f3a4-123">The derived class can override those two methods as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f3a4-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f3a4-124">Requirements</span></span>



| <span data-ttu-id="4f3a4-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f3a4-125">Requirement</span></span> | <span data-ttu-id="4f3a4-126">Valor</span><span class="sxs-lookup"><span data-stu-id="4f3a4-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f3a4-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f3a4-127">Header</span></span><br/>  | <dl> <span data-ttu-id="4f3a4-128"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f3a4-128"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4f3a4-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f3a4-129">Library</span></span><br/> | <dl> <span data-ttu-id="4f3a4-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4f3a4-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f3a4-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f3a4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f3a4-132">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="4f3a4-132">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




