---
description: O método OnError será chamado se ocorrer um erro durante o streaming. A classe derivada deve implementar esse método.
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: Método CPullPin. OnError (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dc8bf7f307ab56609b5f90f6955a1f666854270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780860"
---
# <a name="cpullpinonerror-method"></a>Método CPullPin. OnError

O `OnError` método será chamado se ocorrer um erro durante o streaming. A classe derivada deve implementar esse método.

## <a name="syntax"></a>Sintaxe


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*h* 
</dt> <dd>

Especifica o valor **HRESULT** retornado pelo método que falhou.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O objeto chama esse método sempre que ocorre um erro que interrompe o thread de extração de dados. O filtro pode usar esse método para se recuperar de erros de streaming normalmente. Na maioria dos casos, o erro é retornado do filtro upstream, portanto, o filtro upstream é responsável por reportá-lo para o Gerenciador do grafo de filtro. Se o erro ocorrer dentro do método [**CPullPin:: Receive**](cpullpin-receive.md) , o filtro deverá enviar um evento de [**\_ ERRORABORT do EC**](ec-errorabort.md) . (Consulte [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




