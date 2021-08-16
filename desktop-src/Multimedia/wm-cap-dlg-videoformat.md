---
title: Mensagem de WM_CAP_DLG_VIDEOFORMAT (VFW. h)
description: A mensagem do WM \_ Cap \_ DLG \_ VIDEOFORMAT exibe uma caixa de diálogo na qual o usuário pode selecionar o formato de vídeo.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- mensagem de WM_CAP_DLG_VIDEOFORMAT Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbaa58e99c6a07db9109a0b1a6dae25de8abd46fef2631eb539961de16455ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135395"
---
# <a name="wm_cap_dlg_videoformat-message"></a>Mensagem de VIDEOFORMAT do WM \_ Cap \_ DLG \_

A mensagem do **WM \_ Cap \_ DLG \_ VIDEOFORMAT** exibe uma caixa de diálogo na qual o usuário pode selecionar o formato de vídeo. A caixa de diálogo formato de vídeo pode ser usada para selecionar dimensões de imagem, profundidade de bits e opções de compactação de hardware. Você pode enviar essa mensagem explicitamente ou usando a macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) .


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Depois que essa mensagem é retornada, os aplicativos podem precisar atualizar a estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) porque o usuário pode ter alterado as dimensões da imagem.

A caixa de diálogo formato de vídeo é exclusiva para cada driver de captura. Alguns drivers de captura podem não dar suporte a uma caixa de diálogo de formato de vídeo. Os aplicativos podem determinar se o driver de captura dá suporte a essa mensagem verificando o membro **fHasDlgVideoFormat** de [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).

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

 

 





