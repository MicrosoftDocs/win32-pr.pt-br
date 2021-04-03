---
title: Mensagem de WM_CAP_STOP (VFW. h)
description: A mensagem de parada da Cap do WM \_ \_ interrompe a operação de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureStop.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- Multimídia do Windows de mensagem WM_CAP_STOP
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ded89ea8999fa2b29f576a6d047f5147d492bc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645159"
---
# <a name="wm_cap_stop-message"></a>Mensagem de parada do WM \_ Cap \_

A mensagem de **\_ \_ parada da Cap do WM** interrompe a operação de captura. Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) .

Na captura de quadro da etapa, os dados da imagem coletados antes da mensagem enviada são mantidos no arquivo de captura. Uma duração equivalente de dados de áudio também será retida no arquivo de captura se a captura de áudio tiver sido habilitada.


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A operação de captura deve produzir para usar essa mensagem. Use a mensagem de [**\_ \_ anulação do WM Cap**](wm-cap-abort.md) para abandonar a operação de captura atual.

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

 

 





