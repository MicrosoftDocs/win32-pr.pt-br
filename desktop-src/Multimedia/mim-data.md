---
title: MIM_DATA mensagem (Mmsystem.h)
description: A MIM DATA é enviada para uma função de retorno de chamada de entrada MIDI quando uma mensagem MIDI é recebida \_ por um dispositivo de entrada MIDI.
ms.assetid: 966aab84-420a-42ce-9989-da5910ced9c0
keywords:
- MIM_DATA mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bebbb9ca6016706605de8fed29e5fa5ebaf6055f4a730fb563323f306606b866
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137285"
---
# <a name="mim_data-message"></a>\_MIM Mensagem DATA

A **MIM \_ data é** enviada para uma função de retorno de chamada de entrada MIDI quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI.


```C++
MIM_DATA 
dwParam1 = dwMidiMessage 
dwParam2 = dwTimestamp 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwMidiMessage"></span><span id="dwmidimessage"></span><span id="DWMIDIMESSAGE"></span>*dwMidiMessage*
</dt> <dd>

Mensagem MIDI recebida. A mensagem é empacotada em um valor doubleword da seguinte forma:



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

Hora em que a mensagem foi recebida pelo driver de dispositivo de entrada. O carimbo de data/hora é especificado em milissegundos, começando em zero quando [**a função midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) foi chamada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

As mensagens MIDI recebidas de uma porta de entrada MIDI têm o status de execução desabilitado; cada mensagem é expandida para incluir o byte de status MIDI.

Essa mensagem não é enviada quando uma mensagem exclusiva do sistema MIDI é recebida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MIDI (Instrument Digital Interface)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[Mensagens MIDI](midi-messages.md)
</dt> </dl>

 

