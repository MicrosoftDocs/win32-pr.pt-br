---
title: Padrão de controle de grade
description: Descreve as diretrizes e convenções para implementar o IGridProvider, incluindo informações sobre propriedades e métodos. O padrão de controle de grade é usado para dar suporte a controles que atuam como contêineres para uma coleção de elementos filho.
ms.assetid: c50fb6f7-884a-4147-a6b2-c59d787fc04b
keywords:
- Automação da interface do usuário, implementando o padrão de controle de grade
- Automação da interface do usuário, padrão de controle de grade
- Automação da interface do usuário, IGridProvider
- IGridProvider
- Implementando padrões de controle de grade de automação da IU
- Padrões de controle de grade
- padrões de controle, IGridProvider
- padrões de controle, implementação da grade de automação da interface do usuário
- padrões de controle, grade
- interfaces, IGridProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328d8536a367389a6d17422bd6f6476a3e82aa11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005281"
---
# <a name="grid-control-pattern"></a>Padrão de controle de grade

Descreve as diretrizes e convenções para implementar o [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), incluindo informações sobre propriedades e métodos. O padrão de controle de **grade** é usado para dar suporte a controles que atuam como contêineres para uma coleção de elementos filho.

Os filhos deste elemento devem implementar [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) e ser organizados em um sistema de coordenadas lógico bidimensional que possa ser atravessado por linha e coluna. Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **IGridProvider**](#required-members-for-igridprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle de **grade** , observe as seguintes diretrizes e convenções:

-   As coordenadas de grade são baseadas em zero com o canto superior esquerdo (ou célula superior direita, dependendo da localidade) com coordenadas (0, 0).
-   Se uma célula estiver vazia, um elemento de automação da interface do usuário da Microsoft ainda deverá ser retornado para dar suporte à propriedade [**IGridItemProvider:: ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) dessa célula. Isso é possível quando o layout dos elementos filho na grade é semelhante a uma matriz irregular (Veja o exemplo abaixo).

    ![exemplo de um controle de grade com coordenadas vazias](images/grid.png)

-   Uma grade com um único item ainda é necessária para implementar [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) se for considerada logicamente como uma grade. O número de itens filho na grade é irrelevante.
-   Linhas e colunas ocultas, dependendo da implementação do provedor, podem ser carregadas na árvore de automação da interface do usuário e, portanto, serão refletidas nas propriedades [**IGridProvider:: RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) e [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) . Se as linhas e colunas ocultas ainda não tiverem sido carregadas, elas não deverão ser contadas.
-   [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) não habilita a manipulação ativa de uma grade; [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) deve ser implementado para habilitar essa funcionalidade.
-   Use um [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) para escutar alterações estruturais ou de layout na grade, como células que foram adicionadas, removidas ou mescladas.
-   Use um [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) para acompanhar a passagem pelos itens ou células de uma grade.

## <a name="required-members-for-igridprovider"></a>Membros necessários para **IGridProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) .



| Membros necessários                                        | Tipo de membro | Observações |
|---------------------------------------------------------|-------------|-------|
| [**Linhas**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | Propriedade    | Nenhum  |
| [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | Propriedade    | Nenhum  |
| [**GetItem**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | Método      | Nenhum  |



 

Este padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Padrão de controle GridItem](uiauto-implementinggriditem.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




