---
description: Há duas maneiras de autor do banco de dados de instalação Windows Instalador, de modo que uma ação seja chamada somente quando o pacote for desinstalado.
ms.assetid: 67b205bb-11d8-454f-b5d5-93330219f6cc
title: Ações de condicionação a executar durante a remoção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fa9596dd6868b105f87c795ad70b6edc5ebac96381ffcc2b8b951947c87568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144319"
---
# <a name="conditioning-actions-to-run-during-removal"></a>Ações de condicionação a executar durante a remoção

Há duas maneiras de autor do banco de dados de instalação, de modo que uma ação seja chamada somente quando o pacote for desinstalado:

-   Se a ação for sequenciada após a ação [InstallValidate](installvalidate-action.md) na tabela [InstallExecuteSequence](installexecutesequence-table.md), o autor do pacote poderá especificar uma condição de REMOVE="ALL" para a ação na coluna Condição. Observe que não [**há garantia de**](remove.md) que a propriedade REMOVE seja definida como ALL durante uma desinstalação antes que o instalador execute a ação InstallValidate. Observe que as aspas em torno do valor ALL são necessárias nesse caso.
-   Se a ação for sequenciada após a ação [CostFinalize](costfinalize-action.md) e qualquer ação que possa alterar o estado do recurso, como a [ação MigrateFeatureStates](migratefeaturestates-action.md), a ação poderá ser condicionada no estado de um recurso ou componente específico. Consulte [Sintaxe de instrução condicional](conditional-statement-syntax.md). Use essa opção para chamar uma ação durante a remoção de um recurso ou componente específico, o que pode ocorrer fora da remoção completa do aplicativo.

Observe que [**a propriedade Instalado**](installed.md) pode ser usada em expressões condicionais para determinar se um produto está instalado por computador ou para o usuário atual. Para determinar se o produto está instalado para um usuário diferente, verifique a [**propriedade ProductState.**](productstate.md)

Observe que as versões mais antigas de um produto podem ser removidas durante uma atualização pela [ação RemoveExistingProducts](removeexistingproducts-action.md). A [tabela Upgrade](upgrade-table.md) também pode definir a propriedade [**REMOVE**](remove.md) como ALL nesse caso. Para determinar se um produto está sendo removido por uma atualização, verifique a [**propriedade UPGRADINGPRODUCTCODE.**](upgradingproductcode.md) O instalador só define essa propriedade quando RemoveExistingProducts remove o produto. O instalador não configura a propriedade durante uma desinstalação normal, como a remoção com adicionar/remover programas.

 

 



