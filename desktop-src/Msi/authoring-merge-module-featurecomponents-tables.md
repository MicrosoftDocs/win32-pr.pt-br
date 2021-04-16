---
description: Uma tabela FeatureComponents em branco é necessária em cada módulo de mesclagem. Essa tabela vazia fornecerá um esquema para a ferramenta de mesclagem se o arquivo. msi de destino não tiver sua própria tabela FeatureComponents.
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: Criando tabelas FeatureComponents do módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3522f32f91a66df93e9096bf9c528f8d00e11f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750821"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a><span data-ttu-id="ad231-104">Criando tabelas FeatureComponents do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="ad231-104">Authoring Merge Module FeatureComponents Tables</span></span>

<span data-ttu-id="ad231-105">Uma [tabela FeatureComponents](featurecomponents-table.md) em branco é necessária em cada módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="ad231-105">A blank [FeatureComponents table](featurecomponents-table.md) is required in every merge module.</span></span> <span data-ttu-id="ad231-106">Essa tabela vazia fornecerá um esquema para a ferramenta de mesclagem se o arquivo. msi de destino não tiver sua própria tabela FeatureComponents.</span><span class="sxs-lookup"><span data-stu-id="ad231-106">This empty table provides a schema for the merge tool if the target .msi file does not have its own FeatureComponents table.</span></span>

<span data-ttu-id="ad231-107">Se, e somente se, não houver nenhuma tabela FeatureComponents no arquivo. msi de destino, a ferramenta de mesclagem usará a tabela em branco fornecida no módulo.</span><span class="sxs-lookup"><span data-stu-id="ad231-107">If, and only if, there is no FeatureComponents table in the target .msi file does the merge tool use the blank table provided in the module.</span></span> <span data-ttu-id="ad231-108">Nesse caso, a ferramenta de mesclagem cria uma tabela duplicada no arquivo. msi de destino e adiciona linhas que associam os novos componentes no módulo de mesclagem aos recursos no pacote de instalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ad231-108">In this case, the merge tool creates a duplicate table in the target .msi file and adds rows that associate the new components in the merge module to the features in the application's installation package.</span></span>

 

 



