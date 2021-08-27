---
description: 'O \_ método Get CurrentPosition recupera a posição atual, em relação à duração total do fluxo. Esse método implementa o método IMediaPosition:: get \_ CurrentPosition.'
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: Método de CPosPassThru.get_CurrentPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db49717284f597249603b3c18340855793ebd342632aeb2091861f9742963a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084236"
---
# <a name="cpospassthruget_currentposition-method"></a>CPosPassThru. obter \_ método CurrentPosition

O `get_CurrentPosition` método recupera a posição atual, em relação à duração total do fluxo. Esse método implementa o método [**IMediaPosition:: get \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pllTime* 
</dt> <dd>

Ponteiro para uma variável que recebe a posição atual, em segundos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o valor **HRESULT** do PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




