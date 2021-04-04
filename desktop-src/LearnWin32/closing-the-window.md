---
title: Fechando a janela
description: Quando o usuário fecha uma janela, essa ação dispara uma sequência de mensagens de janela.
ms.assetid: f0449f11-0569-4a3a-92bc-bced7e0db516
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6422966d6b0351654632a1c77b7ebf07e2b5ffef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823773"
---
# <a name="closing-the-window"></a>Fechando a janela

Quando o usuário fecha uma janela, essa ação dispara uma sequência de mensagens de janela.

O usuário pode fechar uma janela de aplicativo clicando no botão **fechar** ou usando um atalho de teclado, como Alt + F4. Qualquer uma dessas ações faz com que a janela receba uma mensagem de [**\_ fechamento do WM**](/windows/desktop/winmsg/wm-close) . A mensagem de **\_ fechamento do WM** lhe dá a oportunidade de solicitar o usuário antes de fechar a janela. Se você realmente quiser fechar a janela, chame a função [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) . Caso contrário, basta retornar zero da mensagem de **\_ fechamento do WM** e o sistema operacional irá ignorar a mensagem e não destruir a janela.

Aqui está um exemplo de como um programa pode manipular o [**WM \_ Close**](/windows/desktop/winmsg/wm-close).

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

Neste exemplo, a função [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) mostra uma caixa de diálogo modal que contém os botões **OK** e **Cancelar** . Se o usuário clicar em **OK**, o programa chamará [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow). Caso contrário, se o usuário clicar em **Cancelar**, a chamada para **DestroyWindow** será ignorada e a janela permanecerá aberta. Em ambos os casos, retorna zero para indicar que você tratou a mensagem.

Se você quiser fechar a janela sem avisar o usuário, basta chamar [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) sem a chamada para [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox). No entanto, há um atalho nesse caso. Lembre-se de que o [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) executa a ação padrão para qualquer mensagem de janela. No caso do [**WM, \_ feche**](/windows/desktop/winmsg/wm-close), o **DefWindowProc** chama automaticamente o **DestroyWindow**. Isso significa que se você ignorar a mensagem de **\_ fechamento do WM** em sua instrução **switch** , a janela será destruída por padrão.

Quando uma janela está prestes a ser destruída, ela recebe uma mensagem do [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) . Essa mensagem é enviada depois que a janela é removida da tela, mas antes que a destruição ocorra (em particular, antes de qualquer janela filho ser destruída).

Na janela principal do aplicativo, você normalmente responderá ao [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) chamando [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

Vimos na seção [mensagens de janela](window-messages.md) que [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) coloca uma mensagem do [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) na fila de mensagens, fazendo com que o loop de mensagem termine.

Aqui está um fluxograma que mostra a maneira típica de processar as mensagens do [**WM \_ Close**](/windows/desktop/winmsg/wm-close) e do [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) :

![fluxograma mostrando como tratar mensagens do WM \- Close e do WM \- Destroy](images/wmclose01.png)

## <a name="next"></a>Avançar

[Gerenciando o estado do aplicativo](managing-application-state-.md)