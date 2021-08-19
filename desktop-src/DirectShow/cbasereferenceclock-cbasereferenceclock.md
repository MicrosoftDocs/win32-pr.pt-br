---
description: Construtor CBaseReferenceClock.CBaseReferenceClock – método construtor.
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: Construtor CBaseReferenceClock.CBaseReferenceClock (Refclock.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ea08e5555aa6286dac80642f19969e6e669a4ec6ccddb4e530d13e0253b4bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954985"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a>Construtor CBaseReferenceClock.CBaseReferenceClock

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pname* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do objeto. Para obter mais informações, [**consulte CBaseObject**](cbaseobject.md).

</dd> <dt>

*Punk* 
</dt> <dd>

Ponteiro para o proprietário desse objeto. Se o objeto for agregado, passe um ponteiro para a interface IUnknown do objeto de agregação. Caso contrário, de definido esse parâmetro como **NULL.**

</dd> <dt>

*Phr* 
</dt> <dd>

Ponteiro para um **valor HRESULT.** Se ocorrer um erro, o método retornará um código de erro nesse parâmetro. Não de definir esse parâmetro como **NULL.**

</dd> <dt>

*pSched* 
</dt> <dd>

Ponteiro para um [**objeto CAMSchedule.**](camschedule.md) Se **NULL**, esse método criará um **novo objeto CAMSchedule.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




