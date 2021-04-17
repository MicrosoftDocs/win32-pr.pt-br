---
title: Apêndice G Acessibilidade Ativa ponte à automação da interface do usuário
description: Este apêndice contém informações sobre a ponte do Microsoft Acessibilidade Ativa.
ms.assetid: f19036c7-5a18-4faa-a98d-564e5e63a94f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df5fdc1ebc4d6e17781e383463974f78bb9334aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105780151"
---
# <a name="appendix-g-active-accessibility-bridge-to-ui-automation"></a>Apêndice G: Acessibilidade Ativa ponte à automação da interface do usuário

Este apêndice contém informações sobre a ponte do Microsoft Acessibilidade Ativa. A ponte Acessibilidade Ativa permite que os aplicativos que implementam o Microsoft Acessibilidade Ativa acessem aplicativos que implementam a automação da interface do usuário da Microsoft. Ao unir o Microsoft Acessibilidade Ativa e a automação da interface do usuário, os clientes baseados no Microsoft Acessibilidade Ativa, como um screenreader no Windows XP, podem interagir programaticamente com provedores baseados na automação da interface do usuário, como um aplicativo Windows Presentation Foundation (WPF). Ele faz parte da API principal de automação da interface do usuário (UIAutomationCore.dll).

O Acessibilidade Ativa Bridge mapeia Propriedades de automação da interface do usuário e eventos para os do Microsoft Acessibilidade Ativa. As tabelas a seguir mapeiam os métodos e as propriedades da interface Microsoft Acessibilidade Ativa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para a automação da interface do usuário. Use essas tabelas para determinar as práticas de codificação apropriadas para o desenvolvimento de seu cliente baseado no Microsoft Acessibilidade Ativa.

### <a name="navigation-and-hierarchy-properties"></a>Propriedades de navegação e hierarquia



| Propriedade IAccessible                                                     | Propriedade de automação da interface do usuário          |
|--------------------------------------------------------------------------|---------------------------------|
| [**obter \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | Não implementado                 |
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | Derivado da árvore de automação da interface do usuário |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | Derivado da árvore de automação da interface do usuário |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)              | Não implementado                 |



 

### <a name="descriptive-properties-and-methods"></a>Propriedades e métodos descritivos



| IAccessible                                                                          | Automação da Interface de Usuário                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)            | Consulte os tipos de controle e a tabela accRole para obter detalhes.                                                                                                                                                                                                                                                                     |
| [**obter \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | Consulte os tipos de controle e a tabela accRole para obter detalhes.                                                                                                                                                                                                                                                                     |
| [**obter \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | AccessKeyPropertyor AcceleratorKeyProperty; Se ambos estiverem presentes, AccessKeyproperty terá precedência.                                                                                                                                                                                                                         |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Nome da                                                                                                                                                                                                                                                                                                             |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | ControlTypeproperty. Consulte os tipos de controle e a tabela accRole para obter detalhes.                                                                                                                                                                                                                                                |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | Consulte os tipos de controle e a tabela accRole para obter detalhes.                                                                                                                                                                                                                                                                     |
| [**obter \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)                       | Valorproperty; com suporte em tipos de controle que suportam o padrão de controle de [valor](uiauto-implementingvalue.md) ou o padrão de controle de padrão de controle [RangeValue](uiauto-implementingrangevalue.md) . Os valores RangeValue são consistentes com o comportamento do Microsoft Acessibilidade Ativa (0 a 100). Os itens de valor usam uma cadeia de caracteres. |
| [**colocar \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue)                       | Valorproperty; com suporte em tipos de controle que dão suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) ou ao padrão de controle [RangeValue](uiauto-implementingrangevalue.md)                                                                                                                                      |
| [**obter \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         | HelpTextproperty                                                                                                                                                                                                                                                                                                         |
| [**obter \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           | Não implementado                                                                                                                                                                                                                                                                                                          |
| [**obter \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               | Não implementado                                                                                                                                                                                                                                                                                                          |



 

### <a name="control-types-and-accrole"></a>Tipos de controle e accRole

A função padrão Microsoft Acessibilidade Ativa é [**\_ \_ cliente do sistema de função**](object-roles.md). Se nenhuma ação padrão for encontrada para um tipo de controle, a ponte de Acessibilidade Ativa também usará os seguintes padrões de controle disponíveis: [Invoke](uiauto-implementinginvoke.md), [ExpandCollapse](uiauto-implementingexpandcollapse.md)e [Toggle](uiauto-implementingtoggle.md). Por exemplo, um controle GroupBox não tem nenhuma ação padrão. Se ele der suporte a ExpandCollapse, a ponte de Acessibilidade Ativa usará isso para a ação padrão.



| Tipo de controle de automação da interface do usuário                              | accRole                                                                     | Ação padrão                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------------|----------------------------------------------------------|
| [Botão](uiauto-supportbuttoncontroltype.md)           | [**\_pressão do sistema de funções \_**](object-roles.md)     | Pressione                                                    |
| [Calendário](uiauto-supportcalendarcontroltype.md)       | [**\_cliente do sistema de função \_**](object-roles.md)             | Nenhum                                                     |
| [CheckBox](uiauto-supportcheckboxcontroltype.md)       | [**\_CHECKBUTTON do sistema de função \_**](object-roles.md)   | Marcar/desmarcar (ativar/desativar)                                   |
| [ComboBox](uiauto-supportcomboboxcontroltype.md)       | [**\_ComboBox do sistema de funções \_**](object-roles.md)         | Nenhum                                                     |
| Personalizado                                                  | [**\_cliente do sistema de função \_**](object-roles.md)             | Nenhum                                                     |
| [DataGrid](uiauto-supportdatagridcontroltype.md)       | [**\_lista do sistema de funções \_**](object-roles.md)                 | Nenhum                                                     |
| [DataItem](uiauto-supportdataitemcontroltype.md)       | [**\_ListItem do sistema de funções \_**](object-roles.md)         | Nenhum                                                     |
| [Documento](uiauto-supportdocumentcontroltype.md)       | [**\_documento do sistema de funções \_**](object-roles.md)         | Nenhum                                                     |
| [Editar](uiauto-supporteditcontroltype.md)               | [**\_texto do sistema de função \_**](object-roles.md)                 | Nenhum                                                     |
| [Grupo](uiauto-supportgroupcontroltype.md)             | [**\_agrupamento do sistema de funções \_**](object-roles.md)         | Nenhum                                                     |
| [Cabeçalho](uiauto-supportheadercontroltype.md)           | [**\_lista do sistema de funções \_**](object-roles.md)                 | Nenhum                                                     |
| [HeaderItem](uiauto-supportheaderitemcontroltype.md)   | [**\_COLUMNHEADER do sistema de funções \_**](object-roles.md) | Clique                                                    |
| [Hiperlink](uiauto-supporthyperlinkcontroltype.md)     | [**\_link do sistema de funções \_**](object-roles.md)                 | Salto (mapeia para invocar)                                    |
| [Imagem](uiauto-supportimagecontroltype.md)             | [**\_elemento gráfico do sistema de funções \_**](object-roles.md)           | Nenhum                                                     |
| [Lista](uiauto-supportlistcontroltype.md)               | [**\_lista do sistema de funções \_**](object-roles.md)                 | Nenhum                                                     |
| [Item](uiauto-supportlistitemcontroltype.md)       | [**\_ListItem do sistema de funções \_**](object-roles.md)         | Clicar duas vezes                                             |
| [Menu](uiauto-supportmenucontroltype.md)               | [**\_MENUPOPUP do sistema de função \_**](object-roles.md)       | Nenhum                                                     |
| [MenuBar](uiauto-supportmenubarcontroltype.md)         | [**\_BarraDeMenu do sistema de funções \_**](object-roles.md)           | Nenhum                                                     |
| [MenuItem](uiauto-supportmenuitemcontroltype.md)       | [**sistema de função \_ \_ MenuItem**](object-roles.md)         | Execute ou abra/feche para itens de menu que têm filhos. |
| [Painel](uiauto-supportpanecontroltype.md)               | [**\_painel do sistema de funções \_**](object-roles.md)                 | Nenhum                                                     |
| [ProgressBar](uiauto-supportprogressbarcontroltype.md) | [**\_PROGRESSBAR do sistema de funções \_**](object-roles.md)   | Nenhum                                                     |
| [RadioButton](uiauto-supportradiobuttoncontroltype.md) | [**\_botão de opção sistema de funções \_**](object-roles.md)   | Verificação                                                    |
| [ScrollBar](uiauto-supportscrollbarcontroltype.md)     | [**\_barra de rolagem do sistema de funções \_**](object-roles.md)       | Nenhum                                                     |
| [Controle deslizante](uiauto-supportslidercontroltype.md)           | [**\_controle deslizante do sistema de funções \_**](object-roles.md)             | Nenhum                                                     |
| [Controle giratório](uiauto-supportspinnercontroltype.md)         | [**\_SPINBUTTON do sistema de funções \_**](object-roles.md)     | Nenhum                                                     |
| [SplitButton](uiauto-supportsplitbuttoncontroltype.md) | [**sistema de função \_ \_ SPLITBUTTON**](object-roles.md)   | Nenhum                                                     |
| [StatusBar](uiauto-supportstatusbarcontroltype.md)     | [**\_STATUSBAR do sistema de funções \_**](object-roles.md)       | Nenhum                                                     |
| [Tab](uiauto-supporttabcontroltype.md)                 | [**\_PAGETABLIST do sistema de função \_**](object-roles.md)   | Nenhum                                                     |
| [TabItem](uiauto-supporttabitemcontroltype.md)         | [**\_PAGETAB do sistema de função \_**](object-roles.md)           | Comutador                                                   |
| [Table](uiauto-supporttablecontroltype.md)             | [**\_tabela do sistema de funções \_**](object-roles.md)               | Nenhum                                                     |
| [Text](uiauto-supporttextcontroltype.md)               | [**\_STATICTEXT do sistema de função \_**](object-roles.md)     | Nenhum                                                     |
| [Comum](uiauto-supportthumbcontroltype.md)             | [**\_indicador do sistema de funções \_**](object-roles.md)       | Nenhum                                                     |
| [TitleBar](uiauto-supporttitlebarcontroltype.md)       | [**\_TITLEBAR do sistema de funções \_**](object-roles.md)         | Nenhum                                                     |
| [Barra](uiauto-supporttoolbarcontroltype.md)         | [**barra de ferramentas do \_ sistema de função \_**](object-roles.md)           | Nenhum                                                     |
| [ToolTip](uiauto-supporttooltipcontroltype.md)         | [**Dica de ferramenta do \_ sistema de função \_**](object-roles.md)           | Nenhum                                                     |
| [Árvore](uiauto-supporttreecontroltype.md)               | [**estrutura de tópicos do \_ sistema de funções \_**](object-roles.md)           | Nenhum                                                     |
| [TreeItem](uiauto-supporttreeitemcontroltype.md)       | [**\_OUTLINEITEM do sistema de função \_**](object-roles.md)   | Expandir ou recolher                                       |
| [Window](uiauto-supportwindowcontroltype.md)           | [**\_janela do sistema de funções \_**](object-roles.md)             | Nenhum                                                     |



 

### <a name="ui-automation-properties-and-accstate"></a>Propriedades de automação da interface do usuário e accState



| accState                                                                                      | Propriedade de automação da interface do usuário                                                                                                                                                        | Alteração de estado de gatilhos |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------|
| [**sistema de estado \_ \_ verificado**](object-state-constants.md)                 | Para ControlType = "checkbox", use ToggleState. on. Para "RadioButton", use [ **SelectionItemPattern:: IsSelected**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-get_currentisselected) | Sim                   |
| [**sistema de estado \_ \_ focado**](object-state-constants.md)             | IsKeyboardFocusableProperty                                                                                                                                                   | Não                    |
| [**Estado do \_ sistema \_ focado**](object-state-constants.md)                 | HasKeyboardFocusProperty                                                                                                                                                      | Não                    |
| [**sistema de estado \_ \_ protegido**](object-state-constants.md)             | IsPasswordProperty                                                                                                                                                            | Não                    |
| [**sistema de estado \_ \_ ReadOnly**](object-state-constants.md)               | IsReadOnlyProperty (padrão de controle de valor e padrão de controle RangeValue)                                                                                                     | Não                    |
| [**sistema de estado \_ \_ indisponível**](object-state-constants.md)         | IsEnabledProperty                                                                                                                                                             | Sim                   |
| [**sistema de estado \_ \_ vinculado**](object-state-constants.md)                   | ControlTypeproperty = "Hiperlink"                                                                                                                                             | Não                    |
| [**sistema de estado \_ \_ selecionável**](object-state-constants.md)           | SelectionItemPattern tem suporte                                                                                                                                             | Não                    |
| [**sistema de estado \_ \_ selecionado**](object-state-constants.md)               | Isselecionoproperty (padrão de controle SelectionItem)                                                                                                                            | Não                    |
| [**sistema de estado \_ \_ recolhido**](object-state-constants.md)             | ExpandCollapseState = recolhido                                                                                                                                               | Sim                   |
| [**sistema de estado \_ \_ expandido**](object-state-constants.md)               | ExpandCollapseState = expandido ou PartiallyExpanded                                                                                                                           | Sim                   |
| [**Estado do \_ sistema \_ HASPOPUP**](object-state-constants.md)               | Itens de menu que dão suporte a expandir/recolher                                                                                                                                       | Não                    |
| [**sistema de estado \_ \_ misto**](object-state-constants.md)                     | ToggleState = indeterminado                                                                                                                                                   | Não                    |
| [**Estado do \_ sistema \_ considerável**](object-state-constants.md)               | [**IUIAutomationTransformPattern:: redimensionar**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanresize)                                                                     | Não                    |
| [**Estado do \_ sistema \_ móvel**](object-state-constants.md)               | [**IUIAutomationTransformPattern:: canmova**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtransformpattern-get_currentcanmove)                                                                         | Não                    |
| [**sistema de estado \_ \_ multiselecionável**](object-state-constants.md) | [**IUIAutomationSelectionPattern::CanSelectMultiple**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionpattern-get_currentcanselectmultiple)                                                     | Não                    |



 

### <a name="selection-and-focus"></a>Seleção e foco



| IAccessible                                                            | Automação da Interface de Usuário                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)         | [**IUIAutomation:: Concentrouelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                | Consulte as propriedades de automação da interface do usuário e a tabela accSelect SELFLAGs para obter detalhes.             |
| [**obter \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection) | [**SelectionPattern:: getseleções**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextpattern-getselection) |



 

### <a name="ui-automation-properties-and-accselect-selflags"></a>Propriedades de automação da interface do usuário e accSelect SELFLAGs



| accSelect SELFLAGs                                                  | Propriedade de automação da interface do usuário                                                                                                         |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**SELFLAG \_ nenhum**](selflag.md)                       | Não disponível                                                                                                                  |
| SELFLAG \_ TAKFOCUS                                                   | [**IUIAutomationElement:: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus)                                                 |
| [**SELFLAG \_ TAKESELECTION**](selflag.md)     | [**IUIAutomationSelectionItemPattern:: SELECT**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select)                           |
| [**SELFLAG \_ ADDseleções**](selflag.md)       | [**IUIAutomationSelectionItemPattern::AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)           |
| SELFLAG \_ TAKEREMOVESELECTION                                        | [**IUIAutomationSelectionItemPattern::RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) |
| [**SELFLAG \_ EXTENDSELECTION**](selflag.md) | Não disponível                                                                                                                  |



 

### <a name="spatial-mapping"></a>Mapeamento espacial



| IAccessible                                                 | Automação da Interface de Usuário                                                                                                                        |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) | BoundingRectangleProperty                                                                                                            |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)   | [**IRawElementProviderFragmentRoot::ElementProviderFromPoint**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragmentroot-elementproviderfrompoint) |



 

### <a name="events"></a>Eventos



| System-Level constantes de evento                                                             | Automação da Interface de Usuário                                                                                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**\_MENUPOPUPSTART do sistema de eventos \_**](event-constants.md)     | [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) (Observação: deve verificar se esta é uma janela pop-up.) |
| [**\_MENUPOPUPEND do sistema de eventos \_**](event-constants.md)         | [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                                                |
| [**\_MENUSTART do sistema de eventos \_**](event-constants.md)               | [**UIA \_ MenuModeStartEventId**](uiauto-event-ids.md)                                          |
| [**\_MENUEND do sistema de eventos \_**](event-constants.md)                   | [**UIA \_ MenuModeEndEventId**](uiauto-event-ids.md)                                              |
| [**\_som do sistema de eventos \_**](event-constants.md)                       |                                                                                                                         |
| [**\_alerta do sistema de eventos \_**](event-constants.md)                       |                                                                                                                         |
| [**\_CAPTURESTART do sistema de eventos \_**](event-constants.md)         |                                                                                                                         |
| [**\_CAPTUREEND do sistema de eventos \_**](event-constants.md)             |                                                                                                                         |
| [**\_DIALOGSTART do sistema de eventos \_**](event-constants.md)           |                                                                                                                         |
| [**\_DIALOGEND do sistema de eventos \_**](event-constants.md)               |                                                                                                                         |
| [**\_MOVESIZESTART do sistema de eventos \_**](event-constants.md)       |                                                                                                                         |
| [**\_MOVESIZEEND do sistema de eventos \_**](event-constants.md)           |                                                                                                                         |
| [**\_CONTEXTHELPSTART do sistema de eventos \_**](event-constants.md) |                                                                                                                         |
| [**\_CONTEXTHELPEND do sistema de eventos \_**](event-constants.md)     | Irrelevante                                                                                                            |
| [**\_DRAGDROPSTART do sistema de eventos \_**](event-constants.md)       |                                                                                                                         |
| [**\_DRAGDROPEND do sistema de eventos \_**](event-constants.md)           |                                                                                                                         |
| [**\_SWITCHSTART do sistema de eventos \_**](event-constants.md)           | Irrelevante                                                                                                            |
| [**\_SWITCHEND do sistema de eventos \_**](event-constants.md)               | Irrelevante                                                                                                            |
| [**\_MINIMIZESTART do sistema de eventos \_**](event-constants.md)       |                                                                                                                         |
| [**\_MINIMIZEEND do sistema de eventos \_**](event-constants.md)           |                                                                                                                         |
| [**\_primeiro plano do sistema de eventos \_**](event-constants.md)             |                                                                                                                         |
| [**\_SCROLLINGSTART do sistema de eventos \_**](event-constants.md)     | Não disponível                                                                                                           |
| [**\_SCROLLINGEND do sistema de eventos \_**](event-constants.md)         | Não disponível                                                                                                           |



 



| Object-Level constantes de evento                                                           | Automação da Interface de Usuário                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_foco do objeto de evento \_**](event-constants.md)                     | AutomationFocusChangedEvent                                                            |
| [**objeto de evento \_ \_ VALUECHANGE**](event-constants.md)         | Valorproperty (padrão de controle de valor e padrão de controle RangeValue)                   |
| [**\_seleção de objeto de evento \_**](event-constants.md)             | ElementSelectedEvent (padrão de controle SelectionItem)                                   |
| [**objeto de evento \_ \_ SELECTIONADD**](event-constants.md)       | ElementAddedToSelectionEvent (padrão de controle SelectionItem)                           |
| [**objeto de evento \_ \_ SELECTIONREMOVE**](event-constants.md) | ElementRemovedFromSelectionEvent                                                       |
| [**objeto de evento \_ \_ SELECTIONWITHIN**](event-constants.md) | EventsSelectionInvalidatedEvent                                                        |
| [**objeto de evento \_ \_ STATECHANGE**](event-constants.md)         | Consulte Propriedades de automação da interface do usuário e tabela accState para Estados que disparam uma alteração de estado |



 

 

 




