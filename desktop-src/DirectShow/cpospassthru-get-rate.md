---
description: 'O \_ método obter taxa recupera a taxa de reprodução. Esse método implementa o método de taxa IMediaPosition:: get \_ .'
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: Método de CPosPassThru.get_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fa8014d23bc488b4f0b8b0cc9b872dfdf4a56cced396cc22eefab5912df1706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073530"
---
# <a name="cpospassthruget_rate-method"></a>Método de taxa CPosPassThru. get \_

O `get_Rate` método recupera a taxa de reprodução. Esse método implementa o método de [**\_ taxa IMediaPosition:: Get**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Rate(
   double *pdRate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pdRate* 
</dt> <dd>

Ponteiro para uma variável que recebe a taxa de reprodução.

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

 

 




