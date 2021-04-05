---
title: Mensagem de WM_CAP_SINGLE_FRAME (VFW. h)
description: A mensagem do quadro do WM \_ Cap \_ \_ anexa um único quadro a um arquivo de captura que foi aberto usando a \_ mensagem de abertura do quadro do WM Cap \_ \_ \_ . Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureSingleFrame.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- Multimídia do Windows de mensagem WM_CAP_SINGLE_FRAME
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a919036ee38fdcf00f55c3d4044cd3f45bd13c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086362"
---
# <a name="wm_cap_single_frame-message"></a>\_Mensagem de \_ \_ quadro único do WM Cap

A mensagem do **\_ \_ \_ quadro do WM Cap** anexa um único quadro a um arquivo de captura que foi aberto usando a mensagem de [**\_ \_ \_ \_ abertura do quadro do WM Cap**](wm-cap-single-frame-open.md) . Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe) .


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

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

 

 





