---
title: Mensagem de WOM_CLOSE (mmsystem. h)
description: A \_ mensagem de fechamento wom é enviada para uma função de retorno de chamada de saída de áudio de forma de onda quando um dispositivo de saída de wave-áudio é fechado. O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.
ms.assetid: ac20216a-6a60-4e62-8241-3ca6f33567f1
keywords:
- Multimídia do Windows de mensagem WOM_CLOSE
topic_type:
- apiref
api_name:
- WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a802d6eceed018fa0c25591ee9e4b38708e1787e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759625"
---
# <a name="wom_close-message"></a>WOM \_ fechar mensagem

A mensagem de **\_ fechamento wom** é enviada para uma função de retorno de chamada de saída de áudio de forma de onda quando um dispositivo de saída de wave-áudio é fechado. O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.


```C++
WOM_CLOSE 
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

 

 





