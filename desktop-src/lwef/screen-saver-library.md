---
title: Lidando com proteções de tela
description: A API do Microsoft Win32 dá suporte a aplicativos especiais chamados de proteções de tela.
ms.assetid: cda5e690-71fe-4df7-b8a2-3a2ad65b1bfb
keywords:
- proteções de tela
- Painel de controle, proteções de tela
- ScreenSaverConfigureDialog
- arquivos de definição de módulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b7e0d0c177af2798b041fa12b4cc5793bf9be0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454040"
---
# <a name="handling-screen-savers"></a><span data-ttu-id="c0132-107">Lidando com proteções de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-107">Handling Screen Savers</span></span>

<span data-ttu-id="c0132-108">A API do Microsoft Win32 dá suporte a aplicativos especiais chamados de *proteções de tela*.</span><span class="sxs-lookup"><span data-stu-id="c0132-108">The Microsoft Win32 API supports special applications called *screen savers*.</span></span> <span data-ttu-id="c0132-109">As proteções de tela iniciam quando o mouse e o teclado ficam ociosos por um período de tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="c0132-109">Screen savers start when the mouse and keyboard have been idle for a specified period of time.</span></span> <span data-ttu-id="c0132-110">Eles são usados por esses dois motivos:</span><span class="sxs-lookup"><span data-stu-id="c0132-110">They are used for these two reasons:</span></span>

-   <span data-ttu-id="c0132-111">Para proteger uma tela da gravação Phosphor causada por imagens estáticas.</span><span class="sxs-lookup"><span data-stu-id="c0132-111">To protect a screen from phosphor burn caused by static images.</span></span>
-   <span data-ttu-id="c0132-112">Ocultar informações confidenciais deixadas em uma tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-112">To conceal sensitive information left on a screen.</span></span>

<span data-ttu-id="c0132-113">Este tópico é dividido nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0132-113">This topic is divided into the following sections.</span></span>

-   [<span data-ttu-id="c0132-114">Sobre as proteções de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-114">About Screen Savers</span></span>](#about-screen-savers)
-   [<span data-ttu-id="c0132-115">Usando as funções de proteção de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-115">Using the Screen Saver Functions</span></span>](#using-the-screen-saver-functions)
    -   [<span data-ttu-id="c0132-116">Criando uma proteção de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-116">Creating a Screen Saver</span></span>](#creating-a-screen-saver)
    -   [<span data-ttu-id="c0132-117">Instalando novas proteções de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-117">Installing New Screen Savers</span></span>](#installing-new-screen-savers)
    -   [<span data-ttu-id="c0132-118">Adicionando ajuda à caixa de diálogo configuração de proteção de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-118">Adding Help to the Screen Saver Configuration Dialog Box</span></span>](#adding-help-to-the-screen-saver-configuration-dialog-box)

## <a name="about-screen-savers"></a><span data-ttu-id="c0132-119">Sobre as proteções de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-119">About Screen Savers</span></span>

<span data-ttu-id="c0132-120">O aplicativo de área de trabalho no painel de controle do Windows permite que os usuários selecionem em uma lista de proteções de tela, especifiquem quanto tempo deve decorrer antes que a proteção de tela seja iniciada, configure as proteções de tela e visualize as proteções de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-120">The Desktop application in the Windows Control Panel lets users select from a list of screen savers, specify how much time should elapse before the screen saver starts, configure screen savers, and preview screen savers.</span></span> <span data-ttu-id="c0132-121">As proteções de tela são carregadas automaticamente quando o Windows é iniciado ou quando um usuário ativa a proteção de tela por meio do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="c0132-121">Screen savers are loaded automatically when Windows starts or when a user activates the screen saver through the Control Panel.</span></span>

<span data-ttu-id="c0132-122">Quando uma proteção de tela é escolhida, o Windows monitora os pressionamentos de tecla e os movimentos do mouse e, em seguida, inicia a proteção de tela após um período de inatividade.</span><span class="sxs-lookup"><span data-stu-id="c0132-122">Once a screen saver is chosen, Windows monitors keystrokes and mouse movements and then starts the screen saver after a period of inactivity.</span></span> <span data-ttu-id="c0132-123">No entanto, o Windows não iniciará a proteção de tela se qualquer uma das seguintes condições existir:</span><span class="sxs-lookup"><span data-stu-id="c0132-123">However, Windows does not start the screen saver if any of the following conditions exist:</span></span>

-   <span data-ttu-id="c0132-124">O aplicativo ativo não é um aplicativo baseado no Windows.</span><span class="sxs-lookup"><span data-stu-id="c0132-124">The active application is not a Windows-based application.</span></span>
-   <span data-ttu-id="c0132-125">Uma janela de treinamento baseado em computador (CBT) está presente.</span><span class="sxs-lookup"><span data-stu-id="c0132-125">A computer-based training (CBT) window is present.</span></span>
-   <span data-ttu-id="c0132-126">O aplicativo ativo recebe a [mensagem \_ SYSCOMMAND do WM](../menurc/wm-syscommand.md) com o parâmetro *wParam* definido como o \_ valor SC SCREENSAVE, mas não passa a mensagem para a função [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="c0132-126">The active application receives the [WM\_SYSCOMMAND](../menurc/wm-syscommand.md) message with the *wParam* parameter set to the SC\_SCREENSAVE value, but it does not pass the message to the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="c0132-127">**Contexto de segurança da proteção de tela**</span><span class="sxs-lookup"><span data-stu-id="c0132-127">**Security Context of the Screen Saver**</span></span>

<span data-ttu-id="c0132-128">O contexto de segurança da proteção de tela depende de se um usuário está conectado interativamente.</span><span class="sxs-lookup"><span data-stu-id="c0132-128">The security context of the screen saver is dependent on whether a user is interactively logged on.</span></span> <span data-ttu-id="c0132-129">Se um usuário estiver conectado interativamente quando a proteção de tela for chamada, a proteção de tela será executada no contexto de segurança do usuário interativo.</span><span class="sxs-lookup"><span data-stu-id="c0132-129">If a user is interactively logged on when the screen saver is invoked, the screen saver runs in the security context of the interactive user.</span></span> <span data-ttu-id="c0132-130">Se nenhum usuário estiver conectado, o contexto de segurança da proteção de tela dependerá da versão do Windows que está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="c0132-130">If no user is logged on, the security context of the screen saver is dependent on the version of Windows being used.</span></span>

-   <span data-ttu-id="c0132-131">Windows XP e Windows 2000-a proteção de tela é executada no contexto de LocalSystem com contas restritas.</span><span class="sxs-lookup"><span data-stu-id="c0132-131">Windows XP and Windows 2000 - screen saver runs in the context of LocalSystem with accounts restricted.</span></span>
-   <span data-ttu-id="c0132-132">Windows 2003-a proteção de tela é executada no contexto de LocalService com todos os privilégios removidos e grupo de administradores desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c0132-132">Windows 2003 - screen saver runs in the context of LocalService with all privileges removed and administrators group disabled.</span></span>
-   <span data-ttu-id="c0132-133">Não se aplica ao Windows NT4.</span><span class="sxs-lookup"><span data-stu-id="c0132-133">Does not apply to Windows NT4.</span></span>

<span data-ttu-id="c0132-134">O contexto de segurança determina o nível de operações privilegiadas que podem ser feitas em uma proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-134">The security context determines the level of privileged operations which can be done from a screen saver.</span></span>

<span data-ttu-id="c0132-135">**Windows Vista e posterior:** Se a proteção por senha estiver habilitada pela política, a proteção de tela será iniciada, independentemente do que um aplicativo faz com a \_ notificação SC SCREENSAVE.</span><span class="sxs-lookup"><span data-stu-id="c0132-135">**Windows Vista and later:** If password protection is enabled by policy, the screen saver is started regardless of what an application does with the SC\_SCREENSAVE notification.</span></span>

<span data-ttu-id="c0132-136">As proteções de tela contêm funções exportadas específicas, definições de recursos e declarações de variáveis.</span><span class="sxs-lookup"><span data-stu-id="c0132-136">Screen savers contain specific exported functions, resource definitions, and variable declarations.</span></span> <span data-ttu-id="c0132-137">A biblioteca de proteção de tela contém a função **principal** e outro código de inicialização necessário para uma proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-137">The screen saver library contains the **main** function and other startup code required for a screen saver.</span></span> <span data-ttu-id="c0132-138">Quando uma proteção de tela é iniciada, o código de inicialização na biblioteca de proteção de tela cria uma janela de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="c0132-138">When a screen saver starts, the startup code in the screen saver library creates a full-screen window.</span></span> <span data-ttu-id="c0132-139">A classe de janela dessa janela é declarada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c0132-139">The window class for this window is declared as follows:</span></span>


```
WNDCLASS cls; 
cls.hCursor        = NULL; 
cls.hIcon          = LoadIcon(hInst, MAKEINTATOM(ID_APP)); 
cls.lpszMenuName   = NULL; 
cls.lpszClassName  = "WindowsScreenSaverClass"; 
cls.hbrBackground  = GetStockObject(BLACK_BRUSH); 
cls.hInstance      = hInst; 
cls.style          = CS_VREDRAW  | CS_HREDRAW | CS_SAVEBITS | CS_DBLCLKS; 
cls.lpfnWndProc    = (WNDPROC) ScreenSaverProc; 
cls.cbWndExtra     = 0; 
cls.cbClsExtra     = 0;
```



<span data-ttu-id="c0132-140">Para criar uma proteção de tela, a maioria dos desenvolvedores cria um módulo de código-fonte que contém três funções necessárias e as vincula à biblioteca de proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-140">To create a screen saver, most developers create a source code module containing three required functions and link them with the screen saver library.</span></span> <span data-ttu-id="c0132-141">Um módulo de proteção de tela é responsável apenas pela configuração e pelo fornecimento de efeitos visuais.</span><span class="sxs-lookup"><span data-stu-id="c0132-141">A screen saver module is responsible only for configuring itself and for providing visual effects.</span></span>

<span data-ttu-id="c0132-142">Uma das três funções necessárias em um módulo de proteção de tela é [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span><span class="sxs-lookup"><span data-stu-id="c0132-142">One of the three required functions in a screen saver module is [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span></span> <span data-ttu-id="c0132-143">Essa função processa mensagens específicas e passa todas as mensagens não processadas de volta para a biblioteca de proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-143">This function processes specific messages and passes any unprocessed messages back to the screen saver library.</span></span> <span data-ttu-id="c0132-144">A seguir estão algumas das mensagens típicas processadas pelo **ScreenSaverProc**.</span><span class="sxs-lookup"><span data-stu-id="c0132-144">Following are some of the typical messages processed by **ScreenSaverProc**.</span></span>



| <span data-ttu-id="c0132-145">Mensagem</span><span class="sxs-lookup"><span data-stu-id="c0132-145">Message</span></span>        | <span data-ttu-id="c0132-146">Significado</span><span class="sxs-lookup"><span data-stu-id="c0132-146">Meaning</span></span>                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0132-147">criação do WM \_</span><span class="sxs-lookup"><span data-stu-id="c0132-147">WM\_CREATE</span></span>     | <span data-ttu-id="c0132-148">Recupere todos os dados de inicialização do arquivo de Regedit.ini.</span><span class="sxs-lookup"><span data-stu-id="c0132-148">Retrieve any initialization data from the Regedit.ini file.</span></span> <span data-ttu-id="c0132-149">Defina um timer de janela para a janela de proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-149">Set a window timer for the screen saver window.</span></span> <span data-ttu-id="c0132-150">Execute qualquer outra inicialização necessária.</span><span class="sxs-lookup"><span data-stu-id="c0132-150">Perform any other required initialization.</span></span>                                     |
| <span data-ttu-id="c0132-151">ERASEBKGND do WM \_</span><span class="sxs-lookup"><span data-stu-id="c0132-151">WM\_ERASEBKGND</span></span> | <span data-ttu-id="c0132-152">Apague a janela proteção de tela e prepare-se para operações de desenho subsequentes.</span><span class="sxs-lookup"><span data-stu-id="c0132-152">Erase the screen saver window and prepare for subsequent drawing operations.</span></span>                                                                                                               |
| <span data-ttu-id="c0132-153">\_temporizador do WM</span><span class="sxs-lookup"><span data-stu-id="c0132-153">WM\_TIMER</span></span>      | <span data-ttu-id="c0132-154">Executar operações de desenho.</span><span class="sxs-lookup"><span data-stu-id="c0132-154">Perform drawing operations.</span></span>                                                                                                                                                                |
| <span data-ttu-id="c0132-155">destruição do WM \_</span><span class="sxs-lookup"><span data-stu-id="c0132-155">WM\_DESTROY</span></span>    | <span data-ttu-id="c0132-156">Destrua os temporizadores criados quando o aplicativo processou a mensagem de [ \_ criação do WM](../winmsg/wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="c0132-156">Destroy the timers created when the application processed the [WM\_CREATE](../winmsg/wm-create.md) message.</span></span> <span data-ttu-id="c0132-157">Execute qualquer limpeza adicional necessária.</span><span class="sxs-lookup"><span data-stu-id="c0132-157">Perform any additional required cleanup.</span></span> |



 

<span data-ttu-id="c0132-158">O [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) passa mensagens não processadas para a biblioteca de proteção de tela chamando a função [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) .</span><span class="sxs-lookup"><span data-stu-id="c0132-158">[**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) passes unprocessed messages to the screen saver library by calling the [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) function.</span></span> <span data-ttu-id="c0132-159">A tabela a seguir descreve como essa função processa várias mensagens.</span><span class="sxs-lookup"><span data-stu-id="c0132-159">The following table describes how this function processes various messages.</span></span>



| <span data-ttu-id="c0132-160">Mensagem</span><span class="sxs-lookup"><span data-stu-id="c0132-160">Message</span></span>         | <span data-ttu-id="c0132-161">Ação</span><span class="sxs-lookup"><span data-stu-id="c0132-161">Action</span></span>                                                                    |
|-----------------|---------------------------------------------------------------------------|
| <span data-ttu-id="c0132-162">WM \_ SETcursor</span><span class="sxs-lookup"><span data-stu-id="c0132-162">WM\_SETCURSOR</span></span>   | <span data-ttu-id="c0132-163">Defina o cursor para o cursor NULL, removendo-o da tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-163">Set the cursor to the null cursor, removing it from the screen.</span></span>           |
| <span data-ttu-id="c0132-164">pintura do WM \_</span><span class="sxs-lookup"><span data-stu-id="c0132-164">WM\_PAINT</span></span>       | <span data-ttu-id="c0132-165">Pinte o plano de fundo da tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-165">Paint the screen background.</span></span>                                              |
| <span data-ttu-id="c0132-166">LBUTTONDOWN do WM \_</span><span class="sxs-lookup"><span data-stu-id="c0132-166">WM\_LBUTTONDOWN</span></span> | <span data-ttu-id="c0132-167">Encerre a proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-167">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="c0132-168">MBUTTONDOWN do WM \_</span><span class="sxs-lookup"><span data-stu-id="c0132-168">WM\_MBUTTONDOWN</span></span> | <span data-ttu-id="c0132-169">Encerre a proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-169">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="c0132-170">RBUTTONDOWN do WM \_</span><span class="sxs-lookup"><span data-stu-id="c0132-170">WM\_RBUTTONDOWN</span></span> | <span data-ttu-id="c0132-171">Encerre a proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-171">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="c0132-172">o WM \_ KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="c0132-172">WM\_KEYDOWN</span></span>     | <span data-ttu-id="c0132-173">Encerre a proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-173">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="c0132-174">admousemove do WM \_</span><span class="sxs-lookup"><span data-stu-id="c0132-174">WM\_MOUSEMOVE</span></span>   | <span data-ttu-id="c0132-175">Encerre a proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-175">Terminate the screen saver.</span></span>                                               |
| <span data-ttu-id="c0132-176">ativar o WM \_</span><span class="sxs-lookup"><span data-stu-id="c0132-176">WM\_ACTIVATE</span></span>    | <span data-ttu-id="c0132-177">Encerre a proteção de tela se o parâmetro *wParam* estiver definido como **false**.</span><span class="sxs-lookup"><span data-stu-id="c0132-177">Terminate the screen saver if the *wParam* parameter is set to **FALSE**.</span></span> |



 

<span data-ttu-id="c0132-178">A segunda função necessária em um módulo de proteção de tela é [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog).</span><span class="sxs-lookup"><span data-stu-id="c0132-178">The second required function in a screen saver module is [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog).</span></span> <span data-ttu-id="c0132-179">Essa função exibe uma caixa de diálogo que permite ao usuário configurar a proteção de tela (um aplicativo deve fornecer um modelo de caixa de diálogo correspondente).</span><span class="sxs-lookup"><span data-stu-id="c0132-179">This function displays a dialog box that enables the user to configure the screen saver (an application must provide a corresponding dialog box template).</span></span> <span data-ttu-id="c0132-180">O Windows exibe a caixa de diálogo configuração quando o usuário seleciona o botão **instalação** na caixa de diálogo proteção de tela do painel de controle.</span><span class="sxs-lookup"><span data-stu-id="c0132-180">Windows displays the configuration dialog box when the user selects the **Setup** button in the Control Panel's Screen Saver dialog box.</span></span>

<span data-ttu-id="c0132-181">A terceira função necessária em um módulo de proteção de tela é [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses).</span><span class="sxs-lookup"><span data-stu-id="c0132-181">The third required function in a screen saver module is [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses).</span></span> <span data-ttu-id="c0132-182">Essa função deve ser chamada por todos os aplicativos de proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-182">This function must be called by all screen saver applications.</span></span> <span data-ttu-id="c0132-183">No entanto, os aplicativos que não exigem janelas especiais ou controles personalizados na caixa de diálogo de configuração podem simplesmente retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="c0132-183">However, applications that do not require special windows or custom controls in the configuration dialog box can simply return **TRUE**.</span></span> <span data-ttu-id="c0132-184">Aplicativos que exigem controles especiais do Windows ou personalizados devem usar essa função para registrar as classes de janela correspondentes.</span><span class="sxs-lookup"><span data-stu-id="c0132-184">Applications requiring special windows or custom controls should use this function to register the corresponding window classes.</span></span>

<span data-ttu-id="c0132-185">Além de criar um módulo que dê suporte às três funções que acabamos de descrever, uma proteção de tela deve fornecer um ícone.</span><span class="sxs-lookup"><span data-stu-id="c0132-185">In addition to creating a module that supports the three functions just described, a screen saver should supply an icon.</span></span> <span data-ttu-id="c0132-186">Esse ícone só é visível quando a proteção de tela é executada como um aplicativo autônomo.</span><span class="sxs-lookup"><span data-stu-id="c0132-186">This icon is visible only when the screen saver is run as a standalone application.</span></span> <span data-ttu-id="c0132-187">(Para ser executado pelo painel de controle, uma proteção de tela deve ter a extensão de nome de arquivo. SCR; para ser executada como um aplicativo autônomo, ela deve ter a extensão de nome de arquivo. exe.) O ícone deve ser identificado no arquivo de recurso da proteção de tela pelo aplicativo de ID de constante \_ , que é definido no arquivo de cabeçalho SCRNSAVE. h.</span><span class="sxs-lookup"><span data-stu-id="c0132-187">(To be run by the Control Panel, a screen saver must have the .scr file name extension; to be run as a standalone application, it must have the .exe file name extension.) The icon must be identified in the screen saver's resource file by the constant ID\_APP, which is defined in the Scrnsave.h header file.</span></span>

<span data-ttu-id="c0132-188">Um requisito final é uma cadeia de caracteres de descrição de proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-188">One final requirement is a screen saver description string.</span></span> <span data-ttu-id="c0132-189">O arquivo de recurso para uma proteção de tela deve conter uma cadeia de caracteres que o painel de controle exibe como o nome da proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-189">The resource file for a screen saver must contain a string that the Control Panel displays as the screen saver name.</span></span> <span data-ttu-id="c0132-190">A cadeia de caracteres de descrição deve ser a primeira cadeia de caracteres na tabela de cadeias de caracteres do arquivo de recurso (identificada com o valor ordinal 1).</span><span class="sxs-lookup"><span data-stu-id="c0132-190">The description string must be the first string in the resource file's string table (identified with the ordinal value 1).</span></span> <span data-ttu-id="c0132-191">No entanto, a cadeia de caracteres de descrição será ignorada pelo painel de controle se a proteção de tela tiver um nome de arquivo longo.</span><span class="sxs-lookup"><span data-stu-id="c0132-191">However, the description string is ignored by the Control Panel if the screen saver has a long filename.</span></span> <span data-ttu-id="c0132-192">Nesse caso, o nome do arquivo será usado como a cadeia de caracteres de descrição.</span><span class="sxs-lookup"><span data-stu-id="c0132-192">In such case, the filename will be used as the description string.</span></span>

## <a name="using-the-screen-saver-functions"></a><span data-ttu-id="c0132-193">Usando as funções de proteção de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-193">Using the Screen Saver Functions</span></span>

<span data-ttu-id="c0132-194">Esta seção usa o código de exemplo obtido de um aplicativo de proteção de tela para ilustrar as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="c0132-194">This section uses example code taken from a screen saver application to illustrate the following tasks:</span></span>

-   [<span data-ttu-id="c0132-195">Criando uma proteção de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-195">Creating a Screen Saver</span></span>](#creating-a-screen-saver)
-   [<span data-ttu-id="c0132-196">Instalando novas proteções de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-196">Installing New Screen Savers</span></span>](#installing-new-screen-savers)
-   [<span data-ttu-id="c0132-197">Adicionando ajuda à caixa de diálogo configuração de proteção de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-197">Adding Help to the Screen Saver Configuration Dialog Box</span></span>](#adding-help-to-the-screen-saver-configuration-dialog-box)

### <a name="creating-a-screen-saver"></a><span data-ttu-id="c0132-198">Criando uma proteção de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-198">Creating a Screen Saver</span></span>

<span data-ttu-id="c0132-199">Em intervalos variando de 1 a 10 segundos, o aplicativo neste exemplo redesenha a tela com uma das quatro cores: branco, cinza claro, cinza escuro e preto.</span><span class="sxs-lookup"><span data-stu-id="c0132-199">At intervals ranging from 1 through 10 seconds, the application in this example repaints the screen with one of four colors: white, light gray, dark gray, and black.</span></span> <span data-ttu-id="c0132-200">O aplicativo pinta a tela toda vez que recebe uma mensagem de [ \_ temporizador do WM](../winmsg/wm-timer.md) .</span><span class="sxs-lookup"><span data-stu-id="c0132-200">The application paints the screen each time it receives a [WM\_TIMER](../winmsg/wm-timer.md) message.</span></span> <span data-ttu-id="c0132-201">O usuário pode ajustar o intervalo no qual essa mensagem é enviada, selecionando a caixa de diálogo configuração do aplicativo e ajustando uma barra de rolagem horizontal única.</span><span class="sxs-lookup"><span data-stu-id="c0132-201">The user can adjust the interval at which this message is sent by selecting the application's configuration dialog box and adjusting a single horizontal scroll bar.</span></span>

### <a name="screen-saver-library"></a><span data-ttu-id="c0132-202">Biblioteca de proteção de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-202">Screen saver library</span></span>

<span data-ttu-id="c0132-203">As funções de proteção de tela estática estão contidas na biblioteca de proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-203">The static screen saver functions are contained in the screen saver library.</span></span> <span data-ttu-id="c0132-204">Há duas versões da biblioteca disponíveis, SCRNSAVE. lib e Scrnsavw. lib.</span><span class="sxs-lookup"><span data-stu-id="c0132-204">There are two versions of the library available, Scrnsave.lib and Scrnsavw.lib.</span></span> <span data-ttu-id="c0132-205">Você deve vincular seu projeto com um deles.</span><span class="sxs-lookup"><span data-stu-id="c0132-205">You must link your project with one of these.</span></span> <span data-ttu-id="c0132-206">SCRNSAVE. lib é usado para proteções de tela que usam caracteres ANSI e Scrnsavw. lib é usado para proteções de tela que usam caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="c0132-206">Scrnsave.lib is used for screen savers that use ANSI characters, and Scrnsavw.lib is used for screen savers that use Unicode characters.</span></span> <span data-ttu-id="c0132-207">Uma proteção de tela vinculada a Scrnsavw. lib será executada somente em plataformas Windows que dão suporte a Unicode, enquanto uma proteção de tela vinculada a SCRNSAVE. lib será executada em qualquer plataforma Windows.</span><span class="sxs-lookup"><span data-stu-id="c0132-207">A screen saver that is linked with Scrnsavw.lib will only run on Windows platforms that support Unicode, while a screen saver linked with Scrnsave.lib will run on any Windows platform.</span></span>

### <a name="supporting-the-configuration-dialog-box"></a><span data-ttu-id="c0132-208">Suporte à caixa de diálogo de configuração</span><span class="sxs-lookup"><span data-stu-id="c0132-208">Supporting the configuration dialog box</span></span>

<span data-ttu-id="c0132-209">A maioria das proteções de tela fornece uma caixa de diálogo de configuração para permitir que o usuário especifique dados de personalização, como cores exclusivas, velocidades de desenho, espessura de linha, fontes e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c0132-209">Most screen savers provide a configuration dialog box to let the user specify customization data such as unique colors, drawing speeds, line thickness, fonts, and so on.</span></span> <span data-ttu-id="c0132-210">Para dar suporte à caixa de diálogo configuração, o aplicativo deve fornecer um modelo de caixa de diálogo e também deve dar suporte à função [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) .</span><span class="sxs-lookup"><span data-stu-id="c0132-210">To support the configuration dialog box, the application must provide a dialog box template and must also support the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function.</span></span> <span data-ttu-id="c0132-211">A seguir está o modelo de caixa de diálogo para o aplicativo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c0132-211">Following is the dialog box template for the sample application.</span></span>


```
DLG_SCRNSAVECONFIGURE DIALOG 6, 18, 160, 63
LANGUAGE LANG_NEUTRAL, SUBLANG_NEUTRAL
STYLE DS_MODALFRAME | WS_POPUP | WS_VISIBLE | WS_CAPTION | WS_SYSMENU
CAPTION "Sample Screen-Saver Setup"
FONT 8, "MS Shell Dlg"
BEGIN
    GROUPBOX      "Redraw Speed", 101, 0, 6, 98, 40
    SCROLLBAR     ID_SPEED, 5, 31, 89, 10
    LTEXT         "Fast", 103, 6, 21, 20, 8
    LTEXT         "Slow", 104, 75, 21, 20, 8
    PUSHBUTTON    "OK", ID_OK, 117, 10, 40, 14
    PUSHBUTTON    "Cancel", ID_CANCEL, 117, 32, 40, 14
END
```



<span data-ttu-id="c0132-212">Você deve definir a constante usada para identificar o modelo da caixa de diálogo usando o valor decimal 2003, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="c0132-212">You must define the constant used to identify the dialog box template by using the decimal value 2003, as in the following example:</span></span>


```
#define  DLG_SCRNSAVECONFIGURE 2003
```



<span data-ttu-id="c0132-213">O exemplo a seguir mostra a função [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) encontrada no aplicativo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c0132-213">The following example shows the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function found in the sample application.</span></span>


```
#define MINVEL  1                 // minimum redraw speed value     
#define MAXVEL  10                // maximum redraw speed value    
#define DEFVEL  5                 // default redraw speed value    
 
LONG    lSpeed = DEFVEL;          // redraw speed variable         
  
extern HINSTANCE hMainInstance;   // screen saver instance handle  
 
CHAR   szAppName[80];             // .ini section name             
CHAR   szTemp[20];                // temporary array of characters  
CHAR   szRedrawSpeed[ ] = "Redraw Speed";   // .ini speed entry 
CHAR   szIniFile[MAXFILELEN];     // .ini or registry file name  
 
BOOL WINAPI ScreenSaverConfigureDialog(hDlg, message, wParam, lParam) 
HWND     hDlg; 
UINT     message; 
DWORD    wParam; 
LONG     lParam; 
HRESULT  hr;
{ 
    static HWND hSpeed;   // handle to speed scroll bar 
    static HWND hOK;      // handle to OK push button  
 
    switch(message) 
    { 
        case WM_INITDIALOG: 
 
            // Retrieve the application name from the .rc file.  
            LoadString(hMainInstance, idsAppName, szAppName, 
                       80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, 
                       MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry. 
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // If the initialization file does not contain an entry 
            // for this screen saver, use the default value. 
            if(lSpeed > MAXVEL || lSpeed < MINVEL) 
                lSpeed = DEFVEL; 
 
            // Initialize the redraw speed scroll bar control.
            hSpeed = GetDlgItem(hDlg, ID_SPEED); 
            SetScrollRange(hSpeed, SB_CTL, MINVEL, MAXVEL, FALSE); 
            SetScrollPos(hSpeed, SB_CTL, lSpeed, TRUE); 
 
            // Retrieve a handle to the OK push button control.  
            hOK = GetDlgItem(hDlg, ID_OK); 
 
            return TRUE; 
 
        case WM_HSCROLL: 

            // Process scroll bar input, adjusting the lSpeed 
            // value as appropriate. 
            switch (LOWORD(wParam)) 
                { 
                    case SB_PAGEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_LINEUP: 
                        --lSpeed; 
                    break; 
 
                    case SB_PAGEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_LINEDOWN: 
                        ++lSpeed; 
                    break; 
 
                    case SB_THUMBPOSITION: 
                        lSpeed = HIWORD(wParam); 
                    break; 
 
                    case SB_BOTTOM: 
                        lSpeed = MINVEL; 
                    break; 
 
                    case SB_TOP: 
                        lSpeed = MAXVEL; 
                    break; 
 
                    case SB_THUMBTRACK: 
                    case SB_ENDSCROLL: 
                        return TRUE; 
                    break; 
                } 

                if ((int) lSpeed <= MINVEL) 
                    lSpeed = MINVEL; 
                if ((int) lSpeed >= MAXVEL) 
                    lSpeed = MAXVEL; 
 
                SetScrollPos((HWND) lParam, SB_CTL, lSpeed, TRUE); 
            break; 
 
        case WM_COMMAND: 
            switch(LOWORD(wParam)) 
            { 
                case ID_OK: 
 
                    // Write the current redraw speed variable to
                    // the .ini file. 
                    hr = StringCchPrintf(szTemp, 20, "%ld", lSpeed);
                    if (SUCCEEDED(hr))
                        WritePrivateProfileString(szAppName, szRedrawSpeed, 
                                                  szTemp, szIniFile); 
 
                case ID_CANCEL: 
                    EndDialog(hDlg, LOWORD(wParam) == ID_OK); 

                return TRUE; 
            } 
    } 
    return FALSE; 
}
```



<span data-ttu-id="c0132-214">Além de fornecer o modelo de caixa de diálogo e dar suporte à função [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) , um aplicativo também deve oferecer suporte à função [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) .</span><span class="sxs-lookup"><span data-stu-id="c0132-214">In addition to providing the dialog box template and supporting the [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) function, an application must also support the [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) function.</span></span> <span data-ttu-id="c0132-215">Essa função registra qualquer classe de janela não padrão exigida pela proteção de tela.</span><span class="sxs-lookup"><span data-stu-id="c0132-215">This function registers any nonstandard window classes required by the screen saver.</span></span> <span data-ttu-id="c0132-216">Como o aplicativo de exemplo usou apenas as classes de janela padrão em seu procedimento de caixa de diálogo, essa função simplesmente retorna **true**, como no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="c0132-216">Because the sample application used only standard window classes in its dialog box procedure, this function simply returns **TRUE**, as in the following example:</span></span>


```
BOOL WINAPI RegisterDialogClasses(hInst) 
HANDLE  hInst; 
{ 
    return TRUE; 
}
```



### <a name="supporting-the-screen-saver-window-procedure"></a><span data-ttu-id="c0132-217">Procedimento de suporte à janela de proteção de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-217">Supporting the screen saver window procedure</span></span>

<span data-ttu-id="c0132-218">Cada proteção de tela deve dar suporte a um procedimento de janela chamado [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span><span class="sxs-lookup"><span data-stu-id="c0132-218">Each screen saver must support a window procedure named [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc).</span></span> <span data-ttu-id="c0132-219">Assim como a maioria dos procedimentos de janela, o **ScreenSaverProc** processa um conjunto de mensagens específicas e passa todas as mensagens não processadas para um procedimento padrão.</span><span class="sxs-lookup"><span data-stu-id="c0132-219">Like most window procedures, **ScreenSaverProc** processes a set of specific messages and passes any unprocessed messages to a default procedure.</span></span> <span data-ttu-id="c0132-220">No entanto, em vez de passá-los para a função [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) , o **ScreenSaverProc** passa mensagens não processadas para a função [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) .</span><span class="sxs-lookup"><span data-stu-id="c0132-220">However, instead of passing them to the [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) function, **ScreenSaverProc** passes unprocessed messages to the [**DefScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-defscreensaverproc) function.</span></span> <span data-ttu-id="c0132-221">Outra diferença entre **ScreenSaverProc** e um procedimento de janela normal é que o identificador passado para **ScreenSaverProc** identifica toda a área de trabalho em vez de uma janela do cliente.</span><span class="sxs-lookup"><span data-stu-id="c0132-221">Another difference between **ScreenSaverProc** and a normal window procedure is that the handle passed to **ScreenSaverProc** identifies the entire desktop rather than a client window.</span></span> <span data-ttu-id="c0132-222">O exemplo a seguir mostra o procedimento de janela **ScreenSaverProc** para a proteção de tela de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c0132-222">The following example shows the **ScreenSaverProc** window procedure for the sample screen saver.</span></span>


```
LONG WINAPI ScreenSaverProc(hwnd, message, wParam, lParam) 
HWND  hwnd; 
UINT  message; 
DWORD wParam; 
LONG  lParam; 
{ 
    static HDC          hdc;      // device-context handle  
    static RECT         rc;       // RECT structure  
    static UINT         uTimer;   // timer identifier  
 
    switch(message) 
    { 
        case WM_CREATE: 
 
            // Retrieve the application name from the .rc file. 
            LoadString(hMainInstance, idsAppName, szAppName, 80 * sizeof(TCHAR)); 
 
            // Retrieve the .ini (or registry) file name. 
            LoadString(hMainInstance, idsIniFile, szIniFile, MAXFILELEN * sizeof(TCHAR)); 
 
            // TODO: Add error checking to verify LoadString success
            //       for both calls.
            
            // Retrieve any redraw speed data from the registry.  
            lSpeed = GetPrivateProfileInt(szAppName, szRedrawSpeed, 
                                          DEFVEL, szIniFile); 
 
            // Set a timer for the screen saver window using the 
            // redraw rate stored in Regedit.ini. 
            uTimer = SetTimer(hwnd, 1, lSpeed * 1000, NULL); 
            break; 
 
        case WM_ERASEBKGND: 
 
            // The WM_ERASEBKGND message is issued before the 
            // WM_TIMER message, allowing the screen saver to 
            // paint the background as appropriate. 

            hdc = GetDC(hwnd); 
            GetClientRect (hwnd, &rc); 
            FillRect (hdc, &rc, GetStockObject(BLACK_BRUSH)); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_TIMER: 
 
            // The WM_TIMER message is issued at (lSpeed * 1000) 
            // intervals, where lSpeed == .001 seconds. This 
            // code repaints the entire desktop with a white, 
            // light gray, dark gray, or black brush each 
            // time a WM_TIMER message is issued. 

            hdc = GetDC(hwnd); 
            GetClientRect(hwnd, &rc); 
            if (i++ <= 4) 
                FillRect(hdc, &rc, GetStockObject(i)); 
            else 
                (i = 0); 
            ReleaseDC(hwnd,hdc); 
            break; 
 
        case WM_DESTROY: 
 
            // When the WM_DESTROY message is issued, the screen saver 
            // must destroy any of the timers that were set at WM_CREATE 
            // time. 

            if (uTimer) 
                KillTimer(hwnd, uTimer); 
            break; 
    } 
 
    // DefScreenSaverProc processes any messages ignored by ScreenSaverProc. 
    return DefScreenSaverProc(hwnd, message, wParam, lParam); 
}
```



### <a name="creating-a-module-definition-file"></a><span data-ttu-id="c0132-223">Criando um arquivo de definição de módulo</span><span class="sxs-lookup"><span data-stu-id="c0132-223">Creating a module-definition file</span></span>

<span data-ttu-id="c0132-224">As funções [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) e [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) devem ser exportadas no arquivo de definição de módulo do aplicativo; No entanto, o [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) não deve ser exportado.</span><span class="sxs-lookup"><span data-stu-id="c0132-224">The [**ScreenSaverProc**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverproc) and [**ScreenSaverConfigureDialog**](/windows/desktop/api/scrnsave/nf-scrnsave-screensaverconfiguredialog) functions must be exported in the application's module-definition file; [**RegisterDialogClasses**](/windows/desktop/api/scrnsave/nf-scrnsave-registerdialogclasses) should not be exported, however.</span></span> <span data-ttu-id="c0132-225">O exemplo a seguir mostra o arquivo de definição de módulo para o aplicativo de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c0132-225">The following example shows the module-definition file for the sample application.</span></span>


```
NAME    SSTEST.SCR 

DESCRIPTION 'SCRNSAVE : Test' 
 
STUB    'WINSTUB.EXE' 
EXETYPE WINDOWS 
 
CODE    MOVEABLE 
DATA    MOVEABLE MULTIPLE 
 
HEAPSIZE  1024 
STACKSIZE 4096 
 
EXPORTS 
        ScreenSaverProc 
        ScreenSaverConfigureDialog
```



### <a name="installing-new-screen-savers"></a><span data-ttu-id="c0132-226">Instalando novas proteções de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-226">Installing New Screen Savers</span></span>

<span data-ttu-id="c0132-227">Ao compilar a lista de proteções de tela disponíveis, o painel de controle pesquisa o diretório de inicialização do Windows em busca de arquivos com a extensão. SCR.</span><span class="sxs-lookup"><span data-stu-id="c0132-227">When compiling the list of available screen savers, the Control Panel searches the Windows Startup directory for files with the .scr extension.</span></span> <span data-ttu-id="c0132-228">Como as proteções de tela são arquivos executáveis padrão do Windows com extensões. exe, você deve renomeá-los para que eles tenham as extensões. SCR e copiá-los para o diretório correto.</span><span class="sxs-lookup"><span data-stu-id="c0132-228">Because screen savers are standard Windows executable files with .exe extensions, you must rename them so they have .scr extensions and copy them to the correct directory.</span></span>

### <a name="adding-help-to-the-screen-saver-configuration-dialog-box"></a><span data-ttu-id="c0132-229">Adicionando ajuda à caixa de diálogo configuração de proteção de tela</span><span class="sxs-lookup"><span data-stu-id="c0132-229">Adding Help to the Screen Saver Configuration Dialog Box</span></span>

<span data-ttu-id="c0132-230">A caixa de diálogo configuração de uma proteção de tela normalmente inclui um botão de **ajuda** .</span><span class="sxs-lookup"><span data-stu-id="c0132-230">The configuration dialog box for a screen saver typically includes a **Help** button.</span></span> <span data-ttu-id="c0132-231">Os aplicativos de proteção de tela podem verificar o identificador do botão de ajuda e chamar a função [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) da mesma forma que a ajuda é fornecida em outros aplicativos baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="c0132-231">Screen saver applications can check for the Help button identifier and call the [**WinHelp**](/windows/desktop/api/winuser/nf-winuser-winhelpa) function in the same way Help is provided in other Windows-based applications.</span></span>

 

 