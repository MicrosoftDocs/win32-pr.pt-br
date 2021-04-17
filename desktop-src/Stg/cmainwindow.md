---
title: CMainWindow
description: O código de exemplo a seguir ilustra esse procedimento.
ms.assetid: a2998232-db71-48ce-b14b-5e17de147172
keywords:
- CMainWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3e9cb538246dfa6931a2f036ba75cab5e962a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105769178"
---
# <a name="cmainwindow"></a><span data-ttu-id="e8708-104">CMainWindow</span><span class="sxs-lookup"><span data-stu-id="e8708-104">CMainWindow</span></span>

<span data-ttu-id="e8708-105">O sistema operacional Microsoft Windows converte as seguintes ações do usuário em mensagens de janela padrão e as envia para o procedimento principal no aplicativo **StoClien** :</span><span class="sxs-lookup"><span data-stu-id="e8708-105">The Microsoft Windows operating system translates the following user actions into standard window messages and sends them to the main procedure in the **StoClien** application:</span></span>

-   <span data-ttu-id="e8708-106">O usuário clica no botão esquerdo do mouse ou na opção de dica de caneta em dispositivos Tablet, para iniciar uma sequência de desenho de linha.</span><span class="sxs-lookup"><span data-stu-id="e8708-106">The user clicks the left mouse button, or the pen tip switch in tablet devices, to initiate a line drawing sequence.</span></span>
-   <span data-ttu-id="e8708-107">O usuário clica e mantém o botão e move o mouse para desenhar uma linha.</span><span class="sxs-lookup"><span data-stu-id="e8708-107">The user clicks and holds the button and moves the mouse to draw a line.</span></span>
-   <span data-ttu-id="e8708-108">A sequência é encerrada quando o botão esquerdo do mouse é liberado.</span><span class="sxs-lookup"><span data-stu-id="e8708-108">The sequence is ended when the left mouse button is released.</span></span>

<span data-ttu-id="e8708-109">O código de exemplo a seguir ilustra esse procedimento.</span><span class="sxs-lookup"><span data-stu-id="e8708-109">The following example code illustrates this procedure.</span></span>

## <a name="cmainwindowwindowproc-stocliencpp"></a><span data-ttu-id="e8708-110">CMainWindow:: WindowProc (STOCLIEN. CPP</span><span class="sxs-lookup"><span data-stu-id="e8708-110">CMainWindow::WindowProc (STOCLIEN.CPP)</span></span>


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



<span data-ttu-id="e8708-111">Uma sequência de desenho de linha é iniciada quando a mensagem do WM \_ LBUTTONDOWN entrega dados de posição do mouse.</span><span class="sxs-lookup"><span data-stu-id="e8708-111">A line drawing sequence starts when the WM\_LBUTTONDOWN message delivers mouse position data.</span></span>

<span data-ttu-id="e8708-112">CMainWindow tem um ponteiro para o objeto CGuiPaper e chama o método [**CGuiPaper:: InkStart**](cguipaper-methods.md) para iniciar a sequência de desenho de linha.</span><span class="sxs-lookup"><span data-stu-id="e8708-112">CMainWindow has a pointer to the CGuiPaper object and calls the [**CGuiPaper::InkStart**](cguipaper-methods.md) method to start the line drawing sequence.</span></span>

<span data-ttu-id="e8708-113">À medida que o mouse é movido para Draw, uma sequência de mensagens do **WM \_ MOUSEMOVE** distintas que contêm dados de posição do mouse são fornecidas para o método [CGuiPaper:: InkDraw](cguipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="e8708-113">As the mouse is moved to draw, a sequence of separate **WM\_MOUSEMOVE** messages that contain mouse position data are provided to the [CGuiPaper::InkDraw](cguipaper-methods.md) method.</span></span>

<span data-ttu-id="e8708-114">Quando o botão esquerdo do mouse é liberado, a mensagem do **WM \_ LBUTTONUP** é recebida.</span><span class="sxs-lookup"><span data-stu-id="e8708-114">When the left mouse button is released, the **WM\_LBUTTONUP** message is received.</span></span> <span data-ttu-id="e8708-115">O método [CGuiPaper:: InkStop](cguipaper-methods.md) interrompe a sequência de desenho de linha.</span><span class="sxs-lookup"><span data-stu-id="e8708-115">The [CGuiPaper::InkStop](cguipaper-methods.md) method stops the line drawing sequence.</span></span>

 

 




