---
title: Tipo de controle StatusBar
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle StatusBar.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle StatusBar
- Automação da Interface do Usuário, tipo de controle StatusBar
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle StatusBar
- Automação da Interface do Usuário, propriedades para o tipo de controle StatusBar
- Automação da Interface do Usuário, padrões de controle para o tipo de controle StatusBar
- Automação da Interface do Usuário, eventos para o tipo de controle StatusBar
- estruturas de árvore, tipo de controle StatusBar
- properties,StatusBar control type
- padrões de controle, tipo de controle StatusBar
- eventos, tipo de controle StatusBar
- suporte para o tipo de controle StatusBar
- StatusBar (tipo de controle)
- tipos de controle, estrutura de árvore para o tipo de controle StatusBar
- tipos de controle, padrões de controle para o tipo de controle StatusBar
- tipos de controle, suporte para StatusBar
- tipos de controle, StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 032c0122bc472a8b2deace8cc48d41926778a11b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473692"
---
# <a name="statusbar-control-type"></a>Tipo de controle StatusBar

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o **tipo de controle StatusBar.**

Um controle de barra de status exibe informações sobre um objeto que está sendo exibido em uma janela de um aplicativo, o componente do objeto ou informações contextuais relacionadas à operação desse objeto em seu aplicativo.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo de **controle StatusBar.** Os Automação da Interface do Usuário requisitos se aplicam a todos os controles de barra de status em que a estrutura/plataforma da interface do usuário Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles da barra de status e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>StatusBar<ul><li>Editar (0 ou mais)</li><li>ProgressBar (0 ou muitos)</li><li>Imagem (0 ou muitos)</li><li>Botão (0 ou muitos)</li></ul></li></ul> | <ul><li>StatusBar<ul><li>Editar (0 ou mais)</li><li>ProgressBar (0 ou muitos)</li><li>Imagem (0 ou muitos)</li><li>Botão (0 ou muitos)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para os controles da barra de status. Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor         | Observações                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações.    | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                                        |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.    | O retângulo delimitante de uma barra de status deve abranger todos os controles contidos nele.                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.    | Com suporte se houver um retângulo delimitador. Se houver áreas dentro do retângulo delimitativo que não são clicáveis e o elemento executar testes de clique especializados, substitua-o e forneça um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **StatusBar** |                                                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | O controle de barra de status sempre é incluído na exibição de conteúdo da Automação da Interface do Usuário de status.                                                                                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE          | O controle de barra de status sempre é incluído na exibição de controle da Automação da Interface do Usuário de status.                                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Depende       | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Depende       | Se um controle de barra de status não estiver visível no momento, ele retornará TRUE para essa propriedade.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO          | O controle de barra de status normalmente não tem um rótulo.                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.    | Cadeia de caracteres localizada correspondente ao **tipo de controle StatusBar.** O valor padrão é "barra de status" para en-US ou inglês (Estados Unidos).                                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.    | O controle de barra de status não precisa de um nome, a menos que mais de um seja usado em um aplicativo. Nesse caso, diferencie cada barra com nomes como "Status da Internet" ou "Status do Aplicativo".                    |
| [**\_OrientationPropertyId da UIA**](uiauto-automation-element-propids.md)                   | Depende       | Um valor que indica a orientação do controle: horizontal ou vertical.                                                                                                                                               |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os Automação da Interface do Usuário de controle necessários para ter suporte para controles de barra de status. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Padrão de controle                               | Suporte  | Observações                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | Opcional | Os controles de barra de status devem dar suporte ao [padrão](uiauto-implementinggrid.md) de controle Grade para que partes individuais possam ser monitoradas e facilmente referenciadas para obter informações. |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles de barra de status são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



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

 

 




