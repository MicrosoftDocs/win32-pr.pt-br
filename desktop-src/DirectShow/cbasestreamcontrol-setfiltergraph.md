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
# <a name="cbasestreamcontrolsetfiltergraph-method"></a>Método CBaseStreamControl. SetFilterGraph

O `SetFilterGraph` método especifica o coletor de eventos para eventos de controle de fluxo.

## <a name="syntax"></a>Sintaxe


```C++
void SetFilterGraph(
   IMediaEventSink *pSink
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSink* 
</dt> <dd>

Ponteiro para a interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) do Gerenciador de gráfico de filtro ou **nulo** quando o filtro deixa o gráfico de filtro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Chame esse método de dentro do método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) do filtro. A classe **CBaseStreamControl** usa a interface **IMediaEventSink** para enviar o controle de [**fluxo do EC \_ \_ \_ iniciado**](ec-stream-control-started.md) e eventos [**\_ \_ \_ interrompidos pelo controle de fluxo do EC**](ec-stream-control-stopped.md) .

Se o filtro deriva de **CBaseFilter**, primeiro chame o método [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) , que define a variável de membro [**CBaseFilter:: m \_ pSink**](cbasefilter-m-psink.md) . Em seguida, passe **m \_ pSink** para o `SetFilterGraph` método. Observe que **m \_ PSink** é **nulo** quando o filtro deixa o grafo, que está correto.

## <a name="examples"></a>Exemplos


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Strmctl. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




