---
description: 'O \_ método Get StopTime recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo. Esse método implementa o método IMediaPosition:: get \_ StopTime.'
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: Método de CPosPassThru.get_StopTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 227b054a9737c06e56f7311acc7e0093766608b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751686"
---
# <a name="cpospassthruget_stoptime-method"></a>CPosPassThru. obter \_ método StopTime

O `get_StopTime` método recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo. Esse método implementa o método [**IMediaPosition:: get \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_StopTime(
   REFTIME *pllTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pllTime* 
</dt> <dd>

Ponteiro para uma variável que recebe a hora de parada, em segundos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o valor **HRESULT** do PIN conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




