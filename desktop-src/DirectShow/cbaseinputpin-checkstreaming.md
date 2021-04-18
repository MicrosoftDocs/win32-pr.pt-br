---
description: Determina se o PIN pode aceitar amostras.
ms.assetid: bc66ab4c-99de-4031-bdac-b1430f736e20
title: Método CBaseInputPin. CheckStreaming (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CheckStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba07d28ac93f7dc511390a851d3c737a833ef3f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751274"
---
# <a name="cbaseinputpincheckstreaming-method"></a>Método CBaseInputPin. CheckStreaming

Determina se o PIN pode aceitar amostras.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CheckStreaming();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** listados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>                   |
| <dl> <dt>**\_falso**</dt> </dl>               | O PIN está sendo liberado no momento.<br/> |
| <dl> <dt>**VFW \_ E \_ erro de tempo de execução \_**</dt> </dl> | Ocorreu um erro em tempo de execução.<br/> |
| <dl> <dt>**VFW \_ E \_ estado incorreto \_**</dt> </dl>   | O PIN foi interrompido.<br/>        |



 

## <a name="remarks"></a>Comentários

A classe derivada pode substituir esse método para executar verificações adicionais. No método de substituição, também chame a implementação da classe base.

O método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) chama esse método. Você deve substituir o método [**CBasePin:: EndOfStream**](cbasepin-endofstream.md) para chamar esse método também.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




