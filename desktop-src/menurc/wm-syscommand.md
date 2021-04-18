---
title: Mensagem de WM_SYSCOMMAND (WinUser. h)
description: Uma janela recebe essa mensagem quando o usuário escolhe um comando no menu janela (anteriormente conhecido como menu do sistema ou controle) ou quando o usuário escolhe o botão Maximizar, o botão minimizar, o botão restaurar ou o botão fechar.
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- WM_SYSCOMMAND menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_SYSCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 25596f30457063bc90124f14489963507f85ff70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813504"
---
# <a name="wm_syscommand-message"></a><span data-ttu-id="bcc8e-104">Mensagem do WM \_ SYSCOMMAND</span><span class="sxs-lookup"><span data-stu-id="bcc8e-104">WM\_SYSCOMMAND message</span></span>

<span data-ttu-id="bcc8e-105">Uma janela recebe essa mensagem quando o usuário escolhe um comando no menu **janela** (anteriormente conhecido como menu do sistema ou controle) ou quando o usuário escolhe o botão Maximizar, o botão minimizar, o botão restaurar ou o botão fechar.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-105">A window receives this message when the user chooses a command from the **Window** menu (formerly known as the system or control menu) or when the user chooses the maximize button, minimize button, restore button, or close button.</span></span>


```C++
#define WM_SYSCOMMAND                   0x0112
```

## <a name="example"></a><span data-ttu-id="bcc8e-106">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bcc8e-106">Example</span></span>

```cpp
 case WM_SYSCOMMAND:
        if (wParam == SC_CLOSE)
        {
            EndDialog (hDlg, TRUE);
            return(TRUE);
        }
        break;

```
<span data-ttu-id="bcc8e-107">Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) no github.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-107">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) on GitHub.</span></span>

## <a name="parameters"></a><span data-ttu-id="bcc8e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bcc8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcc8e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bcc8e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bcc8e-110">O tipo de comando do sistema solicitado.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-110">The type of system command requested.</span></span> <span data-ttu-id="bcc8e-111">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-111">This parameter can be one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bcc8e-112">Valor</span><span class="sxs-lookup"><span data-stu-id="bcc8e-112">Value</span></span></th>
<th><span data-ttu-id="bcc8e-113">Significado</span><span class="sxs-lookup"><span data-stu-id="bcc8e-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SC_CLOSE"></span><span id="sc_close"></span><dl> <span data-ttu-id="bcc8e-114"><dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-114"><dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-115">Fecha a janela.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-115">Closes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl> <span data-ttu-id="bcc8e-116"><dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-116"><dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-117">Altera o cursor para um ponto de interrogação com um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-117">Changes the cursor to a question mark with a pointer.</span></span> <span data-ttu-id="bcc8e-118">Se o usuário clicar em um controle na caixa de diálogo, o controle receberá uma mensagem de <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="bcc8e-118">If the user then clicks a control in the dialog box, the control receives a <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> message.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_DEFAULT"></span><span id="sc_default"></span><dl> <span data-ttu-id="bcc8e-119"><dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-119"><dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-120">Seleciona o item padrão; o usuário clicou duas vezes no menu janela.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-120">Selects the default item; the user double-clicked the window menu.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl> <span data-ttu-id="bcc8e-121"><dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-121"><dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-122">Ativa a janela associada à tecla de acesso especificada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-122">Activates the window associated with the application-specified hot key.</span></span> <span data-ttu-id="bcc8e-123">O parâmetro <em>lParam</em> identifica a janela a ser ativada.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-123">The <em>lParam</em> parameter identifies the window to activate.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl> <span data-ttu-id="bcc8e-124"><dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-124"><dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-125">Rola horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-125">Scrolls horizontally.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl> <span data-ttu-id="bcc8e-126"><dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-126"><dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-127">Indica se a proteção de tela é segura.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-127">Indicates whether the screen saver is secure.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl> <span data-ttu-id="bcc8e-128"><dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-128"><dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-129">Recupera o menu janela como resultado de um pressionamento de tecla.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-129">Retrieves the window menu as a result of a keystroke.</span></span> <span data-ttu-id="bcc8e-130">Para obter mais informações, consulte a seção Comentários.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-130">For more information, see the Remarks section.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl> <span data-ttu-id="bcc8e-131"><dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-131"><dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-132">Maximiza a janela.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-132">Maximizes the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl> <span data-ttu-id="bcc8e-133"><dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-133"><dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-134">Minimiza a janela.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-134">Minimizes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl> <span data-ttu-id="bcc8e-135"><dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-135"><dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-136">Define o estado da exibição.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-136">Sets the state of the display.</span></span> <span data-ttu-id="bcc8e-137">Esse comando dá suporte a dispositivos que têm recursos de economia de energia, como um computador pessoal alimentado por bateria.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-137">This command supports devices that have power-saving features, such as a battery-powered personal computer.</span></span> <br/> <span data-ttu-id="bcc8e-138">O parâmetro <em>lParam</em> pode ter os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="bcc8e-138">The <em>lParam</em> parameter can have the following values:</span></span><br/>
<ul>
<li><span data-ttu-id="bcc8e-139">-1 (a tela está ligando)</span><span class="sxs-lookup"><span data-stu-id="bcc8e-139">-1 (the display is powering on)</span></span></li>
<li><span data-ttu-id="bcc8e-140">1 (a exibição vai ser de baixa energia)</span><span class="sxs-lookup"><span data-stu-id="bcc8e-140">1 (the display is going to low power)</span></span></li>
<li><span data-ttu-id="bcc8e-141">2 (a exibição está sendo desligada)</span><span class="sxs-lookup"><span data-stu-id="bcc8e-141">2 (the display is being shut off)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl> <span data-ttu-id="bcc8e-142"><dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-142"><dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-143">Recupera o menu janela como resultado de um clique do mouse.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-143">Retrieves the window menu as a result of a mouse click.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_MOVE"></span><span id="sc_move"></span><dl> <span data-ttu-id="bcc8e-144"><dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-144"><dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-145">Move a janela.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-145">Moves the window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl> <span data-ttu-id="bcc8e-146"><dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-146"><dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-147">Move para a próxima janela.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-147">Moves to the next window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl> <span data-ttu-id="bcc8e-148"><dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-148"><dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-149">Move para a janela anterior.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-149">Moves to the previous window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_RESTORE"></span><span id="sc_restore"></span><dl> <span data-ttu-id="bcc8e-150"><dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-150"><dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-151">Restaura a posição e o tamanho normais da janela.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-151">Restores the window to its normal position and size.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl> <span data-ttu-id="bcc8e-152"><dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-152"><dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-153">Executa o aplicativo de proteção de tela especificado na seção [boot] do arquivo System.ini.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-153">Executes the screen saver application specified in the [boot] section of the System.ini file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_SIZE"></span><span id="sc_size"></span><dl> <span data-ttu-id="bcc8e-154"><dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-154"><dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-155">Dimensiona a janela.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-155">Sizes the window.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl> <span data-ttu-id="bcc8e-156"><dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-156"><dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-157">Ativa o menu <strong>Iniciar</strong> .</span><span class="sxs-lookup"><span data-stu-id="bcc8e-157">Activates the <strong>Start</strong> menu.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl> <span data-ttu-id="bcc8e-158"><dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </span><span class="sxs-lookup"><span data-stu-id="bcc8e-158"><dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </span></span></dl></td>
<td><span data-ttu-id="bcc8e-159">Rola verticalmente.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-159">Scrolls vertically.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="bcc8e-160">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bcc8e-160">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bcc8e-161">A palavra de ordem inferior Especifica a posição horizontal do cursor, em coordenadas de tela, se um comando de menu de janela for escolhido com o mouse.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-161">The low-order word specifies the horizontal position of the cursor, in screen coordinates, if a window menu command is chosen with the mouse.</span></span> <span data-ttu-id="bcc8e-162">Caso contrário, esse parâmetro não será usado.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-162">Otherwise, this parameter is not used.</span></span>

<span data-ttu-id="bcc8e-163">A palavra de ordem superior especifica a posição vertical do cursor, em coordenadas de tela, se um comando de menu de janela for escolhido com o mouse.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-163">The high-order word specifies the vertical position of the cursor, in screen coordinates, if a window menu command is chosen with the mouse.</span></span> <span data-ttu-id="bcc8e-164">Esse parâmetro será 1 se o comando for escolhido usando um acelerador do sistema ou zero se estiver usando um mnemônico.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-164">This parameter is  1 if the command is chosen using a system accelerator, or zero if using a mnemonic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcc8e-165">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bcc8e-165">Return value</span></span>

<span data-ttu-id="bcc8e-166">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-166">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcc8e-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="bcc8e-167">Remarks</span></span>

<span data-ttu-id="bcc8e-168">Para obter as coordenadas de posição nas coordenadas da tela, use o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="bcc8e-168">To obtain the position coordinates in screen coordinates, use the following code:</span></span>


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



<span data-ttu-id="bcc8e-169">A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) executa a solicitação de menu de janela para as ações predefinidas especificadas na tabela anterior.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-169">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function carries out the window menu request for the predefined actions specified in the previous table.</span></span>

<span data-ttu-id="bcc8e-170">Em mensagens do **WM \_ SYSCOMMAND** , os quatro bits de ordem inferior do parâmetro *wParam* são usados internamente pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-170">In **WM\_SYSCOMMAND** messages, the four low-order bits of the *wParam* parameter are used internally by the system.</span></span> <span data-ttu-id="bcc8e-171">Para obter o resultado correto ao testar o valor de *wParam*, um aplicativo deve combinar o valor 0xFFF0 com o valor *wParam* usando o operador and de bit a passo.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-171">To obtain the correct result when testing the value of *wParam*, an application must combine the value 0xFFF0 with the *wParam* value by using the bitwise AND operator.</span></span>

<span data-ttu-id="bcc8e-172">Os itens de menu em um menu de janela podem ser modificados usando as funções [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)e [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) .</span><span class="sxs-lookup"><span data-stu-id="bcc8e-172">The menu items in a window menu can be modified by using the [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema), and [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) functions.</span></span> <span data-ttu-id="bcc8e-173">Os aplicativos que modificam o menu janela devem processar mensagens do **WM \_ SYSCOMMAND** .</span><span class="sxs-lookup"><span data-stu-id="bcc8e-173">Applications that modify the window menu must process **WM\_SYSCOMMAND** messages.</span></span>

<span data-ttu-id="bcc8e-174">Um aplicativo pode executar qualquer comando do sistema a qualquer momento, passando uma mensagem do **WM \_ SYSCOMMAND** para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="bcc8e-174">An application can carry out any system command at any time by passing a **WM\_SYSCOMMAND** message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="bcc8e-175">Todas as mensagens do **WM \_ SYSCOMMAND** não tratadas pelo aplicativo devem ser passadas para **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-175">Any **WM\_SYSCOMMAND** messages not handled by the application must be passed to **DefWindowProc**.</span></span> <span data-ttu-id="bcc8e-176">Qualquer valor de comando adicionado por um aplicativo deve ser processado pelo aplicativo e não pode ser passado para **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-176">Any command values added by an application must be processed by the application and cannot be passed to **DefWindowProc**.</span></span>

<span data-ttu-id="bcc8e-177">Se a proteção por senha estiver habilitada pela política, a proteção de tela será iniciada, independentemente do que um aplicativo faz com a notificação **sc \_ SCREENSAVE** , mesmo se não conseguir passá-la para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="bcc8e-177">If password protection is enabled by policy, the screen saver is started regardless of what an application does with the **SC\_SCREENSAVE** notification even if fails to pass it to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span>

<span data-ttu-id="bcc8e-178">As teclas de aceleração definidas para escolher itens no menu janela são convertidas em mensagens do **WM \_ SYSCOMMAND** ; todos os outros pressionamentos de teclas do acelerador são convertidos em mensagens de [**\_ comando do WM**](wm-command.md) .</span><span class="sxs-lookup"><span data-stu-id="bcc8e-178">Accelerator keys that are defined to choose items from the window menu are translated into **WM\_SYSCOMMAND** messages; all other accelerator keystrokes are translated into [**WM\_COMMAND**](wm-command.md) messages.</span></span>

<span data-ttu-id="bcc8e-179">Se *wParam* for **sc \_ keymenu**, *lParam* conterá o código de caractere da chave que é usada com a tecla Alt para exibir o menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-179">If the *wParam* is **SC\_KEYMENU**, *lParam* contains the character code of the key that is used with the ALT key to display the popup menu.</span></span> <span data-ttu-id="bcc8e-180">Por exemplo, pressionar ALT + F para exibir o arquivo pop-up causará uma **\_ SYSCOMMAND do WM** com *wParam* igual a **sc \_ keymenu** e *lParam* igual a ' F '.</span><span class="sxs-lookup"><span data-stu-id="bcc8e-180">For example, pressing ALT+F to display the File popup will cause a **WM\_SYSCOMMAND** with *wParam* equal to **SC\_KEYMENU** and *lParam* equal to 'f'.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcc8e-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcc8e-181">Requirements</span></span>



| <span data-ttu-id="bcc8e-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcc8e-182">Requirement</span></span> | <span data-ttu-id="bcc8e-183">Valor</span><span class="sxs-lookup"><span data-stu-id="bcc8e-183">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcc8e-184">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcc8e-184">Minimum supported client</span></span><br/> | <span data-ttu-id="bcc8e-185">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bcc8e-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bcc8e-186">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcc8e-186">Minimum supported server</span></span><br/> | <span data-ttu-id="bcc8e-187">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bcc8e-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bcc8e-188">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bcc8e-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcc8e-189"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bcc8e-189"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcc8e-190">Confira também</span><span class="sxs-lookup"><span data-stu-id="bcc8e-190">See also</span></span>

<dl> <dt>

<span data-ttu-id="bcc8e-191">**Referência**</span><span class="sxs-lookup"><span data-stu-id="bcc8e-191">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="bcc8e-192">**AppendMenu**</span><span class="sxs-lookup"><span data-stu-id="bcc8e-192">**AppendMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[<span data-ttu-id="bcc8e-193">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="bcc8e-193">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="bcc8e-194">**OBTER \_ X \_ lParam**</span><span class="sxs-lookup"><span data-stu-id="bcc8e-194">**GET\_X\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[<span data-ttu-id="bcc8e-195">**OBTER \_ \_ lParam Y**</span><span class="sxs-lookup"><span data-stu-id="bcc8e-195">**GET\_Y\_LPARAM**</span></span>](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[<span data-ttu-id="bcc8e-196">**GetSystemMenu**</span><span class="sxs-lookup"><span data-stu-id="bcc8e-196">**GetSystemMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[<span data-ttu-id="bcc8e-197">**InsertMenu**</span><span class="sxs-lookup"><span data-stu-id="bcc8e-197">**InsertMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[<span data-ttu-id="bcc8e-198">**ModifyMenu**</span><span class="sxs-lookup"><span data-stu-id="bcc8e-198">**ModifyMenu**</span></span>](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[<span data-ttu-id="bcc8e-199">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="bcc8e-199">**WM\_COMMAND**</span></span>](wm-command.md)
</dt> <dt>

<span data-ttu-id="bcc8e-200">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="bcc8e-200">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bcc8e-201">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="bcc8e-201">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

