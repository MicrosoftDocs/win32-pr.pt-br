---
title: Mensagem de ICM_DRAW_RENDERBUFFER (VFW. h)
description: A \_ mensagem ICM Draw \_ RENDERBUFFER notifica um driver de renderização para desenhar os quadros que foram passados para ele. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawRenderBuffer.
ms.assetid: b21be12c-b8a5-49ea-b6b3-d2eb0077a8e9
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_RENDERBUFFER
topic_type:
- apiref
api_name:
- ICM_DRAW_RENDERBUFFER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb02a1fbe334547b9679970ac7598df23237f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918916"
---
# <a name="icm_draw_renderbuffer-message"></a>\_Mensagem de desenho RENDERBUFFER de ICM \_

A mensagem **ICM \_ draw \_ RENDERBUFFER** notifica um driver de renderização para desenhar os quadros que foram passados para ele. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) .


```C++
ICM_DRAW_RENDERBUFFER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Use essa mensagem com hardware que executa sua própria descompactação assíncrona, tempo e desenho.

Essa mensagem é normalmente usada para executar uma operação de busca quando o driver deve ser especificamente instruído para exibir cada quadro de vídeo passado para ele, em vez de reproduzir uma sequência de quadros de vídeo.

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

 

 





