---
description: O método SetFilterGraph especifica o coletor de eventos para eventos de controle de fluxo.
ms.assetid: a4c3dca6-6c80-4eca-87d6-875e746e9ed3
title: Método CBaseStreamControl. SetFilterGraph (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.SetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1cf8b571ee5d017acd056e00a06af54cd90b943a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752501"
---
# <a name="cbasestreamcontrolsetfiltergraph-method"></a><span data-ttu-id="f1467-103">Método CBaseStreamControl. SetFilterGraph</span><span class="sxs-lookup"><span data-stu-id="f1467-103">CBaseStreamControl.SetFilterGraph method</span></span>

<span data-ttu-id="f1467-104">O `SetFilterGraph` método especifica o coletor de eventos para eventos de controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="f1467-104">The `SetFilterGraph` method specifies the event sink for stream control events.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1467-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1467-105">Syntax</span></span>


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a><span data-ttu-id="f1467-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1467-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1467-107">*pSink*</span><span class="sxs-lookup"><span data-stu-id="f1467-107">*pSink*</span></span> 
</dt> <dd>

<span data-ttu-id="f1467-108">Ponteiro para a interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) do Gerenciador de gráfico de filtro ou **nulo** quando o filtro deixa o gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="f1467-108">Pointer to the Filter Graph Manager's [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface, or **NULL** when the filter leaves the filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1467-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1467-109">Return value</span></span>

<span data-ttu-id="f1467-110">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f1467-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1467-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1467-111">Remarks</span></span>

<span data-ttu-id="f1467-112">Chame esse método de dentro do método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) do filtro.</span><span class="sxs-lookup"><span data-stu-id="f1467-112">Call this method from inside the filter's [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span> <span data-ttu-id="f1467-113">A classe **CBaseStreamControl** usa a interface **IMediaEventSink** para enviar o controle de [**fluxo do EC \_ \_ \_ iniciado**](ec-stream-control-started.md) e eventos [**\_ \_ \_ interrompidos pelo controle de fluxo do EC**](ec-stream-control-stopped.md) .</span><span class="sxs-lookup"><span data-stu-id="f1467-113">The **CBaseStreamControl** class uses the **IMediaEventSink** interface to send [**EC\_STREAM\_CONTROL\_STARTED**](ec-stream-control-started.md) and [**EC\_STREAM\_CONTROL\_STOPPED**](ec-stream-control-stopped.md) events.</span></span>

<span data-ttu-id="f1467-114">Se o filtro deriva de **CBaseFilter**, primeiro chame o método [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) , que define a variável de membro [**CBaseFilter:: m \_ pSink**](cbasefilter-m-psink.md) .</span><span class="sxs-lookup"><span data-stu-id="f1467-114">If your filter derives from **CBaseFilter**, first call the [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) method, which sets the [**CBaseFilter::m\_pSink**](cbasefilter-m-psink.md) member variable.</span></span> <span data-ttu-id="f1467-115">Em seguida, passe **m \_ pSink** para o `SetFilterGraph` método.</span><span class="sxs-lookup"><span data-stu-id="f1467-115">Then pass **m\_pSink** to the `SetFilterGraph` method.</span></span> <span data-ttu-id="f1467-116">Observe que **m \_ PSink** é **nulo** quando o filtro deixa o grafo, que está correto.</span><span class="sxs-lookup"><span data-stu-id="f1467-116">Note that **m\_pSink** is **NULL** when the filter leaves the graph, which is correct.</span></span>

## <a name="examples"></a><span data-ttu-id="f1467-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f1467-117">Examples</span></span>


```C++
STDMETHODIMP CMyFilter::JoinFilterGraph(IFilterGraph * pGraph, LPCWSTR pName)
{
    // Note: It's OK if pGraph is NULL.

    HRESULT hr = CBaseFilter::JoinFilterGraph(pGraph, pName);
    if (SUCCEEDED(hr)) 
    {
        m_pMyPin->SetFilterGraph(m_pSink);
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="f1467-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1467-118">Requirements</span></span>



| <span data-ttu-id="f1467-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1467-119">Requirement</span></span> | <span data-ttu-id="f1467-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f1467-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1467-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1467-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f1467-122"><dt>Strmctl. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1467-122"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f1467-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1467-123">Library</span></span><br/> | <dl> <span data-ttu-id="f1467-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f1467-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1467-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1467-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1467-126">**Classe CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="f1467-126">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




