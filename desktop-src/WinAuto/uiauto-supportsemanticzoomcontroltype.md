---
title: Tipo de controle SemanticZoom
description: Este tópico fornece informações sobre Automação da Interface do Usuário suporte para o tipo de controle SemanticZoom.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle SemanticZoom
- Automação da Interface do Usuário, tipo de controle SemanticZoom
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle SemanticZoom
- Automação da Interface do Usuário,propriedades do tipo de controle SemanticZoom
- Automação da Interface do Usuário, padrões de controle para o tipo de controle SemanticZoom
- Automação da Interface do Usuário, eventos para o tipo de controle SemanticZoom
- estruturas de árvore, tipo de controle SemanticZoom
- properties,SemanticZoom control type
- padrões de controle, tipo de controle SemanticZoom
- eventos, tipo de controle SemanticZoom
- suporte para o tipo de controle SemanticZoom
- Tipo de controle SemanticZoom
- tipos de controle, estrutura de árvore para o tipo de controle SemanticZoom
- tipos de controle, padrões de controle para o tipo de controle SemanticZoom
- tipos de controle, suporte para SemanticZoom
- tipos de controle, SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9673c5e9beb0c78ecc7dfccc10b6716d6d3afa3f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467753"
---
# <a name="semanticzoom-control-type"></a>Tipo de controle SemanticZoom

Este tópico fornece informações sobre Automação da Interface do Usuário suporte para o **tipo de controle SemanticZoom.**

Zoom semântico é uma técnica introduzida no Windows 8 para apresentar e navegar por grandes conjuntos de dados ou conteúdos relacionados em uma única exibição, como um álbum de fotos, uma lista de aplicativos ou um livro de endereços. O Zoom Semântico usa dois modos distintos de classificação, ou níveis *de zoom,* para organizar e apresentar o conteúdo. O modo de baixo nível (ou *ampliado*) exibe itens em uma estrutura simples"all-up"; e o modo de alto nível (ou ampliado *)* exibe itens em grupos, permitindo que o usuário navegue rapidamente e navegue pelo conteúdo. Por exemplo, ampliar uma lista de cidades pode mudar para uma lista de estados que contêm essas cidades. Ampliar uma lista de programas pode mudar para uma lista de grupos de programas lógicos.

Para obter mais informações sobre o Zoom Semântico especificamente como usado para aplicativos Windows Store, consulte [Diretrizes para zoom semântico.](/windows/uwp/controls-and-patterns/semantic-zoom)

O modelo de uso para o **tipo de controle SemanticZoom** é incomum, pois ele existe principalmente para acesso programático. Os Automação da Interface do Usuário Microsoft podem monitorar e manipular o controle zoom semântico para controlar o estado ampliado da lista. Os usuários que não estão usando a tecnologia adaptativa normalmente manipulariam o controle de Zoom Semântico diretamente por meio de gestos de toque ou atalhos de teclado.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo de controle **SemanticZoom.** Os Automação da Interface do Usuário se aplicam a todos os controles de Zoom Semântico em que a estrutura/plataforma da interface do usuário Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Propriedades e padrões de controle necessários](#required-control-patterns-and-properties)
-   [Eventos necessários](#required-events)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence ao tipo de controle **SemanticZoom** e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Lista<ul><li>[SemanticZoom]<ul><li>ListItem (0 ou mais)</li></ul></li></ul></li></ul> | <ul><li>Lista<ul><li>ListItem (0 ou mais)</li></ul></li></ul> | 




 

Ou:




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>[SemanticZoom]<ul><li>Lista<ul><li>ListItem (0 ou mais)</li></ul></li></ul></li></ul> | <ul><li>Lista<ul><li>ListItem (0 ou mais)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para os controles que implementam o tipo de **controle SemanticZoom.** Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).




| Automação da Interface do Usuário propriedade | Valor | Observações | 
|------------------------|-------|-------|
| <a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a> | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a> | Consulte observações. | O retângulo mais externo que contém o controle inteiro. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a> | Consulte observações. | Se o controle de lista tiver um ponto clicável (um ponto que pode ser clicado para fazer com que a lista se concentre), esse ponto deverá ser exposto por meio dessa propriedade. Se o valor da propriedade <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> for <strong>TRUE,</strong>tentar recuperar essa propriedade resulta no erro <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> valor. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a> | <strong>SemanticZoom</strong> | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a> | TRUE | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a> | TRUE | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a> | FALSE | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a> | Consulte observações. | Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência a esse controle. | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a> | Consulte observações. | Uma cadeia de caracteres localizada correspondente ao tipo <strong>de controle SemanticZoom.</strong> O valor padrão é "zoom semântico" para en-US ou inglês (Estados Unidos).<blockquote>[!Note]<br />Algumas estruturas concatenaram isso como "semanticzoom".</blockquote><br /> | 
| <a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a> | Consulte observações. | Uma cadeia de caracteres vazia é aceitável ou um nome mais útil pode ser fornecido, desde que não contenha o termo zoom semântico , o que torna a combinação de tipo de controle e nome confuso. | 




 

## <a name="required-control-patterns-and-properties"></a>Propriedades e padrões de controle necessários

A tabela a seguir lista os Automação da Interface do Usuário de controle necessários para serem suportados por todos os controles de Zoom Semântico. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Propriedade Padrão/Padrão de Controle                  | Suporte/Valor | Observações                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Depende       | Os controles de Zoom Semântico [suportam o](uiauto-implementingtoggle.md) padrão de controle Alternar para permitir que o zoom seja habilitado ou desabilitado. [**ToggleState \_ Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponde ao estado simples, all-up e [**ToggleState \_ On**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponde à exibição de alto nível, ampliada. |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles de Zoom Semântico são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade. |                                                                                                                            |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                 | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.   |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.             | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ Evento de alteração de propriedade ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)    |                                                                                                                            |



 

## <a name="remarks"></a>Comentários

Se uma interface do usuário tiver um botão visível para alternar o comportamento do controle zoom semântico, esse botão não deverá ter um tipo de **controle SemanticZoom.** Isso é contra intuitivo, mas o tipo de controle **SemanticZoom** caracteriza o contêiner do conteúdo de zoom, não um botão que controla o zoom. (Esse botão pode ser representado simplesmente como um tipo de controle [Button](uiauto-supportbuttoncontroltype.md) com o padrão [de controle Alternar.)](uiauto-implementingtoggle.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

