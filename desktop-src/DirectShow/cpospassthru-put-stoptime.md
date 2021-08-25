---
description: O \_ método Put StopTime define a hora em que a reprodução será interrompida, em relação à duração do fluxo. Esse método implementa o método IMediaPosition::p UT \_ StopTime.
ms.assetid: 0a344cad-df93-47f1-8c7f-5d5ef775b850
title: Método de CPosPassThru.put_StopTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_StopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d91d49f2517a3d3b9efc50d70ace1b75562b50df8acda7c48826e7c088439928
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055086"
---
# <a name="cpospassthruput_stoptime-method"></a>Método StopTime de CPosPassThru. put \_

O `put_StopTime` método define a hora em que a reprodução será interrompida, em relação à duração do fluxo. Esse método implementa o método [**IMediaPosition::p UT \_ StopTime**](/windows/desktop/api/Control/nf-control-imediaposition-put_stoptime) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_StopTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*llTime* 
</dt> <dd>

Hora de parada como um valor **duplo** , em segundos.

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

 

 




