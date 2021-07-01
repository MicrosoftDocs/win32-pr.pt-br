---
title: Mensagem de MM_MIM_MOREDATA (mmsystem. h)
description: A \_ mensagem mm mim \_ MOREDATA é enviada para uma janela de retorno de chamada quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI, mas o aplicativo não está processando mensagens de dados do mim \_ rápido o suficiente para acompanhar o driver de dispositivo de entrada.
ms.assetid: 25d507f9-01d4-4a9a-afdd-693d74e3bd22
keywords:
- Multimídia do Windows de mensagem MM_MIM_MOREDATA
topic_type:
- apiref
api_name:
- MM_MIM_MOREDATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3079c537ddca056ca690537c27edd95826de1189
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120021"
---
# <a name="mm_mim_moredata-message"></a>MM \_ mensagem do mim \_ MOREDATA

A mensagem **mm \_ mim \_ MOREDATA** é enviada para uma janela de retorno de chamada quando uma mensagem MIDI é recebida por um dispositivo de entrada MIDI, mas o aplicativo não está processando mensagens de [**\_ dados do mim**](mim-data.md) rápido o suficiente para acompanhar o driver de dispositivo de entrada. A janela recebe essa mensagem somente quando o aplicativo especifica o \_ status de e/s de Midi \_ na chamada para a função [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) .


```C++
MM_MIM_MOREDATA 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Identificador para o dispositivo de entrada MIDI que recebeu a mensagem MIDI.

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*
</dt> <dd>

Especifica a mensagem MIDI que foi recebida. A mensagem é empacotada em um valor de doubleword da seguinte maneira:



| Requisito | Valor | Descrição |
|-----------|-----------------|-----------------------------------------------------|
| Palavra alta | Byte de ordem superior | Não usado.                                           |
|           | Byte de ordem inferior  | Contém um segundo byte de dados MIDI (quando necessário).  |
| Palavra inferior  | Byte de ordem superior | Contém o primeiro byte de dados MIDI (quando necessário). |
|           | Byte de ordem inferior  | Contém o status de MIDI.                           |



 

Os dois bytes de dados MIDI são opcionais, dependendo do byte de status de MIDI.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Se seu aplicativo receber dados de MIDI mais rápido do que pode processá-los, você não deve usar um mecanismo de retorno de chamada de janela. Para maximizar a velocidade, use uma função de retorno de chamada e use a mensagem do [**mim \_ MOREDATA**](mim-moredata.md) em vez de mm \_ MOREDATA do mim \_ .

Um aplicativo deve fazer apenas uma quantidade mínima de processamento de \_ mensagens MOREDATA do mim mm \_ . (Em particular, os aplicativos não devem chamar a função [CreateMessage](/windows/win32/api/winuser/nf-winuser-postmessagea) durante o processamento mm \_ MIM \_ MOREDATA.) Em vez disso, o aplicativo deve posicionar os dados de evento em um buffer e, em seguida, retornar.

Quando um aplicativo recebe uma mensagem de [**\_ \_ dados do mim mm**](mm-mim-data.md) após uma série de mensagens mm do \_ mim \_ MOREDATA, ele se inscreveu em eventos de entrada de Midi e pode chamar com segurança funções com uso intensivo de tempo.

As mensagens MIDI recebidas de uma porta de entrada MIDI têm o status de execução desabilitado; cada mensagem é expandida para incluir o byte de status de MIDI.

Essa mensagem não é enviada quando uma mensagem exclusiva do sistema MIDI é recebida. Não há carimbo de data/hora disponível com esta mensagem. Para dados de entrada com carimbo de data/hora, você deve usar as mensagens que são enviadas para funções de retorno de chamada.

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

 

