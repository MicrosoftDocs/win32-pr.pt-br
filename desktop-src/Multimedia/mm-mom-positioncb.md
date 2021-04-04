---
title: Mensagem de MM_MOM_POSITIONCB (mmsystem. h)
description: A \_ mensagem mm Mom \_ POSITIONCB é enviada para uma janela quando um \_ evento de retorno de chamada MEVT F \_ é atingido no fluxo de saída de Midi.
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- Multimídia do Windows de mensagem MM_MOM_POSITIONCB
topic_type:
- apiref
api_name:
- MM_MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86fd6f34ab44d307bbbb0e5fc9fd61d083ccda4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918052"
---
# <a name="mm_mom_positioncb-message"></a>\_Mensagem mm Mom \_ POSITIONCB

A mensagem **mm \_ Mom \_ POSITIONCB** é enviada para uma janela quando um evento de retorno de chamada MEVT \_ F \_ é atingido no fluxo de saída de Midi.


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Ponteiro para uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica o evento que causou o retorno de chamada. O membro **dwOffset** fornece o deslocamento do evento.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Reservado Não use.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

A reprodução do buffer de fluxo continua até mesmo durante a execução da função de chamada de retorno. Todos os eventos após o \_ evento de retorno de chamada de MEVT F \_ no buffer serão agendados e enviados no prazo, independentemente de quanto tempo é gasto na função de retorno de chamada.

Se os retornos de chamada de posição estiverem sendo gerados mais rapidamente do que o seu aplicativo pode processá-los, o membro **dwOffset** da estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) poderá se referir a um evento que seu aplicativo ainda não tenha processado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens MIDI](midi-messages.md)
</dt> </dl>

 

