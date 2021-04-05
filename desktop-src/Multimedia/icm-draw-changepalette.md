---
title: Mensagem de ICM_DRAW_CHANGEPALETTE (VFW. h)
description: A \_ mensagem ICM Draw \_ CHANGEPALETTE notifica um driver de renderização que a paleta de filmes está alterando. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawChangePalette.
ms.assetid: 974fc0d8-d0c7-4a82-af84-68b53f753259
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_CHANGEPALETTE
topic_type:
- apiref
api_name:
- ICM_DRAW_CHANGEPALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6364abb2c535158b2e64ff311041b00490c5958c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824500"
---
# <a name="icm_draw_changepalette-message"></a>\_Mensagem de desenho CHANGEPALETTE de ICM \_

A mensagem **ICM \_ draw \_ CHANGEPALETTE** notifica um driver de renderização que a paleta de filmes está alterando. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) .


```C++
ICM_DRAW_CHANGEPALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) que contém o novo formato e a tabela de cores opcional.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna ICERR \_ OK se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Essa mensagem deve ser suportada por manipuladores de renderização instaláveis que redesenham DIBs com uma estrutura interna que inclui uma paleta.

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

 

