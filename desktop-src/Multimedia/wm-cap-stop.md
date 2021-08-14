---
title: WM_CAP_STOP mensagem (Vfw.h)
description: A mensagem WM \_ CAP STOP interrompe a operação de \_ captura. Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureStop.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- WM_CAP_STOP mensagem Windows Multimídia
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
ms.openlocfilehash: 8bceac7a821a42227a388de6ebc2b9ea548156ec80d1e5baba7f1e1ad708002d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118369325"
---
# <a name="wm_cap_stop-message"></a>Mensagem WM \_ CAP \_ STOP

A **mensagem WM CAP \_ \_ STOP** interrompe a operação de captura. Você pode enviar essa mensagem explicitamente ou usando a [**macro capCaptureStop.**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop)

Na captura de quadro de etapa, os dados de imagem coletados antes que essa mensagem foi enviada são retidos no arquivo de captura. Uma duração equivalente dos dados de áudio também será mantida no arquivo de captura se a captura de áudio tiver sido habilitada.


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

## <a name="remarks"></a>Comentários

A operação de captura deve produzir para usar essa mensagem. Use a [**mensagem WM \_ CAP \_ ABORT**](wm-cap-abort.md) para abandonar a operação de captura atual.

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

 

 





