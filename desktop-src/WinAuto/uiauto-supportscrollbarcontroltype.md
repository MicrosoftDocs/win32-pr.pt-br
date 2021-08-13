---
title: Tipo de controle ScrollBar
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle ScrollBar.
ms.assetid: c89ca087-3e93-4e86-ac79-731e3e7a361d
keywords:
- Automação da interface do usuário, suporte para tipo de controle ScrollBar
- Automação da interface do usuário, tipo de controle ScrollBar
- Automação da interface do usuário, estrutura de árvore para tipo de controle ScrollBar
- Automação da interface do usuário, propriedades para tipo de controle ScrollBar
- Automação da interface do usuário, padrões de controle para tipo de controle ScrollBar
- Automação da interface do usuário, eventos para tipo de controle ScrollBar
- estruturas de árvore, tipo de controle ScrollBar
- Propriedades, tipo de controle ScrollBar
- padrões de controle, tipo de controle ScrollBar
- eventos, tipo de controle ScrollBar
- suporte para tipo de controle ScrollBar
- Tipo de controle ScrollBar
- tipos de controle, estrutura de árvore para tipo de controle ScrollBar
- tipos de controle, padrões de controle para o tipo de controle ScrollBar
- tipos de controle, suporte para ScrollBar
- tipos de controle, barra de rolagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a25d0398ca8e094e1dbec5e06eb725f3e9d7edbb5c193fdc3699e166b118142
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413366"
---
# <a name="scrollbar-control-type"></a>Tipo de controle ScrollBar

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **ScrollBar** .

Os controles de barra de rolagem permitem que um usuário Role o conteúdo dentro de um contêiner de janela ou item. O controle consiste em um conjunto de botões e um controle Thumb.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **ScrollBar** . Os requisitos de automação da interface do usuário se aplicam a todos os controles da barra de rolagem em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de barra de rolagem e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Exibição de controle</th>
<th>Exibição de conteúdo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>ScrollBar
<ul>
<li>Botão (0, 2 ou 4)</li>
<li>Thumb (0 ou 1)</li>
</ul></li>
</ul></td>
<td>Não aplicável. (O controle da barra de rolagem não tem conteúdo.)</td>
</tr>
</tbody>
</table>



 

O controle da barra de rolagem pode ter de zero a cinco filhos. Como a subárvore tem mais de um controle de botão, o elemento deve definir um valor de [**\_ AutomationIdPropertyId de UIA**](uiauto-automation-element-propids.md) específico para cada item para torná-lo detectável para ferramentas de teste automatizadas.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de barra de rolagem. Observe que um controle de barra de rolagem nunca tem conteúdo; sua funcionalidade é exposta por meio do padrão de controle [Scroll](uiauto-implementingscroll.md) , que tem suporte no contêiner que está sendo rolado.

Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor         | Observações                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.    | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.    | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | NaN           | O controle da barra de rolagem não tem pontos clicáveis.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ScrollBar** | Esse valor é o mesmo para todas as estruturas. Barras de rolagem que funcionam como controles deslizantes devem usar o tipo de controle [Slider](uiauto-supportslidercontroltype.md) .                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE         | O controle da barra de rolagem nunca é um elemento de conteúdo. Se a barra de rolagem for um controle autônomo, ela deverá atender ao tipo de controle [Slider](uiauto-supportslidercontroltype.md) e retornar [**UIA \_ SliderControlTypeId**](uiauto-controltype-ids.md) para a propriedade [**IUIAutomationElement:: CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (ou [**CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)). |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | O controle da barra de rolagem sempre é incluído na exibição de controle da árvore de automação da interface do usuário.                                                                                                                                                                                                                                                                                                                                                                                        |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.    | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade. Um controle de barra de rolagem raramente leva o foco, mas quando faz isso, o foco deve permanecer no próprio controle de barra de rolagem, não nos botões filho ou no polegar. O usuário deve ser capaz de executar todas as ações de rolagem usando as chaves seta para cima e seta para baixo (ou seta para a direita e seta para a esquerda), ou as teclas PAGE UP e PAGE DOWN.                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO          | As barras de rolagem não têm rótulos.                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.    | Cadeia de caracteres localizada correspondente ao tipo de controle **ScrollBar** . O valor padrão é "barra de rolagem" para en-US ou inglês (Estados Unidos).                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | NULO          | O controle da barra de rolagem não tem elementos de conteúdo e a propriedade [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) não precisa ser definida.                                                                                                                                                                                                                                                                                           |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Consulte observações.    | O controle da barra de rolagem sempre deve expor sua orientação horizontal ou vertical.                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte de todos os controles de barra de rolagem. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).

> [!Note]  
> Quando uma barra de rolagem é usada como um controle apenas para a manipulação do mouse, ela não oferece suporte a padrões de controle. Se ele for usado como um controle deslizante dentro de um aplicativo, ele deverá receber o tipo de controle [Slider](uiauto-supportslidercontroltype.md) .

 



| Padrão de controle                                           | Suporte | Observações                                                                                                                                                                                                                          |
|-----------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Depende | O padrão de controle [RangeValue](uiauto-implementingrangevalue.md) deve ser suportado somente se o padrão de controle [Scroll](uiauto-implementingscroll.md) não tiver suporte no contêiner que tem a barra de rolagem. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)         | Nunca   | O [padrão de](uiauto-implementingscroll.md) controle De rolagem nunca tem suporte direto na barra de rolagem.                                                                                                                     |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles da barra de rolagem são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade. |                                                                                                                            |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                 | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.   |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.             | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Evento de alteração de propriedade RangeValueValuePropertyId.**](uiauto-control-pattern-propids.md)        | Se o controle for compatível com o padrão de controle [RangeValue,](uiauto-implementingrangevalue.md) ele deverá dar suporte a esse evento.   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




