---
description: uma barra de ferramentas de área de trabalho do aplicativo (também chamada de appbar) é uma janela semelhante à barra de tarefas Windows.
ms.assetid: d9f63cb1-e2cc-4a3b-a3b8-de028e0f0123
title: Usando as barras de ferramentas da área de trabalho do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c8604136040f5f3a1b4c1e9fcecb3b0c26b087724f477e592857ca4046d3a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351446"
---
# <a name="using-application-desktop-toolbars"></a>Usando as barras de ferramentas da área de trabalho do aplicativo

uma *barra de ferramentas de área de trabalho do aplicativo* (também chamada de appbar) é uma janela semelhante à barra de tarefas Windows. Ele é ancorado em uma borda da tela e normalmente contém botões que dão ao usuário acesso rápido a outros aplicativos e janelas. O sistema impede que outros aplicativos usem a área de trabalho usada por um AppBar. Qualquer número de appbars pode existir na área de trabalho em um determinado momento.

Este tópico inclui as seções a seguir.

-   [Sobre as barras de ferramentas da área de trabalho do aplicativo](#about-application-desktop-toolbars)
    -   [Enviando mensagens](#sending-messages)
    -   [Registro](#registration)
    -   [Tamanho e posição do AppBar](#appbar-size-and-position)
    -   [Ocultar automaticamente barras de ferramentas da área de trabalho do aplicativo](#autohide-application-desktop-toolbars)
    -   [Mensagens de notificação do AppBar](#appbar-notification-messages)
-   [Registrando uma barra de ferramentas de área de trabalho do aplicativo](#registering-an-application-desktop-toolbar)
-   [Definindo o tamanho e a posição de AppBar](#setting-the-appbar-size-and-position)
-   [Processando mensagens de notificação AppBar](#processing-appbar-notification-messages)

## <a name="about-application-desktop-toolbars"></a>Sobre as barras de ferramentas da área de trabalho do aplicativo

Windows fornece uma API que permite aproveitar os serviços appbar fornecidos pelo sistema. Os serviços ajudam a garantir que os appbars definidos pelo aplicativo operem suavemente entre si e com a barra de tarefas. O sistema mantém informações sobre cada AppBar e envia as mensagens appbars para notificá-las sobre eventos que podem afetar seu tamanho, posição e aparência.

### <a name="sending-messages"></a>enviando mensagens

Um aplicativo usa um conjunto especial de mensagens, chamadas de mensagens AppBar, para adicionar ou remover um AppBar, definir o tamanho e a posição de um AppBar e recuperar informações sobre o tamanho, a posição e o estado da barra de tarefas. Para enviar uma mensagem AppBar, um aplicativo deve usar a função [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) . Os parâmetros da função incluem um identificador de mensagem, como [**ABM \_ New**](abm-new.md)e o endereço de uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) . Os membros da estrutura contêm informações que o sistema precisa para processar a mensagem determinada.

Para qualquer mensagem AppBar determinada, o sistema usa alguns membros da estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) e ignora os outros. No entanto, o sistema sempre usa os membros **cbSize** e **HWND** , portanto, um aplicativo deve preencher esses membros para cada mensagem AppBar. O membro **cbSize** especifica o tamanho da estrutura e o membro **HWND** é o identificador para a janela do AppBar.

Algumas mensagens AppBar solicitam informações do sistema. Ao processar essas mensagens, o sistema copia as informações solicitadas na estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .

### <a name="registration"></a>Registro

O sistema mantém uma lista interna de appbars e mantém informações sobre cada barra na lista. O sistema usa as informações para gerenciar o appbars, executar serviços para eles e enviar mensagens de notificação.

Um aplicativo deve registrar um AppBar (ou seja, adicioná-lo à lista interna) antes de poder receber serviços AppBar do sistema. Para registrar um AppBar, um aplicativo envia a [**\_ nova**](abm-new.md) mensagem do ABM. A estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) acompanhante inclui o identificador para a janela do AppBar e um identificador de mensagem definido pelo aplicativo. O sistema usa o identificador de mensagem para enviar mensagens de notificação para o procedimento de janela da janela AppBar. Para obter mais informações, consulte mensagens de notificação do AppBar.

Um aplicativo cancela o registro de um AppBar enviando a mensagem [**ABM \_ Remove**](abm-remove.md) . O cancelamento do registro de um AppBar o Remove da lista interna do appbars do sistema. O sistema não envia mais mensagens de notificação para o AppBar ou impede que outros aplicativos usem a área de tela usada pelo AppBar. Um aplicativo sempre deve enviar **ABM \_ remover** antes de destruir um AppBar.

### <a name="appbar-size-and-position"></a>Tamanho e posição do AppBar

Um aplicativo deve definir o tamanho e a posição de um AppBar para que ele não interfira em nenhum outro appbars ou na barra de tarefas. Cada AppBar deve ser ancorado a uma borda específica da tela, e vários appbars podem ser ancorados a uma borda. No entanto, se um AppBar for ancorado à mesma borda da barra de tarefas, o sistema garantirá que a barra de tarefas esteja sempre na borda mais externa.

Para definir o tamanho e a posição de um AppBar, um aplicativo primeiro propõe uma borda de tela e um retângulo delimitador para o AppBar enviando a mensagem [**ABM \_ QUERYPOS**](abm-querypos.md) . O sistema determina se qualquer parte da área da tela dentro do retângulo proposto é usada pela barra de tarefas ou por outro AppBar, ajusta o retângulo (se necessário) e retorna o retângulo ajustado para o aplicativo.

Em seguida, o aplicativo envia a mensagem [**ABM \_ SETPOS**](abm-setpos.md) para definir o novo retângulo delimitador para o AppBar. Novamente, o sistema pode ajustar o retângulo antes de retorná-lo para o aplicativo. Por esse motivo, o aplicativo deve usar o retângulo ajustado retornado por **ABM \_ SETPOS** para definir o tamanho final e a posição. O aplicativo pode usar a função [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para mover o AppBar para a posição.

Usando um processo de duas etapas para definir o tamanho e a posição, o sistema permite que o aplicativo forneça comentários intermediários ao usuário durante a operação de movimentação. Por exemplo, se o usuário arrastar um AppBar, o aplicativo poderá exibir um retângulo sombreado indicando que a nova posição antes da AppBar realmente se moverá.

Um aplicativo deve definir o tamanho e a posição de seu AppBar depois de registrá-lo e sempre que o AppBar receber a mensagem de notificação do [**ABN \_ POSCHANGED**](abn-poschanged.md) . Um AppBar recebe essa mensagem de notificação sempre que ocorre uma alteração no estado de tamanho, posição ou visibilidade da barra de tarefas e sempre que outro AppBar no mesmo lado da tela é redimensionado, adicionado ou removido.

Sempre que um AppBar recebe a \_ mensagem de ativação do WM, ele deve enviar a mensagem de [**\_ ativação do ABM**](abm-activate.md) . Da mesma forma, quando um AppBar recebe uma mensagem do WM \_ WINDOWPOSCHANGED, ele deve chamar [**ABM \_ WINDOWPOSCHANGED**](abm-windowposchanged.md). O envio dessas mensagens garante que o sistema Defina corretamente a ordem z de qualquer AutoOcultar appbars na mesma borda.

### <a name="autohide-application-desktop-toolbars"></a>Ocultar automaticamente barras de ferramentas da área de trabalho do aplicativo

Um AutoOcultar AppBar é aquele que normalmente é oculto, mas fica visível quando o usuário move o cursor do mouse para a borda da tela com a qual o AppBar está associado. O AppBar se oculta novamente quando o usuário move o cursor do mouse para fora do retângulo delimitador da barra.

Embora o sistema permita uma série de appbars diferentes a qualquer momento, ele permite apenas um AutoOcultar AppBar de cada vez para cada borda de tela de acordo com uma base de chegada, servida primeiro. O sistema mantém automaticamente a ordem z de um AutoOcultar AppBar (somente dentro de seu grupo de ordem z).

Um aplicativo usa a mensagem [**ABM \_ SETAUTOHIDEBAR**](abm-setautohidebar.md) para registrar ou cancelar o registro de um AutoOcultar AppBar. A mensagem Especifica a borda para o AppBar e um sinalizador que especifica se o AppBar deve ser registrado ou cancelado. A mensagem falhará se uma AutoOcultar AppBar estiver sendo registrada, mas já houver uma associada à borda especificada. Um aplicativo pode recuperar o identificador para o AppBar de AutoOcultar associado a uma borda enviando a mensagem [**ABM \_ GETAUTOHIDEBAR**](abm-getautohidebar.md) .

Um AutoOcultar AppBar não precisa se registrar como um AppBar normal; ou seja, ele não precisa ser registrado enviando a [**\_ nova mensagem ABM**](abm-new.md) . Um AppBar que não está registrado por **ABM \_** se sobrepõe a qualquer appbars ancorado na mesma borda da tela.

### <a name="appbar-notification-messages"></a>Mensagens de notificação do AppBar

O sistema envia mensagens para notificar um AppBar sobre os eventos que podem afetar sua posição e aparência. As mensagens são enviadas no contexto de uma mensagem definida pelo aplicativo. O aplicativo especifica o identificador da mensagem quando envia a nova mensagem [**ABM \_**](abm-new.md) para registrar o AppBar. O código de notificação está no parâmetro *wParam* da mensagem definida pelo aplicativo.

Um AppBar recebe a mensagem de notificação do [**ABN \_ POSCHANGED**](abn-poschanged.md) quando o tamanho, a posição ou o estado de visibilidade da barra de tarefas é alterado, quando outro AppBar é adicionado à mesma borda da tela ou quando outro AppBar na mesma borda da tela é redimensionado ou removido. Um AppBar deve responder a essa mensagem de notificação enviando mensagens [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS**](abm-setpos.md) . Se uma posição de AppBar for alterada, ela deverá chamar a função [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para se mover para a nova posição.

O sistema envia a mensagem de notificação do [**ABN \_ STATECHANGE**](abn-statechange.md) sempre que o estado de ocultar automaticamente ou sempre visível da barra de tarefas for alterado — ou seja, quando o usuário marcar ou desmarcar a caixa de seleção **sempre visível** ou **ocultar automaticamente** na folha de propriedades da barra de tarefas. Um AppBar pode usar essa mensagem de notificação para definir seu estado de acordo com a barra de tarefas, se desejado.

Quando um aplicativo de tela inteira é iniciado ou quando o último aplicativo de tela inteira é fechado, um AppBar recebe a mensagem de notificação do [**ABN \_ FULLSCREENAPP**](abn-fullscreenapp.md) . O parâmetro *lParam* indica se o aplicativo de tela inteira está abrindo ou fechando. Se estiver abrindo, o AppBar deverá soltar para a parte inferior da ordem z. O AppBar deve restaurar sua posição de ordem z quando o último aplicativo de tela inteira tiver sido fechado.

Um AppBar recebe a mensagem de notificação do [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) quando o usuário seleciona o comando Cascade, Tile horizontal ou Tile verticalmente do lado do menu de atalho da barra de tarefas. O sistema envia a mensagem duas vezes — antes de reorganizar as janelas (*lParam* é **verdadeiro**) e depois de organizar as janelas (*lParam* é **falso**).

Um AppBar pode usar mensagens do [**ABN \_ WINDOWARRANGE**](abn-windowarrange.md) para excluir a si mesmo da operação em cascata ou em bloco. Para excluir a si mesmo, o AppBar deve se ocultar quando *lParam* for **true** e se mostrar quando *lParam* for **falso**. Se um AppBar se esconder em resposta a essa mensagem, ele não precisará enviar as mensagens [**ABM \_ QUERYPOS**](abm-querypos.md) e [**ABM \_ SETPOS**](abm-setpos.md) em resposta à operação em cascata ou em bloco.

## <a name="registering-an-application-desktop-toolbar"></a>Registrando uma barra de ferramentas de área de trabalho do aplicativo

Um aplicativo deve registrar um AppBar enviando a [**\_ nova**](abm-new.md) mensagem do ABM. O registro de um AppBar o adiciona à lista interna do sistema e fornece ao sistema um identificador de mensagem a ser usado para enviar mensagens de notificação para o AppBar. Antes de sair, um aplicativo deve cancelar o registro do AppBar enviando a mensagem [**ABM \_ Remove**](abm-remove.md) . O cancelamento do registro remove o AppBar da lista interna do sistema e impede que a barra receba mensagens de notificação AppBar.

A função no exemplo a seguir registra ou cancela o registro de um AppBar, dependendo do valor de um parâmetro de sinalizador booliano.


```C++
// RegisterAccessBar - registers or unregisters an appbar. 
// Returns TRUE if successful, or FALSE otherwise. 

// hwndAccessBar - handle to the appbar 
// fRegister - register and unregister flag 

// Global variables 
//     g_uSide - screen edge (defaults to ABE_TOP) 
//     g_fAppRegistered - flag indicating whether the bar is registered 

BOOL RegisterAccessBar(HWND hwndAccessBar, BOOL fRegister) 
{ 
    APPBARDATA abd; 
    
    // An application-defined message identifier
    APPBAR_CALLBACK = (WM_USER + 0x01);
    
    // Specify the structure size and handle to the appbar. 
    abd.cbSize = sizeof(APPBARDATA); 
    abd.hWnd = hwndAccessBar; 

    if (fRegister) 
    { 
        // Provide an identifier for notification messages. 
        abd.uCallbackMessage = APPBAR_CALLBACK; 

        // Register the appbar. 
        if (!SHAppBarMessage(ABM_NEW, &abd)) 
            return FALSE; 

        g_uSide = ABE_TOP;       // default edge 
        g_fAppRegistered = TRUE; 

    } 
    else 
    { 
        // Unregister the appbar. 
        SHAppBarMessage(ABM_REMOVE, &abd); 
        g_fAppRegistered = FALSE; 
    } 

    return TRUE; 
}
```



## <a name="setting-the-appbar-size-and-position"></a>Definindo o tamanho e a posição de AppBar

Um aplicativo deve definir o tamanho e a posição de um AppBar depois de registrar o AppBar, depois que o usuário move ou dimensiona o AppBar e sempre que o AppBar recebe a mensagem de notificação do [**ABN \_ POSCHANGED**](abn-poschanged.md) . Antes de definir o tamanho e a posição do AppBar, o aplicativo consulta o sistema em busca de um retângulo delimitador aprovado enviando a mensagem [**\_ QUERYPOS do ABM**](abm-querypos.md) . O sistema retorna um retângulo delimitador que não interfira na barra de tarefas ou em qualquer outro AppBar. O sistema ajusta o retângulo puramente por subtração de retângulo; ele não faz nenhum esforço para preservar o tamanho inicial do retângulo. Por esse motivo, a barra de aplicativos deve reajustar o retângulo, conforme necessário, depois de enviar **ABM \_ QUERYPOS.**

Em seguida, o aplicativo passa o retângulo delimitativo de volta para o sistema usando a [**mensagem \_ SETPOS do ABM.**](abm-setpos.md) Em seguida, ele chama [**a função MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) para mover a barra de aplicativos para a posição.

O exemplo a seguir mostra como definir o tamanho e a posição de uma barra de aplicativos.


```C++
// AppBarQuerySetPos - sets the size and position of an appbar. 

// uEdge - screen edge to which the appbar is to be anchored 
// lprc - current bounding rectangle of the appbar 
// pabd - address of the APPBARDATA structure with the hWnd and cbSize members filled

void PASCAL AppBarQuerySetPos(UINT uEdge, LPRECT lprc, PAPPBARDATA pabd) 
{ 
    int iHeight = 0; 
    int iWidth = 0; 

    pabd->rc = *lprc; 
    pabd->uEdge = uEdge; 

    // Copy the screen coordinates of the appbar's bounding 
    // rectangle into the APPBARDATA structure. 
    if ((uEdge == ABE_LEFT) || (uEdge == ABE_RIGHT)) 
    { 
        iWidth = pabd->rc.right - pabd->rc.left; 
        pabd->rc.top = 0; 
        pabd->rc.bottom = GetSystemMetrics(SM_CYSCREEN); 
    } 
    else 
    { 
        iHeight = pabd->rc.bottom - pabd->rc.top; 
        pabd->rc.left = 0; 
        pabd->rc.right = GetSystemMetrics(SM_CXSCREEN); 
    } 

    // Query the system for an approved size and position. 
    SHAppBarMessage(ABM_QUERYPOS, pabd); 

    // Adjust the rectangle, depending on the edge to which the appbar is anchored.
    switch (uEdge) 
    { 
        case ABE_LEFT: 
            pabd->rc.right = pabd->rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            pabd->rc.left = pabd->rc.right - iWidth; 
            break; 

        case ABE_TOP: 
            pabd->rc.bottom = pabd->rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            pabd->rc.top = pabd->rc.bottom - iHeight; 
            break; 
    } 

    // Pass the final bounding rectangle to the system. 
    SHAppBarMessage(ABM_SETPOS, pabd); 

    // Move and size the appbar so that it conforms to the 
    // bounding rectangle passed to the system. 
    MoveWindow(pabd->hWnd, 
               pabd->rc.left, 
               pabd->rc.top, 
               pabd->rc.right - pabd->rc.left, 
               pabd->rc.bottom - pabd->rc.top, 
               TRUE); 

}
```



## <a name="processing-appbar-notification-messages"></a>Processamento de mensagens de notificação da Barra de Aplicativos

Uma barra de aplicativos recebe uma mensagem de notificação quando o estado da barra de tarefas muda, quando um aplicativo de tela inteira é iniciado (ou o último é fechado) ou quando ocorre um evento que pode afetar o tamanho e a posição da barra de aplicativos. O exemplo a seguir mostra como processar as várias mensagens de notificação.


```C++
// AppBarCallback - processes notification messages sent by the system. 

// hwndAccessBar - handle to the appbar 
// uNotifyMsg - identifier of the notification message 
// lParam - message parameter 

void AppBarCallback(HWND hwndAccessBar, UINT uNotifyMsg, 
    LPARAM lParam) 
{ 
    APPBARDATA abd; 
    UINT uState; 

    abd.cbSize = sizeof(abd); 
    abd.hWnd = hwndAccessBar; 

    switch (uNotifyMsg) 
    { 
        case ABN_STATECHANGE: 

            // Check to see if the taskbar's always-on-top state has changed
            // and, if it has, change the appbar's state accordingly.
            uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

            SetWindowPos(hwndAccessBar, 
                         (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                         0, 0, 0, 0, 
                         SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 

            break; 

        case ABN_FULLSCREENAPP: 

            // A full-screen application has started, or the last full-screen
            // application has closed. Set the appbar's z-order appropriately.
            if (lParam) 
            { 
                SetWindowPos(hwndAccessBar, 
                             (ABS_ALWAYSONTOP & uState) ? HWND_TOPMOST : HWND_BOTTOM, 
                             0, 0, 0, 0, 
                             SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 
            else 
            { 
                uState = SHAppBarMessage(ABM_GETSTATE, &abd); 

                if (uState & ABS_ALWAYSONTOP) 
                    SetWindowPos(hwndAccessBar, 
                                 HWND_TOPMOST, 
                                 0, 0, 0, 0, 
                                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE); 
            } 

        case ABN_POSCHANGED: 

            // The taskbar or another appbar has changed its size or position.
            AppBarPosChanged(&abd); 
            break; 
    } 
}
```



A função a seguir ajusta o retângulo delimitado de uma barra de aplicativos e, em seguida, chama a função AppBarQuerySetPos definida pelo aplicativo (incluída na seção anterior) para definir o tamanho e a posição da barra de acordo.


```C++
// AppBarPosChanged - adjusts the appbar's size and position. 

// pabd - address of an APPBARDATA structure that contains information 
//        used to adjust the size and position. 

void PASCAL AppBarPosChanged(PAPPBARDATA pabd) 
{ 
    RECT rc; 
    RECT rcWindow; 
    int iHeight; 
    int iWidth; 

    rc.top = 0; 
    rc.left = 0; 
    rc.right = GetSystemMetrics(SM_CXSCREEN); 
    rc.bottom = GetSystemMetrics(SM_CYSCREEN); 

    GetWindowRect(pabd->hWnd, &rcWindow); 

    iHeight = rcWindow.bottom - rcWindow.top; 
    iWidth = rcWindow.right - rcWindow.left; 

    switch (g_uSide) 
    { 
        case ABE_TOP: 
            rc.bottom = rc.top + iHeight; 
            break; 

        case ABE_BOTTOM: 
            rc.top = rc.bottom - iHeight; 
            break; 

        case ABE_LEFT: 
            rc.right = rc.left + iWidth; 
            break; 

        case ABE_RIGHT: 
            rc.left = rc.right - iWidth; 
            break; 
    } 

    AppBarQuerySetPos(g_uSide, &rc, pabd); 
}
```



 

 
