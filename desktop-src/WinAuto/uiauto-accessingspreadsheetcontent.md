---
title: Acessando conteúdo da planilha
description: Este tópico descreve como os aplicativos cliente de automação da interface do usuário da Microsoft podem acessar o conteúdo de uma planilha.
ms.assetid: F32EFA46-222B-4A4E-9938-10DE0F6A2CA7
keywords:
- clientes, acessando o conteúdo da planilha
- clientes, controles baseados em texto
- clientes, padrão de controle de planilha
- clientes, padrão de controle SpreadsheetItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31495086614f34aeff378a8565200fa03f2dad62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294425"
---
# <a name="accessing-spreadsheet-content"></a>Acessando conteúdo da planilha

Um controle baseado em texto que contém conteúdo de planilha pode permitir que os clientes acessem o conteúdo ao dar suporte aos padrões de controle de [planilha](uiauto-implementingspreadsheet.md) e [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) . Este tópico descreve como os aplicativos cliente de automação da interface do usuário da Microsoft podem acessar o conteúdo de uma planilha.

Para determinar se um controle baseado em texto dá suporte aos padrões de controle de [planilha](uiauto-implementingspreadsheet.md) e [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) , primeiro recupere a interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para o controle (consulte [obtendo elementos de automação da interface do usuário](uiauto-obtainingelements.md).) Em seguida, chame o método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , especificando um identificador de padrão de controle de [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) ou [**UIA \_ SPREADSHEETITEMPATTERNID**](uiauto-controlpattern-ids.md), e uma variante que recebe true se o controle der suporte ao padrão de controle específico.

Para acessar o conteúdo da planilha, recupere a interface [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) chamando o método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) e especificando [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) como o identificador do padrão de controle. Em seguida, use o método [**IUIAutomationSpreadsheetPattern:: GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) para obter a interface [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) para um item de planilha específico (normalmente, uma célula). Use as propriedades e os métodos da interface **IUIAutomationSpreadsheetItem** para recuperar a fórmula da célula e todas as anotações associadas à célula. Para obter mais informações sobre anotações, consulte [recuperando anotações.](uiauto-usingtextrangeobjects.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte à automação da interface do usuário para conteúdo textual](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Trabalhando com controles baseados em texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 