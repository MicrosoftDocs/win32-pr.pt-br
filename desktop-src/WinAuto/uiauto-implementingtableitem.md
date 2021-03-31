---
title: Padrão de controle TableItem
description: Descreve as diretrizes e convenções para implementar o ITableItemProvider, incluindo informações sobre métodos. O padrão de controle TableItem é usado para dar suporte a controles filho de contêineres que implementam ITableProvider.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- Automação da interface do usuário, implementando o padrão de controle TableItem
- Automação da interface do usuário, padrão de controle TableItem
- Automação da interface do usuário, ITableItemProvider
- ITableItemProvider
- Implementando padrões de controle TableItem de automação da interface do usuário
- Padrões de controle TableItem
- padrões de controle, ITableItemProvider
- padrões de controle, implementando a automação da interface do usuário TableItem
- padrões de controle, TableItem
- interfaces, ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bae3e6d5379ec9a662e31ec6181476b112631381
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635494"
---
# <a name="tableitem-control-pattern"></a>Padrão de controle TableItem

Descreve as diretrizes e convenções para implementar o [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), incluindo informações sobre métodos. O padrão de controle **TableItem** é usado para dar suporte a controles filho de contêineres que implementam [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).

O acesso à funcionalidade de célula individual é fornecido pela implementação simultânea e necessária do [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider). Esse padrão de controle é análogo a **IGridItemProvider** com a distinção de que qualquer controle que implementa [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) deve expor de forma programática a relação entre a célula individual e suas informações de linha e coluna. Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **ITableItemProvider**](#required-members-for-itableitemprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **TableItem** , observe as seguintes diretrizes e convenções:

-   Para obter a funcionalidade de item de grade relacionada, consulte [padrão de controle GridItem](uiauto-implementinggriditem.md).

## <a name="required-members-for-itableitemprovider"></a>Membros necessários para **ITableItemProvider**

Os métodos a seguir são necessários para implementar a interface [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) .



| Membros necessários                                                               | Tipo de membro | Observações |
|--------------------------------------------------------------------------------|-------------|-------|
| [**GetColumnHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | Método      | Nenhum  |
| [**GetRowHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | Método      | Nenhum  |



 

Este padrão de controle não tem propriedades ou eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Padrão de controle de tabela](uiauto-implementingtable.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




