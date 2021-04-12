---
description: A ação FindRelatedProducts é executada em cada registro da tabela de atualização em sequência e compara o código de atualização, a versão do produto e o idioma em cada linha aos produtos instalados no sistema.
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: Ação FindRelatedProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87973631e51315df17a156bc8c57aa9facd84f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297082"
---
# <a name="findrelatedproducts-action"></a>Ação FindRelatedProducts

A ação FindRelatedProducts é executada em cada registro da [tabela de atualização](upgrade-table.md) em sequência e compara o código de atualização, a versão do produto e o idioma em cada linha aos produtos instalados no sistema. Quando o FindRelatedProducts detecta uma correspondência entre as informações de atualização e um produto instalado, ele anexa o código do produto à propriedade especificada na coluna Actionproperty da Atualizaçãotable.

A ação FindRelatedProducts é executada apenas na primeira vez em que o produto é instalado. A ação FindRelatedProducts não é executada durante o modo de manutenção ou a desinstalação.

## <a name="database-tables-queried"></a>Tabelas de banco de dados consultadas

Esta ação consulta a tabela a seguir:

[Atualizar tabela](upgrade-table.md)

## <a name="properties-used"></a>Propriedades usadas

A ação FindRelatedProducts usa a propriedade [**UpgradeCode**](upgradecode.md) e as informações de versão e idioma criadas na tabela de atualização para detectar os produtos instalados afetados pela atualização pendente. Ele acrescenta o código do produto dos produtos detectados à propriedade na coluna Actionproperty da Atualizaçãotable.

O FindRelatedProducts reconhece apenas os produtos existentes que foram instalados usando o Windows Installer com um. msi que define uma propriedade [**UpgradeCode**](upgradecode.md) , uma propriedade [**ProductVersion**](productversion.md) e um valor para a propriedade [**ProductLanguage**](productlanguage.md) que é um dos idiomas listados na propriedade [**Summary do modelo**](template-summary.md) .

Observe que FindRelatedProducts usa o idioma retornado por [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa). Para que o FindRelatedProducts funcione corretamente, o autor do pacote deve ter certeza de que a propriedade [**ProductLanguage**](productlanguage.md) na [tabela de propriedades](property-table.md) está definida como um idioma que também está listado na propriedade [**Summary do modelo**](template-summary.md) . Consulte [preparando um aplicativo para atualizações importantes futuras](preparing-an-application-for-future-major-upgrades.md).

## <a name="sequence-restrictions"></a>Restrições de sequência

FindRelatedProducts deve ser criado na [tabela InstallUISequence](installuisequence-table.md) e nas tabelas [InstallExecuteSequence](installexecutesequence-table.md) . O instalador impede que os produtos FindRelated sejam executados no InstallExecuteSequence se a ação já tiver sido executada no InstallUISequence. A ação FindRelatedProducts deve vir antes da [ação MigrateFeatureStates](migratefeaturestates-action.md) e da [ação RemoveExistingProducts](removeexistingproducts-action.md).

## <a name="actiondata-messages"></a>Mensagens ActionData

O FindRelatedProducts envia uma mensagem de dados de ação para cada produto relacionado que ele detecta no sistema.

 

 



