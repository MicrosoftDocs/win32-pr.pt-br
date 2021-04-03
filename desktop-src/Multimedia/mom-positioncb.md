---
title: Mensagem de MOM_POSITIONCB (mmsystem. h)
description: A mensagem de posição do MOM \_ é enviada quando um evento de retorno de chamada de MEVT \_ F \_ é alcançado no fluxo de saída de Midi.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- Multimídia do Windows de mensagem MOM_POSITIONCB
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
ms.openlocfilehash: 3e5c9528e8f91778c53ed4761c98bb67d405ec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645113"
---
# <a name="mom_positioncb-message"></a>Mensagem do MOM \_ POSITIONCB

A mensagem de **\_ posição do MOM** é enviada quando um evento de **retorno de \_ \_ chamada de MEVT F** é alcançado no fluxo de saída de Midi.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Um ponteiro para uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) que identifica o buffer de entrada.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Não usado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

A reprodução do buffer de fluxo continua até mesmo durante a execução da função de chamada de retorno. Todos os eventos após o evento de **\_ retorno de \_ chamada de MEVT F** no buffer serão agendados e enviados no prazo, independentemente de quanto tempo é gasto na função de retorno de chamada.

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

 

