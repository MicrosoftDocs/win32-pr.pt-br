---
title: Tipo de controle de hiperlink
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle HyperLink.
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- Automação da interface do usuário, suporte para tipo de controle de hiperlink
- Automação da interface do usuário, tipo de controle de hiperlink
- Automação da interface do usuário, estrutura de árvore para tipo de controle de hiperlink
- Automação da interface do usuário, propriedades para tipo de controle de hiperlink
- Automação da interface do usuário, padrões de controle para tipo de controle de hiperlink
- Automação da interface do usuário, eventos para tipo de controle de hiperlink
- estruturas de árvore, tipo de controle de hiperlink
- Propriedades, tipo de controle hiperlink
- padrões de controle, tipo de controle de hiperlink
- eventos, tipo de controle de hiperlink
- suporte para tipo de controle de hiperlink
- tipo de controle Hiperlink
- tipos de controle, estrutura de árvore para tipo de controle de hiperlink
- tipos de controle, padrões de controle para tipo de controle de hiperlink
- tipos de controle, suporte para hiperlink
- tipos de controle, hiperlink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52735983429a60061a548bf4cce71b7b128f4b6e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466953"
---
# <a name="hyperlink-control-type"></a>Tipo de controle de hiperlink

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **Hyperlink** .

Os controles de hiperlink criam links que permitem que os usuários naveguem dentro da mesma página ou de uma página para outra.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Hyperlink** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de hiperlink em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de hiperlink e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Hyperlink</li></ul> | <ul><li>Hyperlink</li></ul> | 




 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de hiperlink. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor         | Observações                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.    | O valor dessa propriedade deve ser exclusivo em todos os controles em um aplicativo.                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.    | O retângulo mais externo que contém o controle inteiro.                                                                                 |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.    | O ponto clicável do controle de hiperlink deve ser um ponto que inicia o hiperlink se clicado com um ponteiro do mouse.                     |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Hiperlink** |                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | O controle HyperLink é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | O controle HyperLink é sempre incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.    | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações.    | Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência a esse controle.                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.    | Cadeia de caracteres localizada correspondente ao tipo de controle de **hiperlink** . O valor padrão é "HYPERLINK" para en-US ou inglês (Estados Unidos). |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.    | O nome do controle de hiperlink é o texto que é exibido na tela como sublinhado.                                                  |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário para os quais os controles de hiperlink precisam dar suporte. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                  | Suporte/valor                | Observações                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | Obrigatório                     | Todos os controles de hiperlink devem dar suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) .                                                                                                                                                       |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Depende                      | Os controles de hiperlink devem dar suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) quando o link contém informações que podem ser usadas e significativas para o usuário.                                                                              |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | Por exemplo, "https://www..". | Uma URL para um endereço de Internet ou intranet é um exemplo de um hiperlink que contém informações que são significativas para o usuário. Um link programático, no entanto, é significativo apenas para um aplicativo e não é recomendado para a propriedade **Value** . |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de hiperlink são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_ invocar \_ InvokedEventId**](uiauto-event-ids.md)                                                     |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                 | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.             | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a>Comentários

O tipo de controle Hiperlink deve ser aplicado somente a um objeto que, quando clicado, faz com que a navegação ocorra; ele não deve ser aplicado ao contêiner do hiperlink. Por exemplo, somente os "pontos de acesso" clicáveis dentro de um mapa de imagem devem ter o **tipo de controle Hiperlink.** O mesmo é verdadeiro para hiperlinks em um campo de texto ou contêiner de documento. Nesse caso, somente o texto ou a imagem de hiperlink deve ter o tipo de controle **Hiperlink,** não o contêiner.

O [padrão de](uiauto-implementingtextandtextrange.md) controle De texto é ideal para dar suporte a hiperlinks inseridos em elementos de texto ou documento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




