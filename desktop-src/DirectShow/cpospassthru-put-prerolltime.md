---
description: O método \_ put PrerollTime define a quantidade de dados que serão colocados na fila antes da posição inicial. Esse método implementa o método IMediaPosition::p ut \_ PrerollTime.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: CPosPassThru.put_PrerollTime método (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_PrerollTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825c3c584fc6db7eb9f94b4e8d01e003f5cf6c36ff8adac4041fd48f792ca858
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909196"
---
# <a name="cpospassthruput_prerolltime-method"></a>Método CPosPassThru.put \_ PrerollTime

O `put_PrerollTime` método define a quantidade de dados que serão ensuados antes da posição inicial. Esse método implementa o [**método IMediaPosition::p ut \_ PrerollTime.**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_PrerollTime(
   REFTIME llTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*llTime* 
</dt> <dd>

Tempo de pré-roll, em segundos.

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

 

 




