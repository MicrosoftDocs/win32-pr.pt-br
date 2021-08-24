---
title: Mensagem de MIM_MOREDATA (mmsystem. h)
description: a MIM \_ mensagem MOREDATA é enviada para uma função de retorno de chamada de entrada de midi quando uma mensagem midi é recebida por um dispositivo de entrada midi, mas o aplicativo não está processando MIM \_ mensagens de dados com rapidez suficiente para acompanhar o driver de dispositivo de entrada.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- mensagem de MIM_MOREDATA Windows multimídia
topic_type:
- apiref
api_name:
- MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 130a07d1d205e9944c7be6ab9ad1294e09d0ebdcdb81d5befc5468ff5a65218f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782966"
---
# <a name="mim_moredata-message"></a>MIM \_ Mensagem MOREDATA

a **MIM mensagem \_ MOREDATA** é enviada para uma função de retorno de chamada de entrada de midi quando uma mensagem midi é recebida por um dispositivo de entrada midi, mas o aplicativo não está processando MIM mensagens de [**\_ dados**](mim-data.md) com rapidez suficiente para acompanhar o driver de dispositivo de entrada. A função de retorno de chamada recebe essa mensagem somente quando o aplicativo especifica o \_ status de e/s de Midi \_ na chamada para a função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

Especifica a mensagem MIDI que foi recebida. A mensagem é empacotada em um valor **DWORD** da seguinte maneira:



| Requisito | Valor | Descrição |
|-----------|-----------------|-----------------------------------------------------|
| Palavra alta | Byte de ordem superior | Não usado.                                           |
|           | Byte de ordem inferior  | Contém um segundo byte de dados MIDI (quando necessário).  |
| Palavra inferior  | Byte de ordem superior | Contém o primeiro byte de dados MIDI (quando necessário). |
|           | Byte de ordem inferior  | Contém o status de MIDI.                           |



 

Os dois bytes de dados MIDI são opcionais, dependendo do byte de status de MIDI.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Especifica a hora em que a mensagem foi recebida pelo driver de dispositivo de entrada. O carimbo de data/hora é especificado em milissegundos, começando em 0 quando a função [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) foi chamada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

um aplicativo deve fazer apenas uma quantidade mínima de processamento de MIM \_ mensagens de MOREDATA. (Em particular, os aplicativos não devem chamar a função [CreateMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante o processamento de mim \_ MOREDATA.) Em vez disso, o aplicativo deve posicionar os dados de evento em um buffer e, em seguida, retornar.

quando um aplicativo recebe uma mensagem de [**\_ dados de MIM**](mim-data.md) após uma série de MIM \_ mensagens MOREDATA, ele foi atualizado com eventos de entrada de MIDI e pode chamar com segurança funções de uso intensivo de tempo.

As mensagens MIDI recebidas de uma porta de entrada MIDI têm o status de execução desabilitado; cada mensagem é expandida para incluir o byte de status de MIDI.

Essa mensagem não é enviada quando uma mensagem exclusiva do sistema MIDI é recebida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MIDI (interface digital de instrumento musical)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Mensagens MIDI](midi-messages.md)
</dt> </dl>

 

