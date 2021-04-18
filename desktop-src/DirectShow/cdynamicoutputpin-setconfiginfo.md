---
description: O método SetConfigInfo especifica o ponteiro IGraphConfig e o evento stop.
ms.assetid: 938fe8be-5622-4954-9ba3-31fc68fbfa31
title: Método CDynamicOutputPin. SetConfigInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.SetConfigInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0c14342a629a38a878649ac59d8f1f814874f12
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749019"
---
# <a name="cdynamicoutputpinsetconfiginfo-method"></a><span data-ttu-id="cc9f4-103">Método CDynamicOutputPin. SetConfigInfo</span><span class="sxs-lookup"><span data-stu-id="cc9f4-103">CDynamicOutputPin.SetConfigInfo method</span></span>

<span data-ttu-id="cc9f4-104">O `SetConfigInfo` método especifica o ponteiro [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e o evento stop.</span><span class="sxs-lookup"><span data-stu-id="cc9f4-104">The `SetConfigInfo` method specifies the [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) pointer and the stop event.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc9f4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cc9f4-105">Syntax</span></span>


```C++
void SetConfigInfo(
   IGraphConfig *pGraphConfig,
   HANDLE       hStopEvent
);
```



## <a name="parameters"></a><span data-ttu-id="cc9f4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cc9f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc9f4-107">*pGraphConfig*</span><span class="sxs-lookup"><span data-stu-id="cc9f4-107">*pGraphConfig*</span></span> 
</dt> <dd>

<span data-ttu-id="cc9f4-108">Ponteiro para a interface [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="cc9f4-108">Pointer to the [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) interface, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc9f4-109">*hStopEvent*</span><span class="sxs-lookup"><span data-stu-id="cc9f4-109">*hStopEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="cc9f4-110">Identificador para um evento que é sinalizado quando o filtro é interrompido ou **nulo**.</span><span class="sxs-lookup"><span data-stu-id="cc9f4-110">Handle to an event that is signaled when the filter stops, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc9f4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cc9f4-111">Return value</span></span>

<span data-ttu-id="cc9f4-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cc9f4-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc9f4-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc9f4-113">Remarks</span></span>

<span data-ttu-id="cc9f4-114">O filtro deve chamar esse método quando ele ingressar no grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="cc9f4-114">The filter must call this method when it joins the filter graph.</span></span> <span data-ttu-id="cc9f4-115">O Gerenciador do grafo de filtro dá suporte a **IGraphConfig**.</span><span class="sxs-lookup"><span data-stu-id="cc9f4-115">The filter graph manager supports **IGraphConfig**.</span></span> <span data-ttu-id="cc9f4-116">Para o parâmetro *hStopEvent* , crie um evento de redefinição manual.</span><span class="sxs-lookup"><span data-stu-id="cc9f4-116">For the *hStopEvent* parameter, create a manual-reset event.</span></span> <span data-ttu-id="cc9f4-117">Quando o filtro deixa o gráfico de filtro, chame esse método novamente com **NULL** para ambos os parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cc9f4-117">When the filter leaves the filter graph, call this method again with **NULL** for both parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc9f4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc9f4-118">Requirements</span></span>



| <span data-ttu-id="cc9f4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc9f4-119">Requirement</span></span> | <span data-ttu-id="cc9f4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cc9f4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc9f4-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc9f4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cc9f4-122"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc9f4-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cc9f4-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc9f4-123">Library</span></span><br/> | <dl> <span data-ttu-id="cc9f4-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cc9f4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc9f4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc9f4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc9f4-126">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="cc9f4-126">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




