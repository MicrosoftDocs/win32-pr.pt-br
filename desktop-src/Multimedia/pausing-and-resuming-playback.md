---
title: Pausando e retomando a reprodução
description: Pausando e retomando a reprodução
ms.assetid: f5a7ef22-993c-4aab-bab0-2700289da7a7
keywords:
- Macro MCIWndPause
- Macro MCIWndResume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce70a95000cda6fc471967e5075b16fe7bad837c71eed4e6216ddeaddddc4508
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805966"
---
# <a name="pausing-and-resuming-playback"></a>Pausando e retomando a reprodução

Você pode interromper a reprodução de um dispositivo ou arquivo associado a uma janela do MCIWnd usando a macro [**MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) . Em seguida, você pode reiniciar a reprodução usando a macro [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) . Se o dispositivo não oferecer suporte a resume ou se ocorrer um erro, você poderá usar a macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) para reiniciar a reprodução.

O exemplo a seguir cria uma janela MCIWnd e executa um arquivo AVI. Os comandos de menu pausar e retomar estão disponíveis para que o usuário interrompa e reinicie a reprodução.

Os estilos de janela MCIWnd são alterados temporariamente usando a macro [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) para inibir uma caixa de diálogo de erro MCI de ser exibida se [**MCIWndResume**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) falhar.


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND:             // creates and plays clip 
            g_hwndMCIWnd = MCIWndCreate(hwnd,  
                g_hinst,                      
                WS_CHILD | WS_VISIBLE |    // standard styles
                MCIWNDF_NOPLAYBAR |        // hides toolbar 
                MCIWNDF_NOTIFYMODE,        // notifies of mode changes
                "sample.avi"); 
 
            MCIWndPlay(g_hwndMCIWnd); 
            break;    
        case IDM_PAUSEMCIWND:              // pauses playback 
            MCIWndPause(g_hwndMCIWnd); 
            MessageBox(hwnd, "MCIWnd", "Pausing Playback", MB_OK); 
            break; 
        case IDM_RESUMEMCIWND:          // resumes playback 
            MCIWndChangeStyles(      // hides error dialog messages
                g_hwndMCIWnd,        // MCIWnd window
                MCIWNDF_NOERRORDLG,  // mask of style to change
                MCIWNDF_NOERRORDLG); // suppresses MCI error dialogs 
 
            lResult = MCIWndResume(g_hwndMCIWnd); 
 
            if(lResult){                   // device doesn't resume 
                MessageBox(hwnd, "MCIWnd", 
                    "Resume with Stop and Play", MB_OK); 
                MCIWndStop(g_hwndMCIWnd); 
                MCIWndPlay(g_hwndMCIWnd); 
 
                MCIWndChangeStyles(        // resumes original styles
                    g_hwndMCIWnd, 
                    MCIWNDF_NOERRORDLG, 
                    NULL); 
        } 
        break; 
    } 
    break; 
 
// Handle other messages here. 
```



 

 




