---
description: Para obter mais informações sobre o diagrama a seguir, consulte a legenda do diagrama de relação de entidade.
ms.assetid: ec4f585d-cbd5-4c25-aaf4-1c1333fd4587
title: Grupo de tabelas principais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a5cc87e80c60505025825353272699db574bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922625"
---
# <a name="core-tables-group"></a><span data-ttu-id="27fa2-103">Grupo de tabelas principais</span><span class="sxs-lookup"><span data-stu-id="27fa2-103">Core Tables Group</span></span>

<span data-ttu-id="27fa2-104">Para obter mais informações sobre o diagrama a seguir, consulte a [legenda do diagrama de relação de entidade](entity-relationship-diagram-legend.md).</span><span class="sxs-lookup"><span data-stu-id="27fa2-104">For more information about the following diagram, see the [entity relationship diagram legend](entity-relationship-diagram-legend.md).</span></span>

![grupo de tabelas principais](images/core.png)

<span data-ttu-id="27fa2-106">O grupo principal consiste em tabelas que descrevem os recursos fundamentais e os componentes do aplicativo e o pacote do instalador.</span><span class="sxs-lookup"><span data-stu-id="27fa2-106">The core group consists of tables describing the fundamental features and components of the application and the installer package.</span></span> <span data-ttu-id="27fa2-107">Os desenvolvedores de instalar pacotes devem, portanto, considerar como preencher essas tabelas primeiro, pois a organização de grande parte do banco de dados ficará aparente com o conteúdo desse grupo.</span><span class="sxs-lookup"><span data-stu-id="27fa2-107">Developers of install packages should therefore consider how to populate these tables first because the organization of much of the database will become apparent from the content of this group.</span></span>

-   <span data-ttu-id="27fa2-108">A [tabela de recursos](feature-table.md) lista todos os recursos que pertencem ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="27fa2-108">The [Feature table](feature-table.md) lists all features belonging to the application.</span></span>
-   <span data-ttu-id="27fa2-109">A [tabela de condição](condition-table.md) contém as expressões condicionais que determinam se um determinado recurso será instalado ou não.</span><span class="sxs-lookup"><span data-stu-id="27fa2-109">The [Condition table](condition-table.md) contains the conditional expressions that determine whether or not a particular feature will be installed.</span></span>
-   <span data-ttu-id="27fa2-110">A [tabela FeatureComponents](featurecomponents-table.md) descreve quais componentes pertencem a cada recurso.</span><span class="sxs-lookup"><span data-stu-id="27fa2-110">The [FeatureComponents table](featurecomponents-table.md) describes which components belong to each feature.</span></span>
-   <span data-ttu-id="27fa2-111">A [tabela de componentes](component-table.md) lista todos os componentes que pertencem à instalação.</span><span class="sxs-lookup"><span data-stu-id="27fa2-111">The [Component table](component-table.md) lists all components belonging to the installation.</span></span>
-   <span data-ttu-id="27fa2-112">A [tabela de diretórios](directory-table.md) lista os diretórios que são necessários durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="27fa2-112">The [Directory table](directory-table.md) lists the directories that are needed during the installation.</span></span> <span data-ttu-id="27fa2-113">Como cada componente deve ser associado a um e apenas um diretório, a tabela de componentes está diretamente relacionada a essa tabela e tem uma chave externa para a tabela de diretórios.</span><span class="sxs-lookup"><span data-stu-id="27fa2-113">Because each component must be associated with one and only one directory, the Component table is closely related to this table and has an external key to the Directory table.</span></span>
-   <span data-ttu-id="27fa2-114">A [tabela PublishComponent](publishcomponent-table.md) lista os recursos e componentes que são publicados para uso por outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="27fa2-114">The [PublishComponent table](publishcomponent-table.md) lists the features and components that are published for use by other applications.</span></span> <span data-ttu-id="27fa2-115">[Componentes e recursos](components-and-features.md) são os dois tipos de anúncio de recursos.</span><span class="sxs-lookup"><span data-stu-id="27fa2-115">[Components and Features](components-and-features.md) are the two types of feature advertisement.</span></span>
-   <span data-ttu-id="27fa2-116">A [tabela MsiAssembly](msiassembly-table.md) Especifica configurações de Windows Installer para assemblies de Common Language Runtime de .NET Framework e assemblies do Win32.</span><span class="sxs-lookup"><span data-stu-id="27fa2-116">The [MsiAssembly table](msiassembly-table.md) specifies Windows Installer settings for .NET Framework common language runtime assemblies and Win32 assemblies.</span></span>
-   <span data-ttu-id="27fa2-117">A [tabela MsiAssemblyName](msiassemblyname-table.md) especifica o esquema para os elementos de um nome de cache de assembly forte para um assembly Common Language Runtime ou Win32.</span><span class="sxs-lookup"><span data-stu-id="27fa2-117">The [MsiAssemblyName table](msiassemblyname-table.md) specifies the schema for the elements of a strong assembly cache name for a common language runtime or Win32 assembly.</span></span>
-   <span data-ttu-id="27fa2-118">A [tabela ComPlus](complus-table.md) contém as informações necessárias para instalar aplicativos com+.</span><span class="sxs-lookup"><span data-stu-id="27fa2-118">The [Complus table](complus-table.md) contains information needed to install COM+ applications.</span></span>
-   <span data-ttu-id="27fa2-119">A [tabela IsolatedComponent](isolatedcomponent-table.md) associa o componente especificado na \_ coluna aplicativo de componente (normalmente um. exe) com o componente especificado na \_ coluna compartilhada componente (normalmente, uma DLL compartilhada).</span><span class="sxs-lookup"><span data-stu-id="27fa2-119">The [IsolatedComponent table](isolatedcomponent-table.md) associates the component specified in the Component\_Application column (commonly an .exe) with the component specified in the Component\_Shared column (commonly a shared DLL).</span></span>
-   <span data-ttu-id="27fa2-120">A [tabela de atualização](upgrade-table.md) contém as informações necessárias durante as [atualizações principais](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="27fa2-120">The [Upgrade table](upgrade-table.md) contains information required during [major upgrades](major-upgrades.md).</span></span>

 

 



