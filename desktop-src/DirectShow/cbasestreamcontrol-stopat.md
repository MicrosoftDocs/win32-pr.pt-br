---
description: 'O método StopAt informa o PIN quando parar de entregar dados. Esse método implementa o método IAMStreamControl:: StopAt.'
ms.assetid: cc9f0fdc-253b-4feb-95ce-56ebc575a49b
title: Método CBaseStreamControl. StopAt (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StopAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e6b794f5f05721f403d943252c2aabd48614519
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778513"
---
# <a name="cbasestreamcontrolstopat-method"></a>Método CBaseStreamControl. StopAt

O `StopAt` método informa o PIN quando parar de entregar dados. Esse método implementa o método [**IAMStreamControl:: StopAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT StopAt(
   const REFERENCE_TIME *ptStop = NULL,
         BOOL           bSendExtra = FALSE,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ptStop* 
</dt> <dd>

Ponteiro para um valor de [**\_ tempo de referência**](reference-time.md) que especifica quando o PIN deve parar de entregar dados.

</dd> <dt>

*bSendExtra* 
</dt> <dd>

Especifica um valor booliano que indica se um exemplo extra deve ser enviado após a hora de término agendada. Se **for true**, o PIN enviará um exemplo extra.

</dd> <dt>

*dwCookie* 
</dt> <dd>

Especifica um valor a ser enviado junto com a notificação de início.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Strmctl. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




