---
title: MM_WOM_OPEN mensagem (Mmsystem.h)
description: A mensagem MM WOM OPEN é enviada para uma janela quando o dispositivo de saída de áudio de forma de onda \_ \_ determinado é aberto.
ms.assetid: 1b0366de-61cd-4203-9173-ababaefdb153
keywords:
- MM_WOM_OPEN mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MM_WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e770d03b847352152846d1095bc528bff8e8eacbcdbb1c9fc46450d21dc185bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065396"
---
# <a name="mm_wom_open-message"></a>Mensagem \_ MM WOM \_ OPEN

A **mensagem MM \_ WOM \_ OPEN** é enviada para uma janela quando o dispositivo de saída de áudio de forma de onda determinado é aberto.


```C++
MM_WOM_OPEN 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Lidar com o dispositivo que foi aberto.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Reservado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Waveform Audio](waveform-audio.md)
</dt> <dt>

[Mensagens de forma de onda](waveform-messages.md)
</dt> </dl>

 

 





