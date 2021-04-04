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
# <a name="closing-the-window"></a><span data-ttu-id="4c0b8-103">Fechando a janela</span><span class="sxs-lookup"><span data-stu-id="4c0b8-103">Closing the Window</span></span>

<span data-ttu-id="4c0b8-104">Quando o usuário fecha uma janela, essa ação dispara uma sequência de mensagens de janela.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-104">When the user closes a window, that action triggers a sequence of window messages.</span></span>

<span data-ttu-id="4c0b8-105">O usuário pode fechar uma janela de aplicativo clicando no botão **fechar** ou usando um atalho de teclado, como Alt + F4.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-105">The user can close an application window by clicking the **Close** button, or by using a keyboard shortcut such as ALT+F4.</span></span> <span data-ttu-id="4c0b8-106">Qualquer uma dessas ações faz com que a janela receba uma mensagem de [**\_ fechamento do WM**](/windows/desktop/winmsg/wm-close) .</span><span class="sxs-lookup"><span data-stu-id="4c0b8-106">Any of these actions causes the window to receive a [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close) message.</span></span> <span data-ttu-id="4c0b8-107">A mensagem de **\_ fechamento do WM** lhe dá a oportunidade de solicitar o usuário antes de fechar a janela.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-107">The **WM\_CLOSE** message gives you an opportunity to prompt the user before closing the window.</span></span> <span data-ttu-id="4c0b8-108">Se você realmente quiser fechar a janela, chame a função [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) .</span><span class="sxs-lookup"><span data-stu-id="4c0b8-108">If you really do want to close the window, call the [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) function.</span></span> <span data-ttu-id="4c0b8-109">Caso contrário, basta retornar zero da mensagem de **\_ fechamento do WM** e o sistema operacional irá ignorar a mensagem e não destruir a janela.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-109">Otherwise, simply return zero from the **WM\_CLOSE** message, and the operating system will ignore the message and not destroy the window.</span></span>

<span data-ttu-id="4c0b8-110">Aqui está um exemplo de como um programa pode manipular o [**WM \_ Close**](/windows/desktop/winmsg/wm-close).</span><span class="sxs-lookup"><span data-stu-id="4c0b8-110">Here is an example of how a program might handle [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close).</span></span>

```C++
case WM_CLOSE:
    if (MessageBox(hwnd, L"Really quit?", L"My application", MB_OKCANCEL) == IDOK)
    {
        DestroyWindow(hwnd);
    }
    // Else: User canceled. Do nothing.
    return 0;
```

<span data-ttu-id="4c0b8-111">Neste exemplo, a função [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) mostra uma caixa de diálogo modal que contém os botões **OK** e **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="4c0b8-111">In this example, the [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) function shows a modal dialog that contains **OK** and **Cancel** buttons.</span></span> <span data-ttu-id="4c0b8-112">Se o usuário clicar em **OK**, o programa chamará [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow).</span><span class="sxs-lookup"><span data-stu-id="4c0b8-112">If the user clicks **OK**, the program calls [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow).</span></span> <span data-ttu-id="4c0b8-113">Caso contrário, se o usuário clicar em **Cancelar**, a chamada para **DestroyWindow** será ignorada e a janela permanecerá aberta.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-113">Otherwise, if the user clicks **Cancel**, the call to **DestroyWindow** is skipped, and the window remains open.</span></span> <span data-ttu-id="4c0b8-114">Em ambos os casos, retorna zero para indicar que você tratou a mensagem.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-114">In either case, return zero to indicate that you handled the message.</span></span>

<span data-ttu-id="4c0b8-115">Se você quiser fechar a janela sem avisar o usuário, basta chamar [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) sem a chamada para [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).</span><span class="sxs-lookup"><span data-stu-id="4c0b8-115">If you want to close the window without prompting the user, you could simply call [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) without the call to [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox).</span></span> <span data-ttu-id="4c0b8-116">No entanto, há um atalho nesse caso.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-116">However, there is a shortcut in this case.</span></span> <span data-ttu-id="4c0b8-117">Lembre-se de que o [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) executa a ação padrão para qualquer mensagem de janela.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-117">Recall that [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) executes the default action for any window message.</span></span> <span data-ttu-id="4c0b8-118">No caso do [**WM, \_ feche**](/windows/desktop/winmsg/wm-close), o **DefWindowProc** chama automaticamente o **DestroyWindow**.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-118">In the case of [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close), **DefWindowProc** automatically calls **DestroyWindow**.</span></span> <span data-ttu-id="4c0b8-119">Isso significa que se você ignorar a mensagem de **\_ fechamento do WM** em sua instrução **switch** , a janela será destruída por padrão.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-119">That means if you ignore the **WM\_CLOSE** message in your **switch** statement, the window is destroyed by default.</span></span>

<span data-ttu-id="4c0b8-120">Quando uma janela está prestes a ser destruída, ela recebe uma mensagem do [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) .</span><span class="sxs-lookup"><span data-stu-id="4c0b8-120">When a window is about to be destroyed, it receives a [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) message.</span></span> <span data-ttu-id="4c0b8-121">Essa mensagem é enviada depois que a janela é removida da tela, mas antes que a destruição ocorra (em particular, antes de qualquer janela filho ser destruída).</span><span class="sxs-lookup"><span data-stu-id="4c0b8-121">This message is sent after the window is removed from the screen, but before the destruction occurs (in particular, before any child windows are destroyed).</span></span>

<span data-ttu-id="4c0b8-122">Na janela principal do aplicativo, você normalmente responderá ao [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) chamando [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).</span><span class="sxs-lookup"><span data-stu-id="4c0b8-122">In your main application window, you will typically respond to [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) by calling [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage).</span></span>

```C++
case WM_DESTROY:
    PostQuitMessage(0);
    return 0;
```

<span data-ttu-id="4c0b8-123">Vimos na seção [mensagens de janela](window-messages.md) que [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) coloca uma mensagem do [**WM \_ Quit**](/windows/desktop/winmsg/wm-quit) na fila de mensagens, fazendo com que o loop de mensagem termine.</span><span class="sxs-lookup"><span data-stu-id="4c0b8-123">We saw in the [Window Messages](window-messages.md) section that [**PostQuitMessage**](/windows/desktop/api/winuser/nf-winuser-postquitmessage) puts a [**WM\_QUIT**](/windows/desktop/winmsg/wm-quit) message on the message queue, causing the message loop to end.</span></span>

<span data-ttu-id="4c0b8-124">Aqui está um fluxograma que mostra a maneira típica de processar as mensagens do [**WM \_ Close**](/windows/desktop/winmsg/wm-close) e do [**WM \_ Destroy**](/windows/desktop/winmsg/wm-destroy) :</span><span class="sxs-lookup"><span data-stu-id="4c0b8-124">Here is a flow chart showing the typical way to process [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close) and [**WM\_DESTROY**](/windows/desktop/winmsg/wm-destroy) messages:</span></span>

![fluxograma mostrando como tratar mensagens do WM \- Close e do WM \- Destroy](images/wmclose01.png)

## <a name="next"></a><span data-ttu-id="4c0b8-126">Avançar</span><span class="sxs-lookup"><span data-stu-id="4c0b8-126">Next</span></span>

[<span data-ttu-id="4c0b8-127">Gerenciando o estado do aplicativo</span><span class="sxs-lookup"><span data-stu-id="4c0b8-127">Managing Application State</span></span>](managing-application-state-.md)