---
title: Automatizando a reprodução para MCIWnd
description: Automatizando a reprodução para MCIWnd
ms.assetid: 7e38e8b1-f56d-4008-83a7-4fba8333e328
keywords:
- Macro MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27328367e58ffa21a2f83abe8ecab9d9a4259e6fb61b7b0a36d3104adaea5d9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065596"
---
# <a name="automating-playback-for-mciwnd"></a>Automatizando a reprodução para MCIWnd

Você pode automatizar a reprodução para MCIWnd especificando determinados estilos de janela na função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) . Para reproduzir o dispositivo, a janela precisa de uma janela pai para processar mensagens de notificação, uma área de reprodução para reproduzir arquivos AVI e notificação de alterações no modo de dispositivo para identificar quando a reprodução é interrompida. A janela não precisa de uma barra de ferramentas. Você pode definir essas características especificando os estilos apropriados em **MCIWndCreate**.

O exemplo a seguir usa comandos de menu para criar uma janela MCIWnd para reproduzir conteúdo de vários tipos diferentes de dispositivos. A função **MCIWndCreate** cria a janela MCIWnd, e os dispositivos e arquivos são carregados usando a macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) nos comandos específicos do dispositivo. Quando um dispositivo termina de ser reproduzido, você fecha o dispositivo interceptando a mensagem [**MCIWNDM \_ notifymode**](mciwndm-notifymode.md) e emitindo a macro [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            dwMCIWndStyle = WS_CHILD |     // child window
                WS_VISIBLE |               // visible
                MCIWNDF_NOTIFYMODE |       // notifies of mode changes
                MCIWNDF_NOPLAYBAR;            // hides toolbar 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, dwMCIWndStyle, NULL); 
            break; 
        case IDM_PLAYCDA: 
            LoadNGoMCIWnd(hwnd, "CDAudio"); 
            break; 
        case IDM_PLAYWAVE: 
            LoadNGoMCIWnd(hwnd, "SoundWave.WAV"); 
            break; 
        case IDM_PLAYMIDI: 
            LoadNGoMCIWnd(hwnd, "MIDIFile.MID"); 
            break; 
        case IDM_PLAYAVI: 
            LoadNGoMCIWnd(hwnd, "AVIFile.AVI"); 
            break; 
        case IDM_EXIT: 
            MCIWndDestroy(g_hwndMCIWnd); 
            DestroyWindow(hwnd); 
            break; 
    } 
    break; 
 
case MCIWNDM_NOTIFYMODE: 
    if (lParam == MCI_MODE_STOP)  // device stopped
    { 
        MessageBox(hwnd,"","Closing Device",MB_OK); 
        MCIWndClose(g_hwndMCIWnd); 
    } 
    break; 

// Handle other messages here. 
 
// LoadNGoMCIWnd - automatically loads and plays a multimedia device 
// 
// hwnd -  handle to the parent window 
// lpstr - pointer to device or filename played by device 
// 
// Global variable 
// extern HINSTANCE g_hwndMCIWnd;  instance handle to MCIWnd window 
 
VOID LoadNGoMCIWnd(HWND hwnd, LPSTR lpstr) 
{ 
    MessageBox(hwnd, lpstr, "Loading Device", MB_OK); 
    MCIWndOpen(g_hwndMCIWnd, lpstr, NULL);   // new device in window 
    MCIWndPlay(g_hwndMCIWnd);                // plays device 
} 
```



 

 




