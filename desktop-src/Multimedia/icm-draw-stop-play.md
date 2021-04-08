---
title: Mensagem de ICM_DRAW_STOP_PLAY (VFW. h)
description: A \_ mensagem de parar reprodução do ICM Draw \_ \_ Notifica um driver de renderização quando uma operação de reprodução é concluída. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawStopPlay.
ms.assetid: cfe2ee98-80d0-4554-bcbd-9873769da674
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_STOP_PLAY
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea3964b623c93d452ab7bf9a32c6b9d9b1573fec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086513"
---
# <a name="icm_draw_stop_play-message"></a>\_Mensagem de \_ parada de \_ execução do ICM Draw

A mensagem de **\_ \_ parar \_ reprodução do ICM Draw** notifica um driver de renderização quando uma operação de reprodução é concluída. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawStopPlay**](/windows/desktop/api/Vfw/nf-vfw-icdrawstopplay) .


```C++
ICM_DRAW_STOP_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Use esta mensagem quando a operação de reprodução for concluída. Use a mensagem de [**\_ \_ parada de desenho ICM**](icm-draw-stop.md) para encerrar o tempo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





