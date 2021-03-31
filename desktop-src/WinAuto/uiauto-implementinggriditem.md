---
title: Padrão de controle GridItem
description: Descreve as diretrizes e convenções para implementar o IGridItemProvider, incluindo informações sobre propriedades. O padrão de controle GridItem é usado para dar suporte a controles filho individuais de contêineres que implementam IGridProvider.
ms.assetid: ae4b9021-1800-485b-99a2-54ddf9c21f93
keywords:
- Automação da interface do usuário, implementando o padrão de controle GridItem
- Automação da interface do usuário, padrão de controle GridItem
- Automação da interface do usuário, IGridItemProvider
- IGridItemProvider
- Implementando padrões de controle GridItem de automação da interface do usuário
- Padrões de controle de GridItem
- padrões de controle, IGridItemProvider
- padrões de controle, implementando o GridItem de automação da interface do usuário
- padrões de controle, GridItem
- interfaces, IGridItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef45b5f655e3ef09350c508271233de49f964a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635633"
---
# <a name="griditem-control-pattern"></a>Padrão de controle GridItem

Descreve as diretrizes e convenções para implementar o [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), incluindo informações sobre propriedades. O padrão de controle **GridItem** é usado para dar suporte a controles filho individuais de contêineres que implementam [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).

Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IGridItemProvider**](#required-members-for-igriditemprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle **GridItem** , observe as seguintes diretrizes e convenções:

-   As coordenadas de grade são baseadas em zero com a célula superior esquerda com coordenadas (0, 0).
-   As células mescladas relatarão suas propriedades de [**linha**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) e [**coluna**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) com base em sua célula de âncora subjacente, conforme definido pelo provedor de automação de interface do usuário da Microsoft. Normalmente, será a linha ou coluna mais alta e mais à esquerda.
-   O [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) não fornece manipulação ativa da grade, como mesclagem ou divisão de células.
-   Controles que implementam [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) normalmente podem ser percorridos (ou seja, um cliente de automação de interface do usuário pode mover para controles adjacentes) usando o teclado.

## <a name="required-members-for-igriditemprovider"></a>Membros necessários para **IGridItemProvider**

As propriedades a seguir são necessárias para implementar a interface [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) .



| Membros necessários                                                  | Tipo de membro | Observações |
|-------------------------------------------------------------------|-------------|-------|
| [**Fila**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)                       | Propriedade    | Nenhum  |
| [**Pilha**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)                 | Propriedade    | Nenhum  |
| [**RowSpan**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_rowspan)               | Propriedade    | Nenhum  |
| [**ColumnSpan**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_columnspan)         | Propriedade    | Nenhum  |
| [**ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) | Propriedade    | Nenhum  |



 

Este padrão de controle não tem nenhum método ou evento associado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Padrão de controle de grade](uiauto-implementinggrid.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




