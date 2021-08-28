---
title: MM_MIXM_CONTROL_CHANGE mensagem (Mmsystem.h)
description: A mensagem MM MIXM CONTROL CHANGE é enviada por um dispositivo mixer para notificar um aplicativo de que o estado de um controle associado a uma linha \_ \_ de áudio foi \_ alterado. O aplicativo deve atualizar seus valores de exibição e armazenados em cache para o controle especificado.
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- MM_MIXM_CONTROL_CHANGE mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MM_MIXM_CONTROL_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44305a5a441e4d12a1b3f43029ae3a41f7642c13b15a50f74a1acab158c2ed58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807176"
---
# <a name="mm_mixm_control_change-message"></a>Mensagem MM \_ MIXM \_ CONTROL \_ CHANGE

A **mensagem MM \_ MIXM CONTROL \_ \_ CHANGE** é enviada por um dispositivo mixer para notificar um aplicativo de que o estado de um controle associado a uma linha de áudio foi alterado. O aplicativo deve atualizar seus valores de exibição e armazenados em cache para o controle especificado.


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

Manipular para o dispositivo de mixer **(HMIXER)** que enviou a mensagem de notificação.

</dd> <dt>

<span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*Dwcontrolid*
</dt> <dd>

Identificador de controle para o controle de mixer que alterou o estado. Esse identificador é o mesmo que **o membro dwControlID** da estrutura **MIXERCONTROL** retornada pela **função mixerGetLineControls.**

</dd> </dl>

## <a name="remarks"></a>Comentários

Um aplicativo deve abrir um dispositivo mixer e especificar uma janela de retorno de chamada para receber a **mensagem MM \_ MIXM CONTROL \_ \_ CHANGE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mixers de áudio](audio-mixers.md)
</dt> <dt>

[Mensagens Mixer áudio](audio-mixer-messages.md)
</dt> </dl>

 

 





