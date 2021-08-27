---
description: O método get StopTime recupera a hora em que a reprodução será parada, em relação \_ à duração do fluxo. Esse método implementa o método IMediaPosition::get \_ StopTime.
ms.assetid: 0ca3f047-ac43-419e-a1ed-b406f89f7af7
title: CPosPassThru.get_StopTime método (Ctlutil.h)
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
ms.openlocfilehash: ea233d7e3a148088edd0f6963f45aeb0b483b41317481a95733fdc73c242027d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108296"
---
# <a name="cpospassthruget_stoptime-method"></a>Método CPosPassThru.get \_ StopTime

O `get_StopTime` método recupera a hora em que a reprodução será parada, em relação à duração do fluxo. Esse método implementa o [**método IMediaPosition::get \_ StopTime.**](/windows/desktop/api/Control/nf-control-imediaposition-get_stoptime)

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

## <a name="return-value"></a>Valor retornado

Retorna o **valor HRESULT** do pino conectado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




