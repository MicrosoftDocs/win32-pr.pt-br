---
title: Desabilitando as teclas de atalho em jogos
description: Este artigo descreve como desabilitar temporariamente atalhos de teclado no Microsoft Windows para evitar a interrupção do jogo para jogos em tela inteira.
ms.assetid: 732523f9-ecff-c6c2-646d-1bc3443232ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aff426e0d728150cf5f6ac3cd8d46a711c9b4f8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454167"
---
# <a name="disabling-shortcut-keys-in-games"></a><span data-ttu-id="9fa34-103">Desabilitando as teclas de atalho em jogos</span><span class="sxs-lookup"><span data-stu-id="9fa34-103">Disabling Shortcut Keys in Games</span></span>

<span data-ttu-id="9fa34-104">Este artigo descreve como desabilitar temporariamente atalhos de teclado no Microsoft Windows para evitar a interrupção do jogo para jogos em tela inteira.</span><span class="sxs-lookup"><span data-stu-id="9fa34-104">This articles describes how to temporarily disable keyboard shortcuts in Microsoft Windows to prevent disruption of game play for full screen games.</span></span> <span data-ttu-id="9fa34-105">A tecla SHIFT e a tecla CTRL são frequentemente usadas como botões de acionamento ou execução em jogos.</span><span class="sxs-lookup"><span data-stu-id="9fa34-105">The SHIFT key and the CTRL key are often used as fire or run buttons in games.</span></span> <span data-ttu-id="9fa34-106">Se os usuários pressionarem acidentalmente a tecla Windows (localizada próximo a essas chaves), eles poderão fazer com que ele saia do aplicativo de repente, o que ruins a experiência do jogo.</span><span class="sxs-lookup"><span data-stu-id="9fa34-106">If users accidentally press the Windows key (located near these keys), they can cause themselves to suddenly jump out of the application, which ruins the game experience.</span></span> <span data-ttu-id="9fa34-107">Simplesmente usar a tecla SHIFT como um botão de jogo pode executar inadvertidamente o atalho de teclas de aderência que pode exibir uma caixa de diálogo de aviso.</span><span class="sxs-lookup"><span data-stu-id="9fa34-107">Simply using the SHIFT key as a game button can inadvertently execute the StickyKeys shortcut which may display a warning dialog.</span></span> <span data-ttu-id="9fa34-108">Para evitar esses problemas, você deve desabilitar essas chaves ao executar no modo de tela inteira e habilitar as chaves de volta para seus manipuladores padrão ao executar no modo de janela ou sair do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9fa34-108">To avoid these issues, you should disable these keys when running in full-screen mode, and either enable the keys back to their default handlers when running in windowed mode or exit the application.</span></span>

<span data-ttu-id="9fa34-109">Este artigo descreve como fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9fa34-109">This article describes how to do the following:</span></span>

-   [<span data-ttu-id="9fa34-110">Desabilitar a tecla Windows com um gancho de teclado</span><span class="sxs-lookup"><span data-stu-id="9fa34-110">Disable the Windows Key with a Keyboard Hook</span></span>](#disable-the-windows-key-with-a-keyboard-hook)
-   [<span data-ttu-id="9fa34-111">Desabilitar as teclas de atalho de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="9fa34-111">Disable the Accessibility Shortcut Keys</span></span>](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a><span data-ttu-id="9fa34-112">Desabilitar a tecla Windows com um gancho de teclado</span><span class="sxs-lookup"><span data-stu-id="9fa34-112">Disable the Windows Key with a Keyboard Hook</span></span>

<span data-ttu-id="9fa34-113">Use um gancho de teclado de baixo nível para filtrar a chave do Windows de ser processada.</span><span class="sxs-lookup"><span data-stu-id="9fa34-113">Use a low-level keyboard hook to filter out the Windows key from being processed.</span></span> <span data-ttu-id="9fa34-114">O gancho de teclado de baixo nível mostrado no exemplo 1 permanece em vigor mesmo que um usuário Minimize a janela ou alterne para outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9fa34-114">The low-level keyboard hook shown in Example 1 remains in effect even if a user minimizes the window or switches to another application.</span></span> <span data-ttu-id="9fa34-115">Isso significa que você deve ter cuidado para assegurar que a chave do Windows não seja desabilitada quando o aplicativo for desativado.</span><span class="sxs-lookup"><span data-stu-id="9fa34-115">This means that you must be careful to ensure that the Windows key is not disabled when the application is deactivated.</span></span> <span data-ttu-id="9fa34-116">O código no exemplo 1 faz isso manipulando a mensagem do WM \_ ACTIVATEAPP.</span><span class="sxs-lookup"><span data-stu-id="9fa34-116">The code in Example 1 does this by handling the WM\_ACTIVATEAPP message.</span></span>

> [!Note]  
> <span data-ttu-id="9fa34-117">Esse método funciona no Windows 2000 e em versões posteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="9fa34-117">This method works on Windows 2000 and later versions of Windows.</span></span> <span data-ttu-id="9fa34-118">Esse método também funciona com contas de usuário com privilégios mínimos (também conhecidos como contas de usuário limitado).</span><span class="sxs-lookup"><span data-stu-id="9fa34-118">This method also works with least-privileged user accounts (also known as limited-user accounts).</span></span>

 

<span data-ttu-id="9fa34-119">Esse método é usado por DXUT e é ilustrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="9fa34-119">This method is used by DXUT and is illustrated in the following code example.</span></span>

<span data-ttu-id="9fa34-120">**Exemplo 1. Usando um gancho de teclado de baixo nível para desabilitar a chave do Windows**</span><span class="sxs-lookup"><span data-stu-id="9fa34-120">**Example 1. Using a low-level keyboard hook to disable the Windows key**</span></span>


```C++
HHOOK g_hKeyboardHook;
BOOL g_bFullscreen;
 
INT WINAPI WinMain( HINSTANCE, HINSTANCE, LPSTR, int )
{
    // Initialization
    g_hKeyboardHook = SetWindowsHookEx( WH_KEYBOARD_LL,  LowLevelKeyboardProc, GetModuleHandle(NULL), 0 );
 
    // 
    // main application code here
    // 
 
    // Cleanup before shutdown
    UnhookWindowsHookEx( g_hKeyboardHook );
}
 
 
LRESULT CALLBACK LowLevelKeyboardProc( int nCode, WPARAM wParam, LPARAM lParam )
{
    if (nCode < 0 || nCode != HC_ACTION )  // do not process message 
        return CallNextHookEx( g_hKeyboardHook, nCode, wParam, lParam); 
 
    bool bEatKeystroke = false;
    KBDLLHOOKSTRUCT* p = (KBDLLHOOKSTRUCT*)lParam;
    switch (wParam) 
    {
        case WM_KEYDOWN:  
        case WM_KEYUP:    
        {
            bEatKeystroke = (g_bFullscreen && g_bWindowActive && ((p->vkCode == VK_LWIN) || (p->vkCode == VK_RWIN)));
            break;
        }
    }
 
    if( bEatKeystroke )
        return 1;
    else
        return CallNextHookEx( g_hKeyboardHook, nCode, wParam, lParam );
}
 
 
LRESULT CALLBACK WndProc( HWND hWnd, UINT uMsg, WPARAM wParam, LPARAM lParam )
{
    switch( uMsg )
    {
       case WM_ACTIVATEAPP:
            // g_bWindowActive is used to control if the Windows key is filtered by the keyboard hook or not.
            if( wParam == TRUE )
                g_bWindowActive  = true;           
            else 
                g_bWindowActive  = false;           
            break;
    }
}
```



## <a name="disable-the-accessibility-shortcut-keys"></a><span data-ttu-id="9fa34-121">Desabilitar as teclas de atalho de acessibilidade</span><span class="sxs-lookup"><span data-stu-id="9fa34-121">Disable the Accessibility Shortcut Keys</span></span>

<span data-ttu-id="9fa34-122">O Windows inclui recursos de acessibilidade como teclas de aderência, teclas de filtragem e alternâncias (consulte [acessibilidade do Windows](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))).</span><span class="sxs-lookup"><span data-stu-id="9fa34-122">Windows includes accessibility features such as StickyKeys, FilterKeys, and ToggleKeys (see [Windows Accessibility](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))).</span></span> <span data-ttu-id="9fa34-123">Cada um deles atende a uma finalidade diferente; As teclas de aderência, por exemplo, foram projetadas para pessoas que têm dificuldade de manter duas ou mais chaves simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="9fa34-123">Each of these serves a different purpose; StickyKeys for example, is designed for people who have difficulty holding down two or more keys simultaneously.</span></span> <span data-ttu-id="9fa34-124">Cada um desses recursos de acessibilidade também tem um atalho de teclado que permite que o recurso seja ativado ou desativado.</span><span class="sxs-lookup"><span data-stu-id="9fa34-124">Each of these accessibility features also has a keyboard shortcut that allows the feature to be turned on or off.</span></span> <span data-ttu-id="9fa34-125">Por exemplo, o atalho de teclas de aderência é disparado pressionando a tecla SHIFT cinco vezes.</span><span class="sxs-lookup"><span data-stu-id="9fa34-125">For example, the StickyKeys shortcut is triggered by pressing the SHIFT key five times.</span></span> <span data-ttu-id="9fa34-126">Se a tecla SHIFT também for usada no jogo, o usuário poderá dispará-lo acidentalmente durante a reprodução do jogo.</span><span class="sxs-lookup"><span data-stu-id="9fa34-126">If the SHIFT key is also used in the game, the user could accidentally trigger this shortcut during game play.</span></span> <span data-ttu-id="9fa34-127">Quando o atalho é disparado, o Windows (por padrão) apresenta um aviso em uma caixa de diálogo, o que faria com que o Windows minimizasse um jogo em execução no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="9fa34-127">When the shortcut is triggered, Windows (by default) presents a warning in a dialog box, which would cause Windows to minimize a game running in full-screen mode.</span></span> <span data-ttu-id="9fa34-128">Isso, é claro, pode ter um efeito drástico na partida do jogo.</span><span class="sxs-lookup"><span data-stu-id="9fa34-128">This, of course, can have a drastic effect on game play.</span></span>

<span data-ttu-id="9fa34-129">Os recursos de acessibilidade são necessários para alguns clientes e não interferem em jogos de tela inteira; Portanto, você não deve alterar as configurações de acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="9fa34-129">The accessibility features are required for some customers and do not themselves interfere with full-screen games; therefore, you should not change the accessibility settings.</span></span> <span data-ttu-id="9fa34-130">No entanto, como os atalhos para recursos de acessibilidade podem interromper o jogo se forem disparados acidentalmente, você deverá desativar um atalho de acessibilidade somente quando esse recurso não estiver habilitado chamando [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).</span><span class="sxs-lookup"><span data-stu-id="9fa34-130">However, because the shortcuts for accessibility features can disrupt game play if triggered accidentally, you should turn off an accessibility shortcut only when that feature is not enabled by calling [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).</span></span>

<span data-ttu-id="9fa34-131">Um atalho de acessibilidade que é desativado pelo [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) permanece desativado mesmo depois que o aplicativo é encerrado.</span><span class="sxs-lookup"><span data-stu-id="9fa34-131">An accessibility shortcut that is turned off by [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) remains turned off even after the application has exited.</span></span> <span data-ttu-id="9fa34-132">Isso significa que você deve restaurar as configurações antes de sair do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9fa34-132">This means that you must restore the settings before exiting the application.</span></span> <span data-ttu-id="9fa34-133">Como é possível que o aplicativo não seja fechado corretamente, você deve gravar essas configurações no armazenamento persistente para que elas possam ser restauradas quando o aplicativo for executado novamente.</span><span class="sxs-lookup"><span data-stu-id="9fa34-133">Because it is possible for the application to fail to exit correctly, you should write these settings to persistent storage so that they can be restored when the application is run again.</span></span> <span data-ttu-id="9fa34-134">Você também pode usar um manipulador de exceção para restaurar essas configurações se ocorrer uma falha.</span><span class="sxs-lookup"><span data-stu-id="9fa34-134">You could also use an exception handler to restore these settings if a crash occurs.</span></span>

<span data-ttu-id="9fa34-135">**Para desativar esses atalhos**</span><span class="sxs-lookup"><span data-stu-id="9fa34-135">**To turn off these shortcuts**</span></span>

1.  <span data-ttu-id="9fa34-136">Capture as configurações de acessibilidade atuais antes de desabilitá-las.</span><span class="sxs-lookup"><span data-stu-id="9fa34-136">Capture the current accessibility settings before disabling them.</span></span>
2.  <span data-ttu-id="9fa34-137">Desabilite o atalho de acessibilidade quando o aplicativo entrar no modo de tela inteira se o recurso de acessibilidade estiver desativado.</span><span class="sxs-lookup"><span data-stu-id="9fa34-137">Disable the accessibility shortcut when the application goes into full-screen mode if the accessibility feature is off.</span></span>
3.  <span data-ttu-id="9fa34-138">Restaure as configurações de acessibilidade quando o aplicativo entrar no modo de janela ou sair.</span><span class="sxs-lookup"><span data-stu-id="9fa34-138">Restore the accessibility settings when the application goes into windowed mode or exits.</span></span>

<span data-ttu-id="9fa34-139">Esse método é usado em DXUT e é ilustrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="9fa34-139">This method is used in DXUT, and is illustrated in the following code example.</span></span>

> [!Note]  
> <span data-ttu-id="9fa34-140">Esse método funciona quando executado em uma conta de usuário limitada.</span><span class="sxs-lookup"><span data-stu-id="9fa34-140">This method works when running on a limited user account.</span></span>

 

<span data-ttu-id="9fa34-141">**Exemplo 2. Desabilitando as teclas de atalho de acessibilidade**</span><span class="sxs-lookup"><span data-stu-id="9fa34-141">**Example 2. Disabling accessibility shortcut keys**</span></span>


```C++
STICKYKEYS g_StartupStickyKeys = {sizeof(STICKYKEYS), 0};
TOGGLEKEYS g_StartupToggleKeys = {sizeof(TOGGLEKEYS), 0};
FILTERKEYS g_StartupFilterKeys = {sizeof(FILTERKEYS), 0};    
 
 
INT WINAPI WinMain( HINSTANCE, HINSTANCE, LPSTR, int )
{
    // Save the current sticky/toggle/filter key settings so they can be restored them later
    SystemParametersInfo(SPI_GETSTICKYKEYS, sizeof(STICKYKEYS), &g_StartupStickyKeys, 0);
    SystemParametersInfo(SPI_GETTOGGLEKEYS, sizeof(TOGGLEKEYS), &g_StartupToggleKeys, 0);
    SystemParametersInfo(SPI_GETFILTERKEYS, sizeof(FILTERKEYS), &g_StartupFilterKeys, 0);
 
    // Disable when full screen
    AllowAccessibilityShortcutKeys( true );
 
    // Restore back when going to windowed or shutting down
    AllowAccessibilityShortcutKeys( false );
}
 
 
void AllowAccessibilityShortcutKeys( bool bAllowKeys )
{
    if( bAllowKeys )
    {
        // Restore StickyKeys/etc to original state and enable Windows key      
        STICKYKEYS sk = g_StartupStickyKeys;
        TOGGLEKEYS tk = g_StartupToggleKeys;
        FILTERKEYS fk = g_StartupFilterKeys;
        
        SystemParametersInfo(SPI_SETSTICKYKEYS, sizeof(STICKYKEYS), &g_StartupStickyKeys, 0);
        SystemParametersInfo(SPI_SETTOGGLEKEYS, sizeof(TOGGLEKEYS), &g_StartupToggleKeys, 0);
        SystemParametersInfo(SPI_SETFILTERKEYS, sizeof(FILTERKEYS), &g_StartupFilterKeys, 0);
    }
    else
    {
        // Disable StickyKeys/etc shortcuts but if the accessibility feature is on, 
        // then leave the settings alone as its probably being usefully used
 
        STICKYKEYS skOff = g_StartupStickyKeys;
        if( (skOff.dwFlags & SKF_STICKYKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            skOff.dwFlags &= ~SKF_HOTKEYACTIVE;
            skOff.dwFlags &= ~SKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETSTICKYKEYS, sizeof(STICKYKEYS), &skOff, 0);
        }
 
        TOGGLEKEYS tkOff = g_StartupToggleKeys;
        if( (tkOff.dwFlags & TKF_TOGGLEKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            tkOff.dwFlags &= ~TKF_HOTKEYACTIVE;
            tkOff.dwFlags &= ~TKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETTOGGLEKEYS, sizeof(TOGGLEKEYS), &tkOff, 0);
        }
 
        FILTERKEYS fkOff = g_StartupFilterKeys;
        if( (fkOff.dwFlags & FKF_FILTERKEYSON) == 0 )
        {
            // Disable the hotkey and the confirmation
            fkOff.dwFlags &= ~FKF_HOTKEYACTIVE;
            fkOff.dwFlags &= ~FKF_CONFIRMHOTKEY;
 
            SystemParametersInfo(SPI_SETFILTERKEYS, sizeof(FILTERKEYS), &fkOff, 0);
        }
    }
}
```



 

 