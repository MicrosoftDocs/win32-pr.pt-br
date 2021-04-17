---
description: O \_ método Put preverttime define a quantidade de dados que serão enfileirados antes da posição inicial. Esse método implementa o método IMediaPosition::p UT \_ preverttime.
ms.assetid: 5c35fb1d-2296-493f-8104-601127d7dd9f
title: Método de CPosPassThru.put_PrerollTime (Ctlutil. h)
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
ms.openlocfilehash: 60bd4eddc7688373386147ea7999fdbd17f9af6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752287"
---
# <a name="cpospassthruput_prerolltime-method"></a>CPosPassThru. put \_ método preverttime

O `put_PrerollTime` método define a quantidade de dados que serão enfileirados antes da posição inicial. Esse método implementa o método [**IMediaPosition::p UT \_ preverttime**](/windows/desktop/api/Control/nf-control-imediaposition-put_prerolltime) .

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

Tempo de preversão, em segundos.

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

 

 




