---
description: O UpgradeCode é usado principalmente para dar suporte a atualizações principais, embora os patches de atualização pequenos e pequenos possam usar o UpgradeCode para validação do produto.
ms.assetid: de62bb80-56a0-4652-9509-5d36ed171c69
title: Usando um UpgradeCode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf32d40364653527b9f906e6dd42de64bb9f697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828020"
---
# <a name="using-an-upgradecode"></a>Usando um UpgradeCode

O [**UpgradeCode**](upgradecode.md) é usado principalmente para dar suporte a atualizações principais, embora os patches de atualização pequenos e pequenos possam usar o **UpgradeCode** para validação do produto. Durante atualizações principais, as ações [FindRelatedProducts](findrelatedproducts-action.md), [MigrateFeatureStates](migratefeaturestates-action.md)e [RemoveExistingProducts](removeexistingproducts-action.md) detectam, migram e removem versões anteriores do produto. A ação FindRelatedProducts pesquisa produtos usando critérios baseados em **UpgradeCode**, [**ProductLanguage**](productlanguage.md)e [**ProductVersion**](productversion.md). Esses critérios são especificados na tabela de [atualização](upgrade-table.md) .

Considerando os critérios usados pela ação [FindRelatedProducts](findrelatedproducts-action.md) , o [**UpgradeCode**](upgradecode.md) pode ser o mesmo para diferentes idiomas e versões de um único produto. Isso ocorre porque a tabela de [atualização](upgrade-table.md) permite diferenciar os produtos em linhas de versão e idioma.

Em diferentes versões do mesmo produto, talvez você nunca precise alterar o [**UpgradeCode**](upgradecode.md). Cada produto autônomo deve ter seu próprio **UpgradeCode**. Um conjunto de produtos também deve ter seu próprio **UpgradeCode**. Isso permitirá que o pacote atualize versões anteriores do pacote ou de produtos autônomos usando várias linhas na [tabela de atualização](upgrade-table.md).

Os dois cenários a seguir ilustram o uso do [**UpgradeCode**](upgradecode.md).

-   O produto A e o produto B foram fornecidos com o mesmo [**ProductLanguage**](productlanguage.md), [**ProductVersion**](productversion.md)e [**UpgradeCode**](upgradecode.md). O produto A e o produto B têm diferentes [**ProductCode**](productcode.md). Como os produtos foram atribuídos ao mesmo **UpgradeCode**, a tabela de [atualização](upgrade-table.md) não pode ser criada para diferenciar a versão mais antiga do produto a da versão mais antiga do produto B. Nesse caso, você não poderá ter uma instalação de atualização do produto A que ignore o produto B. Como esses eram produtos diferentes, eles devem ter sido atribuídos a cada um **UpgradeCode** diferente.
-   As versões em inglês e francês do produto A foram enviadas com o mesmo [**ProductVersion**](productversion.md) e [**UpgradeCode**](upgradecode.md). As versões Inglês e francês do produto A têm diferentes [**ProductLanguages**](productlanguage.md) e [**ProductCode**](productcode.md). Embora as versões do idioma inglês e francês compartilhem o mesmo **UpgradeCode**, é possível criar a tabela de [atualização](upgrade-table.md) de modo que apenas a versão mais antiga do idioma inglês seja detectada e atualizada e a versão mais antiga do francês seja ignorada. Versões de idioma diferentes de um produto podem usar o mesmo **UpgradeCode**.

 

 



