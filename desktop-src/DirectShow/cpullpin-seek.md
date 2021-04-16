---
description: O método Seek define as posições de início e parada do fluxo.
ms.assetid: d84476f5-688c-429d-a51b-7020a6316e35
title: Método CPullPin. Seek (Pullpin. h)
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
ms.openlocfilehash: 6f1a82ec549b5ceb888acc194a7abc2cd3eace47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754147"
---
# <a name="cpullpinseek-method"></a>Método CPullPin. Seek

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

*tStart* 
</dt> <dd>

Especifica a posição inicial, em bytes multiplicada por 10 milhões.

</dd> <dt>

*tStop* 
</dt> <dd>

Especifica a posição de parada, em bytes multiplicada por 10 milhões.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se o método for bem sucedido ou um código de erro do contrário.

## <a name="remarks"></a>Comentários

Se o thread de trabalho estiver em execução, o método pausará o thread, liberará o gráfico de filtro e retomará o thread. O thread começa a extrair dados da nova posição inicial. Caso contrário, os novos valores de posição entram em vigor sempre que o thread for iniciado.

As posições são relativas ao início da fonte original. Multiplique os deslocamentos de bytes desejados pelas unidades constantes, que são definidas na biblioteca de classes base como 10 milhões.

Quando o PIN se conecta pela primeira vez, as posições de parar e iniciar padrão para o início e o fim do fluxo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPullPin**](cpullpin.md)
</dt> </dl>

 

 




