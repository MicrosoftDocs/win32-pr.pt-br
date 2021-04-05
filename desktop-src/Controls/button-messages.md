---
title: 'Mensagens de botão '
description: Um botão pode enviar mensagens para sua janela pai e uma janela pai pode enviar mensagens a um botão.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1601f269ec1242a10579d2ace812723d3ead7f84
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103642785"
---
# <a name="button-messages"></a><span data-ttu-id="73a6f-103">Mensagens de botão </span><span class="sxs-lookup"><span data-stu-id="73a6f-103">Button Messages</span></span>

<span data-ttu-id="73a6f-104">Um botão pode enviar mensagens para sua janela pai e uma janela pai pode enviar mensagens a um botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-104">A button can send messages to its parent window, and a parent window can send messages to a button.</span></span>

<span data-ttu-id="73a6f-105">Os tópicos a seguir são discutidos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="73a6f-105">The following topics are discussed in this section.</span></span>

-   [<span data-ttu-id="73a6f-106">Enviando mensagens para botões</span><span class="sxs-lookup"><span data-stu-id="73a6f-106">Sending Messages to Buttons</span></span>](#sending-messages-to-buttons)
-   [<span data-ttu-id="73a6f-107">Manipulando mensagens de um botão</span><span class="sxs-lookup"><span data-stu-id="73a6f-107">Handling Messages from a Button</span></span>](#handling-messages-from-a-button)
-   [<span data-ttu-id="73a6f-108">Mensagens de notificação de botões</span><span class="sxs-lookup"><span data-stu-id="73a6f-108">Notification Messages from Buttons</span></span>](#notification-messages-from-buttons)
-   [<span data-ttu-id="73a6f-109">Mensagens de cor do botão</span><span class="sxs-lookup"><span data-stu-id="73a6f-109">Button Color Messages</span></span>](#button-color-messages)
-   [<span data-ttu-id="73a6f-110">Botão de processamento de mensagem padrão</span><span class="sxs-lookup"><span data-stu-id="73a6f-110">Button Default Message Processing</span></span>](#button-default-message-processing)
-   [<span data-ttu-id="73a6f-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73a6f-111">Related topics</span></span>](#related-topics)

## <a name="sending-messages-to-buttons"></a><span data-ttu-id="73a6f-112">Enviando mensagens para botões</span><span class="sxs-lookup"><span data-stu-id="73a6f-112">Sending Messages to Buttons</span></span>

<span data-ttu-id="73a6f-113">Uma janela pai pode enviar mensagens a um botão em uma janela sobreposta ou filho usando a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) ou pode enviar mensagens para um botão em uma caixa de diálogo usando as funções [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)e [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .</span><span class="sxs-lookup"><span data-stu-id="73a6f-113">A parent window can send messages to a button in an overlapped or child window by using the [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) function, or it can send messages to a button in a dialog box by using the [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton), and [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) functions.</span></span>

<span data-ttu-id="73a6f-114">Um aplicativo pode usar a [**mensagem \_ getcheck do BM**](bm-getcheck.md) para recuperar o estado de verificação de uma caixa de seleção ou um botão de opção.</span><span class="sxs-lookup"><span data-stu-id="73a6f-114">An application can use the [**BM\_GETCHECK**](bm-getcheck.md) message to retrieve the check state of a check box or radio button.</span></span> <span data-ttu-id="73a6f-115">Um aplicativo também pode usar a [**mensagem \_ GetState do BM**](bm-getstate.md) para recuperar os Estados atuais do botão (o estado de verificação, o estado de push e o estado de foco).</span><span class="sxs-lookup"><span data-stu-id="73a6f-115">An application can also use the [**BM\_GETSTATE**](bm-getstate.md) message to retrieve the button's current states (the check state, push state, and focus state).</span></span> <span data-ttu-id="73a6f-116">Para obter informações sobre um estado específico, use uma bitmask no valor de estado retornado.</span><span class="sxs-lookup"><span data-stu-id="73a6f-116">To get information about a specific state, use a bitmask on the returned state value.</span></span>

<span data-ttu-id="73a6f-117">A [**mensagem \_ SetCheck do BM**](bm-setcheck.md) define o estado de verificação de uma caixa de seleção ou botão de opção; a mensagem retorna zero.</span><span class="sxs-lookup"><span data-stu-id="73a6f-117">The [**BM\_SETCHECK**](bm-setcheck.md) message sets the check state of a check box or radio button; the message returns zero.</span></span> <span data-ttu-id="73a6f-118">A [**mensagem \_ SetState do BM**](bm-setstate.md) define o estado de push de um botão; essa mensagem também retorna zero.</span><span class="sxs-lookup"><span data-stu-id="73a6f-118">The [**BM\_SETSTATE**](bm-setstate.md) message sets the push state of a button; this message also returns zero.</span></span> <span data-ttu-id="73a6f-119">A [**mensagem \_ SetStyle BM**](bm-setstyle.md) altera o estilo de um botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-119">The [**BM\_SETSTYLE**](bm-setstyle.md) message changes the style of a button.</span></span> <span data-ttu-id="73a6f-120">Ele foi projetado para alterar estilos de botão dentro de um tipo (por exemplo, alterar uma caixa de seleção para uma caixa de seleção automática).</span><span class="sxs-lookup"><span data-stu-id="73a6f-120">It is designed for changing button styles within a type (for example, changing a check box to an automatic check box).</span></span> <span data-ttu-id="73a6f-121">Ele não foi projetado para alterar entre os tipos (por exemplo, alterar uma caixa de seleção para um botão de opção).</span><span class="sxs-lookup"><span data-stu-id="73a6f-121">It is not designed for changing between types (for example, changing a check box to a radio button).</span></span> <span data-ttu-id="73a6f-122">Um aplicativo não deve alterar um botão de um tipo para outro.</span><span class="sxs-lookup"><span data-stu-id="73a6f-122">An application should not change a button from one type to another.</span></span>

<span data-ttu-id="73a6f-123">Um botão do estilo de [**\_ ícone**](button-styles.md) de [**\_ bitmap BS**](button-styles.md) ou BS exibe um bitmap ou ícone em vez de texto.</span><span class="sxs-lookup"><span data-stu-id="73a6f-123">A button of the [**BS\_BITMAP**](button-styles.md) or [**BS\_ICON**](button-styles.md) style displays a bitmap or icon instead of text.</span></span> <span data-ttu-id="73a6f-124">A mensagem [**BM \_ SetImage**](bm-setimage.md) associa um identificador a um bitmap ou ícone com um botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-124">The [**BM\_SETIMAGE**](bm-setimage.md) message associates a handle to a bitmap or icon with a button.</span></span> <span data-ttu-id="73a6f-125">A mensagem [**BM \_ GetImage**](bm-getimage.md) recupera um identificador para o bitmap ou ícone associado a um botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-125">The [**BM\_GETIMAGE**](bm-getimage.md) message retrieves a handle to the bitmap or icon associated with a button.</span></span>

<span data-ttu-id="73a6f-126">Um aplicativo também pode usar a mensagem [**DM \_ GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) para recuperar o identificador do controle de botão de ação padrão em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="73a6f-126">An application can also use the [**DM\_GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) message to retrieve the identifier of the default push button control in a dialog box.</span></span> <span data-ttu-id="73a6f-127">Um aplicativo pode usar a mensagem [**DM \_ SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) para definir o botão de ação padrão para uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="73a6f-127">An application can use the [**DM\_SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) message to set the default push button for a dialog box.</span></span>

<span data-ttu-id="73a6f-128">Chamar a função [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) ou [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) é equivalente a enviar uma [**mensagem \_ SetCheck BM**](bm-setcheck.md) .</span><span class="sxs-lookup"><span data-stu-id="73a6f-128">Calling the [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) or [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) function is equivalent to sending a [**BM\_SETCHECK**](bm-setcheck.md) message.</span></span> <span data-ttu-id="73a6f-129">Chamar a função [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) é equivalente a enviar uma mensagem [**BM \_ getcheck**](bm-getcheck.md) .</span><span class="sxs-lookup"><span data-stu-id="73a6f-129">Calling the [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) function is equivalent to sending a [**BM\_GETCHECK**](bm-getcheck.md) message.</span></span>

## <a name="handling-messages-from-a-button"></a><span data-ttu-id="73a6f-130">Manipulando mensagens de um botão</span><span class="sxs-lookup"><span data-stu-id="73a6f-130">Handling Messages from a Button</span></span>

<span data-ttu-id="73a6f-131">As notificações de um botão são enviadas como [**o \_ comando do WM**](/windows/desktop/menurc/wm-command) ou mensagens de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="73a6f-131">Notifications from a button are sent as either [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) or [**WM\_NOTIFY**](wm-notify.md) messages.</span></span> <span data-ttu-id="73a6f-132">As informações sobre qual mensagem é usada podem ser encontradas na página de referência para cada notificação.</span><span class="sxs-lookup"><span data-stu-id="73a6f-132">Information about which message is used can be found on the reference page for each notification.</span></span>

<span data-ttu-id="73a6f-133">Para obter mais informações sobre como lidar com mensagens, consulte [Control messages](control-messages.md).</span><span class="sxs-lookup"><span data-stu-id="73a6f-133">For more information on how to handle messages, see [Control Messages](control-messages.md).</span></span> <span data-ttu-id="73a6f-134">Consulte também mensagens de botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-134">See also Button Messages.</span></span>

## <a name="notification-messages-from-buttons"></a><span data-ttu-id="73a6f-135">Mensagens de notificação de botões</span><span class="sxs-lookup"><span data-stu-id="73a6f-135">Notification Messages from Buttons</span></span>

<span data-ttu-id="73a6f-136">Quando o usuário clica em um botão, seu estado é alterado e o botão envia códigos de notificação, na forma de mensagens de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) , para sua janela pai.</span><span class="sxs-lookup"><span data-stu-id="73a6f-136">When the user clicks a button, its state changes, and the button sends notification codes, in the form of [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages, to its parent window.</span></span> <span data-ttu-id="73a6f-137">Por exemplo, um controle de botão de ação envia o código de notificação [ \_ clicado bilhão](bn-clicked.md) sempre que o usuário escolhe o botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-137">For example, a push button control sends the [BN\_CLICKED](bn-clicked.md) notification code whenever the user chooses the button.</span></span> <span data-ttu-id="73a6f-138">Em todos os casos (exceto [para BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)), a palavra de ordem inferior do parâmetro *wParam* contém o identificador de controle, a palavra de ordem superior de *wParam* contém o código de notificação e o parâmetro *lParam* contém o identificador da janela de controle.</span><span class="sxs-lookup"><span data-stu-id="73a6f-138">In all cases (except for [BCN\_HOTITEMCHANGE](bcn-hotitemchange.md)), the low-order word of the *wParam* parameter contains the control identifier, the high-order word of *wParam* contains the notification code, and the *lParam* parameter contains the control window handle.</span></span>

<span data-ttu-id="73a6f-139">A mensagem e a resposta da janela pai dependem do tipo, do estilo e do estado atual do botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-139">Both the message and the parent window's response depend on the type, style, and current state of the button.</span></span> <span data-ttu-id="73a6f-140">A seguir estão os códigos de notificação do botão que um aplicativo deve monitorar e processar.</span><span class="sxs-lookup"><span data-stu-id="73a6f-140">Following are the button notification codes an application should monitor and process.</span></span>



| <span data-ttu-id="73a6f-141">Código de notificação</span><span class="sxs-lookup"><span data-stu-id="73a6f-141">Notification code</span></span>                                                        | <span data-ttu-id="73a6f-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="73a6f-142">Description</span></span>                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="73a6f-143">BCN \_ HOTITEMCHANGE</span><span class="sxs-lookup"><span data-stu-id="73a6f-143">BCN\_HOTITEMCHANGE</span></span>](bcn-hotitemchange.md)                              | <span data-ttu-id="73a6f-144">O mouse inseriu ou deixou a área do cliente de um botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-144">The mouse entered or left the client area of a button.</span></span> |
| [<span data-ttu-id="73a6f-145">BILHÃO \_ clicou</span><span class="sxs-lookup"><span data-stu-id="73a6f-145">BN\_CLICKED</span></span>](bn-clicked.md)                                            | <span data-ttu-id="73a6f-146">O usuário clicou em um botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-146">The user clicked a button.</span></span>                             |
| <span data-ttu-id="73a6f-147">[Bilhão \_ DBLCLK](bn-dblclk.md) ou [bilhão \_ doubleclicked](bn-doubleclicked.md)</span><span class="sxs-lookup"><span data-stu-id="73a6f-147">[BN\_DBLCLK](bn-dblclk.md) or [BN\_DOUBLECLICKED](bn-doubleclicked.md)</span></span> | <span data-ttu-id="73a6f-148">O usuário clicou duas vezes em um botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-148">The user double-clicked a button.</span></span>                      |
| [<span data-ttu-id="73a6f-149">BILHÃO \_ desabilitar</span><span class="sxs-lookup"><span data-stu-id="73a6f-149">BN\_DISABLE</span></span>](bn-disable.md)                                            | <span data-ttu-id="73a6f-150">Um botão está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="73a6f-150">A button is disabled.</span></span>                                  |
| <span data-ttu-id="73a6f-151">[Bilhão \_ ENVIADO por push](bn-pushed.md) ou [bilhão \_ HILITE](bn-hilite.md)</span><span class="sxs-lookup"><span data-stu-id="73a6f-151">[BN\_PUSHED](bn-pushed.md) or [BN\_HILITE](bn-hilite.md)</span></span>               | <span data-ttu-id="73a6f-152">O usuário enviou um botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-152">The user pushed a button.</span></span>                              |
| [<span data-ttu-id="73a6f-153">BILHÃO \_ KILLFOCUS</span><span class="sxs-lookup"><span data-stu-id="73a6f-153">BN\_KILLFOCUS</span></span>](bn-killfocus.md)                                        | <span data-ttu-id="73a6f-154">O botão perdeu o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="73a6f-154">The button lost the keyboard focus.</span></span>                    |
| [<span data-ttu-id="73a6f-155">BILHÃO \_ Paint</span><span class="sxs-lookup"><span data-stu-id="73a6f-155">BN\_PAINT</span></span>](bn-paint.md)                                                | <span data-ttu-id="73a6f-156">O botão deve ser pintado.</span><span class="sxs-lookup"><span data-stu-id="73a6f-156">The button should be painted.</span></span>                          |
| [<span data-ttu-id="73a6f-157">BILHÃO \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="73a6f-157">BN\_SETFOCUS</span></span>](bn-setfocus.md)                                          | <span data-ttu-id="73a6f-158">O botão ganhou o foco do teclado.</span><span class="sxs-lookup"><span data-stu-id="73a6f-158">The button gained the keyboard focus.</span></span>                  |
| <span data-ttu-id="73a6f-159">[Bilhão \_ Sem envio por PUSH](bn-unpushed.md) ou [bilhão \_ UNHILITE](bn-unhilite.md)</span><span class="sxs-lookup"><span data-stu-id="73a6f-159">[BN\_UNPUSHED](bn-unpushed.md) or [BN\_UNHILITE](bn-unhilite.md)</span></span>       | <span data-ttu-id="73a6f-160">O botão não é mais enviado por push.</span><span class="sxs-lookup"><span data-stu-id="73a6f-160">The button is no longer pushed.</span></span>                        |



 

<span data-ttu-id="73a6f-161">Um botão envia os códigos de notificação [bilhão \_ Disable](bn-disable.md), [bilhão \_ Push](bn-pushed.md), [bilhão \_ KILLFOCUS](bn-killfocus.md), [bilhão \_ Paint](bn-paint.md), [bilhão \_ SETFOCUS](bn-setfocus.md)e [bilhão sem \_ envio](bn-unpushed.md) de notificações somente se ele tiver o estilo de [**\_ notificação BS**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="73a6f-161">A button sends the [BN\_DISABLE](bn-disable.md), [BN\_PUSHED](bn-pushed.md), [BN\_KILLFOCUS](bn-killfocus.md), [BN\_PAINT](bn-paint.md), [BN\_SETFOCUS](bn-setfocus.md), and [BN\_UNPUSHED](bn-unpushed.md) notification codes only if it has the [**BS\_NOTIFY**](button-styles.md) style.</span></span> <span data-ttu-id="73a6f-162">[Bilhão \_](bn-dblclk.md) Os códigos de notificação do DBLCLK são enviados automaticamente para os botões de [**\_ UserButton**](button-styles.md), [**BS \_**](button-styles.md)e BS [**\_ OWNERDRAW**](button-styles.md) da BS.</span><span class="sxs-lookup"><span data-stu-id="73a6f-162">[BN\_DBLCLK](bn-dblclk.md) notification codes are sent automatically for [**BS\_USERBUTTON**](button-styles.md), [**BS\_RADIOBUTTON**](button-styles.md), and [**BS\_OWNERDRAW**](button-styles.md) buttons.</span></span> <span data-ttu-id="73a6f-163">Outros tipos de botão enviam bilhão \_ DBLCLK somente se tiverem o estilo de **\_ notificação BS** .</span><span class="sxs-lookup"><span data-stu-id="73a6f-163">Other button types send BN\_DBLCLK only if they have the **BS\_NOTIFY** style.</span></span> <span data-ttu-id="73a6f-164">Todos os botões enviam o código de notificação [ \_ clicado bilhão](bn-clicked.md) , independentemente de seus estilos de botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-164">All buttons send the [BN\_CLICKED](bn-clicked.md) notification code regardless of their button styles.</span></span>

<span data-ttu-id="73a6f-165">Para botões automáticos, o sistema altera o estado de push e pinta o botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-165">For automatic buttons, the system changes the push state and paints the button.</span></span> <span data-ttu-id="73a6f-166">Nesse caso, o aplicativo normalmente processa apenas os códigos de notificação bilhão [e \_ bilhão](bn-dblclk.md) [ \_ clicados](bn-clicked.md) .</span><span class="sxs-lookup"><span data-stu-id="73a6f-166">In this case, the application typically processes only the [BN\_CLICKED](bn-clicked.md) and [BN\_DBLCLK](bn-dblclk.md) notification codes.</span></span> <span data-ttu-id="73a6f-167">Para botões que não são automáticos, o aplicativo normalmente responde ao código de notificação enviando uma mensagem para alterar o estado do botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-167">For buttons that are not automatic, the application typically responds to the notification code by sending a message to change the state of the button.</span></span> <span data-ttu-id="73a6f-168">Para obter informações sobre como enviar mensagens para botões, consulte [enviando mensagens para botões](#sending-messages-to-buttons).</span><span class="sxs-lookup"><span data-stu-id="73a6f-168">For information about sending messages to buttons, see [Sending Messages to Buttons](#sending-messages-to-buttons).</span></span>

<span data-ttu-id="73a6f-169">Quando o usuário seleciona um botão de desenho proprietário, o botão envia sua janela pai a uma mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) que contém o identificador do controle a ser desenhado e informações sobre suas dimensões e seu estado.</span><span class="sxs-lookup"><span data-stu-id="73a6f-169">When the user selects an owner-drawn button, the button sends its parent window a [**WM\_DRAWITEM**](wm-drawitem.md) message containing the identifier of the control to be drawn and information about its dimensions and state.</span></span>

## <a name="button-color-messages"></a><span data-ttu-id="73a6f-170">Mensagens de cor do botão</span><span class="sxs-lookup"><span data-stu-id="73a6f-170">Button Color Messages</span></span>

<span data-ttu-id="73a6f-171">O sistema fornece valores de cor padrão para botões.</span><span class="sxs-lookup"><span data-stu-id="73a6f-171">The system provides default color values for buttons.</span></span> <span data-ttu-id="73a6f-172">Um aplicativo pode recuperar os valores padrão para essas cores chamando a função [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) ou definir os valores chamando a função [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) .</span><span class="sxs-lookup"><span data-stu-id="73a6f-172">An application can retrieve the default values for these colors by calling the [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) function, or set the values by calling the [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) function.</span></span> <span data-ttu-id="73a6f-173">A tabela a seguir mostra os valores de cor de botão padrão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-173">The following table shows the default button-color values.</span></span>



| <span data-ttu-id="73a6f-174">Valor</span><span class="sxs-lookup"><span data-stu-id="73a6f-174">Value</span></span>               | <span data-ttu-id="73a6f-175">Elemento colorido</span><span class="sxs-lookup"><span data-stu-id="73a6f-175">Element colored</span></span>                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73a6f-176">BTNFACE de cor \_</span><span class="sxs-lookup"><span data-stu-id="73a6f-176">COLOR\_BTNFACE</span></span>      | <span data-ttu-id="73a6f-177">Rostos de botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-177">Button faces.</span></span>                                                                                                              |
| <span data-ttu-id="73a6f-178">BTNHIGHLIGHT de cor \_</span><span class="sxs-lookup"><span data-stu-id="73a6f-178">COLOR\_BTNHIGHLIGHT</span></span> | <span data-ttu-id="73a6f-179">Área de realce (as bordas superior e esquerda) de um botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-179">Highlight area (the top and left edges) of a button.</span></span>                                                                       |
| <span data-ttu-id="73a6f-180">BTNSHADOW de cor \_</span><span class="sxs-lookup"><span data-stu-id="73a6f-180">COLOR\_BTNSHADOW</span></span>    | <span data-ttu-id="73a6f-181">Área de sombra (as bordas inferior e direita) de um botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-181">Shadow area (the bottom and right edges) of a button.</span></span>                                                                      |
| <span data-ttu-id="73a6f-182">BtnText de cor \_</span><span class="sxs-lookup"><span data-stu-id="73a6f-182">COLOR\_BTNTEXT</span></span>      | <span data-ttu-id="73a6f-183">Texto regular (não cinza) em botões.</span><span class="sxs-lookup"><span data-stu-id="73a6f-183">Regular (nongrayed) text in buttons.</span></span>                                                                                       |
| <span data-ttu-id="73a6f-184">GRAYTEXT de cor \_</span><span class="sxs-lookup"><span data-stu-id="73a6f-184">COLOR\_GRAYTEXT</span></span>     | <span data-ttu-id="73a6f-185">Texto desabilitado (cinza) em botões.</span><span class="sxs-lookup"><span data-stu-id="73a6f-185">Disabled (gray) text in buttons.</span></span> <span data-ttu-id="73a6f-186">Essa cor será definida como 0 se o driver de vídeo atual não oferecer suporte a uma cor cinza sólida.</span><span class="sxs-lookup"><span data-stu-id="73a6f-186">This color is set to 0 if the current display driver does not support a solid gray color.</span></span> |
| <span data-ttu-id="73a6f-187">janela de cores \_</span><span class="sxs-lookup"><span data-stu-id="73a6f-187">COLOR\_WINDOW</span></span>       | <span data-ttu-id="73a6f-188">Planos de fundo da janela.</span><span class="sxs-lookup"><span data-stu-id="73a6f-188">Window backgrounds.</span></span>                                                                                                        |
| <span data-ttu-id="73a6f-189">WINDOWFRAME de cor \_</span><span class="sxs-lookup"><span data-stu-id="73a6f-189">COLOR\_WINDOWFRAME</span></span>  | <span data-ttu-id="73a6f-190">Quadros de janela.</span><span class="sxs-lookup"><span data-stu-id="73a6f-190">Window frames.</span></span>                                                                                                             |
| <span data-ttu-id="73a6f-191">WINDOWTEXT de cor \_</span><span class="sxs-lookup"><span data-stu-id="73a6f-191">COLOR\_WINDOWTEXT</span></span>   | <span data-ttu-id="73a6f-192">Texto no Windows.</span><span class="sxs-lookup"><span data-stu-id="73a6f-192">Text in windows.</span></span>                                                                                                           |



 

<span data-ttu-id="73a6f-193">No entanto, chamar [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) afeta todos os aplicativos, portanto, você não deve chamar essa função para personalizar botões para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="73a6f-193">However, calling [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) affects all applications, so you should not call this function to customize buttons for your application.</span></span>

<span data-ttu-id="73a6f-194">O sistema envia uma mensagem do [**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md) para a janela pai de um botão antes de desenhar um botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-194">The system sends a [**WM\_CTLCOLORBTN**](wm-ctlcolorbtn.md) message to a button's parent window before drawing a button.</span></span> <span data-ttu-id="73a6f-195">Essa mensagem contém um identificador para o contexto do dispositivo do botão e um identificador para a janela filho.</span><span class="sxs-lookup"><span data-stu-id="73a6f-195">This message contains a handle to the button's device context and a handle to the child window.</span></span> <span data-ttu-id="73a6f-196">A janela pai pode usar esses identificadores para alterar o texto do botão e as cores do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="73a6f-196">The parent window can use these handles to change the button's text and background colors.</span></span> <span data-ttu-id="73a6f-197">No entanto, somente botões desenhados pelo proprietário respondem à janela pai que processa a mensagem.</span><span class="sxs-lookup"><span data-stu-id="73a6f-197">However, only owner-drawn buttons respond to the parent window processing the message.</span></span>

## <a name="button-default-message-processing"></a><span data-ttu-id="73a6f-198">Botão de processamento de mensagem padrão</span><span class="sxs-lookup"><span data-stu-id="73a6f-198">Button Default Message Processing</span></span>

<span data-ttu-id="73a6f-199">O procedimento de janela para a classe de janela de controle de botão predefinido executa o processamento padrão para todas as mensagens que o procedimento de controle de botão não processa.</span><span class="sxs-lookup"><span data-stu-id="73a6f-199">The window procedure for the predefined button control window class carries out default processing for all messages that the button control procedure does not process.</span></span> <span data-ttu-id="73a6f-200">Quando o procedimento de controle de botão retorna **false** para qualquer mensagem, o procedimento de janela predefinido verifica as mensagens e executa as ações padrão listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="73a6f-200">When the button control procedure returns **FALSE** for any message, the predefined window procedure checks the messages and performs the default actions listed in the following table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73a6f-201">Mensagem</span><span class="sxs-lookup"><span data-stu-id="73a6f-201">Message</span></span></th>
<th><span data-ttu-id="73a6f-202">Ação padrão</span><span class="sxs-lookup"><span data-stu-id="73a6f-202">Default action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73a6f-203"><a href="bm-click.md"><strong>BM_CLICK</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-203"><a href="bm-click.md"><strong>BM_CLICK</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-204">Envia ao botão um <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> e uma mensagem de <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> e envia a janela pai um código de notificação <a href="bn-clicked.md">BN_CLICKED</a> .</span><span class="sxs-lookup"><span data-stu-id="73a6f-204">Sends the button a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> and a <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> message, and sends the parent window a <a href="bn-clicked.md">BN_CLICKED</a> notification code.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-205"><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-205"><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-206">Retorna o estado de verificação do botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-206">Returns the check state of the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-207"><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-207"><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-208">Retorna um identificador para o bitmap ou ícone associado ao botão ou <strong>nulo</strong> se o botão não tiver bitmap ou ícone.</span><span class="sxs-lookup"><span data-stu-id="73a6f-208">Returns a handle to the bitmap or icon associated with the button or <strong>NULL</strong> if the button has no bitmap or icon.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-209"><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-209"><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-210">Retorna o estado de verificação atual, o estado de push e o estado de foco do botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-210">Returns the current check state, push state, and focus state of the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-211"><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-211"><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-212">Define o estado de verificação para todos os estilos de botões de opção e caixas de seleção.</span><span class="sxs-lookup"><span data-stu-id="73a6f-212">Sets the check state for all styles of radio buttons and check boxes.</span></span> <span data-ttu-id="73a6f-213">Se o parâmetro <em>wParam</em> for maior que zero para botões de opção, o botão receberá o estilo de <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="73a6f-213">If the <em>wParam</em> parameter is greater than zero for radio buttons, the button is given the <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> style.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-214"><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-214"><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-215">Associa o bitmap ou o identificador de ícone especificado ao botão e retorna um identificador para o bitmap ou ícone anterior.</span><span class="sxs-lookup"><span data-stu-id="73a6f-215">Associates the specified bitmap or icon handle with the button and returns a handle to the previous bitmap or icon.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-216"><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-216"><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-217">Define o estado de push do botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-217">Sets the push state of the button.</span></span> <span data-ttu-id="73a6f-218">Para botões desenhados pelo proprietário, uma mensagem de <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> será enviada para a janela pai se o estado do botão for alterado.</span><span class="sxs-lookup"><span data-stu-id="73a6f-218">For owner-drawn buttons, a <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> message is sent to the parent window if the state of the button has changed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-219"><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-219"><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-220">Define o estilo do botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-220">Sets the button style.</span></span> <span data-ttu-id="73a6f-221">Se a palavra de ordem inferior do parâmetro <em>lParam</em> for <strong>true</strong>, o botão será redesenhado.</span><span class="sxs-lookup"><span data-stu-id="73a6f-221">If the low-order word of the <em>lParam</em> parameter is <strong>TRUE</strong>, the button is redrawn.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-222"><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-222"><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-223">Verifica uma caixa de seleção ou caixa de seleção automática quando o usuário pressiona as teclas mais (+) ou igual (=).</span><span class="sxs-lookup"><span data-stu-id="73a6f-223">Checks a check box or automatic check box when the user presses the plus (+) or equal (=) keys.</span></span> <span data-ttu-id="73a6f-224">Limpa uma caixa de seleção ou caixa de seleção automática quando o usuário pressiona a tecla menos (-).</span><span class="sxs-lookup"><span data-stu-id="73a6f-224">Clears a check box or automatic check box when the user presses the minus (–) key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-225"><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-225"><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-226">Pinta o botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-226">Paints the button.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-227"><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-227"><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-228">Apaga o plano de fundo dos botões desenhados pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="73a6f-228">Erases the background for owner-drawn buttons.</span></span> <span data-ttu-id="73a6f-229">Os planos de fundo de outros botões são apagados como parte do processamento de <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> e <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="73a6f-229">The backgrounds of other buttons are erased as part of the <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> and <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-230"><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-230"><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-231">Retorna valores que indicam o tipo de entrada processada pelo procedimento de botão padrão, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="73a6f-231">Returns values that indicate the type of input processed by the default button procedure, as shown in the following table.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="73a6f-232">Estilo do botão</span><span class="sxs-lookup"><span data-stu-id="73a6f-232">Button style</span></span></th>
<th><span data-ttu-id="73a6f-233">Retornos</span><span class="sxs-lookup"><span data-stu-id="73a6f-233">Returns</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73a6f-234"><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-234"><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-235">DLGC_WANTCHARS | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="73a6f-235">DLGC_WANTCHARS | DLGC_BUTTON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-236"><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-236"><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-237">DLGC_RADIOBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="73a6f-237">DLGC_RADIOBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-238"><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-238"><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-239">DLGC_WANTCHARS | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="73a6f-239">DLGC_WANTCHARS | DLGC_BUTTON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-240"><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-240"><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-241">DLGC_DEFPUSHBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="73a6f-241">DLGC_DEFPUSHBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-242"><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-242"><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-243">DLGC_STATIC</span><span class="sxs-lookup"><span data-stu-id="73a6f-243">DLGC_STATIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-244"><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-244"><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-245">DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="73a6f-245">DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-246"><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-246"><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-247">DLGC_RADIOBUTTON | DLGC_BUTTON</span><span class="sxs-lookup"><span data-stu-id="73a6f-247">DLGC_RADIOBUTTON | DLGC_BUTTON</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-248"><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-248"><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-249">Retorna um identificador para a fonte atual.</span><span class="sxs-lookup"><span data-stu-id="73a6f-249">Returns a handle to the current font.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-250"><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-250"><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-251">Envia o botão se o usuário pressionar a barra de espaços.</span><span class="sxs-lookup"><span data-stu-id="73a6f-251">Pushes the button if the user presses the SPACEBAR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-252"><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-252"><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-253">Libera a captura do mouse para todos os casos, exceto a tecla TAB.</span><span class="sxs-lookup"><span data-stu-id="73a6f-253">Releases the mouse capture for all cases except the TAB key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-254"><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-254"><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-255">Remove o retângulo de foco de um botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-255">Removes the focus rectangle from a button.</span></span> <span data-ttu-id="73a6f-256">Para botões de push e botões de push padrão, o retângulo de foco é invalidado.</span><span class="sxs-lookup"><span data-stu-id="73a6f-256">For push buttons and default push buttons, the focus rectangle is invalidated.</span></span> <span data-ttu-id="73a6f-257">Se o botão tiver a captura do mouse, a captura será liberada, o botão não será clicado e qualquer estado de push será removido.</span><span class="sxs-lookup"><span data-stu-id="73a6f-257">If the button has the mouse capture, the capture is released, the button is not clicked, and any push state is removed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-258"><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-258"><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-259">Envia um código de notificação <a href="bn-dblclk.md">BN_DBLCLK</a> para a janela pai para botões de opção e botões desenhados pelo proprietário.</span><span class="sxs-lookup"><span data-stu-id="73a6f-259">Sends a <a href="bn-dblclk.md">BN_DBLCLK</a> notification code to the parent window for radio buttons and owner-drawn buttons.</span></span> <span data-ttu-id="73a6f-260">Para outros botões, um clique duplo é processado como uma mensagem <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="73a6f-260">For other buttons, a double-click is processed as a <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-261"><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-261"><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-262">Realça o botão se a posição do cursor do mouse estiver dentro do retângulo do cliente do botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-262">Highlights the button if the position of the mouse cursor is within the button's client rectangle.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-263"><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-263"><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-264">Libera a captura do mouse se o botão tivesse a captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="73a6f-264">Releases the mouse capture if the button had the mouse capture.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-265"><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-265"><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-266">Executa a mesma ação que <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, se o botão tiver a captura do mouse.</span><span class="sxs-lookup"><span data-stu-id="73a6f-266">Performs the same action as <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, if the button has the mouse capture.</span></span> <span data-ttu-id="73a6f-267">Caso contrário, nenhuma ação será executada.</span><span class="sxs-lookup"><span data-stu-id="73a6f-267">Otherwise, no action is performed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-268"><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-268"><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-269">Transforma qualquer botão de <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> em um botão de <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="73a6f-269">Turns any <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> button into a <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> button.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-270"><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-270"><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-271">Retorna HTTRANSPARENT, se o controle de botão for uma caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="73a6f-271">Returns HTTRANSPARENT, if the button control is a group box.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-272"><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-272"><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-273">Desenha o botão de acordo com seu estilo e o estado atual.</span><span class="sxs-lookup"><span data-stu-id="73a6f-273">Draws the button according to its style and current state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-274"><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-274"><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-275">Desenha um retângulo de foco no botão que obtém o foco.</span><span class="sxs-lookup"><span data-stu-id="73a6f-275">Draws a focus rectangle on the button getting the focus.</span></span> <span data-ttu-id="73a6f-276">Para botões de opção e botões de opção automáticos, a janela pai é enviada um código de notificação <a href="bn-clicked.md">BN_CLICKED</a> .</span><span class="sxs-lookup"><span data-stu-id="73a6f-276">For radio buttons and automatic radio buttons, the parent window is sent a <a href="bn-clicked.md">BN_CLICKED</a> notification code.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-277"><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-277"><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-278">Define uma nova fonte e, opcionalmente, atualiza a janela.</span><span class="sxs-lookup"><span data-stu-id="73a6f-278">Sets a new font and optionally updates the window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73a6f-279"><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-279"><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-280">Define o texto do botão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-280">Sets the text of the button.</span></span> <span data-ttu-id="73a6f-281">No caso de uma caixa de grupo, a mensagem pinta sobre o texto preexistente antes de repintar a caixa de grupo com o novo texto.</span><span class="sxs-lookup"><span data-stu-id="73a6f-281">In the case of a group box, the message paints over the preexisting text before repainting the group box with the new text.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73a6f-282"><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></span><span class="sxs-lookup"><span data-stu-id="73a6f-282"><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></span></span></td>
<td><span data-ttu-id="73a6f-283">Libera a captura do mouse para todos os casos, exceto a tecla TAB.</span><span class="sxs-lookup"><span data-stu-id="73a6f-283">Releases the mouse capture for all cases except the TAB key.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="73a6f-284">O procedimento de janela predefinido transmite todas as outras mensagens para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para o processamento padrão.</span><span class="sxs-lookup"><span data-stu-id="73a6f-284">The predefined window procedure passes all other messages to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function for default processing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73a6f-285">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73a6f-285">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73a6f-286">Mensagens de controle</span><span class="sxs-lookup"><span data-stu-id="73a6f-286">Control Messages</span></span>](control-messages.md)
</dt> </dl>

 

 