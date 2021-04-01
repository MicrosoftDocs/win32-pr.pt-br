---
title: Mensagem de WM_CAP_SEQUENCE (VFW. h)
description: A mensagem de sequência do WM \_ Cap \_ inicia o streaming de vídeo e captura de áudio para um arquivo. Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureSequence.
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- Multimídia do Windows de mensagem WM_CAP_SEQUENCE
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ef945510d0d71f1aa0e0cb5827288a613f5991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918592"
---
# <a name="wm_cap_sequence-message"></a>Mensagem de sequência do WM \_ Cap \_

A mensagem de **\_ \_ sequência do WM Cap** inicia o streaming de vídeo e captura de áudio para um arquivo. Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) .


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.

## <a name="remarks"></a>Comentários

Se você quiser alterar os parâmetros que controlam a captura de fluxo, use a mensagem [**configuração de sequência do WM \_ Cap \_ \_ \_ set**](wm-cap-set-sequence-setup.md) antes de iniciar a captura.

Por padrão, a janela de captura não permite que outros aplicativos continuem em execução durante a captura. Para substituir isso, defina o membro **fYield** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) como **true** ou instale uma função yield callback.

Durante a captura de fluxo, a janela de captura pode, opcionalmente, emitir notificações para seu aplicativo de tipos específicos de condições. Para instalar os procedimentos de retorno de chamada para essas notificações, use as seguintes mensagens:

-   [**\_erro de \_ retorno de \_ chamada de Set Cap \_ do WM**](wm-cap-set-callback-error.md)
-   [**WM \_ Cap \_ definir \_ status de retorno de chamada \_**](wm-cap-set-callback-status.md)
-   [**o \_ \_ retorno de \_ chamada de Set Cap do WM \_**](wm-cap-set-callback-yield.md)
-   [**WM \_ Cap \_ set \_ callback \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md)
-   [**\_WAVESTREAM de \_ retorno de \_ chamada de Set Cap \_ do WM**](wm-cap-set-callback-wavestream.md)

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

 

 





