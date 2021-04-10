---
description: Windows Installer os desenvolvedores podem usar as diretrizes neste tópico para criar Windows Installer pacotes que contêm assemblies.
ms.assetid: 60687a4f-aaa4-4264-a3f7-0a16eb1fb336
title: Adicionando assemblies a um pacote
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded0795003ae8faf1b7bb945671990767d3eefb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169215"
---
# <a name="adding-assemblies-to-a-package"></a><span data-ttu-id="38a17-103">Adicionando assemblies a um pacote</span><span class="sxs-lookup"><span data-stu-id="38a17-103">Adding Assemblies to a Package</span></span>

<span data-ttu-id="38a17-104">Windows Installer os desenvolvedores podem usar as diretrizes neste tópico para criar Windows Installer pacotes que contêm assemblies.</span><span class="sxs-lookup"><span data-stu-id="38a17-104">Windows Installer developers can use the guidelines in this topic to author Windows Installer packages that contain assemblies.</span></span>

<span data-ttu-id="38a17-105">As diretrizes a seguir se aplicam a assemblies do Win32 e assemblies que o Common Language Runtime do Microsoft .NET Framework usa.</span><span class="sxs-lookup"><span data-stu-id="38a17-105">The following guidelines apply to Win32 assemblies, and assemblies that the common language runtime of the Microsoft .NET Framework uses.</span></span>

-   <span data-ttu-id="38a17-106">Um componente Windows Installer não deve conter mais de um assembly.</span><span class="sxs-lookup"><span data-stu-id="38a17-106">A Windows Installer component should contain no more than one assembly.</span></span>
-   <span data-ttu-id="38a17-107">Todos os arquivos no assembly devem estar em um único componente.</span><span class="sxs-lookup"><span data-stu-id="38a17-107">All of the files in the assembly should be in a single component.</span></span>
-   <span data-ttu-id="38a17-108">Cada componente que contém um assembly deve ter uma entrada na tabela [MsiAssembly](msiassembly-table.md) .</span><span class="sxs-lookup"><span data-stu-id="38a17-108">Each component that contains an assembly should have an entry in the [MsiAssembly](msiassembly-table.md) table.</span></span>
-   <span data-ttu-id="38a17-109">O nome de cache de assembly forte de cada assembly deve ser criado na tabela [MsiAssemblyName](msiassemblyname-table.md) .</span><span class="sxs-lookup"><span data-stu-id="38a17-109">The strong assembly cache name of each assembly should be authored into the [MsiAssemblyName](msiassemblyname-table.md) table.</span></span>
-   <span data-ttu-id="38a17-110">Use a tabela de [registro](registry-table.md) em vez da tabela de [classes](class-table.md) ao registrar a interoperabilidade com para um assembly.</span><span class="sxs-lookup"><span data-stu-id="38a17-110">Use the [Registry](registry-table.md) table instead of the [Class](class-table.md) table when you register COM Interop for an assembly.</span></span>
-   <span data-ttu-id="38a17-111">Os assemblies que têm o mesmo nome forte são o mesmo assembly.</span><span class="sxs-lookup"><span data-stu-id="38a17-111">Assemblies that have the same strong name are the same assembly.</span></span> <span data-ttu-id="38a17-112">Quando o mesmo assembly é instalado por aplicativos diferentes, os componentes que contêm o assembly devem usar o mesmo valor para o ComponentID em suas tabelas de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="38a17-112">When the same assembly is installed by different applications, the components that contain the assembly should use the same value for the ComponentId in their [Component](component-table.md) tables.</span></span>

> [!Note]  
> <span data-ttu-id="38a17-113">Anúncios de produtos identificam assemblies que podem ser instalados e usados por diferentes aplicativos.</span><span class="sxs-lookup"><span data-stu-id="38a17-113">Product advertisements identify assemblies that can be installed and used by different applications.</span></span> <span data-ttu-id="38a17-114">Os anúncios de produtos não identificam assemblies privados.</span><span class="sxs-lookup"><span data-stu-id="38a17-114">Product advertisements do not identify private assemblies.</span></span>

 

## <a name="adding-win32-assemblies"></a><span data-ttu-id="38a17-115">Adicionando assemblies Win32</span><span class="sxs-lookup"><span data-stu-id="38a17-115">Adding Win32 Assemblies</span></span>

<span data-ttu-id="38a17-116">Use as seguintes diretrizes ao incluir assemblies Win32:</span><span class="sxs-lookup"><span data-stu-id="38a17-116">Use the following guidelines when you include Win32 assemblies:</span></span>

-   <span data-ttu-id="38a17-117">O valor KeyPath na tabela de [componentes](component-table.md) para um componente que contém um assembly Win32 não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="38a17-117">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 assembly should not be Null.</span></span>
-   <span data-ttu-id="38a17-118">O valor KeyPath na tabela de [componentes](component-table.md) para um componente que contém um assembly de política do Win32 deve ser o arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="38a17-118">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 policy assembly should be the manifest file.</span></span>
-   <span data-ttu-id="38a17-119">O valor KeyPath na tabela de [componentes](component-table.md) para um componente que contém um assembly Win32, que não é um assembly de política, não deve ser o arquivo de manifesto ou arquivo de catálogo.</span><span class="sxs-lookup"><span data-stu-id="38a17-119">The KeyPath value in the [Component](component-table.md) table for a component that contains a Win32 assembly, that is not a policy assembly, should not be the manifest file or catalog file.</span></span> <span data-ttu-id="38a17-120">Deve ser um arquivo diferente no assembly.</span><span class="sxs-lookup"><span data-stu-id="38a17-120">It should be a different file in the assembly.</span></span>
-   <span data-ttu-id="38a17-121">Adicione uma linha à tabela [MsiAssemblyName](msiassemblyname-table.md) para cada par de nome e valor listado na seção **AssemblyIdentity** do manifesto do assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="38a17-121">Add a row to the [MsiAssemblyName](msiassemblyname-table.md) table for each name and value pair that are listed in the **assemblyIdentity** section of the Win32 assembly's manifest.</span></span>

## <a name="adding-assemblies-used-with-the-net-framework"></a><span data-ttu-id="38a17-122">Adicionando assemblies usados com o .NET Framework</span><span class="sxs-lookup"><span data-stu-id="38a17-122">Adding Assemblies used with the .NET Framework</span></span>

<span data-ttu-id="38a17-123">Use as diretrizes a seguir ao incluir assemblies que o Common Language Runtime do .NET Framework usa.</span><span class="sxs-lookup"><span data-stu-id="38a17-123">Use the following guidelines when you include assemblies that the common language runtime of the .NET Framework uses.</span></span>

-   <span data-ttu-id="38a17-124">O valor KeyPath na tabela de [componentes](component-table.md) para um componente que contém o assembly não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="38a17-124">The KeyPath value in the [Component](component-table.md) table for a component that contains the assembly should not be Null.</span></span>
-   <span data-ttu-id="38a17-125">Quando você instala um assembly usado pelo Common Language Runtime para o cache de assembly global, o valor na \_ coluna aplicativo de arquivo da tabela MsiAssembly deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="38a17-125">When you install an assembly used by the common language runtime to the global assembly cache, the value in the File\_Application column of the MsiAssembly table must be Null.</span></span>
-   <span data-ttu-id="38a17-126">Adicione uma linha à tabela [MsiAssemblyName](msiassemblyname-table.md) para cada atributo do nome forte do assembly.</span><span class="sxs-lookup"><span data-stu-id="38a17-126">Add a row to the [MsiAssemblyName](msiassemblyname-table.md) table for each attribute of the assembly's strong name.</span></span> <span data-ttu-id="38a17-127">Todos os assemblies devem ter o nome, a versão e os atributos de cultura especificados na tabela MsiAssemblyName.</span><span class="sxs-lookup"><span data-stu-id="38a17-127">All assemblies must have the Name, Version, and Culture attributes that are specified in the MsiAssemblyName table.</span></span> <span data-ttu-id="38a17-128">Um atributo publicKeyToken é necessário para um assembly global.</span><span class="sxs-lookup"><span data-stu-id="38a17-128">A publicKeyToken attribute is required for a global assembly.</span></span> <span data-ttu-id="38a17-129">A tabela a seguir é um exemplo da tabela MsiAssemblyName para um assembly global para uso pelo Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="38a17-129">The following table is an example of the MsiAssemblyName table for a global assembly for use by the common language runtime.</span></span>

[<span data-ttu-id="38a17-130">Tabela MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="38a17-130">MsiAssemblyName Table</span></span>](msiassemblyname-table.md)



| <span data-ttu-id="38a17-131">Componente</span><span class="sxs-lookup"><span data-stu-id="38a17-131">Component</span></span>  | <span data-ttu-id="38a17-132">Nome</span><span class="sxs-lookup"><span data-stu-id="38a17-132">Name</span></span>           | <span data-ttu-id="38a17-133">Valor</span><span class="sxs-lookup"><span data-stu-id="38a17-133">Value</span></span>            |
|------------|----------------|------------------|
| <span data-ttu-id="38a17-134">Componente</span><span class="sxs-lookup"><span data-stu-id="38a17-134">ComponentA</span></span> | <span data-ttu-id="38a17-135">Nome</span><span class="sxs-lookup"><span data-stu-id="38a17-135">Name</span></span>           | <span data-ttu-id="38a17-136">simple</span><span class="sxs-lookup"><span data-stu-id="38a17-136">simple</span></span>           |
| <span data-ttu-id="38a17-137">Componente</span><span class="sxs-lookup"><span data-stu-id="38a17-137">ComponentA</span></span> | <span data-ttu-id="38a17-138">version</span><span class="sxs-lookup"><span data-stu-id="38a17-138">version</span></span>        | <span data-ttu-id="38a17-139">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="38a17-139">1.0.0.0</span></span>          |
| <span data-ttu-id="38a17-140">Componente</span><span class="sxs-lookup"><span data-stu-id="38a17-140">ComponentA</span></span> | <span data-ttu-id="38a17-141">Cultura</span><span class="sxs-lookup"><span data-stu-id="38a17-141">Culture</span></span>        | <span data-ttu-id="38a17-142">neutro</span><span class="sxs-lookup"><span data-stu-id="38a17-142">neutral</span></span>          |
| <span data-ttu-id="38a17-143">Componente</span><span class="sxs-lookup"><span data-stu-id="38a17-143">ComponentA</span></span> | <span data-ttu-id="38a17-144">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="38a17-144">publicKeyToken</span></span> | <span data-ttu-id="38a17-145">9d1ec8380f483f5a</span><span class="sxs-lookup"><span data-stu-id="38a17-145">9d1ec8380f483f5a</span></span> |



 

 

 



