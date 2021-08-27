---
title: Padrão de controle TableItem
description: Descreve diretrizes e convenções para implementar ITableItemProvider, incluindo informações sobre métodos. O padrão de controle TableItem é usado para dar suporte a controles filho de contêineres que implementam ITableProvider.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- Automação da Interface do Usuário, implementando o padrão de controle TableItem
- Automação da Interface do Usuário, padrão de controle TableItem
- Automação da Interface do Usuário,ITableItemProvider
- ITableItemProvider
- implementando padrões Automação da Interface do Usuário controle TableItem
- Padrões de controle TableItem
- padrões de controle, ITableItemProvider
- padrões de controle, implementando Automação da Interface do Usuário TableItem
- padrões de controle, TableItem
- interfaces, ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babb64114bb761b0b6e93a7cc9c0036cb01bb8946eb813bcd0fc3e821d44a183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098266"
---
# <a name="tableitem-control-pattern"></a>Padrão de controle TableItem

Descreve diretrizes e convenções para implementar [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), incluindo informações sobre métodos. O **padrão de controle TableItem** é usado para dar suporte a controles filho de contêineres que implementam [**ITableProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)

O acesso à funcionalidade de célula individual é fornecido pela implementação simultânea necessária de [**IGridItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) Esse padrão de controle é análogo a **IGridItemProvider** com a distinção de que qualquer controle que implemente [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) deve expor programaticamente a relação entre a célula individual e suas informações de linha e coluna. Para exemplos de controles que implementam esse padrão de controle, consulte [Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **ITableItemProvider**](#required-members-for-itableitemprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão **de controle TableItem,** observe as seguintes diretrizes e convenções:

-   Para a funcionalidade de item de grade relacionada, consulte [Padrão de controle GridItem](uiauto-implementinggriditem.md).

## <a name="required-members-for-itableitemprovider"></a>Membros necessários para **ITableItemProvider**

Os métodos a seguir são necessários para implementar a interface [**ITableItemProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)



| Membros necessários                                                               | Tipo de membro | Observações |
|--------------------------------------------------------------------------------|-------------|-------|
| [**GetColumnHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | Método      | Nenhum  |
| [**GetRowHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | Método      | Nenhum  |



 

Esse padrão de controle não tem propriedades ou eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Padrão de controle de tabela](uiauto-implementingtable.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




