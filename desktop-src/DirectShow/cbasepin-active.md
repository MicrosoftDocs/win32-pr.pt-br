---
description: Método CBasePin.Active – o método Ativo notifica o pino de que o filtro agora está ativo.
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: Método CBasePin.Active (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1d651c58693789945af34d266aa8541679d1226d655530b90c542c8b0fc88b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872536"
---
# <a name="cbasepinactive-method"></a>Método CBasePin.Active

O `Active` método notifica o pino de que o filtro agora está ativo.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Quando o filtro passa de parado para pausado, a [**classe CBaseFilter**](cbasefilter.md) chama esse método em todos os pinos conectados do filtro.

Esse método não faz nada na classe base. Classes derivadas podem substituir esse método; por exemplo, um pin pode comprometer alocadores ou obter recursos de hardware.

O estado interno do gerenciador de grafo de filtro não é atualizado até que essa função membro retorne, portanto, não teste o estado desse método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




