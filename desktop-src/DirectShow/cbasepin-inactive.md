---
description: Método CBasePin.Inactive – o método Inativo notifica o pino de que o filtro não está mais ativo.
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Método CBasePin.Inactive (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8307f3823758eee2f70368e41d3f2dc01333fd538fe2feed30d31b7db876f118
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052736"
---
# <a name="cbasepininactive-method"></a>Método CBasePin.Inactive

O `Inactive` método notifica o pino de que o filtro não está mais ativo.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Quando o filtro é interrompido, a [**classe CBaseFilter**](cbasefilter.md) chama esse método em todos os pinos conectados do filtro.

Esse método não faz nada na classe base. As classes derivadas devem substituir esse método para liberar todos os recursos obtidos pelo [**método CBasePin::Active;**](cbasepin-active.md) por exemplo, para delimitar os alocadores do pino.

O estado interno do gerenciador de grafo de filtro não é atualizado até que esse método retorne, portanto, não teste o estado desse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




