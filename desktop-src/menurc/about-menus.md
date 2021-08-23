---
title: Sobre os menus
description: Este tópico discute os menus.
ms.assetid: fd0b26f1-93cd-421b-9097-8502ab7681e9
keywords:
- recursos, menus
- menus, sobre
- submenus
- barras de menu
- menus de nível superior
- menus pop-up
- menus suspensos
- menus, nível superior
- menus, pop-up
- menus, suspensos
- nomes de menu
- menus, atalho
- menus, janela
- menus, sistema
- menus, controle
- menus de atalho
- Menu Janela
- Menu do sistema
- Menu de controle
- identificadores de ajuda
- alças do menu
- itens de menu
- itens de comando
- menu-identificadores de item
- menu-posição do item
- selecionando itens de menu
- limpando itens de menu
- menus desenhados pelo proprietário
- menus, proprietário desenhado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34d35ddf55ad31ed27cc12c6adffa5517e0081db6d70b4d01d3b88780a8797bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034483"
---
# <a name="about-menus"></a>Sobre os menus

Um *menu* é uma lista de itens que especificam opções ou grupos de opções (um submenu) para um aplicativo. Clicar em um item de menu abre um submenu ou faz com que o aplicativo execute um comando. Esta seção fornece informações sobre os seguintes tópicos:

-   [Menus e barras de menus](#menu-bars-and-menus)
    -   [Menus de atalho](#shortcut-menus)
    -   [O menu janela](#the-window-menu)
    -   [Identificador da ajuda](#help-identifier)
-   [Acesso ao teclado para menus](#keyboard-access-to-menus)
    -   [Interface de teclado padrão](#standard-keyboard-interface)
    -   [Teclas de acesso do menu](#menu-access-keys)
    -   [Teclas de atalho do menu](#menu-shortcut-keys)
-   [Criação de menu](#menu-creation)
    -   [Recursos de modelo de menu](#menu-template-resources)
    -   [Modelo de menu na memória](#menu-template-in-memory)
    -   [Alças do menu](#menu-handles)
    -   [Funções de criação de menu](#menu-creation-functions)
    -   [Exibição do menu](#menu-display)
    -   [Menus de classe de janela](#window-class-menus)
-   [Itens de menu](#menu-items)
    -   [Itens de comando e itens que abrem submenus](#command-items-and-items-that-open-submenus)
    -   [Menu-identificador de item](#menu-item-identifier)
    -   [Menu-posição do item](#menu-item-position)
    -   [Acessando itens de menu programaticamente](#accessing-menu-items-programmatically)
    -   [Itens de menu padrão](#default-menu-items)
    -   [Itens de menu selecionados e desmarcados](#selected-and-clear-menu-items)
    -   [Itens de menu habilitados, esmaecidos e desabilitados](#enabled-grayed-and-disabled-menu-items)
    -   [Itens de menu realçados](#highlighted-menu-items)
    -   [Itens de menu de desenho proprietário](#owner-drawn-menu-items)
    -   [Separadores de itens de menu e quebras de linha](#menu-item-separators-and-line-breaks)
-   [Mensagens usadas com menus](#messages-used-with-menus)
-   [Destruição de menu](#menu-destruction)

## <a name="menu-bars-and-menus"></a>Menus e barras de menus

Um menu é organizado em uma hierarquia. No nível superior da hierarquia está a barra de *menus*; que contém uma lista de *menus* que, por sua vez, podem conter *submenus*. Uma barra de menus, às vezes, é chamada de *menu de nível superior*, e os menus e submenus também são conhecidos como *menus pop-up*.

Um item de menu pode executar um comando ou abrir um submenu. Um item que executa um comando é chamado de *item de comando* ou *comando*.

Um item na barra de menus quase sempre abre um menu. Barras de menu raramente contêm itens de comando. Um menu aberto na barra de menus cai da barra de menus e, às vezes, é chamado de *menu suspenso*. Quando um menu suspenso é exibido, ele é anexado à barra de menus. Um item de menu na barra de menus que abre um menu suspenso também é chamado de *nome de menu*.

Os nomes de menu em uma barra de menus representam as principais categorias de comandos que um aplicativo fornece. A seleção de um nome de menu na barra de menus normalmente abre um menu cujos itens de menu correspondem aos comandos em uma categoria. Por exemplo, uma barra de menus pode conter um nome de menu de **arquivo** que, quando clicado pelo usuário, ativa um menu com itens de menu, como **novo**, **abrir** e **salvar**. Para obter informações sobre uma barra de menus, chame [**GetMenuBarInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenubarinfo).

Somente uma janela sobreposta ou pop-up pode conter uma barra de menus; uma janela filho não pode conter uma. Se a janela tiver uma barra de título, o sistema posicionará a barra de menus logo abaixo dela. Uma barra de menus está sempre visível. No entanto, um submenu não fica visível até que o usuário selecione um item de menu que o ative. Para obter mais informações sobre janelas sobrepostas e pop-up, consulte [tipos de janela](/windows/desktop/winmsg/window-features).

Cada menu deve ter uma janela de proprietário. O sistema envia mensagens para a janela do proprietário de um menu quando o usuário seleciona o menu ou escolhe um item no menu.

Esta seção aborda os tópicos a seguir.

-   [Menus de atalho](#shortcut-menus)
-   [O menu janela](#the-window-menu)
-   [Identificador da ajuda](#help-identifier)

### <a name="shortcut-menus"></a>Menus de atalho

O sistema também fornece *menus de atalho*. Um menu de atalho não está anexado à barra de menus; Ele pode aparecer em qualquer lugar na tela. Um aplicativo normalmente associa um menu de atalho com uma parte de uma janela, como a área do cliente, ou com um objeto específico, como um ícone. Por esse motivo, esses menus também são chamados de *menus de contexto*.

Um menu de atalho permanece oculto até que o usuário o ative, normalmente clicando com o botão direito do mouse em uma seleção, uma barra de ferramentas ou um botão da barra de tarefas. Geralmente, o menu é exibido na posição do cursor ou mouse.

### <a name="the-window-menu"></a>O menu janela

O menu **janela** (também conhecido como menu do **sistema** ou menu de **controle** ) é um menu pop-up definido e gerenciado quase exclusivamente pelo sistema operacional. O usuário pode abrir o menu janela clicando no ícone do aplicativo na barra de título ou clicando com o botão direito do mouse em qualquer lugar na barra de título.

O menu **janela** fornece um conjunto padrão de itens de menu que o usuário pode escolher para alterar o tamanho ou a posição de uma janela ou fechar o aplicativo. Os itens no menu janela podem ser adicionados, excluídos e modificados, mas a maioria dos aplicativos usa apenas o conjunto padrão de itens de menu. Uma janela sobreposta, pop-up ou filho pode ter um menu de janela. Não é comum uma janela sobreposta ou pop-up não incluir um menu de janela.

Quando o usuário escolhe um comando no menu **janela** , o sistema envia uma mensagem do [**WM \_ SYSCOMMAND**](wm-syscommand.md) para a janela do proprietário do menu. Na maioria dos aplicativos, o procedimento de janela não processa mensagens no menu janela. Em vez disso, ele simplesmente passa as mensagens para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para o processamento padrão do sistema da mensagem. Se um aplicativo Adicionar um comando ao menu janela, o procedimento de janela deverá processar o comando.

Um aplicativo pode usar a função [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu) para criar uma cópia do menu de janela padrão para modificar. Qualquer janela que não use a função **GetSystemMenu** para fazer sua própria cópia do menu janela receberá o menu de janela padrão.

### <a name="help-identifier"></a>Identificador da ajuda

Associado a cada barra de menus, menu, submenu e menu de atalho é um identificador de ajuda. Se o usuário pressionar a tecla F1 enquanto o menu estiver ativo, esse valor será enviado para a janela do proprietário como parte de uma mensagem de [**\_ ajuda do WM**](../shell/wm-help.md) .

## <a name="keyboard-access-to-menus"></a>Acesso ao teclado para menus

O sistema fornece uma interface de teclado padrão para menus. Você pode aprimorar essa interface fornecendo chaves de acesso mnemônico e teclas de atalho (aceleração) para seus itens de menu.

Os tópicos a seguir descrevem a interface de teclado padrão, as chaves de acesso e as teclas de atalho:

-   [Interface de teclado padrão](#standard-keyboard-interface)
-   [Teclas de acesso do menu](#menu-access-keys)
-   [Teclas de atalho do menu](#menu-shortcut-keys)

### <a name="standard-keyboard-interface"></a>Interface de teclado padrão

O sistema foi projetado para trabalhar com ou sem um mouse ou outro dispositivo apontador. Como o sistema fornece uma interface de teclado padrão, o usuário pode usar o teclado para selecionar itens de menu. Essa interface de teclado não precisa de código especial. Um aplicativo recebe uma mensagem de comando se o usuário seleciona um item de menu por meio do teclado ou usando um mouse. A interface de teclado padrão processa os seguintes pressionamentos de teclas.



| Teclas              | Ação                                                                                                                                                                                                                                   |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Caractere alfabético | Seleciona o primeiro item de menu com o caractere especificado como sua chave de acesso. Se o item selecionado invocar um menu, o menu será exibido e o primeiro item será realçado. Caso contrário, o item de menu será escolhido.                            |
| ALT                    | Alterna para dentro e para fora do modo de barra de menus.                                                                                                                                                                                                     |
| ALT+BARRA DE ESPAÇOS           | Exibe o menu janela.                                                                                                                                                                                                                |
| Enter                  | Ativa um menu e seleciona o primeiro item de menu se um item tiver um menu associado a ele. Caso contrário, esse pressionamento de teclas escolhe o item como se o usuário liberasse o botão do mouse enquanto o item estava selecionado.                              |
| ESC                    | Sai do modo de menu.                                                                                                                                                                                                                         |
| SETA PARA A ESQUERDA             | Circula para o item de menu de nível superior anterior. Os itens de menu de nível superior incluem nomes de menu e o menu janela. Se o item selecionado estiver em um menu, a coluna anterior no menu será selecionada ou o item de menu de nível superior anterior será selecionado. |
| SETA PARA A DIREITA            | Funciona como a tecla de seta para a esquerda, exceto na direção oposta. Em menus, esse pressionamento de teclas avança uma coluna. Quando o item selecionado no momento estiver na coluna da extrema direita, o menu avançar será selecionado.                              |
| SETAS para cima ou para baixo      | Ativa um menu quando é pressionado em um nome de menu. Quando pressionado em um menu, a tecla de seta para cima seleciona o item anterior; a tecla de seta para baixo seleciona o próximo item.                                                                  |



 

### <a name="menu-access-keys"></a>Teclas de acesso do menu

A interface de teclado padrão para menus pode ser aprimorada adicionando chaves de acesso (mnemônicos) a itens de menu. Uma tecla de acesso é uma letra sublinhada no texto de um item de menu. Quando um menu está ativo, o usuário pode selecionar um item de menu pressionando a tecla que corresponde à letra sublinhada do item. O usuário torna a barra de menus ativa pressionando a tecla ALT para realçar o primeiro item na barra de menus. Um menu está ativo quando é exibido.

Para criar uma chave de acesso para um item de menu, preceda qualquer caractere na cadeia de caracteres de texto do item com um e comercial. Por exemplo, a cadeia de texto "&mover" faz com que o sistema sublinhar a letra "M".

### <a name="menu-shortcut-keys"></a>Teclas de atalho do menu

Além de ter uma chave de acesso, um item de menu pode ter uma tecla de atalho associada a ele. Uma tecla de atalho é diferente de uma chave de acesso, porque o menu não precisa estar ativo para que a tecla de atalho funcione. Além disso, uma tecla de acesso é *sempre* associada a um item de menu, enquanto uma tecla de atalho *geralmente* (mas não precisa estar) associada a um item de menu.

O texto que identifica a tecla de atalho é adicionado à cadeia de caracteres de texto do item de menu. O texto do atalho é exibido à direita do nome do item de menu, após uma barra invertida e um caractere de tabulação ( \\ t). Por exemplo, "&fechar \\ tAlt + F4" representa um comando de fechamento com a combinação de teclas ALT + F4 como sua tecla de atalho e com a letra "C" como sua chave de acesso. Para obter mais informações, consulte [aceleradores de teclado](keyboard-accelerators.md).

## <a name="menu-creation"></a>Criação de menu

Você pode criar um menu usando um modelo de menu ou funções de criação de menu. Os modelos de menu normalmente são definidos como recursos. Menu-recursos de modelo podem ser carregados explicitamente ou atribuídos como o menu padrão para uma classe de janela. Você também pode criar recursos de modelo de menu dinamicamente na memória.

Os tópicos a seguir descrevem a criação de menu em detalhes:

-   [Recursos de modelo de menu](#menu-template-resources)
-   [Modelo de menu na memória](#menu-template-in-memory)
-   [Alças do menu](#menu-handles)
-   [Funções de criação de menu](#menu-creation-functions)
-   [Exibição do menu](#menu-display)
-   [Menus de classe de janela](#window-class-menus)

### <a name="menu-template-resources"></a>Recursos de modelo de menu

A maioria dos aplicativos cria menus usando recursos de modelo de menu. Um *modelo de menu* define um menu, incluindo os itens na barra de menus e todos os menus. Para obter informações sobre como criar um recurso de modelo de menu, consulte a documentação incluída com suas ferramentas de desenvolvimento.

Depois de criar um recurso de modelo de menu e adicioná-lo ao arquivo executável (.exe) do seu aplicativo, você pode usar a função [**LoadMenu**](/windows/desktop/api/Winuser/nf-winuser-loadmenua) para carregar o recurso na memória. Essa função retorna um identificador para o menu, que você pode atribuir a uma janela usando a função [**SetMenu**](/windows/desktop/api/Winuser/nf-winuser-setmenu) . Você pode atribuir um menu a qualquer janela que não seja uma janela filho.

A implementação de menus como recursos torna mais fácil a localização de um aplicativo para uso em vários países/regiões. Somente o arquivo de definição de recurso precisa ser localizado para cada idioma, não o código-fonte do aplicativo.

### <a name="menu-template-in-memory"></a>Modelo de menu na memória

Um menu pode ser criado a partir de um modelo de menu que é interno na memória em tempo de execução. Por exemplo, um aplicativo que permite que um usuário personalize seu menu pode criar um modelo de menu na memória com base nas preferências do usuário. O aplicativo poderia, então, salvar o modelo em um arquivo ou no registro para uso futuro. Para criar um menu a partir de um modelo na memória, use a função [**LoadMenuIndirect**](/windows/desktop/api/Winuser/nf-winuser-loadmenuindirecta) . Para obter descrições dos formatos de modelo de menu, consulte [recursos de modelo de menu](#menu-template-resources).

Um modelo de menu padrão consiste em uma estrutura [**MENUITEMTEMPLATEHEADER**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplateheader) seguida por uma ou mais estruturas [**MenuItemTemplate**](/windows/desktop/api/Winuser/ns-winuser-menuitemtemplate) .

Um modelo de menu estendido consiste em uma estrutura de [**\_ \_ cabeçalho de modelo MENUEX**](menuex-template-header.md) seguida por uma ou mais estruturas de [**\_ \_ item de modelo MENUEX**](menuex-template-item.md) .

### <a name="menu-handles"></a>Alças do menu

O sistema gera um identificador exclusivo para cada menu. Um *identificador de menu* é um valor do tipo **HMENU** . Um aplicativo deve especificar um identificador de menu em muitas das funções de menu. Você recebe um identificador para uma barra de menus quando cria o menu ou carrega um recurso de menu.

Para recuperar um alça para a barra de menus de um menu que foi criado ou carregado, use a [**função GetMenu.**](/windows/desktop/api/Winuser/nf-winuser-getmenu) Para recuperar um handle para o submenu associado a um item de menu, use a função [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) ou [**GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) Para recuperar um handle para um menu de janela, use a [**função GetSystemMenu.**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)

### <a name="menu-creation-functions"></a>Funções de criação de menu

Usando funções de criação de menu, você pode criar menus em tempo de executar ou adicionar itens de menu aos menus existentes. Você pode usar a [**função CreateMenu**](/windows/desktop/api/Winuser/nf-winuser-createmenu) para criar uma barra de menus vazia e a [**função CreatePopupMenu**](/windows/desktop/api/Winuser/nf-winuser-createpopupmenu) para criar um menu vazio. Você pode salvar determinadas informações de configurações para um menu usando a [**estrutura MENUINFO.**](/windows/win32/api/winuser/ns-winuser-menuinfo) Para obter ou recuperar as configurações de um menu, use [**GetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuinfo) ou [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo). Para adicionar itens a um menu, use a [**função InsertMenuItem.**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema) As funções [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) e [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua) mais antigas ainda têm suporte, mas **InsertMenuItem** deve ser usado para novos aplicativos.

### <a name="menu-display"></a>Exibição de menu

Depois que um menu tiver sido carregado ou criado, ele deverá ser atribuído a uma janela antes que o sistema possa exibi-lo. Você pode atribuir um menu definindo um menu de classe. Para obter mais informações, consulte [Menus de classe de janela](#window-class-menus). Você também pode atribuir um menu a uma janela especificando um alça para o menu como o parâmetro *hMenu* da função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou chamando a [**função SetMenu.**](/windows/desktop/api/Winuser/nf-winuser-setmenu)

Para exibir um menu de atalho, use a [**função TrackPopupMenuEx.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) Menus de atalho, também chamados de menus pop-up flutuantes ou menus de contexto, normalmente são exibidos quando a mensagem [**WM \_ CONTEXTMENU**](wm-contextmenu.md) é processada.

Você pode atribuir um menu a qualquer janela que não seja uma janela filho.

A função [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) mais antiga ainda tem suporte, mas novos aplicativos devem usar a [**função TrackPopupMenuEx.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)

### <a name="window-class-menus"></a>Menus da classe Window

Você pode especificar um menu padrão, chamado *de menu de classe,* ao registrar uma classe de janela. Para fazer isso, atribua o nome do recurso de modelo de menu ao membro **lpszMenuName** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) usada para registrar a classe.

Por padrão, cada janela recebe o menu de classe para sua classe de janela para que você não precise carregar explicitamente o menu e atribuí-lo a cada janela. Você pode substituir o menu de classe especificando um alça de menu diferente em uma chamada para a [**função CreateWindowEx.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Você também pode alterar o menu de uma janela depois que ela é criada usando a [**função SetMenu.**](/windows/desktop/api/Winuser/nf-winuser-setmenu) Para obter mais informações, consulte [Classes de janela](/windows/desktop/winmsg/window-classes).

## <a name="menu-items"></a>Itens de menu

Os tópicos a seguir discutem o que o sistema faz quando o usuário escolhe um item de menu e as maneiras como um aplicativo pode controlar a aparência e a funcionalidade de um item:

-   [Itens e itens de comando que abrem submenus](#command-items-and-items-that-open-submenus)
-   [Identificador do item de menu](#menu-item-identifier)
-   [Posição do item de menu](#menu-item-position)
-   [Acessando itens de menu programaticamente](#accessing-menu-items-programmatically)
-   [Itens de menu padrão](#default-menu-items)
-   [Itens de menu selecionados e des limpar](#selected-and-clear-menu-items)
-   [Itens de menu habilitados, es cinzas e desabilitados](#enabled-grayed-and-disabled-menu-items)
-   [Itens de menu realçadas](#highlighted-menu-items)
-   [Itens de menu desenhados pelo proprietário](#owner-drawn-menu-items)
-   [Separadores de item de menu e quebras de linha](#menu-item-separators-and-line-breaks)

### <a name="command-items-and-items-that-open-submenus"></a>Itens e itens de comando que abrem submenus

Quando o usuário escolhe um item de comando, o sistema envia uma mensagem de comando para a janela que possui o menu. Se o item de comando estiver no menu da janela, o sistema enviará a mensagem [**\_ WM SYSCOMMAND.**](wm-syscommand.md) Caso contrário, ele enviará [**a mensagem \_ WM COMMAND.**](wm-command.md)

Associado a cada item de menu que abre um submenu é um handle para o submenu correspondente. Quando o usuário aponta para esse item, o sistema abre o submenu. Nenhuma mensagem de comando é enviada para a janela do proprietário. No entanto, o sistema envia [**uma mensagem WM \_ INITMENUPOPUP**](wm-initmenupopup.md) para a janela do proprietário antes de exibir o submenu. Você pode obter um handle para o submenu associado a um item usando a [**função GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) ou [**GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)

Uma barra de menus normalmente contém nomes de menu, mas também pode conter itens de comando. Um submenu normalmente contém itens de comando, mas também pode conter itens que abrem submenus aninhados. Ao adicionar esses itens a submenus, você pode aninhar menus a qualquer profundidade. Para fornecer uma indicação visual para o usuário, o sistema exibe automaticamente uma pequena seta à direita do texto de um item de menu que abre um submenu.

### <a name="menu-item-identifier"></a>Menu-Item identificador de Menu-Item

Associado a cada item de menu é um inteiro exclusivo definido pelo aplicativo, chamado de *identificador de item de menu*. Quando o usuário escolhe um item de comando em um menu, o sistema envia o identificador do item para a janela do proprietário como parte de uma mensagem [**\_ WM COMMAND.**](wm-command.md) O procedimento de janela examina o identificador para determinar a origem da mensagem e processa a mensagem de acordo. Além disso, você pode especificar um item de menu usando seu identificador ao chamar funções de menu; por exemplo, para habilitar ou desabilitar um item de menu.

Itens de menu que abrem submenus têm identificadores, assim como os itens de comando. No entanto, o sistema não envia uma mensagem de comando quando esse item é selecionado em um menu. Em vez disso, o sistema abre o submenu associado ao item de menu.

Para recuperar o identificador do item de menu em uma posição especificada, use a função [**GetMenuItemID**](/windows/desktop/api/Winuser/nf-winuser-getmenuitemid) ou [**GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)

### <a name="menu-item-position"></a>Menu-Item posição

Além de ter um identificador exclusivo, cada item de menu em uma barra de menus ou menu tem um valor de posição exclusivo. O item mais à esquerda em uma barra de menus ou o item superior em um menu tem a posição zero. O valor da posição é incrementado para itens de menu subsequentes. O sistema atribui um valor de posição a todos os itens em um menu, incluindo separadores. A ilustração a seguir mostra os valores de posição dos itens em uma barra de menus e em um menu.

![barra de menus e menu](images/csemn-01.png)

Ao chamar uma função de menu que modifica ou recupera informações sobre um item de menu específico, você pode especificar o item usando seu identificador ou sua posição. Para obter mais informações, consulte a próxima seção.

### <a name="accessing-menu-items-programmatically"></a>Acessando itens de menu programaticamente

A maioria das funções de menu permite que você especifique um item de menu por posição ou por comando. Algumas funções usam os sinalizadores **MF \_ BYPOSITION** e **MF \_ BYCOMMAND** para indicar o algoritmo de pesquisa; outras têm um *parâmetro fByPosition* explícito. Se você especificar o item de menu por posição, o número do item será um índice baseado em zero no menu. Se você especificar o item de menu por comando, o menu e seus submenus serão pesquisados por um item cujo identificador de menu é igual ao número de item fornecido. Se mais de um item na hierarquia de menus corresponde ao número do item, não é especificado qual deles é usado. Se os menus contêm identificadores de menu duplicados, você deve usar operações de menu baseadas em posição para evitar essa ambiguidade.

### <a name="default-menu-items"></a>Itens de menu padrão

Um submenu pode conter um item de menu padrão. Quando o usuário abre um submenu clicando duas vezes, o sistema envia uma mensagem de comando para a janela do proprietário do menu e fecha o menu como se o item de comando padrão tivesse sido escolhido. Se não houver nenhum item de comando padrão, o submenu permanecerá aberto. Para recuperar e definir o item padrão para um submenu, use as funções [**GetMenuDefaultItem**](/windows/desktop/api/Winuser/nf-winuser-getmenudefaultitem) e [**SetMenuDefaultItem.**](/windows/desktop/api/Winuser/nf-winuser-setmenudefaultitem)

### <a name="selected-and-clear-menu-items"></a>Itens de menu selecionados e des limpar

Um item de menu pode ser selecionado ou limpo. O sistema exibe um bitmap ao lado dos itens de menu selecionados para indicar o estado selecionado. O sistema não exibe um bitmap ao lado de limpar itens, a menos que um bitmap "clear" definido pelo aplicativo seja especificado. Somente itens de menu em um menu podem ser selecionados; não é possível selecionar itens em uma barra de menus.

Os aplicativos normalmente verificam ou limpam um item de menu para indicar se uma opção está em vigor. Por exemplo, suponha que um aplicativo tenha uma barra de ferramentas que o usuário pode mostrar ou ocultar usando um comando **barra** de ferramentas em um menu. Quando a barra de ferramentas estiver oculta, o item de menu **Barra** de Ferramentas será limpo. Quando o usuário escolhe o comando, o aplicativo verifica o item de menu e mostra a barra de ferramentas.

Um atributo de marca de seleção controla se um item de menu está selecionado. Você pode definir o atributo de marca de seleção de um item de menu usando a [**função CheckMenuItem.**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) Você pode usar a [**função GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) para determinar se um item de menu está selecionado ou limpo no momento.

Em vez de [**CheckMenuItem**](/windows/desktop/api/Winuser/nf-winuser-checkmenuitem) e [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate), você pode usar as funções [**GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa) e [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) para recuperar e definir o estado de verificação de um item de menu.

Às vezes, um grupo de itens de menu corresponde a um conjunto de opções mutuamente exclusivas. Nesse caso, você pode indicar a opção selecionada usando um item de menu de opção selecionado (análogo a um controle de botão de opção). Os itens de opção selecionados são exibidos com um bitmap com marcador em vez de um bitmap de marca de seleção. Para verificar um item de menu e torná-lo um item de opção, use a [**função CheckMenuRadioItem.**](/windows/desktop/api/Winuser/nf-winuser-checkmenuradioitem)

Por padrão, o sistema exibe uma marca de seleção ou bitmap com marcador ao lado de itens de menu selecionados e nenhum bitmap ao lado de itens de menu limpos. No entanto, você pode usar a [**função SetMenuItemBitmaps**](/windows/desktop/api/Winuser/nf-winuser-setmenuitembitmaps) para associar bitmaps selecionados e limpos definidos pelo aplicativo a um item de menu. Em seguida, o sistema usa os bitmaps especificados para indicar o estado selecionado ou des limpo do item de menu.

Bitmaps definidos pelo aplicativo associados a um item de menu devem ter o mesmo tamanho que o bitmap da marca de seleção padrão, as dimensões das quais podem variar dependendo da resolução da tela. Para recuperar as dimensões corretas, use a [**função GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Você pode criar vários recursos de bitmap para resoluções de tela diferentes; criar um recurso de bitmap e dimensioná-lo, se necessário; ou crie um bitmap em tempo de executar e desenhe uma imagem nele. Os bitmaps podem ser monocromáticos ou de cor. No entanto, como os itens de menu são invertidos quando realçados, a aparência de determinados bitmaps de cor invertidos pode ser indesejável. Para obter mais informações, consulte [Bitmaps](/windows/desktop/gdi/bitmaps).

### <a name="enabled-grayed-and-disabled-menu-items"></a>Itens de menu habilitados, es cinzas e desabilitados

Um item de menu pode ser habilitado, es cinza ou desabilitado. Por padrão, um item de menu está habilitado. Quando o usuário escolhe um item de menu habilitado, o sistema envia uma mensagem de comando para a janela do proprietário ou exibe o submenu correspondente, dependendo do tipo de item de menu.

Quando os itens de menu não estão disponíveis para o usuário, eles devem estar es cinzas ou desabilitados. Itens de menu es cinza e desabilitados não podem ser escolhidos. Um item desabilitado é parecido com um item habilitado. Quando o usuário clica em um item desabilitado, o item não é selecionado e nada acontece. Itens desabilitados podem ser úteis em, por exemplo, um tutorial que apresenta um menu que parece ativo, mas não é.

Um aplicativo acinzenva um item de menu indisponível para fornecer uma indicação visual ao usuário de que um comando não está disponível. Você pode usar um item es cinza quando uma ação  não é apropriada (por exemplo, você pode es cinza no **comando** Imprimir no menu Arquivo quando o sistema não tem uma impressora instalada).

A [**função EnableMenuItem**](/windows/desktop/api/Winuser/nf-winuser-enablemenuitem) habilita, em cinza ou desabilita um item de menu. Para determinar se um item de menu está habilitado, esmaeado ou desabilitado, use a [**função GetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa)

Em vez [**de GetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-getmenuiteminfoa), você também pode usar a função [**GetMenuState**](/windows/desktop/api/Winuser/nf-winuser-getmenustate) para determinar se um item de menu está habilitado, esmaeado ou desabilitado.

### <a name="highlighted-menu-items"></a>Itens de menu realçadas

O sistema realça automaticamente os itens de menu em menus à medida que o usuário os seleciona. No entanto, o realçamento pode ser adicionado ou removido explicitamente de um nome de menu na barra de menus usando a [**função HiliteMenuItem.**](/windows/desktop/api/Winuser/nf-winuser-hilitemenuitem) Essa função não tem efeito sobre itens de menu em menus. No **entanto, quando HiliteMenuItem** é usado para realçar um nome de menu, o nome aparece apenas como selecionado. Se o usuário pressionar a tecla ENTER, o item realçado não será escolhido. Esse recurso pode ser útil em, por exemplo, um aplicativo de treinamento que demonstra o uso de menus.

### <a name="owner-drawn-menu-items"></a>Owner-Drawn itens de menu do Owner-Drawn

Um aplicativo pode controlar completamente a aparência de um item de menu usando um *item desenhado pelo proprietário*. Os itens desenhados pelo proprietário exigem que um aplicativo tome total responsabilidade por desenhar os estados selecionados (realçados), selecionados e limpos. Por exemplo, se um aplicativo forneceu um menu de fonte, ele pode desenhar cada item de menu usando a fonte correspondente; o item para Roman seria desenhado com roman, o item para Itálico seria desenhado em itálico e assim por diante. Para obter mais informações, consulte [Criando Owner-Drawn itens de menu](using-menus.md).

### <a name="menu-item-separators-and-line-breaks"></a>Separadores de item de menu e quebras de linha

O sistema fornece um tipo especial de item de menu, chamado *separador*, que aparece como uma linha horizontal. Você pode usar um separador para dividir um menu em grupos de itens relacionados. Um separador não pode ser usado em uma barra de menus e o usuário não pode selecionar um separador.

Quando uma barra de menus contém mais nomes de menu do que caberão em uma linha, o sistema quebra a barra de menus automaticamente em duas ou mais linhas. Você pode fazer com que uma quebra de linha ocorra em um item específico em uma barra de menus atribuindo o sinalizador de tipo **\_ MFT MENUBREAK** ao item. O sistema coloca esse item e todos os itens subsequentes em uma nova linha.

Quando um menu contiver mais itens do que caberá em uma coluna, o menu será truncado. Você pode fazer com que uma quebra de coluna ocorra em um item específico em um menu atribuindo o sinalizador de tipo **\_ MFT MENUBREAK** ao item ou usando a opção MENUBREAK na [instrução MENUITEM.](/windows/desktop/menurc/menuitem-statement) O sistema coloca esse item e todos os itens subsequentes em uma nova coluna. O **sinalizador de tipo \_ MFT MENUBARBREAK** tem o mesmo efeito, exceto que uma linha vertical aparece entre a nova coluna e a antiga.

Se você usar as funções [**AppendMenu,**](/windows/desktop/api/Winuser/nf-winuser-appendmenua) [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)ou [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) para atribuir quebras de linha, deverá atribuir os sinalizadores de tipo **\_ MF MENUBREAK** ou **MF \_ MENUBARBREAK.**

## <a name="messages-used-with-menus"></a>Mensagens usadas com menus

O sistema relata a atividade relacionada ao menu enviando mensagens para o procedimento de janela da janela que possui o menu. O sistema envia uma série de mensagens quando o usuário seleciona itens na barra de menus ou clica no botão direito do mouse para exibir um menu de atalho.

Quando o usuário ativa um item na barra de menus, a janela do proprietário recebe pela primeira vez uma mensagem [**\_ WM SYSCOMMAND.**](wm-syscommand.md) Essa mensagem inclui um sinalizador que indica se o usuário ativou o menu usando o teclado (SC KEYMENU) ou o \_ mouse (SC \_ MOUSEMENU). Para obter mais informações, consulte [Acesso do teclado aos menus.](#keyboard-access-to-menus)

Em seguida, antes de exibir qualquer menu, o sistema envia a mensagem [**WM \_ INITMENU**](wm-initmenu.md) para o procedimento de janela para que um aplicativo possa modificar os menus antes que o usuário os veja. O sistema envia a mensagem **WM \_ INITMENU** apenas uma vez por ativação de menu.

Quando o usuário aponta para um item de menu que abre um submenu, o sistema envia à janela do proprietário a mensagem [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) antes de exibir o submenu. Essa mensagem oferece ao aplicativo a oportunidade de modificar o submenu antes que ele seja exibido.

Sempre que o usuário move o realçamento de um item para outro, o sistema envia uma mensagem [**\_ WM MENUSELECT**](wm-menuselect.md) para o procedimento de janela da janela do proprietário do menu. Essa mensagem identifica o item de menu selecionado no momento. Muitos aplicativos fornecem uma área de informações na parte inferior das janelas principais e usam essa mensagem para exibir informações adicionais sobre o item de menu selecionado.

Quando o usuário escolhe um item de comando em um menu, o sistema envia uma mensagem [**WM \_ COMMAND**](wm-command.md) para o procedimento de janela. A palavra de ordem baixa do parâmetro *wParam* da mensagem **WM \_ COMMAND** contém o identificador do item escolhido. O procedimento de janela deve examinar o identificador e processar a mensagem de acordo.

Você pode salvar informações para um menu usando a [**estrutura MENUINFO.**](/windows/win32/api/winuser/ns-winuser-menuinfo) Se o menu for definido com **um MENUINFO**. **Valor dwStyle** de MNS NOTIFYBYPOS, o sistema envia \_ WM [**\_ MENUCOMMAND em**](wm-menucommand.md) vez do COMANDO [**WM \_**](wm-command.md) quando um item é selecionado. Isso permite que você acesse as informações na estrutura **MENUINFO** e também fornece o índice do item selecionado diretamente.

Nem todos os menus são acessíveis por meio da barra de menus de uma janela. Muitos aplicativos exibem menus de atalho quando o usuário clica no botão direito do mouse em um local específico. Esses aplicativos devem processar a [**mensagem WM \_ CONTEXTMENU**](wm-contextmenu.md) e exibir um menu de atalho, se apropriado. Se um aplicativo não exibir um menu de atalho, ele deverá passar a mensagem **WM \_ CONTEXTMENU** para a [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para processamento padrão.

A [**mensagem \_ WM MENURBUTTONUP**](wm-menurbuttonup.md) é enviada quando o usuário libera o botão direito do mouse enquanto o cursor está em um item de menu. Essa mensagem é fornecida para que os aplicativos possam exibir um menu de atalho ou contexto para um item de menu.

Há algumas mensagens que envolvem apenas menus do tipo "arrastar e soltar". O [**\_ MENU WMGETOBJECT**](wm-menugetobject.md) é enviado ao proprietário de um menu do tipo "arrastar e soltar" quando o cursor do mouse entra em um item de menu ou se move do centro de um item para a parte superior ou inferior de um item. A [**mensagem \_ WM MENUDRAG**](wm-menudrag.md) é enviada quando o usuário realmente arrasta um item de menu.

Quando um menu suspenso ou um submenu for destruído, o sistema enviará uma mensagem [**WM \_ UNINITMENUPOPUP.**](wm-uninitmenupopup.md)

## <a name="menu-destruction"></a>Destruição de menu

Se um menu for atribuído a uma janela e essa janela for destruída, o sistema destruirá automaticamente o menu e seus submenus, liberando o alça do menu e a memória ocupada pelo menu. O sistema não destrói automaticamente um menu que não está atribuído a uma janela. Um aplicativo deve destruir o menu não atribuído chamando a [**função DestroyMenu.**](/windows/desktop/api/Winuser/nf-winuser-destroymenu) Caso contrário, o menu continuará a existir na memória mesmo após o fechamento do aplicativo. Para encerrar o menu ativo do thread de chamada, use [**EndMenu**](/windows/desktop/api/Winuser/nf-winuser-endmenu). Se uma plataforma não dá suporte a **EndMenu,** envie ao proprietário do menu ativo uma mensagem [**WM \_ CANCELMODE.**](/windows/desktop/winmsg/wm-cancelmode)

 

 