---
title: Padrão de controle de IsContainer
description: Descreve as diretrizes e convenções para implementar o IItemContainerProvider, incluindo informações sobre métodos. O padrão de controle de item contido é usado para dar suporte à virtualização de itens.
ms.assetid: 6f3dd94e-3563-4a13-9db9-5928a02bab77
keywords:
- Automação da interface do usuário, implementando o padrão de controle de contêiner
- Automação da interface do usuário, padrão de controle de IsContainer
- Automação da interface do usuário, IItemContainerProvider
- IItemContainerProvider
- Implementando padrões de controle do contêiner de automação da interface do usuário
- Padrões de controle de IsContainer
- padrões de controle, IItemContainerProvider
- padrões de controle, implementando a automação da interface do usuário
- padrões de controle, IsContainer
- interfaces, IItemContainerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69c0407a8f167a3a89b908c1b5555a9d32363b38b3ce5ab4d1794e726666a8c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413446"
---
# <a name="itemcontainer-control-pattern"></a>Padrão de controle de IsContainer

Descreve as diretrizes e convenções para implementar o [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider), incluindo informações sobre métodos. O padrão de controle de item **contido** é usado para dar suporte à virtualização de itens.

Controles que contêm um grande número de itens filho podem usar a virtualização para gerenciar os itens com eficiência. Com a virtualização, o controle mantém informações completas na memória apenas para um subconjunto de itens em um determinado momento. Normalmente, o subconjunto inclui apenas os itens que estão visíveis para o usuário no momento. As informações completas sobre os itens virtualizados restantes são mantidas no armazenamento e são carregadas na memória ou realizadas, pois o controle precisa dele, por exemplo, à medida que novos itens se tornam visíveis para o usuário.

Por exemplo, o diagrama a seguir mostra uma caixa de listagem que contém milhares de itens virtualizados. Como o controle mantém informações completas apenas para os itens filho que estão visíveis no momento, o provedor pode expor elementos de automação da interface do usuário da Microsoft somente para os itens 100 – 127.

![diagrama mostrando itens em uma caixa de listagem que são virtualizados e não virtualizados](images/virtualizeditems.jpg)

Os controles que usam a virtualização representam um desafio, pois apenas itens obtidos (desvirtualizados) estão totalmente disponíveis como elementos de automação da interface do usuário na árvore de automação da interface do usuário. Os itens virtualizados não existem na árvore, portanto, as informações sobre eles não estão disponíveis.

Para fornecer informações sobre itens virtualizados, os provedores implementam o padrão de controle de item **contido** , que expõe a interface [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) . O método [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) localiza itens filho com base no valor de uma propriedade específica, como **Name**, **AutomationId** ou **IsSelected**. Se um item for virtualizado, **FindItemByProperty** recuperará um elemento de espaço reservado de automação da interface do usuário para o item. Um elemento de espaço reservado é uma implementação da interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) que dá suporte apenas ao padrão de controle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) .

O método [**IVirtualizedItemProvider:: perceba**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) permite que um cliente solicite que um item virtualizado seja percebido, expondo assim um elemento de automação de interface do usuário completo para o item, de forma que todas as propriedades e padrões necessários estejam disponíveis.

Embora o objetivo principal do padrão **de controle de recipiente seja** dar suporte a cenários de contêiner virtualizados, ele pode ser implementado por qualquer contêiner que recupere itens filhos por nome, independentemente de o contêiner usar a virtualização.

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para IItemContainerProvider](#required-members-for-iitemcontainerprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle de **IsContainer** , observe as seguintes diretrizes e convenções:

-   Qualquer controle que possa conter itens virtualizados deve dar suporte ao padrão de controle de **IsContainer** . Qualquer contêiner que dá suporte à recuperação de itens com base em um valor de propriedade pode dar suporte a esse padrão, independentemente de o contêiner usar a virtualização.
-   Quando um contêiner é virtualizado, outros padrões de controles, como [seleção](uiauto-implementingselection.md), [tabela](uiauto-implementingtable.md)e [grade](uiauto-implementinggrid.md) , podem ser afetados. Por exemplo, o método [**ISelectionProvider:: getseleções**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) pode dar suporte apenas a elementos que estão no visor ou apenas a elementos selecionados que não estão virtualizados no momento.
-   O padrão de controle [Scroll](uiauto-implementingscroll.md) não deve ser afetado pela virtualização.
-   Nenhuma informação de contagem ou de índice de itens está disponível para itens virtualizados. Um controle virtualizado pode usar **a propriedade** **DescribedBy** ou o ItemProperty para fornecer essas informações, se necessário.
-   Os desenvolvedores de controle devem documentar e publicar detalhes de todas as propriedades de automação da interface do usuário e padrões de controle afetados pelo uso da virtualização. Embora os padrões de controle de IsContainer e [VirtualizedItem](uiauto-implementingvirtualizeditem.md) ofereçam suporte básico, eles podem não dar suporte a alguns comportamentos de virtualização.

As diretrizes e os requisitos a seguir se aplicam ao método [**IItemContainerProvider:: FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) .

-   Embora não seja necessário, a Microsoft recomenda enfaticamente que o [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) dê suporte às propriedades **Name**, **AutomationId** e **IsSelected** .
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) pode ser lento se precisar percorrer vários objetos para localizar um correspondente.
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) pode ser chamado repetidamente para localizar itens em sequência. Os itens podem estar em qualquer ordem, desde que cada item seja retornado apenas uma vez.
-   [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) pode ser implementado para localizar apenas os elementos que aparecem na exibição de controle ou de conteúdo da árvore de automação da interface do usuário. Os elementos que aparecem somente na exibição bruta podem ser ignorados para evitar a recuperação de vários elementos que representam apenas uma parte de um "item" para o usuário.
-   Quando os critérios de pesquisa correspondem a um item virtualizado, o provedor pode retornar um elemento de espaço reservado que dá suporte ao padrão de controle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) . As diretrizes a seguir se aplicam a elementos de espaço reservado:
    -   A recuperação de um elemento de espaço reservado para um item virtualizado não deve causar alterações na interface do usuário.
    -   O elemento de espaço reservado deve ser um par de outros elementos filho (um evento de alteração de estrutura é necessário).
    -   Quando possível, o provedor pode criar um elemento de automação completa em vez de um espaço reservado.
-   Quando os critérios de pesquisa correspondem a um elemento não virtualizado, o provedor deve retornar o elemento real, não um espaço reservado.
-   Quando nenhum item é encontrado, [**IItemContainerProvider:: FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) deve definir o parâmetro *pFound* como **NULL** e retornar **S \_ OK**.
-   Quando o parâmetro *PropertyId* for 0, o provedor deverá retornar o próximo item após *pStartAfter*.
-   Se o parâmetro *pStartAfter* for **NULL** e *PropertyId* for 0, o provedor deverá retornar o primeiro item no contêiner.
-   Quando o parâmetro *PropertyId* for 0, o parâmetro Value será ignorado.

As diretrizes e os requisitos a seguir se aplicam a elementos de espaço reservado para itens virtualizados na árvore de automação da interface do usuário.

-   Embora os provedores sejam incentivados a dar suporte a mais propriedades e padrões de controle para um elemento de espaço reservado, somente o padrão de controle [VirtualizedItem](uiauto-implementingvirtualizeditem.md) é necessário.
-   O provedor pode invalidar um elemento de espaço reservado anterior quando [**IItemContainerProvider:: FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) é chamado novamente. (Se um cliente precisar perceber o elemento de espaço reservado, ele deverá fazer isso imediatamente; caso contrário, o elemento poderá ser invalidado se **FindItemByProperty** for chamado novamente ou se o visor for alterado por qualquer motivo.)
-   Ações de interface do usuário, como rolagem ou redimensionamento, podem fazer com que o visor do contêiner seja alterado e um novo conjunto de itens filhos se torne visível. Nesse caso, elementos de espaço reservado recuperados anteriormente podem não estar disponíveis na árvore de automação da interface do usuário.
-   O provedor não deve virtualizar os elementos da interface do usuário que estão disponíveis na tela no visor do objeto de contêiner.

## <a name="required-members-for-iitemcontainerprovider"></a>Membros necessários para IItemContainerProvider

O método a seguir é necessário para implementar a interface [**IItemContainerProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iitemcontainerprovider) .



| Membros necessários                                                               | Tipo de membro | Observações |
|--------------------------------------------------------------------------------|-------------|-------|
| [**FindItemByProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iitemcontainerprovider-finditembyproperty) | Método      | Nenhum  |



 

O padrão de controle de **contêiner** não tem propriedades ou eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> <dt>

[Padrão de controle VirtualizedItem](uiauto-implementingvirtualizeditem.md)
</dt> </dl>

 

 




