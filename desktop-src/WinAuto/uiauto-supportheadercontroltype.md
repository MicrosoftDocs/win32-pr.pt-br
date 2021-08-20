---
title: Tipo de controle de cabeçalho
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de cabeçalho.
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- Automação da interface do usuário, suporte para tipo de controle de cabeçalho
- Automação da interface do usuário, tipo de controle de cabeçalho
- Automação da interface do usuário, estrutura de árvore para tipo de controle de cabeçalho
- Automação da interface do usuário, propriedades para tipo de controle de cabeçalho
- Automação da interface do usuário, padrões de controle para tipo de controle de cabeçalho
- Automação da interface do usuário, eventos para tipo de controle de cabeçalho
- estruturas de árvore, tipo de controle de cabeçalho
- Propriedades, tipo de controle de cabeçalho
- padrões de controle, tipo de controle de cabeçalho
- eventos, tipo de controle de cabeçalho
- suporte para tipo de controle de cabeçalho
- tipo Controle Cabeçalho
- tipos de controle, estrutura de árvore para tipo de controle de cabeçalho
- tipos de controle, padrões de controle para o tipo de controle de cabeçalho
- tipos de controle, suporte para cabeçalho
- tipos de controle, cabeçalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472a0d7185fa3c2b2dc1dc7593afd106008890bb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482502"
---
# <a name="header-control-type"></a>Tipo de controle de cabeçalho

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **cabeçalho** .

O controle de cabeçalho fornece um contêiner Visual para os rótulos de linhas ou colunas de informações.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **cabeçalho** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de cabeçalho nos quais a plataforma/estrutura da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de cabeçalho e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Cabeçalho<ul><li>HeaderItem (1 ou mais)</li></ul></li></ul> | (Não aplicável) | 




 

Controles de cabeçalho sempre têm um ou mais filhos na exibição de controle da árvore de automação da interface do usuário.

Os controles de cabeçalho têm zero filhos na exibição de conteúdo da árvore de automação da interface do usuário.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de cabeçalho. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor                                                            | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.                                                       | O valor dessa propriedade deve ser exclusivo em todos os controles em um aplicativo.                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.                                                       | O retângulo mais externo que contém o controle inteiro.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.                                                       | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Cabeçalho**                                                       |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE                                                            | O controle de cabeçalho não está incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE                                                             | O controle de cabeçalho é sempre incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                                                                                 |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.                                                       | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO                                                             | Os controles de cabeçalho não têm um rótulo estático.                                                                                                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.                                                       | O valor padrão é "header" para en-US ou inglês (Estados Unidos).                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.                                                       | O controle de cabeçalho precisa de um nome se houver mais de um cabeçalho de linha ou mais de um cabeçalho de coluna. Isso identifica as informações dentro do cabeçalho.                                              |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | **\_ OrientationType Horizontal** ou **OrientationType \_ vertical** | O valor dessa propriedade expõe a posição do controle de cabeçalho — seja um cabeçalho de linha (**OrientationType \_ horizontal**) ou um cabeçalho de coluna (**OrientationType \_ vertical**).                 |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte para controles de cabeçalho. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                         | Suporte | Observações                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depende | Implemente o padrão de controle [Transform](uiauto-implementingtransform.md) se o controle de cabeçalho puder ser redimensionado. |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de cabeçalho são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



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

 

 




