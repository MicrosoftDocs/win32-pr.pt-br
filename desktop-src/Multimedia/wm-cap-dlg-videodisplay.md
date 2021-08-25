---
title: WM_CAP_DLG_VIDEODISPLAY mensagem (Vfw.h)
description: A mensagem WM \_ CAP \_ DLG VIDEODISPLAY exibe uma caixa de diálogo na qual o usuário \_ pode definir ou ajustar a saída do vídeo.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- WM_CAP_DLG_VIDEODISPLAY mensagem Windows Multimídia
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
ms.openlocfilehash: 16afffbf1d3450670b99d26303627771aa4bd3399a252cd16a68bc690012f541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803866"
---
# <a name="wm_cap_dlg_videodisplay-message"></a>Mensagem WM \_ CAP \_ DLG \_ VIDEODISPLAY

A **mensagem WM CAP \_ \_ DLG \_ VIDEODISPLAY** exibe uma caixa de diálogo na qual o usuário pode definir ou ajustar a saída do vídeo. Essa caixa de diálogo pode conter controles que afetam o matiz, o contraste e o brilho da imagem exibida, bem como o alinhamento da cor da chave. Você pode enviar essa mensagem explicitamente ou usando a [**macro capDlgVideoDisplay.**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay)


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

## <a name="remarks"></a>Comentários

Os controles nesta caixa de diálogo não afetam os dados de vídeo digitalizados; eles afetam apenas a saída ou a reprodução do sinal de vídeo.

A caixa de diálogo Exibição de Vídeo é exclusiva para cada driver de captura. Alguns drivers de captura podem não dar suporte a uma caixa de diálogo Exibição de Vídeo. Os aplicativos podem determinar se o driver de captura dá suporte a essa mensagem verificando **o membro fHasDlgVideoDisplay** da estrutura [**CAPDRIVERCAPS.**](/windows/win32/api/vfw/ns-vfw-capdrivercaps)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

 





