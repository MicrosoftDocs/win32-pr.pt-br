---
description: 'O método JoinFilterGraph notifica o filtro de que ele ingressou ou saiu de um grafo de filtro. Esse método implementa o método IBaseFilter:: JoinFilterGraph.'
ms.assetid: ee02650c-aaf0-4a0e-914f-180230010709
title: Método CBaseFilter. JoinFilterGraph (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.JoinFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45453c6423b8fa9f68e5d8dff86d13b130d65f6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750681"
---
# <a name="cbasefilterjoinfiltergraph-method"></a><span data-ttu-id="57b36-104">Método CBaseFilter. JoinFilterGraph</span><span class="sxs-lookup"><span data-stu-id="57b36-104">CBaseFilter.JoinFilterGraph method</span></span>

<span data-ttu-id="57b36-105">O `JoinFilterGraph` método notifica o filtro de que ele ingressou ou deixou um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="57b36-105">The `JoinFilterGraph` method notifies the filter that it has joined or left a filter graph.</span></span> <span data-ttu-id="57b36-106">Esse método implementa o método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .</span><span class="sxs-lookup"><span data-stu-id="57b36-106">This method implements the [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="57b36-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57b36-107">Syntax</span></span>


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a><span data-ttu-id="57b36-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57b36-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57b36-109">*pGraph*</span><span class="sxs-lookup"><span data-stu-id="57b36-109">*pGraph*</span></span> 
</dt> <dd>

<span data-ttu-id="57b36-110">Ponteiro para a interface [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) do Gerenciador de gráfico de filtro ou **nulo** se o filtro estiver saindo do grafo.</span><span class="sxs-lookup"><span data-stu-id="57b36-110">Pointer to the filter graph manager's [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) interface, or **NULL** if the filter is leaving the graph.</span></span>

</dd> <dt>

<span data-ttu-id="57b36-111">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="57b36-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57b36-112">Ponteiro para uma cadeia de caracteres Unicode que contém um nome para o filtro.</span><span class="sxs-lookup"><span data-stu-id="57b36-112">Pointer to a Unicode string containing a name for the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57b36-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57b36-113">Return value</span></span>

<span data-ttu-id="57b36-114">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="57b36-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="57b36-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="57b36-115">Remarks</span></span>

<span data-ttu-id="57b36-116">Esse método define a variável de membro [**CBaseFilter:: m \_ pGraph**](cbasefilter-m-pgraph.md) igual ao parâmetro *pGraph* .</span><span class="sxs-lookup"><span data-stu-id="57b36-116">This method sets the [**CBaseFilter::m\_pGraph**](cbasefilter-m-pgraph.md) member variable equal to the *pGraph* parameter.</span></span> <span data-ttu-id="57b36-117">Ele também consulta um ponteiro de interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) e o armazena na variável de membro [**CBaseFilter:: m \_ pSink**](cbasefilter-m-psink.md) .</span><span class="sxs-lookup"><span data-stu-id="57b36-117">It also queries for an [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface pointer and stores it in the [**CBaseFilter::m\_pSink**](cbasefilter-m-psink.md) member variable.</span></span> <span data-ttu-id="57b36-118">No entanto, o filtro não mantém uma contagem de referência em nenhuma dessas interfaces.</span><span class="sxs-lookup"><span data-stu-id="57b36-118">However, the filter does not keep a reference count on either of these interfaces.</span></span> <span data-ttu-id="57b36-119">Isso criaria uma contagem de referência circular, pois o Gerenciador do grafo de filtro mantém uma contagem de referência no filtro.</span><span class="sxs-lookup"><span data-stu-id="57b36-119">Doing so would create a circular reference count, because the filter graph manager keeps a reference count on the filter.</span></span>

<span data-ttu-id="57b36-120">O método copia a cadeia de caracteres especificada por *pname* na variável de membro [**CBaseFilter:: m \_ pname**](cbasefilter-m-pname.md) .</span><span class="sxs-lookup"><span data-stu-id="57b36-120">The method copies the string specified by *pName* into the [**CBaseFilter::m\_pName**](cbasefilter-m-pname.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="57b36-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57b36-121">Requirements</span></span>



| <span data-ttu-id="57b36-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="57b36-122">Requirement</span></span> | <span data-ttu-id="57b36-123">Valor</span><span class="sxs-lookup"><span data-stu-id="57b36-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57b36-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57b36-124">Header</span></span><br/>  | <dl> <span data-ttu-id="57b36-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57b36-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="57b36-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57b36-126">Library</span></span><br/> | <dl> <span data-ttu-id="57b36-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="57b36-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57b36-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="57b36-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b36-129">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="57b36-129">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




