---
description: O método \_ put CurrentPosition define a posição atual, em relação à duração total do fluxo. Esse método implementa o método IMediaPosition::p ut \_ CurrentPosition.
ms.assetid: 22d7e9e4-47da-45b5-9be0-3c5128f90353
title: CPosPassThru.put_CurrentPosition método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ab6a8323023e9a2cd20f9453dc00e0c56a688086f10772b72b59b3c012a24702
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909216"
---
# <a name="cpospassthruput_currentposition-method"></a>Método CurrentPosition CPosPassThru.put \_

O `put_CurrentPosition` método define a posição atual, em relação à duração total do fluxo. Esse método implementa o [**método IMediaPosition::p ut \_ CurrentPosition.**](/windows/desktop/api/Control/nf-control-imediaposition-put_currentposition)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_CurrentPosition(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*llTime* 
</dt> <dd>

Nova posição, em segundos.

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

 

 




