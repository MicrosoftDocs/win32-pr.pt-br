---
title: Entrada de teclado (introdução ao Win32 e ao C++)
description: Entrada de teclado
ms.assetid: FC682E8B-8360-4D58-AC42-4CEFD9CB750F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82065d4024428b48d4d3061da31a5384cab417d2
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "105759488"
---
# <a name="keyboard-input-get-started-with-win32-and-c"></a><span data-ttu-id="79039-103">Entrada de teclado (introdução ao Win32 e ao C++)</span><span class="sxs-lookup"><span data-stu-id="79039-103">Keyboard Input (Get Started with Win32 and C++)</span></span>

<span data-ttu-id="79039-104">O teclado é usado para vários tipos distintos de entrada, incluindo:</span><span class="sxs-lookup"><span data-stu-id="79039-104">The keyboard is used for several distinct types of input, including:</span></span>

-   <span data-ttu-id="79039-105">Entrada de caracteres.</span><span class="sxs-lookup"><span data-stu-id="79039-105">Character input.</span></span> <span data-ttu-id="79039-106">Texto que o usuário digita em um documento ou caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="79039-106">Text that the user types into a document or edit box.</span></span>
-   <span data-ttu-id="79039-107">Atalhos de teclado.</span><span class="sxs-lookup"><span data-stu-id="79039-107">Keyboard shortcuts.</span></span> <span data-ttu-id="79039-108">Traços de chave que invocam funções de aplicativo; por exemplo, CTRL + O para abrir um arquivo.</span><span class="sxs-lookup"><span data-stu-id="79039-108">Key strokes that invoke application functions; for example, CTRL + O to open a file.</span></span>
-   <span data-ttu-id="79039-109">Comandos do sistema.</span><span class="sxs-lookup"><span data-stu-id="79039-109">System commands.</span></span> <span data-ttu-id="79039-110">Traços de chave que invocam funções do sistema; por exemplo, ALT + TAB para alternar janelas.</span><span class="sxs-lookup"><span data-stu-id="79039-110">Key strokes that invoke system functions; for example, ALT + TAB to switch windows.</span></span>

<span data-ttu-id="79039-111">Ao pensar sobre a entrada do teclado, é importante lembrar que um traço de chave não é o mesmo que um caractere.</span><span class="sxs-lookup"><span data-stu-id="79039-111">When thinking about keyboard input, it is important to remember that a key stroke is not the same as a character.</span></span> <span data-ttu-id="79039-112">Por exemplo, pressionar a tecla a pode resultar em qualquer um dos caracteres a seguir.</span><span class="sxs-lookup"><span data-stu-id="79039-112">For example, pressing the A key could result in any of the following characters.</span></span>

-   <span data-ttu-id="79039-113">um</span><span class="sxs-lookup"><span data-stu-id="79039-113">a</span></span>
-   <span data-ttu-id="79039-114">Um</span><span class="sxs-lookup"><span data-stu-id="79039-114">A</span></span>
-   <span data-ttu-id="79039-115">á (se o teclado der suporte à combinação de diacríticos)</span><span class="sxs-lookup"><span data-stu-id="79039-115">á (if the keyboard supports combining diacritics)</span></span>

<span data-ttu-id="79039-116">Além disso, se a tecla ALT for mantida pressionada, pressionar a tecla a produz ALT + A, que o sistema não trata como um caractere, mas sim como um comando do sistema.</span><span class="sxs-lookup"><span data-stu-id="79039-116">Further, if the ALT key is held down, pressing the A key produces ALT+A, which the system does not treat as a character at all, but rather as a system command.</span></span>

## <a name="key-codes"></a><span data-ttu-id="79039-117">Códigos-chave</span><span class="sxs-lookup"><span data-stu-id="79039-117">Key Codes</span></span>

<span data-ttu-id="79039-118">Quando você pressiona uma tecla, o hardware gera um *código de verificação*.</span><span class="sxs-lookup"><span data-stu-id="79039-118">When you press a key, the hardware generates a *scan code*.</span></span> <span data-ttu-id="79039-119">Os códigos de verificação variam de um teclado para o outro e há códigos de verificação separados para eventos de tecla para cima e para baixo.</span><span class="sxs-lookup"><span data-stu-id="79039-119">Scan codes vary from one keyboard to the next, and there are separate scan codes for key-up and key-down events.</span></span> <span data-ttu-id="79039-120">Você quase nunca se preocupa com códigos de verificação.</span><span class="sxs-lookup"><span data-stu-id="79039-120">You will almost never care about scan codes.</span></span> <span data-ttu-id="79039-121">O driver de teclado traduz códigos de verificação em *códigos de chave virtual*.</span><span class="sxs-lookup"><span data-stu-id="79039-121">The keyboard driver translates scan codes into *virtual-key codes*.</span></span> <span data-ttu-id="79039-122">Os códigos de chave virtual são independentes de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="79039-122">Virtual-key codes are device-independent.</span></span> <span data-ttu-id="79039-123">Pressionar a tecla a em qualquer teclado gera o mesmo código de chave virtual.</span><span class="sxs-lookup"><span data-stu-id="79039-123">Pressing the A key on any keyboard generates the same virtual-key code.</span></span>

<span data-ttu-id="79039-124">Em geral, os códigos de chave virtual não correspondem a códigos ASCII ou a qualquer outro padrão de codificação de caracteres.</span><span class="sxs-lookup"><span data-stu-id="79039-124">In general, virtual-key codes do not correspond to ASCII codes or any other character-encoding standard.</span></span> <span data-ttu-id="79039-125">Isso é óbvio se você pensar nisso, porque a mesma chave pode gerar caracteres diferentes (a, A, á) e algumas chaves, como teclas de função, não correspondem a nenhum caractere.</span><span class="sxs-lookup"><span data-stu-id="79039-125">This is obvious if you think about it, because the same key can generate different characters (a, A, á), and some keys, such as function keys, do not correspond to any character.</span></span>

<span data-ttu-id="79039-126">Dito isso, os seguintes códigos de chave virtual mapeiam para equivalentes ASCII:</span><span class="sxs-lookup"><span data-stu-id="79039-126">That said, the following virtual-key codes do map to ASCII equivalents:</span></span>

-   <span data-ttu-id="79039-127">0 a 9 chaves = ASCII ' 0 ' – ' 9 ' (0x30 – 0x39)</span><span class="sxs-lookup"><span data-stu-id="79039-127">0 through 9 keys = ASCII '0' – '9' (0x30 – 0x39)</span></span>
-   <span data-ttu-id="79039-128">A a Z Keys = ASCII ' A ' – ' Z ' (0x41 – 0x5A)</span><span class="sxs-lookup"><span data-stu-id="79039-128">A through Z keys = ASCII 'A' – 'Z' (0x41 – 0x5A)</span></span>

<span data-ttu-id="79039-129">Em alguns aspectos, esse mapeamento é incerto, pois você nunca deve considerar os códigos de chave virtual como caracteres, pelos motivos discutidos.</span><span class="sxs-lookup"><span data-stu-id="79039-129">In some respects this mapping is unfortunate, because you should never think of virtual-key codes as characters, for the reasons discussed.</span></span>

<span data-ttu-id="79039-130">O arquivo de cabeçalho WinUser. h define constantes para a maioria dos códigos de chave virtual.</span><span class="sxs-lookup"><span data-stu-id="79039-130">The header file WinUser.h defines constants for most of the virtual-key codes.</span></span> <span data-ttu-id="79039-131">Por exemplo, o código de chave virtual para a tecla de seta para a esquerda é **VK \_ esquerdo** (0x25).</span><span class="sxs-lookup"><span data-stu-id="79039-131">For example, the virtual-key code for the LEFT ARROW key is **VK\_LEFT** (0x25).</span></span> <span data-ttu-id="79039-132">Para obter a lista completa de códigos de chave virtual, consulte [**códigos de chave virtual**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="79039-132">For the complete list of virtual-key codes, see [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span> <span data-ttu-id="79039-133">Nenhuma constante é definida para os códigos de chave virtual que correspondem a valores ASCII.</span><span class="sxs-lookup"><span data-stu-id="79039-133">No constants are defined for the virtual-key codes that match ASCII values.</span></span> <span data-ttu-id="79039-134">Por exemplo, o código de chave virtual para a chave é 0x41, mas não há nenhuma constante chamada **VK \_ A**.</span><span class="sxs-lookup"><span data-stu-id="79039-134">For example, the virtual-key code for the A key is 0x41, but there is no constant named **VK\_A**.</span></span> <span data-ttu-id="79039-135">Em vez disso, basta usar o valor numérico.</span><span class="sxs-lookup"><span data-stu-id="79039-135">Instead, just use the numeric value.</span></span>

## <a name="key-down-and-key-up-messages"></a><span data-ttu-id="79039-136">Mensagens de Key-Down e Key-Up</span><span class="sxs-lookup"><span data-stu-id="79039-136">Key-Down and Key-Up Messages</span></span>

<span data-ttu-id="79039-137">Quando você pressiona uma tecla, a janela que tem o foco do teclado recebe uma das mensagens a seguir.</span><span class="sxs-lookup"><span data-stu-id="79039-137">When you press a key, the window that has keyboard focus receives one of the following messages.</span></span>

-   [<span data-ttu-id="79039-138">**SYSKEYDOWN do WM \_**</span><span class="sxs-lookup"><span data-stu-id="79039-138">**WM\_SYSKEYDOWN**</span></span>](/windows/desktop/inputdev/wm-syskeydown)
-   [<span data-ttu-id="79039-139">**o WM \_ KEYDOWN**</span><span class="sxs-lookup"><span data-stu-id="79039-139">**WM\_KEYDOWN**</span></span>](/windows/desktop/inputdev/wm-keydown)

<span data-ttu-id="79039-140">A mensagem do [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) indica uma *chave do sistema*, que é um traço de chave que invoca um comando do sistema.</span><span class="sxs-lookup"><span data-stu-id="79039-140">The [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message indicates a *system key*, which is a key stroke that invokes a system command.</span></span> <span data-ttu-id="79039-141">Há dois tipos de chave do sistema:</span><span class="sxs-lookup"><span data-stu-id="79039-141">There are two types of system key:</span></span>

-   <span data-ttu-id="79039-142">ALT + qualquer tecla</span><span class="sxs-lookup"><span data-stu-id="79039-142">ALT + any key</span></span>
-   <span data-ttu-id="79039-143">F10</span><span class="sxs-lookup"><span data-stu-id="79039-143">F10</span></span>

<span data-ttu-id="79039-144">A tecla F10 ativa a barra de menus de uma janela.</span><span class="sxs-lookup"><span data-stu-id="79039-144">The F10 key activates the menu bar of a window.</span></span> <span data-ttu-id="79039-145">Várias combinações de teclas ALT invocam comandos do sistema.</span><span class="sxs-lookup"><span data-stu-id="79039-145">Various ALT-key combinations invoke system commands.</span></span> <span data-ttu-id="79039-146">Por exemplo, ALT + TAB alterna para uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="79039-146">For example, ALT + TAB switches to a new window.</span></span> <span data-ttu-id="79039-147">Além disso, se uma janela tiver um menu, a tecla ALT poderá ser usada para ativar itens de menu.</span><span class="sxs-lookup"><span data-stu-id="79039-147">In addition, if a window has a menu, the ALT key can be used to activate menu items.</span></span> <span data-ttu-id="79039-148">Algumas combinações de teclas ALT não fazem nada.</span><span class="sxs-lookup"><span data-stu-id="79039-148">Some ALT key combinations do not do anything.</span></span>

<span data-ttu-id="79039-149">Todos os outros traços de chave são considerados chaves não do sistema e produzem a mensagem do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="79039-149">All other key strokes are considered nonsystem keys and produce the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message.</span></span> <span data-ttu-id="79039-150">Isso inclui as teclas de função diferentes de F10.</span><span class="sxs-lookup"><span data-stu-id="79039-150">This includes the function keys other than F10.</span></span>

<span data-ttu-id="79039-151">Quando você libera uma chave, o sistema envia uma mensagem de chave correspondente:</span><span class="sxs-lookup"><span data-stu-id="79039-151">When you release a key, the system sends a corresponding key-up message:</span></span>

-   [<span data-ttu-id="79039-152">**o WM \_ KEYUP**</span><span class="sxs-lookup"><span data-stu-id="79039-152">**WM\_KEYUP**</span></span>](/windows/desktop/inputdev/wm-keyup)
-   [<span data-ttu-id="79039-153">**SYSKEYUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="79039-153">**WM\_SYSKEYUP**</span></span>](/windows/desktop/inputdev/wm-syskeyup)

<span data-ttu-id="79039-154">Se você mantiver uma chave longa o suficiente para iniciar o recurso de repetição do teclado, o sistema enviará várias mensagens de chave para baixo, seguidos por uma única mensagem de chave.</span><span class="sxs-lookup"><span data-stu-id="79039-154">If you hold down a key long enough to start the keyboard's repeat feature, the system sends multiple key-down messages, followed by a single key-up message.</span></span>

<span data-ttu-id="79039-155">Em todas as quatro mensagens de teclado discutidas até agora, o parâmetro *wParam* contém o código de chave virtual da chave.</span><span class="sxs-lookup"><span data-stu-id="79039-155">In all four of the keyboard messages discussed so far, the *wParam* parameter contains the virtual-key code of the key.</span></span> <span data-ttu-id="79039-156">O parâmetro *lParam* contém algumas informações diversas incluídas em 32 bits.</span><span class="sxs-lookup"><span data-stu-id="79039-156">The *lParam* parameter contains some miscellaneous information packed into 32 bits.</span></span> <span data-ttu-id="79039-157">Normalmente, você não precisa das informações no *lParam*.</span><span class="sxs-lookup"><span data-stu-id="79039-157">You typically do not need the information in *lParam*.</span></span> <span data-ttu-id="79039-158">Um sinalizador que pode ser útil é o bit 30, o sinalizador "estado de chave anterior", que é definido como 1 para mensagens de chave suspensa repetidas.</span><span class="sxs-lookup"><span data-stu-id="79039-158">One flag that might be useful is bit 30, the "previous key state" flag, which is set to 1 for repeated key-down messages.</span></span>

<span data-ttu-id="79039-159">Como o nome indica, os traços de chave do sistema são destinados principalmente para uso pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="79039-159">As the name implies, system key strokes are primarily intended for use by the operating system.</span></span> <span data-ttu-id="79039-160">Se você interceptar a mensagem do [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) , chame [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) posteriormente.</span><span class="sxs-lookup"><span data-stu-id="79039-160">If you intercept the [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message, call [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) afterward.</span></span> <span data-ttu-id="79039-161">Caso contrário, você impedirá que o sistema operacional trate o comando.</span><span class="sxs-lookup"><span data-stu-id="79039-161">Otherwise, you will block the operating system from handling the command.</span></span>

## <a name="character-messages"></a><span data-ttu-id="79039-162">Mensagens de caracteres</span><span class="sxs-lookup"><span data-stu-id="79039-162">Character Messages</span></span>

<span data-ttu-id="79039-163">Os traços de chave são convertidos em caracteres pela função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) , que vimos primeiro no [módulo 1](your-first-windows-program.md).</span><span class="sxs-lookup"><span data-stu-id="79039-163">Key strokes are converted into characters by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function, which we first saw in [Module 1](your-first-windows-program.md).</span></span> <span data-ttu-id="79039-164">Essa função examina as mensagens de chave e as converte em caracteres.</span><span class="sxs-lookup"><span data-stu-id="79039-164">This function examines key-down messages and translates them into characters.</span></span> <span data-ttu-id="79039-165">Para cada caractere produzido, a função **TranslateMessage** coloca uma mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) ou do [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) na fila de mensagens da janela.</span><span class="sxs-lookup"><span data-stu-id="79039-165">For each character that is produced, the **TranslateMessage** function puts a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) or [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) message on the message queue of the window.</span></span> <span data-ttu-id="79039-166">O parâmetro *wParam* da mensagem contém o caractere UTF-16.</span><span class="sxs-lookup"><span data-stu-id="79039-166">The *wParam* parameter of the message contains the UTF-16 character.</span></span>

<span data-ttu-id="79039-167">Como você pode imaginar, as mensagens do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) são geradas de mensagens do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) , enquanto as mensagens do WM [**\_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) são geradas de mensagens do [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) .</span><span class="sxs-lookup"><span data-stu-id="79039-167">As you might guess, [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) messages are generated from [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages, while [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) messages are generated from [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) messages.</span></span> <span data-ttu-id="79039-168">Por exemplo, suponha que o usuário pressione a tecla SHIFT seguida da tecla a.</span><span class="sxs-lookup"><span data-stu-id="79039-168">For example, suppose the user presses the SHIFT key followed by the A key.</span></span> <span data-ttu-id="79039-169">Supondo um layout de teclado padrão, você obteria a seguinte sequência de mensagens:</span><span class="sxs-lookup"><span data-stu-id="79039-169">Assuming a standard keyboard layout, you would get the following sequence of messages:</span></span>

<span data-ttu-id="79039-170">**WM \_ KEYDOWN**: Shift</span><span class="sxs-lookup"><span data-stu-id="79039-170">**WM\_KEYDOWN**: SHIFT</span></span>  
<span data-ttu-id="79039-171">**WM \_ KEYDOWN**: A</span><span class="sxs-lookup"><span data-stu-id="79039-171">**WM\_KEYDOWN**: A</span></span>  
<span data-ttu-id="79039-172">**WM \_ CHAR**: ' A '</span><span class="sxs-lookup"><span data-stu-id="79039-172">**WM\_CHAR**: 'A'</span></span>  


<span data-ttu-id="79039-173">Por outro lado, a combinação ALT + P geraria:</span><span class="sxs-lookup"><span data-stu-id="79039-173">On the other hand, the combination ALT + P would generate:</span></span>

 <span data-ttu-id="79039-174">**WM \_ SYSKEYDOWN**: \_ menu VK</span><span class="sxs-lookup"><span data-stu-id="79039-174">**WM\_SYSKEYDOWN**: VK\_MENU</span></span>  
<span data-ttu-id="79039-175">**WM \_ SYSKEYDOWN**: 0x50</span><span class="sxs-lookup"><span data-stu-id="79039-175">**WM\_SYSKEYDOWN**: 0x50</span></span>  
<span data-ttu-id="79039-176">**WM \_ SYSCHAR**: ' p '</span><span class="sxs-lookup"><span data-stu-id="79039-176">**WM\_SYSCHAR**: 'p'</span></span>  
<span data-ttu-id="79039-177">**WM \_ SYSKEYUP**: 0x50</span><span class="sxs-lookup"><span data-stu-id="79039-177">**WM\_SYSKEYUP**: 0x50</span></span>  
<span data-ttu-id="79039-178">**WM \_ MENU KEYUP**: VK \_</span><span class="sxs-lookup"><span data-stu-id="79039-178">**WM\_KEYUP**: VK\_MENU</span></span>  


<span data-ttu-id="79039-179">(O código de chave virtual para a tecla ALT é chamado de VK \_ MENU por motivos históricos.)</span><span class="sxs-lookup"><span data-stu-id="79039-179">(The virtual-key code for the ALT key is named VK\_MENU for historical reasons.)</span></span>

<span data-ttu-id="79039-180">A mensagem do [**WM \_ SYSCHAR**](/windows/desktop/menurc/wm-syschar) indica um caractere do sistema.</span><span class="sxs-lookup"><span data-stu-id="79039-180">The [**WM\_SYSCHAR**](/windows/desktop/menurc/wm-syschar) message indicates a system character.</span></span> <span data-ttu-id="79039-181">Assim como com o [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), você geralmente deve passar essa mensagem diretamente para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="79039-181">As with [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown), you should generally pass this message directly to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="79039-182">Caso contrário, você pode interferir com os comandos padrão do sistema.</span><span class="sxs-lookup"><span data-stu-id="79039-182">Otherwise, you may interfere with standard system commands.</span></span> <span data-ttu-id="79039-183">Em particular, não trate o **WM \_ SYSCHAR** como texto digitado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="79039-183">In particular, do not treat **WM\_SYSCHAR** as text that the user has typed.</span></span>

<span data-ttu-id="79039-184">A mensagem do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) é o que você normalmente considera como entrada de caracteres.</span><span class="sxs-lookup"><span data-stu-id="79039-184">The [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message is what you normally think of as character input.</span></span> <span data-ttu-id="79039-185">O tipo de dados do caractere é **WCHAR \_ t**, representando um caractere Unicode UTF-16.</span><span class="sxs-lookup"><span data-stu-id="79039-185">The data type for the character is **wchar\_t**, representing a UTF-16 Unicode character.</span></span> <span data-ttu-id="79039-186">A entrada de caracteres pode incluir caracteres fora do intervalo ASCII, especialmente com layouts de teclado que são comumente usados fora do Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="79039-186">Character input can include characters outside the ASCII range, especially with keyboard layouts that are commonly used outside of the United States.</span></span> <span data-ttu-id="79039-187">Você pode experimentar diferentes layouts de teclado instalando um teclado regional e, em seguida, usando o recurso de teclado na tela.</span><span class="sxs-lookup"><span data-stu-id="79039-187">You can try different keyboard layouts by installing a regional keyboard and then using the On-Screen Keyboard feature.</span></span>

<span data-ttu-id="79039-188">Os usuários também podem instalar um IME (editor de método de entrada) para inserir scripts complexos, como caracteres japoneses, com um teclado padrão.</span><span class="sxs-lookup"><span data-stu-id="79039-188">Users can also install an Input Method Editor (IME) to enter complex scripts, such as Japanese characters, with a standard keyboard.</span></span> <span data-ttu-id="79039-189">Por exemplo, usando um IME em Japonês para inserir o caractere katakana カ (ka), você pode receber as seguintes mensagens:</span><span class="sxs-lookup"><span data-stu-id="79039-189">For example, using a Japanese IME to enter the katakana character カ (ka), you might get the following messages:</span></span>

<span data-ttu-id="79039-190">**WM \_ KEYDOWN**: VK \_ PROCESSKEY (a chave de processo do IME)</span><span class="sxs-lookup"><span data-stu-id="79039-190">**WM\_KEYDOWN**: VK\_PROCESSKEY (the IME PROCESS key)</span></span>  
<span data-ttu-id="79039-191">**WM \_ KEYUP**: 0x4b</span><span class="sxs-lookup"><span data-stu-id="79039-191">**WM\_KEYUP**: 0x4B</span></span>  
<span data-ttu-id="79039-192">**WM \_ KEYDOWN**: VK \_ PROCESSKEY</span><span class="sxs-lookup"><span data-stu-id="79039-192">**WM\_KEYDOWN**: VK\_PROCESSKEY</span></span>  
<span data-ttu-id="79039-193">**WM \_ KEYUP**: 0x41</span><span class="sxs-lookup"><span data-stu-id="79039-193">**WM\_KEYUP**: 0x41</span></span>  
<span data-ttu-id="79039-194">**WM \_ KEYDOWN**: VK \_ PROCESSKEY</span><span class="sxs-lookup"><span data-stu-id="79039-194">**WM\_KEYDOWN**: VK\_PROCESSKEY</span></span>  
<span data-ttu-id="79039-195">**WM \_ CHAR**: カ</span><span class="sxs-lookup"><span data-stu-id="79039-195">**WM\_CHAR**: カ</span></span>  
<span data-ttu-id="79039-196">**WM \_ KEYUP**: VK \_ Return</span><span class="sxs-lookup"><span data-stu-id="79039-196">**WM\_KEYUP**: VK\_RETURN</span></span>  


<span data-ttu-id="79039-197">Algumas combinações de teclas CTRL são convertidas em caracteres de controle ASCII.</span><span class="sxs-lookup"><span data-stu-id="79039-197">Some CTRL key combinations are translated into ASCII control characters.</span></span> <span data-ttu-id="79039-198">Por exemplo, CTRL + A é convertido para o caractere ASCII CTRL-A (SOH) (valor ASCII 0x01).</span><span class="sxs-lookup"><span data-stu-id="79039-198">For example, CTRL+A is translated to the ASCII ctrl-A (SOH) character (ASCII value 0x01).</span></span> <span data-ttu-id="79039-199">Para entrada de texto, você geralmente deve filtrar os caracteres de controle.</span><span class="sxs-lookup"><span data-stu-id="79039-199">For text input, you should generally filter out the control characters.</span></span> <span data-ttu-id="79039-200">Além disso, evite usar o [**WM \_ Char**](/windows/desktop/inputdev/wm-char) para implementar atalhos de teclado.</span><span class="sxs-lookup"><span data-stu-id="79039-200">Also, avoid using [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) to implement keyboard shortcuts.</span></span> <span data-ttu-id="79039-201">Em vez disso, use as mensagens do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) ; ou ainda melhor, use uma tabela de acelerador.</span><span class="sxs-lookup"><span data-stu-id="79039-201">Instead, use [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) messages; or even better, use an accelerator table.</span></span> <span data-ttu-id="79039-202">As tabelas do acelerador são descritas no próximo tópico, [tabelas de aceleração](accelerator-tables.md).</span><span class="sxs-lookup"><span data-stu-id="79039-202">Accelerator tables are described in the next topic, [Accelerator Tables](accelerator-tables.md).</span></span>

<span data-ttu-id="79039-203">O código a seguir exibe as principais mensagens do teclado no depurador.</span><span class="sxs-lookup"><span data-stu-id="79039-203">The following code displays the main keyboard messages in the debugger.</span></span> <span data-ttu-id="79039-204">Tente reproduzir com combinações de teclas diferentes e ver quais mensagens são geradas.</span><span class="sxs-lookup"><span data-stu-id="79039-204">Try playing with different keystroke combinations and see what messages are generated.</span></span>


```C++
LRESULT CALLBACK WindowProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    wchar_t msg[32];
    switch (uMsg)
    {
    case WM_SYSKEYDOWN:
        swprintf_s(msg, L"WM_SYSKEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSCHAR:
        swprintf_s(msg, L"WM_SYSCHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    case WM_SYSKEYUP:
        swprintf_s(msg, L"WM_SYSKEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYDOWN:
        swprintf_s(msg, L"WM_KEYDOWN: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_KEYUP:
        swprintf_s(msg, L"WM_KEYUP: 0x%x\n", wParam);
        OutputDebugString(msg);
        break;

    case WM_CHAR:
        swprintf_s(msg, L"WM_CHAR: %c\n", (wchar_t)wParam);
        OutputDebugString(msg);
        break;

    /* Handle other messages (not shown) */

    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```



## <a name="miscellaneous-keyboard-messages"></a><span data-ttu-id="79039-205">Diversas mensagens do teclado</span><span class="sxs-lookup"><span data-stu-id="79039-205">Miscellaneous Keyboard Messages</span></span>

<span data-ttu-id="79039-206">Algumas outras mensagens de teclado podem ser ignoradas com segurança pela maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="79039-206">Some other keyboard messages can safely be ignored by most applications.</span></span>

-   <span data-ttu-id="79039-207">A mensagem do [**WM \_ DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) é enviada para uma chave de combinação, como um diacrítico.</span><span class="sxs-lookup"><span data-stu-id="79039-207">The [**WM\_DEADCHAR**](/windows/desktop/inputdev/wm-deadchar) message is sent for a combining key, such as a diacritic.</span></span> <span data-ttu-id="79039-208">Por exemplo, em um teclado de idioma espanhol, digitar acentos (') seguido de E produz o caractere.</span><span class="sxs-lookup"><span data-stu-id="79039-208">For example, on a Spanish language keyboard, typing accent (') followed by E produces the character é.</span></span> <span data-ttu-id="79039-209">O **\_ DEADCHAR do WM** é enviado para o caractere de acento.</span><span class="sxs-lookup"><span data-stu-id="79039-209">The **WM\_DEADCHAR** is sent for the accent character.</span></span>
-   <span data-ttu-id="79039-210">A mensagem do [**WM \_ UNICHAR**](/windows/desktop/inputdev/wm-unichar) é obsoleta.</span><span class="sxs-lookup"><span data-stu-id="79039-210">The [**WM\_UNICHAR**](/windows/desktop/inputdev/wm-unichar) message is obsolete.</span></span> <span data-ttu-id="79039-211">Ele permite que programas ANSI recebam entrada de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="79039-211">It enables ANSI programs to receive Unicode character input.</span></span>
-   <span data-ttu-id="79039-212">O caractere de caracteres [**\_ \_ IME do WM**](/windows/desktop/Intl/wm-ime-char) é enviado quando um IME converte uma sequência de pressionamento de teclas em caracteres.</span><span class="sxs-lookup"><span data-stu-id="79039-212">The [**WM\_IME\_CHAR**](/windows/desktop/Intl/wm-ime-char) character is sent when an IME translates a keystroke sequence into characters.</span></span> <span data-ttu-id="79039-213">Ele é enviado além da mensagem comum do [**WM \_ Char**](/windows/desktop/inputdev/wm-char) .</span><span class="sxs-lookup"><span data-stu-id="79039-213">It is sent in addition to the usual [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span>

## <a name="keyboard-state"></a><span data-ttu-id="79039-214">Estado do teclado</span><span class="sxs-lookup"><span data-stu-id="79039-214">Keyboard State</span></span>

<span data-ttu-id="79039-215">As mensagens do teclado são controladas por evento.</span><span class="sxs-lookup"><span data-stu-id="79039-215">The keyboard messages are event-driven.</span></span> <span data-ttu-id="79039-216">Ou seja, você recebe uma mensagem quando algo interessante acontece, como um pressionamento de tecla, e a mensagem informa o que acabou de acontecer.</span><span class="sxs-lookup"><span data-stu-id="79039-216">That is, you get a message when something interesting happens, such as a key press, and the message tells you what just happened.</span></span> <span data-ttu-id="79039-217">Mas você também pode testar o estado de uma chave a qualquer momento, chamando a função [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) .</span><span class="sxs-lookup"><span data-stu-id="79039-217">But you can also test the state of a key at any time, by calling the [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function.</span></span>

<span data-ttu-id="79039-218">Por exemplo, considere como você detectaria a combinação de clicar com o botão esquerdo do mouse + ALT tecla.</span><span class="sxs-lookup"><span data-stu-id="79039-218">For example, consider how would you detect the combination of left mouse click + ALT key.</span></span> <span data-ttu-id="79039-219">Você pode acompanhar o estado da tecla ALT ouvindo mensagens de traço de chave e armazenando um sinalizador, mas [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) poupa o problema.</span><span class="sxs-lookup"><span data-stu-id="79039-219">You could track the state of the ALT key by listening for key-stroke messages and storing a flag, but [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) saves you the trouble.</span></span> <span data-ttu-id="79039-220">Quando você receber a [**mensagem \_ LBUTTONDOWN do WM**](/windows/desktop/inputdev/wm-lbuttondown) , basta chamar **GetKeyState** da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="79039-220">When you receive the [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) message, just call **GetKeyState** as follows:</span></span>


```C++
if (GetKeyState(VK_MENU) & 0x8000))
{
    // ALT key is down.
}
```



<span data-ttu-id="79039-221">A mensagem [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) usa um código de chave virtual como entrada e retorna um conjunto de sinalizadores de bit (na verdade, apenas dois sinalizadores).</span><span class="sxs-lookup"><span data-stu-id="79039-221">The [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) message takes a virtual-key code as input and returns a set of bit flags (actually just two flags).</span></span> <span data-ttu-id="79039-222">O valor 0x8000 contém o sinalizador de bit que testa se a chave está pressionada no momento.</span><span class="sxs-lookup"><span data-stu-id="79039-222">The value 0x8000 contains the bit flag that tests whether the key is currently pressed.</span></span>

<span data-ttu-id="79039-223">A maioria dos teclados tem duas teclas ALT, esquerda e direita.</span><span class="sxs-lookup"><span data-stu-id="79039-223">Most keyboards have two ALT keys, left and right.</span></span> <span data-ttu-id="79039-224">O exemplo anterior testa se um deles foi pressionado.</span><span class="sxs-lookup"><span data-stu-id="79039-224">The previous example tests whether either of them of pressed.</span></span> <span data-ttu-id="79039-225">Você também pode usar [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) para distinguir entre as instâncias esquerda e direita das teclas ALT, Shift ou CTRL.</span><span class="sxs-lookup"><span data-stu-id="79039-225">You can also use [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) to distinguish between the left and right instances of the ALT, SHIFT, or CTRL keys.</span></span> <span data-ttu-id="79039-226">Por exemplo, o código a seguir testará se a tecla ALT direita for pressionada.</span><span class="sxs-lookup"><span data-stu-id="79039-226">For example, the following code tests if the right ALT key is pressed.</span></span>


```C++
if (GetKeyState(VK_RMENU) & 0x8000))
{
    // Right ALT key is down.
}
```



<span data-ttu-id="79039-227">A função [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) é interessante porque relata um estado de teclado *virtual* .</span><span class="sxs-lookup"><span data-stu-id="79039-227">The [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) function is interesting because it reports a *virtual* keyboard state.</span></span> <span data-ttu-id="79039-228">Esse estado virtual se baseia no conteúdo da fila de mensagens e é atualizado à medida que você remove mensagens da fila.</span><span class="sxs-lookup"><span data-stu-id="79039-228">This virtual state is based on the contents of your message queue, and gets updated as you remove messages from the queue.</span></span> <span data-ttu-id="79039-229">À medida que o programa processa mensagens de janela, o **GetKeyState** fornece um instantâneo do teclado no momento em que cada mensagem foi enfileirada.</span><span class="sxs-lookup"><span data-stu-id="79039-229">As your program processes window messages, **GetKeyState** gives you a snapshot of the keyboard at the time that each message was queued.</span></span> <span data-ttu-id="79039-230">Por exemplo, se a última mensagem na fila foi o [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), o **GetKeyState** relatará o estado do teclado no momento em que o usuário clicou no botão do mouse.</span><span class="sxs-lookup"><span data-stu-id="79039-230">For example, if the last message on the queue was [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), **GetKeyState** reports the keyboard state at the moment when the user clicked the mouse button.</span></span>

<span data-ttu-id="79039-231">Como o [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) é baseado em sua fila de mensagens, ele também ignora a entrada do teclado que foi enviada para outro programa.</span><span class="sxs-lookup"><span data-stu-id="79039-231">Because [**GetKeyState**](/windows/desktop/api/winuser/nf-winuser-getkeystate) is based on your message queue, it also ignores keyboard input that was sent to another program.</span></span> <span data-ttu-id="79039-232">Se o usuário alternar para outro programa, quaisquer pressionamentos de tecla enviados para esse programa serão ignorados por **GetKeyState**.</span><span class="sxs-lookup"><span data-stu-id="79039-232">If the user switches to another program, any key presses that are sent to that program are ignored by **GetKeyState**.</span></span> <span data-ttu-id="79039-233">Se você realmente deseja saber o estado físico imediato do teclado, há uma função para isso: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span><span class="sxs-lookup"><span data-stu-id="79039-233">If you really want to know the immediate physical state of the keyboard, there is a function for that: [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).</span></span> <span data-ttu-id="79039-234">No entanto, para a maioria dos códigos de interface do usuário, a função correta é **GetKeyState**.</span><span class="sxs-lookup"><span data-stu-id="79039-234">For most UI code, however, the correct function is **GetKeyState**.</span></span>

## <a name="next"></a><span data-ttu-id="79039-235">Avançar</span><span class="sxs-lookup"><span data-stu-id="79039-235">Next</span></span>

[<span data-ttu-id="79039-236">Tabelas do acelerador</span><span class="sxs-lookup"><span data-stu-id="79039-236">Accelerator Tables</span></span>](accelerator-tables.md)

 

 
