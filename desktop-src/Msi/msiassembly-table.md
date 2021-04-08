---
description: A tabela MsiAssembly especifica Windows Installer configurações para assemblies do Microsoft .NET Framework e assemblies do Win32. Para obter mais informações, consulte instalação de assemblies no cache de assembly global e instalação de assemblies do Win32.
ms.assetid: 3a8cd206-0112-4840-8c9d-773483f5c771
title: Tabela MsiAssembly
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b54bd6e58e2ff6d12c582309c23856a7bb825b2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922816"
---
# <a name="msiassembly-table"></a><span data-ttu-id="f630c-104">Tabela MsiAssembly</span><span class="sxs-lookup"><span data-stu-id="f630c-104">MsiAssembly Table</span></span>

<span data-ttu-id="f630c-105">A tabela MsiAssembly especifica Windows Installer configurações para assemblies do Microsoft .NET Framework e assemblies do Win32.</span><span class="sxs-lookup"><span data-stu-id="f630c-105">The MsiAssembly Table specifies Windows Installer settings for Microsoft .NET Framework assemblies and Win32 assemblies.</span></span> <span data-ttu-id="f630c-106">Para obter mais informações, consulte [instalação de assemblies no cache de assembly global](installation-of-assemblies-to-the-global-assembly-cache.md) e [instalação de assemblies do Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="f630c-106">For more information, see [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="f630c-107">No Windows XP, Windows Installer pode instalar assemblies do Win32 como [assemblies lado a lado](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="f630c-107">On Windows XP, Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="f630c-108">Para obter mais informações, consulte a [API do assembly lado a lado](../sbscs/side-by-side-assembly-api.md).</span><span class="sxs-lookup"><span data-stu-id="f630c-108">For more information, see the [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).</span></span>

<span data-ttu-id="f630c-109">**Windows 2000:** Não há suporte para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="f630c-109">**Windows 2000:** This feature is not supported.</span></span>

<span data-ttu-id="f630c-110">A tabela MsiAssembly tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f630c-110">The MsiAssembly Table has the following columns.</span></span>



| <span data-ttu-id="f630c-111">Coluna</span><span class="sxs-lookup"><span data-stu-id="f630c-111">Column</span></span>            | <span data-ttu-id="f630c-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="f630c-112">Type</span></span>                         | <span data-ttu-id="f630c-113">Chave</span><span class="sxs-lookup"><span data-stu-id="f630c-113">Key</span></span> | <span data-ttu-id="f630c-114">Nullable</span><span class="sxs-lookup"><span data-stu-id="f630c-114">Nullable</span></span> |
|-------------------|------------------------------|-----|----------|
| <span data-ttu-id="f630c-115">Componente\_</span><span class="sxs-lookup"><span data-stu-id="f630c-115">Component\_</span></span>       | [<span data-ttu-id="f630c-116">Identificador</span><span class="sxs-lookup"><span data-stu-id="f630c-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="f630c-117">S</span><span class="sxs-lookup"><span data-stu-id="f630c-117">Y</span></span>   | <span data-ttu-id="f630c-118">N</span><span class="sxs-lookup"><span data-stu-id="f630c-118">N</span></span>        |
| <span data-ttu-id="f630c-119">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="f630c-119">Feature\_</span></span>         | [<span data-ttu-id="f630c-120">Identificador</span><span class="sxs-lookup"><span data-stu-id="f630c-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="f630c-121">N</span><span class="sxs-lookup"><span data-stu-id="f630c-121">N</span></span>   | <span data-ttu-id="f630c-122">N</span><span class="sxs-lookup"><span data-stu-id="f630c-122">N</span></span>        |
| <span data-ttu-id="f630c-123">Manifesto do arquivo \_</span><span class="sxs-lookup"><span data-stu-id="f630c-123">File\_Manifest</span></span>    | [<span data-ttu-id="f630c-124">Identificador</span><span class="sxs-lookup"><span data-stu-id="f630c-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="f630c-125">N</span><span class="sxs-lookup"><span data-stu-id="f630c-125">N</span></span>   | <span data-ttu-id="f630c-126">S</span><span class="sxs-lookup"><span data-stu-id="f630c-126">Y</span></span>        |
| <span data-ttu-id="f630c-127">Aplicativo de arquivo \_</span><span class="sxs-lookup"><span data-stu-id="f630c-127">File\_Application</span></span> | [<span data-ttu-id="f630c-128">Identificador</span><span class="sxs-lookup"><span data-stu-id="f630c-128">Identifier</span></span>](identifier.md) | <span data-ttu-id="f630c-129">N</span><span class="sxs-lookup"><span data-stu-id="f630c-129">N</span></span>   | <span data-ttu-id="f630c-130">S</span><span class="sxs-lookup"><span data-stu-id="f630c-130">Y</span></span>        |
| <span data-ttu-id="f630c-131">Atributos</span><span class="sxs-lookup"><span data-stu-id="f630c-131">Attributes</span></span>        | [<span data-ttu-id="f630c-132">Inteiro</span><span class="sxs-lookup"><span data-stu-id="f630c-132">Integer</span></span>](integer.md)       | <span data-ttu-id="f630c-133">N</span><span class="sxs-lookup"><span data-stu-id="f630c-133">N</span></span>   | <span data-ttu-id="f630c-134">S</span><span class="sxs-lookup"><span data-stu-id="f630c-134">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f630c-135">Colunas</span><span class="sxs-lookup"><span data-stu-id="f630c-135">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f630c-136"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="f630c-136"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="f630c-137">A chave na [tabela de componentes](component-table.md) que especifica o componente de Windows Installer que contém esse assembly.</span><span class="sxs-lookup"><span data-stu-id="f630c-137">The key into the [Component Table](component-table.md) that specifies the Windows Installer component that contains this assembly.</span></span>

<span data-ttu-id="f630c-138">O valor neste campo não deve ser definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="f630c-138">The value in this field must not be set to null.</span></span> <span data-ttu-id="f630c-139">O campo caminho do componente na [tabela de componentes](component-table.md) não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="f630c-139">The component KeyPath field in the [Component Table](component-table.md) must not be null.</span></span>

<span data-ttu-id="f630c-140">Para assemblies do Win32, o caminho KeyPath não pode ser o arquivo de manifesto especificado no \_ manifesto do arquivo.</span><span class="sxs-lookup"><span data-stu-id="f630c-140">For Win32 assemblies, the component KeyPath cannot be the manifest file that is specified in File\_Manifest.</span></span> <span data-ttu-id="f630c-141">O manifesto pode ser o caminho Keypara um .NET Framework ou assembly de política.</span><span class="sxs-lookup"><span data-stu-id="f630c-141">The manifest can be the keypath for a .NET Framework or policy assembly.</span></span>

</dd> <dt>

<span data-ttu-id="f630c-142"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_</span><span class="sxs-lookup"><span data-stu-id="f630c-142"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="f630c-143">A chave na [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="f630c-143">Key into the [Feature Table](feature-table.md).</span></span>

<span data-ttu-id="f630c-144">Quando o assembly deve ser instalado por uma instalação de recurso, Windows Installer instala o recurso apontado por esse campo.</span><span class="sxs-lookup"><span data-stu-id="f630c-144">When the assembly must be installed by a feature installation, Windows Installer installs the feature pointed to by this field.</span></span>

</dd> <dt>

<span data-ttu-id="f630c-145"><span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>Manifesto do arquivo \_</span><span class="sxs-lookup"><span data-stu-id="f630c-145"><span id="File_Manifest"></span><span id="file_manifest"></span><span id="FILE_MANIFEST"></span>File\_Manifest</span></span>
</dt> <dd>

<span data-ttu-id="f630c-146">Uma chave externa na [tabela de arquivos](file-table.md) que especifica o arquivo que contém o manifesto para um assembly .NET Framework ou assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="f630c-146">An external key into the [File Table](file-table.md) that specifies the file that contains the manifest for a .NET Framework assembly or Win32 assembly.</span></span>

<span data-ttu-id="f630c-147">Para um assembly Win32, não especifique esse arquivo como o arquivo de caminho de chave de componente no campo KeyPath da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f630c-147">For a Win32 assembly, do not specify this file as the component key path file in the KeyPath field of the [Component Table](component-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="f630c-148"><span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>Aplicativo de arquivo \_</span><span class="sxs-lookup"><span data-stu-id="f630c-148"><span id="File_Application"></span><span id="file_application"></span><span id="FILE_APPLICATION"></span>File\_Application</span></span>
</dt> <dd>

<span data-ttu-id="f630c-149">Para instalar o assembly em um local privado, insira o arquivo de caminho de chave para o componente de assembly neste campo.</span><span class="sxs-lookup"><span data-stu-id="f630c-149">To install the assembly at a private location, enter the key path file for the assembly component in this field.</span></span>

<span data-ttu-id="f630c-150">Esse é o valor que aparece no campo KeyPath da tabela de [componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f630c-150">This is the value that appears in the KeyPath field of the [Component Table](component-table.md).</span></span> <span data-ttu-id="f630c-151">O instalador pode instalar o assembly na estrutura de diretório do componente especificado na [tabela de diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="f630c-151">The Installer can then install the assembly to the directory structure of the component that is specified in the [Directory Table](directory-table.md).</span></span> <span data-ttu-id="f630c-152">Esse campo deverá ser nulo se o assembly for instalado no cache de assembly global.</span><span class="sxs-lookup"><span data-stu-id="f630c-152">This field must be null if the assembly is to be installed into the global assembly cache.</span></span>

</dd> <dt>

<span data-ttu-id="f630c-153"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="f630c-153"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="f630c-154">Insira um valor de 1 (um) para um assembly Win32.</span><span class="sxs-lookup"><span data-stu-id="f630c-154">Enter a value of 1 (one) for a Win32 assembly.</span></span> <span data-ttu-id="f630c-155">Insira um valor de 0 (zero) para um assembly .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f630c-155">Enter a value of 0 (zero) for a .NET Framework assembly.</span></span>

<span data-ttu-id="f630c-156">Se a coluna Attributes for nula, o instalador tratará o assembly como um assembly .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="f630c-156">If the Attributes column is NULL, the Installer treats the assembly as a .NET Framework assembly.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f630c-157">Comentários</span><span class="sxs-lookup"><span data-stu-id="f630c-157">Remarks</span></span>

<span data-ttu-id="f630c-158">Se houver pelo menos uma entrada na tabela MsiAssembly, a [tabela InstallExecuteSequence](installexecutesequence-table.md) deverá conter a [ação MsiPublishAssemblies](msipublishassemblies-action.md)e a [ação MsiUnpublishAssemblies](msiunpublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="f630c-158">If there is at least one entry in the MsiAssembly Table, the [InstallExecuteSequence Table](installexecutesequence-table.md) must contain the [MsiPublishAssemblies Action](msipublishassemblies-action.md), and [MsiUnpublishAssemblies Action](msiunpublishassemblies-action.md).</span></span>

<span data-ttu-id="f630c-159">Como os assemblies não podem ser revertidos depois de serem confirmados, Windows Installer usa um processo de instalação em duas etapas.</span><span class="sxs-lookup"><span data-stu-id="f630c-159">Because assemblies cannot be rolled back after they are committed, Windows Installer uses a two-step installation process.</span></span> <span data-ttu-id="f630c-160">As interfaces para os assemblies são criadas durante as operações de instalação geradas pela [ação MsiPublishAssemblies](msipublishassemblies-action.md).</span><span class="sxs-lookup"><span data-stu-id="f630c-160">The interfaces to the assemblies are created during the installation operations that are generated by the [MsiPublishAssemblies Action](msipublishassemblies-action.md).</span></span>

<span data-ttu-id="f630c-161">Os assemblies não são confirmados até a execução bem-sucedida da [ação InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="f630c-161">The assemblies are not committed until successful execution of the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="f630c-162">Isso significa que, se você criar uma ação personalizada ou um recurso que dependa do assembly, ele deverá ser sequenciado após a [ação InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="f630c-162">This means that if you author a custom action or resource that relies on the assembly, it must be sequenced after the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="f630c-163">Por exemplo, se você precisar iniciar um serviço que depende de um assembly no GAC (cache de assembly global), será necessário agendar o início desse serviço após a [ação InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="f630c-163">For example, if you need to start a service that depends on an assembly in the Global Assembly Cache (GAC), you must schedule the starting of that service after the [InstallFinalize Action](installfinalize-action.md).</span></span> <span data-ttu-id="f630c-164">Isso significa que você não pode usar a [tabela de UserControl](servicecontrol-table.md) para iniciar o serviço, em vez disso, você deve usar uma ação personalizada que é sequenciada após InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="f630c-164">This means you cannot use the [ServiceControl Table](servicecontrol-table.md) to start the service, instead you must use a custom action that is sequenced after InstallFinalize.</span></span>

## <a name="validation"></a><span data-ttu-id="f630c-165">Validação</span><span class="sxs-lookup"><span data-stu-id="f630c-165">Validation</span></span>

<dl>

[<span data-ttu-id="f630c-166">ICE03</span><span class="sxs-lookup"><span data-stu-id="f630c-166">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f630c-167">ICE06</span><span class="sxs-lookup"><span data-stu-id="f630c-167">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f630c-168">ICE32</span><span class="sxs-lookup"><span data-stu-id="f630c-168">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="f630c-169">ICE66</span><span class="sxs-lookup"><span data-stu-id="f630c-169">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="f630c-170">ICE83</span><span class="sxs-lookup"><span data-stu-id="f630c-170">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="f630c-171">ICE94</span><span class="sxs-lookup"><span data-stu-id="f630c-171">ICE94</span></span>](ice94.md)  
</dl>

 

 
