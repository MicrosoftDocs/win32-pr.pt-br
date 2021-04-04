---
title: Captura de vídeo de uma abordagem mínima
description: Captura de vídeo de uma abordagem mínima
ms.assetid: e39ff590-69c0-4927-90c2-786c6082068f
keywords:
- Vídeo para Windows (VFW), captura de vídeo
- VFW (vídeo para Windows), captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a65d5d5bbdc00dfd947c5d917e514d72e3ac069
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823707"
---
# <a name="video-capture-a-minimal-approach"></a>Captura de vídeo: uma abordagem mínima

A captura de vídeo digitaliza um fluxo de dados de áudio e vídeo e o armazena em um disco rígido ou algum outro tipo de dispositivo de armazenamento persistente. Esta seção descreve como adicionar uma forma simples de captura de vídeo a um aplicativo usando três instruções de código. Ele também descreve como terminar ou abortar uma sessão de captura enviando mensagens para a janela de captura.

Uma janela de captura AVICap lida com os detalhes do streaming de áudio e captura de vídeo para arquivos AVI. Isso libera seu aplicativo do envolvimento no formato de arquivo AVI, no gerenciamento do buffer de vídeo e de áudio e no acesso de baixo nível de drivers de dispositivo de áudio e vídeo. O AVICap fornece uma interface flexível para aplicativos. Você pode adicionar a captura de vídeo ao seu aplicativo usando apenas as seguintes linhas de código:


```C++
hWndC = capCreateCaptureWindow ( "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE , 0, 0, 160, 120, hwndParent, nID);

SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0 /* wIndex */, 0L);

SendMessage (hWndC, WM_CAP_SEQUENCE, 0, 0L);
 
```



Também está disponível uma interface de macro que fornece uma alternativa ao uso da função [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) e melhora a legibilidade de um aplicativo. O exemplo a seguir usa a interface de macro para adicionar captura de vídeo a um aplicativo.


```C++
hWndC = capCreateCaptureWindow (   "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE ,   0, 0, 160, 120, hwndParent, nID);

capDriverConnect (hWndC, 0);

capCaptureSequence (hWndC); 
 
```



Depois que o aplicativo cria uma janela de captura da classe de janela AVICap e a conecta a um driver de vídeo, a janela de captura está pronta para capturar dados. Neste ponto, o aplicativo pode simplesmente enviar a mensagem [**de \_ \_ sequência do WM Cap**](wm-cap-sequence.md) (ou a macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) ) para começar a capturar.

Usando as configurações padrão, \_ a \_ sequência de extremidade do WM inicia a captura de vídeo e entrada de áudio para um arquivo chamado CAPTURE.AVI. A captura continua até que ocorra um dos seguintes eventos:

-   O usuário pressiona a tecla ESC ou um botão do mouse.
-   O aplicativo para de ou anula a operação de captura.
-   O disco fica cheio.

Em um aplicativo, você pode parar o streaming de dados capturados em um arquivo enviando a mensagem do [**WM \_ Cap \_ Stop**](wm-cap-stop.md) (ou a macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) ) para uma janela de captura. Você também pode anular a operação de captura enviando a mensagem de [**\_ \_ anulação do WM Cap**](wm-cap-abort.md) (ou a macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) ) para uma janela de captura.

 

 