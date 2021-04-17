---
title: Recuperando propriedades de elementos de automação da interface do usuário
description: Propriedades em objetos IUIAutomationElement contêm informações sobre elementos de interface do usuário, geralmente controles.
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- clientes, obtendo elementos de automação da interface do usuário
- clientes, elementos de automação da interface do usuário
- clientes, propriedades
- clientes, recuperando Propriedades
- clientes, propriedades de automação da interface do usuário
- Automação da interface do usuário, obtendo elementos
- Automação da interface do usuário, elementos
- Automação da interface do usuário, propriedades
- Automação da interface do usuário, recuperando Propriedades
- Recuperando propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e199522dbefaa2f722a67b0ede57fe910b8ed63b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105797597"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a>Recuperando propriedades de elementos de automação da interface do usuário

Propriedades em objetos [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) contêm informações sobre elementos de interface do usuário, geralmente controles. As propriedades de um elemento são genéricas; ou seja, não é específico para um tipo de controle. As propriedades específicas de controle de um elemento são expostas por suas interfaces de padrão de controle.

As propriedades de automação da interface do usuário da Microsoft são somente leitura. Para definir as propriedades de um controle, você deve usar os métodos do padrão de controle apropriado. Por exemplo, use [**IUIAutomationScrollPattern:: Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) para alterar os valores de posição de uma janela de rolagem.

Para melhorar o desempenho, os valores de propriedade de controles e padrões de controle podem ser armazenados em cache quando os elementos são recuperados. Para obter mais informações, consulte [Caching interface de usuário Propriedades de automação e padrões de controle](uiauto-cachingforclients.md).

Este tópico inclui as seções a seguir.

-   [IDs de propriedade](#property-ids)
-   [Condições de propriedade](#property-conditions)
-   [Recuperando propriedades](#retrieving-properties)
-   [Valores de propriedade padrão](#default-property-values)
-   [Tópicos relacionados](#related-topics)

## <a name="property-ids"></a>IDs de propriedade

Os identificadores de propriedade são definidos em UIAutomationClient. h. Eles são usados para especificar propriedades quando você se inscreve em eventos de propriedade alterada, recupera valores de propriedade e cria condições de propriedade. Os identificadores de propriedade também identificam a propriedade que foi alterada quando [**IUIAutomationPropertyChangedEventHandler:: HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) é chamado.

Para obter uma lista de identificadores de propriedade de automação da interface do usuário, consulte [identificadores de propriedade](uiauto-entry-propids.md).

## <a name="property-conditions"></a>Condições de propriedade

As IDs de propriedade são usadas na construção de objetos [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) que são usados para localizar elementos de automação da interface do usuário. Por exemplo, você pode querer encontrar um elemento que tenha um determinado nome ou todos os controles que estão habilitados. Cada condição de propriedade especifica um identificador de propriedade e o valor que a propriedade deve corresponder.

Para obter mais informações, consulte os seguintes tópicos de referência:

-   [**IUIAutomation::CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [**IUIAutomation::CreatePropertyConditionEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [**IUIAutomationElement:: FindFirst**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [**IUIAutomationElement:: FindAll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a>Recuperando propriedades

Algumas propriedades genéricas e todas as propriedades de padrão de controle estão disponíveis como propriedades na interface de padrão de [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ou de controle e podem ser recuperadas usando um acessador, como [**IUIAutomationElement:: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) ou [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).

Além disso, qualquer propriedade atual ou armazenada em cache (diferente das propriedades de padrão de controle) pode ser recuperada usando um dos seguintes métodos:

-   [**GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [**GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [**GetCachedPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

Esses métodos oferecem um desempenho ligeiramente melhor e o acesso à gama completa de propriedades. No entanto, os valores são retornados em estruturas [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , enquanto os acessadores de propriedade individuais convertem o valor para o tipo apropriado.

## <a name="default-property-values"></a>Valores de propriedade padrão

Se um provedor de automação de interface do usuário não implementar uma propriedade, a automação da interface do usuário poderá fornecer um valor padrão. Por exemplo, se o provedor de um controle não oferecer suporte à propriedade identificada por [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md), a automação da interface do usuário retornará uma cadeia de caracteres vazia. Da mesma forma, se o provedor não oferecer suporte à propriedade identificada por [**UIA \_ IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), a automação da interface do usuário retornará **false**.

A diferença entre [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) e [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (e entre pares semelhantes de métodos) é que o método "ex" pode especificar que nenhum valor padrão seja retornado. Nesse caso, o valor de retorno é uma constante exclusiva especial, indicando que não há suporte para a propriedade. Ao receber esse valor, o aplicativo pode fornecer seu próprio valor ou simplesmente ignorar a propriedade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão geral das propriedades de automação da interface do usuário](uiauto-propertiesoverview.md)
</dt> <dt>

[Identificadores de propriedade](uiauto-entry-propids.md)
</dt> </dl>

 

 