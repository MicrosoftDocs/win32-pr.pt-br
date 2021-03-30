---
title: Mensagem de ICM_DRAW_END (VFW. h)
description: A mensagem de final do ICM \_ draw \_ Notifica um driver de renderização para descompactar a imagem atual na tela e liberar recursos alocados para descompactação e desenho. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawEnd.
ms.assetid: 03910752-6122-4a5a-84ff-2cecf66cf439
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_END
topic_type:
- apiref
api_name:
- ICM_DRAW_END
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e420ac37791bc6c5aa7f660d71005be65fc87fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644765"
---
# <a name="icm_draw_end-message"></a>Mensagem de final de \_ desenho ICM \_

A mensagem de **\_ \_ final do ICM Draw** notifica um driver de renderização para descompactar a imagem atual na tela e liberar recursos alocados para descompactação e desenho. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawEnd**](/windows/desktop/api/Vfw/nf-vfw-icdrawend) .


```C++
ICM_DRAW_END 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

As mensagens de final [**ICM \_ draw \_ begin**](icm-draw-begin.md) e **ICM \_ draw \_** não são aninhadas. Se o driver receber o **início de ICM e \_ \_ começar** antes que a descompactação seja interrompida com a **\_ \_ extremidade de desenho ICM**, ela deverá reiniciar a descompactação com novos parâmetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





