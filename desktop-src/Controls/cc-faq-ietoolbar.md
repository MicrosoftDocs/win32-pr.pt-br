---
title: Como criar uma barra de ferramentas de Explorer-Style da Internet
description: Um dos principais recursos da interface do usuário do Windows Internet Explorer é a barra de ferramentas. Ele não apenas fornece aos usuários acesso a uma ampla gama de recursos, e também permite que os usuários personalizem seu layout de acordo com suas preferências pessoais.
ms.assetid: d24969ec-4dea-44c6-b045-5611de8f1cce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d32228f941a7c7e1253884ab5d72368f66f25c7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084937"
---
# <a name="how-to-create-an-internet-explorer-style-toolbar"></a>Como criar uma barra de ferramentas de Explorer-Style da Internet

Um dos principais recursos da interface do usuário do Windows Internet Explorer é a barra de ferramentas. Ele não apenas fornece aos usuários acesso a uma ampla gama de recursos, e também permite que os usuários personalizem seu layout de acordo com suas preferências pessoais.

A captura de tela a seguir mostra a barra de ferramentas do Internet Explorer e realça alguns dos principais recursos.

![captura de tela da barra de ferramentas do Windows Internet Explorer, com rótulos para oito recursos](images/howto1a.jpg)

Essa barra de ferramentas consiste basicamente em um controle rebar com quatro bandas: três barras de ferramentas e uma barra de menus. Como ele é implementado com a API de controles comuns, os desenvolvedores podem criar barras de ferramentas com qualquer ou todos os seus recursos. Este tópico aborda os recursos essenciais da barra de ferramentas do Internet Explorer e como implementá-los em seu aplicativo.

-   [O controle rebar](#the-rebar-control)
    -   [Implementando o controle rebar](#implementing-the-rebar-control)
-   [As barras de ferramentas](#how-to-create-an-internet-explorer-style-toolbar)
    -   [Botões suspensos](#drop-down-buttons)
    -   [Botões de estilo de lista](#list-style-buttons)
    -   [Divisas](#handling-chevrons)
    -   [Acompanhamento dinâmico](#hot-tracking)
-   [Tópicos relacionados](#related-topics)

## <a name="the-rebar-control"></a>O controle rebar

A estrutura subjacente da barra de ferramentas do Internet Explorer é fornecida por um [controle rebar](rebar-controls.md). Esse controle fornece uma maneira para os usuários personalizarem a organização de uma coleção de ferramentas. Cada rebar contém uma ou mais *faixas*, que normalmente são longas, com retângulos estreitos que contêm uma janela filho, normalmente um controle ToolBar.

O controle rebar exibe suas faixas em uma área retangular, normalmente na parte superior da janela. Esse retângulo é subdividido em uma ou mais faixas que são da altura de uma banda. Cada banda pode estar em uma faixa separada, ou várias faixas podem ser colocadas na mesma faixa.

Um controle rebar fornece aos usuários duas maneiras de organizar suas ferramentas:

-   Cada banda geralmente tem uma *garra* em sua borda esquerda. Os garras são usados quando duas ou mais faixas em uma única faixa excedem a largura da janela. Arrastando a garra para a esquerda ou direita, os usuários podem controlar a quantidade de espaço alocada para cada banda.
-   Os usuários podem mover as faixas dentro do retângulo de exibição do rebar arrastando e soltando. Em seguida, o controle rebar altera a exibição para acomodar a nova organização de bandas. Se todas as faixas forem removidas de uma faixa, a altura do rebar será reduzida, aumentando a área de exibição.

Um aplicativo pode adicionar ou remover faixas conforme necessário. Normalmente, os aplicativos permitem que os usuários selecionem quais faixas eles desejam exibir por meio do menu exibir ou de um menu de atalho.

Se a largura combinada das faixas em uma faixa exceder a largura da janela, o controle rebar ajustará suas larguras conforme necessário. Algumas das ferramentas podem ser cobertas pela banda adjacente.

A [versão 5,80](common-control-versions.md) dos controles comuns fornece uma maneira de tornar as ferramentas cobertas por outra banda acessível ao usuário. Se você definir o \_ sinalizador RBBS USECHEVRON no membro **fStyle** da estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) da banda, uma *divisa* será exibida para as barras de ferramentas que foram cobertas. Quando um usuário clica na divisa, é exibido um menu que permite que ele use as ferramentas ocultas. A captura de tela a seguir do Microsoft Internet Explorer 6 mostra o menu que é exibido quando parte da barra de ferramentas padrão é coberta.

![captura de tela que mostra o menu exibido clicando na divisa](images/howto2.jpg)

Como cada banda contém um controle, você pode fornecer flexibilidade adicional por meio da API do controle. Por exemplo, você pode implementar a personalização da barra de ferramentas para permitir que o usuário adicione, mova ou exclua botões em uma barra de ferramentas.

### <a name="implementing-the-rebar-control"></a>Implementando o controle rebar

A maioria dos recursos da barra de ferramentas do Internet Explorer é realmente implementada nas bandas individuais. A implementação do controle rebar em si é direta e está listada abaixo.

1.  Crie o controle rebar com [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Defina *dwExStyle* como [**WS \_ ex \_ TOOLWINDOW**](/windows/desktop/winmsg/extended-window-styles) e *lpClassName* como [**REBARCLASSNAME**](common-control-window-classes.md). O Internet Explorer usa os seguintes estilos de janela:

    -   [**\_BANDBORDERS RBS**](rebar-control-styles.md)
    -   [**\_DBLCLKTOGGLE RBS**](rebar-control-styles.md)
    -   [**\_REGISTERDROP RBS**](rebar-control-styles.md)
    -   [**\_VARHEIGHT RBS**](rebar-control-styles.md)
    -   [**CCS \_ NOdivider**](common-control-styles.md)
    -   [**CCS \_ NOPARENTALIGN**](common-control-styles.md)
    -   [**WS \_ Border**](/windows/desktop/winmsg/window-styles)
    -   [**WS- \_ filho**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ CLIPCHILDREN**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ CLIPSIBLINGS**](/windows/desktop/winmsg/window-styles)
    -   [**WS \_ visível**](/windows/desktop/winmsg/window-styles)

    Defina os outros parâmetros conforme apropriado para seu aplicativo.

2.  Crie um controle com [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou uma função de criação de controle especializada, como [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex).
3.  Inicialize uma banda para o controle preenchendo os membros de [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa). Inclua o \_ estilo RBBS USECHEVRON com o membro **fStyle** para habilitar divisas.
4.  Adicione a banda ao controle rebar com uma mensagem [**\_ INSERTBAND RB**](rb-insertband.md) .
5.  Repita as etapas 2-4 para as faixas restantes.
6.  Implemente manipuladores para as notificações de rebar. Em particular, você precisará manipular [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) para exibir um menu suspenso quando uma divisa for clicada. Para obter mais informações, consulte lidando com as [divisas](#handling-chevrons).

Os garras são incluídos por padrão. Para omitir a garra de uma banda, defina o \_ sinalizador NOgarraer RBBS no membro **fStyle** da estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) da banda. Para obter mais informações sobre como implementar controles Rebar, consulte [sobre controles Rebar](rebar-controls.md).

### <a name="handling-chevrons"></a>Lidando com divisas

Quando um usuário clica em uma divisa, o controle rebar envia ao aplicativo uma notificação [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) . A estrutura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) que é passada com a notificação contém o identificador da banda e uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) com o retângulo ocupado pela divisa. Seu manipulador deve determinar quais botões estão ocultos e exibir os comandos associados em um menu pop-up.

O procedimento a seguir descreve como lidar com uma notificação [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) :

1.  Recupere o retângulo delimitador atual para a faixa selecionada enviando o controle rebar de uma mensagem [**RB \_ GetRect**](rb-getrect.md) .
2.  Recupere o número total de botões enviando a barra de ferramentas da banda uma [**mensagem \_ BUTTONCOUNT de TB**](tb-buttoncount.md) .
3.  A partir do botão mais à esquerda, recupere o retângulo delimitador do botão enviando a barra de ferramentas controle uma mensagem [**\_ GETITEMRECT TB**](tb-getitemrect.md) .
4.  Passe os retângulos de faixa e botão para a função [**IntersectRect**](/windows/desktop/api/winuser/nf-winuser-intersectrect) . Essa função retornará uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que corresponde à parte visível do botão.
5.  Passe o retângulo do botão e o retângulo da parte visível do botão para a função [**EqualRect**](/windows/desktop/api/winuser/nf-winuser-equalrect) .
6.  Se [**EqualRect**](/windows/desktop/api/winuser/nf-winuser-equalrect) retornar **true**, o botão inteiro ficará visível. Repita as etapas 3-5 para o botão Avançar na barra de ferramentas. Se **EqualRect** retornar **false**, o botão será, pelo menos, parcialmente oculto e todos os botões restantes serão completamente ocultos. Siga para a próxima etapa.
7.  Crie um menu pop-up com itens para cada um dos botões ocultos.
8.  Exiba o menu pop-up usando a função [**TrackPopupMenu**](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu) . Use o retângulo de divisa que foi passado com a notificação [RBN \_ CHEVRONPUSHED](rbn-chevronpushed.md) para posicionar o menu. O menu deve estar imediatamente abaixo da divisa, com as bordas esquerda alinhadas.
9.  Manipule os comandos do menu.

## <a name="the-toolbars"></a>As barras de ferramentas

A maior parte da complexidade da barra de ferramentas do Internet Explorer está na implementação de controles que compõem as bandas de rebar. O Internet Explorer geralmente exibe quatro faixas:

-   A barra de menus
-   A barra de ferramentas padrão
-   A barra de ferramentas links
-   A barra de ferramentas de endereço

Todas essas faixas, incluindo a barra de menus, realmente mantêm os controles da barra de ferramentas. Esta seção aborda a implementação das barras de ferramentas padrão e links. A barra de menus é um pouco mais complicada e é discutida separadamente em [como criar uma barra de menus Explorer-Style da Internet](cc-faq-iemenubar.md).

Os procedimentos básicos para implementação de controles da barra de ferramentas são discutidos em [sobre controles da barra de ferramentas](toolbar-controls-overview.md). Esta seção se concentra em alguns dos recursos mais recentes da barra de ferramentas usados pelo Internet Explorer para aumentar a usabilidade do controle.

-   [Botões suspensos](#drop-down-buttons)
-   [Botões de estilo de lista](#list-style-buttons)
-   [Divisas](#handling-chevrons)
-   [Acompanhamento dinâmico](#hot-tracking)

### <a name="drop-down-buttons"></a>Botões suspensos

Os botões suspensos dão suporte a vários comandos. Quando o usuário clica em um botão suspenso, o botão exibe um menu pop-up em vez de iniciar um comando. O usuário inicia um comando selecionando-o no menu. A captura de tela a seguir mostra um botão suspenso e um menu na barra de ferramentas padrão do Internet Explorer.

![captura de tela mostrando o menu suspenso email](images/howto3.jpg)

A funcionalidade suspensa pode ser adicionada a qualquer estilo de botão, adicionando um sinalizador de estilo ao membro **fStyle** da estrutura [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) do botão. Há três estilos de botão suspenso, todos os quais são usados pelo Internet Explorer:

-   Os botões suspensos simples têm o [**estilo \_ suspenso BTNS**](toolbar-control-and-button-styles.md) . Eles se parecem com botões normais, mas exibem um menu quando clicados em vez de iniciar um comando.
-   Botões de seta suspensa simples têm o estilo [**BTNS \_ WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) . Eles têm uma seta exibida ao lado da imagem ou do texto do botão. Além da diferença na aparência, eles são idênticos aos botões suspensos simples. O botão email usado como o exemplo na ilustração anterior é um botão de seta suspensa.
-   Os botões de seta suspensa que adicionam o estilo estendido [**TBSTYLE \_ ex \_ DRAWDDARROWS**](toolbar-extended-styles.md) ao [**\_ menu suspenso BTNS**](toolbar-control-and-button-styles.md) têm uma seta que é separada do texto ou da imagem. Esse estilo de botão combina a funcionalidade dos botões suspensos e padrão. Se o usuário clicar na seta, um menu será exibido e o usuário poderá escolher vários comandos. Se o usuário clicar no botão adjacente, ele iniciará um comando padrão. A captura de tela a seguir mostra o botão **voltar** do Internet Explorer, que usa uma seta separada.

    ![captura de tela que mostra o menu do botão voltar à divisão](images/howto4.jpg)

Quando o usuário clica em um botão suspenso com os estilos de seta simples ou Simple, o controle Toolbar envia ao aplicativo uma notificação [de \_ lista suspensa tbn](tbn-dropdown.md) . Quando seu aplicativo recebe essa mensagem, ele é responsável por criar e exibir o menu e para manipular o comando selecionado.

Quando o usuário clica em uma seta separada, o controle Toolbar envia ao aplicativo uma notificação de [ \_ lista suspensa tbn](tbn-dropdown.md) . Seu aplicativo deve tratá-lo da mesma forma que manipula os outros dois tipos de botões suspensos. Se o usuário clicar no botão principal, seu aplicativo receberá uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) com a ID de comando do botão, assim como se fosse um botão padrão. Normalmente, os aplicativos respondem iniciando o comando top no menu suspenso, mas você está livre para responder de qualquer maneira adequada.

### <a name="list-style-buttons"></a>Botões de List-Style

Com botões padrão, se você adicionar texto, ele será exibido abaixo do bitmap. A captura de tela a seguir mostra os botões de **pesquisa** e **favoritos** do Internet Explorer com texto de botão padrão.

![captura de tela mostrando a barra de ferramentas de pesquisa e favoritos com botões padrão](images/howto6.jpg)

O Microsoft Internet Explorer 5 e versões posteriores usam o estilo de [**\_ lista TBSTYLE**](toolbar-control-and-button-styles.md) . O texto está à direita do bitmap, reduzindo a altura do botão e aumentando a região de exibição. A ilustração a seguir mostra os botões de **pesquisa** e **favoritos** do Internet Explorer 6 com o estilo de **\_ lista TBSTYLE** .

![captura de tela mostrando a barra de ferramentas de pesquisa e favoritos usando botões de estilo de lista](images/howto5.jpg)

### <a name="chevrons"></a>Divisas

Quando o usuário reorganiza as bandas no controle rebar, parte de uma barra de ferramentas pode ser coberta. Se a banda tiver sido criada com o \_ estilo RBBS USECHEVRON, o controle rebar exibirá uma divisa na borda direita da barra de ferramentas. O usuário clica na divisa para exibir um menu com as ferramentas ocultas.

### <a name="hot-tracking"></a>Hot-Tracking

Quando o acompanhamento de quente está habilitado, um botão fica *quente* quando o cursor está sobre ele. O botão quente normalmente é diferenciado dos outros botões na barra de ferramentas por uma imagem distinta. Por padrão, um botão quente parece ser gerado acima do restante da barra de ferramentas. Quando um novo botão se tornar quente, seu aplicativo receberá uma notificação [tbn \_ HOTITEMCHANGE](tbn-hotitemchange.md) . A ilustração a seguir mostra os botões de **pesquisa** e **favoritos** do Internet Explorer 5, com um botão de **pesquisa** a quente. Além de ter uma aparência elevada, o bitmap cinza do botão foi substituído por um colorido.

![captura de tela mostrando os botões de pesquisa e favoritos, com um botão de pesquisa a quente](images/howto7.jpg)

Para habilitar o controle de acesso, crie um controle de barra de ferramentas com o estilo de [**\_ lista**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ simples**](toolbar-control-and-button-styles.md) ou TBSTYLE. Eles são chamados de barras de ferramentas *simples* porque os botões individuais não são realçados de nenhuma forma. Os bitmaps são simplesmente exibidos ao lado um do outro. Eles assumem uma aparência semelhante a um botão somente quando estão quentes. Esses dois estilos também são Transparent, o que significa que o plano de fundo dos ícones será a cor da janela do cliente subjacente.

Para que um bitmap diferente seja exibido quando o botão estiver quente, crie uma segunda [lista de imagens](image-lists.md) que contenha imagens ativas para todos os botões na barra de ferramentas. O tamanho e a ordem dessas imagens devem ser os mesmos da lista de imagens padrão. Envie a barra de ferramentas para controlar uma mensagem [**\_ SETHOTIMAGELIST TB**](tb-sethotimagelist.md) para definir a lista de imagens ativas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Como criar uma barra de menus do Internet Explorer-Style](cc-faq-iemenubar.md)
</dt> </dl>

 

 