---
title: Mensagem de MIM_MOREDATA (mmsystem. h)
description: A mensagem do MIM \_ MOREDATA é enviada para uma função de retorno de chamada de entrada de Midi quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI, mas o aplicativo não está processando mensagens de dados do mim \_ com rapidez suficiente para acompanhar o driver de dispositivo de entrada.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- Multimídia do Windows de mensagem MIM_MOREDATA
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
ms.openlocfilehash: ececb41bc0f9dc0cef187c083afc72ba5fc899a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645257"
---
# <a name="mim_moredata-message"></a>Mensagem do MIM \_ MOREDATA

A mensagem do **mim \_ MOREDATA** é enviada para uma função de retorno de chamada de entrada de Midi quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI, mas o aplicativo não está processando mensagens de [**\_ dados do mim**](mim-data.md) com rapidez suficiente para acompanhar o driver de dispositivo de entrada. A função de retorno de chamada recebe essa mensagem somente quando o aplicativo especifica o \_ status de e/s de Midi \_ na chamada para a função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .


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



| Requisito | Valor |
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

Um aplicativo deve fazer apenas uma quantidade mínima de processamento de \_ mensagens MOREDATA do mim. (Em particular, os aplicativos não devem chamar a função [CreateMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante o processamento do mim \_ MOREDATA.) Em vez disso, o aplicativo deve posicionar os dados de evento em um buffer e, em seguida, retornar.

Quando um aplicativo recebe uma mensagem de [**\_ dados do mim**](mim-data.md) após uma série de mensagens do mim \_ MOREDATA, ele se deparou com eventos de entrada de Midi e pode chamar com segurança funções de uso intensivo de tempo.

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

 

