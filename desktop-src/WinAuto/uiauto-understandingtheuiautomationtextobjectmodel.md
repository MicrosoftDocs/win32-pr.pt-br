---
title: Compreendendo o modelo de objeto de texto de automação da interface do usuário
description: Este tópico descreve como os aplicativos cliente de automação da interface do usuário da Microsoft acessam o conteúdo textual de um controle baseado em texto.
ms.assetid: 8545EBA3-6995-4336-A197-27CE3A3339EE
keywords:
- clientes, entendendo o modelo de objeto de texto de automação de interface
- clientes, controles baseados em texto
- clientes, intervalos de texto
- clientes, padrão de controle de texto
- clientes, padrão de controle TextRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f6dae1fc5ca02af69ab3d5386461e6bd7a864d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635515"
---
# <a name="understanding-the-ui-automation-text-object-model"></a>Compreendendo o modelo de objeto de texto de automação da interface do usuário

Este tópico descreve como os aplicativos cliente de automação da interface do usuário da Microsoft acessam o conteúdo textual de um controle baseado em texto.

-   [Modelo de objeto específico de controle](#control-specific-object-model)
-   [Tópicos relacionados](#related-topics)

Controles baseados em texto expõem conteúdo textual para aplicativos cliente de automação da interface do usuário por meio de um modelo de objeto de texto simples. Os aplicativos cliente têm acesso ao modelo de objeto de texto por meio das interfaces de padrão de controle [Text e TextRange](uiauto-about-text-and-textrange-patterns.md) , incluindo [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) e [**IUIAutomationTextRange**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange). Os aplicativos cliente podem usar essas interfaces para recuperar conteúdo textual, atributos de texto e objetos incorporados, como tabelas e hiperlinks, de controles baseados em texto.

Os tipos de controle que dão suporte ao modelo de objeto de texto de automação da interface do usuário incluem os tipos de controle [Editar](uiauto-supporteditcontroltype.md) e [documento](uiauto-supportdocumentcontroltype.md) . Outros tipos de controle, como [ToolTip](uiauto-supporttooltipcontroltype.md) e [Text](uiauto-supporttextcontroltype.md) , também podem oferecer suporte ao modelo de objeto de texto, mas não são obrigatórios.

> [!Note]  
> O modelo de objeto de texto de automação da interface do usuário não fornece um meio para inserir ou modificar texto. No entanto, alguns controles permitem que o texto seja inserido ou modificado por meio da interface [**IUIAutomationValuePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvaluepattern) ou por meio de entrada de teclado direta.

 

## <a name="control-specific-object-model"></a>Modelo de objeto específico de controle

Um controle baseado em texto que implementa seu próprio Modelo de Objeto do Documento (DOM) pode expor o DOM implementando o padrão de controle [ObjectModel](uiauto-implementingobjectmodel.md) . Expor o DOM pode fornecer aos aplicativos cliente maior acesso e controle sobre o conteúdo de um controle baseado em texto.

Um aplicativo cliente pode descobrir se um determinado controle baseado em texto implementa um DOM recuperando a interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) do controle. Em seguida, chame o método [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) , especificando o identificador da propriedade [**UIA \_ IsObjectModelPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md) e uma variante que receberá true se o controle implementar um dom.

Para acessar o DOM, chame o método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , especificando o identificador de padrão de controle [**UIA \_ ObjectModelPatternId**](uiauto-controlpattern-ids.md) e uma variável que recebe a interface [**IUIAutomationObjectModelPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationobjectmodelpattern) . Chame o método [**IUIAutomationObjectModelPattern:: GetUnderlyingObjectModel**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationobjectmodelpattern-getunderlyingobjectmodel) para recuperar a interface dom.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Padrões de controle Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Suporte à automação da interface do usuário para conteúdo textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabalhando com controles baseados em texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 




