---
description: Você pode controlar quais opções de instalação de recurso estão disponíveis para que os usuários e aplicativos selecionem criando a tabela de recursos e a tabela de componentes.
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: Controlando Estados de seleção de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadedf4b6038f8257d06671e0774afc258391898
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171692"
---
# <a name="controlling-feature-selection-states"></a><span data-ttu-id="ad7dc-103">Controlando Estados de seleção de recursos</span><span class="sxs-lookup"><span data-stu-id="ad7dc-103">Controlling Feature Selection States</span></span>

<span data-ttu-id="ad7dc-104">Você pode controlar quais opções de instalação de recurso estão disponíveis para que os usuários e aplicativos selecionem criando a [tabela de recursos](feature-table.md) e a [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="ad7dc-104">You can control which feature installation options are available for users and applications to select by authoring the [Feature table](feature-table.md) and [Component table](component-table.md).</span></span>

-   <span data-ttu-id="ad7dc-105">Para evitar a seleção do estado de anúncio de um recurso, inclua **msidbFeatureAttributesDisallowAdvertise** no campo atributos do recurso na [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="ad7dc-105">To prevent selection of the advertise state for a feature, include **msidbFeatureAttributesDisallowAdvertise** in the feature's Attributes field in the [Feature table](feature-table.md).</span></span>
-   <span data-ttu-id="ad7dc-106">Para evitar a seleção dos Estados de execução da origem ou execução da rede para um recurso, inclua **msidbComponentAttributesLocalOnly** nos campos de atributos na [tabela de componentes](component-table.md) para cada componente pertencente ao recurso.</span><span class="sxs-lookup"><span data-stu-id="ad7dc-106">To prevent selection of the run-from-source or run-from-network states for a feature, include **msidbComponentAttributesLocalOnly** in the Attributes fields in the [Component table](component-table.md) for every component belonging to the feature.</span></span> <span data-ttu-id="ad7dc-107">Se um recurso não tiver componentes, o recurso sempre terá as opções executar-de-origem e executar-de-meu-computador disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ad7dc-107">If a feature has no components, the feature always has the run-from-source and run-from-my-computer options available.</span></span>
-   <span data-ttu-id="ad7dc-108">Para evitar a seleção do estado de execução de meu computador para um recurso, inclua **msidbComponentAttributesSourceOnly** nos campos de atributos na [tabela de componentes](component-table.md) para cada componente pertencente ao recurso.</span><span class="sxs-lookup"><span data-stu-id="ad7dc-108">To prevent selection of the run-from-my-computer state for a feature, include **msidbComponentAttributesSourceOnly** in the Attributes fields in the [Component table](component-table.md) for every component belonging to the feature.</span></span> <span data-ttu-id="ad7dc-109">Se um recurso não tiver componentes, o recurso sempre terá as opções executar-de-origem e executar-de-meu-computador disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ad7dc-109">If a feature has no components, the feature always has the run-from-source and run-from-my-computer options available.</span></span>
-   <span data-ttu-id="ad7dc-110">Novos recursos filho podem ser criados incluindo **msidbFeatureAttributesFollowParent** e **MsidbFeatureAttributesUIDisallowAbsent** no campo atributos da [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="ad7dc-110">New child features can be authored by including **msidbFeatureAttributesFollowParent** and **msidbFeatureAttributesUIDisallowAbsent** in the Attributes field of the [Feature table](feature-table.md).</span></span>

 

 



