---
title: Padrão de controle de planilha
description: Descreve as diretrizes e convenções para implementar o ISpreadsheetProvider, incluindo informações sobre métodos.
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- Automação da interface do usuário, implementação do padrão de controle da planilha
- Automação da interface do usuário, padrão de controle da planilha
- Automação da interface do usuário, ISpreadsheetProvider
- ISpreadsheetProvider
- Implementando o padrão de controle da planilha de automação da interface
- padrão de controle de planilha
- padrões de controle, ISpreadsheetProvider
- padrões de controle, implementação da planilha de automação da interface do usuário
- padrões de controle, planilha
- interfaces, ISpreadsheetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be34174745ccf91435db92665b98eb387f7241a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294273"
---
# <a name="spreadsheet-control-pattern"></a>Padrão de controle de planilha

Descreve as diretrizes e convenções para implementar o [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), incluindo informações sobre métodos. Links para referências adicionais são listados no final do tópico. O padrão de controle de **planilha** é usado para expor o conteúdo de uma planilha ou outro documento baseado em grade.

O padrão de controle de **planilha** está fortemente relacionado ao padrão de controle de [grade](uiauto-implementinggrid.md) ; os controles que implementam o padrão de controle de **planilha** também devem implementar o padrão de controle de grade. Os controles também podem implementar o padrão de controle de [tabela](uiauto-implementingtable.md) , se apropriado. Para obter exemplos de controles que implementam esses padrões de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).

## <a name="implementation-guidelines-and-conventions"></a>Diretrizes e convenções de implementação

Ao implementar o padrão de controle de **planilha** , observe as seguintes diretrizes e convenções:

-   Se uma planilha implementar a interface [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) , suas células deverão implementar a interface [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) .
-   O método [**ISpreadsheetProvider:: GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) destina-se a fornecer o mesmo tipo de navegação que um aplicativo pode fornecer com um recurso de **salto para rótulo** . Muitos programas de planilha permitem que células específicas recebam um nome amigável ou rótulo. O **GetItemByName** permite que o cliente pesquise uma célula com base em seu nome amigável. Esse método não deve recuperar nenhuma célula que contenha o texto de nome porque os resultados podem ser altamente ambíguos. Se o programa de planilha permitir que várias células na mesma planilha tenham o mesmo nome amigável ou rótulo, o comportamento da automação da interface do usuário da Microsoft será indefinido.

## <a name="required-members-for-ispreadsheetprovider"></a>Membros necessários para **ISpreadsheetProvider**

O método a seguir é necessário para implementar a interface [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) .



| Membros necessários                                                       | Tipo de membro | Observações |
|------------------------------------------------------------------------|-------------|-------|
| [**GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | Método      | Nenhum  |



 

Este padrão de controle não tem eventos associados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md)
</dt> <dt>

[Visão Geral de Padrões de Controle de Automação de Interface de Usuário](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Visão geral da árvore de automação de interface do usuário](uiauto-treeoverview.md)
</dt> </dl>

 

 