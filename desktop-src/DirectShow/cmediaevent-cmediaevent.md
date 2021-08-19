---
description: Construtor CMediaEvent.CMediaEvent – Método do construtor.
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: Construtor CMediaEvent.CMediaEvent (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.CMediaEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b1809bcca029838e7e1df6d71c5d005aec3d21bdbcde9ccbd1b7a23b77dd9ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402019"
---
# <a name="cmediaeventcmediaevent-constructor"></a>Construtor CMediaEvent.CMediaEvent

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pname* 
</dt> <dd>

Ponteiro para o nome do objeto para fins de depuração.

</dd> <dt>

*Punk* 
</dt> <dd>

Ponteiro para o proprietário desse objeto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Aloce o *parâmetro pName* na memória estática. Esse nome aparece no terminal de depuração após a criação e exclusão do objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CMediaEvent**](cmediaevent.md)
</dt> </dl>

 

 




