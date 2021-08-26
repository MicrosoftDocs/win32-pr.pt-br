---
title: Tipo de controle Separator
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle Separator.
ms.assetid: 4987b05a-101e-48b1-aed2-bd7206146f70
keywords:
- Automação da interface do usuário, suporte para tipo de controle Separator
- Automação da interface do usuário, tipo de controle Separator
- Automação da interface do usuário, estrutura de árvore para tipo de controle Separator
- Automação da interface do usuário, propriedades para tipo de controle Separator
- Automação da interface do usuário, padrões de controle para tipo de controle Separator
- Automação da interface do usuário, eventos para tipo de controle Separator
- estruturas de árvore, tipo de controle Separator
- Propriedades, tipo de controle Separator
- padrões de controle, tipo de controle Separator
- eventos, tipo de controle Separator
- suporte para tipo de controle Separator
- tipo de controle Separador
- tipos de controle, estrutura de árvore para tipo de controle Separator
- tipos de controle, padrões de controle para o tipo de controle Separator
- tipos de controle, suporte para separador
- tipos de controle, separador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0685f21565a6252febfadad115c8edf10990995c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477712"
---
# <a name="separator-control-type"></a>Tipo de controle Separator

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **Separator** .

Os controles separadores são usados para dividir visualmente um espaço em duas regiões. Por exemplo, um controle Separator pode ser uma barra que define dois painéis em uma janela. Se o separador puder ser movido, o controle deverá ser exposto como Thumb no tipo de controle.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Separator** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de separador onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles separadores e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Separador</li></ul> | <ul><li>O tipo de controle <strong>Separator</strong> nunca tem conteúdo.</li></ul> | 




 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para controles de separadores. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor         | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.    | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.    | O retângulo mais externo que contém o controle inteiro.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.    | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Caractere** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE         | O controle Separator nunca tem conteúdo.                                                                                                                                                              |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | O controle Separator sempre deve ser um controle.                                                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.    | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO          | O controle Separator não tem um rótulo estático.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.    | Cadeia de caracteres localizada correspondente ao tipo de controle **Separator** . O valor padrão é "separador" para en-US ou inglês (Estados Unidos).                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | ""            | O controle Separator não requer uma propriedade **Name** .                                                                                                                                          |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

O controle Separator não é necessário para dar suporte a nenhum padrão de controle. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles separadores são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                 | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.             | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




