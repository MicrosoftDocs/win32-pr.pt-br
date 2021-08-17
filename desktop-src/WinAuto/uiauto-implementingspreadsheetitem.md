---
title: Padrão de controle SpreadsheetItem
description: Descreve as diretrizes e convenções para implementar o ISpreadsheetItemProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- Automação da interface do usuário, implementando o padrão de controle SpreadsheetItem
- Automação da interface do usuário, padrão de controle SpreadsheetItem
- Automação da interface do usuário, ISpreadsheetItemProvider
- ISpreadsheetItemProvider
- Implementando o padrão de controle SpreadsheetItem Automation UI
- Padrão de controle SpreadsheetItem
- padrões de controle, ISpreadsheetItemProvider
- padrões de controle, implementando a automação da interface do usuário SpreadsheetItem
- padrões de controle, SpreadsheetItem
- interfaces, ISpreadsheetItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d5feaa32b5fe79635c6acc01e1e0b18b9ba77c382ba3f07c64f7cb3e921b06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324366"
---
# <a name="spreadsheetitem-control-pattern"></a>Padrão de controle SpreadsheetItem

Descreve as diretrizes e convenções para implementar o [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), incluindo informações sobre propriedades e métodos. O padrão de controle **SpreadsheetItem** é usado para expor as propriedades de uma célula em uma planilha ou outro documento baseado em grade.

O padrão de controle **SpreadsheetItem** está fortemente relacionado ao padrão de controle [GridItem](uiauto-implementinggriditem.md) ; os controles que implementam o padrão de controle **SpreadsheetItem** também devem implementar o padrão de controle GridItem. Os controles também podem implementar o padrão de controle [TableItem](uiauto-implementingtableitem.md) , se apropriado. Para obter exemplos de controles que implementam esses padrões de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **ISpreadsheetItemProvider**](#required-members-for-ispreadsheetitemprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **SpreadsheetItem** , observe as seguintes diretrizes e convenções:

-   Ao implementar os métodos [**ISpreadsheetItemProvider:: GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) e [**ISpreadsheetItemProvider:: GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) , consulte a documentação do [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) . Esses métodos retornam matrizes para permitir que os provedores ofereçam suporte a várias anotações em uma única célula.
-   Alguns tipos de anotações não exigem uma implementação completa da interface [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) . Por exemplo, um indicador de erro ortográfico simples poderia ser representado ao fazer com que [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) retornasse um identificador de atributo de texto de [**\_ SpellingError de AnnotationType**](uiauto-annotation-type-identifiers.md)e ter [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) retornado um valor nulo.

## <a name="required-members-for-ispreadsheetitemprovider"></a>Membros necessários para **ISpreadsheetItemProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) .



| Membros necessários                                                                         | Tipo de membro | Observações                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Fórmula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | Propriedade    | A implementação de uma propriedade de [**fórmula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) separada é necessária porque a propriedade de [valor](value-property.md) de uma célula normalmente retorna o valor calculado da célula. A propriedade de **fórmula** deverá ser **nula** se nenhuma fórmula for definida. |
| [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | Método      | Retorna uma matriz de provedores de elementos que se refere às anotações vinculadas a esta célula. Os ponteiros dentro da matriz poderão ser nulos se uma anotação não tiver um provedor vinculado.                                                                                                       |
| [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | Método      | Retorna uma matriz de identificadores de tipo de anotação que descrevem as anotações nesta célula. A matriz deve ter o mesmo tamanho que a matriz retornada por [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).                                         |



 

Este padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Padrão de controle de planilha](uiauto-implementingspreadsheet.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 