---
description: O método Seek define as posições de início e parada do fluxo.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: Método CPullPin.Seek (Pullpin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Seek
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 65ea4deddd000d1064adf8b8caf5a636eed87105856d506191d677e70978d096
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953985"
---
# <a name="cpullpinseek-method"></a>Método CPullPin.Seek

O `Seek` método define as posições de início e parada do fluxo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Seek(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tstart* 
</dt> <dd>

Especifica a posição inicial, em bytes multiplicados por 10.000.000.

</dd> <dt>

*tStop* 
</dt> <dd>

Especifica a posição de parada, em bytes multiplicados por 10.000.000.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK se o método for bem-sucedido ou um código de erro, caso contrário.

## <a name="remarks"></a>Comentários

Se o thread de trabalho estiver em execução, o método pausará o thread, liberará o grafo de filtro e retomará o thread. O thread começa a esvasá-los da nova posição inicial. Caso contrário, os novos valores de posição se tornarão efetivos sempre que o thread for iniciado.

As posições são relativas ao início da origem original. Multiplique os deslocamentos de byte desejados pelas UNIDADES constantes, que é definida na biblioteca de classes base como 10.000.000.

Quando o pino se conecta pela primeira vez, as posições de parada e início são padrão para o início e o fim do fluxo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin.h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




