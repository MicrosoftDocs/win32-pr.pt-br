---
title: Mensagem de MM_MIXM_LINE_CHANGE (mmsystem. h)
description: A \_ mensagem de alteração de linha MIXM mm \_ \_ é enviada por um dispositivo de mixer para notificar um aplicativo de que o estado de uma linha de áudio no dispositivo especificado foi alterado. O aplicativo deve atualizar seus valores de exibição e armazenados em cache para a linha de áudio especificada.
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- mensagem de MM_MIXM_LINE_CHANGE Windows multimídia
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3bd1c122d5e0cf62aa39266da547cd3701e43e6afbf01b853c7d24040504d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373564"
---
# <a name="mm_mixm_line_change-message"></a>\_Mensagem de \_ alteração de linha MIXM mm \_

A mensagem de **\_ \_ \_ alteração de linha MIXM mm** é enviada por um dispositivo de mixer para notificar um aplicativo de que o estado de uma linha de áudio no dispositivo especificado foi alterado. O aplicativo deve atualizar seus valores de exibição e armazenados em cache para a linha de áudio especificada.


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

Identificador para o dispositivo de mixer que enviou a mensagem de notificação.

</dd> <dt>

<span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwLineID*
</dt> <dd>

Identificador de linha para a linha de áudio que tem o estado alterado. Esse identificador é o mesmo que o membro **dwLineID** da estrutura de **mixer** retornada pela função **mixerGetLineInfo**.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um aplicativo deve abrir um dispositivo de mixer e especificar uma janela de retorno de chamada para receber a mensagem de **\_ \_ \_ alteração de linha MIXM mm** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mixers de áudio](audio-mixers.md)
</dt> <dt>

[mensagens de Mixer de áudio](audio-mixer-messages.md)
</dt> </dl>

 

 





