---
description: Crítico para organizar de quais arquivos de qual gravador deve ser feito backup ou restaurado é o conceito de um componente.
ms.assetid: 5f85bd0e-31bb-45aa-af7c-15299ed31b26
title: Componentes de metadados do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c913262158d59a69de21a6e0d49e31979c1a0cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811380"
---
# <a name="vss-metadata-components"></a><span data-ttu-id="f2462-103">Componentes de metadados do VSS</span><span class="sxs-lookup"><span data-stu-id="f2462-103">VSS Metadata Components</span></span>

<span data-ttu-id="f2462-104">Crítico para organizar de quais arquivos de qual gravador deve ser feito backup ou restaurado é o conceito de um [*componente*](vssgloss-c.md).</span><span class="sxs-lookup"><span data-stu-id="f2462-104">Critical to organizing which files of which writer are to be backed up or restored is the concept of a [*component*](vssgloss-c.md).</span></span>

<span data-ttu-id="f2462-105">Os componentes permitem que um gravador indique para um mecanismo de backup como seus arquivos devem ser organizados, as dependências entre os arquivos e os tipos de dados que esses arquivos podem conter.</span><span class="sxs-lookup"><span data-stu-id="f2462-105">Components allow a writer to indicate to a backup engine how its files are to be organized, dependencies between files, and what type of data those files can contain.</span></span> <span data-ttu-id="f2462-106">Isso permite que um mecanismo de backup decida como armazenar arquivos para obter máxima eficiência.</span><span class="sxs-lookup"><span data-stu-id="f2462-106">This allows a backup engine to decide how to store files for maximum efficiency.</span></span>

<span data-ttu-id="f2462-107">Além disso, os aplicativos baseados em VSS usam componentes como os blocos de construção para seus metadados e a mídia para a comunicação do gravador/solicitante.</span><span class="sxs-lookup"><span data-stu-id="f2462-107">In addition, VSS-based applications use components as the building blocks for their metadata and the medium for writer/requester communication.</span></span>

<span data-ttu-id="f2462-108">Gravadores e solicitantes armazenam informações sobre componentes separadamente — no documento de metadados do gravador e no documento de componentes de backup, respectivamente, e as informações diferem em cada representação.</span><span class="sxs-lookup"><span data-stu-id="f2462-108">Writers and requesters store information about components separately—in the Writer Metadata Document and the Backup Components Document, respectively—and the information differs in each representation.</span></span>

<span data-ttu-id="f2462-109">As informações de componente nos documentos de metadados do gravador incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f2462-109">Component information in Writer Metadata Documents includes the following:</span></span>

-   <span data-ttu-id="f2462-110">Informações de apenas um gravador em cada documento</span><span class="sxs-lookup"><span data-stu-id="f2462-110">Information from only one writer in each document</span></span>
-   <span data-ttu-id="f2462-111">Todos os componentes do escritor, se eles podem ser [*explicitamente incluídos*](vssgloss-e.md) ou devem ser [*incluídos implicitamente*](vssgloss-i.md) em uma operação de backup ou restauração</span><span class="sxs-lookup"><span data-stu-id="f2462-111">All of that writer's components, whether they can be [*explicitly included*](vssgloss-e.md) or must be [*implicitly included*](vssgloss-i.md) in a backup or restore operation</span></span>
-   <span data-ttu-id="f2462-112">Informações de [*caminho lógico*](vssgloss-l.md) usadas para associar uma selecionável para o componente de backup com um determinado não selecionável para componentes de backup, formando assim um conjunto de componentes</span><span class="sxs-lookup"><span data-stu-id="f2462-112">[*Logical path*](vssgloss-l.md) information used to associate a selectable for backup component with particular nonselectable for backup components, thus forming a component set</span></span>
-   <span data-ttu-id="f2462-113">As informações do [*conjunto de arquivos*](vssgloss-f.md) — caminho, especificação de arquivo e sinalizador de recursão — gerenciado para cada componente</span><span class="sxs-lookup"><span data-stu-id="f2462-113">The [*file set*](vssgloss-f.md) information—path, file specification, and recursion flag—managed for each component</span></span>

<span data-ttu-id="f2462-114">Os documentos de metadados do gravador também contêm informações de metadados no nível do gravador, como métodos de restauração e mapeamentos de local alternativos para restauração.</span><span class="sxs-lookup"><span data-stu-id="f2462-114">Writer Metadata Documents also contain writer-level metadata information, such as restore methods and alternate location mappings for restore.</span></span> <span data-ttu-id="f2462-115">Os documentos de metadados do gravador são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f2462-115">Writer Metadata Documents are read-only.</span></span> <span data-ttu-id="f2462-116">A interface para examinar essas informações é [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).</span><span class="sxs-lookup"><span data-stu-id="f2462-116">The interface for examining this information is [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).</span></span>

<span data-ttu-id="f2462-117">As informações de componente em documentos de componentes de backup incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f2462-117">Component information in Backup Components Documents includes the following:</span></span>

-   <span data-ttu-id="f2462-118">Apenas informações sobre componentes explicitamente incluídos</span><span class="sxs-lookup"><span data-stu-id="f2462-118">Only information on explicitly included components</span></span>
-   <span data-ttu-id="f2462-119">Informações de metadados em nível de gravador, como mapeamentos e restaurações de local alternativos</span><span class="sxs-lookup"><span data-stu-id="f2462-119">Writer-level metadata information, such as alternate location mappings and restore</span></span>
-   <span data-ttu-id="f2462-120">Informações de estado que descrevem uma operação de backup ou restauração</span><span class="sxs-lookup"><span data-stu-id="f2462-120">State information describing a backup or restore operation</span></span>

<span data-ttu-id="f2462-121">Os documentos de componente de backup não contêm informações sobre [*conjuntos de arquivos*](vssgloss-f.md)de componentes.</span><span class="sxs-lookup"><span data-stu-id="f2462-121">Backup Component Documents do not contain information on components' [*file sets*](vssgloss-f.md).</span></span> <span data-ttu-id="f2462-122">Os documentos do componente de backup não são somente leitura e podem ser modificados pelo gravador.</span><span class="sxs-lookup"><span data-stu-id="f2462-122">Backup Component Documents are not read-only and can be modified by the writer.</span></span> <span data-ttu-id="f2462-123">A interface para acessar essas informações é [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).</span><span class="sxs-lookup"><span data-stu-id="f2462-123">The interface for accessing this information is [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).</span></span>

<span data-ttu-id="f2462-124">O ciclo de vida e a relação entre as duas expressões de um componente podem ser compreendidos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f2462-124">The life cycle and relationship between the two expressions of a component can be understood as follows:</span></span>

-   <span data-ttu-id="f2462-125">Os gravadores são responsáveis pelas definições iniciais dos componentes.</span><span class="sxs-lookup"><span data-stu-id="f2462-125">Writers are responsible for the initial definitions of components.</span></span>
-   <span data-ttu-id="f2462-126">Um solicitante examina os metadados de todos os gravadores e seus componentes.</span><span class="sxs-lookup"><span data-stu-id="f2462-126">A requester examines the metadata of all writers and their components.</span></span>
-   <span data-ttu-id="f2462-127">Das informações de seleção e caminho lógico dos componentes, um solicitante determina quais componentes devem ser incluídos explicitamente, que podem ser incluídos explicitamente, que definem os conjuntos de componentes e que são membros de conjuntos de componentes.</span><span class="sxs-lookup"><span data-stu-id="f2462-127">From components' selectability and logical path information, a requester determines which components must be explicitly included, which may be explicitly included, which define component sets, and which are members of component sets.</span></span>
-   <span data-ttu-id="f2462-128">Um solicitante adiciona os componentes que exigem inclusão explícita e inclui implicitamente subcomponentes em [*conjuntos de componentes*](/windows) (cujas informações não estão no documento de componentes de backup).</span><span class="sxs-lookup"><span data-stu-id="f2462-128">A requester adds those components that require explicit inclusion, and implicitly includes subcomponents in [*component sets*](/windows) (whose information is not in the Backup Components Document).</span></span>
-   <span data-ttu-id="f2462-129">Ao manipular eventos, gravadores e solicitantes podem modificar e examinar as informações de componente armazenadas no documento de componentes de backup para coordenar suas atividades.</span><span class="sxs-lookup"><span data-stu-id="f2462-129">When handling events, writers and requesters may modify and examine the component information stored in the Backup Components Document to coordinate their activity.</span></span>

<span data-ttu-id="f2462-130">As informações de componente do gravador e do solicitante são necessárias para executar corretamente as operações de backup e restauração, e ambas devem ser armazenadas com os dados submetidos a backup:</span><span class="sxs-lookup"><span data-stu-id="f2462-130">Both the writer and the requester versions component information are required to properly execute backup and restore operations, and both must be stored with any backed-up data:</span></span>

-   [<span data-ttu-id="f2462-131">Tipos de componentes</span><span class="sxs-lookup"><span data-stu-id="f2462-131">Component Types</span></span>](component-types.md)
-   [<span data-ttu-id="f2462-132">Definição de componentes por gravadores</span><span class="sxs-lookup"><span data-stu-id="f2462-132">Definition of Components by Writers</span></span>](definition-of-components-by-writers.md)
-   [<span data-ttu-id="f2462-133">Uso de componentes pelo solicitante</span><span class="sxs-lookup"><span data-stu-id="f2462-133">Use of Components by the Requester</span></span>](use-of-components-by-the-requestor.md)

 

 
