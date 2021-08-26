---
description: O método AddAdvisePacket adiciona uma solicitação de aviso à lista de solicitações pendentes.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: Método CAMSchedule. AddAdvisePacket (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.AddAdvisePacket
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9a7509e4696214279e99ff15f21f2634dce7921796ae2ca112ae563ab170a2d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084526"
---
# <a name="camscheduleaddadvisepacket-method"></a>Método CAMSchedule. AddAdvisePacket

O `AddAdvisePacket` método adiciona uma solicitação de aviso à lista de solicitações pendentes.

## <a name="syntax"></a>Sintaxe


```C++
DWORD_PTR AddAdvisePacket(
  [ref] const REFERENCE_TIME &time1,
  [ref] const REFERENCE_TIME &time2,
              HANDLE         hNotify,
              BOOL           bPeriodic
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*time1* \[ referência\]
</dt> <dd>

Hora solicitada para o aviso.

</dd> <dt>

*time2* \[ referência\]
</dt> <dd>

Para solicitações de aviso periódicas, o tempo entre as notificações. Esse parâmetro será ignorado se *bPeriodic* for **false**.

</dd> <dt>

*hNotify* 
</dt> <dd>

Manipule um semáforo se *bPeriodic* for **verdadeiro** ou manipule um evento se *bPeriodic* for **false**.

</dd> <dt>

*bPeriodic* 
</dt> <dd>

Valor booliano que especifica se uma notificação periódica ou uma notificação de uma imagem deve ser adicionada. Se for **true**, a notificação será periódica; o parâmetro *time2* especifica o tempo entre as notificações. Se **for false**, a notificação ocorrerá apenas uma vez.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um identificador para a solicitação de aviso (o "cookie"). Se o método falhar, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dsschedule. h (incluir Fluxos. h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




