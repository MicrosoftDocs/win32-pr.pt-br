---
description: Um manifesto de aplicativo é um arquivo XML que descreve e identifica os assemblies lado a lado particulares e compartilhados aos quais um aplicativo deve se associar em tempo de execução.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Manifestos do aplicativo
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: 2fb7297310102134dfcacf0e5f0d907fbf3a3e0b
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230237"
---
# <a name="application-manifests"></a><span data-ttu-id="1faae-103">Manifestos do aplicativo</span><span class="sxs-lookup"><span data-stu-id="1faae-103">Application Manifests</span></span>

<span data-ttu-id="1faae-104">Um manifesto de aplicativo é um arquivo XML que descreve e identifica os assemblies lado a lado particulares e compartilhados aos quais um aplicativo deve se associar em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="1faae-104">An application manifest is an XML file that describes and identifies the shared and private side-by-side assemblies that an application should bind to at run time.</span></span> <span data-ttu-id="1faae-105">Elas devem ser as mesmas versões de assembly que foram usadas para testar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1faae-105">These should be the same assembly versions that were used to test the application.</span></span> <span data-ttu-id="1faae-106">Os manifestos de aplicativo também podem descrever metadados para arquivos que são particulares ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1faae-106">Application manifests may also describe metadata for files that are private to the application.</span></span>

<span data-ttu-id="1faae-107">Para obter uma lista completa do esquema XML, consulte [manifest File Schema](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="1faae-107">For a complete listing of the XML schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="1faae-108">Os manifestos do aplicativo têm os seguintes elementos e atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-108">Application manifests have the following elements and attributes.</span></span>

| <span data-ttu-id="1faae-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="1faae-109">Element</span></span>                               | <span data-ttu-id="1faae-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="1faae-110">Attributes</span></span>                | <span data-ttu-id="1faae-111">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1faae-111">Required</span></span> |
|---------------------------------------|---------------------------|----------|
| <span data-ttu-id="1faae-112">**)**</span><span class="sxs-lookup"><span data-stu-id="1faae-112">**assembly**</span></span>                          |                           | <span data-ttu-id="1faae-113">Sim</span><span class="sxs-lookup"><span data-stu-id="1faae-113">Yes</span></span>      |
|                                       | <span data-ttu-id="1faae-114">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="1faae-114">**manifestVersion**</span></span>       | <span data-ttu-id="1faae-115">Sim</span><span class="sxs-lookup"><span data-stu-id="1faae-115">Yes</span></span>      |
| <span data-ttu-id="1faae-116">**NoInherit**</span><span class="sxs-lookup"><span data-stu-id="1faae-116">**noInherit**</span></span>                         |                           | <span data-ttu-id="1faae-117">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-117">No</span></span>       |
| <span data-ttu-id="1faae-118">**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="1faae-118">**assemblyIdentity**</span></span>                  |                           | <span data-ttu-id="1faae-119">Sim</span><span class="sxs-lookup"><span data-stu-id="1faae-119">Yes</span></span>      |
|                                       | <span data-ttu-id="1faae-120">**tipo**</span><span class="sxs-lookup"><span data-stu-id="1faae-120">**type**</span></span>                  | <span data-ttu-id="1faae-121">Sim</span><span class="sxs-lookup"><span data-stu-id="1faae-121">Yes</span></span>      |
|                                       | <span data-ttu-id="1faae-122">**name**</span><span class="sxs-lookup"><span data-stu-id="1faae-122">**name**</span></span>                  | <span data-ttu-id="1faae-123">Sim</span><span class="sxs-lookup"><span data-stu-id="1faae-123">Yes</span></span>      |
|                                       | <span data-ttu-id="1faae-124">**linguagem**</span><span class="sxs-lookup"><span data-stu-id="1faae-124">**language**</span></span>              | <span data-ttu-id="1faae-125">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-125">No</span></span>       |
|                                       | <span data-ttu-id="1faae-126">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="1faae-126">**processorArchitecture**</span></span> | <span data-ttu-id="1faae-127">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-127">No</span></span>       |
|                                       | <span data-ttu-id="1faae-128">**version**</span><span class="sxs-lookup"><span data-stu-id="1faae-128">**version**</span></span>               | <span data-ttu-id="1faae-129">Sim</span><span class="sxs-lookup"><span data-stu-id="1faae-129">Yes</span></span>      |
|                                       | <span data-ttu-id="1faae-130">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="1faae-130">**publicKeyToken**</span></span>        | <span data-ttu-id="1faae-131">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-131">No</span></span>       |
| <span data-ttu-id="1faae-132">**compatibilidade**</span><span class="sxs-lookup"><span data-stu-id="1faae-132">**compatibility**</span></span>                     |                           | <span data-ttu-id="1faae-133">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-133">No</span></span>       |
| <span data-ttu-id="1faae-134">**aplicativo**</span><span class="sxs-lookup"><span data-stu-id="1faae-134">**application**</span></span>                       |                           | <span data-ttu-id="1faae-135">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-135">No</span></span>       |
| <span data-ttu-id="1faae-136">**supportedOS**</span><span class="sxs-lookup"><span data-stu-id="1faae-136">**supportedOS**</span></span>                       | <span data-ttu-id="1faae-137">**Id**</span><span class="sxs-lookup"><span data-stu-id="1faae-137">**Id**</span></span>                    | <span data-ttu-id="1faae-138">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-138">No</span></span>       |
| <span data-ttu-id="1faae-139">**maxversiontested**</span><span class="sxs-lookup"><span data-stu-id="1faae-139">**maxversiontested**</span></span>                  | <span data-ttu-id="1faae-140">**Id**</span><span class="sxs-lookup"><span data-stu-id="1faae-140">**Id**</span></span>                    | <span data-ttu-id="1faae-141">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-141">No</span></span>       |
| <span data-ttu-id="1faae-142">**Estados**</span><span class="sxs-lookup"><span data-stu-id="1faae-142">**dependency**</span></span>                        |                           | <span data-ttu-id="1faae-143">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-143">No</span></span>       |
| <span data-ttu-id="1faae-144">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="1faae-144">**dependentAssembly**</span></span>                 |                           | <span data-ttu-id="1faae-145">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-145">No</span></span>       |
| <span data-ttu-id="1faae-146">**file**</span><span class="sxs-lookup"><span data-stu-id="1faae-146">**file**</span></span>                              |                           | <span data-ttu-id="1faae-147">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-147">No</span></span>       |
|                                       | <span data-ttu-id="1faae-148">**name**</span><span class="sxs-lookup"><span data-stu-id="1faae-148">**name**</span></span>                  | <span data-ttu-id="1faae-149">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-149">No</span></span>       |
|                                       | <span data-ttu-id="1faae-150">**hashalg**</span><span class="sxs-lookup"><span data-stu-id="1faae-150">**hashalg**</span></span>               | <span data-ttu-id="1faae-151">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-151">No</span></span>       |
|                                       | <span data-ttu-id="1faae-152">**hash**</span><span class="sxs-lookup"><span data-stu-id="1faae-152">**hash**</span></span>                  | <span data-ttu-id="1faae-153">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-153">No</span></span>       |
| <span data-ttu-id="1faae-154">**activeCodePage**</span><span class="sxs-lookup"><span data-stu-id="1faae-154">**activeCodePage**</span></span>                    |                           | <span data-ttu-id="1faae-155">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-155">No</span></span>       |
| <span data-ttu-id="1faae-156">**Elevação de autoelevação**</span><span class="sxs-lookup"><span data-stu-id="1faae-156">**autoElevate**</span></span>                       |                           | <span data-ttu-id="1faae-157">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-157">No</span></span>       |
| <span data-ttu-id="1faae-158">**disableTheming**</span><span class="sxs-lookup"><span data-stu-id="1faae-158">**disableTheming**</span></span>                    |                           | <span data-ttu-id="1faae-159">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-159">No</span></span>       |
| <span data-ttu-id="1faae-160">**disableWindowFiltering**</span><span class="sxs-lookup"><span data-stu-id="1faae-160">**disableWindowFiltering**</span></span>            |                           | <span data-ttu-id="1faae-161">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-161">No</span></span>       |
| <span data-ttu-id="1faae-162">**dpiAware**</span><span class="sxs-lookup"><span data-stu-id="1faae-162">**dpiAware**</span></span>                          |                           | <span data-ttu-id="1faae-163">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-163">No</span></span>       |
| <span data-ttu-id="1faae-164">**dpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="1faae-164">**dpiAwareness**</span></span>                      |                           | <span data-ttu-id="1faae-165">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-165">No</span></span>       |
| <span data-ttu-id="1faae-166">**gdiScaling**</span><span class="sxs-lookup"><span data-stu-id="1faae-166">**gdiScaling**</span></span>                        |                           | <span data-ttu-id="1faae-167">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-167">No</span></span>       |
| <span data-ttu-id="1faae-168">**highResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="1faae-168">**highResolutionScrollingAware**</span></span>      |                           | <span data-ttu-id="1faae-169">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-169">No</span></span>       |
| <span data-ttu-id="1faae-170">**longPathAware**</span><span class="sxs-lookup"><span data-stu-id="1faae-170">**longPathAware**</span></span>                     |                           | <span data-ttu-id="1faae-171">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-171">No</span></span>       |
| <span data-ttu-id="1faae-172">**printerDriverIsolation**</span><span class="sxs-lookup"><span data-stu-id="1faae-172">**printerDriverIsolation**</span></span>            |                           | <span data-ttu-id="1faae-173">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-173">No</span></span>       |
| <span data-ttu-id="1faae-174">**ultraHighResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="1faae-174">**ultraHighResolutionScrollingAware**</span></span> |                           | <span data-ttu-id="1faae-175">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-175">No</span></span>       |
| <span data-ttu-id="1faae-176">**msix**</span><span class="sxs-lookup"><span data-stu-id="1faae-176">**msix**</span></span>                              |                           | <span data-ttu-id="1faae-177">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-177">No</span></span>       |
| <span data-ttu-id="1faae-178">**heaptype**</span><span class="sxs-lookup"><span data-stu-id="1faae-178">**heapType**</span></span>                          |                           | <span data-ttu-id="1faae-179">Não</span><span class="sxs-lookup"><span data-stu-id="1faae-179">No</span></span>       |

## <a name="file-location"></a><span data-ttu-id="1faae-180">Local do arquivo</span><span class="sxs-lookup"><span data-stu-id="1faae-180">File Location</span></span>

<span data-ttu-id="1faae-181">Os manifestos do aplicativo devem ser incluídos como um recurso no arquivo EXE ou DLL do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1faae-181">Application manifests should be included as a resource in the application's EXE file or DLL.</span></span>

<span data-ttu-id="1faae-182">Para obter mais informações, consulte [instalando assemblies lado a lado](installing-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="1faae-182">For more information, see [Installing Side-by-side Assemblies](installing-side-by-side-assemblies.md).</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="1faae-183">Sintaxe de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="1faae-183">File Name Syntax</span></span>

<span data-ttu-id="1faae-184">O nome de um arquivo de manifesto do aplicativo é o nome do executável do aplicativo seguido por. manifest.</span><span class="sxs-lookup"><span data-stu-id="1faae-184">The name of an application manifest file is the name of the application's executable followed by .manifest.</span></span>

<span data-ttu-id="1faae-185">Por exemplo, um manifesto de aplicativo que se refere a example.exe ou example.dll usaria a seguinte sintaxe de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1faae-185">For example, an application manifest that refers to example.exe or example.dll would use the following file name syntax.</span></span> <span data-ttu-id="1faae-186">Você pode omitir o campo <*ID de recurso*> se a ID do recurso for 1.</span><span class="sxs-lookup"><span data-stu-id="1faae-186">You can omit the <*resource ID*> field if resource ID is 1.</span></span>

<span data-ttu-id="1faae-187">**example.exe. <*ID do recurso*>. manifest**</span><span class="sxs-lookup"><span data-stu-id="1faae-187">**example.exe.<*resource ID*>.manifest**</span></span>

<span data-ttu-id="1faae-188">**example.dll. <*ID do recurso*>. manifest**</span><span class="sxs-lookup"><span data-stu-id="1faae-188">**example.dll.<*resource ID*>.manifest**</span></span>

## <a name="elements"></a><span data-ttu-id="1faae-189">Elementos</span><span class="sxs-lookup"><span data-stu-id="1faae-189">Elements</span></span>

<span data-ttu-id="1faae-190">Os nomes de elementos e atributos diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1faae-190">Names of elements and attributes are case-sensitive.</span></span> <span data-ttu-id="1faae-191">Os valores de elementos e atributos não diferenciam maiúsculas de minúsculas, exceto para o valor do atributo de tipo.</span><span class="sxs-lookup"><span data-stu-id="1faae-191">The values of elements and attributes are case-insensitive, except for the value of the type attribute.</span></span>

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a><span data-ttu-id="1faae-192">assembly</span><span class="sxs-lookup"><span data-stu-id="1faae-192">assembly</span></span>

<span data-ttu-id="1faae-193">Um elemento de contêiner.</span><span class="sxs-lookup"><span data-stu-id="1faae-193">A container element.</span></span> <span data-ttu-id="1faae-194">Seu primeiro subelemento deve ser um elemento **NoInherit** ou **AssemblyIdentity** .</span><span class="sxs-lookup"><span data-stu-id="1faae-194">Its first subelement must be a **noInherit** or **assemblyIdentity** element.</span></span> <span data-ttu-id="1faae-195">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1faae-195">Required.</span></span>

<span data-ttu-id="1faae-196">O elemento **assembly** deve estar no namespace "urn: schemas-microsoft-com: asm. v1".</span><span class="sxs-lookup"><span data-stu-id="1faae-196">The **assembly** element must be in the namespace "urn:schemas-microsoft-com:asm.v1".</span></span> <span data-ttu-id="1faae-197">Os elementos filho do assembly também devem estar nesse namespace, por herança ou por marcação.</span><span class="sxs-lookup"><span data-stu-id="1faae-197">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="1faae-198">O elemento **assembly** tem os atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="1faae-198">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="1faae-199">Atributo</span><span class="sxs-lookup"><span data-stu-id="1faae-199">Attribute</span></span>           | <span data-ttu-id="1faae-200">Descrição</span><span class="sxs-lookup"><span data-stu-id="1faae-200">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="1faae-201">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="1faae-201">**manifestVersion**</span></span> | <span data-ttu-id="1faae-202">O **atributo manifestVersion** deve ser definido como 1.0.</span><span class="sxs-lookup"><span data-stu-id="1faae-202">The **manifestVersion** attribute must be set to 1.0.</span></span> |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a><span data-ttu-id="1faae-203">Noinherit</span><span class="sxs-lookup"><span data-stu-id="1faae-203">noInherit</span></span>

<span data-ttu-id="1faae-204">Inclua esse elemento em um manifesto do aplicativo para definir os [contextos de ativação gerados](activation-contexts.md) do manifesto com o sinalizador "no inherit".</span><span class="sxs-lookup"><span data-stu-id="1faae-204">Include this element in an application manifest to set the [activation contexts](activation-contexts.md) generated from the manifest with the "no inherit" flag.</span></span> <span data-ttu-id="1faae-205">Quando esse sinalizador não é definido em um contexto de ativação e o contexto de ativação está ativo, ele é herdado por novos threads no mesmo processo, janelas, procedimentos de janela e Chamadas [de](/windows/desktop/Sync/asynchronous-procedure-calls)Procedimento Assíncrono .</span><span class="sxs-lookup"><span data-stu-id="1faae-205">When this flag is not set in an activation context, and the activation context is active, it is inherited by new threads in the same process, windows, window procedures, and [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span> <span data-ttu-id="1faae-206">Definir esse sinalizador impede que o novo objeto herde o contexto ativo.</span><span class="sxs-lookup"><span data-stu-id="1faae-206">Setting this flag prevents the new object from inheriting the active context.</span></span>

<span data-ttu-id="1faae-207">O **elemento noInherit** é opcional e normalmente omitido.</span><span class="sxs-lookup"><span data-stu-id="1faae-207">The **noInherit** element is optional and typically omitted.</span></span> <span data-ttu-id="1faae-208">A maioria dos assemblies não funciona corretamente usando um contexto de ativação não herdado porque o assembly deve ser projetado explicitamente para gerenciar a propagação de seu próprio contexto de ativação.</span><span class="sxs-lookup"><span data-stu-id="1faae-208">Most assemblies do not work correctly using a no-inherit activation context because the assembly must be explicitly designed to manage the propagation of their own activation context.</span></span> <span data-ttu-id="1faae-209">O uso do **elemento noInherit** requer que todos os assemblies dependentes referenciados pelo manifesto do aplicativo tenham um elemento **noInherit** em seu [manifesto do assembly](assembly-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="1faae-209">The use of the **noInherit** element requires that any dependent assemblies referenced by the application manifest have a **noInherit** element in their [assembly manifest](assembly-manifests.md).</span></span>

<span data-ttu-id="1faae-210">Se **noInherit** for usado em um manifesto, ele deverá ser o primeiro subelemento do elemento **assembly.**</span><span class="sxs-lookup"><span data-stu-id="1faae-210">If **noInherit** is used in a manifest, it must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="1faae-211">O **elemento assemblyIdentity** deve vir imediatamente após **o elemento noInherit.**</span><span class="sxs-lookup"><span data-stu-id="1faae-211">The **assemblyIdentity** element should come immediately after the **noInherit** element.</span></span> <span data-ttu-id="1faae-212">Se **noInherit** não for usado, **assemblyIdentity** deverá ser o primeiro subelemento do elemento **assembly.**</span><span class="sxs-lookup"><span data-stu-id="1faae-212">If **noInherit** is not used, **assemblyIdentity** must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="1faae-213">O **elemento noInherit** não tem elementos filho.</span><span class="sxs-lookup"><span data-stu-id="1faae-213">The **noInherit** element has no child elements.</span></span> <span data-ttu-id="1faae-214">Não é um elemento válido nos [manifestos do assembly.](assembly-manifests.md)</span><span class="sxs-lookup"><span data-stu-id="1faae-214">It is not a valid element in [assembly manifests](assembly-manifests.md).</span></span>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a><span data-ttu-id="1faae-215">assemblyIdentity</span><span class="sxs-lookup"><span data-stu-id="1faae-215">assemblyIdentity</span></span>

<span data-ttu-id="1faae-216">Como o primeiro subelemento de um elemento **de assembly,** **assemblyIdentity** descreve e identifica exclusivamente o aplicativo que possui esse manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1faae-216">As the first subelement of an **assembly** element, **assemblyIdentity** describes and uniquely identifies the application owning this application manifest.</span></span> <span data-ttu-id="1faae-217">Como o primeiro subelemento de um elemento **dependentAssembly,** **assemblyIdentity** descreve um assembly lado a lado exigido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1faae-217">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="1faae-218">Observe que cada assembly referenciado no manifesto do aplicativo requer uma **assemblyIdentity** que corresponde exatamente à **assemblyIdentity** no manifesto de assembly próprio do assembly referenciado.</span><span class="sxs-lookup"><span data-stu-id="1faae-218">Note that every assembly referenced in the application manifest requires an **assemblyIdentity** that exactly matches the **assemblyIdentity** in the referenced assembly's own assembly manifest.</span></span>

<span data-ttu-id="1faae-219">O **elemento assemblyIdentity** tem os seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-219">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="1faae-220">Ele não tem subelementos.</span><span class="sxs-lookup"><span data-stu-id="1faae-220">It has no subelements.</span></span>

| <span data-ttu-id="1faae-221">Atributo</span><span class="sxs-lookup"><span data-stu-id="1faae-221">Attribute</span></span>                 | <span data-ttu-id="1faae-222">Descrição</span><span class="sxs-lookup"><span data-stu-id="1faae-222">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1faae-223">**tipo**</span><span class="sxs-lookup"><span data-stu-id="1faae-223">**type**</span></span>                  | <span data-ttu-id="1faae-224">Especifica o tipo de aplicativo ou assembly.</span><span class="sxs-lookup"><span data-stu-id="1faae-224">Specifies the application or assembly type.</span></span> <span data-ttu-id="1faae-225">O valor deve ser Win32 e todos em menor caso.</span><span class="sxs-lookup"><span data-stu-id="1faae-225">The value must be Win32 and all in lower case.</span></span> <span data-ttu-id="1faae-226">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1faae-226">Required.</span></span>                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="1faae-227">**name**</span><span class="sxs-lookup"><span data-stu-id="1faae-227">**name**</span></span>                  | <span data-ttu-id="1faae-228">Nomeia exclusivamente o aplicativo ou assembly.</span><span class="sxs-lookup"><span data-stu-id="1faae-228">Uniquely names the application or assembly.</span></span> <span data-ttu-id="1faae-229">Use o seguinte formato para o nome: Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="1faae-229">Use the following format for the name: Organization.Division.Name.</span></span> <span data-ttu-id="1faae-230">Por exemplo, Microsoft.Windows.mysampleApp.</span><span class="sxs-lookup"><span data-stu-id="1faae-230">For example Microsoft.Windows.mysampleApp.</span></span> <span data-ttu-id="1faae-231">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1faae-231">Required.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="1faae-232">**linguagem**</span><span class="sxs-lookup"><span data-stu-id="1faae-232">**language**</span></span>              | <span data-ttu-id="1faae-233">Identifica o idioma do aplicativo ou assembly.</span><span class="sxs-lookup"><span data-stu-id="1faae-233">Identifies the language of the application or assembly.</span></span> <span data-ttu-id="1faae-234">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1faae-234">Optional.</span></span> <span data-ttu-id="1faae-235">Se o aplicativo ou assembly for específico do idioma, especifique o código de linguagem DHTML.</span><span class="sxs-lookup"><span data-stu-id="1faae-235">If the application or assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="1faae-236">Na **assemblyIdentidade de um** aplicativo destinado ao uso mundial (idioma neutro) omite o atributo de idioma.</span><span class="sxs-lookup"><span data-stu-id="1faae-236">In the **assemblyIdentity** of an application intended for worldwide use (language neutral) omit the language attribute.</span></span><br/> <span data-ttu-id="1faae-237">Em um **assemblyIdentidade de** um assembly destinado ao uso mundial (neutro na linguagem), de definido o valor da linguagem como " \* ".</span><span class="sxs-lookup"><span data-stu-id="1faae-237">In an **assemblyIdentity** of an assembly intended for worldwide use (language neutral) set the value of language to "\*".</span></span><br/> |
| <span data-ttu-id="1faae-238">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="1faae-238">**processorArchitecture**</span></span> | <span data-ttu-id="1faae-239">Especifica o processador.</span><span class="sxs-lookup"><span data-stu-id="1faae-239">Specifies the processor.</span></span> <span data-ttu-id="1faae-240">Os valores válidos incluem `x86`, `amd64`, `arm` e `arm64`.</span><span class="sxs-lookup"><span data-stu-id="1faae-240">Valid values include `x86`, `amd64`, `arm` and `arm64`.</span></span> <span data-ttu-id="1faae-241">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1faae-241">Optional.</span></span>                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="1faae-242">**version**</span><span class="sxs-lookup"><span data-stu-id="1faae-242">**version**</span></span>               | <span data-ttu-id="1faae-243">Especifica a versão do aplicativo ou assembly.</span><span class="sxs-lookup"><span data-stu-id="1faae-243">Specifies the application or assembly version.</span></span> <span data-ttu-id="1faae-244">Use o formato de versão de quatro partes: mmmmm.nnnnn.ooooo.ppppp.</span><span class="sxs-lookup"><span data-stu-id="1faae-244">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="1faae-245">Cada uma das partes separadas por períodos pode ser de 0 a 65535, inclusive.</span><span class="sxs-lookup"><span data-stu-id="1faae-245">Each of the parts separated by periods can be 0-65535 inclusive.</span></span> <span data-ttu-id="1faae-246">Para obter mais informações, consulte [Versões do assembly](assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="1faae-246">For more information, see [Assembly Versions](assembly-versions.md).</span></span> <span data-ttu-id="1faae-247">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="1faae-247">Required.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="1faae-248">**Publickeytoken**</span><span class="sxs-lookup"><span data-stu-id="1faae-248">**publicKeyToken**</span></span>        | <span data-ttu-id="1faae-249">Uma cadeia de caracteres hexadecimal de 16 caracteres que representa os últimos 8 bytes do hash SHA-1 da chave pública na qual o aplicativo ou assembly está assinado.</span><span class="sxs-lookup"><span data-stu-id="1faae-249">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the application or assembly is signed.</span></span> <span data-ttu-id="1faae-250">A chave pública usada para assinar o catálogo deve ter 2.048 bits ou mais.</span><span class="sxs-lookup"><span data-stu-id="1faae-250">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="1faae-251">Necessário para todos os assemblies compartilhados lado a lado.</span><span class="sxs-lookup"><span data-stu-id="1faae-251">Required for all shared side-by-side assemblies.</span></span>                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a><span data-ttu-id="1faae-252">compatibilidade</span><span class="sxs-lookup"><span data-stu-id="1faae-252">compatibility</span></span>

<span data-ttu-id="1faae-253">Contém pelo menos um **aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="1faae-253">Contains at least one **application**.</span></span> <span data-ttu-id="1faae-254">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-254">It has no attributes.</span></span> <span data-ttu-id="1faae-255">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1faae-255">Optional.</span></span> <span data-ttu-id="1faae-256">Manifestos de aplicativo sem um elemento de compatibilidade padrão para a compatibilidade do Windows Vista no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1faae-256">Application manifests without a compatibility element default to Windows Vista compatibility on Windows 7.</span></span>

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a><span data-ttu-id="1faae-257">aplicativo</span><span class="sxs-lookup"><span data-stu-id="1faae-257">application</span></span>

<span data-ttu-id="1faae-258">Contém pelo menos um **elemento DOOS** com suporte.</span><span class="sxs-lookup"><span data-stu-id="1faae-258">Contains at least one **supportedOS** element.</span></span> <span data-ttu-id="1faae-259">A partir Windows 10, versão 1903, ele também pode conter um **elemento maxversiontested** opcional.</span><span class="sxs-lookup"><span data-stu-id="1faae-259">Starting in Windows 10, version 1903, it can also contain one optional **maxversiontested** element.</span></span> <span data-ttu-id="1faae-260">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-260">It has no attributes.</span></span> <span data-ttu-id="1faae-261">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1faae-261">Optional.</span></span>

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a><span data-ttu-id="1faae-262">supportedOS</span><span class="sxs-lookup"><span data-stu-id="1faae-262">supportedOS</span></span>

<span data-ttu-id="1faae-263">O **elemento supportedOS** tem o atributo a seguir.</span><span class="sxs-lookup"><span data-stu-id="1faae-263">The **supportedOS** element has the following attribute.</span></span> <span data-ttu-id="1faae-264">Ele não tem subelementos.</span><span class="sxs-lookup"><span data-stu-id="1faae-264">It has no subelements.</span></span>

| <span data-ttu-id="1faae-265">Atributo</span><span class="sxs-lookup"><span data-stu-id="1faae-265">Attribute</span></span> | <span data-ttu-id="1faae-266">Descrição</span><span class="sxs-lookup"><span data-stu-id="1faae-266">Description</span></span>   |
|-----------|-----------------------|
| <span data-ttu-id="1faae-267">**Id**</span><span class="sxs-lookup"><span data-stu-id="1faae-267">**Id**</span></span>    | <span data-ttu-id="1faae-268">De definir o atributo Id como **{e2011457-1546-43c5-a5fe-008deee3d3f0}** para executar o aplicativo usando a funcionalidade vista.</span><span class="sxs-lookup"><span data-stu-id="1faae-268">Set the Id attribute to **{e2011457-1546-43c5-a5fe-008deee3d3f0}** to run the application using Vista functionality.</span></span> <span data-ttu-id="1faae-269">Isso pode permitir que um aplicativo projetado para o Windows Vista seja executado em um sistema operacional posterior.</span><span class="sxs-lookup"><span data-stu-id="1faae-269">This can enable an application designed for Windows Vista to run on a later operating system.</span></span> <br/> <span data-ttu-id="1faae-270">De definir o atributo Id como **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** para executar o aplicativo usando a funcionalidade do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1faae-270">Set the Id attribute to **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** to run the application using Windows 7 functionality.</span></span><br/> <span data-ttu-id="1faae-271">Os aplicativos que suportam o Windows Vista, o Windows 7 e Windows 8 funcionalidade não exigem manifestos separados.</span><span class="sxs-lookup"><span data-stu-id="1faae-271">Applications that support Windows Vista, Windows 7, and Windows 8 functionality do not require separate manifests.</span></span> <span data-ttu-id="1faae-272">Nesse caso, adicione os GUIDs para todos os sistemas operacionais Windows.</span><span class="sxs-lookup"><span data-stu-id="1faae-272">In this case, add the GUIDs for all the Windows operating systems.</span></span><br/> <span data-ttu-id="1faae-273">Para obter informações sobre o comportamento do atributo **de ID** no Windows, consulte o guia Windows 8 e o Guia de Compatibilidade do [Windows Server 2012.](https://www.microsoft.com/download/details.aspx?id=27416)</span><span class="sxs-lookup"><span data-stu-id="1faae-273">For info about the **Id** attribute behavior in Windows, see the [Windows 8 and Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span></span><br/> <span data-ttu-id="1faae-274">Os seguintes GUIDs correspondem aos sistemas operacionais indicados:</span><span class="sxs-lookup"><span data-stu-id="1faae-274">The following GUIDs correspond with the indicated operating systems:</span></span><br/> <span data-ttu-id="1faae-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 e Windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="1faae-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 and Windows Server 2019</span></span><br/> <span data-ttu-id="1faae-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 e Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1faae-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 and Windows Server 2012 R2</span></span><br/> <span data-ttu-id="1faae-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 e Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1faae-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 and Windows Server 2012</span></span><br/> <span data-ttu-id="1faae-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 e Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1faae-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 and Windows Server 2008 R2</span></span><br/> <span data-ttu-id="1faae-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista e Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1faae-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista and Windows Server 2008</span></span><br/> <span data-ttu-id="1faae-280">Você pode testar isso no Windows 7 ou Windows 8.x executando Monitor de Recursos (resmon), indo para a guia CPU, clicando com o botão direito do mouse nos rótulos de coluna, "Selecionar Coluna..." e marque "Contexto do Sistema Operacional".</span><span class="sxs-lookup"><span data-stu-id="1faae-280">You can test this on Windows 7 or Windows 8.x by running Resource Monitor (resmon), going to the CPU tab, right-clicking on the column labels, "Select Column...", and check "Operating System Context".</span></span> <span data-ttu-id="1faae-281">No Windows 8.x, você também pode encontrar essa coluna disponível no Gerenciador de Tarefas (taskmgr).</span><span class="sxs-lookup"><span data-stu-id="1faae-281">On Windows 8.x, you can also find this column available in the Task Manager (taskmgr).</span></span> <span data-ttu-id="1faae-282">O conteúdo da coluna mostra o valor mais alto encontrado ou "Windows Vista" como o padrão.</span><span class="sxs-lookup"><span data-stu-id="1faae-282">The content of the column shows the highest value found or "Windows Vista" as the default.</span></span> <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a><span data-ttu-id="1faae-283">maxversiontested</span><span class="sxs-lookup"><span data-stu-id="1faae-283">maxversiontested</span></span>

<span data-ttu-id="1faae-284">O **elemento maxversiontested** especifica as versões do Windows em que o aplicativo foi testado a partir da versão mínima do sistema operacional que o aplicativo dá suporte até a versão máxima.</span><span class="sxs-lookup"><span data-stu-id="1faae-284">The **maxversiontested** element specifies the versions of Windows that the application was tested against starting with the minimum OS version the application supports up to the maximum version.</span></span> <span data-ttu-id="1faae-285">O conjunto completo de versões pode ser encontrado [aqui.](https://developer.microsoft.com/windows/downloads/sdk-archive/)</span><span class="sxs-lookup"><span data-stu-id="1faae-285">The complete set of versions can be found [here](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span> <span data-ttu-id="1faae-286">Isso destina-se a ser usado por aplicativos da área de trabalho que usam Ilhas [XAML](/windows/apps/desktop/modernize/xaml-islands) e que não são implantados em um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="1faae-286">This is intended to be used by desktop applications that use [XAML Islands](/windows/apps/desktop/modernize/xaml-islands) and that are not deployed in an MSIX package.</span></span> <span data-ttu-id="1faae-287">Esse elemento tem suporte no Windows 10, versão 1903 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="1faae-287">This element is supported in Windows 10, version 1903, and later versions.</span></span>

<span data-ttu-id="1faae-288">O **elemento maxversiontested** tem o atributo a seguir.</span><span class="sxs-lookup"><span data-stu-id="1faae-288">The **maxversiontested** element has the following attribute.</span></span> <span data-ttu-id="1faae-289">Ele não tem subelementos.</span><span class="sxs-lookup"><span data-stu-id="1faae-289">It has no subelements.</span></span>

| <span data-ttu-id="1faae-290">Atributo</span><span class="sxs-lookup"><span data-stu-id="1faae-290">Attribute</span></span> | <span data-ttu-id="1faae-291">Descrição</span><span class="sxs-lookup"><span data-stu-id="1faae-291">Description</span></span>    |
|-----------|----------------|
| <span data-ttu-id="1faae-292">**Id**</span><span class="sxs-lookup"><span data-stu-id="1faae-292">**Id**</span></span>    | <span data-ttu-id="1faae-293">De definir o atributo Id como uma cadeia de caracteres de versão de 4 partes que especifica a versão máxima do Windows em que o aplicativo foi testado.</span><span class="sxs-lookup"><span data-stu-id="1faae-293">Set the Id attribute to a 4-part version string that specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="1faae-294">Por exemplo, "10.0.18226.0".</span><span class="sxs-lookup"><span data-stu-id="1faae-294">For example, "10.0.18226.0".</span></span> |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a><span data-ttu-id="1faae-295">dependência</span><span class="sxs-lookup"><span data-stu-id="1faae-295">dependency</span></span>

<span data-ttu-id="1faae-296">Contém pelo menos um **dependentAssembly.**</span><span class="sxs-lookup"><span data-stu-id="1faae-296">Contains at least one **dependentAssembly**.</span></span> <span data-ttu-id="1faae-297">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-297">It has no attributes.</span></span> <span data-ttu-id="1faae-298">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1faae-298">Optional.</span></span>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a><span data-ttu-id="1faae-299">dependentAssembly</span><span class="sxs-lookup"><span data-stu-id="1faae-299">dependentAssembly</span></span>

<span data-ttu-id="1faae-300">O primeiro subelemento de **dependentAssembly** deve ser um **elemento assemblyIdentity** que descreve um assembly lado a lado exigido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1faae-300">The first subelement of **dependentAssembly** must be an **assemblyIdentity** element that describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="1faae-301">Cada **dependentAssembly** deve estar dentro de exatamente uma **dependência**.</span><span class="sxs-lookup"><span data-stu-id="1faae-301">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="1faae-302">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-302">It has no attributes.</span></span>

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a><span data-ttu-id="1faae-303">file</span><span class="sxs-lookup"><span data-stu-id="1faae-303">file</span></span>

<span data-ttu-id="1faae-304">Especifica arquivos que são privados para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1faae-304">Specifies files that are private to the application.</span></span> <span data-ttu-id="1faae-305">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1faae-305">Optional.</span></span>

<span data-ttu-id="1faae-306">O **elemento** file tem os atributos mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1faae-306">The **file** element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="1faae-307">Atributo</span><span class="sxs-lookup"><span data-stu-id="1faae-307">Attribute</span></span>   | <span data-ttu-id="1faae-308">Descrição</span><span class="sxs-lookup"><span data-stu-id="1faae-308">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1faae-309">**name**</span><span class="sxs-lookup"><span data-stu-id="1faae-309">**name**</span></span>    | <span data-ttu-id="1faae-310">Nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="1faae-310">Name of the file.</span></span> <span data-ttu-id="1faae-311">Por exemplo, Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="1faae-311">For example, Comctl32.dll.</span></span>                                                            |
| <span data-ttu-id="1faae-312">**Hashalg**</span><span class="sxs-lookup"><span data-stu-id="1faae-312">**hashalg**</span></span> | <span data-ttu-id="1faae-313">Algoritmo usado para criar um hash do arquivo.</span><span class="sxs-lookup"><span data-stu-id="1faae-313">Algorithm used to create a hash of the file.</span></span> <span data-ttu-id="1faae-314">Esse valor deve ser SHA1.</span><span class="sxs-lookup"><span data-stu-id="1faae-314">This value should be SHA1.</span></span>                                 |
| <span data-ttu-id="1faae-315">**hash**</span><span class="sxs-lookup"><span data-stu-id="1faae-315">**hash**</span></span>    | <span data-ttu-id="1faae-316">Um hash do arquivo referenciado pelo nome.</span><span class="sxs-lookup"><span data-stu-id="1faae-316">A hash of the file referred to by name.</span></span> <span data-ttu-id="1faae-317">Uma cadeia de caracteres hexadecimal de comprimento, dependendo do algoritmo de hash.</span><span class="sxs-lookup"><span data-stu-id="1faae-317">A hexadecimal string of length depending on the hash algorithm.</span></span> |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a><span data-ttu-id="1faae-318">activeCodePage</span><span class="sxs-lookup"><span data-stu-id="1faae-318">activeCodePage</span></span>

<span data-ttu-id="1faae-319">Force um processo a usar UTF-8 como a página de código do processo.</span><span class="sxs-lookup"><span data-stu-id="1faae-319">Force a process to use UTF-8 as the process code page.</span></span>

<span data-ttu-id="1faae-320">**activeCodePage** foi adicionado na versão 1903 do Windows (atualização de maio de 2019).</span><span class="sxs-lookup"><span data-stu-id="1faae-320">**activeCodePage** was added in Windows Version 1903 (May 2019 Update).</span></span> <span data-ttu-id="1faae-321">Você pode declarar essa propriedade e o destino/executar em builds anteriores do Windows, mas deve lidar com a detecção e a conversão de página de código herddas como de costume.</span><span class="sxs-lookup"><span data-stu-id="1faae-321">You can declare this property and target/run on earlier Windows builds, but you must handle legacy code page detection and conversion as usual.</span></span> <span data-ttu-id="1faae-322">Consulte [Usar a página de código UTF-8](/windows/uwp/design/globalizing/use-utf8-code-page) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="1faae-322">See [Use the UTF-8 code page](/windows/uwp/design/globalizing/use-utf8-code-page) for details.</span></span>

<span data-ttu-id="1faae-323">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-323">This element has no attributes.</span></span> <span data-ttu-id="1faae-324">**UTF-8 é** apenas um valor válido para **o elemento activeCodePage.**</span><span class="sxs-lookup"><span data-stu-id="1faae-324">**UTF-8** is only valid value for **activeCodePage** element.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2019/WindowsSettings"> 
      <activeCodePage>UTF-8</activeCodePage> 
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="autoElevate"></span><span id="autoelevate"></span><span id="AUTOELEVATE"></span>

### <a name="autoelevate"></a><span data-ttu-id="1faae-325">autoElevate</span><span class="sxs-lookup"><span data-stu-id="1faae-325">autoElevate</span></span>

<span data-ttu-id="1faae-326">Especifica se a elevação automática está habilitada.</span><span class="sxs-lookup"><span data-stu-id="1faae-326">Specifies whether auto elevate is enabled.</span></span> <span data-ttu-id="1faae-327">**TRUE** indica que ele está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1faae-327">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="1faae-328">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-328">It has no attributes.</span></span>

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a><span data-ttu-id="1faae-329">disableTheming</span><span class="sxs-lookup"><span data-stu-id="1faae-329">disableTheming</span></span>

<span data-ttu-id="1faae-330">Especifica se a entrega de elementos da interface do usuário a um tema está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="1faae-330">Specifies whether giving UI elements a theme is disabled.</span></span> <span data-ttu-id="1faae-331">**TRUE** indica desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1faae-331">**TRUE** indicates disabled.</span></span> <span data-ttu-id="1faae-332">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-332">It has no attributes.</span></span>

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a><span data-ttu-id="1faae-333">disableWindowFiltering</span><span class="sxs-lookup"><span data-stu-id="1faae-333">disableWindowFiltering</span></span>

<span data-ttu-id="1faae-334">Especifica se a filtragem de janelas deve ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="1faae-334">Specifies whether to disable window filtering.</span></span> <span data-ttu-id="1faae-335">**TRUE** desabilita a filtragem de janelas para que você possa enumerar janelas imersivas da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="1faae-335">**TRUE** disables window filtering so you can enumerate immersive windows from the desktop.</span></span> <span data-ttu-id="1faae-336">**disableWindowFiltering** foi adicionado Windows 8 e não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-336">**disableWindowFiltering** was added in Windows 8 and has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <disableWindowFiltering>true</disableWindowFiltering>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAware"></span><span id="dpiaware"></span><span id="DPIAWARE"></span>

### <a name="dpiaware"></a><span data-ttu-id="1faae-337">dpiAware</span><span class="sxs-lookup"><span data-stu-id="1faae-337">dpiAware</span></span>

<span data-ttu-id="1faae-338">Especifica se o processo atual está ciente de pontos por polegada (dpi).</span><span class="sxs-lookup"><span data-stu-id="1faae-338">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="1faae-339">**Windows 10, versão 1607:** O **elemento dpiAware** será ignorado se **o elemento dpiAwareness** estiver presente.</span><span class="sxs-lookup"><span data-stu-id="1faae-339">**Windows 10, version 1607:** The **dpiAware** element is ignored if the **dpiAwareness** element is present.</span></span> <span data-ttu-id="1faae-340">Você pode incluir ambos os elementos em um manifesto se quiser especificar um comportamento diferente para Windows 10, versão 1607 do que para uma versão anterior do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1faae-340">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="1faae-341">A tabela a seguir descreve o comportamento que resulta com base na presença do **elemento dpiAware** e no texto que ele contém.</span><span class="sxs-lookup"><span data-stu-id="1faae-341">The following table describes the behavior that results based upon the presence of the **dpiAware** element and the text that it contains.</span></span> <span data-ttu-id="1faae-342">O texto dentro do elemento não é sensível a minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1faae-342">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="1faae-343">Estado do **elemento dpiAware**</span><span class="sxs-lookup"><span data-stu-id="1faae-343">State of the **dpiAware** element</span></span> | <span data-ttu-id="1faae-344">Descrição</span><span class="sxs-lookup"><span data-stu-id="1faae-344">Description</span></span>     |
|-----------------------------------|---------|
| <span data-ttu-id="1faae-345">Absent</span><span class="sxs-lookup"><span data-stu-id="1faae-345">Absent</span></span>                            | <span data-ttu-id="1faae-346">O processo atual não tem conhecimento de dpi por padrão.</span><span class="sxs-lookup"><span data-stu-id="1faae-346">The current process is dpi unaware by default.</span></span> <span data-ttu-id="1faae-347">Você pode alterar essa configuração programaticamente chamando a [**função SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**ou SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="1faae-347">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>                                                                                                                                                            |
| <span data-ttu-id="1faae-348">Contém "true"</span><span class="sxs-lookup"><span data-stu-id="1faae-348">Contains "true"</span></span>                   | <span data-ttu-id="1faae-349">O processo atual reconhece o dpi do sistema.</span><span class="sxs-lookup"><span data-stu-id="1faae-349">The current process is system dpi aware.</span></span>                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="1faae-350">Contém "false"</span><span class="sxs-lookup"><span data-stu-id="1faae-350">Contains "false"</span></span>                  | <span data-ttu-id="1faae-351">**Windows Vista, Windows 7 e Windows 8:** O comportamento é o mesmo de quando **o dpiAware** está ausente.</span><span class="sxs-lookup"><span data-stu-id="1faae-351">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="1faae-352">**Windows 8.1 e Windows 10:** O processo atual não tem conhecimento de dpi e você não pode alterar essa configuração programaticamente chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="1faae-352">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |
| <span data-ttu-id="1faae-353">Contém "true/pm"</span><span class="sxs-lookup"><span data-stu-id="1faae-353">Contains "true/pm"</span></span>                | <span data-ttu-id="1faae-354">**Windows Vista, Windows 7 e Windows 8:** O processo atual reconhece o dpi do sistema.</span><span class="sxs-lookup"><span data-stu-id="1faae-354">**Windows Vista, Windows 7 and Windows 8:** The current process is system dpi aware.</span></span><br/> <span data-ttu-id="1faae-355">**Windows 8.1 e Windows 10:** O processo atual reconhece dpi por monitor.</span><span class="sxs-lookup"><span data-stu-id="1faae-355">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="1faae-356">Contém "por monitor"</span><span class="sxs-lookup"><span data-stu-id="1faae-356">Contains "per monitor"</span></span>            | <span data-ttu-id="1faae-357">**Windows Vista, Windows 7 e Windows 8:** O comportamento é o mesmo de quando **o dpiAware** está ausente.</span><span class="sxs-lookup"><span data-stu-id="1faae-357">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="1faae-358">**Windows 8.1 e Windows 10:** O processo atual reconhece dpi por monitor.</span><span class="sxs-lookup"><span data-stu-id="1faae-358">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="1faae-359">Contém qualquer outra cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="1faae-359">Contains any other string</span></span>         | <span data-ttu-id="1faae-360">**Windows Vista, Windows 7 e Windows 8:** O comportamento é o mesmo de quando **o dpiAware** está ausente.</span><span class="sxs-lookup"><span data-stu-id="1faae-360">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="1faae-361">**Windows 8.1 e Windows 10:** O processo atual não tem conhecimento de dpi e você não pode alterar essa configuração programaticamente chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="1faae-361">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |

<span data-ttu-id="1faae-362">Para obter mais informações sobre as configurações de reconhecimento de dpi, consulte [Comparação de níveis de reconhecimento de DPI](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="1faae-362">For more information about dpi awareness settings, see [Comparison of DPI Awareness Levels](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

<span data-ttu-id="1faae-363">**dpiAware** não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-363">**dpiAware** has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAwareness"></span><span id="dpiawareness"></span><span id="DPIAWARENESS"></span>

### <a name="dpiawareness"></a><span data-ttu-id="1faae-364">dpiAwareness</span><span class="sxs-lookup"><span data-stu-id="1faae-364">dpiAwareness</span></span>

<span data-ttu-id="1faae-365">Especifica se o processo atual está ciente de pontos por polegada (dpi).</span><span class="sxs-lookup"><span data-stu-id="1faae-365">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="1faae-366">A versão mínima do sistema operacional que dá suporte ao **elemento dpiAwareness** é Windows 10 versão 1607.</span><span class="sxs-lookup"><span data-stu-id="1faae-366">The minimum version of the operating system that supports the **dpiAwareness** element is Windows 10, version 1607.</span></span> <span data-ttu-id="1faae-367">Para versões que suportam **o elemento dpiAwareness,** **o dpiAwareness** substitui o **elemento dpiAware.**</span><span class="sxs-lookup"><span data-stu-id="1faae-367">For versions that support the **dpiAwareness** element, the **dpiAwareness** overrides the **dpiAware** element.</span></span> <span data-ttu-id="1faae-368">Você pode incluir ambos os elementos em um manifesto se quiser especificar um comportamento diferente para Windows 10, versão 1607 do que para uma versão anterior do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1faae-368">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="1faae-369">O **elemento dpiAwareness** pode conter um único item ou uma lista de itens separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="1faae-369">The **dpiAwareness** element can contain a single item or a list of comma-separated items.</span></span> <span data-ttu-id="1faae-370">No último caso, o primeiro item (mais à esquerda) na lista reconhecido pelo sistema operacional é usado.</span><span class="sxs-lookup"><span data-stu-id="1faae-370">In the latter case, the first (leftmost) item in the list recognized by the operating system is used.</span></span> <span data-ttu-id="1faae-371">Dessa forma, você pode especificar diferentes comportamentos com suporte em versões futuras do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="1faae-371">In this way, you can specify different behaviors supported in future Windows operating system versions.</span></span>

<span data-ttu-id="1faae-372">A tabela a seguir descreve o comportamento que resulta com base na presença do elemento **dpiAwareness** e no texto que ele contém em seu item reconhecido mais à esquerda.</span><span class="sxs-lookup"><span data-stu-id="1faae-372">The following table describes the behavior that results based upon the presence of the **dpiAwareness** element and the text that it contains in its leftmost recognized item.</span></span> <span data-ttu-id="1faae-373">O texto dentro do elemento não é sensível a minúsculas.</span><span class="sxs-lookup"><span data-stu-id="1faae-373">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="1faae-374">**Status do elemento dpiAwareness:**</span><span class="sxs-lookup"><span data-stu-id="1faae-374">**dpiAwareness** element status:</span></span>        | <span data-ttu-id="1faae-375">Descrição</span><span class="sxs-lookup"><span data-stu-id="1faae-375">Description</span></span>                          |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="1faae-376">O elemento está ausente</span><span class="sxs-lookup"><span data-stu-id="1faae-376">Element is absent</span></span>                       | <span data-ttu-id="1faae-377">O **elemento dpiAware** especifica se o processo está ciente de dpi.</span><span class="sxs-lookup"><span data-stu-id="1faae-377">The **dpiAware** element specifies whether the process is dpi aware.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="1faae-378">Não contém nenhum item reconhecido</span><span class="sxs-lookup"><span data-stu-id="1faae-378">Contains no recognized items</span></span>            | <span data-ttu-id="1faae-379">O processo atual não tem conhecimento de dpi por padrão.</span><span class="sxs-lookup"><span data-stu-id="1faae-379">The current process is dpi unaware by default.</span></span> <span data-ttu-id="1faae-380">Você pode alterar essa configuração programaticamente chamando a [**função SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) [**ou SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="1faae-380">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span> |
| <span data-ttu-id="1faae-381">O primeiro item reconhecido é "system"</span><span class="sxs-lookup"><span data-stu-id="1faae-381">First recognized item is "system"</span></span>       | <span data-ttu-id="1faae-382">O processo atual reconhece o dpi do sistema.</span><span class="sxs-lookup"><span data-stu-id="1faae-382">The current process is system dpi aware.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="1faae-383">O primeiro item reconhecido é "permonitor"</span><span class="sxs-lookup"><span data-stu-id="1faae-383">First recognized item is "permonitor"</span></span>   | <span data-ttu-id="1faae-384">O processo atual reconhece dpi por monitor.</span><span class="sxs-lookup"><span data-stu-id="1faae-384">The current process is per-monitor dpi aware.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="1faae-385">O primeiro item reconhecido é "permonitorv2"</span><span class="sxs-lookup"><span data-stu-id="1faae-385">First recognized item is "permonitorv2"</span></span> | <span data-ttu-id="1faae-386">O processo atual usa o contexto de reconhecimento de dpi por monitor-v2.</span><span class="sxs-lookup"><span data-stu-id="1faae-386">The current process uses the per-monitor-v2 dpi awareness context.</span></span> <span data-ttu-id="1faae-387">Esse item só será reconhecido no Windows 10 versão 1703 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="1faae-387">This item will only be recognized on Windows 10 version 1703 or later.</span></span>                                                                                              |
| <span data-ttu-id="1faae-388">O primeiro item reconhecido é "não ciente"</span><span class="sxs-lookup"><span data-stu-id="1faae-388">First recognized item is "unaware"</span></span>      | <span data-ttu-id="1faae-389">O processo atual não tem conhecimento de dpi.</span><span class="sxs-lookup"><span data-stu-id="1faae-389">The current process is dpi unaware.</span></span> <span data-ttu-id="1faae-390">Você **não pode** alterar essa configuração programaticamente chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware.**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware)</span><span class="sxs-lookup"><span data-stu-id="1faae-390">You **cannot** programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>      |

<span data-ttu-id="1faae-391">Para obter mais informações sobre as configurações de reconhecimento de dpi com suporte por esse elemento, consulte [RECONHECIMENTO de DPI \_ ](/windows/desktop/api/windef/ne-windef-dpi_awareness) e CONTEXTO DE RECONHECIMENTO [de DPI \_ \_ ](/windows/desktop/hidpi/dpi-awareness-context).</span><span class="sxs-lookup"><span data-stu-id="1faae-391">For more information about dpi awareness settings supported by this element, see [DPI\_AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) and [DPI\_AWARENESS\_CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).</span></span>

<span data-ttu-id="1faae-392">**dpiAwareness** não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-392">**dpiAwareness** has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <dpiAwareness>PerMonitorV2, unaware</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="gdiScaling"></span><span id="gdiscaling"></span><span id="GDISCALING"></span>

### <a name="gdiscaling"></a><span data-ttu-id="1faae-393">gdiScaling</span><span class="sxs-lookup"><span data-stu-id="1faae-393">gdiScaling</span></span>

<span data-ttu-id="1faae-394">Especifica se o dimensionamento GDI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1faae-394">Specifies whether GDI scaling is enabled.</span></span> <span data-ttu-id="1faae-395">A versão mínima do sistema operacional que dá suporte ao **elemento gdiScaling** é Windows 10 versão 1703.</span><span class="sxs-lookup"><span data-stu-id="1faae-395">The minimum version of the operating system that supports the **gdiScaling** element is Windows 10 version 1703.</span></span>

<span data-ttu-id="1faae-396">A estrutura GDI (interface do dispositivo gráfico) pode aplicar o dimensionamento de DPI a primitivos e texto por monitor sem atualizações para o próprio aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1faae-396">The GDI (graphics device interface) framework can apply DPI scaling to primitives and text on a per-monitor basis without updates to the application itself.</span></span> <span data-ttu-id="1faae-397">Isso pode ser útil para que os aplicativos GDI não sejam mais atualizados ativamente.</span><span class="sxs-lookup"><span data-stu-id="1faae-397">This can be useful for GDI applications no longer being actively updated.</span></span>

<span data-ttu-id="1faae-398">Gráficos não vetoriais (como bitmaps, ícones ou barras de ferramentas) não podem ser dimensionados por esse elemento.</span><span class="sxs-lookup"><span data-stu-id="1faae-398">Non-vector graphics (such as bitmaps, icons, or toolbars) cannot be scaled by this element.</span></span> <span data-ttu-id="1faae-399">Além disso, elementos gráficos e textos que aparecem em bitmaps construídos dinamicamente por aplicativos também não podem ser dimensionados por esse elemento.</span><span class="sxs-lookup"><span data-stu-id="1faae-399">In addition, graphics and text appearing within bitmaps dynamically constructed by applications also cannot be scaled by this element.</span></span>

<span data-ttu-id="1faae-400">**TRUE** indica que esse elemento está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1faae-400">**TRUE** indicates that this element is enabled.</span></span> <span data-ttu-id="1faae-401">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-401">It has no attributes.</span></span>


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">
      <gdiScaling>true</gdiScaling>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="highResolutionScrollingAware"></span><span id="highresolutionscrollingaware"></span><span id="HIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="highresolutionscrollingaware"></a><span data-ttu-id="1faae-402">highResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="1faae-402">highResolutionScrollingAware</span></span>

<span data-ttu-id="1faae-403">Especifica se o com conhecimento de rolagem de alta resolução está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1faae-403">Specifies whether high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="1faae-404">**TRUE** indica que ele está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1faae-404">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="1faae-405">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-405">It has no attributes.</span></span>

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a><span data-ttu-id="1faae-406">longPathAware</span><span class="sxs-lookup"><span data-stu-id="1faae-406">longPathAware</span></span>

<span data-ttu-id="1faae-407">Habilita caminhos longos que **excedem MAX_PATH** comprimento.</span><span class="sxs-lookup"><span data-stu-id="1faae-407">Enables long paths that exceed **MAX_PATH** in length.</span></span> <span data-ttu-id="1faae-408">Esse elemento tem suporte no Windows 10, versão 1607 e posterior.</span><span class="sxs-lookup"><span data-stu-id="1faae-408">This element is supported in Windows 10, version 1607, and later.</span></span> <span data-ttu-id="1faae-409">Para obter mais informações, consulte [este artigo](../fileio/maximum-file-path-limitation.md).</span><span class="sxs-lookup"><span data-stu-id="1faae-409">For more information, see [this article](../fileio/maximum-file-path-limitation.md).</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <ws2:longPathAware>true</ws2:longPathAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="printerDriverIsolation"></span><span id="printerdriverisolation"></span><span id="PRINTERDRIVERISOLATION"></span>

### <a name="printerdriverisolation"></a><span data-ttu-id="1faae-410">printerDriverIsolation</span><span class="sxs-lookup"><span data-stu-id="1faae-410">printerDriverIsolation</span></span>

<span data-ttu-id="1faae-411">Especifica se o isolamento do driver de impressora está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1faae-411">Specifies whether printer driver isolation is enabled.</span></span> <span data-ttu-id="1faae-412">**TRUE** indica que ele está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1faae-412">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="1faae-413">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-413">It has no attributes.</span></span> <span data-ttu-id="1faae-414">O isolamento do driver de impressora melhora a confiabilidade do serviço de impressão do Windows, permitindo que os drivers de impressora sejam executados em processos separados do processo no qual o spooler de impressão é executado.</span><span class="sxs-lookup"><span data-stu-id="1faae-414">Printer driver isolation improves the reliability of the Windows print service by enabling printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="1faae-415">Suporte para isolamento de driver de impressora iniciado no Windows 7 e Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="1faae-415">Support for printer driver isolation started in Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="1faae-416">Um aplicativo pode declarar o isolamento do driver de impressora em seu manifesto do aplicativo para isolar-se do driver de impressora e melhorar sua confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="1faae-416">An app can declare printer driver isolation in its app manifest to isolate itself from the printer driver and improve its reliability.</span></span> <span data-ttu-id="1faae-417">Ou seja, o aplicativo não falhará se o driver da impressora tiver um erro.</span><span class="sxs-lookup"><span data-stu-id="1faae-417">That is, the app won't crash if the printer driver has an error.</span></span>


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <printerDriverIsolation>true</printerDriverIsolation>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="ultraHighResolutionScrollingAware"></span><span id="ultrahighresolutionscrollingaware"></span><span id="ULTRAHIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="ultrahighresolutionscrollingaware"></a><span data-ttu-id="1faae-418">ultraHighResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="1faae-418">ultraHighResolutionScrollingAware</span></span>

<span data-ttu-id="1faae-419">Especifica se o ultra-high-resolution-scrolling aware está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1faae-419">Specifies whether ultra-high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="1faae-420">**TRUE** indica que ele está habilitado.</span><span class="sxs-lookup"><span data-stu-id="1faae-420">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="1faae-421">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-421">It has no attributes.</span></span>

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a><span data-ttu-id="1faae-422">MSIX</span><span class="sxs-lookup"><span data-stu-id="1faae-422">msix</span></span>

<span data-ttu-id="1faae-423">Especifica as informações de identidade de um [pacote MSIX esparso](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) para o aplicativo atual.</span><span class="sxs-lookup"><span data-stu-id="1faae-423">Specifies the identity info of a [sparse MSIX package](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) for the current application.</span></span> <span data-ttu-id="1faae-424">Esse elemento tem suporte no Windows 10, versão 2004 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="1faae-424">This element is supported in Windows 10, version 2004, and later versions.</span></span>

<span data-ttu-id="1faae-425">O **elemento msix** deve estar no namespace `urn:schemas-microsoft-com:msix.v1` .</span><span class="sxs-lookup"><span data-stu-id="1faae-425">The **msix** element must be in the namespace `urn:schemas-microsoft-com:msix.v1`.</span></span> <span data-ttu-id="1faae-426">Ele tem os atributos mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1faae-426">It has the attributes shown in the following table.</span></span>

| <span data-ttu-id="1faae-427">Atributo</span><span class="sxs-lookup"><span data-stu-id="1faae-427">Attribute</span></span>   | <span data-ttu-id="1faae-428">Descrição</span><span class="sxs-lookup"><span data-stu-id="1faae-428">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1faae-429">**Editor**</span><span class="sxs-lookup"><span data-stu-id="1faae-429">**publisher**</span></span>    | <span data-ttu-id="1faae-430">Descreve as informações do editor.</span><span class="sxs-lookup"><span data-stu-id="1faae-430">Describes the publisher information.</span></span> <span data-ttu-id="1faae-431">Esse valor deve corresponder ao **atributo Publicador** no [elemento Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) no manifesto do pacote esparso.</span><span class="sxs-lookup"><span data-stu-id="1faae-431">This value must match the **Publisher** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span> |
| <span data-ttu-id="1faae-432">**packageName**</span><span class="sxs-lookup"><span data-stu-id="1faae-432">**packageName**</span></span> | <span data-ttu-id="1faae-433">Descreve o conteúdo do pacote.</span><span class="sxs-lookup"><span data-stu-id="1faae-433">Describes the contents of the package.</span></span> <span data-ttu-id="1faae-434">Esse valor deve corresponder ao **atributo Name** no [elemento Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) no manifesto do pacote esparso.</span><span class="sxs-lookup"><span data-stu-id="1faae-434">This value must match the **Name** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span>    |
| <span data-ttu-id="1faae-435">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="1faae-435">**applicationId**</span></span>    | <span data-ttu-id="1faae-436">O identificador exclusivo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1faae-436">The unique identifier of the application.</span></span> <span data-ttu-id="1faae-437">Esse valor deve corresponder ao **atributo ID** no [elemento Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) no manifesto do pacote esparso.</span><span class="sxs-lookup"><span data-stu-id="1faae-437">This value must match the **Id** attribute in the [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) element in your sparse package manifest.</span></span>  |

```xml
<?xml version="1.0" encoding="utf-8"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1">
  <assemblyIdentity version="1.0.0.0" name="Contoso.PhotoStoreApp"/>
  <msix xmlns="urn:schemas-microsoft-com:msix.v1"
          publisher="CN=Contoso"
          packageName="ContosoPhotoStore"
          applicationId="ContosoPhotoStore"
        />
</assembly>
```

### <a name="heaptype"></a><span data-ttu-id="1faae-438">heapType</span><span class="sxs-lookup"><span data-stu-id="1faae-438">heapType</span></span>

<span data-ttu-id="1faae-439">Substitui a implementação de heap padrão para as [APIs de heap do Win32](../Memory/heap-functions.md) a usar.</span><span class="sxs-lookup"><span data-stu-id="1faae-439">Overrides the default heap implementation for the [Win32 heap APIs](../Memory/heap-functions.md) to use.</span></span>

* <span data-ttu-id="1faae-440">O valor **SegmentHeap** indica que o heap de segmento será usado.</span><span class="sxs-lookup"><span data-stu-id="1faae-440">The value **SegmentHeap** indicates that segment heap will be used.</span></span> <span data-ttu-id="1faae-441">O heap de segmento é uma implementação de heap moderna que geralmente reduzirá o uso geral de memória.</span><span class="sxs-lookup"><span data-stu-id="1faae-441">Segment heap is a modern heap implementation that will generally reduce your overall memory usage.</span></span> <span data-ttu-id="1faae-442">Esse elemento tem suporte no Windows 10, versão 2004 (build 19041) e posterior.</span><span class="sxs-lookup"><span data-stu-id="1faae-442">This element is supported in Windows 10, version 2004 (build 19041) and later.</span></span>
* <span data-ttu-id="1faae-443">Todos os outros valores são ignorados.</span><span class="sxs-lookup"><span data-stu-id="1faae-443">All other values are ignored.</span></span>

<span data-ttu-id="1faae-444">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="1faae-444">This element has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">
      <heapType>SegmentHeap</heapType>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

## <a name="example"></a><span data-ttu-id="1faae-445">Exemplo</span><span class="sxs-lookup"><span data-stu-id="1faae-445">Example</span></span>

<span data-ttu-id="1faae-446">A seguir está um exemplo de um manifesto do aplicativo para um aplicativo chamado MySampleApp.exe.</span><span class="sxs-lookup"><span data-stu-id="1faae-446">The following is an example of an application manifest for an application named MySampleApp.exe.</span></span> <span data-ttu-id="1faae-447">O aplicativo consome o assembly lado a lado SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="1faae-447">The application consumes the SampleAssembly side-by-side assembly.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">

  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--This Id value indicates the application supports Windows Vista functionality -->
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--This Id value indicates the application supports Windows 7 functionality-->
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--This Id value indicates the application supports Windows 8 functionality-->
          <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
        <!--This Id value indicates the application supports Windows 8.1 functionality-->
          <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
      </application> 
  </compatibility>

  <assemblyIdentity type="win32" 
                    name="myOrganization.myDivision.mySampleApp" 
                    version="6.0.0.0" 
                    processorArchitecture="x86" 
                    publicKeyToken="0000000000000000"
  />
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" 
                        name="Proseware.Research.SampleAssembly" 
                        version="6.0.0.0" 
                        processorArchitecture="X86" 
                        publicKeyToken="0000000000000000" 
                        language="*"
      />
    </dependentAssembly>
  </dependency>
</assembly>
```
