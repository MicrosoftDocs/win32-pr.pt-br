---
title: Mensagem de WM_CAP_ABORT (VFW. h)
description: A \_ mensagem de anulação da Cap do WM \_ interrompe a operação de captura.
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- Multimídia do Windows de mensagem WM_CAP_ABORT
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2843e3c4d59b62f2b58be20cef63ed0dc2e79d4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499356"
---
# <a name="wm_cap_abort-message"></a>\_Mensagem de anulação de Cap do WM \_

A mensagem de **\_ \_ anulação da Cap do WM** interrompe a operação de captura. No caso da captura de etapa, os dados de imagem coletados até o ponto da mensagem de **\_ \_ anulação de Cap do WM** serão retidos no arquivo de captura, mas o áudio não será capturado. Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) .


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A operação de captura deve produzir para usar essa mensagem.

Use a mensagem de [**\_ \_ parada da Cap do WM**](wm-cap-stop.md) para interromper a captura da etapa na posição atual e, em seguida, capturar áudio.

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

 

 





