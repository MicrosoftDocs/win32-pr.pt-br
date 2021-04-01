---
title: Diretrizes de implementação do IAccessibleEx
description: O núcleo de automação da interface do usuário da Microsoft pode recuperar todas as propriedades de Acessibilidade Ativa da Microsoft para qualquer objeto acessível exposto por um servidor por meio da interface IAccessible.
ms.assetid: d047127c-1be2-4f34-bb97-330b5509ca0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82403a51e4848142a26194a98dce3922619b06f4
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103639069"
---
# <a name="iaccessibleex-implementation-guidelines"></a>Diretrizes de implementação do IAccessibleEx

O núcleo de automação da interface do usuário da Microsoft pode recuperar todas as propriedades de Acessibilidade Ativa da Microsoft para qualquer objeto acessível exposto por um servidor por meio da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Ao implementar o [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), você deve expor apenas os aspectos da funcionalidade da interface do usuário que não podem ser expostos por meio das propriedades existentes do Microsoft acessibilidade ativa. Este tópico identifica as propriedades de automação da interface do usuário e padrões de controle que representam a funcionalidade da interface do usuário que não tem uma contraparte no Microsoft Acessibilidade Ativa — elas são as propriedades e os padrões de controle que você pode expor em uma implementação de **IAccessibleEx** .

Este tópico contém as seguintes seções:

-   [Propriedades](#properties)
-   [Padrões de controle](#control-patterns)
-   [WinEvents para eventos de alteração da propriedade de automação da interface do usuário](#winevents-for-ui-automation-property-changed-events)
-   [Tópicos relacionados](#related-topics)

## <a name="properties"></a>Propriedades

As propriedades de automação da interface do usuário a seguir não se sobrepõem à funcionalidade do Microsoft Acessibilidade Ativa. Eles podem ser usados em uma implementação de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) :

-   AriaProperties
-   AriaRole
-   AutomationId
-   ClassName
-   ClickablePoint
-   ControllerFor
-   Cultura
-   DescribedBy
-   Fluxos de
-   FrameworkId
-   Iscontem-ContentElement
-   IsControlElement
-   IsDataValidForForm
-   IsRequiredForForm
-   De status
-   ItemType
-   LabeledBy
-   LocalizedControlType
-   Orientation

Embora as propriedades de automação da interface do usuário AcceleratorKey e AccessKey se sobreponham com a propriedade accKeyboardShortcut Microsoft Acessibilidade Ativa, você ainda pode usá-las em uma implementação [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para controles que tenham uma chave de acesso e um acelerador. Da mesma forma, a propriedade de automação de interface do usuário do ControlType se sobrepõe à propriedade accRole do Microsoft Acessibilidade Ativa, mas você ainda pode usá-la em uma implementação **IAccessibleEx** para definir uma função mais específica para um controle.

Como as propriedades do elemento de automação da interface do usuário a seguir já estão cobertas pelas propriedades do Microsoft Acessibilidade Ativa, não é necessário usá-las em uma implementação [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .



| Propriedade de automação da interface do usuário | Equivalente da Microsoft Acessibilidade Ativa                                                                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BoundingRectangle      | accLocation                                                                                                                                                                   |
| HasKeyboardFocus       | accState, [ **\_ \_ foco no sistema de estado**](object-state-constants.md)                                                                                       |
| IsEnabled              | accState, [ **sistema de estado \_ \_ indisponível**](object-state-constants.md)                                                                               |
| IsKeyboardFocusable    | accState, [ **sistema de estado \_ \_ focado**](object-state-constants.md)                                                                                   |
| IsPassword             | accState, [ **sistema de estado \_ \_ protegido**](object-state-constants.md)                                                                                   |
| HelpText               | accHelp                                                                                                                                                                       |
| Nome                   | accName                                                                                                                                                                       |
| NativeWindowHandle     | [**WindowFromAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-windowfromaccessibleobject)                                                                                                              |
| IsOffscreen            | accState, estado do sistema de estado [**\_ \_ invisível do sistema**](object-state-constants.md) / [**fora da \_ \_ tela**](object-state-constants.md) |
| ProcessId              | Fornecido pelo núcleo de automação da interface do usuário                                                                                                                                                |



 

Para qualquer propriedade de automação de interface do usuário sem suporte, sua implementação do método [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) deve definir o parâmetro *pRetVal* como VT \_ vazio e retornar S \_ OK. Retornar [**UIA \_ e \_ sem suporte**](uiauto-error-codes.md) pode fazer com que o proxy de MSAA-to-UIA remova o mapeamento padrão para a propriedade correspondente.

## <a name="control-patterns"></a>Padrões de controle

Os seguintes padrões de controle de automação da interface do usuário não se sobrepõem à funcionalidade do Microsoft Acessibilidade Ativa. Eles podem ser usados em uma implementação de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) :

-   Dock
-   ExpandCollapse
-   Grid
-   GridItem
-   MultipleView
-   RangeValue
-   Rolagem
-   ScrollItem
-   SynchronizedInput
-   Tabela
-   TableItem
-   Transformar

Para os padrões de controle RangeValue e Transform, alguns métodos se sobrepõem entre o padrão de controle de automação da interface do usuário e os métodos de Acessibilidade Ativa da Microsoft. Nesses casos, ambos devem ser implementados. Por exemplo, os métodos [**IAccessible:: get \_ AccValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) e iaccessible do Microsoft acessibilidade ativa [**::p UT \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue) devem ser implementados, como devem ser os métodos Automation [**IRangeValueProvider:: Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) e [**IRangeValueProvider:: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue) da interface do usuário. Internamente, uma implementação pode compartilhar código para eles. Esse requisito para implementar os dois conjuntos evita ter uma implementação parcial de uma interface de padrão e, ao mesmo tempo, manter a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) utilizável por clientes existentes do Microsoft acessibilidade ativa.

Os padrões de controle de automação da interface do usuário a seguir não são necessários quando o controle tem uma das funções descritas abaixo; caso contrário, eles devem ter suporte explícito, se relevante.



| Padrão de controle de automação da interface do usuário | Função do Microsoft Acessibilidade Ativa                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InvokePattern                 | [**Função \_ do Botão de \_ pressão do sistema**](object-roles.md), sistema de [**função \_ \_ MenuItem**](object-roles.md), [**sistema de função \_ \_ BUTTONDROPDOWN**](object-roles.md), [**sistema de função \_ \_ SPLITBUTTON**](object-roles.md)e qualquer outra função em que o valor da Propriedade accDefaultAction não seja **nulo**. |
| SelectionItemPattern          | [**Função \_ do \_ListItem do sistema**](object-roles.md), [ **botão de \_ \_ opção do sistema de funções**](object-roles.md)                                                                                                                                                                                                                                                 |
| SelectionPattern              | [**\_lista do sistema de funções \_**](object-roles.md)                                                                                                                                                                                                                                                                                                                                    |
| TogglePattern                 | [**\_CHECKBUTTON do sistema de função \_**](object-roles.md)                                                                                                                                                                                                                                                                                                                      |
| ValuePattern                  | [**Função \_ do \_Texto do sistema**](object-roles.md) (quando não é somente leitura), [**PROGRESSBAR do \_ sistema \_ de função**](object-roles.md), [**ComboBox do \_ sistema \_ de função**](object-roles.md)e qualquer outra função quando o valor da propriedade accValue não for **nulo**.                                                                            |
| WindowPattern                 | Com suporte automático em Microsoft Win32 **HWND** s de nível superior.                                                                                                                                                                                                                                                                                                                                |



 

## <a name="winevents-for-ui-automation-property-changed-events"></a>WinEvents para eventos de alteração da propriedade de automação da interface do usuário

Além dos eventos definidos para o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), os seguintes identificadores de evento também são definidos e podem ser usados com uma implementação [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) como eventos de alteração de propriedade para propriedades de automação da interface do usuário correspondentes. Eles usam o mesmo mecanismo que os eventos definidos para o **IAccessible**. Para obter mais informações, consulte [WinEvents](winevents-infrastructure.md).



| ID de WinEvent para implementações de IAccessibleEx                                                                                              | ID do WinEvent relacionado do Microsoft Acessibilidade Ativa                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**UIA \_ AriaPropertiesPropertyId**](uiauto-automation-element-propids.md)                                    | Nenhum                                                                                   |
| [**UIA \_ AriaRolePropertyId**](uiauto-automation-element-propids.md)                                                | Nenhum                                                                                   |
| [**UIA \_ ControllerForPropertyId**](uiauto-automation-element-propids.md)                                      | Nenhum                                                                                   |
| [**UIA \_ DescribedByPropertyId**](uiauto-automation-element-propids.md)                                          | Nenhum                                                                                   |
| [**UIA \_ ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) | [**objeto de evento \_ \_ STATECHANGE**](event-constants.md)         |
| [**UIA \_ FlowsToPropertyId**](uiauto-automation-element-propids.md)                                                  | Nenhum                                                                                   |
| [**UIA \_ InputDiscardedEventId**](uiauto-event-ids.md)                                                           | Nenhum                                                                                   |
| [**UIA \_ InputReachedOtherElementEventId**](uiauto-event-ids.md)                                       | Nenhum                                                                                   |
| [**UIA \_ InputReachedTargetEventId**](uiauto-event-ids.md)                                                   | Nenhum                                                                                   |
| [**UIA \_ IsDataValidForFormPropertyId**](uiauto-automation-element-propids.md)                            | Nenhum                                                                                   |
| [**UIA \_ IsEnabledPropertyId**](uiauto-automation-element-propids.md)                                              | [**objeto de evento \_ \_ STATECHANGE**](event-constants.md)         |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                                            | Nenhum                                                                                   |
| [**UIA \_ MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md)                     | Nenhum                                                                                   |
| [**UIA \_ ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md)           | Nenhum                                                                                   |
| [**UIA \_ ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md)         | [**objeto de evento \_ \_ CONTENTSCROLLED**](event-constants.md) |
| [**UIA \_ ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md)                   | Nenhum                                                                                   |
| [**UIA \_ ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md)               | Nenhum                                                                                   |
| [**UIA \_ ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md)             | [**objeto de evento \_ \_ CONTENTSCROLLED**](event-constants.md) |
| [**UIA \_ ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md)                       | Nenhum                                                                                   |
| [**UIA \_ ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md)                                 | [**objeto de evento \_ \_ STATECHANGE**](event-constants.md)         |



 

Para os eventos acima que têm um valor de objeto de evento \_ \_ listado depois deles, e a implementação de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) deve acionar esse evento além do evento alterado listado. Isso permite que o código de cliente **IAccessibleEx** existente continue funcionando, ao mesmo tempo que transmite informações de eventos mais granulares para clientes interessados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[WinEvents](winevents-infrastructure.md)
</dt> <dt>

[A interface IAccessibleEx](iaccessibleex.md)
</dt> </dl>

 

 




