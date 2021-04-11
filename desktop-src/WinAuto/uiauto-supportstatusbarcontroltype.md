---
title: Tipo de controle StatusBar
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle StatusBar.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- Automação da interface do usuário, suporte para tipo de controle StatusBar
- Automação da interface do usuário, tipo de controle StatusBar
- Automação da interface do usuário, estrutura de árvore para tipo de controle StatusBar
- Automação da interface do usuário, propriedades para tipo de controle StatusBar
- Automação da interface do usuário, padrões de controle para tipo de controle StatusBar
- Automação da interface do usuário, eventos para tipo de controle StatusBar
- estruturas de árvore, tipo de controle StatusBar
- Propriedades, tipo de controle StatusBar
- padrões de controle, tipo de controle StatusBar
- eventos, tipo de controle StatusBar
- suporte para tipo de controle StatusBar
- StatusBar (tipo de controle)
- tipos de controle, estrutura de árvore para tipo de controle StatusBar
- tipos de controle, padrões de controle para o tipo de controle StatusBar
- tipos de controle, suporte para StatusBar
- tipos de controle, StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ace64d34429a6d381dfdef2d99d82a3693fca2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292465"
---
# <a name="statusbar-control-type"></a>Tipo de controle StatusBar

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **StatusBar** .

Um controle barra de status exibe informações sobre um objeto que está sendo exibido em uma janela de um aplicativo, o componente do objeto ou informações contextuais relacionadas à operação desse objeto em seu aplicativo.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **StatusBar** . Os requisitos de automação da interface do usuário se aplicam a todos os controles da barra de status, em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence aos controles da barra de status e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>StatusBar
<ul>
<li>Editar (0 ou mais)</li>
<li>ProgressBar (0 ou muitos)</li>
<li>Imagem (0 ou muitos)</li>
<li>Botão (0 ou muitos)</li>
</ul></li>
</ul></td>
<td><ul>
<li>StatusBar
<ul>
<li>Editar (0 ou mais)</li>
<li>ProgressBar (0 ou muitos)</li>
<li>Imagem (0 ou muitos)</li>
<li>Botão (0 ou muitos)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles da barra de status. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor         | Observações                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.    | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                        |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.    | O retângulo delimitador de uma barra de status deve abranger todos os controles contidos nela.                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.    | Com suporte se houver um retângulo delimitador. Se houver áreas dentro do retângulo delimitador que não são clicáveis, e o elemento executar um teste de clique especializado, substitua isso e forneça um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **StatusBar** |                                                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | O controle da barra de status é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | O controle da barra de status é sempre incluído na exibição de controle da árvore de automação da interface do usuário.                                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Depende       | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Depende       | Se um controle da barra de status não estiver visível no momento, ele retornará TRUE para essa propriedade.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO          | O controle da barra de status normalmente não tem um rótulo.                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.    | Cadeia de caracteres localizada correspondente ao tipo de controle **StatusBar** . O valor padrão é "barra de status" para en-US ou inglês (Estados Unidos).                                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.    | O controle da barra de status não precisa de um nome, a menos que mais de um seja usado em um aplicativo. Nesse caso, diferencie cada barra com nomes como "status da Internet" ou "status do aplicativo".                    |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Depende       | Um valor que indica a orientação do controle: horizontal ou vertical.                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para ter suporte para controles de barra de status. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                               | Suporte  | Observações                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | Opcional | Os controles da barra de status devem dar suporte ao padrão de controle de [grade](uiauto-implementinggrid.md) para que partes individuais possam ser monitoradas e facilmente referenciadas por informações. |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de barra de status são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                   | Observações                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId. |                                                                                   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                 | Se o controle oferecer suporte à propriedade **IsEnabled** , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.             | Se o controle oferecer suporte à propriedade **IsOffscreen** , ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a>Comentários

Recomendamos que os controles de edição sejam usados como elementos de grade filho em uma barra de status. O uso de controles de edição facilita a associação do objetivo do campo status com seu valor usando o nome do elemento e a propriedade Value. Como os controles de texto não devem dar suporte ao padrão de controle de **valor** , eles não devem ser usados como elementos de grade filho.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




