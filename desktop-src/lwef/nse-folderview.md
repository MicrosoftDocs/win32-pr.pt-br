---
title: Implementação de uma Exibição de pasta
description: O Shell do Windows fornece uma implementação padrão da exibição de pasta, coloquialmente conhecida como DefView, para que você possa evitar grande parte do trabalho de implementar sua própria extensão de namespace.
ms.assetid: 8c6712d8-c3cb-4450-8277-3a8675622651
keywords:
- objeto de exibição de pasta
- IShellView
- IShellBrowser, objetos de exibição de pasta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c7b86d587154a034f276d4bdab903e5337ed4b
ms.sourcegitcommit: 469b6de41e2a565b7ead231d7f282ec4071ac158
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/11/2020
ms.locfileid: "104366858"
---
# <a name="implementing-a-folder-view"></a>Implementação de uma Exibição de pasta

O Shell do Windows fornece uma implementação padrão da exibição de pasta, coloquialmente conhecida como DefView, para que você possa evitar grande parte do trabalho de implementar sua própria extensão de namespace. Como alguns recursos de exibição não podem ser obtidos por meio de exibições personalizadas, geralmente é recomendável que o objeto de exibição de pasta do sistema padrão seja usado no lugar de uma exibição personalizada. Para obter mais informações, consulte [**SHCreateShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderview). O restante deste tópico aborda a implementação de uma exibição de pasta personalizada que não dá suporte a recursos de exibição mais recentes.

Ao contrário do modo de exibição de árvore, o Windows Explorer não gerencia o conteúdo de uma exibição de pasta. Em vez disso, a janela de exibição de pasta hospeda uma janela filho que é fornecida pelo objeto Folder. O objeto Folder é responsável por criar um objeto de exibição de pasta para exibir o conteúdo da pasta na janela filho.

A chave para implementar um objeto de exibição de pasta é a interface [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) . Essa interface é usada pelo Windows Explorer para se comunicar com o objeto de exibição de pasta. Antes de exibir uma exibição de pasta, o Windows Explorer chama o método [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) do objeto de pasta com *RIID* definido como IID \_ IShellView. Crie um objeto de exibição de pasta e retorne sua interface **IShellView** . O objeto de exibição de pasta deve criar uma janela filho da janela de exibição de pasta e usar a janela filho para exibir informações sobre o conteúdo da pasta.

Além de controlar como os dados são exibidos, as extensões também podem personalizar vários recursos do Windows Explorer. Por exemplo, uma extensão pode adicionar itens à barra de ferramentas ou à barra de menus ou exibir informações na barra de status.

-   [O objeto de exibição de pasta](#the-folder-view-object)
-   [Inicializando o objeto de exibição de pasta](#initializing-the-folder-view-object)
-   [Exibindo a exibição de pasta](#displaying-the-folder-view)
-   [Implementando IShellView](#implementing-ishellview)
    -   [AddPropertySheetPages](#addpropertysheetpages)
    -   [GetCurrentInfo](#getcurrentinfo)
    -   [Atualizar](#refresh)
    -   [SaveViewState](#saveviewstate)
    -   [TranslateAcelerator](#translateacelerator)
-   [Usando o IShellBrowser para se comunicar com o Windows Explorer](#using-ishellbrowser-to-communicate-with-windows-explorer)
    -   [Modificando a barra de menus do Windows Explorer](#modifying-the-windows-explorer-menu-bar)
    -   [Modificando a barra de ferramentas do Windows Explorer](#modifying-the-windows-explorer-toolbar)
    -   [Modificando a barra de status do Windows Explorer](#modifying-the-windows-explorer-status-bar)
    -   [Armazenando informações específicas da exibição](#storing-view-specific-information)

## <a name="the-folder-view-object"></a>O objeto de exibição de pasta

Um objeto de exibição de pasta é um objeto de Component Object Model (COM) que expõe uma interface [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) . Este objeto é responsável por:

-   Criar uma janela filho da janela de exibição de pasta e usá-la para exibir o conteúdo da pasta.
-   Lidando com a comunicação com o Windows Explorer.
-   Adicionar comandos específicos da pasta à barra de menus do Windows Explorer e à barra de ferramentas e manipular esses comandos quando eles são selecionados.
-   Gerenciar a interação do usuário com a janela de exibição de pasta, como exibir menus de atalho ou manipular operações de arrastar e soltar.

Este documento aborda os três primeiros tópicos. Como a interação do usuário com o modo de exibição de pasta ocorre dentro de sua janela filho, o objeto de exibição de pasta é responsável por tratá-lo como faria em qualquer outra janela.

O Windows Explorer solicita um objeto de exibição de pasta chamando o objeto de pasta [**IShellFolder:: CreateViewObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-createviewobject) com *RIID* definido como IID \_ IShellView. O procedimento para criar uma exibição de pasta é:

1.  O objeto de pasta cria uma nova instância do objeto de exibição de pasta e retorna um ponteiro para sua interface [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) .
2.  O Windows Explorer Inicializa o objeto de exibição de pasta chamando o método [**IShellView:: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) . Crie uma janela filho da janela de exibição de pasta e retorne seu identificador para o Windows Explorer.
3.  O objeto de exibição de pasta usa a interface [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) do Windows Explorer para personalizar a barra de ferramentas, a barra de menus e a barra de status do Windows Explorer.
4.  O objeto de exibição de pasta exibe o conteúdo da pasta na janela filho.
5.  O objeto de exibição de pasta manipula a interação do usuário com o modo de exibição de pasta e qualquer barra de ferramentas ou itens de barra de menus específicos da pasta.

## <a name="initializing-the-folder-view-object"></a>Inicializando o objeto de exibição de pasta

O Windows Explorer Inicializa o objeto de exibição de pasta chamando o método [**IShellView:: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) . Os parâmetros do método fornecem o objeto de exibição de pasta com as informações necessárias para criar a janela filho que será usada para exibir o conteúdo da pasta:

-   Um ponteiro para a interface de [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) do objeto de exibição de pasta anterior. Esse parâmetro pode ser definido como **nulo**.
-   Uma estrutura [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) que contém as configurações da exibição da pasta anterior.
-   Um ponteiro para a interface [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) do Windows Explorer.
-   Uma estrutura [Rect](/previous-versions//ms536136(v=vs.85)) com as dimensões da janela de exibição de pasta.

O método [**IShellView:: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) é chamado antes de o objeto de exibição de pasta anterior ser destruído. Assim, o ponteiro de interface [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) permite que você se comunique com o objeto de exibição de pasta anterior. Essa interface é útil principalmente se a pasta anterior pertencia à sua extensão e usou o mesmo esquema de exibição. Nesse caso, você pode se comunicar com o objeto de exibição de pasta anterior para tais finalidades como a troca de configurações privadas.

Uma maneira simples de determinar se o ponteiro [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) pertence à sua extensão é fazer com que todos os objetos de exibição de pasta exponham uma interface privada. Chame [IShellView:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para solicitar a interface privada e examine o valor de retorno para determinar se o objeto de exibição de pasta é um dos seus. Você pode usar um método particular nessa interface para trocar informações.

A estrutura [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) contém as configurações de exibição da exibição de pasta anterior. A configuração principal é o modo de exibição: ícone grande, ícone pequeno, lista ou detalhes. Há também um sinalizador que contém as configurações de uma variedade de opções de exibição, como se a exibição deve ser alinhada à esquerda. A exibição da pasta deve seguir essas configurações na extensão possível, para fornecer aos usuários uma experiência consistente, uma vez que eles vão de uma pasta para outra. Você deve armazenar essa estrutura e atualizá-la conforme a alteração das configurações. O Windows Explorer chama [**IShellView:: GetCurrentInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo) para obter o valor mais recente dessa estrutura antes de abrir a próxima exibição de pasta.

A interface [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) é exposta pelo Windows Explorer. Essa interface é um complemento do [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) e permite que um objeto de exibição de pasta se comunique com o Windows Explorer. Não há nenhuma outra maneira de recuperar esse ponteiro de interface, portanto, o objeto de exibição de pasta deve armazená-lo para uso posterior. Em particular, você precisará chamar [IShellBrowser:: GetWindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) para recuperar a janela de exibição da pasta pai que será usada para criar sua janela filho. Observe que o método IShellBrowser:: GetWindow não está incluído na documentação do **IShellBrowser** porque ele é herdado de [IOleWindow](/windows/win32/api/oleidl/nn-oleidl-iolewindow). Depois de armazenar o ponteiro de interface, lembre-se de chamar [IShellBrowser:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) para incrementar a contagem de referência da interface. Quando você não precisar mais da interface, chame [IShellBrowser:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

Para criar sua janela filho:

1.  Examine as estruturas [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) e [Rect](/previous-versions//ms536136(v=vs.85)) .
2.  Se necessário, obtenha as configurações particulares do objeto de exibição de pasta anterior.
3.  Chame [IShellBrowser:: GetWindow](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) para recuperar a janela de exibição da pasta pai.
4.  Crie um filho da janela de exibição de pasta obtida na etapa anterior e retorne-o para o Windows Explorer.

## <a name="displaying-the-folder-view"></a>Exibindo a exibição de pasta

Depois de criar a janela filho e retorne-a para o Windows Explorer, você poderá exibir o conteúdo da pasta. Normalmente, as extensões exibem suas informações fazendo com que a janela filho hospede um [controle de exibição de lista](../controls/list-view-control-reference.md) ou um **controle WebBrowser**. O controle de exibição de lista permite replicar a [exibição clássica](web-view.md)do Windows Explorer. O controle WebBrowser permite que você use um documento HTML dinâmico (DHTML) para exibir suas informações, assim como a exibição da Web do Windows Explorer. Para obter mais informações, consulte a documentação desses controles.

A janela de exibição de pasta sempre existe, mesmo que ela não tenha foco. Portanto, você deve manter três Estados para sua janela filho:

-   Ativado com foco. O modo de exibição de pasta foi criado e tem foco. Defina a barra de menus ou os itens da barra de ferramentas que são apropriados para um estado focalizado.
-   Ativado sem foco. A exibição de pasta foi criada e está ativa, mas não tem foco. Defina a barra de menus ou os itens da barra de ferramentas que são apropriados para um estado não focalizado. Omita todos os itens que se aplicam à seleção de itens no modo de exibição de pasta.
-   Desativado. A exibição de pasta está prestes a ser destruída. Remova todos os itens de menu específicos da pasta.

O Windows Explorer notifica seu objeto de exibição de pasta quando o estado da janela é alterado chamando [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate). Por sua vez, o objeto de exibição de pasta deve notificar o Windows Explorer quando um usuário ativar a janela de exibição de pasta chamando [**IShellBrowser:: OnViewWindowActive**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-onviewwindowactive). Para obter mais informações sobre essa interface, consulte [usando o IShellBrowser para se comunicar com o Windows Explorer](#using-ishellbrowser-to-communicate-with-windows-explorer).

Embora a exibição de pasta esteja ativa, você precisa processar todas as mensagens do Windows, como o [ \_ tamanho do WM](../winmsg/wm-size.md), que pertencem à sua janela filho. O procedimento de janela também receberá mensagens de [ \_ comando do WM](../menurc/wm-command.md) para todos os itens que você adicionou à barra de menus ou barra de ferramentas do Windows Explorer.

Depois de criar a exibição de pasta, o Windows Explorer chama a interface [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) do objeto de exibição de pasta para passar uma variedade de informações. O objeto deve modificar sua exibição de acordo. Quando a exibição de pasta está prestes a ser destruída, o Windows Explorer notifica o objeto de exibição de pasta chamando seu método [**IShellView::D estroyviewwindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-destroyviewwindow) .

## <a name="implementing-ishellview"></a>Implementando IShellView

Depois que o objeto Folder tiver sido criado, o Windows Explorer chamará vários métodos [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) para solicitar informações ou notificar o objeto de uma alteração no estado do Windows Explorer. Esta seção descreve como implementar esses métodos **IShellView** . Os métodos restantes são usados para fins mais especializados, como a caixa de diálogo abrir arquivo comum. Para obter detalhes, consulte a documentação do **IShellView** .

### <a name="addpropertysheetpages"></a>AddPropertySheetPages

Quando um usuário seleciona **Opções de pasta** no menu **ferramentas** do Windows Explorer, é exibida uma folha de propriedades que permite ao usuário modificar as opções de pasta. O Windows Explorer chama o método [**IShellView:: AddPropertySheetPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages) do objeto de exibição de pasta para permitir que você adicione uma página a essa folha de propriedades.

O Windows Explorer passa um ponteiro para uma função de retorno de chamada [AddPropSheetPageProc](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) no parâmetro *lpfn* de [**IShellView:: AddPropertySheetPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-addpropertysheetpages). Chame [CreatePropertySheetPage](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) para criar a página e, em seguida, chame o AddPropSheetPageProc para adicioná-lo à folha de propriedades. Para obter mais informações sobre como lidar com folhas de propriedades, consulte [folhas de propriedades](../controls/property-sheets.md).

### <a name="getcurrentinfo"></a>GetCurrentInfo

Quando o usuário alterna de uma pasta para outra, o Windows Explorer tenta manter uma exibição de pasta semelhante. Por exemplo, se a exibição de pasta anterior mostrar ícones grandes, o próximo também deverá ser. Quando o Windows Explorer chama [**IShellView:: CreateViewWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-createviewwindow) para inicializar o objeto de exibição de pasta, o método recebe uma estrutura [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) . Essa estrutura contém informações que permitem que você torne o modo de exibição de pasta consistente com o modo de exibição de pasta anterior.

Para ajudar a garantir que a próxima exibição seja consistente com a exibição atual, armazene a estrutura [**FOLDERSETTINGS**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-foldersettings) . Se a exibição for alterada, por exemplo, de ícones grandes para pequenos, atualize a estrutura de acordo. Antes de alternar as exibições, o Windows Explorer chamará [**IShellView:: GetCurrentInfo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-getcurrentinfo) para solicitar os valores de **FOLDERSETTINGS** atuais para passá-los para o próximo objeto de exibição de pasta.

### <a name="refresh"></a>Atualizar

O usuário pode garantir que a exibição de pasta reflita o estado atual da pasta selecionando **Atualizar** no menu **Exibir** ou pressionando a tecla F5. Quando o usuário faz isso, o Windows Explorer chama o método [**IShellView:: Refresh**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-refresh) . O objeto de exibição de pasta deve atualizar imediatamente a exibição de exibição de pasta.

### <a name="saveviewstate"></a>SaveViewState

O Windows Explorer chama o método [**IShellView:: SaveViewState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate) para solicitar que o objeto de exibição de pasta salve seu estado de exibição. Em seguida, você pode recuperar o estado na próxima vez que a pasta for exibida. A maneira preferida de salvar um estado de exibição é chamando o método [**IShellBrowser:: GetViewStateStream**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream) . Esse método retorna uma interface [IStream](/windows/win32/api/objidl/nn-objidl-istream) que o objeto de exibição de pasta pode usar para salvar seu estado. Ao criar outra exibição de pasta, você pode chamar o mesmo método **IShellBrowser:: GetViewStateStream** para obter um ponteiro de IStream que permite que você leia as configurações salvas pelas exibições de pasta anteriores.

### <a name="translateacelerator"></a>TranslateAcelerator

Quando o usuário pressiona uma tecla de atalho, o Windows Explorer passa a mensagem para o objeto de exibição de pasta chamando [**IShellView:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator). Retorne \_ os S false para que o Windows Explorer processe a mensagem. Se o objeto de exibição de pasta tiver processado a mensagem, retorne S \_ OK.

Quando a janela de exibição de pasta tem foco, o Windows Explorer chama [**IShellView:: TranslateAccelerator**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-translateaccelerator) antes de processar a mensagem. Como a maioria das mensagens é normalmente associada à barra de menus ou aos comandos da barra de ferramentas do Windows Explorer, o objeto de exibição de pasta normalmente retorna S \_ false. O Windows Explorer pode processar a mensagem normalmente. Retorne \_ os S Ok somente se a mensagem for específica da pasta e você não quiser que o Windows Explorer faça nenhum processamento adicional. Se a exibição de pasta não tiver foco, o Windows Explorer processará a mensagem primeiro. Ele chama [**IShellBrowser:: TranslateAcceleratorSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-translateacceleratorsb) somente se não tratar a mensagem.

## <a name="using-ishellbrowser-to-communicate-with-windows-explorer"></a>Usando o IShellBrowser para se comunicar com o Windows Explorer

A interface [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser) é usada pelo objeto de exibição de pasta para se comunicar com o Windows Explorer para uma variedade de finalidades, incluindo:

-   [Modificando a barra de menus do Windows Explorer](#modifying-the-windows-explorer-menu-bar)
-   [Modificando a barra de ferramentas do Windows Explorer](#modifying-the-windows-explorer-toolbar)
-   [Modificando a barra de status do Windows Explorer](#modifying-the-windows-explorer-status-bar)
-   [Armazenando informações específicas da exibição](#storing-view-specific-information)

### <a name="modifying-the-windows-explorer-menu-bar"></a>Modificando a barra de menus do Windows Explorer

A barra de menus do Windows Explorer permite que o usuário inicie uma variedade de comandos. Por padrão, a barra de menus só dá suporte a comandos que são específicos do Windows Explorer. As mensagens [de \_ comando do WM](../menurc/wm-command.md) relacionadas são processadas pelo Windows Explorer e não são passadas para o objeto de exibição de pasta. No entanto, você pode modificar a barra de menus para incluir um ou mais itens de menu específicos da pasta com [**IShellBrowser**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser). O Windows Explorer passa as \_ mensagens de comando do WM associadas a esses itens para o procedimento de janela do seu objeto de pasta para processamento. Você também pode remover ou desabilitar os comandos padrão que não se aplicam ao seu aplicativo.

Os objetos de exibição de pasta normalmente modificam a barra de menus antes de a exibição de pasta ser exibida pela primeira vez. Eles devem retornar a barra de menus para seu estado original quando a exibição de pasta for destruída. Talvez você também precise modificar a barra de menus sempre que a exibição da pasta obtiver ou perder o foco.

Como o Windows Explorer chama [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) sempre que o estado da janela de exibição de pasta é alterado, a modificação da barra de menus normalmente é incluída na implementação desse método. O procedimento básico para modificar a barra de menus do Windows Explorer é:

1.  Chame [CreateMenu](/windows/win32/api/winuser/nf-winuser-createmenu) para criar um identificador de menu.
2.  Passe esse identificador de menu para o Windows Explorer chamando [**IShellBrowser:: InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb). O Windows Explorer preencherá suas informações de menu.
3.  Modifique o menu conforme necessário.
4.  Chame [**IShellBrowser:: SetMenuSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) para que o Windows Explorer exiba a barra de menus modificada.

O Windows Explorer tem seis menus pop-up na barra de menus. Assim como acontece com todos os contêineres OLE, o menu do Windows Explorer é dividido em seis grupos: arquivo, editar, contêiner, objeto, janela e ajuda. A tabela a seguir lista os menus pop-up do Windows Explorer e seu grupo associado, juntamente com as IDs de menu.



| Menu pop-up | ID                     | Grupo     |
|-------------|------------------------|-----------|
| Arquivo        | \_arquivo de menu FCIDM \_      | Arquivo      |
| Editar        | \_edição do menu FCIDM \_      | Arquivo      |
| Visualizar        | \_exibição do menu FCIDM \_      | Contêiner |
| Favoritos   | \_favoritos do menu FCIDM \_ | Contêiner |
| Ferramentas       | \_Ferramentas do menu FCIDM \_     | Contêiner |
| Ajuda        | \_ajuda do menu FCIDM \_      | Janela    |



 

Ao passar o identificador de menu para o Windows Explorer chamando [**IShellBrowser:: InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb), você também deve passar um ponteiro para uma estrutura [OLEMENUGROUPWIDTHS](/windows/win32/api/oleidl/ns-oleidl-olemenugroupwidths) cujos membros foram inicializados como zero.

Quando [**IShellBrowser:: InsertMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) retornar, o Windows Explorer terá adicionado seus itens de menu. Você pode usar o identificador de menu retornado com funções de menu padrão do Windows, como [InsertMenuItem](/windows/win32/api/winuser/nf-winuser-insertmenuitema) para:

-   Adicione itens aos menus pop-up do Windows Explorer.
-   Modifique ou exclua itens existentes nos menus pop-up do Windows Explorer.
-   Adicione novos menus pop-up.

Use as IDs listadas na tabela para identificar os vários menus pop-up do Windows Explorer.

> [!Note]  
> Para evitar conflitos com IDs de comando do Windows Explorer, as IDs de qualquer item de menu que você adicionar devem estar entre FCIDM \_ SHVIEWFIRST e FCIDM \_ SHVIEWLAST. Esses dois valores são definidos em shlobj. h.

 

Depois de terminar de modificar o menu, chame [**IShellBrowser:: SetMenuSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) para que o Windows Explorer exiba a nova barra de menus.

Depois que a exibição de pasta é exibida inicialmente, o Windows Explorer chama [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) sempre que a exibição da pasta Obtém ou perde o foco. Se você tiver itens de menu sensíveis ao estado do modo de exibição de pasta, modifique o menu adequadamente, sempre que o estado for alterado. Por exemplo, você pode ter um item de menu que atue em um item no modo de exibição de pasta que foi selecionado pelo usuário. Você deve desabilitar ou remover esse item de menu quando a exibição de pasta perder o foco.

Quando o Windows Explorer chama [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) para indicar que a exibição de pasta está sendo desativada, restaure a barra de menus para seu estado original chamando [**IShellBrowser:: RemoveMenusSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-removemenussb).

### <a name="modifying-the-windows-explorer-toolbar"></a>Modificando a barra de ferramentas do Windows Explorer

Além de modificar a barra de menus do Windows Explorer, você também pode adicionar botões à barra de ferramentas. Assim como acontece com a barra de menus, a modificação da barra de ferramentas geralmente faz parte da implementação [**IShellView:: UIActivate**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-uiactivate) . O procedimento para adicionar botões à barra de ferramentas do Windows Explorer é:

1.  Adicione o bitmap do botão à lista de imagens da barra de ferramentas.
2.  Defina a cadeia de texto do botão.
3.  Adicione o botão à barra de ferramentas.

Para adicionar um bitmap à lista de imagens de uma barra de ferramentas, envie a barra de ferramentas uma mensagem de [TB \_ AddBitmap](../controls/tb-addbitmap.md) chamando [**IShellBrowser:: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg). Para especificar o controle ToolBar, defina o parâmetro *ID* do método como **FCW \_ Toolbar**. Defina *wParam* como o número de imagens de botão no bitmap e *lParam* para o endereço de uma estrutura [TBADDBITMAP](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) . O índice de imagem é retornado no parâmetro *pret* .

Há duas maneiras de definir uma cadeia de caracteres para o botão:

-   Atribua a cadeia de caracteres ao membro **isastring** da estrutura [TBBUTTON](/windows/win32/api/commctrl/ns-commctrl-tbbutton) do botão.
-   Chame [**IShellBrowser:: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg) para enviar a barra de ferramentas para o controle de uma mensagem de [TB \_ AddString](../controls/tb-addstring.md) . O parâmetro *wParam* deve ser definido como zero e o parâmetro *lParam* para a cadeia de caracteres. O índice de cadeia de caracteres é retornado no parâmetro *pret* .

Para adicionar o botão à barra de ferramentas, preencha uma estrutura [TBBUTTON](/windows/win32/api/commctrl/ns-commctrl-tbbutton) e passe-a para [**IShellBrowser:: SetToolbarItems**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-settoolbaritems). Assim como no menu, a ID de comando deve estar entre FCIDM \_ SHVIEWFIRST e FCIDM \_ SHVIEWLAST. A barra de ferramentas acrescentará o botão à direita dos botões existentes.

Por exemplo, o fragmento de código a seguir adiciona um botão padrão à barra de ferramentas do Windows Explorer com uma ID de comando de MYBUTTON de IDB \_ .


```
TBADDBITMAP tbadbm;
int iButtonIndex;
TBBUTTON tbb;

tbadbm.hInst = g_hInstance;    // The module's instance handle
tbadbm.nID = IDB_BUTTONIMAGE;  // The bitmap's resource ID

psb->SendControlMsg(FCW_TOOLBAR, TB_ADDBITMAP, 1,
                    reinterpret_cast<LPARAM>(&tbadbm), &iButtonIndex);

psb->SendControlMsg(FCW_TOOLBAR, TB_ADDSTRING, NULL,
                    reinterpret_cast<LPARAM>(szLabel), &iStringIndex);

ZeroMemory(&tbb, sizeof(TBBUTTON));
tbb.iBitmap = iButtonIndex;
tbb.iCommand = IDB_MYBUTTON;
tbb.iString = iStringIndex;
tbb.fsState = TBSTATE_ENABLED;
tbb.fsStyle = TBSTYLE_BUTTON;

psb->SetToolbarItems(&tbb, 1, FCT_MERGE);
```



Para obter mais informações sobre como manipular controles da barra de ferramentas, consulte [controles da barra de ferramentas](../controls/toolbar-control-reference.md).

### <a name="modifying-the-windows-explorer-status-bar"></a>Modificando a barra de status do Windows Explorer

Você pode usar a barra de status do Windows Explorer para exibir uma variedade de informações úteis. Há duas maneiras de usar a barra de status:

-   Use [**IShellBrowser:: SetStatusTextSB**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setstatustextsb) para exibir uma cadeia de texto na barra de status.
-   Envie mensagens diretamente para o controle da barra de status com [**IShellBrowser:: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg).

O primeiro método é simples, mas suficiente para muitas finalidades. Para obter maior flexibilidade, você pode enviar mensagens diretamente para o controle da barra de status chamando [**IShellBrowser:: SendControlMsg**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg) com o parâmetro *ID* definido como **FCW \_ status**. Para obter mais informações sobre controles de barra de status, consulte [barras de status](../controls/status-bars.md).

### <a name="storing-view-specific-information"></a>Armazenando informações específicas da exibição

Quando uma exibição está prestes a ser destruída, geralmente é útil armazenar informações como o estado da exibição ou as configurações. O Windows Explorer solicita que você execute essa tarefa chamando [**IShellView:: SaveViewState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellview-saveviewstate). A maneira preferida de salvar informações específicas do modo de exibição é chamar [**IShellBrowser:: GetViewStateStream**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-getviewstatestream). Esse método fornece uma interface [IStream](/windows/win32/api/objidl/nn-objidl-istream) que você pode usar para armazenar as informações. Você está livre para usar qualquer formato de dados adequado.

 

 
