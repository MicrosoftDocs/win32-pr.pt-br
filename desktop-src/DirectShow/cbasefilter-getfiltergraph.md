---
description: O método GetFilterGraph recupera um ponteiro para o Gerenciador do grafo de filtro.
ms.assetid: 80b41272-2ca1-40db-8624-0d99d66f3c34
title: Método CBaseFilter. GetFilterGraph (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0843c7789afc1500565d2737d863cbc8af114d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752519"
---
# <a name="cbasefiltergetfiltergraph-method"></a>Método CBaseFilter. GetFilterGraph

O `GetFilterGraph` método recupera um ponteiro para o Gerenciador de gráfico de filtro.

## <a name="syntax"></a>Sintaxe


```C++
IFilterGraph* GetFilterGraph();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna o valor de [**CBaseFilter:: m \_ pGraph**](cbasefilter-m-pgraph.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




