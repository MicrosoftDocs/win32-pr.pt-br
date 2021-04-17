---
description: O método OnRenderStart é chamado quando a renderização está prestes a ser iniciada.
ms.assetid: 46af24cf-9075-4ebc-a49b-85f8f0c3da6f
title: Método CBaseRenderer. OnRenderStart (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7838b0ba43c1e570b745541882a2f2f815dd948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783193"
---
# <a name="cbaserendereronrenderstart-method"></a><span data-ttu-id="82ae2-103">Método CBaseRenderer. OnRenderStart</span><span class="sxs-lookup"><span data-stu-id="82ae2-103">CBaseRenderer.OnRenderStart method</span></span>

<span data-ttu-id="82ae2-104">O `OnRenderStart` método é chamado quando a renderização está prestes a ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="82ae2-104">The `OnRenderStart` method is called when rendering is about to start.</span></span>

## <a name="syntax"></a><span data-ttu-id="82ae2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="82ae2-105">Syntax</span></span>


```C++
virtual void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="82ae2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82ae2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82ae2-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="82ae2-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="82ae2-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="82ae2-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82ae2-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="82ae2-109">Return value</span></span>

<span data-ttu-id="82ae2-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="82ae2-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82ae2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="82ae2-111">Remarks</span></span>

<span data-ttu-id="82ae2-112">O método [**CBaseRenderer:: render**](cbaserenderer-render.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="82ae2-112">The [**CBaseRenderer::Render**](cbaserenderer-render.md) method calls this method.</span></span> <span data-ttu-id="82ae2-113">Ele não faz nada na classe base, mas a classe derivada pode substituí-la; por exemplo, para coletar dados de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="82ae2-113">It does nothing in the base class, but the derived class can override it; for example, to collect quality-control data.</span></span>

## <a name="requirements"></a><span data-ttu-id="82ae2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82ae2-114">Requirements</span></span>



| <span data-ttu-id="82ae2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="82ae2-115">Requirement</span></span> | <span data-ttu-id="82ae2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="82ae2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82ae2-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="82ae2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="82ae2-118"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="82ae2-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="82ae2-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82ae2-119">Library</span></span><br/> | <dl> <span data-ttu-id="82ae2-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="82ae2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82ae2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="82ae2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82ae2-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="82ae2-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




