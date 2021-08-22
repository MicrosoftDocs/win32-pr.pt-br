---
title: WM_CAP_SEQUENCE_NOFILE mensagem (Vfw.h)
description: A mensagem WM \_ CAP \_ SEQUENCE \_ NOFILE inicia a captura de vídeo de streaming sem escrever dados em um arquivo. Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureSequenceNoFile.
ms.assetid: 60cbcb62-3bfa-4182-a049-1e3cb2ede423
keywords:
- WM_CAP_SEQUENCE_NOFILE mensagem Windows Multimídia
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
ms.openlocfilehash: 3d9344b53a52caa2e536483a339439a6d942ff1fea0313767d0e1be520c09b48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940724"
---
# <a name="wm_cap_sequence_nofile-message"></a>Mensagem WM \_ CAP \_ SEQUENCE \_ NOFILE

A **mensagem WM CAP SEQUENCE \_ \_ \_ NOFILE** inicia a captura de vídeo de streaming sem escrever dados em um arquivo. Você pode enviar essa mensagem explicitamente ou usando a [**macro capCaptureSequenceNoFile.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile)


```C++
WM_CAP_SEQUENCE_NOFILE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

## <a name="remarks"></a>Comentários

Essa mensagem é útil em conjunto com funções de retorno de chamada de fluxo de vídeo ou waveform-audio stream que permitem que seu aplicativo use os dados de áudio e vídeo diretamente.

Se você quiser alterar os parâmetros que controlam a captura de streaming, use a mensagem [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) antes de iniciar a captura.

Por padrão, a janela de captura não permite que outros aplicativos continuem em execução durante a captura. Para substituir isso, de definir o **membro fYield** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) como **TRUE** ou instalar uma função de retorno de chamada de retorno de chamada de rendimento.

Durante a captura de streaming, a janela de captura pode, opcionalmente, emitir notificações para sua aplicação de tipos específicos de condições. Para instalar procedimentos de retorno de chamada para essas notificações, use as seguintes mensagens:

-   [**ERRO DE RETORNO DE CHAMADA DO WM \_ CAP \_ SET \_ \_**](wm-cap-set-callback-error.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ STATUS**](wm-cap-set-callback-status.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ YIELD**](wm-cap-set-callback-yield.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ VIDEOSTREAM**](wm-cap-set-callback-videostream.md)
-   [**WM \_ CAP \_ SET \_ CALLBACK \_ WAVESTREAM**](wm-cap-set-callback-wavestream.md)

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

 

 





