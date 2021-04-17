---
description: 'O método EndOfStream notifica o PIN de que nenhum dado adicional é esperado. Esse método implementa o método IPin:: EndOfStream. Chame esse método somente em Pins de entrada.'
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Método CBasePin. EndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2324bae8ec1266dce2471049f8ba2f06b0c9e6e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769243"
---
# <a name="cbasepinendofstream-method"></a>Método CBasePin. EndOfStream

O `EndOfStream` método notifica o PIN de que nenhum dado adicional é esperado. Esse método implementa o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) . Chame esse método somente em Pins de entrada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

O filtro deve passar notificações de fim de fluxo downstream para os Pins de entrada dos filtros conectados. Se o filtro for um renderizador, ele deverá lançar uma notificação de evento do [**EC \_ Complete**](ec-complete.md) para o Gerenciador do grafo de filtro. Para obter mais informações, consulte [fluxo de dados no grafo de filtro](data-flow-in-the-filter-graph.md).

Na classe base, esse método não faz nada. Classes derivadas devem substituir esse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




