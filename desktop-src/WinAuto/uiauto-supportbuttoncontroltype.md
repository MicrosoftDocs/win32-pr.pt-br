---
title: Tipo de controle de botão
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle Button.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle Button
- Automação da Interface do Usuário, tipo de controle Button
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle Button
- Automação da Interface do Usuário,propriedades para o tipo de controle Button
- Automação da Interface do Usuário, padrões de controle para o tipo de controle Button
- Automação da Interface do Usuário, eventos para o tipo de controle Button
- estruturas de árvore, Tipo de controle de botão
- properties,Button control type
- padrões de controle, Tipo de controle de botão
- eventos, Tipo de controle de botão
- suporte para o tipo de controle Button
- Tipo Controle de botão
- tipos de controle, estrutura de árvore para o tipo de controle Button
- tipos de controle, padrões de controle para o tipo de controle Button
- tipos de controle, suporte para Button
- tipos de controle, Botão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c080018e0fcaf8cd196204f80c61041d03fc1589
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478032"
---
# <a name="button-control-type"></a>Tipo de controle de botão

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o **tipo de controle** Button.

Um botão é um objeto com o que um usuário interage para executar uma ação, como os botões OK e Cancelar em uma caixa de diálogo. O controle de botão é um controle simples a ser expor porque mapeia para um único comando que o usuário deseja concluir.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo **de controle** Button. Os Automação da Interface do Usuário se aplicam a todos os controles de botão em que a estrutura/plataforma da interface do usuário Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de botão e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Botão<ul><li>Imagem (0 ou mais)</li><li>Texto (0 ou mais)</li></ul></li></ul> | <ul><li>Botão</li></ul> | 




 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para os controles que implementam o tipo de controle **Button** (como controles de botão). Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor      | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Um controle de botão normalmente dá suporte a uma tecla de acelerador para permitir que o usuário final execute rapidamente a ação representada pelo botão do teclado.                                             |
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitadores são clicáveis e o elemento executa testes de clique especializados, substitua e forneça um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Botão** |                                                                                                                                                                                                      |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações. | O texto da ajuda deve indicar qual será o resultado final da ativação do botão. Normalmente, esse é o mesmo tipo de informação apresentado por meio de uma dica de ferramenta.                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de botão sempre deve ser conteúdo.                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de botão sempre deve ser um controle.                                                                                                                                                         |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Nulo       | Os controles de botão são rotulados por seu conteúdo.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo **de controle** Button. O valor padrão é "button" para en-US ou inglês (Estados Unidos).                                                                   |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O nome do controle de botão é o texto usado para rotulá-lo. Sempre que uma imagem é usada para rotular um botão, um texto alternativo deve ser fornecido para a propriedade **Nome do** botão.                        |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista Automação da Interface do Usuário padrões de controle necessários para serem suportados por todos os controles de botão. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Propriedade Padrão/Padrão de Controle                                  | Suporte/Valor | Observações                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Consulte observações.    | Quando um botão é hospedado como um filho de um botão de divisão, o botão filho pode dar suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) em vez do padrão de controle [Invocar](uiauto-implementinginvoke.md) ou [Alternar.](uiauto-implementingtoggle.md) O padrão de controle ExpandCollapse pode ser usado para abrir ou fechar um menu ou outra sub-estrutura associada ao elemento de botão. |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Consulte observações.    | Todos os botões devem dar suporte ao [padrão de](uiauto-implementinginvoke.md) controle Invoke ou ao padrão de [controle Alternar,](uiauto-implementingtoggle.md) mas não a ambos. O padrão de controle Invoke deve ter suporte quando o botão executa um comando na solicitação do usuário. Esse comando é mapeado para uma única operação, como Recortar, Copiar, Colar ou Excluir.                                                              |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Consulte observações.    | Todos os botões devem dar suporte ao [padrão de](uiauto-implementinginvoke.md) controle Invoke ou ao padrão de [controle Alternar,](uiauto-implementingtoggle.md) mas não a ambos. O padrão de controle De alternância deverá ter suporte se o botão puder passar por uma série de até três estados. Normalmente, isso é visto como uma opção de ligar/desligar para recursos específicos.                                                                        |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles de botão são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade. |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                     | Se o controle for compatível [com o padrão de](uiauto-implementinginvoke.md) controle Invoke, ele deverá dar suporte a esse evento.           |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                 | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.   |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.             | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ Evento de alteração de propriedade NamePropertyId.**](uiauto-automation-element-propids.md)                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Evento de alteração de propriedade ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)    | Se o controle for compatível com [o padrão de controle Alternar,](uiauto-implementingtoggle.md) ele deverá dar suporte a esse evento.           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




