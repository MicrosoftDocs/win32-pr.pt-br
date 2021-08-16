---
title: WIM_OPEN mensagem (Mmsystem.h)
description: A mensagem WIM OPEN é enviada para uma função de retorno de chamada de entrada waveform-audio quando um dispositivo de entrada \_ waveform-audio é aberto.
ms.assetid: de18e6b2-ea28-46d9-812c-e6dac49838ee
keywords:
- WIM_OPEN mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- WIM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337d86c7c1262094993bbac4973b96f1d442149b07d3a48a3e88bd384fee2997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369749"
---
# <a name="wim_open-message"></a>Mensagem WIM \_ OPEN

A **mensagem WIM \_ OPEN** é enviada para uma função de retorno de chamada de entrada waveform-audio quando um dispositivo de entrada waveform-audio é aberto.


```C++
WIM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*Dwparam1*
</dt> <dd>

Reservado; deve ser zero.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*Dwparam2*
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

 

 





