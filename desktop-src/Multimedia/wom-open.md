---
title: Mensagem de WOM_OPEN (mmsystem. h)
description: A \_ mensagem de abertura wom é enviada para uma função de retorno de chamada de saída de áudio de forma de onda quando um dispositivo de saída de wave-áudio é aberto.
ms.assetid: 7fa175d3-7c07-4ca0-a0bd-4526fbc24f8d
keywords:
- mensagem de WOM_OPEN Windows multimídia
topic_type:
- apiref
api_name:
- WOM_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77d0e145bf533bf9b48b88a87d449679e7728b679e72ed70a787168b5936f5aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940653"
---
# <a name="wom_open-message"></a>WOM \_ Abrir mensagem

A mensagem de **\_ abertura wom** é enviada para uma função de retorno de chamada de saída de áudio de forma de onda quando um dispositivo de saída de wave-áudio é aberto.


```C++
WOM_OPEN 
dwParam1 = reserved 
dwParam2 = reserved 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Reservado deve ser zero.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Reservado deve ser zero.

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

[Áudio de onda](waveform-audio.md)
</dt> <dt>

[Mensagens de formato de onda](waveform-messages.md)
</dt> </dl>

 

 





