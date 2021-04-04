---
description: A ação InstallInitialize e a ação InstallFinalize marcam o início e o final de uma sequência de ações que alteram o sistema.
ms.assetid: c2637070-3fd9-422c-9252-cf15045c6485
title: Ação InstallInitialize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80d500779ed018905edfc5347d85d21cc40e6175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647325"
---
# <a name="installinitialize-action"></a>Ação InstallInitialize

A ação InstallInitialize e a ação [InstallFinalize](installfinalize-action.md) marcam o início e o final de uma sequência de ações que alteram o sistema.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação InstallInitialize deve ser sequenciada antes de qualquer ação que altere o sistema, como a ação [InstallFiles](installfiles-action.md) , a ação [WriteRegistryValues](writeregistryvalues-action.md) , a ação [SelfRegModules](selfregmodules-action.md) e a ação [ProcessComponents](processcomponents-action.md) . A ação InstallInitialize deve, portanto, ser sequenciada antes da ação [InstallFinalize](installfinalize-action.md) e da ação [InstallExecute](installexecute-action.md) .

As [ações personalizadas](custom-actions.md) que modificam o pacote de Windows Installer, por exemplo, adicionando linhas a uma tabela que manipula recursos instaláveis, como a tabela de [registro](registry-table.md) ou a tabela [duplicatafile](duplicatefile-table.md) , devem ser sequenciadas antes da ação InstallInitialize.

## <a name="actiondata-messages"></a>Mensagens ActionData

Não há nenhuma mensagem ActionData.

 

 



