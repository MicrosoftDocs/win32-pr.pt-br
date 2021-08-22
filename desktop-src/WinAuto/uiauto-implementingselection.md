---
title: Padrão de controle de seleção
description: Descreve diretrizes e convenções para implementar ISelectionProvider, incluindo informações sobre propriedades, métodos e eventos.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- Automação da Interface do Usuário, implementando o padrão de controle Seleção
- Automação da Interface do Usuário, Padrão de controle de seleção
- Automação da Interface do Usuário,ISelectionProvider
- ISelectionProvider
- implementando padrões Automação da Interface do Usuário controle Seleção
- Padrões de controle de seleção
- padrões de controle, ISelectionProvider
- padrões de controle, implementando Automação da Interface do Usuário Seleção
- padrões de controle, Seleção
- interfaces,ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d0578dcdcfa9d381272afaa474338a54caa1f4b17989f2461f9aec5086bc18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098316"
---
# <a name="selection-control-pattern"></a>Padrão de controle de seleção

Descreve diretrizes e convenções para implementar [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), incluindo informações sobre propriedades, métodos e eventos. O **padrão de** controle Seleção é usado para dar suporte a controles que atuam como contêineres para uma coleção de itens filho selecionáveis. Os filhos desse elemento devem implementar [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

Para exemplos de controles que implementam esse padrão de controle, consulte [Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **ISelectionProvider**](#required-members-for-iselectionprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão **de controle** Seleção, observe as seguintes diretrizes e convenções:

-   Os controles [**que implementam ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) permitem que itens individuais ou vários filhos sejam selecionados. Por exemplo, caixas de listagem, exibições de lista e exibições de árvore são suportadas por várias seleções, enquanto caixas de combinação, controles deslizantes e grupos de botões de botão de rádio suportam seleção única.
-   Os controles que têm um intervalo mínimo, máximo e contínuo, como o controle deslizante **volume** de um player de mídia, devem implementar [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) em vez [**de ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).
-   Controles de seleção única que gerenciam controles filho que implementam [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), como o controle deslizante resolução de tela na caixa de diálogo Propriedades de Vídeo para Windows ou o controle de seleção Seletor de Cor do Microsoft Word (consulte a imagem  **a** seguir), devem implementar [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider);  seus filhos devem implementar [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) e [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).

    ![imagem mostrando um exemplo de mapeamento de cadeia de caracteres de amostra de cor](images/uia-valuepattern-colorpicker.jpg)

-   Os menus não são suportados pelo **padrão de controle** Seleção. Se você estiver trabalhando com itens de menu que  incluem gráficos e texto (como os itens do Painel de Visualização no **menu** Exibir no Microsoft Outlook) e precisar transmitir o estado, implemente [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).

## <a name="required-members-for-iselectionprovider"></a>Membros necessários para **ISelectionProvider**

As propriedades, métodos e eventos a seguir são necessários para implementar a interface [**ISelectionProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)



| Membros necessários                                                                                | Tipo de membro | Observações                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | Propriedade    | Nenhum                                                                        |
| [**Isselectionrequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | Propriedade    | Nenhum                                                                        |
| [**Getselection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | Método      | Nenhum                                                                        |
| [**Seleção de UIA \_ \_ InvalidatedEventId**](uiauto-event-ids.md) | Evento       | Aumente esse evento quando uma seleção em um contêiner tiver sido alterada significativamente. |



 

As [**propriedades ISelectionProvider::IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) e [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) podem ser dinâmicas. Por exemplo, o estado inicial de um controle pode não ter nenhum item selecionado por padrão, indicando que **IsSelectionRequired** é false. No entanto, depois que um item é selecionado, o controle sempre deve ter pelo menos um item selecionado. Da mesma forma, em casos raros, um controle pode permitir que vários itens sejam selecionados na inicialização, mas posteriormente permitem que apenas seleções únicas sejam feitas.

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

 

 




