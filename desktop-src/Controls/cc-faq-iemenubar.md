---
title: Como criar uma barra de menus do Internet Explorer-Style
description: À primeira vista, a barra de menus no Microsoft Internet Explorer 5 e posterior é semelhante a um menu padrão. No entanto, ele é bastante diferente quando você começa a usá-lo.
ms.assetid: e0fe25f2-3d49-4c5a-a3f9-2f468f2cfef2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b262bc55407d263c97d4bd7e3938a9794d3a58f5
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103824007"
---
# <a name="how-to-create-an-internet-explorer-style-menu-bar"></a>Como criar uma barra de menus do Internet Explorer-Style

À primeira vista, a barra de menus no Microsoft Internet Explorer 5 e posterior é semelhante a um menu padrão. No entanto, ele é bastante diferente quando você começa a usá-lo.

A captura de tela a seguir mostra a barra de menus do Windows Internet Explorer com o menu ferramentas selecionado.

![captura de tela que mostra a barra de menus do Windows Internet Explorer, com o menu ferramentas selecionado](images/howto8.jpg)

A barra de menus é, na verdade, um controle da barra de ferramentas que se parece com um menu padrão. Em vez de itens de menu de nível superior, uma barra de menus tem uma série de botões somente texto que exibem um menu suspenso quando clicados. No entanto, como um tipo especializado de barra de ferramentas, uma barra de menus tem alguns recursos que os menus padrão não têm:

-   Ele pode ser personalizado usando técnicas de barra de ferramentas padrão, permitindo que o usuário mova, exclua ou adicione itens.
-   Ele pode ter acompanhamento dinâmico, para que os usuários saibam quando estão em um item de nível superior sem precisar clicar em primeiro.

Uma barra de menus pode ser incorporada a um controle rebar, dando a ele os seguintes recursos:

-   Ele pode ter uma garra, que permite ao usuário mover ou redimensionar a banda.
-   Ele pode compartilhar uma faixa no controle rebar com outras faixas, como a barra de ferramentas padrão na ilustração anterior.
-   Ele pode exibir uma divisa quando ela é coberta por uma faixa adjacente, dando ao usuário acesso aos itens ocultos.
-   Ele pode ter um bitmap em segundo plano definido pelo aplicativo.

Este tópico discute como implementar uma barra de menus. Como uma barra de menus é uma implementação especializada de um controle da barra de ferramentas, o foco estará em tópicos específicos das barras de menus. Para obter uma discussão sobre como incorporar uma barra de ferramentas em um controle rebar, consulte [como criar uma barra de ferramentas Explorer-Style da Internet](cc-faq-ietoolbar.md) e [sobre controles Rebar](rebar-controls.md).

-   [Criando uma barra de ferramentas em uma barra de menus](#making-a-toolbar-into-a-menu-bar)
-   [Manipulando a navegação com o menu Hot-Tracking desabilitado](#handling-navigation-with-menu-hot-tracking-disabled)
    -   [Navegação do mouse](#mouse-navigation)
    -   [Navegação por teclado](#keyboard-navigation)
    -   [Navegação mista](#mixed-navigation)
-   [Manipulando a navegação com o menu Hot-Tracking habilitado](#handling-navigation-with-menu-hot-tracking-enabled)
    -   [Processamento de mensagens para rastreamento dinâmico de menu](#message-processing-for-menu-hot-tracking)
    -   [Navegação do mouse](#mouse-navigation)
    -   [Navegação por teclado](#keyboard-navigation)

## <a name="making-a-toolbar-into-a-menu-bar"></a>Criando uma barra de ferramentas em uma barra de menus

Para criar uma barra de ferramentas em uma barra de menus:

-   Crie uma barra de ferramentas simples incluindo [**TBSTYLE \_ plana**](toolbar-control-and-button-styles.md) com os outros sinalizadores de estilo de janela. O **estilo \_ simples TBSTYLE** também permite o controle de acesso. Com esse estilo, a barra de menus é muito parecida com um menu padrão até que o usuário ative um botão. Em seguida, o botão aparece para destacar a barra de ferramentas e solte quando clicado, exatamente como um botão padrão. Como o acompanhamento de quente está habilitado, tudo o que é necessário para ativar um botão é para o cursor passar sobre ele. Se o cursor mudar para outro botão, ele será ativado e o botão antigo é desativado.
-   Crie botões de estilo de lista incluindo [**TBSTYLE \_ lista**](toolbar-control-and-button-styles.md) com os outros sinalizadores de estilo de janela. Esse estilo cria um botão mais fino que é mais parecido com um item de menu de nível superior padrão.
-   Torne os botões somente texto definindo o membro **iBitmap** da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) do botão como I \_ IMAGENONE e o membro **isastring** para o texto do botão.
-   Dê a cada botão o estilo [**\_ suspenso BTNS**](toolbar-control-and-button-styles.md) . Quando o botão é clicado, o controle Toolbar envia ao seu aplicativo uma notificação de [ \_ lista suspensa tbn](tbn-dropdown.md) para solicitar que ele exiba o menu do botão.
-   Incorpore a barra de menus em uma faixa Rebar. Habilite as duas garras e divisas, conforme discutido em [como criar uma barra de ferramentas de Explorer-Style da Internet](cc-faq-ietoolbar.md).
-   Implemente um manipulador de [ \_ lista suspensa tbn](tbn-dropdown.md) para exibir o *menu* suspenso do botão quando ele for clicado. O menu suspenso é um tipo de menu pop-up. Ele é criado usando a função [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) , com seu canto superior esquerdo alinhado ao canto inferior esquerdo do botão.
-   Implemente a navegação do teclado para que a barra de menus esteja totalmente acessível sem um mouse.
-   Implemente o controle de acesso de menus. Com menus padrão, uma vez que o menu de um item de menu de nível superior foi exibido, mover o cursor sobre outro item de nível superior exibe automaticamente seu menu e recolhe o menu do item anterior. O controle da barra de ferramentas irá acompanhar o cursor e alterar a imagem do botão, mas exibirá automaticamente o novo menu. Seu aplicativo deve fazer isso explicitamente.

A maioria desses itens é simples de implementar e é discutida em outro lugar. Veja [como criar uma barra de ferramentas Explorer-Style da Internet](cc-faq-ietoolbar.md), [sobre controles da barra de ferramentas](toolbar-controls-overview.md)ou [sobre controles Rebar](rebar-controls.md) para obter uma discussão geral sobre como usar barras de ferramentas e controles Rebar. Consulte os [menus](/windows/desktop/menurc/menus) para obter uma discussão de como lidar com menus pop-up. Os dois últimos itens, navegação por teclado e controle de acesso de menus, são discutidos no restante deste tópico.

## <a name="handling-navigation-with-menu-hot-tracking-disabled"></a>Manipulando a navegação com o menu Hot-Tracking desabilitado

Os usuários podem optar por navegar na barra de menus com o mouse, o teclado ou uma mistura de ambos. Para implementar a navegação de barra de menus, seu aplicativo deve manipular notificações da barra de ferramentas e monitorar o mouse e o teclado. Essa tarefa pode ser dividida em duas partes distintas: com e sem controle de acesso ao menu. Esta seção discute como tratar a navegação quando nenhum menu é exibido e o controle de acesso de menus não está habilitado.

### <a name="mouse-navigation"></a>Navegação do mouse

Se o controle de acesso ao menu estiver desabilitado, você poderá tratar uma barra de menus como uma barra de ferramentas normal. Se o usuário estiver navegando com um mouse, todo o aplicativo precisará lidar com a [notificação \_ suspensa tbn](tbn-dropdown.md) . Quando essa notificação for recebida, exiba o menu suspenso apropriado e habilite o controle de acesso ao menu. A partir de então, você está no menu regime de rastreamento de quente discutido na [manipulação de navegação com o menu Hot-Tracking habilitado](#handling-navigation-with-menu-hot-tracking-enabled).

Conforme discutido em [navegação mista](#mixed-navigation), você também precisa manipular a notificação [de \_ HOTITEMCHANGE do tbn](tbn-hotitemchange.md) para controlar o botão ativo. Essa notificação é irrelevante se o usuário está apenas navegando com o mouse, mas é necessário quando a navegação do mouse e do teclado são misturadas.

### <a name="keyboard-navigation"></a>Navegação por teclado

Conforme observado na seção anterior, o usuário pode fazer várias operações de navegação com o teclado quando o controle de acesso ao menu estiver desabilitado. Os controles da barra de ferramentas dão suporte à navegação por teclado apenas se tiverem foco. Eles também não manipulam todos os pressionamentos de tecla que são necessários para barras de menu. A solução mais simples para lidar com a navegação de teclado é processar explicitamente os eventos de pressionamento de tecla relevantes.

Se o controle de acesso ao menu estiver desabilitado, seu aplicativo deverá lidar com esses eventos de pressionamento de tecla da seguinte maneira:

-   A tecla F10. Ative o primeiro botão com [**TB de \_ SETHOTITEM**](tb-sethotitem.md).
-   As teclas seta para a esquerda e seta para a direita. Ative o botão adjacente com [**TB \_ SETHOTITEM**](tb-sethotitem.md). Se o usuário tentar navegar para fora da extremidade da barra de menus, ative o primeiro botão na extremidade oposta.
-   A tecla ESCAPE. Desative o botão ativo com [**TB de \_ SETHOTITEM**](tb-sethotitem.md). A barra de menus deve ser retornada ao estado que tinha antes de ativar o primeiro botão.
-   Uma tecla ALT-*Key* Accelerator. Use a mensagem [**TB \_ MAPACCELERATOR**](tb-mapaccelerator.md) para determinar a qual botão o caractere de *chave* corresponde. Exiba o menu suspenso do botão e habilite o controle de acesso ao menu.
-   A tecla SETA PARA BAIXO. Se um botão estiver ativo, mas nenhum menu tiver sido exibido, exiba o menu do botão e habilite o controle de acesso ao menu.
-   A tecla ENTER. Desative o botão ativo com [**TB de \_ SETHOTITEM**](tb-sethotitem.md). A barra de menus deve ser retornada ao estado que tinha antes de ativar o primeiro botão.

### <a name="mixed-navigation"></a>Navegação mista

Os manipuladores de navegação do teclado descritos na seção anterior basicamente fazem duas tarefas: manter o controle do botão ativo e exibir o menu apropriado quando um botão é selecionado. Esses manipuladores são suficientes, desde que o usuário navegue apenas com o teclado. No entanto, os usuários geralmente misturam a navegação por teclado e mouse. Por exemplo, eles podem ativar o primeiro botão com a tecla F10, usar o mouse para ativar um botão diferente e, em seguida, abrir o menu com a tecla de seta para baixo. Se você estiver monitorando apenas os pressionamentos de tecla para controlar a chave ativa, você exibirá o menu errado. Você também deve lidar com a notificação [tbn \_ HOTITEMCHANGE](tbn-hotitemchange.md) para manter o controle do botão ativo com precisão.

## <a name="handling-navigation-with-menu-hot-tracking-enabled"></a>Manipulando a navegação com o menu Hot-Tracking habilitado

Quando o controle de acesso ao menu estiver habilitado, seu aplicativo deverá alterar a maneira como ele responde à navegação do usuário. Para replicar o comportamento dos menus padrão, você deve implementar os recursos a seguir explicitamente.

Com a navegação do mouse:

-   Se o usuário move o cursor sobre outro botão, esse menu aparece imediatamente e o menu anterior desaparece.
-   O rastreamento dinâmico de menu permanece ativo até que o usuário selecione um comando ou clique em um ponto que não seja parte da região do menu. Qualquer ação desativa o controle de acesso ao menu até que outro botão seja clicado.
-   Se o cursor sair do menu, o menu suspenso atual permanecerá até que o cursor volte para, ou o usuário clicar em um ponto fora, a área coberta pelo menu. Se o cursor retornar a um botão diferente daquele que está sendo exibido no momento, o menu antigo será recolhido e o novo menu será exibido.

Com navegação por teclado:

-   A tecla de seta para a direita move o foco para a direita. Se o item tiver um submenu, exiba o submenu. Se o item não tiver um submenu, recolha o menu e qualquer submenu, ative o botão Avançar com [**TB \_ SETHOTITEM**](tb-sethotitem.md)e exiba o menu do botão adjacente. Se o último botão estiver ativo quando essa mensagem for recebida, exiba o menu do primeiro botão.
-   A tecla de seta para a esquerda move o foco para a esquerda. Se o item for um submenu, recolha-o e mude o foco para seu menu pai. Se o item não for um submenu, recolha o menu, ative o botão Avançar com [**TB \_ SETHOTITEM**](tb-sethotitem.md)e exiba o menu desse botão.

<!-- -->

-   A tecla ESCAPE faz backup da exibição uma etapa.
    -   Se um submenu for exibido, ele será recolhido e o foco mudará para o menu pai.
    -   Se o menu de um botão for exibido, ele será recolhido e o controle de acesso ao menu estará desabilitado. O botão do item permanece ativo.
    -   Se nenhum menu for exibido, mas um botão estiver ativo, o botão será desativado e o controle de acesso ao menu estará desabilitado.
-   As teclas de seta para cima e seta para baixo são usadas apenas para navegar em um menu específico.
-   A tecla ENTER inicia o comando associado a um item de menu. Se o item de menu tiver um submenu, a tecla ENTER o exibirá.

Assim como acontece com o caso desabilitado de acompanhamento dinâmico de menus, seu aplicativo deve ser capaz de manipular o mouse, o teclado e a navegação mista. No entanto, o fato de que um menu é exibido significa que as mensagens terão que ser tratadas de forma um pouco diferente.

### <a name="message-processing-for-menu-hot-tracking"></a>Processamento de mensagens para o menu Hot-Tracking

O controle de acesso de menus requer que um menu seja exibido em todos os momentos, além do breve intervalo necessário para alternar para um novo menu. No entanto, o menu suspenso exibido por [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) é modal. Seu aplicativo continuará a receber algumas mensagens diretamente, incluindo [**o \_ comando do WM**](/windows/desktop/menurc/wm-command), [tbn \_ HOTITEMCHANGE](tbn-hotitemchange.md)e mensagens normais relacionadas ao menu, como o [**WM \_ MENUSELECT**](/windows/desktop/menurc/wm-menuselect). No entanto, ele não receberá mensagens de teclado ou mouse de baixo nível diretamente. Para lidar com mensagens como o [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove), você deve definir um gancho de mensagem para interceptar mensagens que são direcionadas para o menu.

Quando um menu suspenso for exibido, defina o gancho da mensagem chamando a função [**SetWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-setwindowshookexa) com o parâmetro *IDHOOK* definido como qu \_ MSGFILTER. Todas as mensagens destinadas ao menu serão passadas para o seu [procedimento de gancho](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)). Por exemplo, o fragmento de código a seguir define um gancho de mensagem que irá interceptar mensagens que vão para um menu suspenso. `MsgHook` é o nome do procedimento de gancho e `hhookMsg` é o identificador para o procedimento.


```
hhookMsg = SetWindowsHookEx(WH_MSGFILTER, MsgHook, HINST_THISDLL, 0);
```



As mensagens de menu são identificadas definindo o parâmetro *nCode* do procedimento de gancho para o \_ menu MSGF. O parâmetro *lParam* apontará para uma estrutura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) com a mensagem. Os detalhes de quais mensagens precisam ser tratadas e como são discutidos no restante deste tópico.

Seu aplicativo deve passar todas as mensagens para o próximo gancho de mensagem chamando a função [**CallNextHookEx**](/windows/desktop/api/winuser/nf-winuser-callnexthookex) . Você também deve enviar mensagens do mouse diretamente para o controle da barra de ferramentas, convertendo quaisquer coordenadas de ponto no espaço de coordenadas do cliente da barra de ferramentas. O envio de mensagens diretamente garante que o controle Toolbar receba as mensagens de mouse apropriadas. Por exemplo, a barra de ferramentas precisa receber mensagens do [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) para rastrear seus botões.

Quando um novo botão é ativado, seu aplicativo deve recolher o antigo menu suspenso com uma mensagem do [**WM \_ cancelable**](/windows/desktop/winmsg/wm-cancelmode) e exibir um novo menu. Ele também deve recolher o menu suspenso quando o foco é tirado da barra de menus com navegação de teclado ou clicando fora da área de menu. Sempre que você recolhe um menu, deve liberar seu gancho de mensagem usando a função [**UnhookWindowsHookEx**](/windows/desktop/api/winuser/nf-winuser-unhookwindowshookex) . Se você precisar exibir outro menu suspenso, crie um novo gancho de mensagem. Quando um comando é iniciado, o menu será recolhido automaticamente, mas você deverá liberar explicitamente o gancho da mensagem.

O exemplo de código a seguir libera o gancho de mensagem que foi definido no exemplo anterior.


```
UnhookWindowsHookEx(hhookMsg);
```



### <a name="mouse-navigation"></a>Navegação do mouse

Quando um controle de barra de ferramentas normal controla os botões de rastreio, ele realça o botão ativo e envia ao aplicativo uma notificação [tbn \_ HOTITEMCHANGE](tbn-hotitemchange.md) sempre que um novo botão é ativado. Seu aplicativo é responsável por exibir o menu suspenso apropriado. Ela deverá:

-   Manipule a notificação [tbn \_ HOTITEMCHANGE](tbn-hotitemchange.md) para acompanhar o botão ativo. Quando o botão ativo for alterado, recolha o menu antigo e crie um novo.
-   Manipule a [notificação \_ suspensa tbn](tbn-dropdown.md) que é enviada quando um botão é clicado. Em seguida, ele deve recolher o menu e desabilitar o controle de acesso de menus. O botão permanece ativo.
-   Manipule as mensagens do [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown), do [**WM \_ RBUTTONDOWN**](/windows/desktop/inputdev/wm-rbuttondown)e do [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) em seu procedimento de gancho de mensagem para controlar a posição do mouse. Se o mouse for clicado fora da área de menu, recolha o menu suspenso atual, desative o controle de acesso ao menu e retorne a barra de menus para seu estado de preativação.
-   Quando um comando de menu é iniciado, desabilite o controle de acesso ao menu. O menu será recolhido automaticamente, mas você deverá liberar explicitamente o gancho da mensagem.

Você também deve manipular mensagens relacionadas ao menu, como a mensagem do [**WM \_ INITMENUPOPUP**](/windows/desktop/menurc/wm-initmenupopup) , que é enviada quando um item de menu precisa exibir um submenu. Para obter uma discussão sobre como lidar com essas mensagens, consulte [menus](/windows/desktop/menurc/menus).

### <a name="keyboard-navigation"></a>Navegação por teclado

Seu aplicativo deve processar mensagens de teclado no procedimento de gancho de mensagem e agir sobre aquelas que afetam o controle de acesso de menus. Os seguintes pressionamentos de tecla devem ser tratados:

-   A tecla ESCAPE. A tecla ESCAPE faz backup da exibição um nível acima. Se um submenu estiver sendo exibido, ele deverá ser recolhido. Se o menu principal de um botão for exibido, recolha-o e desabilite o controle de acesso ao menu. O botão permanece ativo.
-   A tecla SETA PARA A DIREITA. Se o item tiver um submenu, exiba-o. Se o item não tiver um submenu, recolha o menu e qualquer submenu, ative o botão Avançar com [**TB \_ SETHOTITEM**](tb-sethotitem.md)e exiba seu menu. Se o último botão estava ativo quando essa notificação foi recebida, exiba o menu do primeiro botão.
-   A tecla SETA PARA A ESQUERDA. Se o item estiver em um submenu, recolha-o e mude o foco para seu menu pai. Se o item não for um submenu, recolha o menu, ative o botão adjacente com [**TB \_ SETHOTITEM**](tb-sethotitem.md)e exiba seu menu. Se o primeiro botão estava ativo quando essa notificação foi recebida, exiba o menu do último botão.
-   As teclas seta para cima e seta para baixo. Essas chaves são usadas para navegar em um menu, mas não afetam diretamente o controle de acesso de menus.
-   Uma tecla ALT-*Key* Accelerator. Use a mensagem [**TB \_ MAPACCELERATOR**](tb-mapaccelerator.md) para determinar a qual botão o caractere de *chave* corresponde. Se ele corresponder a um botão diferente do atualmente ativo, recolha o menu suspenso atual, ative o botão novo com [**TB \_ SETHOTITEM**](tb-sethotitem.md)e exiba o menu do botão adjacente. Se o *caractere de chave* corresponder ao botão atualmente exibido, recolha o menu suspenso e desabilite o controle de acesso de menus. O botão deve permanecer ativo.

 

 