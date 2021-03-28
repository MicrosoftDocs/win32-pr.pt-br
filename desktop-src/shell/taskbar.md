---
description: A interface do Windows inclui uma barra de ferramentas de área de trabalho de aplicativo especial chamada barra de tarefas. Você pode usar a barra de tarefas do para essa tarefa, como alternar entre janelas abertas e iniciar novos aplicativos.
ms.assetid: 14d520e7-7c15-441d-9662-24b972d208ac
title: A barra de tarefas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cce37991c6265f02ab92ece62dbae341031d272a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989055"
---
# <a name="the-taskbar"></a>A barra de tarefas

A interface do Windows inclui uma [barra de ferramentas de área de trabalho de aplicativo](application-desktop-toolbars.md) especial chamada barra de *tarefas*. Você pode usar a barra de tarefas do para essa tarefa, como alternar entre janelas abertas e iniciar novos aplicativos.

> [!Note]  
> Para obter informações sobre as alterações feitas na barra de tarefas a partir do Windows 7, consulte [extensões da barra de tarefas](taskbar-extensions.md).

 

Este tópico inclui as seções a seguir.

-   [Sobre a barra de tarefas](#about-the-taskbar)
    -   [Opções de exibição da barra de tarefas](#taskbar-display-options)
    -   [Adicionando atalhos ao menu iniciar](#adding-shortcuts-to-the-start-menu)
    -   [Gerenciando botões da barra de tarefas](#managing-taskbar-buttons)
    -   [Adicionando, modificando e excluindo ícones na área de notificação](#adding-modifying-and-deleting-icons-in-the-notification-area)
    -   [Notificação de criação da barra de tarefas](#taskbar-creation-notification)
-   [Usando a barra de tarefas](#using-the-taskbar)
    -   [Adicionando e excluindo ícones da barra de tarefas na área de notificação](#adding-and-deleting-taskbar-icons-in-the-notification-area)
    -   [Recebendo eventos do mouse](#receiving-mouse-events)

## <a name="about-the-taskbar"></a>Sobre a barra de tarefas

A barra de tarefas inclui o seguinte:

-   Menu **Iniciar**
-   Barra de início rápido (somente Windows Vista e anterior)
-   Botões da barra de tarefas
-   Barras de ferramentas (opcional)
-   Área de notificação

O menu **Iniciar** contém comandos que podem acessar programas, documentos e configurações. Esses comandos incluem **todos os programas**, **documentos**, **painel de controle**, **jogos**, **ajuda e suporte**, **desligamento** e **pesquisa de programas e arquivos**.

O **início** em versões anteriores do Windows continha itens como **Localizar** e **executar**, a funcionalidade do que foi incluída em **Pesquisar programas e arquivos** no Windows Vista e versões posteriores.

A barra de início rápido, disponível em versões do Windows anteriores ao Windows 7, contém atalhos para aplicativos. O Windows fornece entradas padrão, como o Windows Internet Explorer, e o usuário pode adicionar outros atalhos que escolherem. Os ícones nessa área respondem a um único clique. No Windows 7 e posterior, essa funcionalidade está incluída nos botões da barra de tarefas.

O Shell coloca um botão na barra de tarefas sempre que um aplicativo cria uma janela sem proprietário, ou seja, uma janela que não tem um pai e que tem os bits de estilo estendido apropriados (consulte [Gerenciando botões da barra de tarefas](#managing-taskbar-buttons), abaixo). Para alternar para uma janela, o usuário clica em seu botão de janela. Essa funcionalidade foi bastante expandida a partir do Windows 7. Para obter mais informações, consulte [extensões da barra de tarefas](taskbar-extensions.md).

Os aplicativos podem colocar ícones na área de notificação para indicar o status de uma operação ou para notificar o usuário sobre um evento. Por exemplo, um aplicativo pode colocar um ícone de impressora na área de notificação para mostrar que um trabalho de impressão está em caminho. No entanto, no Windows 7 e posterior, algumas das informações fornecidas anteriormente pela área de notificação devem ser fornecidas por meio do botão da barra de tarefas de um aplicativo. A área de notificação está localizada na borda direita da barra de tarefas (se a barra de tarefas for horizontal) ou na parte inferior (se a barra de tarefas for vertical). Para obter mais informações, consulte [notificações e a área de notificação](notification-area.md).

A área de notificação também exibirá a hora atual se essa opção estiver selecionada. A opção é encontrada como:

-   **Windows 7 e posterior**: a lista suspensa **relógio** na página **Ativar ou desativar ícones do sistema** do aplicativo do painel de controle **ícones da área de notificação** (também acessível por meio das propriedades da área de notificação).
-   **Windows Vista**: a caixa de seleção de **relógio** na página **área de notificação** da barra de tarefas e da janela Propriedades do **menu iniciar** .
-   **Windows XP**: a caixa de seleção **mostrar o relógio** na **barra de tarefas e** na janela Propriedades do menu iniciar.

O usuário pode clicar com o botão direito do mouse na barra de tarefas para exibir o menu de atalho. O menu de atalho inclui comandos para janelas em cascata, janelas de pilha, mostrar janelas lado a lado, mostrar a área de trabalho, iniciar o Gerenciador de tarefas e definir propriedades da barra de tarefas. O menu de atalho também fornece a opção de adicionar ou remover um conjunto de barras de ferramentas da barra de tarefas. Você pode adicionar novas barras de ferramentas a esse menu registrando-as na \_ categoria DeskBand de CATID. Para obter mais informações, consulte [implementando objetos de banda](band-objects.md). Observe que, a partir do Windows 7, a barra de tarefas e a área de notificação têm menus de atalho separados. Esses menus de atalho compartilham algumas opções, como a disposição da janela e adicionam outras.

### <a name="taskbar-display-options"></a>Opções de exibição da barra de tarefas

A barra de tarefas dá suporte a duas opções de exibição: Ocultar automaticamente e, no Windows Vista e versões anteriores, Always On superior (a barra de tarefas sempre está nesse modo no Windows 7 e posterior). Para definir essas opções, o usuário deve abrir o menu de atalho da barra de tarefas, clicar em **Propriedades** e marcar ou desmarcar a caixa de seleção **ocultar automaticamente a barra** de tarefas ou a caixa de seleção **manter a barra de tarefas no topo de outras janelas** . Para recuperar o estado dessas opções de exibição, use a [**mensagem \_ GetState do ABM**](abm-getstate.md) . Se você quiser ser notificado quando o estado dessas opções de exibição for alterado, processe a mensagem de notificação do [**ABN \_ STATECHANGE**](abn-statechange.md) em seu procedimento de janela. Para alterar o estado dessas opções de exibição, use a [**mensagem \_ SetState do ABM**](abm-setstate.md) .

A *área de trabalho* é a parte da tela não obscurecida pela barra de tarefas. Para recuperar o tamanho da área de trabalho, chame a função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) com o valor de **SPI \_ GETWORKAREA** definido. Para recuperar as coordenadas de retângulo que descrevem o local da barra de tarefas, use a mensagem [**ABM \_ GETTASKBARPOS**](abm-gettaskbarpos.md) .

É possível cobrir a barra de tarefas definindo explicitamente o tamanho do retângulo da janela igual ao tamanho da tela com [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos). Para sistemas Windows 2000 ou posterior, a janela deve ter a opção [**WS \_ Caption**](../winmsg/window-styles.md) ou [**WS \_ THICKFRAME**](../winmsg/window-styles.md), ou a janela deve ser dimensionada para que a área do cliente cubra toda a tela. Além desses sistemas, se a barra de tarefas for definida como Always On superior, ela permanecerá oculta somente quando o aplicativo for o aplicativo em primeiro plano.

### <a name="adding-shortcuts-to-the-start-menu"></a>Adicionando atalhos ao menu iniciar

Para adicionar um item ao submenu **programas** no Microsoft Windows NT 4,0, Windows 2000 e posterior ou Windows 95 ou posterior, siga estas etapas.

1.  Crie um [link do Shell](./links.md) usando a interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .
2.  Obtenha o PIDL da pasta Programs usando [**SHGetSpecialFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetspecialfolderlocation), passando [**\_ programas de CSIDL**](csidl.md).
3.  Adicione o link do Shell à pasta programas. Você também pode criar uma pasta na pasta programas e adicionar o link a essa pasta.

### <a name="managing-taskbar-buttons"></a>Gerenciando botões da barra de tarefas

O Shell cria um botão na barra de tarefas sempre que um aplicativo cria uma janela que não é de propriedade. Para garantir que o botão de janela seja colocado na barra de tarefas, crie uma janela sem proprietário com o estilo estendido [**WS \_ ex \_ APPWINDOW**](../winmsg/extended-window-styles.md) . Para impedir que o botão de janela seja colocado na barra de tarefas, crie a janela sem proprietário com o estilo estendido [**WS \_ ex \_ TOOLWINDOW**](../winmsg/extended-window-styles.md) . Como alternativa, você pode criar uma janela oculta e tornar essa janela oculta o proprietário da janela visível.

O Shell removerá o botão de uma janela da barra de tarefas somente se o estilo da janela der suporte a botões visíveis da barra de tarefas. Se você quiser alterar dinamicamente o estilo de uma janela para uma que não dê suporte a botões da barra de tarefas visíveis, deverá ocultar a janela primeiro (chamando [**a janela de apresentação com o**](/windows/win32/api/winuser/nf-winuser-showwindow) **SW \_ Hide**), alterar o estilo da janela e mostrar a janela.

O botão janela normalmente contém o ícone do aplicativo e o título. No entanto, se o aplicativo não contiver um menu do sistema, o botão janela será criado sem o ícone.

Se você quiser que seu aplicativo obtenha a atenção do usuário quando a janela não estiver ativa, use a função [**FlashWindow**](/windows/win32/api/winuser/nf-winuser-flashwindow) para permitir que o usuário saiba que uma mensagem está aguardando. Essa função pisca o botão de janela. Depois que o usuário clicar no botão de janela para ativar a janela, seu aplicativo poderá exibir a mensagem.

### <a name="modifying-the-contents-of-the-taskbar"></a>Modificando o conteúdo da barra de tarefas

A [versão 4,71 e posterior](versions.md) do Shell32.dll adiciona a capacidade de modificar o conteúdo da barra de tarefas. Em um aplicativo, agora você pode adicionar, remover e ativar botões da barra de tarefas. Ativar o item não ativa a janela; Ele mostra o item conforme pressionado na barra de tarefas.

Os recursos de modificação da barra de tarefas são implementados em um objeto de Component Object Model (COM) (CLSIDlist \_ ) que expõe a interface [**ITASKBARLIST**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) (IID \_ ITaskbarList). Você deve chamar o método [**ITaskbarList:: HrInit**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist-hrinit) para inicializar o objeto. Em seguida, você pode usar os métodos da interface [**ITaskbarList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist) para modificar o conteúdo da barra de tarefas.

### <a name="adding-modifying-and-deleting-icons-in-the-notification-area"></a>Adicionando, modificando e excluindo ícones na área de notificação

Use a [**função \_ NotifyIcon do Shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) para adicionar, modificar ou excluir ícones da área de notificação. O parâmetro *dwMessage* do **shell \_ NotifyIcon** é uma mensagem para a barra de tarefas que especifica a ação a ser executada. O parâmetro *pnid* é um ponteiro para uma estrutura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) que é usada para identificar o ícone e passar quaisquer informações adicionais necessárias para o sistema processar a mensagem.

Você pode executar as seguintes ações com ícones da área de notificação.

-   Para adicionar um ícone à área de notificação da barra de tarefas, chame o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) com o parâmetro *dwMessage* definido como Nim \_ Add. A estrutura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) é usada para especificar a alça e o identificador do ícone e qualquer texto de dica de ferramenta. Se o usuário tiver selecionado a caixa de seleção **Mostrar relógio** nas propriedades da barra de tarefas, o sistema colocará o ícone à esquerda imediata do relógio. Caso contrário, o ícone será exibido no lado direito ou na parte inferior da barra de tarefas. Todos os ícones existentes são deslocados para a esquerda para liberar espaço para o novo ícone.
-   Para modificar as informações de um ícone, incluindo o identificador de ícone, o texto da dica de ferramenta e a mensagem de retorno de chamada, chame o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) com *dwMessage* definido como Nim \_ Modify.
-   Para excluir um ícone da área de notificação, chame o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) com o parâmetro *dwMessage* definido como Nim \_ Delete.

Quando você tiver concluído uma operação de interface do usuário, retorne o foco para a área de notificação chamando o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) com *dwMessage* definido como Nim \_ SETFOCUS. Por exemplo, você pode fazer isso quando um ícone da barra de tarefas exibe um menu de atalho, mas o usuário o cancela pressionando a tecla ESCAPE.

### <a name="receiving-notification-area-callback-messages"></a>Recebendo mensagens de retorno de chamada da área de notificação

Aplicativos normalmente colocam ícones na área de notificação da barra de tarefas para servir como indicadores de status. Você pode fornecer informações adicionais quando o usuário executa ações do mouse, como mover o ponteiro do mouse sobre o ícone ou clicar no ícone.

O sistema notifica você sobre eventos de mouse e teclado enviando uma mensagem de retorno de chamada definida pelo aplicativo que está associada a um ícone específico. Dessa forma, o sistema pode notificar um aplicativo quando o usuário, por exemplo, clicar no ícone ou selecioná-lo pressionando uma tecla.

Você define a mensagem de retorno de chamada de um ícone ao adicionar o ícone à barra de tarefas. O identificador de mensagem de retorno de chamada é especificado no membro **uCallbackMessage** da estrutura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) passada com Nim \_ Add. Quando um evento ocorre, o sistema envia a mensagem de retorno de chamada para o procedimento de janela da janela especificada pelo membro **HWND** . O parâmetro *wParam* da mensagem contém o identificador do ícone da barra de tarefas no qual o evento ocorreu. O parâmetro *lParam* contém a mensagem de mouse ou de teclado associada ao evento. Por exemplo, quando o ponteiro do mouse se move para um ícone da barra de tarefas, *lParam* contém o [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md).

Os resultados de vários eventos de mouse podem ser resumidos da seguinte maneira:

-   Quando o usuário move o ponteiro do mouse sobre o ícone, o sistema exibe o texto da dica de ferramenta que foi especificado em [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa).
-   Quando o usuário clica no ícone, seu aplicativo recebe uma notificação do [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) .
-   Quando o usuário clica com o botão direito do mouse no ícone, seu aplicativo recebe uma notificação do [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) .
-   Quando o usuário clica duas vezes no ícone, seu aplicativo recebe uma notificação do [**WM \_ LBUTTONDBLCLK**](../inputdev/wm-lbuttondblclk.md) .

Normalmente, clicar no ícone faz com que o aplicativo exiba uma janela com informações adicionais, clicar com o botão direito do mouse exibe um menu de atalho e clicar duas vezes executa o comando de menu de atalho padrão.

Para obter um exemplo de como alterar o texto da dica de ferramenta associado a um ícone da área de notificação, consulte [Tooltips de balão para ícones da barra de status](../controls/tooltip-controls.md).

As versões 5,0 e posteriores do Shell tratam eventos de mouse e teclado do [**shell \_**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) , de maneiras diferentes das versões anteriores do Shell encontradas no Windows NT 4,0, Windows 95 e Windows 98. As diferenças são:

-   Se um usuário solicitar o menu de atalho de um ícone de notificação com o teclado, o Shell da versão 5,0 enviará ao aplicativo associado uma mensagem de [**\_ CONTEXTMENU do WM**](../menurc/wm-contextmenu.md) . As versões anteriores enviam as mensagens do [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) e do [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) .
-   Se um usuário selecionar um ícone de notificação com o teclado e ativá-lo com a barra de espaço ou Inserir chave, a versão 5,0 do Shell enviará ao aplicativo associado uma notificação de **\_ seleção de Nin** . As versões anteriores enviam as mensagens do [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) e do [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) .
-   Se um usuário selecionar um ícone de notificação com o mouse e ativá-lo com a tecla ENTER, a versão 5,0 do Shell enviará ao aplicativo associado uma notificação de **\_ seleção do NIN** . As versões anteriores enviam as mensagens do [**WM \_ RBUTTONDOWN**](../inputdev/wm-rbuttondown.md) e do [**WM \_ RBUTTONUP**](../inputdev/wm-rbuttonup.md) .
-   Se um usuário passar o ponteiro do mouse sobre um ícone com o qual uma dica de ferramenta de balão está associada, o Shell da versão 6,0 (Windows XP) enviará as mensagens a seguir.
    -   -   **Nin \_ BALLOONSHOW** -enviado quando o balão é mostrado (os balões são colocados na fila).
        -   **Nin \_ BALLOONHIDE** -enviado quando o balão desaparece — por exemplo, quando o ícone é excluído. Essa mensagem não será enviada se o balão for descartado devido a um tempo limite ou a um clique do mouse.
        -   **Nin \_ BALLOONTIMEOUT** -enviado quando o balão é Descartado devido a um tempo limite.
        -   **Nin \_ BALLOONUSERCLICK** -enviado quando o balão é Descartado devido a um clique do mouse.

Você pode selecionar a maneira como o Shell deve se comportar chamando o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) com *dwMessage* definido como **Nim \_ SetVersion**. Defina o membro **uVersion** da estrutura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) para indicar se você deseja o comportamento da versão 5,0 ou anterior à versão 5,0.

### <a name="taskbar-creation-notification"></a>Notificação de criação da barra de tarefas

Com o Microsoft Internet Explorer 4,0 e posterior, o Shell notifica os aplicativos que a barra de tarefas foi criada. Quando a barra de tarefas é criada, ela registra uma mensagem com a cadeia de caracteres TaskbarCreated e, em seguida, transmite essa mensagem para todas as janelas de nível superior. Quando o aplicativo da barra de tarefas recebe essa mensagem, ele deve assumir que os ícones da barra de tarefas adicionados foram removidos e adicioná-los novamente. Esse recurso geralmente se aplica apenas a serviços que já estão em execução quando o Shell é iniciado. O exemplo a seguir mostra um método muito simplificado para lidar com esse caso.

No Windows 10, a barra de tarefas também transmite essa mensagem quando o DPI da exibição primária é alterado.

```
LRESULT CALLBACK WndProc(HWND hWnd, 
                         UINT uMessage, 
                         WPARAM wParam, 
                         LPARAM lParam)
{
    static UINT s_uTaskbarRestart;

    switch(uMessage)
    {
        case WM_CREATE:
            s_uTaskbarRestart = RegisterWindowMessage(TEXT("TaskbarCreated"));
            break;
        
        default:
            if(uMessage == s_uTaskbarRestart)
                AddTaskbarIcons();
            break;
    }

    return DefWindowProc(hWnd, uMessage, wParam, lParam);
}
```



## <a name="using-the-taskbar"></a>Usando a barra de tarefas

Esta seção inclui exemplos que demonstram como adicionar ícones à área de notificação da barra de tarefas e como processar mensagens de retorno de chamada para ícones da barra de tarefas.

### <a name="adding-and-deleting-taskbar-icons-in-the-notification-area"></a>Adicionando e excluindo ícones da barra de tarefas na área de notificação

Você adiciona um ícone à área de notificação da barra de tarefas preenchendo uma estrutura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) e, em seguida, passando a estrutura para o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) com *dwMessage* definido como **Nim \_ Add**. Os membros da estrutura devem especificar o identificador para a janela que está adicionando o ícone, bem como o identificador de ícone e o identificador de ícone. Você também pode especificar o texto da dica de ferramenta para o ícone. Se você precisar receber mensagens do mouse para o ícone, especifique o identificador da mensagem de retorno de chamada que o sistema deve usar para enviar a mensagem para o procedimento de janela.

A função no exemplo a seguir demonstra como adicionar um ícone à barra de tarefas.


```
// MyTaskBarAddIcon - adds an icon to the notification area. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window to receive callback messages 
// uID - identifier of the icon 
// hicon - handle to the icon to add 
// lpszTip - tooltip text 

BOOL MyTaskBarAddIcon(HWND hwnd, UINT uID, HICON hicon, LPSTR lpszTip) 
{ 
    BOOL res; 
    NOTIFYICONDATA tnid; 
 
    tnid.cbSize = sizeof(NOTIFYICONDATA); 
    tnid.hWnd = hwnd; 
    tnid.uID = uID; 
    tnid.uFlags = NIF_MESSAGE | NIF_ICON | NIF_TIP; 
    tnid.uCallbackMessage = MYWM_NOTIFYICON; 
    tnid.hIcon = hicon; 
    if (lpszTip) 
        hr = StringCbCopyN(tnid.szTip, sizeof(tnid.szTip), lpszTip, 
                           sizeof(tnid.szTip));
        // TODO: Add error handling for the HRESULT.
    else 
        tnid.szTip[0] = (TCHAR)'\0'; 
 
    res = Shell_NotifyIcon(NIM_ADD, &tnid); 
 
    if (hicon) 
        DestroyIcon(hicon); 
 
    return res; 
}
```



Para excluir um ícone da área de notificação da barra de tarefas, preencha uma estrutura [**NOTIFYICONDATA**](/windows/desktop/api/Shellapi/ns-shellapi-notifyicondataa) e chame o [**shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) com *dwMessage* definido como **Nim \_ delete**. Ao excluir um ícone da barra de tarefas, especifique somente os membros **cbSize**, **HWND** e **UID** da estrutura. Por exemplo:


```
// MyTaskBarDeleteIcon - deletes an icon from the notification area. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window that added the icon. 
// uID - identifier of the icon to delete. 

BOOL MyTaskBarDeleteIcon(HWND hwnd, UINT uID) 
{ 
    BOOL res; 
    NOTIFYICONDATA tnid; 
 
    tnid.cbSize = sizeof(NOTIFYICONDATA); 
    tnid.hWnd = hwnd; 
    tnid.uID = uID; 
         
    res = Shell_NotifyIcon(NIM_DELETE, &tnid); 
    return res; 
}
```



### <a name="receiving-mouse-events"></a>Recebendo eventos do mouse

Se você especificar uma mensagem de retorno de chamada para um ícone da barra de tarefas, o sistema enviará a mensagem para seu aplicativo sempre que um evento do mouse ocorrer no retângulo delimitador do ícone. O parâmetro *wParam* da mensagem Especifica o identificador do ícone da barra de tarefas e o parâmetro *lParam* da mensagem Especifica a mensagem que o sistema gerou como resultado do evento do mouse.

A função no exemplo a seguir é de um aplicativo que adiciona os ícones de bateria e de impressora à barra de tarefas. O aplicativo chama a função quando recebe uma mensagem de retorno de chamada. A função determina se o usuário clicou em um dos ícones e, se um clique tiver ocorrido, chama uma função definida pelo aplicativo para exibir informações de status.


```
// On_MYWM_NOTIFYICON - processes callback messages for taskbar icons. 
// wParam - first message parameter of the callback message. 
// lParam - second message parameter of the callback message. 

void On_MYWM_NOTIFYICON(WPARAM wParam, LPARAM lParam) 
{ 
    UINT uID; 
    UINT uMouseMsg; 
 
    uID = (UINT) wParam; 
    uMouseMsg = (UINT) lParam; 
 
    if (uMouseMsg == WM_LBUTTONDOWN) 
    { 
        switch (uID) 
        { 
            case IDI_MYBATTERYICON: 
 
                // The user clicked the battery icon. Display the 
                // battery status. 
                ShowBatteryStatus(); 
                break; 
 
            case IDI_MYPRINTERICON: 
 
                // The user clicked the printer icon. Display the 
                // status of the print job. 
                ShowJobStatus(); 
                break; 
 
            default: 
                break; 
        } 
     } 

     return; 
 }
```



 

 
