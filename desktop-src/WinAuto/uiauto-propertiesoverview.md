---
title: Visão geral das propriedades de automação da interface do usuário
description: Os provedores de automação da interface do usuário da Microsoft expõem propriedades em elementos de automação de interface As propriedades permitem que os aplicativos cliente recuperem informações sobre controles.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- Automação da interface do usuário, visão geral das propriedades
- Automação da interface do usuário, Propriedades vs. eventos
- Automação da interface do usuário, eventos vs. Propriedades
- Propriedades, sobre
- Propriedades, identificadores
- Propriedades, valores
- Propriedades, eventos
- eventos, propriedades
- Propriedades, dinâmicas
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

Os provedores de automação da interface do usuário da Microsoft expõem propriedades em elementos de automação de interface As propriedades permitem que os aplicativos cliente recuperem informações sobre controles.

A automação da interface do usuário expõe dois tipos diferentes de propriedades: *Propriedades do elemento Automation* e *padrões de controle*. As propriedades do elemento Automation consistem em um conjunto comum de propriedades, como Name, AcceleratorKey e ClassName, que são expostas por todos os elementos de automação da interface do usuário, independentemente do tipo de controle. A maioria das propriedades de elementos de automação são valores estáticos.

As propriedades de padrão de controle são aquelas que são expostas por um controle que dá suporte a um padrão de controle específico. Cada padrão de controle tem um conjunto correspondente de propriedades de padrão de controle que o controle deve expor. Por exemplo, um controle que dá suporte ao padrão de controle de [grade](uiauto-implementinggrid.md) expõe as propriedades ColumnCount e RowCount. A maioria das propriedades de padrão de controle são valores dinâmicos.

Este tópico inclui as seções a seguir.

-   [Identificadores de propriedade](#property-identifiers)
-   [Valores de propriedade](#property-values)
-   [Propriedades e eventos](#properties-and-events)
-   [Tópicos relacionados](#related-topics)

## <a name="property-identifiers"></a>Identificadores de propriedade

Cada propriedade é identificada por um valor numérico **PropertyId** chamado de *identificador de propriedade* (ID). Provedores e clientes usam as IDs numéricas em chamadas de método, como [**IRawElementProviderAdviseEvents:: AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) e [**IUIAutomationElement:: GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) para identificar solicitações de propriedade. Para obter uma descrição detalhada de cada identificador de propriedade de automação de interface do usuário, incluindo o tipo de dados e o valor padrão de cada propriedade, consulte [identificadores de propriedade](uiauto-entry-propids.md).

## <a name="property-values"></a>Valores da propriedade

Todas as propriedades são somente leitura, embora algumas possam ser alteradas usando métodos que atuam no controle, como [**IDockProvider:: SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (Provider) ou [**IUIAutomationDockPattern:: SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (Client).

Para obter informações sobre como recuperar valores de propriedade, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).

## <a name="properties-and-events"></a>Propriedades e eventos

Fortemente associado às propriedades na automação da interface do usuário é o conceito de *eventos de alteração de propriedade*. Para propriedades dinâmicas, um aplicativo cliente precisa de uma maneira de saber que um valor de propriedade foi alterado, para que ele possa atualizar seu cache de informações ou reagir às novas informações de alguma outra maneira. Os clientes podem se registrar para escutar eventos de propriedade alterada em qualquer propriedade.

Os provedores geram eventos quando algo na interface do usuário é alterado. Por exemplo, se uma caixa de seleção for marcada ou desmarcada, um evento de alteração de propriedade será gerado pela implementação do provedor do padrão de controle de [alternância](uiauto-implementingtoggle.md) . Os provedores podem gerar eventos seletivamente, dependendo se algum cliente está ouvindo eventos ou escutando eventos específicos.

Nem todas as alterações de propriedade geram eventos; Isso é inteiramente a implementação do provedor de automação da interface do usuário para o elemento. Por exemplo, os provedores de proxy padrão para caixas de listagem não geram um evento de alteração de propriedade quando a propriedade Selection é alterada. Nesse caso, o aplicativo deve escutar o evento gerado quando a seleção é alterada ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)).

Os clientes escutam eventos assinando-os, conforme descrito em [inscrever-se em eventos de automação da interface do usuário](uiauto-eventsforclients.md). Para eventos de propriedade alterada em particular, os clientes devem implementar [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) e passar a interface para [**IUIAutomation:: AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) ou [**IUIAutomation:: AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[**GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[**GetCachedPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral sobre eventos de automação de interface do usuário](uiauto-eventsoverview.md)
</dt> </dl>

 

 




