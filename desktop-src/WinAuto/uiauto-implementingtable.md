---
title: Padrão de controle de tabela
description: Descreve diretrizes e convenções para implementar ITableProvider, incluindo informações sobre propriedades e métodos. O padrão de controle Tabela é usado para dar suporte a controles que atuam como contêineres para uma coleção de elementos filho.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- Automação da Interface do Usuário, implementando o padrão de controle Tabela
- Automação da Interface do Usuário, Padrão de controle de tabela
- Automação da Interface do Usuário,ITableProvider
- ITableProvider
- implementando padrões Automação da Interface do Usuário controle tabela
- Padrões de controle de tabela
- padrões de controle, ITableProvider
- padrões de controle, implementando Automação da Interface do Usuário Tabela
- padrões de controle, Tabela
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

Descreve diretrizes e convenções para implementar [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), incluindo informações sobre propriedades e métodos. O **padrão de** controle Tabela é usado para dar suporte a controles que atuam como contêineres para uma coleção de elementos filho.

Os filhos do elemento de contêiner devem implementar [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) e ser organizados em um sistema de coordenadas lógica bidimensional que pode ser percorrido por linha e coluna. Esse padrão de controle é análogo a [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) com a distinção de que qualquer controle que implemente [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) também deve expor uma relação de coluna e/ou de título de linha para cada elemento filho. Para exemplos de controles que implementam esse padrão de controle, consulte [Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

Este tópico inclui as seções a seguir.

-   [Diretrizes e convenções de implementação](#implementation-guidelines-and-conventions)
-   [Membros necessários para **ITableProvider**](#required-members-for-itableprovider)
-   [Tópicos relacionados](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão **de controle** Tabela, observe as seguintes diretrizes e convenções:

-   O acesso ao conteúdo de células individuais é por meio de um sistema de coordenadas lógica bidimensional ou matriz fornecida pela implementação simultânea necessária de [**IGridProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)
-   Uma coluna ou um header de linha pode estar contido em um objeto de tabela ou ser um objeto de header separado associado a um objeto de tabela.
-   Os headers de coluna e linha podem incluir um header primário, bem como todos os headers de suporte.
    > [!Note]  
    > Esse conceito fica evidente em uma planilha Microsoft Excel em que um usuário definiu uma **coluna Nome.** Essa coluna agora tem dois  títulos, incluindo o título Nome definido pelo usuário e a designação alfanumérico para essa coluna atribuída pelo aplicativo.

     

-   Confira [Padrão de Controle de Grade](uiauto-implementinggrid.md) para ver a funcionalidade de grade relacionada.

    A imagem a seguir mostra uma tabela com os headers de coluna complexos.

    ![tabela com headers de coluna complexos](images/uia-valuepattern-colorpicker.jpg)

    A imagem a seguir mostra uma tabela com uma propriedade [**ITableProvider::RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) ambígua.

    ![table com uma propriedade roworcolumnmajor ambígua](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a>Membros necessários para **ITableProvider**

As seguintes propriedades e métodos são necessários para implementar a interface [**ITableProvider.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)



| Membros necessários                                                   | Tipo de membro | Observações |
|--------------------------------------------------------------------|-------------|-------|
| [**Roworcolumnmajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | Propriedade    | Nenhum  |
| [**GetColumnHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | Método      | Nenhum  |
| [**GetRowHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | Método      | Nenhum  |



 

Esse padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Padrão de controle TableItem](uiauto-implementingtableitem.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 




