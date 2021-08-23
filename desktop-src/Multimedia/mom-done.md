---
title: Mensagem de MOM_DONE (Mciapi. h)
description: A \_ mensagem Mom Done é enviada para uma função de retorno de chamada de saída de Midi quando o buffer especificado exclusivo pelo sistema ou fluxo foi reproduzido e está sendo retornado para o aplicativo.
ms.assetid: 0b9bd0e1-c87d-4f21-912e-5ac9f5c04192
keywords:
- mensagem de MOM_DONE Windows multimídia
topic_type:
- apiref
api_name:
- MOM_DONE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b4361ef25af7bab629138d4371c852d661373891e9d9513ae30b8ad79e97670
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807026"
---
# <a name="mom_done-message"></a>Mensagem do MOM \_ concluída

A mensagem **Mom \_ Done** é enviada para uma função de retorno de chamada de saída de Midi quando o buffer especificado exclusivo pelo sistema ou fluxo foi reproduzido e está sendo retornado para o aplicativo.


```C++
MOM_DONE 
dwParam1 = (DWORD) lpMidiHdr 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Ponteiro para uma estrutura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) identificando o buffer.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Reservado Não use.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens MIDI](midi-messages.md)
</dt> </dl>

 

