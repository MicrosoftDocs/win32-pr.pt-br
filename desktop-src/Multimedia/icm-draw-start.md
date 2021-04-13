---
title: Mensagem de ICM_DRAW_START (VFW. h)
description: A mensagem de início do ICM \_ draw \_ Notifica um driver de renderização para iniciar seu relógio interno durante o tempo dos quadros de desenho. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawStart.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_START
topic_type:
- apiref
api_name:
- ICM_DRAW_START
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538659eb9878be819ee6ec1506403fcce314eb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369528"
---
# <a name="icm_draw_start-message"></a>Mensagem de início do ICM \_ draw \_

A mensagem de **\_ \_ início do ICM Draw** notifica um driver de renderização para iniciar seu relógio interno durante o tempo dos quadros de desenho. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) .


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Essa mensagem é usada por hardware que executa sua própria descompactação assíncrona, tempo e desenho.

Quando o driver recebe essa mensagem, ele deve iniciar a renderização de dados na taxa especificada com a mensagem de [**\_ \_ início de empate de ICM**](icm-draw-begin.md) .

As mensagens de parada do **ICM \_ trace \_ Start** e [**ICM \_ draw \_**](icm-draw-stop.md) não são aninhadas. Se o seu driver receber o **início de ICM e \_ \_ Iniciar** antes que a renderização seja interrompida com a **\_ \_ parada de desenho ICM**, ela deverá reiniciar a renderização com novos parâmetros.

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

 

 





