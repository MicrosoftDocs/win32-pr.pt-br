---
title: Mensagem de MM_MIXM_CONTROL_CHANGE (mmsystem. h)
description: A \_ mensagem de alteração do controle MIXM mm \_ \_ é enviada por um dispositivo de mixer para notificar um aplicativo de que o estado de um controle associado a uma linha de áudio foi alterado. O aplicativo deve atualizar seus valores de exibição e armazenados em cache para o controle especificado.
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- Multimídia do Windows de mensagem MM_MIXM_CONTROL_CHANGE
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
ms.openlocfilehash: 12daa4d9e107a9ba687331731ee9fd7e6f0dc886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105750583"
---
# <a name="mm_mixm_control_change-message"></a>MM \_ MIXM \_ controle de \_ alteração de mensagem

A mensagem de **\_ \_ \_ alteração do controle MIXM mm** é enviada por um dispositivo de mixer para notificar um aplicativo de que o estado de um controle associado a uma linha de áudio foi alterado. O aplicativo deve atualizar seus valores de exibição e armazenados em cache para o controle especificado.


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hMixer*
</dt> <dd>

Identificador para o dispositivo de mixer (**HMIXER**) que enviou a mensagem de notificação.

</dd> <dt>

<span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwControlID*
</dt> <dd>

Identificador de controle para o controle do mixer que alterou o estado. Esse identificador é o mesmo que o membro **dwControlID** da estrutura **MIXERCONTROL** retornada pela função **mixerGetLineControls**.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um aplicativo deve abrir um dispositivo de mixer e especificar uma janela de retorno de chamada para receber a mensagem de **\_ \_ \_ alteração do controle MIXM mm** .

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

[Mensagens do mixer de áudio](audio-mixer-messages.md)
</dt> </dl>

 

 





