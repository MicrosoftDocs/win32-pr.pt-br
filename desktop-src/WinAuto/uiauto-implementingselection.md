---
title: Padrão de controle de seleção
description: Descreve as diretrizes e convenções para implementar o ISelectionProvider, incluindo informações sobre propriedades, métodos e eventos.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- Automação da interface do usuário, implementando padrão de controle de seleção
- Automação da interface do usuário, padrão de controle de seleção
- Automação da interface do usuário, ISelectionProvider
- ISelectionProvider
- Implementando padrões de controle de seleção de automação de IU
- Padrões de controle de seleção
- padrões de controle, ISelectionProvider
- padrões de controle, implementando a seleção de automação da interface do usuário
- padrões de controle, seleção
- interfaces, ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6950302373494f307c91c0aadaeab1db0132a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005577"
---
# <a name="selection-control-pattern"></a>Padrão de controle de seleção

Descreve as diretrizes e convenções para implementar o [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), incluindo informações sobre propriedades, métodos e eventos. O padrão de controle **Selection** é usado para dar suporte a controles que atuam como contêineres para uma coleção de itens filho selecionáveis. Os filhos deste elemento devem implementar [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **ISelectionProvider**](#required-members-for-iselectionprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle de **seleção** , observe as seguintes diretrizes e convenções:

-   Controles que implementam [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) permitem que um ou vários itens filho sejam selecionados. Por exemplo, caixas de listagem, exibições de lista e exibições de árvore dão suporte a várias seleções, enquanto caixas de combinação, controles deslizantes e grupos de botões de opção suportam seleção única.
-   Controles que têm um intervalo mínimo, máximo e contínuo, como o controle deslizante de **volume** de um player de mídia, devem implementar [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) em vez de [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).
-   Controles de seleção única que gerenciam controles filho que implementam [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), como o controle deslizante de **resolução de tela** na caixa de diálogo **Propriedades de exibição** para Windows, ou o controle seleção de **seletor de cor** do Microsoft Word (consulte a imagem a seguir), deve implementar [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); seus filhos devem implementar [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) e [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

    ![imagem mostrando um exemplo de mapeamento de cadeia de caracteres de amostra de cor](images/uia-valuepattern-colorpicker.jpg)

-   Os menus não dão suporte ao padrão de controle **Selection** . Se você estiver trabalhando com itens de menu que incluem elementos gráficos e texto (como os itens do **painel de visualização** no menu **Exibir** no Microsoft Outlook) e precisar transmitir o estado, você deve implementar [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).

## <a name="required-members-for-iselectionprovider"></a>Membros necessários para **ISelectionProvider**

As propriedades, os métodos e os eventos a seguir são necessários para implementar a interface [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .



| Membros necessários                                                                                | Tipo de membro | Observações                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | Propriedade    | Nenhum                                                                        |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | Propriedade    | Nenhum                                                                        |
| [**Getseleções**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | Método      | Nenhum                                                                        |
| [**\_InvalidatedEventId de seleção de UIA \_**](uiauto-event-ids.md) | Evento       | Gerar esse evento quando uma seleção em um contêiner tiver sido alterada significativamente. |



 

As propriedades [**ISelectionProvider:: IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) e [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) podem ser dinâmicas. Por exemplo, o estado inicial de um controle pode não ter nenhum item selecionado por padrão, indicando que **IsSelectionRequired** é false. No entanto, depois que um item é selecionado, o controle sempre deve ter pelo menos um item selecionado. Da mesma forma, em casos raros, um controle pode permitir que vários itens sejam selecionados na inicialização, mas posteriormente permitir que apenas seleções únicas sejam feitas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Padrão de controle SelectionItem](uiauto-implementingselectionitem.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




