---
description: O método PreparePerformanceData define os \_ valores m trLate e m \_ trFrame do quadro atual.
ms.assetid: c4c5701b-eccd-4259-a1d1-7c5000f6b2df
title: Método CBaseVideoRenderer. PreparePerformanceData (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.PreparePerformanceData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12dd61dee7416ce8ca7ac07cba62cbc769df5973
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749026"
---
# <a name="cbasevideorendererprepareperformancedata-method"></a><span data-ttu-id="7ee1e-103">Método CBaseVideoRenderer. PreparePerformanceData</span><span class="sxs-lookup"><span data-stu-id="7ee1e-103">CBaseVideoRenderer.PreparePerformanceData method</span></span>

<span data-ttu-id="7ee1e-104">O `PreparePerformanceData` método define os valores **m \_ trLate** e **m \_ trFrame** do quadro atual.</span><span class="sxs-lookup"><span data-stu-id="7ee1e-104">The `PreparePerformanceData` method sets the **m\_trLate** and **m\_trFrame** values of the current frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ee1e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ee1e-105">Syntax</span></span>


```C++
void PreparePerformanceData(
   int trLate,
   int trFrame
);
```



## <a name="parameters"></a><span data-ttu-id="7ee1e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ee1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ee1e-107">*trLate*</span><span class="sxs-lookup"><span data-stu-id="7ee1e-107">*trLate*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee1e-108">Valor que indica o quão tarde o exemplo estava além do tempo de vida, em unidades de tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="7ee1e-108">Value indicating how late the sample was beyond its due time, in reference time units.</span></span>

</dd> <dt>

<span data-ttu-id="7ee1e-109">*trFrame*</span><span class="sxs-lookup"><span data-stu-id="7ee1e-109">*trFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="7ee1e-110">Tempo entre quadros, em unidades de tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="7ee1e-110">Interframe time, in reference time units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ee1e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ee1e-111">Return value</span></span>

<span data-ttu-id="7ee1e-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="7ee1e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ee1e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ee1e-113">Remarks</span></span>

<span data-ttu-id="7ee1e-114">Essa função de membro **define m \_ trLate** como o valor de *trLate* e **m \_ trFrame** como o valor de *trFrame*.</span><span class="sxs-lookup"><span data-stu-id="7ee1e-114">This member function sets **m\_trLate** to the value of *trLate* and **m\_trFrame** to the value of *trFrame*.</span></span>

<span data-ttu-id="7ee1e-115">Quando a função de membro [**CBaseVideoRenderer:: RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) é chamada de [**CBaseVideoRenderer:: OnRenderStart**](cbasevideorenderer-onrenderstart.md) ou [**CBaseVideoRenderer:: OnDirectRender**](cbasevideorenderer-ondirectrender.md), ela passa os valores de **m \_ trLate** e **m \_ trFrame** para que ele atualize as estatísticas.</span><span class="sxs-lookup"><span data-stu-id="7ee1e-115">When the [**CBaseVideoRenderer::RecordFrameLateness**](cbasevideorenderer-recordframelateness.md) member function is called from either [**CBaseVideoRenderer::OnRenderStart**](cbasevideorenderer-onrenderstart.md) or [**CBaseVideoRenderer::OnDirectRender**](cbasevideorenderer-ondirectrender.md), it passes the values of **m\_trLate** and **m\_trFrame** for it to update the statistics.</span></span> <span data-ttu-id="7ee1e-116">`PreparePerformanceData` é chamado de [**CBaseVideoRenderer:: OnWaitEnd**](cbasevideorenderer-onwaitend.md) para definir esses valores de membro de dados.</span><span class="sxs-lookup"><span data-stu-id="7ee1e-116">`PreparePerformanceData` is called from [**CBaseVideoRenderer::OnWaitEnd**](cbasevideorenderer-onwaitend.md) to set these data member values.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ee1e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ee1e-117">Requirements</span></span>



| <span data-ttu-id="7ee1e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ee1e-118">Requirement</span></span> | <span data-ttu-id="7ee1e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7ee1e-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ee1e-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ee1e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7ee1e-121"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ee1e-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7ee1e-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ee1e-122">Library</span></span><br/> | <dl> <span data-ttu-id="7ee1e-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7ee1e-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ee1e-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ee1e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ee1e-125">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="7ee1e-125">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




