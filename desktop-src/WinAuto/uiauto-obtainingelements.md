---
title: Obtendo elementos da automação interface do usuário
description: Este tópico descreve várias maneiras de obter interfaces IUIAutomationElement para elementos de interface do usuário.
ms.assetid: 8675851a-4a72-4cbe-ab71-ed6fc891be17
keywords:
- clientes, obtendo elementos de automação da interface do usuário
- clientes, elementos de automação da interface do usuário
- clientes, elementos raiz
- clientes, escopo da pesquisa
- Automação da interface do usuário, obtendo elementos
- Automação da interface do usuário, elementos
- Automação da interface do usuário, elementos raiz
- Automação da interface do usuário, condições
- Automação da interface do usuário, escopo da pesquisa
- obtendo elementos de automação da interface do usuário
- elementos raiz
- escopo da pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: a1adbcea5cea81f97350ef15c491b289e07d3ee6
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/20/2021
ms.locfileid: "105813355"
---
# <a name="obtaining-ui-automation-elements"></a>Obtendo elementos da automação interface do usuário

Este tópico descreve várias maneiras de obter interfaces [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para elementos de interface do usuário.

**IUIAutomationElement** é usado no [aplicativo de exemplo de cliente de conteúdo do documento de automação de IU](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient).

## <a name="root-element"></a>Elemento Root

Embora elementos possam ser recuperados diretamente usando métodos, como [**IUIAutomation:: Getconcentrouelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), alguns aplicativos cliente exigem uma exibição da estrutura hierárquica dos elementos, conhecida como árvore de automação da interface do usuário. O elemento raiz dessa hierarquia é a área de trabalho. Você pode obter esse elemento usando o método [**IUIAutomation:: getRootElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelement) ou o método [**IUIAutomation:: GetRootElementBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getrootelementbuildcache) . Ambos os métodos recuperam um ponteiro de interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) . Você pode Pesquisar elementos descendentes usando métodos, como [**IUIAutomationElement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) e [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall).

> [!Note]  
> Em geral, você deve tentar obter apenas filhos diretos do elemento raiz. Uma pesquisa por descendentes pode iterar por centenas ou milhares de elementos. Se você estiver tentando obter um elemento específico em um nível inferior, deverá iniciar a pesquisa na janela do aplicativo ou em um contêiner em um nível inferior.

 

## <a name="conditions"></a>Condições

Para a maioria das técnicas que você usa para recuperar elementos de automação da interface do usuário, você deve especificar uma condição. Uma condição é um conjunto de critérios que define os elementos que você deseja recuperar. Uma condição é representada pela interface [**IUIAutomationCondition**](/windows/win32/api/uiautomationclient/nn-uiautomationclient-iuiautomationcondition) .

A condição mais simples é a condição verdadeira, que é um objeto predefinido que especifica que todos os elementos no escopo de pesquisa devem ser retornados. A condição false é o inverso da condição verdadeira e é menos útil, pois isso impediria que nenhum elemento fosse encontrado. Você pode obter uma interface para a condição verdadeira usando [**IUIAutomation:: CreateTrueCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtruecondition).

Três outras condições predefinidas, disponíveis como propriedades no objeto [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) , podem ser usadas sozinhas ou em combinação com outras condições: [**IUIAutomation:: ContentViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewcondition), [**ControlViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewcondition)e [**RawViewCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewcondition). **RawViewCondition**, usado por si só, é equivalente à condição true, porque não filtra elementos pelas propriedades [**IUIAutomationElement:: CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) ou [**CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) .

Outras condições são criadas a partir de objetos Condition, cada um deles especifica um valor de propriedade. Por exemplo, uma condição de propriedade pode especificar que o elemento está habilitado ou que ele dá suporte a um determinado padrão de controle.

As condições que usam a lógica booliana podem ser combinadas chamando [**IUIAutomation:: CreateAndCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createandcondition), [**CreateOrCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createorcondition), [**CreateNotCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createnotcondition)e métodos relacionados.

## <a name="search-scope"></a>Escopo de pesquisa

As pesquisas executadas usando [**IUIAutomationElement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) ou [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) devem ter um escopo e um local de início.

> [!Note]  
> Comentários sobre esses dois métodos também se aplicam a [**IUIAutomationElement:: FindFirstBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirstbuildcache) e [**FindAllBuildCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findallbuildcache).

 

O escopo define o espaço em volta do local inicial que deve ser pesquisado. Isso pode incluir o próprio elemento, seus irmãos, seu pai, seus filhos imediatos e seus descendentes. Lembre-se de que os métodos **Find** não dão suporte à pesquisa da árvore de automação da interface do usuário da Microsoft. ou seja, não há suporte para a pesquisa de elementos ancestrais.

O escopo de uma pesquisa é definido por uma combinação de bits de valores do tipo enumerado [**TreeScope**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope) .

## <a name="finding-a-known-element"></a>Encontrando um elemento conhecido

Para localizar um elemento conhecido que é identificado por nome, ID de automação ou alguma outra propriedade ou combinação de propriedades, é mais fácil usar o método [**IUIAutomationElement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst) . Se o elemento procurado for uma janela de aplicativo, o ponto de partida da pesquisa poderá ser o elemento raiz.

Essa forma de localizar elementos de automação da interface do usuário é mais útil em cenários de teste automatizados.

Para obter um exemplo de código que mostra como encontrar um elemento conhecer, consulte [localizando um elemento por nome](uiauto-howto-find-ui-elements.md).

## <a name="finding-elements-in-a-subtree"></a>Localizando elementos em uma subárvore

Para localizar todos os elementos que atendem a critérios específicos e estão relacionados a um elemento conhecido, você pode chamar [**IUIAutomationElement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall) no elemento conhecido. Por exemplo, use esse método para recuperar itens de lista ou itens de menu de uma lista ou menu, ou para identificar todos os controles em uma caixa de diálogo.

Para obter um exemplo de código que mostra como localizar elementos em uma subárvore, consulte [Localizando elementos relacionados](uiauto-howto-find-ui-elements.md).

## <a name="walking-a-subtree"></a>Examinando uma subárvore

Se você não tiver conhecimento prévio dos aplicativos com os quais seu cliente pode ser usado, poderá construir uma subárvore de todos os elementos de interesse usando o [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker). O cliente pode fazer isso, por exemplo, em resposta a um evento de alteração de foco; ou seja, quando um aplicativo ou controle recebe o foco de entrada, o cliente de automação da interface do usuário examina os filhos e talvez todos os descendentes do elemento focado.

Lembre-se de que a movimentação da árvore de automação da interface do usuário exige muitos recursos. Oriente a árvore somente quando não for possível usar os métodos [**IUIAutomationElement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst), [**FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)ou [**BuildUpdatedCache**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-buildupdatedcache) .

Você pode definir seu próprio Walker de árvore passando uma condição personalizada para [**IUIAutomation:: CreateTreeWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createtreewalker)ou pode usar um dos seguintes objetos predefinidos que são definidos como propriedades do [**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation)base.



| Objeto                                                              | Finalidade                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker) | Localiza somente elementos cuja propriedade [**IUIAutomationElement:: CurrentIsContentElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontentelement) é **true**. |
| [**ControlViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_controlviewwalker) | Localiza somente elementos cuja propriedade [**IUIAutomationElement:: CurrentIsControlElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentiscontrolelement) é **true**. |
| [**RawViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_rawviewwalker)         | Localiza todos os elementos.                                                                                                                                          |



 

Depois de obter um [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker), chame os métodos **IUIAutomationTreeWalker:: GetXxx** para navegar pelos elementos da subárvore, passando o elemento do qual iniciar a movimentação.

O método [**IUIAutomationTreeWalker:: Normalize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtreewalker-normalizeelement) pode ser usado para navegar para um elemento na subárvore de outro elemento que não faz parte da exibição. Por exemplo, suponha que você crie uma exibição de uma subárvore usando [**IUIAutomation:: ContentViewWalker**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-get_contentviewwalker). Seu aplicativo recebe uma notificação de que uma barra de rolagem recebeu o foco de entrada. Como uma barra de rolagem não é um elemento de conteúdo, ela não está presente na exibição da subárvore. No entanto, você pode passar o [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) que representa a barra de rolagem para **IUIAutomationTreeWalker:: Normalize** e recuperar o ancestral mais próximo que está na exibição de conteúdo.

Para obter exemplos de código que mostram como usar a interface [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) , consulte [como percorrer a árvore de automação da interface do usuário](uiauto-howto-walk-uiautomation-tree.md).

## <a name="other-ways-to-retrieve-an-element"></a>Outras maneiras de recuperar um elemento

Além de pesquisas e navegação, você pode recuperar um [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) das seguintes maneiras.

### <a name="from-an-event"></a>De um evento

Quando seu aplicativo recebe um evento de automação de interface do usuário, o objeto de origem passado para o manipulador de eventos é representado por um [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement). Por exemplo, se você se inscrever em eventos de foco alterado, a origem passada para seu [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) é o elemento que recebeu o foco. Para obter mais informações, consulte [inscrevendo-se em eventos de automação da interface do usuário](uiauto-eventsforclients.md).

### <a name="from-a-point"></a>De um ponto

Para recuperar um [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de coordenadas de tela, por exemplo, uma posição de cursor, use o método [**IUIAutomation:: ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint) .

### <a name="from-a-window-handle"></a>De um identificador de janela

Para recuperar um [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de um **HWND**, use o método [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle) .

### <a name="from-the-focused-control"></a>Do controle focado

Para recuperar um [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) que representa o controle focalizado, use o método [**IUIAutomation:: getconcentrouelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement) .

## <a name="related-topics"></a>Tópicos relacionados

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)

[Aplicativo de amostra do cliente de conteúdo do documento de automação de IU](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/UIAutomationDocumentClient)
