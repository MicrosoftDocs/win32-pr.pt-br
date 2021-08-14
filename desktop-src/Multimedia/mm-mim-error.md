---
title: Mensagem de MM_MIM_ERROR (mmsystem. h)
description: a \_ mensagem de erro MM MIM \_ é enviada para uma janela quando uma mensagem MIDI inválida é recebida.
ms.assetid: 03760bfc-a4ef-48cd-97a9-1b93b56fc641
keywords:
- mensagem de MM_MIM_ERROR Windows multimídia
topic_type:
- apiref
api_name:
- MM_MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b2f615434d47a60297991e170a27acd2c6fabefcb5fed0b71624d373a35ed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802414"
---
# <a name="mm_mim_error-message"></a>MM \_ MIM \_ mensagem de erro

a mensagem de **\_ \_ erro MM MIM** é enviada para uma janela quando uma mensagem MIDI inválida é recebida.


```C++
MM_MIM_ERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Identificador para o dispositivo de entrada MIDI que recebeu a mensagem inválida.

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*
</dt> <dd>

Mensagem MIDI inválida. A mensagem é empacotada em um valor **DWORD** com o primeiro byte da mensagem no byte de ordem inferior.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

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

 

 





