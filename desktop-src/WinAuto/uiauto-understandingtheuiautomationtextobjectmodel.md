---
title: Noções básicas Automação da Interface do Usuário modelo de objeto de texto
description: Este tópico descreve como a Microsoft Automação da Interface do Usuário aplicativos cliente acessam o conteúdo textual de um controle baseado em texto.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- clientes, noções básicas Automação da Interface do Usuário modelo de objeto de texto
- clientes, controles baseados em texto
- clientes, intervalos de texto
- clientes, Padrão de controle de texto
- clientes, padrão de controle TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655f291e9cc11d925f947617fe31be96ebd81a2dbff73506a0e474dcde9e4446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823882"
---
# <a name="understanding-the-ui-automation-text-object-model"></a>Noções básicas Automação da Interface do Usuário modelo de objeto de texto

Este tópico descreve como a Microsoft Automação da Interface do Usuário aplicativos cliente acessam o conteúdo textual de um controle baseado em texto.

-   [Modelo de objeto específico do controle](#control-specific-object-model)
-   [Tópicos relacionados](#related-topics)

Controles baseados em texto expõem conteúdo textual para Automação da Interface do Usuário aplicativos cliente por meio de um modelo de objeto de texto simples. Os aplicativos cliente têm acesso ao modelo de objeto de texto por meio das interfaces de padrão de controle Text e [TextRange,](uiauto-about-text-and-textrange-patterns.md) incluindo [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) [**e IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange). Os aplicativos cliente podem usar essas interfaces para recuperar conteúdo textual, atributos de texto e objetos inseridos, como tabelas e hiperlinks de controles baseados em texto.

Os tipos de controle que suportam Automação da Interface do Usuário modelo de objeto de texto [incluem os tipos de](uiauto-supporteditcontroltype.md) [controle](uiauto-supportdocumentcontroltype.md) Editar e Documento. Outros tipos de controle, como [ToolTip](uiauto-supporttooltipcontroltype.md) e [Text,](uiauto-supporttextcontroltype.md) também podem dar suporte ao modelo de objeto de texto, mas não são necessários.

> [!Note]  
> O Automação da Interface do Usuário modelo de objeto de texto não fornece um meio de inserir ou modificar texto. No entanto, alguns controles permitem que o texto seja inserido ou modificado por meio da interface [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) ou por meio da entrada direta do teclado.

 

## <a name="control-specific-object-model"></a>Modelo de objeto específico do controle

Um controle baseado em texto que implementa seus próprios Modelo de Objeto do Documento (DOM) pode expor o DOM implementando o padrão de controle [ObjectModel.](uiauto-implementingobjectmodel.md) Expor o DOM pode dar aos aplicativos cliente maior acesso e controle sobre o conteúdo de um controle baseado em texto.

Um aplicativo cliente pode descobrir se um controle baseado em texto específico implementa um DOM recuperando a interface [**IUIAutomationElement do**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) controle. Em seguida, chame o método [**IUIAutomationElement::GetCurrentPropertyValue,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) especificando o identificador de propriedade [**\_ IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) da UIA e uma variante que receberá TRUE se o controle implementar um DOM.

Para acessar o DOM, chame o método [**IUIAutomationElement::GetCurrentPattern,**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) especificando o identificador de padrão de controle [**\_ ObjectModelPatternId**](uiauto-controlpattern-ids.md) da UIA e uma variável que recebe a interface [**IUIAutomationObjectModelPattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) Chame o [**método IUIAutomationObjectModelPattern::GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) para recuperar a interface DOM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Padrões de controle Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Automação da Interface do Usuário suporte para conteúdo textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabalhando com controles baseados em texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




