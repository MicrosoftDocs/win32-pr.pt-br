---
title: WM_CAP_DRIVER_DISCONNECT mensagem (Vfw.h)
description: A mensagem WM \_ CAP \_ DRIVER DISCONNECT \_ desconecta um driver de captura de uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capDriverDisconnect.
ms.assetid: a420f24a-aa7d-4788-9120-2c11e5e2c14c
keywords:
- WM_CAP_DRIVER_DISCONNECT mensagem Windows Multimídia
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
ms.openlocfilehash: f6365366c6ea37b36734262d1d7a8412a7729406ff3fcc12e10ae9ba55d9ba84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803856"
---
# <a name="wm_cap_driver_disconnect-message"></a>Mensagem WM \_ CAP \_ DRIVER \_ DISCONNECT

A **mensagem WM CAP DRIVER \_ \_ \_ DISCONNECT** desconecta um driver de captura de uma janela de captura. Você pode enviar essa mensagem explicitamente ou usando a [**macro capDriverDisconnect.**](/windows/desktop/api/Vfw/nf-vfw-capdriverdisconnect)


```C++
WM_CAP_DRIVER_DISCONNECT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **TRUE** se for bem-sucedido **ou FALSE** se a janela de captura não estiver conectada a um driver de captura.

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

 

 





