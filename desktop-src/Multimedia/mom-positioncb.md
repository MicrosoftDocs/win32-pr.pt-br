---
title: MOM_POSITIONCB mensagem (Mmsystem.h)
description: A mensagem MOM POSITION é enviada quando um evento DE RETORNO DE CHAMADA \_ \_ MEVT F é atingido no fluxo de saída \_ MIDI.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- MOM_POSITIONCB mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d403d9d913628f6b00a7b36dba96d0f4d491f486ef9c3edf7a5c3d5a30c345f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806996"
---
# <a name="mom_positioncb-message"></a>Mensagem MOM \_ POSITIONCB

A **mensagem \_ MOM POSITION** é enviada quando um evento DE RETORNO DE CHAMADA **\_ MEVT F \_** é atingido no fluxo de saída MIDI.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*Dwparam1*
</dt> <dd>

Um ponteiro para uma [**estrutura MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica o buffer de entrada.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*Dwparam2*
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

A reprodução do buffer de fluxo continua mesmo enquanto a função de retorno de chamada está em execução. Todos os eventos após o evento DE RETORNO DE CHAMADA **\_ \_ MEVT F** no buffer serão agendados e enviados no horário, independentemente de quanto tempo é gasto na função de retorno de chamada.

Se os retornos de chamada de posição estão sendo gerados mais rapidamente do que seu aplicativo pode processá-los, o membro **dwOffset** da estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) pode se referir a um evento que seu aplicativo ainda não processou.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens MIDI](midi-messages.md)
</dt> </dl>

 

