---
title: Mensagem de MM_WOM_CLOSE (mmsystem. h)
description: A \_ mensagem mm wom \_ fechar é enviada para uma janela quando um dispositivo de saída de wave-áudio é fechado. O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.
ms.assetid: 6505b688-88a1-43b2-ad4e-2f88e496430a
keywords:
- mensagem de MM_WOM_CLOSE Windows multimídia
topic_type:
- apiref
api_name:
- MM_WOM_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7624c85554fca997ce9542170e370711f8b3c3cefc22cf0e8d2fe9ea3e88687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065446"
---
# <a name="mm_wom_close-message"></a>MM \_ wom \_ fechar mensagem

A mensagem **mm \_ wom \_ Fechar** é enviada para uma janela quando um dispositivo de saída de wave-áudio é fechado. O identificador do dispositivo não é mais válido depois que essa mensagem é enviada.


```C++
MM_WOM_CLOSE 
wParam = (WPARAM) hOutputDev 
lParam = reserved 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="hOutputDev"></span><span id="houtputdev"></span><span id="HOUTPUTDEV"></span>*hOutputDev*
</dt> <dd>

Identificador para o dispositivo que foi fechado.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
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

 

 





