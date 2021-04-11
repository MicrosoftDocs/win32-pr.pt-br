---
title: Automatizando a reprodução para MCIWnd
description: Automatizando a reprodução para MCIWnd
ms.assetid: 7e38e8b1-f56d-4008-83a7-4fba8333e328
keywords:
- Macro MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b9224cfa4f5a93488f226d1aefa83201b8b0637
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292723"
---
# <a name="automating-playback-for-mciwnd"></a><span data-ttu-id="0f46b-104">Automatizando a reprodução para MCIWnd</span><span class="sxs-lookup"><span data-stu-id="0f46b-104">Automating Playback for MCIWnd</span></span>

<span data-ttu-id="0f46b-105">Você pode automatizar a reprodução para MCIWnd especificando determinados estilos de janela na função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) .</span><span class="sxs-lookup"><span data-stu-id="0f46b-105">You can automate playback for MCIWnd by specifying certain window styles in the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function.</span></span> <span data-ttu-id="0f46b-106">Para reproduzir o dispositivo, a janela precisa de uma janela pai para processar mensagens de notificação, uma área de reprodução para reproduzir arquivos AVI e notificação de alterações no modo de dispositivo para identificar quando a reprodução é interrompida.</span><span class="sxs-lookup"><span data-stu-id="0f46b-106">To play the device, the window needs a parent window to process notification messages, a playback area to play AVI files, and notification of device mode changes to identify when playback stops.</span></span> <span data-ttu-id="0f46b-107">A janela não precisa de uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="0f46b-107">The window does not need a toolbar.</span></span> <span data-ttu-id="0f46b-108">Você pode definir essas características especificando os estilos apropriados em **MCIWndCreate**.</span><span class="sxs-lookup"><span data-stu-id="0f46b-108">You can set these characteristics by specifying the appropriate styles in **MCIWndCreate**.</span></span>

<span data-ttu-id="0f46b-109">O exemplo a seguir usa comandos de menu para criar uma janela MCIWnd para reproduzir conteúdo de vários tipos diferentes de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="0f46b-109">The following example uses menu commands to create an MCIWnd window to play content from several different types of devices.</span></span> <span data-ttu-id="0f46b-110">A função **MCIWndCreate** cria a janela MCIWnd, e os dispositivos e arquivos são carregados usando a macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) nos comandos específicos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0f46b-110">The **MCIWndCreate** function creates the MCIWnd window, and devices and files are loaded by using the [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) macro in the device-specific commands.</span></span> <span data-ttu-id="0f46b-111">Quando um dispositivo termina de ser reproduzido, você fecha o dispositivo interceptando a mensagem [**MCIWNDM \_ notifymode**](mciwndm-notifymode.md) e emitindo a macro [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) .</span><span class="sxs-lookup"><span data-stu-id="0f46b-111">When a device finishes playing, you close the device by trapping the [**MCIWNDM\_NOTIFYMODE**](mciwndm-notifymode.md) message and issuing the [**MCIWndClose**](/windows/desktop/api/Vfw/nf-vfw-mciwndclose) macro.</span></span>


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



 

 




