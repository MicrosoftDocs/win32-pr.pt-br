---
title: Desabilitando as teclas de atalho em jogos
description: este artigo descreve como desabilitar temporariamente atalhos de teclado no Microsoft Windows para evitar a interrupção do jogo para jogos em tela inteira.
ms.assetid: 732523f9-ecff-c6c2-646d-1bc3443232ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08eae2ee1b30e78b17440f2c6144c529de4e6d7b6272a5d497de5c5e631ac1c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070516"
---
# <a name="disabling-shortcut-keys-in-games"></a>Desabilitando as teclas de atalho em jogos

este artigo descreve como desabilitar temporariamente atalhos de teclado no Microsoft Windows para evitar a interrupção do jogo para jogos em tela inteira. A tecla SHIFT e a tecla CTRL são frequentemente usadas como botões de acionamento ou execução em jogos. se os usuários pressionarem acidentalmente a chave de Windows (localizada próximo a essas chaves), eles poderão fazer com que ele saia do aplicativo de repente, o que ruins a experiência do jogo. Simplesmente usar a tecla SHIFT como um botão de jogo pode executar inadvertidamente o atalho de teclas de aderência que pode exibir uma caixa de diálogo de aviso. Para evitar esses problemas, você deve desabilitar essas chaves ao executar no modo de tela inteira e habilitar as chaves de volta para seus manipuladores padrão ao executar no modo de janela ou sair do aplicativo.

Este artigo descreve como fazer o seguinte:

-   [desabilitar a chave de Windows com um gancho de teclado](#disable-the-windows-key-with-a-keyboard-hook)
-   [Desabilitar as teclas de atalho de acessibilidade](#disable-the-accessibility-shortcut-keys)

## <a name="disable-the-windows-key-with-a-keyboard-hook"></a>desabilitar a chave de Windows com um gancho de teclado

Use um gancho de teclado de baixo nível para filtrar a chave de Windows de ser processada. O gancho de teclado de baixo nível mostrado no exemplo 1 permanece em vigor mesmo que um usuário Minimize a janela ou alterne para outro aplicativo. isso significa que você deve ter cuidado para garantir que a chave de Windows não seja desabilitada quando o aplicativo for desativado. O código no exemplo 1 faz isso manipulando a mensagem do WM \_ ACTIVATEAPP.

> [!Note]  
> esse método funciona em Windows 2000 e em versões posteriores do Windows. Esse método também funciona com contas de usuário com privilégios mínimos (também conhecidos como contas de usuário limitado).

 

Esse método é usado por DXUT e é ilustrado no exemplo de código a seguir.

**Exemplo 1. usando um gancho de teclado de baixo nível para desabilitar a chave de Windows**


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



## <a name="disable-the-accessibility-shortcut-keys"></a>Desabilitar as teclas de atalho de acessibilidade

Windows inclui recursos de acessibilidade como teclas de aderência, teclas de filtragem e alternâncias (consulte [Windows acessibilidade](/previous-versions/visualstudio/visual-studio-6.0/aa227589(v=vs.60))). Cada um deles atende a uma finalidade diferente; As teclas de aderência, por exemplo, foram projetadas para pessoas que têm dificuldade de manter duas ou mais chaves simultaneamente. Cada um desses recursos de acessibilidade também tem um atalho de teclado que permite que o recurso seja ativado ou desativado. Por exemplo, o atalho de teclas de aderência é disparado pressionando a tecla SHIFT cinco vezes. Se a tecla SHIFT também for usada no jogo, o usuário poderá dispará-lo acidentalmente durante a reprodução do jogo. quando o atalho é disparado, Windows (por padrão) apresenta um aviso em uma caixa de diálogo, o que faria com que Windows minimizasse um jogo em execução no modo de tela inteira. Isso, é claro, pode ter um efeito drástico na partida do jogo.

Os recursos de acessibilidade são necessários para alguns clientes e não interferem em jogos de tela inteira; Portanto, você não deve alterar as configurações de acessibilidade. No entanto, como os atalhos para recursos de acessibilidade podem interromper o jogo se forem disparados acidentalmente, você deverá desativar um atalho de acessibilidade somente quando esse recurso não estiver habilitado chamando [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)).

Um atalho de acessibilidade que é desativado pelo [**SystemParametersInfo**](/previous-versions/visualstudio/visual-studio-6.0/aa227580(v=vs.60)) permanece desativado mesmo depois que o aplicativo é encerrado. Isso significa que você deve restaurar as configurações antes de sair do aplicativo. Como é possível que o aplicativo não seja fechado corretamente, você deve gravar essas configurações no armazenamento persistente para que elas possam ser restauradas quando o aplicativo for executado novamente. Você também pode usar um manipulador de exceção para restaurar essas configurações se ocorrer uma falha.

**Para desativar esses atalhos**

1.  Capture as configurações de acessibilidade atuais antes de desabilitá-las.
2.  Desabilite o atalho de acessibilidade quando o aplicativo entrar no modo de tela inteira se o recurso de acessibilidade estiver desativado.
3.  Restaure as configurações de acessibilidade quando o aplicativo entrar no modo de janela ou sair.

Esse método é usado em DXUT e é ilustrado no exemplo de código a seguir.

> [!Note]  
> Esse método funciona quando executado em uma conta de usuário limitada.

 

**Exemplo 2. Desabilitando as teclas de atalho de acessibilidade**


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



 

 