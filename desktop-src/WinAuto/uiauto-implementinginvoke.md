---
title: Padrão de controle Invoke
description: Descreve diretrizes e convenções para implementar IInvokeProvider, incluindo informações sobre métodos.
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- Automação da Interface do Usuário, implementando o padrão de controle Invoke
- Automação da Interface do Usuário, invocar padrão de controle
- Automação da Interface do Usuário,IInvokeProvider
- IInvokeProvider
- implementando padrões Automação da Interface do Usuário de controle Invoke
- Invocar padrões de controle
- padrões de controle, IInvokeProvider
- padrões de controle, implementando Automação da Interface do Usuário Invoke
- padrões de controle, Invocar
- interfaces,IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fbd675a9c30daf0e7b097a706dae9ff0d7767f92f7b785b3098d72ddf6f7cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997936"
---
# <a name="invoke-control-pattern"></a>Padrão de controle Invoke

Descreve diretrizes e convenções para implementar [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), incluindo informações sobre métodos. O **padrão de** controle Invoke é usado para dar suporte a controles que não mantêm o estado quando ativados, mas, em vez disso, iniciam ou executam uma única ação não ambígua.

Os controles que mantêm o estado, como caixas de seleção e botões de rádio, devem implementar [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) e [**ISelectionProvider,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) respectivamente. Para exemplos de controles que implementam esse padrão de controle, consulte [Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IInvokeProvider**](#required-members-for-iinvokeprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão **de controle Invoke,** observe as seguintes diretrizes e convenções:

-   Os controles [**implementarão IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) se o mesmo comportamento não for exposto por meio de outro provedor de padrão de controle. Por exemplo, se o método [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) em um controle executar a mesma ação que o método [**IUIAutomationExpandCollapsePattern::Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) ou [**Collapse,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) o controle não deverá implementar **IInvokeProvider**.
-   A invocação de um controle geralmente é executada clicando ou clicando duas vezes ou pressionando ENTER, um atalho de teclado predefinido ou alguma combinação alternativa de pressionamentos de tecla.
-   O **evento Invocado** ([**UIA Invoke \_ \_ InvokedEventId**](uiauto-event-ids.md)) é acionado em um controle que foi ativado (como uma resposta a um controle que realiza sua ação associada). Se possível, o evento deverá ser gerado depois que o controle tiver concluído a ação e retornado sem bloqueio. O **evento Invocado** (**UIA Invoke \_ \_ InvokedEventId**) deve ser gerado antes de atender à solicitação **Invoke** nos seguintes cenários:
    -   Não é possível ou prático aguardar até que a ação seja concluída.
    -   A ação requer interação do usuário.
    -   A ação é demorada e fará com que o cliente de chamada seja bloqueado por um período significativo.
-   Se invocar o controle tiver efeitos colaterais significativos, esses efeitos colaterais deverão ser expostos por meio da **propriedade HelpText.** Por exemplo, embora [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) não seja associado à seleção, **Invoke** pode fazer com que outro controle se torne selecionado.
-   Efeitos de passar o mouse (ou passar o mouse) geralmente não constituem **um evento** invocado. No entanto, os controles que executam uma ação (em vez de causar um efeito visual) com base no estado de foco devem dar suporte ao padrão de controle **Invoke.**
    > [!Note]  
    > Essa implementação será considerada um problema de acessibilidade se o controle puder ser invocado apenas como resultado de um efeito colateral relacionado ao mouse.

     

-   Invocar um controle é diferente de selecionar um item. No entanto, dependendo do controle, invocá-lo pode fazer com que o item seja selecionado como um efeito colateral. Por exemplo, invocar um item Microsoft Word de lista de documentos na pasta Meus Documentos seleciona o item e abre o documento.
-   Um elemento pode desaparecer da árvore de Automação da Interface do Usuário Microsoft imediatamente após ser invocado. A solicitação de informações do elemento fornecido pelo retorno de chamada de evento pode falhar como resultado. Buscar previamente as informações armazenadas em cache é a solução alternativa recomendada.
-   Os controles podem implementar vários padrões de controle. Por exemplo, o **controle Cor** de Preenchimento na barra de ferramentas Microsoft Excel implementa os padrões de controle Invoke e [ExpandCollapse.](uiauto-implementingexpandcollapse.md) O padrão de controle ExpandCollapse expõe o menu e o padrão de controle **Invoke** preenche a seleção ativa com a cor escolhida.

## <a name="required-members-for-iinvokeprovider"></a>Membros necessários para **IInvokeProvider**

O método a seguir é necessário para implementar a interface [**IInvokeProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)



| Membros necessários                                | Tipo de membro | Observações                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | Método      | **Invoke** é uma chamada assíncrona e deve retornar imediatamente sem bloqueio.<br/> Esse comportamento é particularmente crítico para controles que, direta ou indiretamente, iniciam uma caixa de diálogo modal quando invocadas. Qualquer Automação da Interface do Usuário cliente que bloqueou o evento permanecerá bloqueado até que a caixa de diálogo modal seja fechada. <br/> |



 

Esse padrão de controle não tem propriedades ou eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> <dt>

[**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)
</dt> </dl>

 

 





