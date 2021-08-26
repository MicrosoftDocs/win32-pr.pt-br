---
description: A ação InstallInitialize e InstallFinalize marcam o início e o fim de uma sequência de ações que alteram o sistema.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Ação InstallInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7031ab79bc099ea067fd8d83cb83d8cefd1f36a1e83f696a1ee3b4487b3cac88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996566"
---
# <a name="installinitialize-action"></a>Ação InstallInitialize

A ação InstallInitialize e [InstallFinalize](installfinalize-action.md) marcam o início e o fim de uma sequência de ações que alteram o sistema.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação InstallInitialize deve ser sequenciada antes de qualquer ação que altere o sistema, como a ação [InstallFiles,](installfiles-action.md) a ação [WriteRegistryValues,](writeregistryvalues-action.md) a [ação SelfRegModules](selfregmodules-action.md) e a [ação ProcessComponents.](processcomponents-action.md) Portanto, a ação InstallInitialize deve ser sequenciada antes da [ação InstallFinalize](installfinalize-action.md) e da [ação InstallExecute.](installexecute-action.md)

[Ações personalizadas](custom-actions.md) que modificam o pacote do instalador do Windows, por exemplo, adicionando [](registry-table.md) linhas a uma tabela que lida com recursos instaláveis, como a tabela Registro ou a tabela [DuplicateFile,](duplicatefile-table.md) devem ser sequenciadas antes da ação InstallInitialize.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há mensagens ActionData.

 

 



