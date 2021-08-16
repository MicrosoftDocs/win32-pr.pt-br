---
title: Como consultar um item virtualizado no modo de exibição de itens
description: este tópico descreve como usar a automação da interface do usuário da Microsoft para recuperar informações da interface do usuário sobre itens virtualizados na exibição de itens Windows 7.
ms.assetid: a0bff8a1-47b1-4750-8086-e2e65a79099e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9196d62e7aa93b21aed15b76b8ced6a9520b27fb5bcee74a0e0d4ddc510c86f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759237"
---
# <a name="how-to-query-a-virtualized-item-in-items-view"></a>Como consultar um item virtualizado no modo de exibição de itens

este tópico descreve como usar a automação da interface do usuário da Microsoft para recuperar informações da interface do usuário sobre itens virtualizados na exibição de itens Windows 7. Este tópico inclui as seções a seguir.

> [!Note]  
> este tópico aplica-se somente ao Windows 7. Lembre-se de que os recursos de acessibilidade descritos neste tópico podem ser alterados em versões futuras do Windows.

 

-   [Visão geral](#overview)
-   [Estrutura de árvore de exibição de itens](#items-view-tree-structure)
-   [Virtualização](#virtualization)
-   [Obtendo uma contagem de todos os itens](#obtaining-a-count-of-all-items)
-   [Obtendo um índice de item com relação a todos os itens](#obtaining-an-item-index-with-respect-to-all-items)
-   [Obtendo uma referência a um item Vitualized](#obtaining-a-reference-to-a-vitualized-item)
-   [Rolando um item virtualizado na tela](#scrolling-a-virtualized-item-on-screen)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

A exibição de itens é um componente de interface do usuário que permite aos usuários exibir e interagir com arquivos e outros itens. no Windows 7, a exibição de itens substitui o controle de exibição de lista para apresentar itens na exibição padrão do Windows Explorer. a exibição itens também é usada na caixa de diálogo Item comum, menu Iniciar resultados da pesquisa e outros elementos da interface do usuário do Windows 7 que usam o controle navegador do Explorer. Em comparação com o controle de exibição de lista, a exibição de itens oferece as seguintes vantagens para os usuários:

-   A exibição de itens pode apresentar itens de maneiras mais úteis, desejáveis e relevantes, permitindo que os usuários encontrem e organizem itens de forma mais simples, rápida e apreciada.
-   A exibição de itens pode exibir grandes conjuntos de itens de fontes de dados que têm características de desempenho diferentes, permitindo que os usuários naveguem e pesquisem toda a coleção de itens em várias fontes.

a imagem a seguir mostra a exibição itens no Windows Explorer.

![captura de tela mostrando o componente de exibição de itens com o Windows Explorer](images/itemsview.gif)

Da perspectiva de um desenvolvedor, a estrutura geral e a funcionalidade da exibição de itens é semelhante à do controle de exibição de lista. A principal diferença é que a exibição de itens dá suporte à virtualização, enquanto o controle de exibição de lista não. Além disso, a exibição de itens usa duas novas interfaces de automação de interface do usuário para garantir que o conteúdo virtualizado fornecido pela exibição de itens seja acessível. Essas interfaces são descritas nas seções a seguir deste tópico.

Para obter informações gerais sobre a virtualização na automação da interface do usuário, consulte [trabalhando com itens virtualizados](uiauto-workingwithvirtualizeditems.md).

## <a name="items-view-tree-structure"></a>Estrutura de árvore de exibição de itens

Na árvore de automação da interface do usuário, o elemento da automação da interface do usuário de nível superior da exibição itens tem o nome "ItemsView" e o tipo de controle "lista". Na imagem anterior, o elemento de automação da interface do usuário do amItemsView é descrito em vermelho. Existem vários elementos de automação da interface do usuário abaixo do nível superior de ItemsView, mas somente dois outros elementos de automação da interface do usuário são referenciados neste documento: itens de grupo e itens de lista.

Os itens de grupo são os elementos de automação da interface do usuário que contêm todos os itens de lista desse grupo — seu tipo de controle é "grupo" e seus nomes variam de acordo com o nome do grupo. Na imagem anterior, o primeiro item de grupo contém o cabeçalho "A-H (1)" e o item de lista "pasta", e seu nome é "A-H".

Os itens de lista são os elementos de automação da interface do usuário que representam os itens de folha na exibição — o tipo de controle é "ListItem" e seus nomes variam de acordo com o nome do item. Na imagem anterior, os elementos da lista são os elementos folha, como "pasta", "música" e "imagem". Esses três elementos de automação de interface do usuário são referidos pelo elemento terms ItemsView, elemento Group e element ListItem no restante deste documento.

## <a name="virtualization"></a>Virtualização

A exibição de itens usa a virtualização, o que significa que os itens fora da área visível da exibição não são buscados no sistema e a representação da interface do usuário deles não é criada. Esses itens são chamados de *itens virtualizados*. Como eles não são criados, os itens virtualizados não têm elementos de automação da interface do usuário e, portanto, não aparecem na árvore de automação da interface do usuário quando um cliente de automação da interface do usuário enumera a árvore. Além disso, os padrões de controle de automação da interface do usuário operam somente em elementos visíveis. Por exemplo, o padrão de controle [Selection](uiauto-implementingselection.md) retorna apenas os itens visíveis selecionados quando um cliente chama o método [**IUIAutomationSelectionPattern:: GetCurrentSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-getcurrentselection) .

A exibição de itens dá suporte à capacidade de recuperar as seguintes informações sobre itens virtualizados:

-   Uma contagem do número total de itens, incluindo itens virtualizados
-   Elementos de automação da interface do usuário para itens virtualizados
-   Elementos de automação da interface do usuário para os itens virtualizados que são selecionados

## <a name="obtaining-a-count-of-all-items"></a>Obtendo uma contagem de todos os itens

Um cliente pode usar o elemento ItemsView para obter uma contagem de todos os itens, bem como uma contagem dos itens selecionados. O elemento ItemsView fornece duas maneiras de obter essas contagens. A primeira é obter a propriedade ItemProperty do elemento ItemsView, e a segunda é obter propriedades personalizadas do elemento ItemsView.

A propriedade ItemProperty é uma cadeia de caracteres que especifica uma contagem do número total de itens e uma contagem dos itens selecionados, separados por uma vírgula. Por exemplo: "3 itens, 1 item selecionado". Essa cadeia de caracteres é localizada e pode ser comunicada diretamente ao usuário.

As propriedades personalizadas do elemento ItemsView incluem uma propriedade para a contagem de itens e outra para a contagem de seleção. Eles incluem:

-   \_ \_ ABBF5C45-5CCC-47b7-BB4E-87CB87BBD162 (GUID da propriedade ItemCount) — a contagem de todos os itens exclusivos na exibição. Se agrupado por uma propriedade de vários valores (MVP) para que um único item possa aparecer várias vezes, cada item é contado apenas uma vez.

    (UIAutomationType: [**UIAutomationType \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), nome programático: "ItemCount")

-   \_ \_ GUID da propriedade SELECTEDITEMCOUNT (92A053DA-2969-4021-BF27-514CFC2E4A69) — a contagem de todos os itens exclusivos selecionados na exibição. Se agrupado por uma propriedade de vários valores (MVP) para que um único item possa aparecer várias vezes, cada item é contado apenas uma vez.

    (UIAutomationType: [**UIAutomationType \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), nome programático: "SelectedItemCount")

essas propriedades personalizadas são definidas em Shlguid. h, que está incluído no SDK (Software Development Kit) Windows, e essas propriedades são registradas por meio do método [**IUIAutomationRegistrar:: registerproperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) . Os clientes de automação da interface do usuário usam **RegisterProperty** para recuperar identificadores de propriedade (PROPERTYIDs) para as propriedades personalizadas.

## <a name="obtaining-an-item-index-with-respect-to-all-items"></a>Obtendo um índice de item com relação a todos os itens

Um cliente pode obter o índice de um item obtendo a propriedade ItemProperty de um elemento ListItem ou obtendo uma propriedade personalizada de um elemento ListItem.

A propriedade ItemProperty é uma cadeia de caracteres que contém o índice de um item em relação ao número total de itens. Por exemplo: "item 1 de 3". Essa cadeia de caracteres é localizada e pode ser comunicada diretamente ao usuário.

A propriedade personalizada a seguir obtém o índice de item de um elemento ListItem:

-   \_ \_ GUID da propriedade ITEMINDEX (92A053DA-2969-4021-BF27-514CFC2E4A69) — o índice absoluto com base em 1 de um item. Se agrupado por uma propriedade de vários valores (MVP) para que um único item possa aparecer duas vezes, cada aparência do item obterá um índice separado.

    (UIAutomationType: [**UIAutomationType \_ int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), nome programático: "ItemIndex")

essa propriedade personalizada é definida em Shlguid. h, que é incluída no SDK do Windows e é registrada por meio do método [**IUIAutomationRegistrar:: registerproperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) . Os clientes de automação da interface do usuário usam **RegisterProperty** para recuperar um PROPERTYIDs (identificador de propriedade) para a propriedade personalizada.

## <a name="obtaining-a-reference-to-a-vitualized-item"></a>Obtendo uma referência a um item Vitualized

Um elemento ItemsView implementa o padrão de controle [MyContainer](uiauto-implementingitemcontainer.md) (interface [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) ), que permite que um cliente obtenha um elemento de automação da interface do usuário para um item virtualizado (um item que está fora da área visível). ItemsView permite que o cliente encontre um elemento ListItem pesquisando nas propriedades Name e Selection — tentar Pesquisar em qualquer outra propriedade falhará.

Um elemento virtual implementa apenas o padrão de controle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) (interface [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) ). Como o item representado por um elemento de automação de interface do usuário virtualizado ainda não existe, a tentativa de obter qualquer outro padrão de controle ou Propriedade do elemento falhará.

Os elementos ListItem e Group são virtualizados, mas somente elementos ListItem podem ser retornados do padrão de controle de item [contido](uiauto-implementingitemcontainer.md) . Como a chamada para o método [**IUIAutomationItemContainerPattern:: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) é executada no thread da interface do usuário e está sendo bloqueada, a exibição não responderá até que **FindItemByProperty** seja retornado, e quaisquer outras chamadas de método no provedor deverão aguardar até que **FindItemByProperty** seja concluído. Em alguns casos, o **FindItemByProperty** deve processar todo o conjunto de dados antes de retornar, o que pode consumir muitos recursos. A especificação de **NULL** como o elemento inicial faz com que **FindItemByProperty** inicie a pesquisa com o primeiro item na exibição.

O ItemsView dá suporte às seguintes propriedades para [**FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty):

-   Name (UIA \_ NamePropertyId) – procura o primeiro item cujo nome corresponde totalmente à cadeia de caracteres especificada. A pesquisa não diferencia maiúsculas de minúsculas. Não há suporte para caracteres curinga ou correspondência parcial. Se um nome **nulo** for especificado, o próximo item após o elemento inicial será retornado. A especificação de nomes **nulos** permite que um cliente de automação da interface do usuário Enumere todos os itens na exibição; no entanto, a enumeração de todos os itens é desencorajada porque faz com que todos os itens na exibição sejam percebidos.
-   SelectionItem \_ IsSelected (UIA \_ SelectionItemIsSelectedPropertyId) — procura o primeiro item cuja \_ propriedade IsSelected SelectionItem corresponde ao valor especificado. Especifique **true** para localizar o primeiro item selecionado ou **false** para localizar o primeiro item não selecionado. Tenha cuidado ao enumerar todos os itens selecionados porque o número de itens selecionados pode ser muito grande, especialmente se o usuário tiver selecionado todos os itens.

## <a name="scrolling-a-virtualized-item-on-screen"></a>Rolando um item virtualizado na tela

Depois de obter uma referência a um elemento de automação da interface do usuário para um item virtualizado (fora da tela), o cliente pode rolar o item para a exibição usando o método [**IUIAutomationVirtualizeItemPattern:: perceba**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) do padrão de controle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . Depois que o item é percebido, ele fica visível e todas as propriedades e padrões de controle normalmente associados a um elemento ListItem estão disponíveis para o cliente.

Somente os elementos ListItem obtidos pelo método [**IUIAutomationItemContainerPattern:: FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) expõem o padrão de controle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . Quando um elemento na tela é rolado para fora da tela, o elemento torna-se inválido e o cliente deve chamar **FindItemByProperty** para obter a referência fora da tela.

Também é possível mover itens para dentro e fora do modo de exibição usando o padrão de controle [Scroll](uiauto-implementingscroll.md) (ou usando as barras de rolagem). Itens e grupos são realizados conforme rolam para a exibição e são virtualizados à medida que rolam para fora da exibição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com itens virtualizados](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




