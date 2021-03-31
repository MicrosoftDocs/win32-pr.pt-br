---
title: Invocar padrão de controle
description: Descreve as diretrizes e convenções para implementar o IInvokeProvider, incluindo informações sobre métodos.
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- Automação da interface do usuário, implementando o padrão de controle Invoke
- Automação da interface do usuário, invocar padrão de controle
- Automação da interface do usuário, IInvokeProvider
- IInvokeProvider
- implementação da automação da interface do usuário invocar padrões de controle
- Invocar padrões de controle
- padrões de controle, IInvokeProvider
- padrões de controle, implementando invocação de automação de interface do usuário
- padrões de controle, Invoke
- interfaces, IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963f8d9ccd6ea2a50557ec26a655d5c7f43c6123
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822521"
---
# <a name="invoke-control-pattern"></a>Invocar padrão de controle

Descreve as diretrizes e convenções para implementar o [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), incluindo informações sobre métodos. O padrão de controle **Invoke** é usado para dar suporte a controles que não mantêm o estado quando ativado, mas, em vez disso, inicia ou executa uma ação única e não ambígua.

Os controles que mantêm o estado, como caixas de seleção e botões de opção, devem implementar [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) e [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) , respectivamente. Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IInvokeProvider**](#required-members-for-iinvokeprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **Invoke** , observe as seguintes diretrizes e convenções:

-   Os controles implementam [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) se o mesmo comportamento não é exposto por meio de outro provedor de padrão de controle. Por exemplo, se o método [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) em um controle executar a mesma ação que o método [**IUIAutomationExpandCollapsePattern:: Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) ou [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) , o controle não deverá implementar **IInvokeProvider**.
-   Invocar um controle geralmente é executado clicando ou clicando duas vezes ou pressionando ENTER, um atalho de teclado predefinido ou alguma combinação alternativa de pressionamentos de teclas.
-   O evento **invocado** ([**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)) é gerado em um controle que foi ativado (como uma resposta a um controle que realiza sua ação associada). Se possível, o evento deve ser gerado depois que o controle tiver concluído a ação e retornado sem bloqueio. O evento **chamado** (**UIA \_ Invoke \_ InvokedEventId**) deve ser gerado antes de atender à solicitação **Invoke** nos seguintes cenários:
    -   Não é possível ou prático aguardar até que a ação seja concluída.
    -   A ação requer interação do usuário.
    -   A ação é demorada e fará com que o cliente de chamada seja bloqueado por um período significativo.
-   Se invocar o controle tiver efeitos colaterais significativos, esses efeitos colaterais devem ser expostos por meio da propriedade **HelpText** . Por exemplo, embora [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) não esteja associado à seleção, **Invoke** pode fazer com que outro controle se torne selecionado.
-   Os efeitos de focalizar (ou passar pelo mouse) geralmente não constituem um evento **chamado** . No entanto, os controles que executam uma ação (em oposição a causar um efeito visual) com base no estado de foco devem dar suporte ao padrão de controle **Invoke** .
    > [!Note]  
    > Essa implementação é considerada um problema de acessibilidade se o controle puder ser invocado somente como resultado de um efeito colateral relacionado ao mouse.

     

-   Invocar um controle é diferente de selecionar um item. No entanto, dependendo do controle, a invocação pode fazer com que o item se torne selecionado como um efeito colateral. Por exemplo, invocar um item de lista de documentos do Microsoft Word na pasta meus documentos seleciona o item e abre o documento.
-   Um elemento pode desaparecer da árvore de automação da interface do usuário da Microsoft imediatamente após ser invocado. A solicitação de informações do elemento fornecido pelo retorno de chamada do evento pode falhar como resultado. A solução prévia de informações em cache é a alternativa recomendada.
-   Os controles podem implementar vários padrões de controle. Por exemplo, o controle **cor de preenchimento** na barra de ferramentas do Microsoft Excel implementa os padrões de controle Invoke e [ExpandCollapse](uiauto-implementingexpandcollapse.md) . O padrão de controle ExpandCollapse expõe o menu e o padrão de controle **Invoke** preenche a seleção ativa com a cor escolhida.

## <a name="required-members-for-iinvokeprovider"></a>Membros necessários para **IInvokeProvider**

O método a seguir é necessário para implementar a interface [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) .



| Membros necessários                                | Tipo de membro | Observações                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Chame**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | Método      | **Invoke** é uma chamada assíncrona e deve retornar imediatamente sem bloqueio.<br/> Esse comportamento é particularmente crítico para controles que, direta ou indiretamente, iniciam uma caixa de diálogo modal quando invocada. Qualquer cliente de automação de interface do usuário que atraia o evento permanecerá bloqueado até que a caixa de diálogo modal seja fechada. <br/> |



 

Este padrão de controle não tem propriedades ou eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> <dt>

[**UIA \_ invocar \_ InvokedEventId**](uiauto-event-ids.md)
</dt> </dl>

 

 





