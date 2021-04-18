---
title: Mensagem de ICM_DRAW_FLUSH (VFW. h)
description: A \_ mensagem de liberação de desenho ICM \_ Notifica um driver de renderização para renderizar o conteúdo de quaisquer buffers de imagem que estão aguardando para serem desenhados. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawFlush.
ms.assetid: c29ed751-c773-4476-98fe-6edef3ff0cf4
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_FLUSH
topic_type:
- apiref
api_name:
- ICM_DRAW_FLUSH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38ec42c51222313f7d3599c3b4f264dbd21a9434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758751"
---
# <a name="icm_draw_flush-message"></a>Mensagem de liberação de \_ desenho ICM \_

A mensagem de **\_ \_ liberação de desenho ICM** notifica um driver de renderização para renderizar o conteúdo de quaisquer buffers de imagem que estão aguardando para serem desenhados. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawFlush**](/windows/desktop/api/Vfw/nf-vfw-icdrawflush) .


```C++
ICM_DRAW_FLUSH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

Essa mensagem é usada somente por hardware que executa sua própria descompactação assíncrona, tempo e desenho.

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

 

 





