---
title: Tipo de controle AppBar
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle AppBar.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle AppBar
- Automação da Interface do Usuário, tipo de controle AppBar
- Automação da Interface do Usuário, padrões de controle para o tipo de controle AppBar
- padrões de controle, tipo de controle AppBar
- suporte para o tipo de controle AppBar
- Tipo de controle AppBar
- tipos de controle, AppBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc8cf562b125267e9b35239e8490f11ed6ae830
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472882"
---
# <a name="appbar-control-type"></a>Tipo de controle AppBar

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle **AppBar.**

Uma barra de aplicativos é um elemento de interface do usuário que apresenta navegação, comandos e ferramentas para o usuário. Para Windows Store, as barras de aplicativos para aplicativos podem ser exibidas pressionando Windows Chave + Z.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo de controle **AppBar.**

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Eventos necessários](#required-events)
-   [Eventos relevantes](#relevant-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles **AppBar** e descreve o que pode estar contido em cada exibição. **Button** é o elemento mais comum dentro de um **AppBar,** mas outros controles que invocam ações para um aplicativo também são possíveis. Um **AppBar** também pode ter 0 ou mais separadores ( tipo de controle **Separador),** que aparecem na exibição de controle como colocados entre os outros controles. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>AppBar<ul><li>Botão (0 ou muitos)</li><li>Outros controles (0 ou muitos)</li></ul></li></ul> | <ul><li>Não aplicável<ul><li>Botão (0 ou muitos)</li><li>Outros controles (0 ou muitos)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para os controles que implementam o tipo de controle **AppBar.** Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor      | Observações                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                                                |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O valor exposto por essa propriedade deve incluir todos os controles contidos nele.                                                                                                                                    |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **AppBar** |                                                                                                                                                                                                                             |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE      | Um controle de barra de aplicativos não está incluído na exibição de conteúdo da árvore Automação da Interface do Usuário aplicativo.                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Um controle de barra de aplicativos sempre é incluído na exibição de controle da árvore Automação da Interface do Usuário aplicativo.                                                                                                                                        |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte as observações  | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade. Os controles na barra de aplicativos normalmente podem usar o foco do teclado.                                                                                    |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Consulte observações. | O valor dessa propriedade depende se o controle pode ser exibido na tela.                                                                                                                                        |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Nulo       | Os controles da barra de aplicativos geralmente não têm um rótulo.                                                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo **de controle AppBar.** O valor padrão é "barra de aplicativos" para en-US ou inglês (Estados Unidos).                                                                                         |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O controle de barra de aplicativos não precisa de um nome, a menos que um aplicativo tenha mais de uma barra de aplicativos. Se houver mais de uma barra de aplicativos em um aplicativo, use essa propriedade para expor nomes diferenciados, como "Top" ou "Bottom". |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles da barra de aplicativos são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade. |                                                                                                                            |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                 | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.   |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.             | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a>Eventos relevantes

A tabela a seguir lista Automação da Interface do Usuário eventos que são especialmente relevantes para os controles que implementam o tipo de controle **AppBar,** mas não estritamente necessários.



| Automação da Interface do Usuário evento                                                                                 | Observações                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Menu \_ UIAClosedEventId**](uiauto-event-ids.md)                            | As implementações de plataforma podem disparar esse evento quando o controle de barra de aplicativos é fechado. |
| [**Menu \_ UIAOpenedEventId**](uiauto-event-ids.md)                            | As implementações de plataforma podem disparar esse evento quando o controle de barra de aplicativos é aberto. |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Manipulador de eventos alterado por propriedade.                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> <dt>

**Referência**
</dt> <dt>

[**Controle AppBar XAML**](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

[**Objeto WinJS.UI.AppBar**](/previous-versions/windows/apps/br229670(v=win.10))
</dt> </dl>

 

 
