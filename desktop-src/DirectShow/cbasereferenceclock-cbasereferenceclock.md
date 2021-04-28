---
description: Construtor de CBaseReferenceClock. CBaseReferenceClock-método de construtor.
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: Construtor CBaseReferenceClock. CBaseReferenceClock (Refclock. h)
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
ms.openlocfilehash: 9840bb9d733641ada7c45b0df1470a4150b8ec85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119934"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a>Construtor CBaseReferenceClock. CBaseReferenceClock

Método de construtor.

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

*pName* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do objeto. Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para o proprietário deste objeto. Se o objeto for agregado, passe um ponteiro para a interface IUnknown do objeto de agregação. Caso contrário, defina esse parâmetro como **NULL**.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para um valor **HRESULT** . Se ocorrer um erro, o método retornará um código de erro nesse parâmetro. Não defina esse parâmetro como **NULL**.

</dd> <dt>

*pSched* 
</dt> <dd>

Ponteiro para um objeto [**CAMSchedule**](camschedule.md) . Se for **NULL**, esse método criará um novo objeto **CAMSchedule** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




