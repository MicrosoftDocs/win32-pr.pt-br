---
title: Menus (menus e outros recursos)
description: Esta seção discute os menus.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\menus.htm
keywords:
- recursos, menus
- menus, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c376aa1d2f55fa482ca7a2f98f57ae15236bf26b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369048"
---
# <a name="menus-menus-and-other-resources"></a>Menus (menus e outros recursos)

Esta seção descreve os menus e explica como usá-los.

### <a name="in-this-section"></a>Nesta seção



| Nome                                 | Descrição                                                  |
|--------------------------------------|--------------------------------------------------------------|
| [Sobre os menus](about-menus.md)       | Discute os menus.<br/>                                  |
| [Uso de Menus](using-menus.md)       | Fornece exemplos de código de tarefas relacionadas aos menus.<br/> |
| [Referência de menu](menu-reference.md) | Contém a referência de API.<br/>                       |



 

### <a name="menu-functions"></a>Funções de menu



| Nome                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)                                 | Anexa um novo item ao final da barra de menus, menu suspenso, submenu ou menu de atalho especificados. Você pode usar essa função para especificar o conteúdo, a aparência e o comportamento do item de menu. <br/>                                                                                                                                                                                                  |
| [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem)                           | Define o estado do atributo de marca de seleção do item de menu especificado como selecionado ou desmarcado.<br/>                                                                                                                                                                                                                                                                                                      |
| [**CheckMenuRadioItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)                 | Verifica um item de menu especificado e o transforma em um item de rádio. Ao mesmo tempo, a função limpa todos os outros itens de menu no grupo associado e limpa o sinalizador de tipo de item de rádio para esses itens.<br/>                                                                                                                                                                                                    |
| [**CreateMenu**](/windows/desktop/api/Winuser/nf-winuser-createmenu)                                 | Cria um menu. O menu está inicialmente vazio, mas pode ser preenchido com itens de menu usando as funções [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)e [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) . <br/>                                                                                                                                                                        |
| [**CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu)                       | Cria um menu suspenso, submenu ou menu de atalho. Inicialmente, o menu está vazio. Você pode inserir ou acrescentar itens de menu usando a função [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) . Você também pode usar a função [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) para inserir itens de menu e a função [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) para acrescentar itens de menu.<br/>                                                  |
| [**DeleteMenu**](/windows/desktop/api/Winuser/nf-winuser-deletemenu)                                 | Exclui um item do menu especificado. Se o item de menu abrir um menu ou submenu, essa função destruirá o identificador para o menu ou submenu e liberará a memória usada pelo menu ou submenu. <br/>                                                                                                                                                                                                     |
| [**DestroyMenu**](/windows/desktop/api/Winuser/nf-winuser-destroymenu)                               | Destrói o menu especificado e libera qualquer memória ocupada pelo menu. <br/>                                                                                                                                                                                                                                                                                                                          |
| [**DrawMenuBar**](/windows/desktop/api/Winuser/nf-winuser-drawmenubar)                               | Redesenha a barra de menus da janela especificada. Se a barra de menus for alterada depois que o sistema tiver criado a janela, essa função deverá ser chamada para desenhar a barra de menus alterada. <br/>                                                                                                                                                                                                                         |
| [**EnableMenuItem**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem)                         | Habilita, desabilita ou acinzenta o item de menu especificado. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**Menu**](/windows/desktop/api/Winuser/nf-winuser-endmenu)                                       | Encerra o menu ativo do thread de chamada.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**GetMenu**](/windows/desktop/api/Winuser/nf-winuser-getmenu)                                       | Recupera um identificador para o menu atribuído à janela especificada. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**GetMenuBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo)                         | Recupera informações sobre a barra de menus especificada.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**GetMenuCheckMarkDimensions**](/windows/desktop/api/Winuser/nf-winuser-getmenucheckmarkdimensions) | Recupera as dimensões do bitmap de marca de seleção padrão. O sistema exibe esse bitmap ao lado dos itens de menu selecionados. Antes de chamar a função [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) para substituir o bitmap de marca de seleção padrão para um item de menu, um aplicativo deve determinar o tamanho de bitmap correto chamando [**GetMenuCheckMarkDimensions**](/windows/desktop/api/Winuser/nf-winuser-getmenucheckmarkdimensions). <br/> |
| [**GetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem)                 | Determina o item de menu padrão no menu especificado.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**GetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo)                               | Recupera informações sobre um menu especificado.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**GetMenuItemCount**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemcount)                     | Recupera o número de itens no menu especificado. <br/>                                                                                                                                                                                                                                                                                                                                              |
| [**Getmenuitemid**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid)                           | Recupera o identificador de item de menu de um item de menu localizado na posição especificada em um menu. <br/>                                                                                                                                                                                                                                                                                                    |
| [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)                       | Recupera informações sobre um item de menu.<br/>                                                                                                                                                                                                                                                                                                                                                           |
| [**GetMenuItemRect**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemrect)                       | Recupera o retângulo delimitador para o item de menu especificado.<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate)                             | Recupera os sinalizadores de menu associados ao item de menu especificado. Se o item de menu abrir um submenu, essa função também retornará o número de itens no submenu. <br/>                                                                                                                                                                                                                                |
| [**Getmenustring**](/windows/desktop/api/Winuser/nf-winuser-getmenustringa)                           | Copia a cadeia de texto do item de menu especificado no buffer especificado. <br/>                                                                                                                                                                                                                                                                                                                      |
| [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)                                 | Recupera um identificador para o menu suspenso ou o submenu ativado pelo item de menu especificado. <br/>                                                                                                                                                                                                                                                                                                         |
| [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)                           | Permite que o aplicativo acesse o menu janela (também conhecido como menu do sistema ou menu controle) para copiar e modificar. <br/>                                                                                                                                                                                                                                                                  |
| [**HiliteMenuItem**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem)                         | Realça ou remove o realce de um item em uma barra de menus. <br/>                                                                                                                                                                                                                                                                                                                                |
| [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)                         | Insere um novo item de menu na posição especificada em um menu.<br/>                                                                                                                                                                                                                                                                                                                                       |
| [**Ismenu**](/windows/desktop/api/Winuser/nf-winuser-ismenu)                                         | Determina se um identificador é um identificador de menu. <br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)                                     | Carrega o recurso de menu especificado do arquivo executável (. exe) associado a uma instância do aplicativo. <br/>                                                                                                                                                                                                                                                                                        |
| [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta)                     | Carrega o modelo de menu especificado na memória. <br/>                                                                                                                                                                                                                                                                                                                                                      |
| [**MenuItemFromPoint**](/windows/desktop/api/Winuser/nf-winuser-menuitemfrompoint)                   | Determina qual item de menu, se houver, está no local especificado.<br/>                                                                                                                                                                                                                                                                                                                                  |
| [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)                                 | Altera um item de menu existente. Essa função é usada para especificar o conteúdo, a aparência e o comportamento do item de menu. <br/>                                                                                                                                                                                                                                                                           |
| [**RemoveMenu**](/windows/desktop/api/Winuser/nf-winuser-removemenu)                                 | Exclui um item de menu ou desanexa um submenu do menu especificado. Se o item de menu abrir um menu suspenso ou submenu, o [**RemoveMenu**](/windows/desktop/api/Winuser/nf-winuser-removemenu) não destruirá o menu ou seu identificador, permitindo que o menu seja reutilizado. Antes que essa função seja chamada, a função [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) deve recuperar um identificador para o menu suspenso ou submenu. <br/>                         |
| [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu)                                       | Atribui um novo menu à janela especificada. <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**SetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem)                 | Define o item de menu padrão para o menu especificado.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)                               | Define informações para um menu especificado.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps)                 | Associa o bitmap especificado a um item de menu. Se o item de menu for selecionado ou desmarcado, o sistema exibirá o bitmap apropriado ao lado do item de menu. <br/>                                                                                                                                                                                                                                   |
| [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa)                       | Altera informações sobre um item de menu.<br/>                                                                                                                                                                                                                                                                                                                                                             |
| [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)                         | Exibe um menu de atalho no local especificado e controla a seleção de itens no menu. O menu de atalho pode aparecer em qualquer lugar na tela.<br/>                                                                                                                                                                                                                                             |
| [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)                     | Exibe um menu de atalho no local especificado e controla a seleção de itens no menu de atalho. O menu de atalho pode aparecer em qualquer lugar na tela.<br/>                                                                                                                                                                                                                                    |



 

A função a seguir é obsoleta.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-insertmenua"><strong>InsertMenu</strong></a></td>
<td>Insere um novo item de menu em um menu, movendo outros itens para baixo no menu.
<blockquote>
[!Note]<br />
A função <a href="/windows/desktop/api/Winuser/nf-winuser-insertmenua"><strong>InsertMenu</strong></a> foi substituída pela função <a href="/windows/desktop/api/Winuser/nf-winuser-insertmenuitema"><strong>InsertMenuItem</strong></a> . No entanto, você ainda poderá usar o <strong>InsertMenu</strong>se não precisar de nenhum dos recursos estendidos do <strong>InsertMenuItem</strong>.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="menu-notifications"></a>Notificações de menu



| Nome                                                  | Descrição                                                                                                                                                                          |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**comando do WM \_**](wm-command.md)                     | Enviado quando o usuário seleciona um item de comando em um menu, quando um controle envia uma mensagem de notificação para sua janela pai ou quando um pressionamento de teclas de acelerador é traduzido. <br/> |
| [**CONTEXTMENU do WM \_**](wm-contextmenu.md)             | Informa uma janela de que o usuário clicou com o botão direito do mouse (*clicado com* o botão direito) na janela.<br/>                                                                            |
| [**ENTERMENULOOP do WM \_**](wm-entermenuloop.md)         | Informa ao procedimento de janela principal de um aplicativo que um loop modal de menu foi inserido. <br/>                                                                                  |
| [**EXITMENULOOP do WM \_**](wm-exitmenuloop.md)           | Informa ao procedimento de janela principal de um aplicativo que um loop modal de menu foi encerrado. <br/>                                                                                   |
| [**GETTITLEBARINFOEX do WM \_**](wm-gettitlebarinfoex.md) | Enviado para solicitar informações da barra de título estendida. Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .<br/>                                  |
| [**MENUCOMMAND do WM \_**](wm-menucommand.md)             | Enviado quando o usuário faz uma seleção de um menu. <br/>                                                                                                                        |
| [**MENUDRAG do WM \_**](wm-menudrag.md)                   | Enviado ao proprietário de um menu de arrastar e soltar quando o usuário arrasta um item de menu. <br/>                                                                                               |
| [**MENUGETOBJECT do WM \_**](wm-menugetobject.md)         | Enviado ao proprietário de um menu de arrastar e soltar quando o cursor do mouse entra em um item de menu ou se move do centro do item para a parte superior ou inferior do item. <br/>                |
| [**MENURBUTTONUP do WM \_**](wm-menurbuttonup.md)         | Enviado quando o usuário libera o botão direito do mouse enquanto o cursor está em um item de menu. <br/>                                                                                   |
| [**NEXTMENU do WM \_**](wm-nextmenu.md)                   | Enviado a um aplicativo quando a tecla de seta para a direita ou para a esquerda é usada para alternar entre a barra de menus e o menu do sistema. <br/>                                                      |
| [**UNINITMENUPOPUP do WM \_**](wm-uninitmenupopup.md)     | Enviado quando um menu suspenso ou submenu foi destruído. <br/>                                                                                                                |



 

### <a name="menu-structures"></a>Estruturas de menu



| Nome                                                       | Descrição                                                                                                                                                     |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)                         | Contém informações sobre o menu a ser ativado. <br/>                                                                                                |
| [**MENUBARINFO**](/windows/win32/api/winuser/ns-winuser-menubarinfo)                         | Contém informações da barra de menus.<br/>                                                                                                                       |
| [**\_cabeçalho do modelo MENUEX \_**](menuex-template-header.md) | Define o cabeçalho de um modelo de menu estendido. Esta definição de estrutura é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão. <br/> |
| [**\_item de modelo MENUEX \_**](menuex-template-item.md)     | Define um item de menu em um modelo de menu estendido. Esta definição de estrutura é apenas para fins de explicação; Ele não está presente em nenhum arquivo de cabeçalho padrão.<br/>  |
| [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)             | Contém informações sobre o menu em que o cursor do mouse está.<br/>                                                                                     |
| [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo)                               | Contém informações sobre um menu.<br/>                                                                                                                   |
| [**MENUITEMINFO**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa)                       | Contém informações sobre um item de menu. <br/>                                                                                                             |
| [**MENUITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate)               | Define um item de menu em um modelo de menu. <br/>                                                                                                             |
| [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader)   | Define o cabeçalho de um modelo de menu. Um modelo de menu completo consiste em um cabeçalho e uma ou mais listas de itens de menu. <br/>                              |
| [**TPMPARAMS**](/windows/win32/api/winuser/ns-winuser-tpmparams)                             | Contém parâmetros estendidos para a função [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) .<br/>                                                          |



 

 

