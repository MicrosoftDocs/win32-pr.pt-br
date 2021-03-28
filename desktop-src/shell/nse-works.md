---
description: O Windows Explorer fornece uma representação gráfica do namespace do Shell combinada com ferramentas que permitem aos usuários interagir com objetos do Shell.
ms.assetid: cc387338-15fa-4350-b039-61a0f1c5030a
title: Noções básicas sobre extensões de namespace do Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0150092a25708c1f079160a9d106a7b8205e231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968006"
---
# <a name="understanding-shell-namespace-extensions"></a>Noções básicas sobre extensões de namespace do Shell

O Windows Explorer fornece uma representação gráfica do namespace do Shell combinada com ferramentas que permitem aos usuários interagir com objetos do Shell. Com uma extensão de namespace, você pode obter qualquer corpo de dados e fazer com que o Windows Explorer o apresente ao usuário como uma pasta virtual. Quando um usuário navega nessa pasta, seus dados são apresentados como uma hierarquia estruturada em árvore de pastas e arquivos, assim como o restante do namespace do Shell. Os usuários e aplicativos podem interagir com o conteúdo dessa pasta virtual da mesma maneira que com qualquer outro objeto de namespace. Este documento discute como criar uma extensão de namespace.

-   [Como funciona uma extensão de namespace](#how-a-namespace-extension-works)
-   [O objeto de exibição de pasta do sistema padrão (DefView)](#the-default-system-folder-view-object-defview)
-   [Como o Windows Explorer interage com uma extensão de namespace](#how-windows-explorer-interacts-with-a-namespace-extension)
    -   [Exibição de árvore](#tree-view)
    -   [Exibição de pasta](#folder-view)
    -   [Barra de menus e barras de ferramentas](#menu-bar-and-toolbars)
    -   [Barra de Status](#status-bar)

## <a name="how-a-namespace-extension-works"></a>Como funciona uma extensão de namespace

Nos bastidores, todas as pastas que o Windows Explorer exibe são representadas por um objeto de Component Object Model (COM) chamado de *objeto de pasta*. Cada vez que o usuário interage com uma pasta ou seu conteúdo, o Shell se comunica com o objeto de pasta associado por meio de uma de várias interfaces padrão. Em seguida, o objeto Folder faz o que for necessário para responder à ação do usuário e o Shell atualiza a exibição do Windows Explorer.

A maioria dos arquivos e pastas com os quais os usuários interagem fazem parte do sistema de arquivos ou de uma pasta virtual do sistema, como a lixeira. Outra documentação abordou como você pode personalizar o comportamento dessas pastas padrão para atender aos requisitos do seu aplicativo modificando o registro ou implementando [manipuladores de extensão de shell](handlers.md). No entanto, estender o Shell dessas maneiras é mais útil quando suas informações podem ser prontamente empacotadas na forma de arquivos ou pastas normais do sistema de arquivos.

Há várias situações em que o armazenamento de dados como uma coleção de arquivos e pastas do sistema de arquivos pode ser indesejável ou até mesmo impossível. Alguns exemplos desse tipo de dados incluem:

-   Uma coleção de itens que é empacotada mais efetivamente em um único arquivo, como um banco de dados.
-   Uma coleção de itens armazenados em um computador remoto que não tem um sistema de arquivos padrão do Windows. Um exemplo desses dados são as informações armazenadas em um PDA (assistente digital pessoal) ou em uma câmera digital.
-   Uma coleção de itens que não representa dados armazenados. Um exemplo desses dados são os links de impressora contidos na pasta impressoras padrão.

Uma maneira de apresentar esse tipo de dados a um usuário é escrever um aplicativo para permitir que os usuários exibam e interajam com os vários itens. No entanto, se os dados puderem ser apresentados como uma hierarquia de pastas/arquivos, grande parte da funcionalidade que você precisará implementar poderá ser os serviços de interface do usuário que já são fornecidos pelo Windows Explorer. Uma abordagem muito mais eficiente poderia ser escrever uma extensão de namespace e deixar o Windows Explorer se tornar sua GUI.

Para implementar uma extensão de namespace, suas informações devem ser organizadas como um namespace estruturado em árvore. A *raiz do namespace* é apresentada como uma pasta virtual no namespace do Shell. A pasta raiz e todas as suas subpastas e itens de dados, tornam-se parte do namespace do Shell e o Windows Explorer se torna sua interface do usuário. Portanto, você pode apresentar suas informações para o usuário de uma maneira familiar e prontamente acessível com muito menos programação de interface do usuário do que seria necessário para um aplicativo personalizado.

Uma extensão de namespace consiste em dois componentes básicos:

-   Um Gerenciador de dados
-   Uma interface entre o Gerenciador de dados e o Windows Explorer

O primeiro componente da lista depende inteiramente de você. Você pode armazenar e gerenciar seus dados de qualquer maneira que seja mais eficiente. O segundo componente é o código necessário para empacotar seus dados como objetos de pasta e lidar com a interação com o Windows Explorer. O Windows Explorer pode então chamar esses objetos para permitir que os usuários exibam e interajam com seus dados como se fossem uma coleção de pastas e arquivos. Os objetos de pasta da extensão do namespace devem interagir com o Windows Explorer como se fossem pastas normais. Antes de tentar implementar uma extensão de namespace, você deve primeiro entender como o Windows Explorer lida com um objeto de pasta.

## <a name="the-default-system-folder-view-object-defview"></a>O objeto de exibição de pasta do sistema padrão (DefView)

O Shell fornece uma implementação padrão da exibição de pasta, coloquialmente conhecida como DefView, para que você possa evitar grande parte do trabalho de implementar sua própria extensão de namespace. Como alguns recursos de exibição não podem ser obtidos por meio de exibições personalizadas, geralmente é recomendável que o objeto de exibição de pasta do sistema padrão seja usado no lugar de uma exibição personalizada. Para obter mais informações, consulte [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview).

## <a name="how-windows-explorer-interacts-with-a-namespace-extension"></a>Como o Windows Explorer interage com uma extensão de namespace

O Windows Explorer fornece aos usuários uma GUI que permite que eles realizem uma variedade de tarefas, incluindo:

-   [Navegar](navigate.md) na hierarquia de namespace e exibir o conteúdo das pastas.
-   [Gerenciando](manage.md) o conteúdo do namespace movendo, excluindo e copiando objetos.
-   [Recuperando](folder-info.md) uma variedade de informações sobre objetos.
-   [Iniciando](launch.md) aplicativos.

A GUI do Windows Explorer tem cinco componentes básicos. A ilustração a seguir nomeia os componentes e mostra onde eles são normalmente exibidos no Windows Explorer.

![ilustração mostrando componentes da interface do usuário do Windows Explorer ](images/nse1.png)

Quando um usuário exibe uma pasta que pertence a uma extensão de namespace no Windows Explorer, o objeto de pasta tem pelo menos controle parcial sobre o conteúdo de todas as cinco áreas.

### <a name="tree-view"></a>Modo de exibição de árvore

O modo de exibição de árvore fornece uma exibição de alto nível do namespace. Essa área hospeda um [controle de exibição de árvore](../controls/tree-view-controls.md) que pode exibir cada pasta de namespace e a posição da pasta na hierarquia de namespace. Um usuário pode executar várias operações com a área de exibição de árvore, incluindo:

-   Exibindo ou ocultando o próximo nível no namespace.
-   Copiar, mover ou excluir pastas.
-   Clicando com o botão direito do mouse em uma pasta para exibir um menu de atalho.
-   Selecionar uma pasta e exibir seu conteúdo na exibição de pasta.

O modo de exibição de árvore se comunica com objetos de pasta principalmente por meio de sua interface [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Por exemplo, quando um usuário clica no sinal de mais (+) ao lado do ícone da pasta, o Windows Explorer expande a exibição para mostrar as subpastas da pasta. Para obter as informações necessárias para atualizar o modo de exibição de árvore, o Shell faz várias chamadas para a interface **IShellFolder** do objeto de pasta para:

-   Solicite os atributos da pasta.
-   Enumere o conteúdo da pasta.
-   Solicitar nomes de exibição para cada subpasta.
-   Solicite um ícone para exibir ao lado de cada pasta.

Em seguida, o Windows Explorer atualiza o modo de exibição de árvore para mostrar as subpastas da pasta selecionada. Se as subpastas tiverem subpastas, um caractere ' + ' será exibido ao lado do ícone de pasta. Há uma série de tarefas mais sofisticadas que um usuário também pode executar com o modo de exibição de árvore, incluindo:

-   Usando a área de transferência para recortar ou copiar uma pasta e colá-la em outra pasta.
-   Usando o recurso de arrastar e soltar para recortar ou copiar uma pasta e soltá-la em outra pasta.
-   Usando um mecanismo de pesquisa para pesquisar itens em uma pasta ou em suas subpastas.
-   Modificando as propriedades da pasta.

Para obter uma discussão mais detalhada sobre como uma extensão de namespace manipula essas ações de usuário, consulte [implementando as interfaces de objeto de pasta básica](nse-implement.md).

### <a name="folder-view"></a>Exibição de pasta

Quando um usuário seleciona uma pasta, o conteúdo da pasta é exibido no modo de exibição de pasta. Até certo ponto, a funcionalidade normal da exibição de pasta se sobrepõe à exibição de árvore. Os usuários podem mover ou copiar pastas, alterar as propriedades da pasta, exibir o conteúdo de uma subpasta, exibir um menu de atalho para uma pasta e assim por diante. No entanto, há algumas diferenças distintas entre a exibição de árvore e a exibição de pasta:

-   A exibição de pasta exibe somente o conteúdo de uma única pasta, não parte ou toda a hierarquia de namespace.
-   A exibição de pasta exibe objetos de arquivo, bem como objetos de pasta.
-   A exibição de pasta pode exibir muito mais informações sobre objetos do que o modo de exibição de árvore.
-   A exibição de pasta permite que extensões de namespace tenham controle quase total sobre quais informações são exibidas e como. Somente os aspectos secundários do modo de exibição de árvore, como ícones de pasta, podem ser modificados.

Ao contrário do modo de exibição de árvore, o Windows Explorer não controla diretamente o conteúdo da exibição de pasta. A exibição de pasta é uma área que o Windows Explorer fornece a objetos de pasta. Exibir e gerenciar o conteúdo de uma pasta na exibição de pasta é responsabilidade do objeto de pasta. Embora a maioria das exibições de pasta siga um formato bastante padrão, há poucas limitações no que pode ser exibido ou como. Um caso extremo é a pasta da Internet, que é um navegador completo.

Quando um usuário seleciona uma pasta que pertence à sua extensão de namespace, você cria uma janela e passa sua alça para o Windows Explorer. Essa janela torna-se um filho da janela de exibição de pasta. O Windows Explorer fornece as dimensões da janela de exibição de pasta, mas não coloca nenhuma restrição no conteúdo da janela filho. Você pode usar a janela filho para exibir a exibição de pasta da pasta.

As extensões de namespace usam uma das duas abordagens para criar uma exibição de pasta:

-   Use sua janela filho para hospedar um controle de [exibição de lista](../controls/list-view-control-reference.md) . Esse controle permite que você exiba o conteúdo de uma pasta praticamente da mesma forma que a [exibição clássica](../lwef/web-view.md)do Windows Explorer.
-   Use sua janela filho para hospedar um [controle WebBrowser](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752044(v=vs.85)) e use um documento HTML dinâmico (DHTML) para exibir o conteúdo da pasta.

Ambas as abordagens exibem uma exibição de pasta que parece muito parecida com a exibida para pastas do sistema. No entanto, se você quiser usar um esquema de exibição diferente, será gratuito fazê-lo.

### <a name="menu-bar-and-toolbars"></a>Barra de menus e barras de ferramentas

Como a maioria dos aplicativos do Windows, o Windows Explorer fornece ao usuário uma coleção de ferramentas. Uma seleção completa de ferramentas está disponível na barra de menus. As ferramentas mais comumente usadas também são representadas por botões ou caixas de edição em uma barra de ferramentas. Ao contrário de muitos aplicativos do Windows, a barra de menus do Windows Explorer é, na verdade, um [controle Toolbar](../controls/toolbar-control-reference.md) que foi personalizado para se comportar como um menu convencional. A barra de menus e a barra de ferramentas são incorporadas a um [controle rebar](../controls/rebar-control-reference.md) para permitir que os usuários organizem os controles individuais de acordo com suas necessidades.

Por padrão, o Windows Explorer dá suporte a um conjunto padrão de botões e itens de menu, como copiar e propriedades. A extensão do namespace pode personalizar a barra de menus e as barras de ferramentas excluindo ferramentas padrão e adicionando ferramentas personalizadas. Quando o objeto de exibição de pasta é inicializado, o Windows Explorer passa um ponteiro para sua interface [**IShellBrowser**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) . Essa interface dá suporte a vários métodos que você pode chamar para personalizar a barra de menus e a barra de ferramentas. Quando o usuário seleciona um dos seus itens de menu personalizados ou botões da barra de ferramentas, o Windows Explorer encaminha \_ as mensagens de comando do WM para o menu personalizado e itens da barra de ferramentas para o procedimento de janela da janela filho.

### <a name="status-bar"></a>Barra de Status

A barra de status do Windows Explorer exibe informações sobre o objeto atualmente selecionado. Sua extensão de namespace pode usar a barra de status para exibir informações de status, como uma cadeia de texto. Você pode personalizar a barra de status chamando [**IShellBrowser**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellbrowser).

 

 
