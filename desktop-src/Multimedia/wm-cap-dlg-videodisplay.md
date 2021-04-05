---
title: Mensagem de WM_CAP_DLG_VIDEODISPLAY (VFW. h)
description: A mensagem do WM \_ Cap \_ DLG \_ VIDEODISPLAY exibe uma caixa de diálogo na qual o usuário pode definir ou ajustar a saída do vídeo.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- Multimídia do Windows de mensagem WM_CAP_DLG_VIDEODISPLAY
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEODISPLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378d80923f9c0b7eda65fac83809e30626d53406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918417"
---
# <a name="wm_cap_dlg_videodisplay-message"></a>Mensagem de VIDEODISPLAY do WM \_ Cap \_ DLG \_

A mensagem do **WM \_ Cap \_ DLG \_ VIDEODISPLAY** exibe uma caixa de diálogo na qual o usuário pode definir ou ajustar a saída do vídeo. Essa caixa de diálogo pode conter controles que afetam o matiz, o contraste e o brilho da imagem exibida, bem como o alinhamento de cores-chave. Você pode enviar essa mensagem explicitamente ou usando a macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) .


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Os controles nessa caixa de diálogo não afetam os dados de vídeo digitalizados; eles afetam apenas a saída ou a reexibição do sinal de vídeo.

A caixa de diálogo vídeo Display é exclusiva para cada driver de captura. Alguns drivers de captura podem não dar suporte a uma caixa de diálogo de exibição de vídeo. Os aplicativos podem determinar se o driver de captura dá suporte a essa mensagem verificando o membro **fHasDlgVideoDisplay** da estrutura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .

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

 

 





