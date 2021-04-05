---
title: Mensagens de controle
description: Esta seção contém informações sobre como as mensagens do Windows são usadas para se comunicar com controles.
ms.assetid: 94d34132-25c2-4a1a-bd0e-35e5a666bbfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923a1b47d625a2797a900a6c582d00c5169097f3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103824094"
---
# <a name="control-messages"></a><span data-ttu-id="0e350-103">Mensagens de controle</span><span class="sxs-lookup"><span data-stu-id="0e350-103">Control Messages</span></span>

<span data-ttu-id="0e350-104">Esta seção contém informações sobre como as mensagens do Windows são usadas para se comunicar com controles.</span><span class="sxs-lookup"><span data-stu-id="0e350-104">This section contains information about how Windows messages are used to communicate with controls.</span></span>

<span data-ttu-id="0e350-105">Os tópicos a seguir são discutidos.</span><span class="sxs-lookup"><span data-stu-id="0e350-105">The following topics are discussed.</span></span>

-   [<span data-ttu-id="0e350-106">Mensagens para controles comuns</span><span class="sxs-lookup"><span data-stu-id="0e350-106">Messages to Common Controls</span></span>](#messages-to-common-controls)
-   [<span data-ttu-id="0e350-107">Notificações de controles</span><span class="sxs-lookup"><span data-stu-id="0e350-107">Notifications from Controls</span></span>](#notifications-from-controls)
-   [<span data-ttu-id="0e350-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e350-108">Related topics</span></span>](#related-topics)

## <a name="messages-to-common-controls"></a><span data-ttu-id="0e350-109">Mensagens para controles comuns</span><span class="sxs-lookup"><span data-stu-id="0e350-109">Messages to Common Controls</span></span>

<span data-ttu-id="0e350-110">Como os controles comuns são janelas, um aplicativo pode se comunicar com eles usando mensagens comuns do Microsoft Win32, como [**WM \_ GetFont**](/windows/desktop/winmsg/wm-getfont) ou [**WM \_ SetText**](/windows/desktop/winmsg/wm-settext).</span><span class="sxs-lookup"><span data-stu-id="0e350-110">Because common controls are windows, an application can communicate with them by using common Microsoft Win32 messages such as [**WM\_GETFONT**](/windows/desktop/winmsg/wm-getfont) or [**WM\_SETTEXT**](/windows/desktop/winmsg/wm-settext).</span></span> <span data-ttu-id="0e350-111">Além disso, a classe Window de cada controle comum dá suporte a um conjunto de mensagens específicas de controle.</span><span class="sxs-lookup"><span data-stu-id="0e350-111">In addition, the window class of each common control supports a set of control-specific messages.</span></span> <span data-ttu-id="0e350-112">Normalmente, um aplicativo usa [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) ou [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) para passar mensagens para o controle (geralmente recebendo informações no valor de retorno).</span><span class="sxs-lookup"><span data-stu-id="0e350-112">Typically, an application uses [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) or [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea) to pass messages to the control (often receiving information in the return value).</span></span>

<span data-ttu-id="0e350-113">Alguns controles comuns também têm um conjunto de macros que um aplicativo pode usar em vez de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span><span class="sxs-lookup"><span data-stu-id="0e350-113">Some common controls also have a set of macros that an application can use instead of [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).</span></span> <span data-ttu-id="0e350-114">Normalmente, as macros são mais fáceis de usar do que as funções.</span><span class="sxs-lookup"><span data-stu-id="0e350-114">The macros are typically easier to use than the functions.</span></span> <span data-ttu-id="0e350-115">O código de exemplo a seguir recupera o texto do item de exibição de árvore selecionado, primeiro usando as mensagens brutas e segundo usando as macros equivalentes.</span><span class="sxs-lookup"><span data-stu-id="0e350-115">The following example code retrieves the text of the selected tree-view item, first by using the raw messages, and second by using the equivalent macros.</span></span> <span data-ttu-id="0e350-116">Suponha que *HWND* é o identificador da janela de controle.</span><span class="sxs-lookup"><span data-stu-id="0e350-116">Assume that *hwnd* is the handle of the control window.</span></span>


```
BOOL fSuccess;
WCHAR itemText[99];
TVITEM tvItem = { 0 };
tvItem.mask = TVIF_TEXT;
tvItem.cchTextMax = ARRAYSIZE(itemText);
tvItem.pszText = itemText;

// This...
tvItem.hItem = (HTREEITEM)SendMessage(hwnd, TVM_GETNEXTITEM, TVGN_CARET, NULL);
fSuccess = SendMessage(hwnd, TVM_GETITEM, 0, (LPARAM)&tvItem);

// ... is equivalent to this.
tvItem.hItem = TreeView_GetSelection(hwnd);
fSuccess = TreeView_GetItem(hwnd, &tvItem);
```



<span data-ttu-id="0e350-117">Quando uma alteração é feita nas configurações de cores do sistema, o Windows envia uma mensagem do [**WM \_ SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) para todas as janelas de nível superior.</span><span class="sxs-lookup"><span data-stu-id="0e350-117">When a change is made to the system color settings, Windows sends a [**WM\_SYSCOLORCHANGE**](/windows/desktop/gdi/wm-syscolorchange) message to all top-level windows.</span></span> <span data-ttu-id="0e350-118">A janela de nível superior deve encaminhar a mensagem do **WM \_ SYSCOLORCHANGE** para seus controles comuns; caso contrário, os controles não serão notificados sobre a alteração de cor.</span><span class="sxs-lookup"><span data-stu-id="0e350-118">Your top-level window must forward the **WM\_SYSCOLORCHANGE** message to its common controls; otherwise, the controls will not be notified of the color change.</span></span> <span data-ttu-id="0e350-119">O encaminhamento da mensagem garante que as cores usadas por seus controles comuns sejam consistentes com as usadas por outros objetos da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="0e350-119">Forwarding the message ensures that the colors used by your common controls are consistent with those used by other user interface objects.</span></span> <span data-ttu-id="0e350-120">Por exemplo, um controle Toolbar usa a cor "3D Objects" para desenhar seus botões.</span><span class="sxs-lookup"><span data-stu-id="0e350-120">For example, a toolbar control uses the "3-D Objects" color to draw its buttons.</span></span> <span data-ttu-id="0e350-121">Se o usuário alterar a cor do objeto 3-D, mas a mensagem do **WM \_ SYSCOLORCHANGE** não for encaminhada para a barra de ferramentas, os botões da barra de ferramentas permanecerão na cor original (ou até mesmo mudarão para uma combinação de cores novas e antigas), enquanto a cor dos outros botões no sistema é alterada.</span><span class="sxs-lookup"><span data-stu-id="0e350-121">If the user changes the 3-D Object's color but the **WM\_SYSCOLORCHANGE** message is not forwarded to the toolbar, the toolbar buttons will remain in their original color (or even change to a combination of old and new colors) while the color of other buttons in the system changes.</span></span>

## <a name="notifications-from-controls"></a><span data-ttu-id="0e350-122">Notificações de controles</span><span class="sxs-lookup"><span data-stu-id="0e350-122">Notifications from Controls</span></span>

<span data-ttu-id="0e350-123">Os controles são janelas filhas que enviam mensagens de notificação para a janela pai quando eventos, geralmente disparados pela entrada do usuário, ocorrem no controle.</span><span class="sxs-lookup"><span data-stu-id="0e350-123">Controls are child windows that send notification messages to the parent window when events, usually triggered by input from the user, occur in the control.</span></span> <span data-ttu-id="0e350-124">O aplicativo depende dessas mensagens de notificação para determinar a ação que o usuário deseja executar.</span><span class="sxs-lookup"><span data-stu-id="0e350-124">The application relies on these notification messages to determine what action the user wants it to take.</span></span> <span data-ttu-id="0e350-125">Exceto para trackbars, que usam as mensagens do [**WM \_ HSCROLL**](wm-hscroll.md) e do [**WM \_ VSCROLL**](wm-vscroll.md) para notificar o pai das alterações, os controles comuns enviam notificações como o [**\_ comando do WM**](/windows/desktop/menurc/wm-command) ou mensagens de [**\_ notificação do WM**](wm-notify.md) , conforme especificado no tópico de referência para a notificação.</span><span class="sxs-lookup"><span data-stu-id="0e350-125">Except for trackbars, which use the [**WM\_HSCROLL**](wm-hscroll.md) and [**WM\_VSCROLL**](wm-vscroll.md) messages to notify their parent of changes, common controls send notifications as either [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages, as specified in the reference topic for the notification.</span></span> <span data-ttu-id="0e350-126">Normalmente, as notificações mais antigas (aquelas que estavam na API há muito tempo) usam o **\_ comando do WM**.</span><span class="sxs-lookup"><span data-stu-id="0e350-126">Typically, older notifications (those that have been in the API for a long time) use **WM\_COMMAND**.</span></span>

<span data-ttu-id="0e350-127">O parâmetro *lParam* do [**WM \_ Notify**](wm-notify.md) é o endereço de uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) ou o endereço de uma estrutura maior que inclui **NMHDR** como seu primeiro membro.</span><span class="sxs-lookup"><span data-stu-id="0e350-127">The *lParam* parameter of [**WM\_NOTIFY**](wm-notify.md) is either the address of an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure or the address of a larger structure that includes **NMHDR** as its first member.</span></span> <span data-ttu-id="0e350-128">A estrutura contém o código de notificação e identifica o controle comum que enviou a mensagem de notificação.</span><span class="sxs-lookup"><span data-stu-id="0e350-128">The structure contains the notification code and identifies the common control that sent the notification message.</span></span> <span data-ttu-id="0e350-129">O significado dos membros da estrutura restantes, se houver, varia dependendo do código de notificação.</span><span class="sxs-lookup"><span data-stu-id="0e350-129">The meaning of the remaining structure members, if any, varies depending on the notification code.</span></span>

<span data-ttu-id="0e350-130">Cada tipo de controle comum tem um conjunto correspondente de códigos de notificação.</span><span class="sxs-lookup"><span data-stu-id="0e350-130">Each type of common control has a corresponding set of notification codes.</span></span> <span data-ttu-id="0e350-131">A biblioteca de controle comum também fornece códigos de notificação que podem ser enviados por mais de um tipo de controle comum.</span><span class="sxs-lookup"><span data-stu-id="0e350-131">The common control library also provides notification codes that can be sent by more than one type of common control.</span></span> <span data-ttu-id="0e350-132">Consulte a documentação do controle de interesse para determinar quais códigos de notificação serão enviados e qual será o formato adotado.</span><span class="sxs-lookup"><span data-stu-id="0e350-132">See the documentation for the control of interest to determine which notification codes it will send and what format they take.</span></span>

<span data-ttu-id="0e350-133">Por exemplo, código que mostra como lidar com mensagens de [**\_ notificação do WM**](wm-notify.md) , consulte o tópico de referência para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="0e350-133">For example code showing how to handle [**WM\_NOTIFY**](wm-notify.md) messages, see the reference topic for that message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e350-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e350-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e350-135">Referência de controle geral</span><span class="sxs-lookup"><span data-stu-id="0e350-135">General Control Reference</span></span>](common-control-reference.md)
</dt> </dl>

 

 
