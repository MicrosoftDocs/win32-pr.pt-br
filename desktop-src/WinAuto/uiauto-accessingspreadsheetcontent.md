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
# <a name="accessing-spreadsheet-content"></a><span data-ttu-id="32bcf-107">Acessando conteúdo da planilha</span><span class="sxs-lookup"><span data-stu-id="32bcf-107">Accessing Spreadsheet Content</span></span>

<span data-ttu-id="32bcf-108">Um controle baseado em texto que contém conteúdo de planilha pode permitir que os clientes acessem o conteúdo ao dar suporte aos padrões de controle de [planilha](uiauto-implementingspreadsheet.md) e [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) .</span><span class="sxs-lookup"><span data-stu-id="32bcf-108">A text-based control that contains spreadsheet content can enable clients to access the content by supporting the [Spreadsheet](uiauto-implementingspreadsheet.md) and [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) control patterns.</span></span> <span data-ttu-id="32bcf-109">Este tópico descreve como os aplicativos cliente de automação da interface do usuário da Microsoft podem acessar o conteúdo de uma planilha.</span><span class="sxs-lookup"><span data-stu-id="32bcf-109">This topic describes how Microsoft UI Automation client applications can access the content of a spreadsheet.</span></span>

<span data-ttu-id="32bcf-110">Para determinar se um controle baseado em texto dá suporte aos padrões de controle de [planilha](uiauto-implementingspreadsheet.md) e [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) , primeiro recupere a interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para o controle (consulte [obtendo elementos de automação da interface do usuário](uiauto-obtainingelements.md).) Em seguida, chame o método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , especificando um identificador de padrão de controle de [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) ou [**UIA \_ SPREADSHEETITEMPATTERNID**](uiauto-controlpattern-ids.md), e uma variante que recebe true se o controle der suporte ao padrão de controle específico.</span><span class="sxs-lookup"><span data-stu-id="32bcf-110">To determine whether a text-based control supports the [Spreadsheet](uiauto-implementingspreadsheet.md) and [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) control patterns, first retrieve the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface for the control (see [Obtaining UI Automation Elements](uiauto-obtainingelements.md).) Next, call the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method, specifying a control pattern identifier of [**UIA\_SpreadsheetPatternId**](uiauto-controlpattern-ids.md) or [**UIA\_SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md), and a variant that receives TRUE if the control supports the particular control pattern.</span></span>

<span data-ttu-id="32bcf-111">Para acessar o conteúdo da planilha, recupere a interface [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) chamando o método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) e especificando [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) como o identificador do padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="32bcf-111">To access the spreadsheet content, retrieve the [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) interface by calling [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method and specifying [**UIA\_SpreadsheetPatternId**](uiauto-controlpattern-ids.md) as the control pattern identifier.</span></span> <span data-ttu-id="32bcf-112">Em seguida, use o método [**IUIAutomationSpreadsheetPattern:: GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) para obter a interface [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) para um item de planilha específico (normalmente, uma célula).</span><span class="sxs-lookup"><span data-stu-id="32bcf-112">Next, use the [**IUIAutomationSpreadsheetPattern::GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) method to get the [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) interface for a particular spreadsheet item (typically a cell).</span></span> <span data-ttu-id="32bcf-113">Use as propriedades e os métodos da interface **IUIAutomationSpreadsheetItem** para recuperar a fórmula da célula e todas as anotações associadas à célula.</span><span class="sxs-lookup"><span data-stu-id="32bcf-113">Use the properties and methods of the **IUIAutomationSpreadsheetItem** interface to retrieve the formula for the cell, and any annotations associated with the cell.</span></span> <span data-ttu-id="32bcf-114">Para obter mais informações sobre anotações, consulte [recuperando anotações.](uiauto-usingtextrangeobjects.md)</span><span class="sxs-lookup"><span data-stu-id="32bcf-114">For more information about annotations, see [Retrieving Annotations.](uiauto-usingtextrangeobjects.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="32bcf-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32bcf-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32bcf-116">Suporte à automação da interface do usuário para conteúdo textual</span><span class="sxs-lookup"><span data-stu-id="32bcf-116">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="32bcf-117">Trabalhando com controles baseados em texto</span><span class="sxs-lookup"><span data-stu-id="32bcf-117">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 