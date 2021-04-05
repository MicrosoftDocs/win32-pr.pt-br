---
title: Mensagem de ICM_DRAW_GET_PALETTE (VFW. h)
description: A \_ mensagem ICM Draw \_ obter \_ paleta solicita um driver de renderização para retornar uma paleta.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_GET_PALETTE
topic_type:
- apiref
api_name:
- ICM_DRAW_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03f3658d2a2653f940e18e9b82b7cc3d7690ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008983"
---
# <a name="icm_draw_get_palette-message"></a>\_Mensagem de \_ obtenção de \_ paleta do ICM Draw

A mensagem **ICM \_ draw \_ obter \_ paleta** solicita um driver de renderização para retornar uma paleta.


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

O driver deve retornar um dos seguintes: um identificador da paleta que está sendo usada, **nulo** se não tiver um identificador para retornar ou ICERR sem \_ suporte se não oferecer suporte a paletas.

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

 

 





