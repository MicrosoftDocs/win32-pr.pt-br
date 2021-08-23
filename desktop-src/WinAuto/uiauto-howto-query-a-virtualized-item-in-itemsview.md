---
title: Como consultar um item virtualizado na exibição de itens
description: Este tópico descreve como usar o Microsoft Automação da Interface do Usuário para recuperar informações da interface do usuário sobre itens virtualizados na exibição Windows 7 Itens.
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
# <a name="how-to-query-a-virtualized-item-in-items-view"></a>Como consultar um item virtualizado na exibição de itens

Este tópico descreve como usar o Microsoft Automação da Interface do Usuário para recuperar informações da interface do usuário sobre itens virtualizados na exibição Windows 7 Itens. Este tópico inclui as seções a seguir.

> [!Note]  
> Este tópico se aplica somente Windows 7. Esteja ciente de que os recursos de acessibilidade descritos neste tópico podem mudar em versões futuras do Windows.

 

-   [Visão geral](#overview)
-   [Estrutura da árvore de exibição de itens](#items-view-tree-structure)
-   [Virtualização](#virtualization)
-   [Obtendo uma contagem de todos os itens](#obtaining-a-count-of-all-items)
-   [Obtendo um índice de item em relação a todos os itens](#obtaining-an-item-index-with-respect-to-all-items)
-   [Obtendo uma referência a um item vitualizado](#obtaining-a-reference-to-a-vitualized-item)
-   [Rolar um item virtualizado na tela](#scrolling-a-virtualized-item-on-screen)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

Exibição de Itens é um componente de interface do usuário que permite aos usuários exibir e interagir com arquivos e outros itens. No Windows 7, a Exibição de Itens substitui o controle de exibição de lista para apresentar itens na exibição padrão do Windows Explorer. A Exibição de Itens também é usada na caixa de diálogo Item Comum, menu Iniciar resultados da pesquisa e outros Windows 7 interface do usuário que usam o controle Explorer Browser. Em comparação com o controle de exibição de lista, a Exibição de Itens oferece as seguintes vantagens para os usuários:

-   A Exibição de Itens pode apresentar itens de maneiras mais úteis, desejáveis e relevantes, permitindo que os usuários encontrem e organizem itens de maneira mais simples, rápida e conveniente.
-   A Exibição de Itens pode exibir grandes conjuntos de itens de fontes de dados que têm características de desempenho diferentes, permitindo que os usuários naveguem e pesquisem toda a coleção de itens em várias fontes.

A imagem a seguir mostra a Exibição de Itens no Windows Explorer.

![captura de tela mostrando o windows explorer com o componente de exibição de itens](images/itemsview.gif)

Da perspectiva de um desenvolvedor, a estrutura geral e a funcionalidade da Exibição de Itens são semelhantes às do controle de exibição de lista. A principal diferença é que a Exibição de Itens dá suporte à virtualização, enquanto o controle de exibição de lista não dá suporte. Além disso, a Exibição de Itens usa duas novas interfaces Automação da Interface do Usuário para garantir que o conteúdo virtualizado fornecido pela Exibição de Itens seja acessível. Essas interfaces são descritas nas seções a seguir deste tópico.

Para obter informações gerais sobre a virtualização Automação da Interface do Usuário, consulte [Trabalhando com itens virtualizados.](uiauto-workingwithvirtualizeditems.md)

## <a name="items-view-tree-structure"></a>Estrutura da árvore de exibição de itens

Na árvore Automação da Interface do Usuário, o elemento Automação da Interface do Usuário nível superior da Exibição de Itens tem o nome "ItemsView" e o tipo de controle "list". Na imagem anterior, o elemento itemsView Automação da Interface do Usuário é descrito em vermelho. Vários Automação da Interface do Usuário existem abaixo do nível superior de ItemsView, mas apenas dois outros Automação da Interface do Usuário elementos são referenciados neste documento: itens de grupo e itens de lista.

Os itens de grupo são os Automação da Interface do Usuário que contêm todos os itens de lista desse grupo— seu tipo de controle é "Grupo" e seus nomes variam dependendo do nome do grupo. Na imagem anterior, o primeiro item de grupo contém o título "A-H (1)" e o item de lista "Pasta" e seu nome é "A-H".

Os itens de lista são Automação da Interface do Usuário elementos que representam os itens folha na exibição— seu tipo de controle é "ListItem" e seus nomes variam dependendo do nome do item. Na imagem anterior, os elementos de lista são os elementos folha, como "Pasta", "Música" e "Imagem". Esses três Automação da Interface do Usuário elementos são referenciados pelos termos elemento ItemsView, elemento Group e elemento ListItem no restante deste documento.

## <a name="virtualization"></a>Virtualização

A Exibição de Itens usa virtualização, o que significa que os itens fora da área visível da exibição não são buscados do sistema e a representação da interface do usuário deles não é criada. Esses itens são chamados *de itens virtualizados.* Como eles não são criados, os itens virtualizados não têm Automação da Interface do Usuário elementos e, portanto, não aparecem na árvore Automação da Interface do Usuário quando um cliente Automação da Interface do Usuário enumera a árvore. Além disso, Automação da Interface do Usuário de controle operam somente em elementos visíveis. Por exemplo, [](uiauto-implementingselection.md) o padrão de controle Seleção retorna apenas os itens selecionados visíveis quando um cliente chama o método [**IUIAutomationSelectionPattern::GetCurrentSelection.**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-getcurrentselection)

A Exibição de Itens dá suporte à capacidade de recuperar as seguintes informações sobre itens virtualizados:

-   Uma contagem do número total de itens, incluindo itens virtualizados
-   Automação da Interface do Usuário elementos para itens virtualizados
-   Automação da Interface do Usuário elementos para os itens virtualizados selecionados

## <a name="obtaining-a-count-of-all-items"></a>Obtendo uma contagem de todos os itens

Um cliente pode usar o elemento ItemsView para obter uma contagem de todos os itens, bem como uma contagem dos itens selecionados. O elemento ItemsView fornece duas maneiras de obter essas contagens. A primeira é obter a propriedade ItemStatus do elemento ItemsView e a segunda é obter propriedades personalizadas do elemento ItemsView.

A propriedade ItemStatus é uma cadeia de caracteres que especifica uma contagem do número total de itens e uma contagem dos itens selecionados, separados por uma vírgula. Por exemplo: "3 itens, 1 item selecionado". Essa cadeia de caracteres é localizada e pode ser comunicada diretamente ao usuário.

As propriedades personalizadas do elemento ItemsView incluem uma propriedade para a contagem de itens e outra para a contagem de seleção. Eles incluem:

-   GUID da propriedade ItemCount \_ \_ (ABBF5C45-5CCC-47b7-BB4E-87CB87BBD162)— A contagem de todos os itens exclusivos na exibição. Se agrupado por uma propriedade de vários valores (MVP) para que um único item possa aparecer várias vezes, cada item será contado apenas uma vez.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Nome programático: "ItemCount")

-   GUID da Propriedade SelectedItemCount \_ \_ (92A053DA-2969-4021-BF27-514CFC2E4A69)— A contagem de todos os itens exclusivos selecionados na exibição. Se agrupado por uma propriedade de vários valores (MVP) para que um único item possa aparecer várias vezes, cada item será contado apenas uma vez.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Nome programático: "SelectedItemCount")

Essas propriedades personalizadas são definidas em Shlguid.h, que está incluído no SDK (Software Development Kit) do Windows e essas propriedades são registradas por meio do método [**IUIAutomationRegistrar::RegisterProperty.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) Automação da Interface do Usuário clientes usam **RegisterProperty** para recuperar identificadores de propriedade (PROPERTYIDs) para as propriedades personalizadas.

## <a name="obtaining-an-item-index-with-respect-to-all-items"></a>Obtendo um índice de item em relação a todos os itens

Um cliente pode obter o índice de um item obtendo a propriedade ItemStatus de um elemento ListItem ou obtendo uma propriedade personalizada de um elemento ListItem.

A propriedade ItemStatus é uma cadeia de caracteres que contém o índice de um item em relação ao número total de itens. Por exemplo: "item 1 de 3". Essa cadeia de caracteres é localizada e pode ser comunicada diretamente ao usuário.

A seguinte propriedade personalizada obtém o índice de item de um elemento ListItem:

-   GUID da propriedade ItemIndex \_ \_ (92A053DA-2969-4021-BF27-514CFC2E4A69)— o índice absoluto baseado em 1 de um item. Se agrupado por uma propriedade de vários valores (MVP) para que um único item possa aparecer duas vezes, cada aparência do item obtém um índice separado.

    (UIAutomationType: [**UIAutomationType \_ Int**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype), Nome programático: "ItemIndex")

Essa propriedade personalizada é definida em Shlguid.h, que está incluída no SDK do Windows e é registrada por meio do método [**IUIAutomationRegistrar::RegisterProperty.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) Automação da Interface do Usuário clientes usam **RegisterProperty** para recuperar um identificador de propriedade (PROPERTYIDs) para a propriedade personalizada.

## <a name="obtaining-a-reference-to-a-vitualized-item"></a>Obtendo uma referência a um item vitualizado

Um elemento ItemsView implementa o padrão de controle [ItemContainer](uiauto-implementingitemcontainer.md) (interface [**IItemContainerProvider),**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) que permite que um cliente receba um elemento Automação da Interface do Usuário para um item virtualizado (um item que está fora da área visível). ItemsView permite que o cliente encontre um elemento ListItem pesquisando as propriedades Nome e Seleção – a tentativa de pesquisar em qualquer outra propriedade falhará.

Um elemento virtual implementa apenas o padrão de controle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) ( interface [**IVirtualizedItemProvider).**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) Como o item representado por um elemento Automação da Interface do Usuário virtualizado ainda não existe, a tentativa de obter qualquer outro padrão de controle ou propriedade do elemento falhará.

Os elementos ListItem e Group são virtualizados, mas somente elementos ListItem podem ser retornados do [padrão de controle ItemContainer.](uiauto-implementingitemcontainer.md) Como a chamada para o método [**IUIAutomationItemContainerPattern::FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) é executado no thread da interface do usuário e está bloqueando, a exibição não responderá até **que FindItemByProperty** retorne e quaisquer outras chamadas de método no provedor devem aguardar até que **FindItemByProperty** seja finalada. Em alguns casos, **FindItemByProperty** deve processar todo o conjunto de dados antes de retornar, o que pode ser intensivo de recursos. Especificar **NULL como** o elemento inicial faz **com que FindItemByProperty** inicie a pesquisa com o primeiro item na exibição.

O ItemsView dá suporte às seguintes propriedades [**para FindItemByProperty:**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty)

-   Name (UIA NamePropertyId)— pesquisa o primeiro item cujo nome corresponde totalmente \_ à cadeia de caracteres especificada. A pesquisa não diferencia maiúsculas de minúsculas. Não há suporte para caracteres curinga ou correspondência parcial. Se um **nome NULL** for especificado, o próximo item após o elemento inicial será retornado. Especificar nomes **NULL** permite que um cliente Automação da Interface do Usuário enumerar todos os itens na exibição; No entanto, não é possível enumerar todos os itens porque isso faz com que todos os itens na exibição sejam realizados.
-   SelectionItem \_ IsSelected (UIA \_ SelectionItemIsSelectedPropertyId)— pesquisa o primeiro item cuja propriedade SelectionItem IsSelected corresponde ao \_ valor especificado. **Especifique TRUE** para encontrar o primeiro item selecionado ou **FALSE** para encontrar o primeiro item não selecionado. Tenha cuidado ao enumerar todos os itens selecionados porque o número de itens selecionados pode ser muito grande, especialmente se o usuário tiver selecionado todos os itens.

## <a name="scrolling-a-virtualized-item-on-screen"></a>Rolar um item virtualizado na tela

Depois de obter uma referência a um elemento Automação da Interface do Usuário para um item virtualizado (fora da tela), o cliente pode rolar o item para a exibição usando o método [**IUIAutomationVirtualizeItemPattern::Realize**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize) do padrão de controle [VirtualizedItem.](uiauto-implementingvirtualizeditem.md) Depois que o item é realizado, ele fica visível e todas as propriedades e padrões de controle normalmente associados a um elemento ListItem estão disponíveis para o cliente.

Somente elementos ListItem obtidos pelo [**método IUIAutomationItemContainerPattern::FindItemByProperty**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationitemcontainerpattern-finditembyproperty) expõem o padrão de [controle VirtualizedItem.](uiauto-implementingvirtualizeditem.md) Quando um elemento na tela é rolado para fora da tela, o elemento se torna inválido e o cliente deve chamar **FindItemByProperty** para obter a referência fora da tela.

Também é possível mover itens para dentro e [](uiauto-implementingscroll.md) fora da exibição usando o padrão de controle De rolagem (ou usando as barras de rolagem). Os itens e os grupos são percebidos quando rolam para a exibição e são virtualizados à medida que rolam para fora da exibição.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com itens virtualizados](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




