---
title: Visão geral das propriedades de automação da interface do usuário
description: Os provedores Automação da Interface do Usuário Microsoft expõem propriedades em Automação da Interface do Usuário elementos. As propriedades permitem que os aplicativos cliente recuperem informações sobre controles.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- Automação da Interface do Usuário,visão geral das propriedades
- Automação da Interface do Usuário, propriedades versus eventos
- Automação da Interface do Usuário, eventos versus propriedades
- propriedades, sobre
- propriedades, identificadores
- propriedades, valores
- propriedades, eventos
- eventos, propriedades
- properties,dynamic
- propriedades dinâmicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58267fae50fe71c320b334c35b8da7831657e00bdd1b222db596addd40f3afef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745026"
---
# <a name="ui-automation-properties-overview"></a>Visão geral das propriedades de automação da interface do usuário

Os provedores Automação da Interface do Usuário Microsoft expõem propriedades em Automação da Interface do Usuário elementos. As propriedades permitem que os aplicativos cliente recuperem informações sobre controles.

Automação da Interface do Usuário expõe dois tipos diferentes de propriedades: propriedades do *elemento* de automação e o padrão *de controle se apropriado.* As propriedades do elemento de automação consistem em um conjunto comum de propriedades, como Name, AcceleratorKey e ClassName, que são expostas por todos os Automação da Interface do Usuário, independentemente do tipo de controle. A maioria das propriedades do elemento de automação são valores estáticos.

As propriedades do padrão de controle são aquelas expostas por um controle que dá suporte a um padrão de controle específico. Cada padrão de controle tem um conjunto correspondente de propriedades de padrão de controle que o controle deve expor. Por exemplo, um controle que dá suporte ao [padrão de controle Grid](uiauto-implementinggrid.md) expõe as propriedades ColumnCount e RowCount. A maioria das propriedades de padrão de controle são valores dinâmicos.

Este tópico inclui as seções a seguir.

-   [Identificadores de propriedade](#property-identifiers)
-   [Valores da propriedade](#property-values)
-   [Propriedades e eventos](#properties-and-events)
-   [Tópicos relacionados](#related-topics)

## <a name="property-identifiers"></a>Identificadores de propriedade

Cada propriedade é identificada por **um valor numérico PROPERTYID** chamado ID (identificador *de* propriedade). Provedores e clientes usam as IDs numéricas em chamadas de método, como [**IRawElementProviderAdviseEvents::AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) [**e IUIAutomationElement::GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) para identificar solicitações de propriedade. Para uma descrição detalhada de cada Automação da Interface do Usuário identificador de propriedade, incluindo o tipo de dados e o valor padrão de cada propriedade, consulte [Identificadores de propriedade](uiauto-entry-propids.md).

## <a name="property-values"></a>Valores da propriedade

Todas as propriedades são somente leitura, embora algumas possam ser alteradas usando métodos que atuam no controle, como [**IDockProvider::SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (provedor) ou [**IUIAutomationDockPattern::SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (cliente).

Para obter informações sobre como recuperar valores de propriedade, consulte Recuperando propriedades [de Automação da Interface do Usuário Elementos](uiauto-propertiesforclients.md).

## <a name="properties-and-events"></a>Propriedades e eventos

Estreitamente associado às propriedades no Automação da Interface do Usuário é o conceito de *eventos alterados por propriedade.* Para propriedades dinâmicas, um aplicativo cliente precisa de uma maneira de saber que um valor da propriedade foi alterado, para que ele possa atualizar seu cache de informações ou reagir às novas informações de alguma outra maneira. Os clientes podem se registrar para escutar eventos alterados por propriedade em qualquer propriedade.

Os provedores adem eventos quando algo na interface do usuário muda. Por exemplo, se uma caixa de seleção estiver marcada ou desalocada, um evento de propriedade alterada será gerado pela implementação do provedor do padrão de controle [Alternar.](uiauto-implementingtoggle.md) Os provedores podem agar eventos seletivamente, dependendo se algum cliente está escutando eventos ou escutando eventos específicos.

Nem todas as alterações de propriedade adem eventos; que depende totalmente da implementação do provedor Automação da Interface do Usuário para o elemento . Por exemplo, os provedores de proxy padrão para caixas de listagem não ativas um evento de propriedade alterada quando a propriedade Selection é alterada. Nesse caso, o aplicativo deve escutar o evento gerado quando a seleção for mudada ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)).

Os clientes escutam eventos assinando-os, conforme descrito em [Assinando](uiauto-eventsforclients.md)Automação da Interface do Usuário Eventos . Para eventos alterados por propriedade em particular, os clientes devem implementar [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) e passar a interface para [**IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) ou [**IUIAutomation::AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**Getcurrentpropertyvalue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[**Getcachedpropertyvalue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[**GetCachedPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral sobre eventos de automação de interface do usuário](uiauto-eventsoverview.md)
</dt> </dl>

 

 




