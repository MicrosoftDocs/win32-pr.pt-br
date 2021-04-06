---
title: Personalizando o processo de gravação
description: Personalizando o processo de gravação
ms.assetid: 9453b9d3-ae9c-4f57-8dd6-f84b9a76618e
keywords:
- Função MCIWndCreate
- Macro MCIWndNew
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec46f61ef4624ba613025f01b081ccc1ebda1cad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916246"
---
# <a name="customizing-the-recording-process"></a>Personalizando o processo de gravação

Você pode personalizar o processo de gravação, assumindo controle total da maioria das coisas — desde a criação da janela MCIWnd até a gravação das informações gravadas em um arquivo. O exemplo a seguir consulta o dispositivo MCI para gravar e salvar recursos e inclui comandos de menu para gravar no início ou no final do conteúdo.

O exemplo a seguir usa a função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) para criar uma nova janela e permite que você especifique um arquivo existente para armazenar os dados gravados e a macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) para associar um novo arquivo à janela. Como alternativa, você pode usar a macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) ou [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) para especificar um arquivo.

O exemplo usa a macro [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) para verificar se o dispositivo pode gravar e a macro [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) para verificar se o dispositivo salvou as informações. O exemplo define a posição de reprodução atual usando as macros [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) e [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend) . O exemplo inicia a gravação usando a macro [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) . Depois que as informações são registradas, o exemplo a salva usando a macro [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate( hwnd, g_hinst, 
                WS_VISIBLE | WS_CHILD | 
                MCIWNDF_RECORD,                   // add Record button
                NULL ); 
 
            MCIWndNew(g_hwndMCIWnd, "waveaudio"); // new file 
 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MessageBox( hwnd, 
                "Press the red button on the toolbar to record.", 
                "MCIWnd Record", 
                MB_OK ); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK ); 
            } 
            break; 
        case IDM_RECORDATSTART: 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MCIWndHome(g_hwndMCIWnd); 
                MCIWndRecord(g_hwndMCIWnd); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK); 
            } 
            break; 
        case IDM_RECORDATEND: 
            if( MCIWndCanRecord(g_hwndMCIWnd) ) 
            { 
                MCIWndEnd(g_hwndMCIWnd); 
                MCIWndRecord(g_hwndMCIWnd); 
            } 
            else 
            { 
                MessageBox( hwnd, 
                    "This device doesn't record.", 
                    "MCIWnd Record", 
                    MB_OK); 
            } 
            break; 
        case IDM_SAVEMCIWND: 
            if( MCIWndCanSave(g_hwndMCIWnd) ) 
                MCIWndSaveDialog(g_hwndMCIWnd); 
    } 
    break; 
 
    // Handle other messages here. 
```



 

 




