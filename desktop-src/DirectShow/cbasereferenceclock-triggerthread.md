---
description: O método TriggerThread ativa o thread de trabalho que lida com o agendamento.
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: Método CBaseReferenceClock. TriggerThread (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.TriggerThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8b53af246e029b5142b68840cfde0e776208e3c51093438042dd74f42a1b3a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076436"
---
# <a name="cbasereferenceclocktriggerthread-method"></a>Método CBaseReferenceClock. TriggerThread

O `TriggerThread` método ativa o thread de trabalho que lida com o agendamento.

## <a name="syntax"></a>Sintaxe


```C++
void TriggerThread();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O relógio usa um thread de trabalho que chama o método [**CAMSchedule:: Advise**](camschedule-advise.md) em momentos apropriados. A classe derivada pode chamar `TriggerThread` para ativar o thread.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Refclock. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> </dl>

 

 




