---
title: Criando uma janela MCIWnd
description: Criando uma janela MCIWnd
ms.assetid: bd45e813-5807-43cd-bef1-03285df9a018
keywords:
- Janela MCIWnd, criando
- Função MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c205e87acf3e5f529d4b5cc9c9163b7fe887fe04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789759"
---
# <a name="creating-an-mciwnd-window"></a>Criando uma janela MCIWnd

A função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) registra e cria uma janela MCIWnd. A janela pode ser uma janela pai, filho ou pop-up. O exemplo a seguir cria uma janela MCIWnd como uma janela filho e permite que o controle de usuário seja reproduzido fornecendo acesso aos botões TrackBar e **Play**, **Stop** e **menu** . O exemplo especifica um identificador de uma janela pai e especifica **NULL** para os estilos de janela, de modo que os estilos de janela padrão de WS \_ Child, WS \_ Border e WS \_ Visible são usados para criar a janela MCIWnd.


```C++
// Global variable and constants 
// extern HINSTANCE g_hinst;       instance handle 
// extern HWND g_hwndMCIWnd;       MCIWnd window handle 
 
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, NULL, 
            "sample.avi"); 
        break;    
    } 
    break; 
```



> [!Note]  
> Você também pode especificar **NULL** para o identificador de janela pai e os estilos de janela; nesse caso, os estilos de janela padrão seriam WS \_ Overlapped e WS \_ Visible.

 

 

 




