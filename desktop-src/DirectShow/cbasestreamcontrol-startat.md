---
description: O método StartAt informa ao pin quando iniciar a entrega de dados. Esse método implementa o método IAMStreamControl::StartAt.
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: Método CBaseStreamControl.StartAt (Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40570933e7eed054694b2da927d71e077b86941aea816ff2ca6de5c91372b9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814106"
---
# <a name="cbasestreamcontrolstartat-method"></a>Método CBaseStreamControl.StartAt

O `StartAt` método informa o pin quando iniciar a entrega de dados. Esse método implementa o [**método IAMStreamControl::StartAt.**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ptStart* 
</dt> <dd>

Ponteiro para um [**valor \_ REFERENCE TIME**](reference-time.md) que especifica quando o pino deve começar a entregar dados.

</dd> <dt>

*Dwcookie* 
</dt> <dd>

Especifica um valor a ser enviado junto com a notificação de início.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Strmctl.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseStreamControl**](cbasestreamcontrol.md)
</dt> </dl>

 

 




