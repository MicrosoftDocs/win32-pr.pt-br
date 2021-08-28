---
title: Mensagem de ICM_DRAW_START (VFW. h)
description: a ICM \_ \_ iniciar mensagem de início notifica um driver de renderização para iniciar seu relógio interno durante o tempo dos quadros de desenho. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawStart.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- mensagem de ICM_DRAW_START Windows multimídia
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
ms.openlocfilehash: 720d8c2f919d2b00955892a42ba8fca95b2b426c3cbb396aa4ac71a5cf912307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690946"
---
# <a name="icm_draw_start-message"></a>ICM \_ DESENHAR \_ mensagem de início

a **ICM \_ \_ iniciar** mensagem de início notifica um driver de renderização para iniciar seu relógio interno durante o tempo dos quadros de desenho. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) .


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Essa mensagem é usada por hardware que executa sua própria descompactação assíncrona, tempo e desenho.

quando o driver recebe essa mensagem, ele deve iniciar a renderização de dados na taxa especificada com a ICM mensagem de [**\_ \_ início de empate**](icm-draw-begin.md) .

as mensagens de **\_ início ICM \_ iniciar** e [**ICM de \_ \_ parada de desenho**](icm-draw-stop.md) não são aninhadas. se o seu driver **receber \_ ICM \_ iniciar início** antes de a renderização ser interrompida com **ICM a \_ \_ parada de desenho**, ela deverá reiniciar a renderização com novos parâmetros.

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

 

 





