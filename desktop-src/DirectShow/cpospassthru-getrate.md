---
description: 'Método CPosPassThru. GetRate – o método GetRate recupera a taxa de reprodução. Esse método implementa o método IMediaSeeking:: GetRate.'
ms.assetid: 19de3ea3-280e-4320-9cce-2c29801bd84b
title: Método CPosPassThru. GetRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9976b87b22fbe5ac81c56de006e5ca65862716a9bda62a5f881c141b1e108a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954025"
---
# <a name="cpospassthrugetrate-method"></a>Método CPosPassThru. GetRate

O `GetRate` método recupera a taxa de reprodução. Esse método implementa o método [**IMediaSeeking:: GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetRate(
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

 

 




