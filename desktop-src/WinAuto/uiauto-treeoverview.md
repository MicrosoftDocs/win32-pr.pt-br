---
title: Visão geral da árvore de automação de interface do usuário
description: Produtos de tecnologia assistencial e scripts de teste navegam pela árvore de automação da interface do usuário da Microsoft para reunir informações sobre a interface do usuário e seus elementos.
ms.assetid: f3afe258-baa7-41b5-a27e-cdc94b467d73
keywords:
- Automação da interface do usuário, visão geral da árvore
- Automação da interface do usuário, exibição da árvore
- Automação da interface do usuário, exibição bruta da árvore
- Automação da interface do usuário, exibição de controle da árvore
- Automação da interface do usuário, exibição de conteúdo da árvore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76bc9aa6568a3f4d63194d35ff0c7d8f59510c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822529"
---
# <a name="ui-automation-tree-overview"></a>Visão geral da árvore de automação de interface do usuário

Produtos de tecnologia assistencial e scripts de teste navegam pela árvore de automação da interface do usuário da Microsoft para reunir informações sobre a interface do usuário e seus elementos.

Na árvore de automação da interface do usuário, há um elemento raiz que representa a janela da área de trabalho do Windows ("a área de trabalho") e cujos elementos filho representam janelas de aplicativo. Cada um desses elementos filho pode conter elementos que representam partes da interface do usuário, como menus, botões, barras de ferramentas e caixas de listagem. Esses elementos podem conter elementos, como itens de lista.

A árvore de automação da interface do usuário não é uma estrutura fixa. Raramente é visto em sua totalidade porque pode conter milhares de elementos. Partes da árvore de automação da interface do usuário são criadas à medida que um cliente precisa delas, e a estrutura da árvore é alterada à medida que os elementos são adicionados, movidos ou removidos.

Provedores de automação de interface do usuário dão suporte à árvore de automação da interface do usuário implementando a navegação entre os itens em um fragmento Um fragmento é uma subárvore completa de elementos de uma estrutura específica e tem um elemento raiz (chamado de *raiz do fragmento*) que normalmente é hospedado em uma janela.

Os provedores não se preocupam com a navegação de um controle para outro. Isso é gerenciado pelo núcleo de automação da interface do usuário, que usa informações dos provedores de janela padrão.

Este tópico inclui as seções a seguir.

-   [Exibições da árvore de automação da interface do usuário](#views-of-the-ui-automation-tree)
    -   [Exibição bruta](#raw-view)
    -   [Exibição de controle](#control-view)
    -   [Exibição de conteúdo](#content-view)
-   [Tópicos relacionados](#related-topics)

## <a name="views-of-the-ui-automation-tree"></a>Exibições da árvore de automação da interface do usuário

A árvore de automação da interface do usuário pode ser filtrada para criar exibições que contêm somente os elementos de automação da interface do usuário que são relevantes para um cliente específico. Essa abordagem permite que os clientes personalizem a estrutura apresentada por meio da automação da interface do usuário para suas necessidades específicas.

O cliente pode personalizar a exibição por escopo e filtrando. O escopo está definindo a extensão da exibição, começando a partir de um elemento base. Por exemplo, o aplicativo pode querer localizar apenas filhos diretos da área de trabalho ou todos os descendentes de uma janela de aplicativo. A filtragem está definindo os tipos de elementos incluídos na exibição.

Os provedores de automação de interface do usuário dão suporte à filtragem definindo propriedades em elementos, incluindo as propriedades [**IUIAutomationElement:: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) e [**IUIAutomationElement:: IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) .

A automação da interface do usuário fornece três exibições padrão: modo de exibição bruto, exibição de controle e exibição de conteúdo. Essas exibições são definidas pelo tipo de filtragem executada. O escopo de qualquer exibição é definido pelo aplicativo. O aplicativo pode aplicar outros filtros nas propriedades; por exemplo, para incluir somente controles habilitados em um modo de exibição de controle.

### <a name="raw-view"></a>Exibição bruta

A exibição bruta da árvore de automação da interface do usuário é a árvore completa de elementos de automação para os quais a área de trabalho é a raiz. A exibição bruta segue melhor a estrutura programática nativa de um aplicativo e é a exibição mais detalhada disponível. Também é a base na qual as outras exibições da árvore são criadas. Como essa exibição depende da estrutura subjacente da interface do usuário, a exibição bruta de um botão Windows Presentation Foundation (WPF) tem uma exibição bruta diferente de um botão do Microsoft Win32.

A exibição bruta é obtida pesquisando elementos sem especificar propriedades ou usando [**IUIAutomation:: RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker) para obter uma interface [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) para navegar pela árvore.

### <a name="control-view"></a>Exibição de controle

O modo de exibição de controle é um subconjunto da exibição bruta. Ele inclui somente os itens da interface do usuário que têm a propriedade [**IUIAutomationElement:: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) definida como **true**.

O modo de exibição de controle inclui os itens de interface do usuário que fornecem informações para o usuários ou permitem que o usuário execute uma ação. Esses são os itens da interface do usuário que são mais interessantes para testar aplicativos automatizados.

O modo de exibição de controle também inclui itens de interface do usuário não interativos que contribuem para a estrutura lógica da interface do usuário. Isso inclui contêineres de item, como cabeçalhos de exibição de lista, barras de ferramentas, menus e a barra de status. Outros itens não interativos que aparecem no modo de exibição de controle são elementos gráficos com informações e texto estático em uma caixa de diálogo.

Itens não interativos usados somente para fins de layout ou decorativos, como painéis usados para dispor controles em uma caixa de diálogo, não aparecem no modo de exibição de controle.

A exibição de controle da árvore de automação da interface do usuário é mapeada para a estrutura da interface do usuário percebida por um usuário final. Isso torna mais fácil para o produto de tecnologia assistencial descrever a interface do usuário final e ajudar o usuário final a interagir com o aplicativo.

O modo de exibição de controle é obtido pesquisando os elementos que têm a propriedade [**IUIAutomationElement:: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) definida como true ou usando [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) para obter uma interface [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) para navegar pela árvore.

### <a name="content-view"></a>Exibição de conteúdo

A exibição de conteúdo da árvore de automação da interface do usuário é um subconjunto da exibição de controle. Ele inclui somente os itens da interface do usuário que têm a propriedade [**IUIAutomationElement:: IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) e [**IUIAutomationElement:: IsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) definida como **true**.

O modo de exibição de conteúdo contém itens de interface do usuário que transmitem as informações reais em uma interface de usuários, incluindo itens de IU que podem receber o foco do teclado e algum texto que não seja um rótulo em um item da interface do usuário. Esses são os itens da interface do usuário que são mais interessantes para um aplicativo de leitor de tela. Por exemplo, os valores em uma caixa de combinação suspensa aparecem no modo de exibição de conteúdo porque os valores representam informações usadas por um usuário final.

No modo de exibição de conteúdo, uma caixa de combinação e uma caixa de listagem são representadas como uma coleção de itens de interface do usuário em que um ou mais de um item pode ser selecionado. O fato de um item estar sempre aberto e um item pode ser expandido e recolhido é irrelevante no modo de exibição de conteúdo porque ele foi projetado para mostrar os dados, ou o conteúdo, que está sendo apresentado ao usuário.

A exibição de conteúdo é obtida pesquisando os elementos que têm a propriedade [**IsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) e [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) definida como **true** ou usando [**IUIAutomation:: ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) para obter uma interface [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) para navegar pela árvore.

As imagens a seguir mostram as diferenças entre a exibição de controle e a exibição de conteúdo. A primeira imagem mostra uma caixa de combinação simples com três itens na lista suspensa. A segunda imagem mostra como os itens da interface do usuário da caixa de combinação aparecem nas exibições de controle e conteúdo do aplicativo UISpy.exe.

![captura de tela de uma caixa de combinação simples com três itens suspensos](images/combobox.png)

![captura de tela do aplicativo UISpy com exibições de controle e conteúdo dos itens da caixa de combinação](images/treeviews.jpg)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Criando o objeto CUIAutomation](uiauto-creatingcuiautomation.md)
</dt> <dt>

[Obtendo elementos da automação interface do usuário](uiauto-obtainingelements.md)
</dt> <dt>

[Conceitos básicos de automação da interface do usuário](entry-uiautocore-overview.md)
</dt> </dl>

 

 




