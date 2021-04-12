---
description: O banco de dados de um módulo de mesclagem contém todas as propriedades de instalação e a lógica de instalação para o módulo.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Mesclar banco de dados do módulo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74158e38d10b302c28520f6c1736e9cc6d823641
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297080"
---
# <a name="merge-module-database"></a><span data-ttu-id="ac3e6-103">Mesclar banco de dados do módulo</span><span class="sxs-lookup"><span data-stu-id="ac3e6-103">Merge Module Database</span></span>

<span data-ttu-id="ac3e6-104">O banco de dados de um módulo de mesclagem contém todas as propriedades de instalação e a lógica de instalação para o módulo.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-104">The database of a merge module contains all the installation properties and setup logic for the module.</span></span> <span data-ttu-id="ac3e6-105">Ele é essencialmente um [banco de dados do instalador](installer-database.md) simplificado ou arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-105">It is essentially a simplified [installer database](installer-database.md) or .msi file.</span></span> <span data-ttu-id="ac3e6-106">Os arquivos de banco de dados do módulo de mesclagem padrão são indicados por uma extensão. msm.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-106">Standard merge module database files are indicated by an .msm extension.</span></span> <span data-ttu-id="ac3e6-107">Para obter uma lista de todas as tabelas de banco de dados que podem existir em módulos de mesclagem, consulte [mesclar tabelas de banco de dados](merge-module-database-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ac3e6-107">For a list of all database tables that can exist in merge modules, see [Merge Module Database Tables](merge-module-database-tables.md).</span></span> <span data-ttu-id="ac3e6-108">As tabelas a seguir são necessárias no banco de dados de cada arquivo. msm:</span><span class="sxs-lookup"><span data-stu-id="ac3e6-108">The following tables are required in the database of every .msm file:</span></span>

[<span data-ttu-id="ac3e6-109">Componente</span><span class="sxs-lookup"><span data-stu-id="ac3e6-109">Component</span></span>](component-table.md)

[<span data-ttu-id="ac3e6-110">Diretório</span><span class="sxs-lookup"><span data-stu-id="ac3e6-110">Directory</span></span>](directory-table.md)

[<span data-ttu-id="ac3e6-111">FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="ac3e6-111">FeatureComponents</span></span>](featurecomponents-table.md)

[<span data-ttu-id="ac3e6-112">Arquivo</span><span class="sxs-lookup"><span data-stu-id="ac3e6-112">File</span></span>](file-table.md)

[<span data-ttu-id="ac3e6-113">ModuleSignature</span><span class="sxs-lookup"><span data-stu-id="ac3e6-113">ModuleSignature</span></span>](modulesignature-table.md)

[<span data-ttu-id="ac3e6-114">ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="ac3e6-114">ModuleComponents</span></span>](modulecomponents-table.md)

<span data-ttu-id="ac3e6-115">Observe que o componente, o diretório, o FeatureComponents e as tabelas de arquivos também estão presentes em todos os arquivos. msi.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-115">Note that the Component, Directory, FeatureComponents, and File tables are also present in all .msi files.</span></span> <span data-ttu-id="ac3e6-116">Um banco de dados de módulo de mesclagem não contém uma [tabela de recursos](feature-table.md) e, portanto, o arquivo. msm não pode ser instalado sozinha.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-116">A merge module database does not contain a [Feature table](feature-table.md) and so the .msm file cannot be installed alone.</span></span> <span data-ttu-id="ac3e6-117">Para instalar um módulo de mesclagem, ele deve primeiro ser mesclado usando uma ferramenta de mesclagem em um arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-117">To install a merge module, it must first be merged by using a merge tool into an .msi file.</span></span>

<span data-ttu-id="ac3e6-118">A [tabela ModuleSignature](modulesignature-table.md) está presente apenas em arquivos. msi que foram mesclados com pelo menos um arquivo. msm.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-118">The [ModuleSignature Table](modulesignature-table.md) is only present in .msi files that has been merged with at least one .msm file.</span></span> <span data-ttu-id="ac3e6-119">Se essa tabela estiver presente em um arquivo. msi, ela conterá um registro para cada módulo de mesclagem que foi mesclado anteriormente no banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-119">If this table is present in an .msi file, it contains one record for each merge module that has been previously merged into the installation database.</span></span>

<span data-ttu-id="ac3e6-120">Os módulos de mesclagem podem conter tabelas de sequência MergeModule opcionais.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-120">Merge modules may contain optional MergeModule Sequence tables.</span></span> <span data-ttu-id="ac3e6-121">Essas tabelas ocorrem somente em arquivos. msm.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-121">These tables occur only in .msm files.</span></span> <span data-ttu-id="ac3e6-122">Quando os arquivos. msm são mesclados em um arquivo. msi, essas tabelas modificam as [*tabelas de sequência*](s-gly.md) de ação do arquivo. msi.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-122">When the .msm files are merged into an .msi file, these tables modify the action [*sequence tables*](s-gly.md) of the .msi file.</span></span>

<span data-ttu-id="ac3e6-123">Os módulos de mesclagem podem conter tabelas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-123">Merge modules may contain custom tables.</span></span> <span data-ttu-id="ac3e6-124">Essas tabelas são usadas por [ações personalizadas](custom-actions.md) definidas no módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-124">These tables are used by [custom actions](custom-actions.md) defined in the merge module.</span></span>

<span data-ttu-id="ac3e6-125">Os módulos de mesclagem raramente exigem tabelas de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-125">Merge modules rarely require user interface tables.</span></span> <span data-ttu-id="ac3e6-126">Essas tabelas precisam estar presentes apenas em casos raros em que o módulo de mesclagem requer entrada do usuário durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="ac3e6-126">These tables need to be present only in rare cases where the merge module requires input from the user during installation.</span></span> <span data-ttu-id="ac3e6-127">Para obter mais informações, consulte [Criando interfaces do usuário em módulos de mesclagem](authoring-user-interfaces-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="ac3e6-127">For more information, see [Authoring User Interfaces in Merge Modules](authoring-user-interfaces-in-merge-modules.md).</span></span>

 

 



