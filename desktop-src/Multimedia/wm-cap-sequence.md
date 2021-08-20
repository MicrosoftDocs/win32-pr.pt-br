---
title: WM_CAP_SEQUENCE mensagem (Vfw.h)
description: A mensagem WM \_ CAP SEQUENCE inicia a transmissão de vídeo e captura de áudio para um \_ arquivo. Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureSequence.
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- WM_CAP_SEQUENCE mensagem Windows Multimídia
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
ms.openlocfilehash: 023fd22d79fdfcd1df1f44b2862814ed809fd93c43ab9cd7122414ee1e27db39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800261"
---
# <a name="wm_cap_sequence-message"></a>Mensagem WM \_ CAP \_ SEQUENCE

A **mensagem WM CAP \_ \_ SEQUENCE** inicia a transmissão de vídeo e captura de áudio para um arquivo. Você pode enviar essa mensagem explicitamente ou usando a [**macro capCaptureSequence.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence)


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR,**](wm-cap-set-callback-error.md) a função de retorno de chamada de erro será chamada.

## <a name="remarks"></a>Comentários

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

 

 





