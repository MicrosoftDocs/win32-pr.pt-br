---
title: Barra de Status
description: Esta seção contém informações sobre os elementos de programação usados com controles de barra de status.
ms.assetid: 77923055-9d00-4528-bda7-b602a26b577f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca6e46f1c573b75439cc10aa27ae3245e47e3de9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103642147"
---
# <a name="status-bar"></a><span data-ttu-id="d9e94-103">Barra de Status</span><span class="sxs-lookup"><span data-stu-id="d9e94-103">Status Bar</span></span>

<span data-ttu-id="d9e94-104">Esta seção contém informações sobre os elementos de programação usados com controles de barra de status.</span><span class="sxs-lookup"><span data-stu-id="d9e94-104">This section contains information about the programming elements used with status bar controls.</span></span>

### <a name="overviews"></a><span data-ttu-id="d9e94-105">Visões gerais</span><span class="sxs-lookup"><span data-stu-id="d9e94-105">Overviews</span></span>



| <span data-ttu-id="d9e94-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="d9e94-106">Topic</span></span>                          | <span data-ttu-id="d9e94-107">Sumário</span><span class="sxs-lookup"><span data-stu-id="d9e94-107">Contents</span></span>                                                                                                                                                   |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9e94-108">Barras de status</span><span class="sxs-lookup"><span data-stu-id="d9e94-108">Status Bars</span></span>](status-bars.md) | <span data-ttu-id="d9e94-109">Uma *barra de status* é uma janela horizontal na parte inferior de uma janela pai na qual um aplicativo pode exibir vários tipos de informações de status.</span><span class="sxs-lookup"><span data-stu-id="d9e94-109">A *status bar* is a horizontal window at the bottom of a parent window in which an application can display various kinds of status information.</span></span><br/> |



 

### <a name="functions"></a><span data-ttu-id="d9e94-110">Funções</span><span class="sxs-lookup"><span data-stu-id="d9e94-110">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d9e94-111">Tópico</span><span class="sxs-lookup"><span data-stu-id="d9e94-111">Topic</span></span></th>
<th><span data-ttu-id="d9e94-112">Sumário</span><span class="sxs-lookup"><span data-stu-id="d9e94-112">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9e94-113"><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9e94-113"><a href="/windows/desktop/api/Commctrl/nf-commctrl-createstatuswindowa"><strong>CreateStatusWindow</strong></a></span></span></td>
<td><span data-ttu-id="d9e94-114">Cria uma janela de status, que normalmente é usada para exibir o status de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d9e94-114">Creates a status window, which is typically used to display the status of an application.</span></span> <span data-ttu-id="d9e94-115">A janela geralmente aparece na parte inferior da janela pai e contém o texto especificado.</span><span class="sxs-lookup"><span data-stu-id="d9e94-115">The window generally appears at the bottom of the parent window, and it contains the specified text.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="d9e94-116">Essa função está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="d9e94-116">This function is obsolete.</span></span> <span data-ttu-id="d9e94-117">Em vez disso, use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d9e94-117">Use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowa"><strong>CreateWindow</strong></a> instead.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9e94-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9e94-118"><a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a></span></span></td>
<td><span data-ttu-id="d9e94-119">A função <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> desenha o texto especificado no estilo de uma janela de status com bordas.</span><span class="sxs-lookup"><span data-stu-id="d9e94-119">The <a href="/windows/desktop/api/Commctrl/nf-commctrl-drawstatustexta"><strong>DrawStatusText</strong></a> function draws the specified text in the style of a status window with borders.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9e94-120"><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></span><span class="sxs-lookup"><span data-stu-id="d9e94-120"><a href="/windows/desktop/api/Commctrl/nf-commctrl-menuhelp"><strong>MenuHelp</strong></a></span></span></td>
<td><span data-ttu-id="d9e94-121">Processa <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> e <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> mensagens e exibe o texto de ajuda sobre o menu atual na janela de status especificada.</span><span class="sxs-lookup"><span data-stu-id="d9e94-121">Processes <a href="/windows/desktop/menurc/wm-menuselect"><strong>WM_MENUSELECT</strong></a> and <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> messages and displays Help text about the current menu in the specified status window.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a><span data-ttu-id="d9e94-122">Mensagens</span><span class="sxs-lookup"><span data-stu-id="d9e94-122">Messages</span></span>



| <span data-ttu-id="d9e94-123">Tópico</span><span class="sxs-lookup"><span data-stu-id="d9e94-123">Topic</span></span>                                               | <span data-ttu-id="d9e94-124">Sumário</span><span class="sxs-lookup"><span data-stu-id="d9e94-124">Contents</span></span>                                                                                                                                                                                             |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9e94-125">**$ \_ Borders SB**</span><span class="sxs-lookup"><span data-stu-id="d9e94-125">**SB\_GETBORDERS**</span></span>](sb-getborders.md)             | <span data-ttu-id="d9e94-126">Recupera as larguras atuais das bordas horizontais e verticais de uma janela de status.</span><span class="sxs-lookup"><span data-stu-id="d9e94-126">Retrieves the current widths of the horizontal and vertical borders of a status window.</span></span> <br/>                                                                                                  |
| [<span data-ttu-id="d9e94-127">**SB \_ GETicon**</span><span class="sxs-lookup"><span data-stu-id="d9e94-127">**SB\_GETICON**</span></span>](sb-geticon.md)                   | <span data-ttu-id="d9e94-128">Recupera o ícone de uma parte em uma barra de status.</span><span class="sxs-lookup"><span data-stu-id="d9e94-128">Retrieves the icon for a part in a status bar.</span></span> <br/>                                                                                                                                           |
| [<span data-ttu-id="d9e94-129">**@ @ \_ Parts SB**</span><span class="sxs-lookup"><span data-stu-id="d9e94-129">**SB\_GETPARTS**</span></span>](sb-getparts.md)                 | <span data-ttu-id="d9e94-130">Recupera uma contagem das partes em uma janela de status.</span><span class="sxs-lookup"><span data-stu-id="d9e94-130">Retrieves a count of the parts in a status window.</span></span> <span data-ttu-id="d9e94-131">A mensagem também recupera a coordenada da borda direita do número especificado de partes.</span><span class="sxs-lookup"><span data-stu-id="d9e94-131">The message also retrieves the coordinate of the right edge of the specified number of parts.</span></span> <br/>                                         |
| [<span data-ttu-id="d9e94-132">**SB \_ GETrect**</span><span class="sxs-lookup"><span data-stu-id="d9e94-132">**SB\_GETRECT**</span></span>](sb-getrect.md)                   | <span data-ttu-id="d9e94-133">Recupera o retângulo delimitador de uma parte em uma janela de status.</span><span class="sxs-lookup"><span data-stu-id="d9e94-133">Retrieves the bounding rectangle of a part in a status window.</span></span> <br/>                                                                                                                           |
| [<span data-ttu-id="d9e94-134">**SB \_ GETtext**</span><span class="sxs-lookup"><span data-stu-id="d9e94-134">**SB\_GETTEXT**</span></span>](sb-gettext.md)                   | <span data-ttu-id="d9e94-135">A mensagem de [**\_ gettext do SB**](sb-gettext.md) recupera o texto da parte especificada de uma janela de status.</span><span class="sxs-lookup"><span data-stu-id="d9e94-135">The [**SB\_GETTEXT**](sb-gettext.md) message retrieves the text from the specified part of a status window.</span></span> <br/>                                                                             |
| [<span data-ttu-id="d9e94-136">**SB \_ GETTEXTLENGTH**</span><span class="sxs-lookup"><span data-stu-id="d9e94-136">**SB\_GETTEXTLENGTH**</span></span>](sb-gettextlength.md)       | <span data-ttu-id="d9e94-137">A mensagem [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) recupera o comprimento, em caracteres, do texto da parte especificada de uma janela de status.</span><span class="sxs-lookup"><span data-stu-id="d9e94-137">The [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) message retrieves the length, in characters, of the text from the specified part of a status window.</span></span> <br/>                                   |
| [<span data-ttu-id="d9e94-138">**SB \_ GETTIPTEXT**</span><span class="sxs-lookup"><span data-stu-id="d9e94-138">**SB\_GETTIPTEXT**</span></span>](sb-gettiptext.md)             | <span data-ttu-id="d9e94-139">Recupera o texto da dica de ferramenta de uma parte em uma barra de status.</span><span class="sxs-lookup"><span data-stu-id="d9e94-139">Retrieves the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="d9e94-140">A barra de status deve ser criada com o estilo de [**\_ dicas de ferramenta SBT**](status-bar-styles.md) para habilitar dicas de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="d9e94-140">The status bar must be created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span> <br/>         |
| [<span data-ttu-id="d9e94-141">**SB \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d9e94-141">**SB\_GETUNICODEFORMAT**</span></span>](sb-getunicodeformat.md) | <span data-ttu-id="d9e94-142">Recupera o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="d9e94-142">Retrieves the Unicode character format flag for the control.</span></span> <br/>                                                                                                                             |
| [<span data-ttu-id="d9e94-143">**SB \_ ISsimples**</span><span class="sxs-lookup"><span data-stu-id="d9e94-143">**SB\_ISSIMPLE**</span></span>](sb-issimple.md)                 | <span data-ttu-id="d9e94-144">Verifica um controle de barra de status para determinar se ele está no modo simples.</span><span class="sxs-lookup"><span data-stu-id="d9e94-144">Checks a status bar control to determine if it is in simple mode.</span></span> <br/>                                                                                                                        |
| [<span data-ttu-id="d9e94-145">**SB \_ SETBKCOLOR**</span><span class="sxs-lookup"><span data-stu-id="d9e94-145">**SB\_SETBKCOLOR**</span></span>](sb-setbkcolor.md)             | <span data-ttu-id="d9e94-146">Define a cor do plano de fundo em uma barra de status.</span><span class="sxs-lookup"><span data-stu-id="d9e94-146">Sets the background color in a status bar.</span></span> <br/>                                                                                                                                               |
| [<span data-ttu-id="d9e94-147">**ÍCONE da SB \_**</span><span class="sxs-lookup"><span data-stu-id="d9e94-147">**SB\_SETICON**</span></span>](sb-seticon.md)                   | <span data-ttu-id="d9e94-148">Define o ícone de uma parte em uma barra de status.</span><span class="sxs-lookup"><span data-stu-id="d9e94-148">Sets the icon for a part in a status bar.</span></span> <br/>                                                                                                                                                |
| [<span data-ttu-id="d9e94-149">**SB \_ SETMINHEIGHT**</span><span class="sxs-lookup"><span data-stu-id="d9e94-149">**SB\_SETMINHEIGHT**</span></span>](sb-setminheight.md)         | <span data-ttu-id="d9e94-150">Define a altura mínima da área de desenho de uma janela de status.</span><span class="sxs-lookup"><span data-stu-id="d9e94-150">Sets the minimum height of a status window's drawing area.</span></span> <br/>                                                                                                                               |
| [<span data-ttu-id="d9e94-151">**conpartes da SB \_**</span><span class="sxs-lookup"><span data-stu-id="d9e94-151">**SB\_SETPARTS**</span></span>](sb-setparts.md)                 | <span data-ttu-id="d9e94-152">Define o número de partes em uma janela de status e a coordenada da borda direita de cada parte.</span><span class="sxs-lookup"><span data-stu-id="d9e94-152">Sets the number of parts in a status window and the coordinate of the right edge of each part.</span></span> <br/>                                                                                           |
| [<span data-ttu-id="d9e94-153">**SB \_ SETtext**</span><span class="sxs-lookup"><span data-stu-id="d9e94-153">**SB\_SETTEXT**</span></span>](sb-settext.md)                   | <span data-ttu-id="d9e94-154">A mensagem do SB \_ SetText define o texto na parte especificada de uma janela de status.</span><span class="sxs-lookup"><span data-stu-id="d9e94-154">The SB\_SETTEXT message sets the text in the specified part of a status window.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="d9e94-155">**SB \_ SETTIPTEXT**</span><span class="sxs-lookup"><span data-stu-id="d9e94-155">**SB\_SETTIPTEXT**</span></span>](sb-settiptext.md)             | <span data-ttu-id="d9e94-156">Define o texto da dica de ferramenta para uma parte em uma barra de status.</span><span class="sxs-lookup"><span data-stu-id="d9e94-156">Sets the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="d9e94-157">A barra de status deve ter sido criada com o estilo de [**\_ dicas de ferramenta SBT**](status-bar-styles.md) para habilitar dicas de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="d9e94-157">The status bar must have been created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span><br/>        |
| [<span data-ttu-id="d9e94-158">**SB \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="d9e94-158">**SB\_SETUNICODEFORMAT**</span></span>](sb-setunicodeformat.md) | <span data-ttu-id="d9e94-159">Define o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="d9e94-159">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="d9e94-160">Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.</span><span class="sxs-lookup"><span data-stu-id="d9e94-160">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <br/> |
| [<span data-ttu-id="d9e94-161">**SB \_ simples**</span><span class="sxs-lookup"><span data-stu-id="d9e94-161">**SB\_SIMPLE**</span></span>](sb-simple.md)                     | <span data-ttu-id="d9e94-162">Especifica se uma janela de status exibe texto simples ou exibe todas as partes da janela definidas por uma mensagem do [**SB \_ SetParts**](sb-setparts.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="d9e94-162">Specifies whether a status window displays simple text or displays all window parts set by a previous [**SB\_SETPARTS**](sb-setparts.md) message.</span></span> <br/>                                       |



 

### <a name="notifications"></a><span data-ttu-id="d9e94-163">Notificações</span><span class="sxs-lookup"><span data-stu-id="d9e94-163">Notifications</span></span>



| <span data-ttu-id="d9e94-164">Tópico</span><span class="sxs-lookup"><span data-stu-id="d9e94-164">Topic</span></span>                                                 | <span data-ttu-id="d9e94-165">Sumário</span><span class="sxs-lookup"><span data-stu-id="d9e94-165">Contents</span></span>                                                                                                                                                                                                                                                           |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9e94-166">\_Clique de nm (barra de status)</span><span class="sxs-lookup"><span data-stu-id="d9e94-166">NM\_CLICK (status bar)</span></span>](nm-click-status-bar.md)     | <span data-ttu-id="d9e94-167">Notifica a janela pai de um controle de barra de status que o usuário clicou com o botão esquerdo do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="d9e94-167">Notifies the parent window of a status bar control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="d9e94-168">[Nm \_ CLIQUE (barra de status)](nm-click-status-bar.md) é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e94-168">[NM\_CLICK (status bar)](nm-click-status-bar.md) is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>              |
| [<span data-ttu-id="d9e94-169">NM \_ DBLCLK (barra de status)</span><span class="sxs-lookup"><span data-stu-id="d9e94-169">NM\_DBLCLK (status bar)</span></span>](nm-dblclk-status-bar.md)   | <span data-ttu-id="d9e94-170">Notifica a janela pai de um controle de barra de status que o usuário clicou duas vezes com o botão esquerdo do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="d9e94-170">Notifies the parent window of a status bar control that the user has double-clicked the left mouse button within the control.</span></span> <span data-ttu-id="d9e94-171">Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e94-171">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>                                       |
| [<span data-ttu-id="d9e94-172">NM \_ RCLICK (barra de status)</span><span class="sxs-lookup"><span data-stu-id="d9e94-172">NM\_RCLICK (status bar)</span></span>](nm-rclick-status-bar.md)   | <span data-ttu-id="d9e94-173">Notifica a janela pai de um controle de barra de status que o usuário clicou com o botão direito do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="d9e94-173">Notifies the parent window of a status bar control that the user has clicked the right mouse button within the control.</span></span> <span data-ttu-id="d9e94-174">Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e94-174">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/>                                             |
| [<span data-ttu-id="d9e94-175">NM \_ RDBLCLK (barra de status)</span><span class="sxs-lookup"><span data-stu-id="d9e94-175">NM\_RDBLCLK (status bar)</span></span>](nm-rdblclk-status-bar.md) | <span data-ttu-id="d9e94-176">Notifica as janelas pai de um controle de barra de status que o usuário clicou duas vezes com o botão direito do mouse dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="d9e94-176">Notifies the parent windows of a status bar control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="d9e94-177">[Nm \_ RDBLCLK (barra de status)](nm-rdblclk-status-bar.md) é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e94-177">[NM\_RDBLCLK (status bar)](nm-rdblclk-status-bar.md) is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span><br/> |
| [<span data-ttu-id="d9e94-178">SBN \_ SIMPLEMODECHANGE</span><span class="sxs-lookup"><span data-stu-id="d9e94-178">SBN\_SIMPLEMODECHANGE</span></span>](sbn-simplemodechange.md)     | <span data-ttu-id="d9e94-179">Enviado por um controle de barra de status quando o modo simples é alterado devido a uma mensagem [**\_ simples do SB**](sb-simple.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e94-179">Sent by a status bar control when the simple mode changes due to a [**SB\_SIMPLE**](sb-simple.md) message.</span></span> <span data-ttu-id="d9e94-180">Essa notificação é enviada na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d9e94-180">This notification is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span> <br/>                                                        |



 

### <a name="constants"></a><span data-ttu-id="d9e94-181">Constantes</span><span class="sxs-lookup"><span data-stu-id="d9e94-181">Constants</span></span>



| <span data-ttu-id="d9e94-182">Tópico</span><span class="sxs-lookup"><span data-stu-id="d9e94-182">Topic</span></span>                                      | <span data-ttu-id="d9e94-183">Sumário</span><span class="sxs-lookup"><span data-stu-id="d9e94-183">Contents</span></span>                                                                                                              |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9e94-184">Estilos da barra de status</span><span class="sxs-lookup"><span data-stu-id="d9e94-184">Status Bar Styles</span></span>](status-bar-styles.md) | <span data-ttu-id="d9e94-185">Esta seção lista os estilos, além dos estilos de janela padrão, suportados pelos controles de *barra de status* .</span><span class="sxs-lookup"><span data-stu-id="d9e94-185">This section lists the styles, in addition to standard window styles, supported by *status bar* controls.</span></span> <br/> |



 

 

