---
title: Monitorando o progresso do Descompactador e o Progresso do Descompactador
description: Monitorando o progresso do Descompactador e o Progresso do Descompactador
ms.assetid: 7c87c688-75b6-4d3e-9dd5-5f509ff2e473
keywords:
- VCM (gerenciador de compactação de vídeo), monitoramento
- VCM (gerenciador de compactação de vídeo), monitoramento
- Função ICSetStatusProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724d3e6a8bee645717ef624eddd1276d3e55e856f1aab3c6edc5f9585b3f5feb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137177"
---
# <a name="monitoring-compressor-and-decompressor-progress"></a>Monitorando o progresso do Descompactador e o Progresso do Descompactador

O exemplo a seguir mostra como a [**função ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) é usada para informar o descompactador ou o descompactador do endereço da função de retorno de chamada:


```C++
ICSetStatusProc(compvars.hic, 0, (LPARAM) (UINT) hwndApp, 
    &PreviewStatusProc); 
 
```



O exemplo a seguir mostra a função de retorno de chamada instalada pelo fragmento anterior:


```C++
LONG CALLBACK export PreviewStatusProc(LPARAM lParam, 
    UINT message, LONG l) 
{ 
    switch (message) 
    { 
        MSG msg; 
        case ICSTATUS_START: 
         
        // Create and display status dialog box. 
         
            break; 
        case ICSTATUS_STATUS: 
            ProSetBarPos((int) l); // sets status bar positions 
 
        // Watch for abort message 
            while(PeekMessage(&msg, NULL, 0, 0, PM_REMOVE)) 
            { 
                if (msg.message == WM_KEYDOWN && msg.wParam == 
                    VK_ESCAPE) 
                    return 1; 
                if (msg.message == WM_SYSCOMMAND && 
                    (msg.wParam & 0xFFF0) == SC_CLOSE) 
                    return 1; 
 
                TranslateMessage(&msg); 
                DispatchMessage(&msg); 
            } 
            break; 
        case ICSTATUS_END: 
         
        // Close and destroy status dialog box. 
         
            break; 
        case ICSTATUS_YIELD: 
         
         
         
            break; 
    } 
    return 0; 
} 
 
```



 

 




