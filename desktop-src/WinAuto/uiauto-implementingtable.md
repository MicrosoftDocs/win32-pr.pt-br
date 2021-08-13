---
title: Padrão de controle de tabela
description: Descreve as diretrizes e convenções para implementar o ITableProvider, incluindo informações sobre propriedades e métodos. O padrão de controle Table é usado para dar suporte a controles que atuam como contêineres para uma coleção de elementos filho.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- Automação da interface do usuário, implementando o padrão de controle de tabela
- Automação da interface do usuário, padrão de controle de tabela
- Automação da interface do usuário, ITableProvider
- ITableProvider
- Implementando padrões de controle de tabela de automação de IU
- Padrões de controle de tabela
- padrões de controle, ITableProvider
- padrões de controle, implementação da tabela de automação da interface do usuário
- padrões de controle, tabela
- interfaces, ITableProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb484245ee7c2f982ca6c5624ad108a0c75a4721ba7f6cbdf7a8af8ee2d91881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324121"
---
# <a name="table-control-pattern"></a>Padrão de controle de tabela

Descreve as diretrizes e convenções para implementar o [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), incluindo informações sobre propriedades e métodos. O padrão de controle **Table** é usado para dar suporte a controles que atuam como contêineres para uma coleção de elementos filho.

Os filhos do elemento container devem implementar [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) e ser organizados em um sistema de coordenadas lógico bidimensional que possa ser percorrido por linha e coluna. Esse padrão de controle é análogo a [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) com a distinção de que qualquer controle que implementa [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) também deve expor uma relação de cabeçalho de coluna e/ou linha para cada elemento filho. Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **ITableProvider**](#required-members-for-itableprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle de **tabela** , observe as seguintes diretrizes e convenções:

-   O acesso ao conteúdo de células individuais é por meio de um sistema de coordenadas lógica bidimensional ou uma matriz fornecida pela implementação de [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)necessária e simultânea.
-   Um cabeçalho de coluna ou de linha pode estar contido em um objeto de tabela ou ser um objeto de cabeçalho separado que está associado a um objeto de tabela.
-   Cabeçalhos de coluna e linha podem incluir um cabeçalho principal, bem como quaisquer cabeçalhos de suporte.
    > [!Note]  
    > esse conceito se torna evidente em uma planilha Microsoft Excel em que um usuário definiu uma coluna de **nome** . Agora, esta coluna tem dois cabeçalhos, incluindo o primeiro cabeçalho de **nome** definido pelo usuário e a designação alfanumérica para aquela coluna atribuída pelo aplicativo.

     

-   Consulte [padrão de controle de grade](uiauto-implementinggrid.md) para funcionalidade de grade relacionada.

    A imagem a seguir mostra uma tabela com cabeçalhos de coluna complexos.

    ![tabela com cabeçalhos de coluna complexos](images/uia-valuepattern-colorpicker.jpg)

    A imagem a seguir mostra uma tabela com uma propriedade [**ITableProvider:: RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) ambígua.

    ![tabela com uma propriedade RowOrColumnMajor ambígua](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a>Membros necessários para **ITableProvider**

As propriedades e os métodos a seguir são necessários para implementar a interface [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) .



| Membros necessários                                                   | Tipo de membro | Observações |
|--------------------------------------------------------------------|-------------|-------|
| [**RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | Propriedade    | Nenhum  |
| [**GetColumnHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | Método      | Nenhum  |
| [**GetRowHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | Método      | Nenhum  |



 

Este padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Padrão de controle TableItem](uiauto-implementingtableitem.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




