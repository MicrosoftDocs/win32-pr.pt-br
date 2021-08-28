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
ms.openlocfilehash: 304ec081ce7087d822ce3382bf4784c05cbc8782fadb3cdfee887f6bd8f0acfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502636"
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

ponteiro para o filtro Graph interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) do gerenciador ou **nulo** quando o filtro deixa o gráfico de filtro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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
| parâmetro<br/>  | <dl> <dt>Strmctl. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




