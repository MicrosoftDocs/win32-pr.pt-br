---
title: Mensagem de WM_CAP_EDIT_COPY (VFW. h)
description: A mensagem de cópia de edição da Cap do WM \_ \_ \_ copia o conteúdo do buffer de quadros de vídeo e a paleta associada para a área de transferência. Você pode enviar essa mensagem explicitamente ou usando a macro capEditCopy.
ms.assetid: 16f1dd7d-af4d-4096-add8-eec5f0a0607f
keywords:
- Multimídia do Windows de mensagem WM_CAP_EDIT_COPY
topic_type:
- apiref
api_name:
- WM_CAP_EDIT_COPY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb81c21fc10846adaa113c02b6250bbb35cfff50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085896"
---
# <a name="wm_cap_edit_copy-message"></a>\_Mensagem de \_ cópia de edição do WM Cap \_

A mensagem de cópia de edição da Cap do WM copia o conteúdo do buffer de quadros de vídeo e a paleta associada para a área de transferência. **\_ \_ \_** Você pode enviar essa mensagem explicitamente ou usando a macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) .


```C++
WM_CAP_EDIT_COPY 
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

 

 





