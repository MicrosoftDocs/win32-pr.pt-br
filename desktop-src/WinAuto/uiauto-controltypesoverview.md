---
title: Visão Geral dos Tipos de Controle de Automação de Interface do Usuário
description: Os tipos de controle de automação da interface do usuário da Microsoft são propriedades que servem como identificadores bem conhecidos que indicam o tipo de controle que um determinado elemento da interface do usuário representa, como uma caixa de combinação ou um botão.
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- Visão geral da automação da interface do usuário, tipos de controle
- Automação da interface do usuário, Propriedade UIA_LocalizedControlTypePropertyId
- tipos de controle, sobre
- tipos de controle, requisitos
- tipos de controle, pré-requisitos
- tipos de controle, predefinidos
- tipos de controle, Propriedade UIA_LocalizedControlTypePropertyId
- tipos de controle predefinidos
- Propriedade UIA_LocalizedControlTypePropertyId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b504de2c8f0ae660a27b3b16fa4537630a468f5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499056"
---
# <a name="ui-automation-control-types-overview"></a>Visão Geral dos Tipos de Controle de Automação de Interface do Usuário

Os tipos de controle de automação da interface do usuário da Microsoft são propriedades que servem como identificadores bem conhecidos que indicam o tipo de controle que um determinado elemento da interface do usuário representa, como uma caixa de combinação ou um botão. Os aplicativos cliente usam o tipo para identificar os recursos de um controle e para determinar como interagir com ele.

Este tópico contém as seguintes seções:

-   [Requisitos de tipo de controle de automação da interface do usuário](#ui-automation-control-type-requisites)
-   [A propriedade LocalizedControlType](#the-localizedcontroltype-property)
-   [Tipos de controle de automação da interface do usuário atuais](#current-ui-automation-control-types)
-   [Tópicos relacionados](#related-topics)

## <a name="ui-automation-control-type-requisites"></a>Requisitos de tipo de controle de automação da interface do usuário

Cada tipo de controle de automação da interface do usuário tem um conjunto de condições associadas a ele. Quando um provedor atribui um tipo de controle a um controle, o provedor deve garantir que o controle atenda a todas as condições associadas a esse tipo de controle. As condições incluem o seguinte:

-   Padrões de controle de automação da interface do usuário: cada tipo de controle tem um conjunto de padrões de controle ao qual o controle deve dar suporte, um conjunto que é opcional e um conjunto ao qual o controle não deve dar suporte.
-   Valores de propriedades da Automação da Interface do Usuário: cada tipo de controle possui um conjunto de propriedades que o controle tem que permitir.
-   Eventos de Automação da Interface do Usuário: cada tipo de controle possui um conjunto de eventos que o controle tem que permitir.
-   Estrutura da árvore de automação da IU: cada tipo de controle define como o controle deve aparecer na estrutura da árvore de automação da IU.

Quando um controle atende às condições de um tipo de controle específico, o valor da propriedade [**IUIAutomationElement:: CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (ou [**IUIAutomationElement:: CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) indicará o tipo de controle.

Se o seu controle não atender as especificações de um determinado tipo de controle, use [**UIA \_ CustomControlTypeId**](uiauto-controltype-ids.md) como a ID de tipo de controle e descreva completamente o controle usando os padrões de controle e as propriedades relevantes. Você também pode definir a propriedade [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) como uma cadeia de caracteres que melhor descreva o tipo de seu controle.

## <a name="the-localizedcontroltype-property"></a>A propriedade LocalizedControlType

Se você usar um tipo de controle predefinido para descrever seu controle, use o valor padrão para a propriedade [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) e permita que a automação da interface do usuário forneça uma cadeia de caracteres localizada para que os provedores exponham corretamente. Se você não puder usar um tipo de controle predefinido para descrever seu controle, defina a propriedade **UIA \_ LocalizedControlTypePropertyId** como uma cadeia de caracteres localizada que descreva com precisão o tipo de seu controle. A cadeia de caracteres deve ser concisa, mas precisa o suficiente para que uma tecnologia assistencial, como um leitor de tela, possa usá-la na interface do usuário para informar o tipo do controle.

## <a name="current-ui-automation-control-types"></a>Tipos de controle de automação da interface do usuário atuais

Os tópicos a seguir descrevem os tipos de controle de automação da interface do usuário. Para cada tipo de controle, a descrição inclui o conjunto de condições que um controle do tipo fornecido deve suportar:

-   Tipo de controle AppBar
-   [Tipo de controle de botão](uiauto-supportbuttoncontroltype.md)
-   [Tipo de controle de calendário](uiauto-supportcalendarcontroltype.md)
-   [Tipo de controle de caixa de seleção](uiauto-supportcheckboxcontroltype.md)
-   [Tipo de controle ComboBox](uiauto-supportcomboboxcontroltype.md)
-   [Tipo de controle DataGrid](uiauto-supportdatagridcontroltype.md)
-   [Tipo de controle DataItem](uiauto-supportdataitemcontroltype.md)
-   [Tipo de controle de documento](uiauto-supportdocumentcontroltype.md)
-   [Editar tipo de controle](uiauto-supporteditcontroltype.md)
-   [Tipo de controle de grupo](uiauto-supportgroupcontroltype.md)
-   [Tipo de controle de cabeçalho](uiauto-supportheadercontroltype.md)
-   [Tipo de controle HeaderItem](uiauto-supportheaderitemcontroltype.md)
-   [Tipo de controle de hiperlink](uiauto-supporthyperlinkcontroltype.md)
-   [Tipo de controle de imagem](uiauto-supportimagecontroltype.md)
-   [Tipo de controle de lista](uiauto-supportlistcontroltype.md)
-   [Tipo de controle ListItem](uiauto-supportlistitemcontroltype.md)
-   [Tipo de controle de menu](uiauto-supportmenucontroltype.md)
-   [Tipo de controle MenuBar](uiauto-supportmenubarcontroltype.md)
-   [Tipo de controle MenuItem](uiauto-supportmenuitemcontroltype.md)
-   [Tipo de controle de painel](uiauto-supportpanecontroltype.md)
-   [Tipo de controle ProgressBar](uiauto-supportprogressbarcontroltype.md)
-   [Tipo de controle RadioButton](uiauto-supportradiobuttoncontroltype.md)
-   [Tipo de controle ScrollBar](uiauto-supportscrollbarcontroltype.md)
-   [Tipo de controle SemanticZoom](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [Tipo de controle Separator](uiauto-supportseparatorcontroltype.md)
-   [Tipo de controle Slider](uiauto-supportslidercontroltype.md)
-   [Tipo de controle Spinner](uiauto-supportspinnercontroltype.md)
-   [Tipo de controle SplitButton](uiauto-supportsplitbuttoncontroltype.md)
-   [Tipo de controle StatusBar](uiauto-supportstatusbarcontroltype.md)
-   [Tipo de controle da guia](uiauto-supporttabcontroltype.md)
-   [Tipo de controle TabItem](uiauto-supporttabitemcontroltype.md)
-   [Tipo de controle de tabela](uiauto-supporttablecontroltype.md)
-   [Tipo de controle de texto](uiauto-supporttextcontroltype.md)
-   [Tipo de controle Thumb](uiauto-supportthumbcontroltype.md)
-   [Tipo de controle TitleBar](uiauto-supporttitlebarcontroltype.md)
-   [Tipo de controle ToolBar](uiauto-supporttoolbarcontroltype.md)
-   [Tipo de controle ToolTip](uiauto-supporttooltipcontroltype.md)
-   [Tipo de controle de árvore](uiauto-supporttreecontroltype.md)
-   [Tipo de controle TreeItem](uiauto-supporttreeitemcontroltype.md)
-   [Tipo de controle de janela](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Identificadores de tipo de controle](uiauto-controltype-ids.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Suporte a tipos de controle de automação da interface do usuário](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[Suporte de automação de interface do usuário para Controles Padrão](uiauto-controlsupport.md)
</dt> <dt>

[Conceitos básicos de automação da interface do usuário](entry-uiautocore-overview.md)
</dt> </dl>

 

 