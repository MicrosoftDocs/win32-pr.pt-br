---
description: O método OnRenderEnd é chamado depois que um exemplo é renderizado.
ms.assetid: c9b3a3b2-a5c0-4a08-9e55-53c27a4d1032
title: Método CBaseRenderer. OnRenderEnd (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5859cf81a5fd0306f3470ee0fc6d54476e99833d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752502"
---
# <a name="cbaserendereronrenderend-method"></a><span data-ttu-id="12bfe-103">Método CBaseRenderer. OnRenderEnd</span><span class="sxs-lookup"><span data-stu-id="12bfe-103">CBaseRenderer.OnRenderEnd method</span></span>

<span data-ttu-id="12bfe-104">O `OnRenderEnd` método é chamado depois que um exemplo é renderizado.</span><span class="sxs-lookup"><span data-stu-id="12bfe-104">The `OnRenderEnd` method is called after a sample is rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="12bfe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12bfe-105">Syntax</span></span>


```C++
virtual void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="12bfe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12bfe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12bfe-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="12bfe-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="12bfe-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="12bfe-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12bfe-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12bfe-109">Return value</span></span>

<span data-ttu-id="12bfe-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="12bfe-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12bfe-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="12bfe-111">Remarks</span></span>

<span data-ttu-id="12bfe-112">O método [**CBaseRenderer:: render**](cbaserenderer-render.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="12bfe-112">The [**CBaseRenderer::Render**](cbaserenderer-render.md) method calls this method.</span></span> <span data-ttu-id="12bfe-113">Ele não faz nada na classe base, mas a classe derivada pode substituí-la; por exemplo, para coletar dados de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="12bfe-113">It does nothing in the base class, but the derived class can override it; for example, to collect quality-control data.</span></span>

## <a name="requirements"></a><span data-ttu-id="12bfe-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12bfe-114">Requirements</span></span>



| <span data-ttu-id="12bfe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="12bfe-115">Requirement</span></span> | <span data-ttu-id="12bfe-116">Valor</span><span class="sxs-lookup"><span data-stu-id="12bfe-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12bfe-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12bfe-117">Header</span></span><br/>  | <dl> <span data-ttu-id="12bfe-118"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12bfe-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="12bfe-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12bfe-119">Library</span></span><br/> | <dl> <span data-ttu-id="12bfe-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="12bfe-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12bfe-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="12bfe-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12bfe-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="12bfe-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




