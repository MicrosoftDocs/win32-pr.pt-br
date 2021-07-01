---
title: MIM_MOREDATA mensagem (Mmsystem.h)
description: A mensagem MIM MOREDATA é enviada para uma função de retorno de chamada de entrada MIDI quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI, mas o aplicativo não está processando mensagens MIM DATA rápido o suficiente para acompanhar o driver de dispositivo de \_ \_ entrada.
ms.assetid: 74ed46ab-a18e-4df5-bf36-ab3dec7fafa5
keywords:
- MIM_MOREDATA mensagem Multimídia do Windows
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
ms.openlocfilehash: c6342823e13a085b377a3e71f28a0f9ff016681c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119401"
---
# <a name="mim_moredata-message"></a>Mensagem MIM \_ MOREDATA

A **mensagem MIM \_ MOREDATA** é enviada para uma função de retorno de chamada de entrada MIDI quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI, mas o aplicativo não está processando mensagens [**MIM \_ DATA**](mim-data.md) rápido o suficiente para acompanhar o driver de dispositivo de entrada. A função de retorno de chamada recebe essa mensagem somente quando o aplicativo especifica o STATUS de E/S MIDI na chamada para a \_ \_ função [**midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)


```C++
MIM_MOREDATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

Especifica a mensagem MIDI recebida. A mensagem é empacotada em um **valor DWORD** da seguinte forma:



| Requisito | Valor | Descrição |
|-----------|-----------------|-----------------------------------------------------|
| Palavra alta | Byte de ordem alta | Não usado.                                           |
|           | Byte de baixa ordem  | Contém um segundo byte de dados MIDI (quando necessário).  |
| Palavra baixa  | Byte de ordem alta | Contém o primeiro byte de dados MIDI (quando necessário). |
|           | Byte de baixa ordem  | Contém o status MIDI.                           |



 

Os dois bytes de dados MIDI são opcionais, dependendo do byte de status MIDI.

</dd> <dt>

<span id="dwTimestamp"></span><span id="dwtimestamp"></span><span id="DWTIMESTAMP"></span>*dwTimestamp*
</dt> <dd>

Especifica a hora em que a mensagem foi recebida pelo driver de dispositivo de entrada. O carimbo de data/hora é especificado em milissegundos, começando em 0 quando a [**função midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) foi chamada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Um aplicativo deve fazer apenas uma quantidade mínima de processamento de mensagens MIM \_ MOREDATA. (Em particular, os aplicativos não devem chamar a [função PostMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante o processamento do MIM \_ MOREDATA.) Em vez disso, o aplicativo deve colocar os dados do evento em um buffer e, em seguida, retornar.

Quando um aplicativo recebe uma mensagem [**MIM \_ DATA**](mim-data.md) após uma série de mensagens MIM MOREDATA, ele foi atualizado com eventos MIDI de entrada e pode chamar funções com uso intensivo \_ de tempo com segurança.

As mensagens MIDI recebidas de uma porta de entrada MIDI têm o status de execução desabilitado; cada mensagem é expandida para incluir o byte de status MIDI.

Essa mensagem não é enviada quando uma mensagem exclusiva do sistema MIDI é recebida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (inclua Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MIDI (Instrument Digital Interface)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Mensagens MIDI](midi-messages.md)
</dt> </dl>

 

