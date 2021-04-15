---
description: Há duas maneiras de criar o banco de dados de instalação do Windows Installer de modo que uma ação seja chamada apenas quando o pacote for desinstalado.
ms.assetid: 67b205bb-11d8-454f-b5d5-93330219f6cc
title: Ações de condicionamento a serem executadas durante a remoção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0e84f21b42f569744af9b8a7a46bb1e3df7a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505725"
---
# <a name="conditioning-actions-to-run-during-removal"></a>Ações de condicionamento a serem executadas durante a remoção

Há duas maneiras de criar o banco de dados de instalação, de modo que uma ação seja chamada apenas quando o pacote for desinstalado:

-   Se a ação for sequenciada após a [ação InstallValidate](installvalidate-action.md) na [tabela InstallExecuteSequence](installexecutesequence-table.md), o autor do pacote poderá especificar uma condição de Remove = "All" para a ação na coluna Condition. Observe que a propriedade [**Remove**](remove.md) não tem garantia de ser definida como All durante uma desinstalação antes que o instalador execute a ação InstallValidate. Observe que as aspas em volta do valor todos são necessárias nesse caso.
-   Se a ação for sequenciada após a [ação CostFinalize](costfinalize-action.md) e quaisquer ações que possam alterar o estado do recurso, como a [ação MigrateFeatureStates](migratefeaturestates-action.md), a ação poderá ser condicional no estado de um recurso ou componente específico. Consulte [sintaxe de instrução condicional](conditional-statement-syntax.md). Use esta opção para chamar uma ação durante a remoção de um determinado recurso ou componente, o que pode ocorrer fora da remoção completa do aplicativo.

Observe que a propriedade [**installed**](installed.md) pode ser usada em expressões condicionais para determinar se um produto está instalado por computador ou para o usuário atual. Para determinar se o produto está instalado para um usuário diferente, verifique a propriedade [**productstate**](productstate.md) .

Observe que as versões mais antigas de um produto podem ser removidas durante uma atualização pela [ação RemoveExistingProducts](removeexistingproducts-action.md). A [tabela de atualização](upgrade-table.md) também pode definir a propriedade [**Remove**](remove.md) para todos nesse caso. Para determinar se um produto está sendo removido por uma atualização, verifique a propriedade [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) . O instalador só define essa propriedade quando RemoveExistingProducts remove o produto. O instalador não define a propriedade durante uma desinstalação normal, como a remoção com adicionar/remover programas.

 

 



