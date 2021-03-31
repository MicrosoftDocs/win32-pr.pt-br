---
title: Padrão de controle ExpandCollapse
description: Descreve as diretrizes e convenções para implementar o IExpandCollapseProvider, incluindo informações sobre propriedades, métodos e eventos.
ms.assetid: 0ffc26c3-8696-44f9-b463-902a69e06d21
keywords:
- Automação da interface do usuário, implementando o padrão de controle ExpandCollapse
- Automação da interface do usuário, padrão de controle ExpandCollapse
- Automação da interface do usuário, IExpandCollapseProvider
- IExpandCollapseProvider
- Implementando padrões de controle ExpandCollapse de automação da interface do usuário
- Padrões de controle ExpandCollapse
- padrões de controle, IExpandCollapseProvider
- padrões de controle, implementando a automação da interface do usuário ExpandCollapse
- padrões de controle, ExpandCollapse
- interfaces, IExpandCollapseProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bd28ddcc201dcff0a4811a1eb8e04670f93091
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005282"
---
# <a name="expandcollapse-control-pattern"></a>Padrão de controle ExpandCollapse

Descreve as diretrizes e convenções para implementar o [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider), incluindo informações sobre propriedades, métodos e eventos. O padrão de controle **ExpandCollapse** é usado para dar suporte a controles que expandem visualmente para exibir mais conteúdo e recolher para ocultar o conteúdo.

Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IExpandCollapseProvider**](#required-members-for-iexpandcollapseprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **ExpandCollapse** , observe as seguintes diretrizes e convenções:

-   Os controles de agregação, criados com objetos filho que fornecem a interface do usuário com funcionalidade de expandir/recolher, devem dar suporte ao padrão de controle **ExpandCollapse** , enquanto seus elementos filho não. Por exemplo, um controle de caixa de combinação é criado com uma combinação de controles de caixa de listagem, botões e edição, mas é apenas a caixa de combinação pai que deve dar suporte ao padrão de controle **ExpandCollapse** .
    > [!Note]  
    > Uma exceção é o controle de menu, que é uma agregação de objetos de item de menu individuais. Os objetos de item de menu podem dar suporte ao padrão de controle **ExpandCollapse** , mas o controle de menu pai não pode. Uma exceção semelhante se aplica aos controles de item de árvore e árvore.

     

-   Quando [**IExpandCollapseProvider:: ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) de um controle é definido como **ExpandCollapseState \_ leafnode**, qualquer funcionalidade de **ExpandCollapse** está inativa no momento para o controle e as únicas informações que podem ser obtidas usando esse padrão de controle são o **ExpandCollapseState**. Se qualquer objeto filho for adicionado posteriormente, as alterações de **ExpandCollapseState** e a funcionalidade **ExpandCollapse** serão ativadas.
-   [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) refere-se apenas à visibilidade de objetos filho imediatos; Ele não se refere à visibilidade de todos os objetos descendentes.
-   [**IExpandCollapseProvider:: expandir**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) e [**recolher**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) funcionalidade é específico do controle. Veja a seguir exemplos desse comportamento.
    -   O menu pessoal do Office pode ser um item de menu de três Estados ("expandido", "recolhido" e "PartiallyExpanded") em que o controle Especifica o estado a ser adotado quando [**expandir**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) ou [**recolher**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) é chamado.
    -   Chamar [**expandir**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) em um item de árvore pode exibir todos os descendentes ou apenas filhos imediatos.
    -   Se chamar [**expandir**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) ou [**recolher**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) em um controle mantiver o estado de seus descendentes, um evento de alteração de visibilidade deverá ser enviado, não um evento de alteração de estado. Se o controle pai não mantiver o estado de seus descendentes quando recolhido, o controle poderá destruir todos os descendentes que não estão mais visíveis e gerar um evento destruído; ou pode alterar o [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) para cada descendente e gerar um evento de alteração de visibilidade.
-   Para garantir a navegação, é desejável que um objeto esteja na árvore de automação da interface do usuário da Microsoft (com o estado de visibilidade apropriado), independentemente de seus pais [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate). Se os descendentes forem gerados sob demanda, eles só poderão aparecer na árvore de automação da interface do usuário depois de serem exibidos pela primeira vez ou somente enquanto estiverem visíveis.

## <a name="required-members-for-iexpandcollapseprovider"></a>Membros necessários para **IExpandCollapseProvider**

As propriedades, os métodos e os eventos a seguir são necessários para implementar a interface [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) .



| Membros necessários                                                                                    | Tipo de membro | Observações                                                                  |
|-----------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------|
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)                   | Propriedade    | Nenhum                                                                   |
| [**Expanda**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)                                             | Método      | Nenhum                                                                   |
| [**Recolher**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)                                         | Método      | Nenhum                                                                   |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Evento       | Este controle não tem eventos associados; Use este manipulador de eventos genérico. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




