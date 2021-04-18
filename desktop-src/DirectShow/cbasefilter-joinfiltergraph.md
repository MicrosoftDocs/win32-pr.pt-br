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
# <a name="cbasefilterjoinfiltergraph-method"></a>Método CBaseFilter. JoinFilterGraph

O `JoinFilterGraph` método notifica o filtro de que ele ingressou ou deixou um grafo de filtro. Esse método implementa o método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT JoinFilterGraph(
       IFilterGraph *pGraph,
  [in] LPCWSTR      pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pGraph* 
</dt> <dd>

Ponteiro para a interface [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph) do Gerenciador de gráfico de filtro ou **nulo** se o filtro estiver saindo do grafo.

</dd> <dt>

*pname* \[ no\]
</dt> <dd>

Ponteiro para uma cadeia de caracteres Unicode que contém um nome para o filtro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método define a variável de membro [**CBaseFilter:: m \_ pGraph**](cbasefilter-m-pgraph.md) igual ao parâmetro *pGraph* . Ele também consulta um ponteiro de interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) e o armazena na variável de membro [**CBaseFilter:: m \_ pSink**](cbasefilter-m-psink.md) . No entanto, o filtro não mantém uma contagem de referência em nenhuma dessas interfaces. Isso criaria uma contagem de referência circular, pois o Gerenciador do grafo de filtro mantém uma contagem de referência no filtro.

O método copia a cadeia de caracteres especificada por *pname* na variável de membro [**CBaseFilter:: m \_ pname**](cbasefilter-m-pname.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




