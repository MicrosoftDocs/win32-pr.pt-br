---
title: Padrão de controle ExpandCollapse
description: Descreve diretrizes e convenções para implementar IExpandCollapseProvider, incluindo informações sobre propriedades, métodos e eventos.
ms.assetid: 0ffc26c3-8696-44f9-b463-902a69e06d21
keywords:
- Automação da Interface do Usuário, implementando o padrão de controle ExpandCollapse
- Automação da Interface do Usuário, padrão de controle ExpandCollapse
- Automação da Interface do Usuário,IExpandCollapseProvider
- IExpandCollapseProvider
- implementando Automação da Interface do Usuário de controle ExpandCollapse
- Padrões de controle ExpandCollapse
- padrões de controle, IExpandCollapseProvider
- padrões de controle, implementando Automação da Interface do Usuário ExpandCollapse
- padrões de controle, ExpandCollapse
- interfaces,IExpandCollapseProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7fa1461110a7fcdee83b8b3c20c15653e7bd5740187b89337620f5410b2bf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998036"
---
# <a name="expandcollapse-control-pattern"></a>Padrão de controle ExpandCollapse

Descreve diretrizes e convenções para implementar [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider), incluindo informações sobre propriedades, métodos e eventos. O **padrão de controle ExpandCollapse** é usado para dar suporte a controles que se expandem visualmente para exibir mais conteúdo e recaia para ocultar conteúdo.

Para exemplos de controles que implementam esse padrão de controle, consulte [Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IExpandCollapseProvider**](#required-members-for-iexpandcollapseprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão **de controle ExpandCollapse,** observe as seguintes diretrizes e convenções:

-   Os controles de agregação, construídos com objetos filho que fornecem à interface do usuário a funcionalidade de expansão/regregação, devem dar suporte ao padrão de controle **ExpandCollapse,** enquanto seus elementos filho não dão suporte. Por exemplo, um controle de caixa de combinação é criado com uma combinação de controles de caixa de listagem, botão e edição, mas é apenas a caixa de combinação pai que deve dar suporte ao padrão de controle **ExpandCollapse.**
    > [!Note]  
    > Uma exceção é o controle de menu, que é uma agregação de objetos de item de menu individuais. Os objetos de item de menu podem dar suporte **ao padrão de controle ExpandCollapse,** mas o controle de menu pai não pode. Uma exceção semelhante se aplica aos controles de árvore e item de árvore.

     

-   Quando [**IExpandCollapseProvider::ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) de um controle é definido como **ExpandCollapseState \_ LeafNode**, qualquer funcionalidade **ExpandCollapse** está atualmente inativa para o controle e as únicas informações que podem ser obtidas usando esse padrão de controle são **ExpandCollapseState**. Se algum objeto filho for subsequentemente adicionado, a **funcionalidade ExpandCollapseState** e **ExpandCollapse** será ativada.
-   [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) refere-se apenas à visibilidade de objetos filho imediatos; ele não se refere à visibilidade de todos os objetos descendentes.
-   [**A funcionalidade IExpandCollapseProvider::Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) and [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) é específica do controle. A seguir estão exemplos desse comportamento.
    -   O menu Office Personal pode ser um item de menu de três estados ("Expandido", "Recolhido" e "Parcialmente [](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) Expandido") em que o controle especifica o estado a ser adotado quando [**Expandir**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) ou Recolhido é chamado.
    -   Chamar [**Expandir**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) em um item de árvore pode exibir todos os descendentes ou apenas filhos imediatos.
    -   Se chamar [**Expandir**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) ou [**Fechar**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) em um controle manter o estado de seus descendentes, um evento de alteração de visibilidade deverá ser enviado, não um evento de alteração de estado. Se o controle pai não mantiver o estado de seus descendentes quando recolhido, o controle poderá destruir todos os descendentes que não estão mais visíveis e a fim de criar um evento destruído; ou pode alterar o [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) para cada descendente e aumentar um evento de alteração de visibilidade.
-   Para garantir a navegação, é desejável que um objeto seja na árvore microsoft Automação da Interface do Usuário (com o estado de visibilidade apropriado), independentemente de seus pais [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate). Se os descendentes são gerados sob demanda, eles só podem aparecer na árvore Automação da Interface do Usuário depois de serem exibidos pela primeira vez ou apenas enquanto estão visíveis.

## <a name="required-members-for-iexpandcollapseprovider"></a>Membros necessários para **IExpandCollapseProvider**

As propriedades, métodos e eventos a seguir são necessários para implementar a interface [**IExpandCollapseProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)



| Membros necessários                                                                                    | Tipo de membro | Observações                                                                  |
|-----------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------|
| [**Expandcollapsestate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)                   | Propriedade    | Nenhum                                                                   |
| [**Expanda**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)                                             | Método      | Nenhum                                                                   |
| [**Recolher**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)                                         | Método      | Nenhum                                                                   |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Evento       | Esse controle não tem eventos associados; use esse manipulador de eventos genérico. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




