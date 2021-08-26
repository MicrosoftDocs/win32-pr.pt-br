---
title: Tipo de controle thumb
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle Thumb.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle Thumb
- Automação da Interface do Usuário, tipo de controle Thumb
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle Thumb
- Automação da Interface do Usuário,propriedades para o tipo de controle Thumb
- Automação da Interface do Usuário, padrões de controle para o tipo de controle Thumb
- Automação da Interface do Usuário, eventos para o tipo de controle Thumb
- estruturas de árvore, tipo de controle Thumb
- propriedades, tipo de controle Thumb
- padrões de controle, tipo de controle Thumb
- eventos, tipo de controle Thumb
- suporte para o tipo de controle Thumb
- tipo de controle Posição
- tipos de controle, estrutura de árvore para o tipo de controle Thumb
- tipos de controle, padrões de controle para o tipo de controle Thumb
- tipos de controle, suporte para Thumb
- tipos de controle, Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea75b39ae0b17be23886823d446667299e5f0df
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478782"
---
# <a name="thumb-control-type"></a>Tipo de controle thumb

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo **de** controle Thumb.

Os controles thumb fornecem a funcionalidade que permite que um controle seja movido (ou arrastado), como um botão de barra de rolagem ou relizado, como um widget de re tamanho de janela. Observe que um controle thumb não fornece a funcionalidade do "arrastar e soltar". Os controles thumb podem receber o foco do mouse, mas não o foco do teclado. O desenvolvedor de controle deve implementar o controle para que ele atue adequadamente (pode ser arrastado ou ressado).

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo **de** controle Thumb. Os Automação da Interface do Usuário aplicativos aplicam todos os controles thumb em que a estrutura/plataforma da interface do usuário Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence a controles de miniatura e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Posição</li></ul> | (Não aplicável) | 




 

Os controles thumb nunca aparecem na exibição de conteúdo porque existem apenas para serem manipulados com um mouse. Eles são expostos por outro padrão [](uiauto-implementingscroll.md) de controle, como o padrão de controle [Scroll,](uiauto-implementingtransform.md) o padrão de controle Transformar ou o padrão de controle [RangeValue,](uiauto-implementingrangevalue.md) com suporte no contêiner do controle thumb.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para controles thumb. Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor      | Observações                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Um ponto dentro da área de cliente visível do controle de thumb.                                                                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Polegar**  |                                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE      | O controle de miniatura nunca é incluído na exibição de conteúdo da árvore Automação da Interface do Usuário dados.                                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de thumb está sempre incluído na exibição de controle da árvore Automação da Interface do Usuário dados.                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade. Um controle thumb poderá receber o foco se ele for usado como um objeto de "controle" para o uso de uma janela ou um painel. Um controle de thumb em um controle deslizante ou barra de rolagem nunca deve receber o foco. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO       | Os controles thumb nunca têm um rótulo.                                                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo **de controle** Thumb. O valor padrão é "thumb" para en-US ou inglês (Estados Unidos).                                                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | NULO       | Como o controle thumb não está disponível na exibição de conteúdo da árvore Automação da Interface do Usuário, ele não requer um nome.                                                                                                                                        |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista Automação da Interface do Usuário padrões de controle necessários para serem suportados por controles thumb. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Padrão de controle                                         | Suporte  | Observações                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Obrigatório | Permite que o controle de thumb seja movido na tela. Como o controle thumb normalmente não pode ser [](uiauto-implementingtransform.md) reessado ou girado, o padrão de controle Transformar dá suporte principalmente à [**função Mover.**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles thumb são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade. |                                                                                                                            |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                 | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.   |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.             | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




