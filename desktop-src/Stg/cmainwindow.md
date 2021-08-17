---
title: CMainWindow
description: O código de exemplo a seguir ilustra esse procedimento.
ms.assetid: a2998232-db71-48ce-b14b-5e17de147172
keywords:
- CMainWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f67fd2a00bb6f3ab082499e5ca2a4a991a9fb33159a4f43c05923ae393efcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117962463"
---
# <a name="cmainwindow"></a>CMainWindow

o sistema operacional Microsoft Windows converte as seguintes ações do usuário em mensagens de janela padrão e as envia para o procedimento principal no aplicativo **StoClien** :

-   O usuário clica no botão esquerdo do mouse ou na opção de dica de caneta em dispositivos Tablet, para iniciar uma sequência de desenho de linha.
-   O usuário clica e mantém o botão e move o mouse para desenhar uma linha.
-   A sequência é encerrada quando o botão esquerdo do mouse é liberado.

O código de exemplo a seguir ilustra esse procedimento.

## <a name="cmainwindowwindowproc-stocliencpp"></a>CMainWindow:: WindowProc (STOCLIEN. CPP


```C++
LRESULT CMainWindow::WindowProc(
            UINT uMsg,
            WPARAM wParam,
            LPARAM lParam)
  {
    LRESULT lResult = FALSE;

    switch (uMsg)
    {
      case WM_CREATE:
        break;

      case WM_ACTIVATE:
        // A mouse click reactivates the paint procedure.
        // This is used to paint a new window when a user
        // selects a portion of the STOCLIEN window that is 
        // visible beneath another window. This message is  
        // sent in the WindowProc handle.
        if (WA_CLICKACTIVE == LOWORD(wParam))
          m_pGuiPaper->PaintWin();
        lResult = ::DefWindowProc(m_hWnd, uMsg, wParam, lParam);
        break;

      case WM_SIZE:
        // Handle a resize of this window.
        m_wWidth = LOWORD(lParam);
        m_wHeight = HIWORD(lParam);
        // Inform CGuiPaper of the change.
        m_pGuiPaper->Resize(m_wWidth, m_wHeight);
        break;

      case WM_PAINT:
        // This is a message to repaint the window.
        {
          PAINTSTRUCT ps;

          if(BeginPaint(m_hWnd, &ps))
            EndPaint(m_hWnd, &ps);

          m_pGuiPaper->PaintWin();
        }
        break;

      case WM_LBUTTONDOWN:
        // Start sequence of ink drawing to the paper.
        m_pGuiPaper->InkStart(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_MOUSEMOVE:
        // Draw inking sequence data.
        m_pGuiPaper->InkDraw(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_LBUTTONUP:
        // Stop an ink drawing sequence.
        m_pGuiPaper->InkStop(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_COMMAND:
        // Dispatch and handle any Menu command messages received.
        lResult = DoMenu(wParam, lParam);
        break;

      case WM_CHAR:
        if (wParam == 0x1b)
        {
          // Exit this application if user presses the ESC key.
          ::PostMessage(m_hWnd, WM_CLOSE, 0, 0);
        }
        break;

      case WM_CLOSE:
        // The user selected Close on the main window System menu
        // or Exit on the File menu.
        // If there is unsaved ink data, then prompt
        // the user. If the user cancels, do not close the window.
        if (IDCANCEL == m_pGuiPaper->AskSave())
          break;
      case WM_QUIT:
        // When exiting the application, close any associated help
        // windows.
        // ::WinHelp(m_hWnd, m_szHelpFile, HELP_QUIT, 0);
      default:
        // If there are any messages that have not been handled,
        // send them to the default window procedure.
        lResult = ::DefWindowProc(m_hWnd, uMsg, wParam, lParam);
        break;
    }

    return(lResult);
  }
```



Uma sequência de desenho de linha é iniciada quando a mensagem do WM \_ LBUTTONDOWN entrega dados de posição do mouse.

CMainWindow tem um ponteiro para o objeto CGuiPaper e chama o método [**CGuiPaper:: InkStart**](cguipaper-methods.md) para iniciar a sequência de desenho de linha.

À medida que o mouse é movido para Draw, uma sequência de mensagens do **WM \_ MOUSEMOVE** distintas que contêm dados de posição do mouse são fornecidas para o método [CGuiPaper:: InkDraw](cguipaper-methods.md) .

Quando o botão esquerdo do mouse é liberado, a mensagem do **WM \_ LBUTTONUP** é recebida. O método [CGuiPaper:: InkStop](cguipaper-methods.md) interrompe a sequência de desenho de linha.

 

 




