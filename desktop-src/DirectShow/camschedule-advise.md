---
description: O método Advise expedi todas as solicitações agendadas para um horário especificado ou anterior.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: Método CAMSchedule.Advise (Dsschedule.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Advise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0943479aaa7fe2e6d699bba147977a73f48fc31186fb64ea26a211e2ea31d8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757786"
---
# <a name="camscheduleadvise-method"></a>Método CAMSchedule.Advise

O `Advise` método expedi todas as solicitações agendadas para um horário especificado ou anterior.

## <a name="syntax"></a>Sintaxe


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rtTime* \[ Ref\]
</dt> <dd>

Valor que especifica a hora de referência atual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o tempo de referência da próxima solicitação de consultoria agendada ou MAX \_ TIME se não houver mais nenhuma.

## <a name="remarks"></a>Comentários

Quando o relógio chama esse método, ele especifica a hora de referência atual. O agendador determina qual solicitação de consultoria expirou, se há, e as envia. Se uma solicitação única expirar, o agendador a excluirá. Se uma solicitação periódica expirar, o agendador a agendará para a próxima hora de consultoria. O método retorna a hora da próxima solicitação pendente.

Para expedir uma solicitação de consultoria, o agendador sinaliza o evento ou semáforo dado no parâmetro *hNotify* do [**método CAMSchedule::AddAdvisePacket.**](camschedule-addadvisepacket.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dsschedule.h (incluir Fluxos.h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




