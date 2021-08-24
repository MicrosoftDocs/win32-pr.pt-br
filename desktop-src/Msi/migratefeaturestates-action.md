---
description: A ação MigrateFeatureStates é usada durante a atualização e ao instalar um novo aplicativo em um aplicativo relacionado.
ms.assetid: 3f53c555-02a9-4249-9f1a-98cd655fc79f
title: Ação MigrateFeatureStates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbac96a3b2babf5f92ae8078ecc703875c09a0e2f61155fd565985919b5a6393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745166"
---
# <a name="migratefeaturestates-action"></a>Ação MigrateFeatureStates

A ação MigrateFeatureStates é usada durante a atualização e ao instalar um novo aplicativo em um aplicativo relacionado. MigrateFeatureStates lê os Estados de recursos no aplicativo existente e define esses Estados de recursos na instalação pendente. O método só é útil quando a nova árvore de recursos não mudou muito do original.

A ação MigrateFeatureStates é executada apenas na primeira vez em que o produto é instalado. A ação MigrateFeatureStates não é executada durante o modo de manutenção ou a desinstalação.

A ação MigrateFeatureStates é executada por meio de cada registro da [tabela de atualização](upgrade-table.md) em sequência e compara o código de atualização, a versão do produto e o idioma em cada linha para todos os produtos instalados no sistema. Se a ação MigrateFeatureStates detectar uma correspondência e se o sinalizador de bit msidbUpgradeAttributesMigrateFeatures estiver definido na coluna atributos da tabela de atualização, o instalador consultará os Estados de recurso existentes para o produto e definirá esses Estados para os mesmos recursos no novo aplicativo. A ação migrará apenas os Estados do recurso se a propriedade [**preselecionada**](preselected.md) não estiver definida.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação MigrateFeatureStates deve vir imediatamente após a [ação CostFinalize](costfinalize-action.md). MigrateFeatureStates deve ser sequenciado na [tabela InstallUISequence](installuisequence-table.md) e na [tabela InstallExecuteSequence](installexecutesequence-table.md). O instalador impede que o MigrateFeatureStates seja executado em InstallExecuteSequence se a ação já tiver sido executada no InstallUISequence.

## <a name="actiondata-messages"></a>Mensagens ActionData

MigrateFeatureSettings envia uma mensagem de dados de ação para cada produto.

## <a name="remarks"></a>Comentários

Se mais de um produto instalado compartilhar um recurso, o estado de instalação desse recurso poderá ser diferente entre os produtos. A ação MigrateFeatureState usa a seguinte ordem de precedência ao migrar Estados de instalação de recursos: executar local, executar da origem, anunciado e desinstalado. Por exemplo, o produto instalado A pode ter o recurso Y como INSTALLstate \_ local e o produto B instalado pode ter o recurso y como InstallState \_ ausente. Se uma atualização instalar o produto C e migrar o estado de instalação do recurso Y, o MigrateFeatureState definirá o estado de instalação do recurso Y no produto C para INSTALLstate \_ local.

Para obter mais informações sobre como usar a ação MigrateFeatureStates para atualizações de produto, consulte [preparando um aplicativo para atualizações principais futuras](preparing-an-application-for-future-major-upgrades.md).

 

 



