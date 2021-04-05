---
description: ICE13 valida que as caixas de diálogo em tabelas de sequência aparecem nas tabelas AdminUISequence ou InstallUISequence. As caixas de diálogo não devem ser listadas nas tabelas InstallExecuteSequence, AdminExecuteSequence ou AdvtExecuteSequence.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fff440217ccffe41d5e4036f4ea0d03d1eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922021"
---
# <a name="ice13"></a>ICE13

ICE13 valida que as caixas de diálogo em tabelas de sequência aparecem nas tabelas [AdminUISequence](adminuisequence-table.md)ou [InstallUISequence](installuisequence-table.md) . As caixas de diálogo não devem ser listadas nas tabelas [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)ou [AdvtExecuteSequence](advtexecutesequence-table.md) .

## <a name="result"></a>Resultado

ICE13 posta uma mensagem de erro se uma caixa de diálogo aparecer em uma tabela de sequência de execução.

## <a name="example"></a>Exemplo

Para o exemplo a seguir, ICE13 posta uma mensagem de erro informando que o ' WelcomeDialog ' não pode ser listado na tabela ' InstallExecuteSequence '.

[Tabela InstallExecuteSequence](installexecutesequence-table.md) (parcial)



| Ação          |
|-----------------|
| InstallFinalize |
| CostFinalize    |
| WelcomeDialog   |



 

[Tabela InstallUISequence](installuisequence-table.md) (parcial)



| Ação         |
|----------------|
| CostFinalize   |
| CostInitialize |
| BrowseDialog   |



 

[Tabela de diálogo](dialog-table.md) (parcial)



| caixa de diálogo        |
|---------------|
| BrowseDialog  |
| WelcomeDialog |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



