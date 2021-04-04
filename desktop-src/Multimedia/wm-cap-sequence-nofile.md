---
title: Mensagem de WM_CAP_SEQUENCE_NOFILE (VFW. h)
description: A \_ \_ mensagem nofile da sequência do WM Cap inicia a \_ captura de vídeo de streaming sem gravar dados em um arquivo. Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureSequenceNoFile.
ms.assetid: 60cbcb62-3bfa-4182-a049-1e3cb2ede423
keywords:
- Multimídia do Windows de mensagem WM_CAP_SEQUENCE_NOFILE
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE_NOFILE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a08f470989b8000e9757c1cb81924b875b5303
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085237"
---
# <a name="wm_cap_sequence_nofile-message"></a>\_ \_ \_ Mensagem nofile da sequência do WM

A **mensagem \_ \_ \_ nofile da sequência do WM Cap** inicia a captura de vídeo de streaming sem gravar dados em um arquivo. Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) .


```C++
WM_CAP_SEQUENCE_NOFILE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Essa mensagem é útil em conjunto com o fluxo de vídeo ou funções de retorno de chamada de fluxo de áudio de forma de onda que permitem que seu aplicativo use os dados de áudio e vídeo diretamente.

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

 

 





