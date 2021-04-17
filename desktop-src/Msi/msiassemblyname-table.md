---
description: A tabela MsiAssembly e a tabela MsiAssemblyName especificam Windows Installer configurações para assemblies de Common Language Runtime e assemblies do Win32.
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: Tabela MsiAssemblyName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12008682c82d7be20ed8713d8dc1c416f9c7065c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783268"
---
# <a name="msiassemblyname-table"></a><span data-ttu-id="d9e38-103">Tabela MsiAssemblyName</span><span class="sxs-lookup"><span data-stu-id="d9e38-103">MsiAssemblyName Table</span></span>

<span data-ttu-id="d9e38-104">A tabela [MsiAssembly](msiassembly-table.md) e a tabela MsiAssemblyName especificam Windows Installer configurações para assemblies de Common Language Runtime e assemblies do Win32.</span><span class="sxs-lookup"><span data-stu-id="d9e38-104">The [MsiAssembly Table](msiassembly-table.md) and MsiAssemblyName Table specify Windows Installer settings for common language runtime assemblies and Win32 assemblies.</span></span> <span data-ttu-id="d9e38-105">Para obter informações, consulte [instalação de assemblies no cache de assembly global](installation-of-assemblies-to-the-global-assembly-cache.md) e [instalação de assemblies do Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="d9e38-105">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="d9e38-106">A tabela MsiAssemblyName especifica o esquema para os elementos de um nome de cache de assembly forte para um assembly .NET Framework ou Win32.</span><span class="sxs-lookup"><span data-stu-id="d9e38-106">The MsiAssemblyName Table specifies the schema for the elements of a strong assembly cache name for a .NET Framework or Win32 assembly.</span></span> <span data-ttu-id="d9e38-107">O nome é construído acrescentando todos os elementos com a mesma chave de componente \_ .</span><span class="sxs-lookup"><span data-stu-id="d9e38-107">The name is constructed by appending all elements with the same Component\_ key.</span></span> <span data-ttu-id="d9e38-108">Veja o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9e38-108">See the following example.</span></span>

<span data-ttu-id="d9e38-109">Windows Installer pode instalar assemblies do Win32 como [assemblies lado a lado](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="d9e38-109">Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="d9e38-110">Para obter mais informações, consulte a [API do assembly lado a lado](../sbscs/side-by-side-assembly-api.md).</span><span class="sxs-lookup"><span data-stu-id="d9e38-110">For more information, see the [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).</span></span>

<span data-ttu-id="d9e38-111">A tabela MsiAssemblyName tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="d9e38-111">The MsiAssemblyName Table has the following columns.</span></span>



| <span data-ttu-id="d9e38-112">Coluna</span><span class="sxs-lookup"><span data-stu-id="d9e38-112">Column</span></span>      | <span data-ttu-id="d9e38-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9e38-113">Type</span></span>                         | <span data-ttu-id="d9e38-114">Chave</span><span class="sxs-lookup"><span data-stu-id="d9e38-114">Key</span></span> | <span data-ttu-id="d9e38-115">Nullable</span><span class="sxs-lookup"><span data-stu-id="d9e38-115">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="d9e38-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="d9e38-116">Component\_</span></span> | [<span data-ttu-id="d9e38-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="d9e38-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="d9e38-118">S</span><span class="sxs-lookup"><span data-stu-id="d9e38-118">Y</span></span>   | <span data-ttu-id="d9e38-119">N</span><span class="sxs-lookup"><span data-stu-id="d9e38-119">N</span></span>        |
| <span data-ttu-id="d9e38-120">Nome</span><span class="sxs-lookup"><span data-stu-id="d9e38-120">Name</span></span>        | [<span data-ttu-id="d9e38-121">Text</span><span class="sxs-lookup"><span data-stu-id="d9e38-121">Text</span></span>](text.md)             | <span data-ttu-id="d9e38-122">S</span><span class="sxs-lookup"><span data-stu-id="d9e38-122">Y</span></span>   | <span data-ttu-id="d9e38-123">N</span><span class="sxs-lookup"><span data-stu-id="d9e38-123">N</span></span>        |
| <span data-ttu-id="d9e38-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d9e38-124">Value</span></span>       | [<span data-ttu-id="d9e38-125">Text</span><span class="sxs-lookup"><span data-stu-id="d9e38-125">Text</span></span>](text.md)             | <span data-ttu-id="d9e38-126">N</span><span class="sxs-lookup"><span data-stu-id="d9e38-126">N</span></span>   | <span data-ttu-id="d9e38-127">N</span><span class="sxs-lookup"><span data-stu-id="d9e38-127">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d9e38-128">Colunas</span><span class="sxs-lookup"><span data-stu-id="d9e38-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d9e38-129"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="d9e38-129"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="d9e38-130">A chave na [tabela de componentes](component-table.md) que especifica o componente de Windows Installer que contém esse assembly.</span><span class="sxs-lookup"><span data-stu-id="d9e38-130">Key into the [Component Table](component-table.md) that specifies the Windows Installer component that contains this assembly.</span></span>

</dd> <dt>

<span data-ttu-id="d9e38-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomes</span><span class="sxs-lookup"><span data-stu-id="d9e38-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="d9e38-132">Nome do atributo associado ao valor especificado na coluna valor.</span><span class="sxs-lookup"><span data-stu-id="d9e38-132">Name of the attribute associated with the value specified in the Value column.</span></span>

</dd> <dt>

<span data-ttu-id="d9e38-133"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor</span><span class="sxs-lookup"><span data-stu-id="d9e38-133"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="d9e38-134">Valor associado ao nome especificado na coluna nome.</span><span class="sxs-lookup"><span data-stu-id="d9e38-134">Value associated with the name specified in the Name column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9e38-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="d9e38-135">Remarks</span></span>

<span data-ttu-id="d9e38-136">As informações criadas na tabela MsiAssemblyName devem corresponder às informações no arquivo de manifesto do assembly.</span><span class="sxs-lookup"><span data-stu-id="d9e38-136">The information authored into the MsiAssemblyName Table must match the information in the manifest file of the assembly.</span></span> <span data-ttu-id="d9e38-137">Se as informações no manifesto e na tabela MsiAssemblyName não corresponderem, a remoção do aplicativo poderá deixar o assembly no computador.</span><span class="sxs-lookup"><span data-stu-id="d9e38-137">If the information in the manifest and MsiAssemblyName Table do not match, removal of the application can leave the assembly on the computer.</span></span>

<span data-ttu-id="d9e38-138">Para assemblies do Win32, deve haver uma linha na tabela MsiAssemblyName para cada uma das seguintes entradas no campo Nome: tipo, nome, versão, idioma, publicKeyToken e processorArchitecture.</span><span class="sxs-lookup"><span data-stu-id="d9e38-138">For Win32 assemblies there must be a row in the MsiAssemblyName Table for each of the following entries in the Name field: type, name, version, language, publicKeyToken and processorArchitecture.</span></span> <span data-ttu-id="d9e38-139">O valor correspondente para cada nome pode ser inserido no campo valor.</span><span class="sxs-lookup"><span data-stu-id="d9e38-139">The corresponding value for each name can be entered into the Value field.</span></span> <span data-ttu-id="d9e38-140">Os pares de nome-valor na tabela MsiAssemblyName devem corresponder aos atributos Type, Name, Version, language, publicKeyToken e processorArchitecture no manifesto do assembly.</span><span class="sxs-lookup"><span data-stu-id="d9e38-140">The name-value pairs in MsiAssemblyName Table must match the type, name, version, language, publicKeyToken and processorArchitecture attributes in the manifest of the assembly.</span></span>

<span data-ttu-id="d9e38-141">Para assemblies de Common Language Runtime privada (.NET Frameworkversions 1,0 e 1,1), a tabela MsiAssemblyName deve incluir uma linha para cada uma das seguintes entradas no campo Nome: nome, versão e cultura.</span><span class="sxs-lookup"><span data-stu-id="d9e38-141">For private common language runtime assemblies (.NET Frameworkversions 1.0 and 1.1), the MsiAssemblyName Table must include a row for each of the following entries in the Name field: Name, Version, and Culture.</span></span> <span data-ttu-id="d9e38-142">O valor correspondente para cada nome pode ser inserido no campo valor.</span><span class="sxs-lookup"><span data-stu-id="d9e38-142">The corresponding value for each Name can be entered into the Value field.</span></span>

<span data-ttu-id="d9e38-143">Para assemblies de Common Language Runtime global (.NET Framework versões 1,0 e 1,1), a tabela MsiAssemblyName deve incluir uma linha para cada uma das seguintes entradas no campo Nome: nome, versão, cultura e PublicKeyToken.</span><span class="sxs-lookup"><span data-stu-id="d9e38-143">For global common language runtime assemblies (.NET Framework versions 1.0 and 1.1), the MsiAssemblyName Table must include a row for each of the following entries in the Name field: Name, Version, Culture, and PublicKeyToken.</span></span> <span data-ttu-id="d9e38-144">O valor correspondente para cada nome pode ser inserido no campo valor.</span><span class="sxs-lookup"><span data-stu-id="d9e38-144">The corresponding value for each Name can be entered into the Value field.</span></span>

<span data-ttu-id="d9e38-145">A versão .NET Framework 1,1 é a versão mínima que pode ser usada para executar uma atualização in-loco de um assembly de Common Language Runtime global.</span><span class="sxs-lookup"><span data-stu-id="d9e38-145">The .NET Framework version 1.1 is the minimum version that can be used to perform an in-place update of a global common language runtime assembly.</span></span> <span data-ttu-id="d9e38-146">Você pode verificar a propriedade [**MsiNetAssemblySupport**](msinetassemblysupport.md) para a versão.</span><span class="sxs-lookup"><span data-stu-id="d9e38-146">You can check the [**MsiNetAssemblySupport**](msinetassemblysupport.md) property for the version.</span></span> <span data-ttu-id="d9e38-147">A tabela MsiAssemblyName também deve ter um campo FileVersion porque esse tipo de atualização de assembly altera apenas o FileVersion.</span><span class="sxs-lookup"><span data-stu-id="d9e38-147">The MsiAssemblyName Table must also have a FileVersion field because this type of assembly update only changes the FileVersion.</span></span> <span data-ttu-id="d9e38-148">Para obter mais informações, consulte [atualizando assemblies](updating-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="d9e38-148">For more information, see [Updating Assemblies](updating-assemblies.md).</span></span>

<span data-ttu-id="d9e38-149">Por exemplo, o manifesto do assembly para componenteA pode ter uma seção assemblyIdentity da seguinte maneira para um assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="d9e38-149">For example, the assembly manifest for ComponentA might have an assemblyIdentity section as follows for a Win32 assembly.</span></span>

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

<span data-ttu-id="d9e38-150">Nesse caso, preencha a tabela MsiAssemblyName da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="d9e38-150">In this case, populate the MsiAssemblyName Table as follows.</span></span>



| <span data-ttu-id="d9e38-151">Componente</span><span class="sxs-lookup"><span data-stu-id="d9e38-151">Component</span></span>  | <span data-ttu-id="d9e38-152">Nome</span><span class="sxs-lookup"><span data-stu-id="d9e38-152">Name</span></span>                  | <span data-ttu-id="d9e38-153">Valor</span><span class="sxs-lookup"><span data-stu-id="d9e38-153">Value</span></span>             |
|------------|-----------------------|-------------------|
| <span data-ttu-id="d9e38-154">Componente</span><span class="sxs-lookup"><span data-stu-id="d9e38-154">ComponentA</span></span> | <span data-ttu-id="d9e38-155">tipo</span><span class="sxs-lookup"><span data-stu-id="d9e38-155">type</span></span>                  | <span data-ttu-id="d9e38-156">Win32</span><span class="sxs-lookup"><span data-stu-id="d9e38-156">win32</span></span>             |
| <span data-ttu-id="d9e38-157">Componente</span><span class="sxs-lookup"><span data-stu-id="d9e38-157">ComponentA</span></span> | <span data-ttu-id="d9e38-158">name</span><span class="sxs-lookup"><span data-stu-id="d9e38-158">name</span></span>                  | <span data-ttu-id="d9e38-159">MS-sxstest-simples</span><span class="sxs-lookup"><span data-stu-id="d9e38-159">ms-sxstest-simple</span></span> |
| <span data-ttu-id="d9e38-160">Componente</span><span class="sxs-lookup"><span data-stu-id="d9e38-160">ComponentA</span></span> | <span data-ttu-id="d9e38-161">version</span><span class="sxs-lookup"><span data-stu-id="d9e38-161">version</span></span>               | <span data-ttu-id="d9e38-162">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="d9e38-162">1.0.0.0</span></span>           |
| <span data-ttu-id="d9e38-163">Componente</span><span class="sxs-lookup"><span data-stu-id="d9e38-163">ComponentA</span></span> | <span data-ttu-id="d9e38-164">Linguagem</span><span class="sxs-lookup"><span data-stu-id="d9e38-164">language</span></span>              | <span data-ttu-id="d9e38-165">en</span><span class="sxs-lookup"><span data-stu-id="d9e38-165">en</span></span>                |
| <span data-ttu-id="d9e38-166">Componente</span><span class="sxs-lookup"><span data-stu-id="d9e38-166">ComponentA</span></span> | <span data-ttu-id="d9e38-167">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="d9e38-167">publicKeyToken</span></span>        | <span data-ttu-id="d9e38-168">1111111111222222</span><span class="sxs-lookup"><span data-stu-id="d9e38-168">1111111111222222</span></span>  |
| <span data-ttu-id="d9e38-169">Componente</span><span class="sxs-lookup"><span data-stu-id="d9e38-169">ComponentA</span></span> | <span data-ttu-id="d9e38-170">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="d9e38-170">processorArchitecture</span></span> | <span data-ttu-id="d9e38-171">x86</span><span class="sxs-lookup"><span data-stu-id="d9e38-171">x86</span></span>               |



 

## <a name="validation"></a><span data-ttu-id="d9e38-172">Validação</span><span class="sxs-lookup"><span data-stu-id="d9e38-172">Validation</span></span>

<dl>

[<span data-ttu-id="d9e38-173">ICE03</span><span class="sxs-lookup"><span data-stu-id="d9e38-173">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d9e38-174">ICE06</span><span class="sxs-lookup"><span data-stu-id="d9e38-174">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d9e38-175">ICE32</span><span class="sxs-lookup"><span data-stu-id="d9e38-175">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d9e38-176">ICE66</span><span class="sxs-lookup"><span data-stu-id="d9e38-176">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="d9e38-177">ICE83</span><span class="sxs-lookup"><span data-stu-id="d9e38-177">ICE83</span></span>](ice83.md)  
</dl>

 

 
