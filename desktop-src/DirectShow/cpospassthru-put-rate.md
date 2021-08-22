---
description: O \_ método de taxa Put define a taxa de reprodução. Esse método implementa o método de taxa IMediaPosition::p UT \_ .
ms.assetid: c077f344-de34-4f8a-8e08-6d7086a5a4f1
title: Método de CPosPassThru.put_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.put_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90c89c9730ee057bea3bc776f551061c0e828385fe3c6ae054f4161bdb705ab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565496"
---
# <a name="cpospassthruput_rate-method"></a>Método de taxa CPosPassThru. put \_

O `put_Rate` método define a taxa de reprodução. Esse método implementa o método de [**\_ taxa IMediaPosition::p UT**](/windows/desktop/api/Control/nf-control-imediaposition-put_rate) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_Rate(
   double dRate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dRate* 
</dt> <dd>

Taxa de reprodução. Não deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna E \_ INVALIDARG se *drate* for zero. Caso contrário, retorna o valor **HRESULT** do PIN conectado.

## <a name="remarks"></a>Comentários

As taxas negativas indicam a reprodução reversa. Nem toda mídia dará suporte à reprodução inversa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CPosPassThru**](cpospassthru.md)
</dt> </dl>

 

 




