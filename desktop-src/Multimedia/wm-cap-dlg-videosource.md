---
title: Mensagem de WM_CAP_DLG_VIDEOSOURCE (VFW. h)
description: A \_ mensagem WM Cap \_ DLG \_ Exibir vídeo exibe uma caixa de diálogo na qual o usuário pode controlar a fonte de vídeo.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- mensagem de WM_CAP_DLG_VIDEOSOURCE Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1f05d7e3dc421759229adffa4ecc4b78affc26f1b4244887b017614c2ab4d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803876"
---
# <a name="wm_cap_dlg_videosource-message"></a>Mensagem de vídeo do WM \_ Cap \_ DLG \_

A mensagem **WM \_ Cap DLG exibir \_ \_ vídeo** exibe uma caixa de diálogo na qual o usuário pode controlar a fonte de vídeo. A caixa de diálogo fonte de vídeo pode conter controles que selecionam fontes de entrada; alterar o matiz, o contraste, o brilho da imagem; e modifique a qualidade do vídeo antes de digitalizar as imagens no buffer de quadros. Você pode enviar essa mensagem explicitamente ou usando a macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) .


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A caixa de diálogo fonte de vídeo é exclusiva para cada driver de captura. Alguns drivers de captura podem não dar suporte a uma caixa de diálogo de fonte de vídeo. Os aplicativos podem determinar se o driver de captura dá suporte a essa mensagem verificando o membro **fHasDlgVideoSource** da estrutura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





