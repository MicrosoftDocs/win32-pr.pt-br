---
title: Gravando com controles MCIWnd
description: Gravando com controles MCIWnd
ms.assetid: 65a57400-aeea-4a27-8d51-37d3d9e9bd55
keywords:
- Função MCIWndCreate
- Macro MCIWndNew
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a02dfd62985b0267c685e6893512f977340f47f95801e8821d46005d5371397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805556"
---
# <a name="recording-with-mciwnd-controls"></a>Gravando com controles MCIWnd

O exemplo a seguir registra áudio de forma de onda usando os controles internos da janela MCIWnd. O exemplo cria uma janela MCIWnd usando o estilo de \_ janela de registro MCIWNDF com a função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) para adicionar um botão de **registro** à barra de ferramentas. A macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) indica que um novo arquivo está associado à janela MCIWnd e que um dispositivo de forma de onda-áudio fornecerá seu conteúdo. Um segundo comando de menu, \_ a IDM SAVEMCIWND, permite que o usuário salve a gravação e selecione um nome de arquivo usando a macro [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .


```C++
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, 
            WS_VISIBLE | MCIWNDF_RECORD, NULL); 
        MCIWndNew(g_hwndMCIWnd, "waveaudio"); 
        break;    
    case IDM_SAVEMCIWND: 
        MCIWndSaveDialog(g_hwndMCIWnd); 
        break; 
    } 
```



 

 




