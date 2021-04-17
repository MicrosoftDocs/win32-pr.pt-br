---
description: 'O \_ método Get Duration recupera a duração do fluxo. Esse método implementa o método de duração IMediaPosition:: get \_ .'
ms.assetid: 326a8cd3-d05f-49d0-941d-08f9778e9a06
title: Método de CPosPassThru.get_Duration (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: df518a0691a4fe1a6c0443ba93a83e65577efe21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789961"
---
# <a name="cpospassthruget_duration-method"></a>Método Duration de CPosPassThru. get \_

O `get_Duration` método recupera a duração do fluxo. Esse método implementa o método de [**\_ duração IMediaPosition:: Get**](/windows/desktop/api/Control/nf-control-imediaposition-get_duration) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Duration(
   REFTIME *plength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*plength* 
</dt> <dd>

Ponteiro para uma variável que recebe o tamanho total do fluxo, em segundos.

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

 

 




