---
title: Mensagem de WM_CAP_DRIVER_DISCONNECT (VFW. h)
description: A \_ mensagem de desconexão do driver do WM Cap \_ \_ desconecta um driver de captura de uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capDriverDisconnect.
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- Multimídia do Windows de mensagem WM_CAP_DRIVER_DISCONNECT
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_DISCONNECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acad628cc61bbb50c56f68fda91ac87be4feb728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918323"
---
# <a name="wm_cap_driver_disconnect-message"></a>\_Mensagem de \_ \_ desconexão do driver do WM Cap

A mensagem de **\_ \_ \_ desconexão do driver do WM Cap desconecta** um driver de captura de uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro [**capDriverDisconnect**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect) .


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** se a janela de captura não estiver conectada a um driver de captura.

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

 

 





