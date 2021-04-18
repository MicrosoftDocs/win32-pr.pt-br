---
title: Mensagem de MM_MOM_CLOSE (mmsystem. h)
description: A \_ mensagem mm Mom \_ Close é enviada para uma janela quando um dispositivo de saída de Midi é fechado.
ms.assetid: 4829bbe5-5103-4354-88a7-37def22e926e
keywords:
- Multimídia do Windows de mensagem MM_MOM_CLOSE
topic_type:
- apiref
api_name:
- MM_MOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae55cbca7c5effc146dee0c5ef9be67469a9201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454741"
---
# <a name="mm_mom_close-message"></a>Mensagem de fechamento do \_ Mom mm \_

A mensagem **mm \_ Mom \_ Close** é enviada para uma janela quando um dispositivo de saída de Midi é fechado.


```C++
MM_MOM_CLOSE 
wParam = (WPARAM) hOutput 
lParam = reserved 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hOutput"></span><span id="houtput"></span><span id="HOUTPUT"></span>*hOutput*
</dt> <dd>

Identificador para o dispositivo de saída de MIDI.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Reservado Não use.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mensagens MIDI](midi-messages.md)
</dt> </dl>

 

 





