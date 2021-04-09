---
description: Uma tabela de componentes é necessária em cada módulo de mesclagem.
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: Criando tabelas de componentes do módulo de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46557541b3a6b89841fe3e26cef7c00e59dc3911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010915"
---
# <a name="authoring-merge-module-component-tables"></a><span data-ttu-id="54a49-103">Criando tabelas de componentes do módulo de mesclagem</span><span class="sxs-lookup"><span data-stu-id="54a49-103">Authoring Merge Module Component Tables</span></span>

<span data-ttu-id="54a49-104">Uma [tabela de componentes](component-table.md) é necessária em cada módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="54a49-104">A [Component table](component-table.md) is required in every merge module.</span></span> <span data-ttu-id="54a49-105">Esta tabela contém um registro para cada componente fornecido pelo módulo de mesclagem para o arquivo. msi de destino.</span><span class="sxs-lookup"><span data-stu-id="54a49-105">This table contains a record for each component delivered by the merge module to the target .msi file.</span></span> <span data-ttu-id="54a49-106">Observe que cada um desses componentes também deve ser especificado na [tabela ModuleComponents](modulecomponents-table.md) , descrita em [criando tabelas ModuleComponents](authoring-modulecomponents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="54a49-106">Note that each of these components must also be specified in the [ModuleComponents table](modulecomponents-table.md) described in [Authoring ModuleComponents Tables](authoring-modulecomponents-tables.md).</span></span>

<span data-ttu-id="54a49-107">Use a Convenção de nomenclatura padrão ao inserir nomes na coluna componente para garantir que o identificador de cada componente seja exclusivo para todos os módulos de mesclagem e bancos de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="54a49-107">Use the standard naming convention when entering names into the Component column to ensure that the identifier for each component is unique for all merge modules and installation databases.</span></span> <span data-ttu-id="54a49-108">Para obter mais informações, consulte [nomeando chaves primárias em bancos de dados do módulo de mesclagem](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="54a49-108">For more information, see [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

<span data-ttu-id="54a49-109">Preencha os campos restantes em cada registro, conforme descrito em um banco de dados de instalação na [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="54a49-109">Complete the remaining fields in each record as described for an installation database in [Component table](component-table.md).</span></span> <span data-ttu-id="54a49-110">Os componentes adicionados a um pacote por um módulo de mesclagem devem aderir às diretrizes para componentes válidos do Windows Installer descritos nas seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="54a49-110">The components added to a package by a merge module must adhere to the guidelines for valid Windows Installer Components described in the following sections:</span></span>

-   [<span data-ttu-id="54a49-111">Componentes do Windows Installer</span><span class="sxs-lookup"><span data-stu-id="54a49-111">Windows Installer Components</span></span>](windows-installer-components.md)
-   [<span data-ttu-id="54a49-112">Organizando aplicativos em componentes</span><span class="sxs-lookup"><span data-stu-id="54a49-112">Organizing Applications into Components</span></span>](organizing-applications-into-components.md)

 

 



