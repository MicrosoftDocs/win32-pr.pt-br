---
description: O método Advise despacha todas as solicitações agendadas para um período especificado ou anterior.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: Método CAMSchedule. Advise (Dsschedule. h)
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
ms.openlocfilehash: 70880243cef294ebe747463cd11737027faf9277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758884"
---
# <a name="camscheduleadvise-method"></a>Método CAMSchedule. Advise

O `Advise` método despacha todas as solicitações agendadas para um período especificado ou anterior.

## <a name="syntax"></a>Sintaxe


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*rtTime* \[ referência\]
</dt> <dd>

Valor que especifica o tempo de referência atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o tempo de referência da próxima solicitação de aviso agendada ou o \_ tempo máximo se não houver nenhum restante.

## <a name="remarks"></a>Comentários

Quando o relógio chama esse método, ele especifica o tempo de referência atual. O Agendador determina quais solicitações de aviso expiraram, se houver, e as expedem. Se uma solicitação de uma única expirar, o Agendador a excluirá. Se uma solicitação periódica expirar, o Agendador o agendará novamente para o próximo horário de aviso. O método retorna a hora da próxima solicitação pendente.

Para distribuir uma solicitação de aviso, o Agendador sinaliza o evento ou o semáforo fornecido no parâmetro *hNotify* do método [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dsschedule. h (incluir fluxos. h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




