---
title: Mensagem de MM_MIM_DATA (mmsystem. h)
description: a \_ mensagem MM MIM \_ dados é enviada para uma janela quando uma mensagem midi completa é recebida por um dispositivo de entrada midi.
ms.assetid: 9c580e48-78f3-4914-bdea-393823fb8482
keywords:
- mensagem de MM_MIM_DATA Windows multimídia
topic_type:
- apiref
api_name:
- MM_MIM_DATA
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4309149c8b69fd4396de3a4e67ab18c49008dd7051ed52d4fe992867d1262fe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807376"
---
# <a name="mm_mim_data-message"></a>MM \_ MIM \_ mensagem de dados

a mensagem **MM \_ MIM \_ dados** é enviada para uma janela quando uma mensagem midi completa é recebida por um dispositivo de entrada midi.


```C++
MM_MIM_DATA 
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

Mensagem MIDI recebida. A mensagem é empacotada em um valor de doubleword da seguinte maneira:



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

 

 





