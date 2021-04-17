---
description: Um manifesto de aplicativo é um arquivo XML que descreve e identifica os assemblies lado a lado particulares e compartilhados aos quais um aplicativo deve se associar em tempo de execução.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Manifestos do aplicativo
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: cb065bc4d6d29f4142c23cdd91c83769e2fb9b87
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "105751169"
---
# <a name="application-manifests"></a><span data-ttu-id="a3a86-103">Manifestos do aplicativo</span><span class="sxs-lookup"><span data-stu-id="a3a86-103">Application Manifests</span></span>

<span data-ttu-id="a3a86-104">Um manifesto de aplicativo é um arquivo XML que descreve e identifica os assemblies lado a lado particulares e compartilhados aos quais um aplicativo deve se associar em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="a3a86-104">An application manifest is an XML file that describes and identifies the shared and private side-by-side assemblies that an application should bind to at run time.</span></span> <span data-ttu-id="a3a86-105">Elas devem ser as mesmas versões de assembly que foram usadas para testar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-105">These should be the same assembly versions that were used to test the application.</span></span> <span data-ttu-id="a3a86-106">Os manifestos de aplicativo também podem descrever metadados para arquivos que são particulares ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-106">Application manifests may also describe metadata for files that are private to the application.</span></span>

<span data-ttu-id="a3a86-107">Para obter uma lista completa do esquema XML, consulte [manifest File Schema](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="a3a86-107">For a complete listing of the XML schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="a3a86-108">Os manifestos do aplicativo têm os seguintes elementos e atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-108">Application manifests have the following elements and attributes.</span></span>

| <span data-ttu-id="a3a86-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="a3a86-109">Element</span></span>                               | <span data-ttu-id="a3a86-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="a3a86-110">Attributes</span></span>                | <span data-ttu-id="a3a86-111">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a3a86-111">Required</span></span> |
|---------------------------------------|---------------------------|----------|
| <span data-ttu-id="a3a86-112">**)**</span><span class="sxs-lookup"><span data-stu-id="a3a86-112">**assembly**</span></span>                          |                           | <span data-ttu-id="a3a86-113">Yes</span><span class="sxs-lookup"><span data-stu-id="a3a86-113">Yes</span></span>      |
|                                       | <span data-ttu-id="a3a86-114">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="a3a86-114">**manifestVersion**</span></span>       | <span data-ttu-id="a3a86-115">Yes</span><span class="sxs-lookup"><span data-stu-id="a3a86-115">Yes</span></span>      |
| <span data-ttu-id="a3a86-116">**NoInherit**</span><span class="sxs-lookup"><span data-stu-id="a3a86-116">**noInherit**</span></span>                         |                           | <span data-ttu-id="a3a86-117">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-117">No</span></span>       |
| <span data-ttu-id="a3a86-118">**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="a3a86-118">**assemblyIdentity**</span></span>                  |                           | <span data-ttu-id="a3a86-119">Yes</span><span class="sxs-lookup"><span data-stu-id="a3a86-119">Yes</span></span>      |
|                                       | <span data-ttu-id="a3a86-120">**tipo**</span><span class="sxs-lookup"><span data-stu-id="a3a86-120">**type**</span></span>                  | <span data-ttu-id="a3a86-121">Sim</span><span class="sxs-lookup"><span data-stu-id="a3a86-121">Yes</span></span>      |
|                                       | <span data-ttu-id="a3a86-122">**name**</span><span class="sxs-lookup"><span data-stu-id="a3a86-122">**name**</span></span>                  | <span data-ttu-id="a3a86-123">Sim</span><span class="sxs-lookup"><span data-stu-id="a3a86-123">Yes</span></span>      |
|                                       | <span data-ttu-id="a3a86-124">**linguagem**</span><span class="sxs-lookup"><span data-stu-id="a3a86-124">**language**</span></span>              | <span data-ttu-id="a3a86-125">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-125">No</span></span>       |
|                                       | <span data-ttu-id="a3a86-126">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="a3a86-126">**processorArchitecture**</span></span> | <span data-ttu-id="a3a86-127">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-127">No</span></span>       |
|                                       | <span data-ttu-id="a3a86-128">**version**</span><span class="sxs-lookup"><span data-stu-id="a3a86-128">**version**</span></span>               | <span data-ttu-id="a3a86-129">Yes</span><span class="sxs-lookup"><span data-stu-id="a3a86-129">Yes</span></span>      |
|                                       | <span data-ttu-id="a3a86-130">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="a3a86-130">**publicKeyToken**</span></span>        | <span data-ttu-id="a3a86-131">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-131">No</span></span>       |
| <span data-ttu-id="a3a86-132">**compatibilidade**</span><span class="sxs-lookup"><span data-stu-id="a3a86-132">**compatibility**</span></span>                     |                           | <span data-ttu-id="a3a86-133">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-133">No</span></span>       |
| <span data-ttu-id="a3a86-134">**aplicativo**</span><span class="sxs-lookup"><span data-stu-id="a3a86-134">**application**</span></span>                       |                           | <span data-ttu-id="a3a86-135">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-135">No</span></span>       |
| <span data-ttu-id="a3a86-136">**supportedOS**</span><span class="sxs-lookup"><span data-stu-id="a3a86-136">**supportedOS**</span></span>                       | <span data-ttu-id="a3a86-137">**Id**</span><span class="sxs-lookup"><span data-stu-id="a3a86-137">**Id**</span></span>                    | <span data-ttu-id="a3a86-138">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-138">No</span></span>       |
| <span data-ttu-id="a3a86-139">**maxversiontested**</span><span class="sxs-lookup"><span data-stu-id="a3a86-139">**maxversiontested**</span></span>                  | <span data-ttu-id="a3a86-140">**Id**</span><span class="sxs-lookup"><span data-stu-id="a3a86-140">**Id**</span></span>                    | <span data-ttu-id="a3a86-141">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-141">No</span></span>       |
| <span data-ttu-id="a3a86-142">**Estados**</span><span class="sxs-lookup"><span data-stu-id="a3a86-142">**dependency**</span></span>                        |                           | <span data-ttu-id="a3a86-143">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-143">No</span></span>       |
| <span data-ttu-id="a3a86-144">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="a3a86-144">**dependentAssembly**</span></span>                 |                           | <span data-ttu-id="a3a86-145">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-145">No</span></span>       |
| <span data-ttu-id="a3a86-146">**file**</span><span class="sxs-lookup"><span data-stu-id="a3a86-146">**file**</span></span>                              |                           | <span data-ttu-id="a3a86-147">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-147">No</span></span>       |
|                                       | <span data-ttu-id="a3a86-148">**name**</span><span class="sxs-lookup"><span data-stu-id="a3a86-148">**name**</span></span>                  | <span data-ttu-id="a3a86-149">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-149">No</span></span>       |
|                                       | <span data-ttu-id="a3a86-150">**hashalg**</span><span class="sxs-lookup"><span data-stu-id="a3a86-150">**hashalg**</span></span>               | <span data-ttu-id="a3a86-151">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-151">No</span></span>       |
|                                       | <span data-ttu-id="a3a86-152">**hash**</span><span class="sxs-lookup"><span data-stu-id="a3a86-152">**hash**</span></span>                  | <span data-ttu-id="a3a86-153">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-153">No</span></span>       |
| <span data-ttu-id="a3a86-154">**activeCodePage**</span><span class="sxs-lookup"><span data-stu-id="a3a86-154">**activeCodePage**</span></span>                    |                           | <span data-ttu-id="a3a86-155">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-155">No</span></span>       |
| <span data-ttu-id="a3a86-156">**Elevação de autoelevação**</span><span class="sxs-lookup"><span data-stu-id="a3a86-156">**autoElevate**</span></span>                       |                           | <span data-ttu-id="a3a86-157">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-157">No</span></span>       |
| <span data-ttu-id="a3a86-158">**disableTheming**</span><span class="sxs-lookup"><span data-stu-id="a3a86-158">**disableTheming**</span></span>                    |                           | <span data-ttu-id="a3a86-159">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-159">No</span></span>       |
| <span data-ttu-id="a3a86-160">**disableWindowFiltering**</span><span class="sxs-lookup"><span data-stu-id="a3a86-160">**disableWindowFiltering**</span></span>            |                           | <span data-ttu-id="a3a86-161">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-161">No</span></span>       |
| <span data-ttu-id="a3a86-162">**dpiAware**</span><span class="sxs-lookup"><span data-stu-id="a3a86-162">**dpiAware**</span></span>                          |                           | <span data-ttu-id="a3a86-163">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-163">No</span></span>       |
| <span data-ttu-id="a3a86-164">**dpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="a3a86-164">**dpiAwareness**</span></span>                      |                           | <span data-ttu-id="a3a86-165">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-165">No</span></span>       |
| <span data-ttu-id="a3a86-166">**gdiScaling**</span><span class="sxs-lookup"><span data-stu-id="a3a86-166">**gdiScaling**</span></span>                        |                           | <span data-ttu-id="a3a86-167">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-167">No</span></span>       |
| <span data-ttu-id="a3a86-168">**highResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="a3a86-168">**highResolutionScrollingAware**</span></span>      |                           | <span data-ttu-id="a3a86-169">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-169">No</span></span>       |
| <span data-ttu-id="a3a86-170">**longPathAware**</span><span class="sxs-lookup"><span data-stu-id="a3a86-170">**longPathAware**</span></span>                     |                           | <span data-ttu-id="a3a86-171">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-171">No</span></span>       |
| <span data-ttu-id="a3a86-172">**printerDriverIsolation**</span><span class="sxs-lookup"><span data-stu-id="a3a86-172">**printerDriverIsolation**</span></span>            |                           | <span data-ttu-id="a3a86-173">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-173">No</span></span>       |
| <span data-ttu-id="a3a86-174">**ultraHighResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="a3a86-174">**ultraHighResolutionScrollingAware**</span></span> |                           | <span data-ttu-id="a3a86-175">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-175">No</span></span>       |
| <span data-ttu-id="a3a86-176">**MSIX**</span><span class="sxs-lookup"><span data-stu-id="a3a86-176">**msix**</span></span>                              |                           | <span data-ttu-id="a3a86-177">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-177">No</span></span>       |
| <span data-ttu-id="a3a86-178">**heaptype**</span><span class="sxs-lookup"><span data-stu-id="a3a86-178">**heapType**</span></span>                          |                           | <span data-ttu-id="a3a86-179">No</span><span class="sxs-lookup"><span data-stu-id="a3a86-179">No</span></span>       |

## <a name="file-location"></a><span data-ttu-id="a3a86-180">Local do arquivo</span><span class="sxs-lookup"><span data-stu-id="a3a86-180">File Location</span></span>

<span data-ttu-id="a3a86-181">Os manifestos do aplicativo devem ser incluídos como um recurso no arquivo EXE ou DLL do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-181">Application manifests should be included as a resource in the application's EXE file or DLL.</span></span>

<span data-ttu-id="a3a86-182">Para obter mais informações, consulte [instalando assemblies lado a lado](installing-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="a3a86-182">For more information, see [Installing Side-by-side Assemblies](installing-side-by-side-assemblies.md).</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="a3a86-183">Sintaxe de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="a3a86-183">File Name Syntax</span></span>

<span data-ttu-id="a3a86-184">O nome de um arquivo de manifesto do aplicativo é o nome do executável do aplicativo seguido por. manifest.</span><span class="sxs-lookup"><span data-stu-id="a3a86-184">The name of an application manifest file is the name of the application's executable followed by .manifest.</span></span>

<span data-ttu-id="a3a86-185">Por exemplo, um manifesto de aplicativo que se refere a example.exe ou example.dll usaria a seguinte sintaxe de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-185">For example, an application manifest that refers to example.exe or example.dll would use the following file name syntax.</span></span> <span data-ttu-id="a3a86-186">Você pode omitir o campo <*ID de recurso*> se a ID do recurso for 1.</span><span class="sxs-lookup"><span data-stu-id="a3a86-186">You can omit the <*resource ID*> field if resource ID is 1.</span></span>

<span data-ttu-id="a3a86-187">**example.exe. <*ID do recurso*>. manifest**</span><span class="sxs-lookup"><span data-stu-id="a3a86-187">**example.exe.<*resource ID*>.manifest**</span></span>

<span data-ttu-id="a3a86-188">**example.dll. <*ID do recurso*>. manifest**</span><span class="sxs-lookup"><span data-stu-id="a3a86-188">**example.dll.<*resource ID*>.manifest**</span></span>

## <a name="elements"></a><span data-ttu-id="a3a86-189">Elementos</span><span class="sxs-lookup"><span data-stu-id="a3a86-189">Elements</span></span>

<span data-ttu-id="a3a86-190">Os nomes de elementos e atributos diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a3a86-190">Names of elements and attributes are case-sensitive.</span></span> <span data-ttu-id="a3a86-191">Os valores de elementos e atributos não diferenciam maiúsculas de minúsculas, exceto para o valor do atributo de tipo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-191">The values of elements and attributes are case-insensitive, except for the value of the type attribute.</span></span>

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a><span data-ttu-id="a3a86-192">assembly</span><span class="sxs-lookup"><span data-stu-id="a3a86-192">assembly</span></span>

<span data-ttu-id="a3a86-193">Um elemento de contêiner.</span><span class="sxs-lookup"><span data-stu-id="a3a86-193">A container element.</span></span> <span data-ttu-id="a3a86-194">Seu primeiro subelemento deve ser um elemento **NoInherit** ou **AssemblyIdentity** .</span><span class="sxs-lookup"><span data-stu-id="a3a86-194">Its first subelement must be a **noInherit** or **assemblyIdentity** element.</span></span> <span data-ttu-id="a3a86-195">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a3a86-195">Required.</span></span>

<span data-ttu-id="a3a86-196">O elemento **assembly** deve estar no namespace "urn: schemas-microsoft-com: asm. v1".</span><span class="sxs-lookup"><span data-stu-id="a3a86-196">The **assembly** element must be in the namespace "urn:schemas-microsoft-com:asm.v1".</span></span> <span data-ttu-id="a3a86-197">Os elementos filho do assembly também devem estar nesse namespace, por herança ou por marcação.</span><span class="sxs-lookup"><span data-stu-id="a3a86-197">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="a3a86-198">O elemento **assembly** tem os atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a3a86-198">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="a3a86-199">Atributo</span><span class="sxs-lookup"><span data-stu-id="a3a86-199">Attribute</span></span>           | <span data-ttu-id="a3a86-200">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3a86-200">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="a3a86-201">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="a3a86-201">**manifestVersion**</span></span> | <span data-ttu-id="a3a86-202">O atributo **manifestVersion** deve ser definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="a3a86-202">The **manifestVersion** attribute must be set to 1.0.</span></span> |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a><span data-ttu-id="a3a86-203">NoInherit</span><span class="sxs-lookup"><span data-stu-id="a3a86-203">noInherit</span></span>

<span data-ttu-id="a3a86-204">Inclua esse elemento em um manifesto de aplicativo para definir os [contextos de ativação](activation-contexts.md) gerados do manifesto com o sinalizador "sem herança".</span><span class="sxs-lookup"><span data-stu-id="a3a86-204">Include this element in an application manifest to set the [activation contexts](activation-contexts.md) generated from the manifest with the "no inherit" flag.</span></span> <span data-ttu-id="a3a86-205">Quando esse sinalizador não é definido em um contexto de ativação e o contexto de ativação está ativo, ele é herdado por novos threads no mesmo processo, janelas, procedimentos de janela e [chamadas de procedimento assíncronos](/windows/desktop/Sync/asynchronous-procedure-calls).</span><span class="sxs-lookup"><span data-stu-id="a3a86-205">When this flag is not set in an activation context, and the activation context is active, it is inherited by new threads in the same process, windows, window procedures, and [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span> <span data-ttu-id="a3a86-206">Definir esse sinalizador impede que o novo objeto herde o contexto ativo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-206">Setting this flag prevents the new object from inheriting the active context.</span></span>

<span data-ttu-id="a3a86-207">O elemento **NoInherit** é opcional e normalmente é omitido.</span><span class="sxs-lookup"><span data-stu-id="a3a86-207">The **noInherit** element is optional and typically omitted.</span></span> <span data-ttu-id="a3a86-208">A maioria dos assemblies não funciona corretamente usando um contexto de ativação sem herança porque o assembly deve ser explicitamente projetado para gerenciar a propagação de seu próprio contexto de ativação.</span><span class="sxs-lookup"><span data-stu-id="a3a86-208">Most assemblies do not work correctly using a no-inherit activation context because the assembly must be explicitly designed to manage the propagation of their own activation context.</span></span> <span data-ttu-id="a3a86-209">O uso do elemento **NoInherit** requer que quaisquer assemblies dependentes referenciados pelo manifesto do aplicativo tenham um elemento **NoInherit** em seu [manifesto do assembly](assembly-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="a3a86-209">The use of the **noInherit** element requires that any dependent assemblies referenced by the application manifest have a **noInherit** element in their [assembly manifest](assembly-manifests.md).</span></span>

<span data-ttu-id="a3a86-210">Se **NoInherit** for usado em um manifesto, ele deverá ser o primeiro subelemento do elemento **assembly** .</span><span class="sxs-lookup"><span data-stu-id="a3a86-210">If **noInherit** is used in a manifest, it must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="a3a86-211">O elemento **AssemblyIdentity** deve vir imediatamente após o elemento **NoInherit** .</span><span class="sxs-lookup"><span data-stu-id="a3a86-211">The **assemblyIdentity** element should come immediately after the **noInherit** element.</span></span> <span data-ttu-id="a3a86-212">Se **NoInherit** não for usado, **AssemblyIdentity** deverá ser o primeiro subelemento do elemento **assembly** .</span><span class="sxs-lookup"><span data-stu-id="a3a86-212">If **noInherit** is not used, **assemblyIdentity** must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="a3a86-213">O elemento **NoInherit** não tem nenhum elemento filho.</span><span class="sxs-lookup"><span data-stu-id="a3a86-213">The **noInherit** element has no child elements.</span></span> <span data-ttu-id="a3a86-214">Não é um elemento válido em [manifestos de assembly](assembly-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="a3a86-214">It is not a valid element in [assembly manifests](assembly-manifests.md).</span></span>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a><span data-ttu-id="a3a86-215">assemblyIdentity</span><span class="sxs-lookup"><span data-stu-id="a3a86-215">assemblyIdentity</span></span>

<span data-ttu-id="a3a86-216">Como o primeiro subelemento de um elemento de **assembly** , **AssemblyIdentity** descreve e identifica exclusivamente o aplicativo proprietário deste manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-216">As the first subelement of an **assembly** element, **assemblyIdentity** describes and uniquely identifies the application owning this application manifest.</span></span> <span data-ttu-id="a3a86-217">Como o primeiro subelemento de um elemento **dependentAssembly** , **AssemblyIdentity** descreve um assembly lado a lado exigido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-217">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="a3a86-218">Observe que cada assembly referenciado no manifesto do aplicativo requer um **AssemblyIdentity** que corresponda exatamente ao **AssemblyIdentity** no manifesto do assembly do assembly referenciado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-218">Note that every assembly referenced in the application manifest requires an **assemblyIdentity** that exactly matches the **assemblyIdentity** in the referenced assembly's own assembly manifest.</span></span>

<span data-ttu-id="a3a86-219">O elemento **AssemblyIdentity** tem os atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="a3a86-219">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="a3a86-220">Ele não tem subelementos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-220">It has no subelements.</span></span>

| <span data-ttu-id="a3a86-221">Atributo</span><span class="sxs-lookup"><span data-stu-id="a3a86-221">Attribute</span></span>                 | <span data-ttu-id="a3a86-222">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3a86-222">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a86-223">**tipo**</span><span class="sxs-lookup"><span data-stu-id="a3a86-223">**type**</span></span>                  | <span data-ttu-id="a3a86-224">Especifica o tipo de aplicativo ou assembly.</span><span class="sxs-lookup"><span data-stu-id="a3a86-224">Specifies the application or assembly type.</span></span> <span data-ttu-id="a3a86-225">O valor deve ser Win32 e todos em letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a3a86-225">The value must be Win32 and all in lower case.</span></span> <span data-ttu-id="a3a86-226">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a3a86-226">Required.</span></span>                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="a3a86-227">**name**</span><span class="sxs-lookup"><span data-stu-id="a3a86-227">**name**</span></span>                  | <span data-ttu-id="a3a86-228">Nomeia exclusivamente o aplicativo ou o assembly.</span><span class="sxs-lookup"><span data-stu-id="a3a86-228">Uniquely names the application or assembly.</span></span> <span data-ttu-id="a3a86-229">Use o seguinte formato para o nome: Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="a3a86-229">Use the following format for the name: Organization.Division.Name.</span></span> <span data-ttu-id="a3a86-230">Por exemplo, Microsoft. Windows. mysampleApp.</span><span class="sxs-lookup"><span data-stu-id="a3a86-230">For example Microsoft.Windows.mysampleApp.</span></span> <span data-ttu-id="a3a86-231">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a3a86-231">Required.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a3a86-232">**linguagem**</span><span class="sxs-lookup"><span data-stu-id="a3a86-232">**language**</span></span>              | <span data-ttu-id="a3a86-233">Identifica o idioma do aplicativo ou assembly.</span><span class="sxs-lookup"><span data-stu-id="a3a86-233">Identifies the language of the application or assembly.</span></span> <span data-ttu-id="a3a86-234">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a3a86-234">Optional.</span></span> <span data-ttu-id="a3a86-235">Se o aplicativo ou o assembly for específico a um idioma, especifique o código de linguagem DHTML.</span><span class="sxs-lookup"><span data-stu-id="a3a86-235">If the application or assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="a3a86-236">No **AssemblyIdentity** de um aplicativo destinado para uso mundial (neutro à linguagem), omita o atributo language.</span><span class="sxs-lookup"><span data-stu-id="a3a86-236">In the **assemblyIdentity** of an application intended for worldwide use (language neutral) omit the language attribute.</span></span><br/> <span data-ttu-id="a3a86-237">Em um **AssemblyIdentity** de um assembly destinado para uso mundial (neutro à linguagem), defina o valor de idioma como " \* ".</span><span class="sxs-lookup"><span data-stu-id="a3a86-237">In an **assemblyIdentity** of an assembly intended for worldwide use (language neutral) set the value of language to "\*".</span></span><br/> |
| <span data-ttu-id="a3a86-238">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="a3a86-238">**processorArchitecture**</span></span> | <span data-ttu-id="a3a86-239">Especifica o processador.</span><span class="sxs-lookup"><span data-stu-id="a3a86-239">Specifies the processor.</span></span> <span data-ttu-id="a3a86-240">Os valores válidos incluem `x86`, `amd64`, `arm` e `arm64`.</span><span class="sxs-lookup"><span data-stu-id="a3a86-240">Valid values include `x86`, `amd64`, `arm` and `arm64`.</span></span> <span data-ttu-id="a3a86-241">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a3a86-241">Optional.</span></span>                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="a3a86-242">**version**</span><span class="sxs-lookup"><span data-stu-id="a3a86-242">**version**</span></span>               | <span data-ttu-id="a3a86-243">Especifica a versão do aplicativo ou do assembly.</span><span class="sxs-lookup"><span data-stu-id="a3a86-243">Specifies the application or assembly version.</span></span> <span data-ttu-id="a3a86-244">Use o formato de versão de quatro partes: mmmmm. NNNNN. Ooooo. ppppp.</span><span class="sxs-lookup"><span data-stu-id="a3a86-244">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="a3a86-245">Cada uma das partes separadas por períodos pode ser de 0-65535 inclusive.</span><span class="sxs-lookup"><span data-stu-id="a3a86-245">Each of the parts separated by periods can be 0-65535 inclusive.</span></span> <span data-ttu-id="a3a86-246">Para obter mais informações, consulte [versões de assembly](assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="a3a86-246">For more information, see [Assembly Versions](assembly-versions.md).</span></span> <span data-ttu-id="a3a86-247">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="a3a86-247">Required.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="a3a86-248">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="a3a86-248">**publicKeyToken**</span></span>        | <span data-ttu-id="a3a86-249">Uma cadeia de caracteres hexadecimal de 16 caracteres que representa os últimos 8 bytes do hash SHA-1 da chave pública sob a qual o aplicativo ou assembly é assinado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-249">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the application or assembly is signed.</span></span> <span data-ttu-id="a3a86-250">A chave pública usada para assinar o catálogo deve ter 2048 bits ou mais.</span><span class="sxs-lookup"><span data-stu-id="a3a86-250">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="a3a86-251">Necessário para todos os assemblies compartilhados lado a lado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-251">Required for all shared side-by-side assemblies.</span></span>                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a><span data-ttu-id="a3a86-252">compatibilidade</span><span class="sxs-lookup"><span data-stu-id="a3a86-252">compatibility</span></span>

<span data-ttu-id="a3a86-253">Contém pelo menos um **aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="a3a86-253">Contains at least one **application**.</span></span> <span data-ttu-id="a3a86-254">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-254">It has no attributes.</span></span> <span data-ttu-id="a3a86-255">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a3a86-255">Optional.</span></span> <span data-ttu-id="a3a86-256">Manifestos do aplicativo sem um elemento de compatibilidade padrão para compatibilidade com o Windows Vista no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a3a86-256">Application manifests without a compatibility element default to Windows Vista compatibility on Windows 7.</span></span>

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a><span data-ttu-id="a3a86-257">aplicativo</span><span class="sxs-lookup"><span data-stu-id="a3a86-257">application</span></span>

<span data-ttu-id="a3a86-258">Contém pelo menos um elemento **supportedOS** .</span><span class="sxs-lookup"><span data-stu-id="a3a86-258">Contains at least one **supportedOS** element.</span></span> <span data-ttu-id="a3a86-259">A partir do Windows 10, versão 1903, ele também pode conter um elemento **maxversiontested** opcional.</span><span class="sxs-lookup"><span data-stu-id="a3a86-259">Starting in Windows 10, version 1903, it can also contain one optional **maxversiontested** element.</span></span> <span data-ttu-id="a3a86-260">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-260">It has no attributes.</span></span> <span data-ttu-id="a3a86-261">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a3a86-261">Optional.</span></span>

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a><span data-ttu-id="a3a86-262">supportedOS</span><span class="sxs-lookup"><span data-stu-id="a3a86-262">supportedOS</span></span>

<span data-ttu-id="a3a86-263">O elemento **supportedOS** tem o atributo a seguir.</span><span class="sxs-lookup"><span data-stu-id="a3a86-263">The **supportedOS** element has the following attribute.</span></span> <span data-ttu-id="a3a86-264">Ele não tem subelementos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-264">It has no subelements.</span></span>

| <span data-ttu-id="a3a86-265">Atributo</span><span class="sxs-lookup"><span data-stu-id="a3a86-265">Attribute</span></span> | <span data-ttu-id="a3a86-266">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3a86-266">Description</span></span>   |
|-----------|-----------------------|
| <span data-ttu-id="a3a86-267">**Id**</span><span class="sxs-lookup"><span data-stu-id="a3a86-267">**Id**</span></span>    | <span data-ttu-id="a3a86-268">Defina o atributo ID como **{e2011457-1546-43c5-a5fe-008deee3d3f0}** para executar o aplicativo usando a funcionalidade do vista.</span><span class="sxs-lookup"><span data-stu-id="a3a86-268">Set the Id attribute to **{e2011457-1546-43c5-a5fe-008deee3d3f0}** to run the application using Vista functionality.</span></span> <span data-ttu-id="a3a86-269">Isso pode permitir que um aplicativo projetado para o Windows Vista seja executado em um sistema operacional posterior.</span><span class="sxs-lookup"><span data-stu-id="a3a86-269">This can enable an application designed for Windows Vista to run on a later operating system.</span></span> <br/> <span data-ttu-id="a3a86-270">Defina o atributo ID como **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** para executar o aplicativo usando a funcionalidade do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a3a86-270">Set the Id attribute to **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** to run the application using Windows 7 functionality.</span></span><br/> <span data-ttu-id="a3a86-271">Os aplicativos que dão suporte à funcionalidade do Windows Vista, do Windows 7 e do Windows 8 não exigem manifestos separados.</span><span class="sxs-lookup"><span data-stu-id="a3a86-271">Applications that support Windows Vista, Windows 7, and Windows 8 functionality do not require separate manifests.</span></span> <span data-ttu-id="a3a86-272">Nesse caso, adicione os GUIDs para todos os sistemas operacionais Windows.</span><span class="sxs-lookup"><span data-stu-id="a3a86-272">In this case, add the GUIDs for all the Windows operating systems.</span></span><br/> <span data-ttu-id="a3a86-273">Para obter informações sobre o comportamento de atributo de **ID** no Windows, consulte o manual de compatibilidade do Windows [8 e do Windows Server 2012](https://www.microsoft.com/download/details.aspx?id=27416).</span><span class="sxs-lookup"><span data-stu-id="a3a86-273">For info about the **Id** attribute behavior in Windows, see the [Windows 8 and Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span></span><br/> <span data-ttu-id="a3a86-274">Os GUIDs a seguir correspondem aos sistemas operacionais Indicados:</span><span class="sxs-lookup"><span data-stu-id="a3a86-274">The following GUIDs correspond with the indicated operating systems:</span></span><br/> <span data-ttu-id="a3a86-275">**{8e0f7a12-bfb3-4FE8-B9A5-48fd50a15a9a}** -> Windows 10, windows Server 2016 e windows Server 2019</span><span class="sxs-lookup"><span data-stu-id="a3a86-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 and Windows Server 2019</span></span><br/> <span data-ttu-id="a3a86-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 e Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a3a86-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 and Windows Server 2012 R2</span></span><br/> <span data-ttu-id="a3a86-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 e windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3a86-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 and Windows Server 2012</span></span><br/> <span data-ttu-id="a3a86-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 e windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a3a86-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 and Windows Server 2008 R2</span></span><br/> <span data-ttu-id="a3a86-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> o Windows Vista e o windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3a86-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista and Windows Server 2008</span></span><br/> <span data-ttu-id="a3a86-280">Você pode testar isso no Windows 7 ou no Windows 8. x executando Monitor de Recursos (resmon), acessando a guia CPU, clicando com o botão direito do mouse nos rótulos de coluna, "Selecionar coluna..." e confira "contexto do sistema operacional".</span><span class="sxs-lookup"><span data-stu-id="a3a86-280">You can test this on Windows 7 or Windows 8.x by running Resource Monitor (resmon), going to the CPU tab, right-clicking on the column labels, "Select Column...", and check "Operating System Context".</span></span> <span data-ttu-id="a3a86-281">No Windows 8. x, você também pode encontrar essa coluna disponível no Gerenciador de tarefas (taskmgr).</span><span class="sxs-lookup"><span data-stu-id="a3a86-281">On Windows 8.x, you can also find this column available in the Task Manager (taskmgr).</span></span> <span data-ttu-id="a3a86-282">O conteúdo da coluna mostra o valor mais alto encontrado ou "Windows Vista" como o padrão.</span><span class="sxs-lookup"><span data-stu-id="a3a86-282">The content of the column shows the highest value found or "Windows Vista" as the default.</span></span> <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a><span data-ttu-id="a3a86-283">maxversiontested</span><span class="sxs-lookup"><span data-stu-id="a3a86-283">maxversiontested</span></span>

<span data-ttu-id="a3a86-284">O elemento **maxversiontested** especifica a versão máxima do Windows para a qual o aplicativo foi testado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-284">The **maxversiontested** element specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="a3a86-285">Isso se destina a ser usado por aplicativos de área de trabalho que usam [ilhas XAML](/windows/apps/desktop/modernize/xaml-islands) e que não são implantados em um pacote MSIX.</span><span class="sxs-lookup"><span data-stu-id="a3a86-285">This is intended to be used by desktop applications that use [XAML Islands](/windows/apps/desktop/modernize/xaml-islands) and that are not deployed in an MSIX package.</span></span> <span data-ttu-id="a3a86-286">Esse elemento tem suporte no Windows 10, versão 1903 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="a3a86-286">This element is supported in Windows 10, version 1903, and later versions.</span></span>

<span data-ttu-id="a3a86-287">O elemento **maxversiontested** tem o atributo a seguir.</span><span class="sxs-lookup"><span data-stu-id="a3a86-287">The **maxversiontested** element has the following attribute.</span></span> <span data-ttu-id="a3a86-288">Ele não tem subelementos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-288">It has no subelements.</span></span>

| <span data-ttu-id="a3a86-289">Atributo</span><span class="sxs-lookup"><span data-stu-id="a3a86-289">Attribute</span></span> | <span data-ttu-id="a3a86-290">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3a86-290">Description</span></span>    |
|-----------|----------------|
| <span data-ttu-id="a3a86-291">**Id**</span><span class="sxs-lookup"><span data-stu-id="a3a86-291">**Id**</span></span>    | <span data-ttu-id="a3a86-292">Defina o atributo ID como uma cadeia de caracteres de versão de 4 partes que especifica a versão máxima do Windows para a qual o aplicativo foi testado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-292">Set the Id attribute to a 4-part version string that specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="a3a86-293">Por exemplo, "10.0.18226.0".</span><span class="sxs-lookup"><span data-stu-id="a3a86-293">For example, "10.0.18226.0".</span></span> |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a><span data-ttu-id="a3a86-294">dependência</span><span class="sxs-lookup"><span data-stu-id="a3a86-294">dependency</span></span>

<span data-ttu-id="a3a86-295">Contém pelo menos um **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="a3a86-295">Contains at least one **dependentAssembly**.</span></span> <span data-ttu-id="a3a86-296">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-296">It has no attributes.</span></span> <span data-ttu-id="a3a86-297">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a3a86-297">Optional.</span></span>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a><span data-ttu-id="a3a86-298">dependentAssembly</span><span class="sxs-lookup"><span data-stu-id="a3a86-298">dependentAssembly</span></span>

<span data-ttu-id="a3a86-299">O primeiro subelemento de **dependentAssembly** deve ser um elemento **AssemblyIdentity** que descreve um assembly lado a lado exigido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-299">The first subelement of **dependentAssembly** must be an **assemblyIdentity** element that describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="a3a86-300">Cada **dependentAssembly** deve estar dentro de exatamente uma **dependência**.</span><span class="sxs-lookup"><span data-stu-id="a3a86-300">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="a3a86-301">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-301">It has no attributes.</span></span>

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a><span data-ttu-id="a3a86-302">arquivo</span><span class="sxs-lookup"><span data-stu-id="a3a86-302">file</span></span>

<span data-ttu-id="a3a86-303">Especifica os arquivos que são privados para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-303">Specifies files that are private to the application.</span></span> <span data-ttu-id="a3a86-304">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a3a86-304">Optional.</span></span>

<span data-ttu-id="a3a86-305">O elemento **File** tem os atributos mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a3a86-305">The **file** element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="a3a86-306">Atributo</span><span class="sxs-lookup"><span data-stu-id="a3a86-306">Attribute</span></span>   | <span data-ttu-id="a3a86-307">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3a86-307">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a86-308">**name**</span><span class="sxs-lookup"><span data-stu-id="a3a86-308">**name**</span></span>    | <span data-ttu-id="a3a86-309">Nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-309">Name of the file.</span></span> <span data-ttu-id="a3a86-310">Por exemplo, Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="a3a86-310">For example, Comctl32.dll.</span></span>                                                            |
| <span data-ttu-id="a3a86-311">**hashalg**</span><span class="sxs-lookup"><span data-stu-id="a3a86-311">**hashalg**</span></span> | <span data-ttu-id="a3a86-312">Algoritmo usado para criar um hash do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-312">Algorithm used to create a hash of the file.</span></span> <span data-ttu-id="a3a86-313">Esse valor deve ser SHA1.</span><span class="sxs-lookup"><span data-stu-id="a3a86-313">This value should be SHA1.</span></span>                                 |
| <span data-ttu-id="a3a86-314">**hash**</span><span class="sxs-lookup"><span data-stu-id="a3a86-314">**hash**</span></span>    | <span data-ttu-id="a3a86-315">Um hash do arquivo referido pelo nome.</span><span class="sxs-lookup"><span data-stu-id="a3a86-315">A hash of the file referred to by name.</span></span> <span data-ttu-id="a3a86-316">Uma cadeia de caracteres hexadecimal de comprimento, dependendo do algoritmo de hash.</span><span class="sxs-lookup"><span data-stu-id="a3a86-316">A hexadecimal string of length depending on the hash algorithm.</span></span> |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a><span data-ttu-id="a3a86-317">activeCodePage</span><span class="sxs-lookup"><span data-stu-id="a3a86-317">activeCodePage</span></span>

<span data-ttu-id="a3a86-318">Force um processo a usar UTF-8 como a página de código do processo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-318">Force a process to use UTF-8 as the process code page.</span></span>

<span data-ttu-id="a3a86-319">o **activeCodePage** foi adicionado na versão 1903 do Windows (maio de 2019 atualização).</span><span class="sxs-lookup"><span data-stu-id="a3a86-319">**activeCodePage** was added in Windows Version 1903 (May 2019 Update).</span></span> <span data-ttu-id="a3a86-320">Você pode declarar essa propriedade e o destino/executar em compilações anteriores do Windows, mas você deve manipular a detecção de página de código herdada e a conversão como de costume.</span><span class="sxs-lookup"><span data-stu-id="a3a86-320">You can declare this property and target/run on earlier Windows builds, but you must handle legacy code page detection and conversion as usual.</span></span> <span data-ttu-id="a3a86-321">Consulte [usar a página de código UTF-8](/windows/uwp/design/globalizing/use-utf8-code-page) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="a3a86-321">See [Use the UTF-8 code page](/windows/uwp/design/globalizing/use-utf8-code-page) for details.</span></span>

<span data-ttu-id="a3a86-322">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-322">This element has no attributes.</span></span> <span data-ttu-id="a3a86-323">**UTF-8** é apenas um valor válido para o elemento **activeCodePage** .</span><span class="sxs-lookup"><span data-stu-id="a3a86-323">**UTF-8** is only valid value for **activeCodePage** element.</span></span>

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

### <a name="autoelevate"></a><span data-ttu-id="a3a86-324">Elevação de autoelevação</span><span class="sxs-lookup"><span data-stu-id="a3a86-324">autoElevate</span></span>

<span data-ttu-id="a3a86-325">Especifica se a elevação automática está habilitada.</span><span class="sxs-lookup"><span data-stu-id="a3a86-325">Specifies whether auto elevate is enabled.</span></span> <span data-ttu-id="a3a86-326">**Verdadeiro** indica que está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-326">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="a3a86-327">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-327">It has no attributes.</span></span>

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a><span data-ttu-id="a3a86-328">disableTheming</span><span class="sxs-lookup"><span data-stu-id="a3a86-328">disableTheming</span></span>

<span data-ttu-id="a3a86-329">Especifica se a concessão de elementos da interface do usuário um tema está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-329">Specifies whether giving UI elements a theme is disabled.</span></span> <span data-ttu-id="a3a86-330">**Verdadeiro** indica desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-330">**TRUE** indicates disabled.</span></span> <span data-ttu-id="a3a86-331">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-331">It has no attributes.</span></span>

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a><span data-ttu-id="a3a86-332">disableWindowFiltering</span><span class="sxs-lookup"><span data-stu-id="a3a86-332">disableWindowFiltering</span></span>

<span data-ttu-id="a3a86-333">Especifica se a filtragem de janela deve ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="a3a86-333">Specifies whether to disable window filtering.</span></span> <span data-ttu-id="a3a86-334">**Verdadeiro** desabilita a filtragem de janela para que você possa enumerar janelas de imersão da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="a3a86-334">**TRUE** disables window filtering so you can enumerate immersive windows from the desktop.</span></span> <span data-ttu-id="a3a86-335">**disableWindowFiltering** foi adicionado ao Windows 8 e não tem nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-335">**disableWindowFiltering** was added in Windows 8 and has no attributes.</span></span>

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

### <a name="dpiaware"></a><span data-ttu-id="a3a86-336">dpiAware</span><span class="sxs-lookup"><span data-stu-id="a3a86-336">dpiAware</span></span>

<span data-ttu-id="a3a86-337">Especifica se o processo atual tem reconhecimento de pontos por polegada (DPI).</span><span class="sxs-lookup"><span data-stu-id="a3a86-337">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="a3a86-338">**Windows 10, versão 1607:** O elemento **dpiAware** será ignorado se o elemento **dpiAwareness** estiver presente.</span><span class="sxs-lookup"><span data-stu-id="a3a86-338">**Windows 10, version 1607:** The **dpiAware** element is ignored if the **dpiAwareness** element is present.</span></span> <span data-ttu-id="a3a86-339">Você pode incluir os dois elementos em um manifesto se quiser especificar um comportamento diferente para o Windows 10, versão 1607 do que para uma versão anterior do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a3a86-339">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="a3a86-340">A tabela a seguir descreve o comportamento que resulta com base na presença do elemento **dpiAware** e no texto que ele contém.</span><span class="sxs-lookup"><span data-stu-id="a3a86-340">The following table describes the behavior that results based upon the presence of the **dpiAware** element and the text that it contains.</span></span> <span data-ttu-id="a3a86-341">O texto dentro do elemento não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a3a86-341">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="a3a86-342">Estado do elemento **dpiAware**</span><span class="sxs-lookup"><span data-stu-id="a3a86-342">State of the **dpiAware** element</span></span> | <span data-ttu-id="a3a86-343">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3a86-343">Description</span></span>     |
|-----------------------------------|---------|
| <span data-ttu-id="a3a86-344">Absent</span><span class="sxs-lookup"><span data-stu-id="a3a86-344">Absent</span></span>                            | <span data-ttu-id="a3a86-345">O processo atual é DPI sem reconhecimento por padrão.</span><span class="sxs-lookup"><span data-stu-id="a3a86-345">The current process is dpi unaware by default.</span></span> <span data-ttu-id="a3a86-346">Você pode alterar programaticamente essa configuração chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="a3a86-346">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>                                                                                                                                                            |
| <span data-ttu-id="a3a86-347">Contém "true"</span><span class="sxs-lookup"><span data-stu-id="a3a86-347">Contains "true"</span></span>                   | <span data-ttu-id="a3a86-348">O processo atual reconhece o DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="a3a86-348">The current process is system dpi aware.</span></span>                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="a3a86-349">Contém "false"</span><span class="sxs-lookup"><span data-stu-id="a3a86-349">Contains "false"</span></span>                  | <span data-ttu-id="a3a86-350">**Windows Vista, Windows 7 e Windows 8:** O comportamento é o mesmo que quando o **dpiAware** está ausente.</span><span class="sxs-lookup"><span data-stu-id="a3a86-350">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="a3a86-351">**Windows 8.1 e Windows 10:** O processo atual é de reconhecimento de dpi e não é possível alterar programaticamente essa configuração chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="a3a86-351">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |
| <span data-ttu-id="a3a86-352">Contém "true/PM"</span><span class="sxs-lookup"><span data-stu-id="a3a86-352">Contains "true/pm"</span></span>                | <span data-ttu-id="a3a86-353">**Windows Vista, Windows 7 e Windows 8:** O processo atual reconhece o DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="a3a86-353">**Windows Vista, Windows 7 and Windows 8:** The current process is system dpi aware.</span></span><br/> <span data-ttu-id="a3a86-354">**Windows 8.1 e Windows 10:** O processo atual tem reconhecimento de DPI por monitor.</span><span class="sxs-lookup"><span data-stu-id="a3a86-354">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="a3a86-355">Contém "por monitor"</span><span class="sxs-lookup"><span data-stu-id="a3a86-355">Contains "per monitor"</span></span>            | <span data-ttu-id="a3a86-356">**Windows Vista, Windows 7 e Windows 8:** O comportamento é o mesmo que quando o **dpiAware** está ausente.</span><span class="sxs-lookup"><span data-stu-id="a3a86-356">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="a3a86-357">**Windows 8.1 e Windows 10:** O processo atual tem reconhecimento de DPI por monitor.</span><span class="sxs-lookup"><span data-stu-id="a3a86-357">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="a3a86-358">Contém qualquer outra cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="a3a86-358">Contains any other string</span></span>         | <span data-ttu-id="a3a86-359">**Windows Vista, Windows 7 e Windows 8:** O comportamento é o mesmo que quando o **dpiAware** está ausente.</span><span class="sxs-lookup"><span data-stu-id="a3a86-359">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="a3a86-360">**Windows 8.1 e Windows 10:** O processo atual é de reconhecimento de dpi e não é possível alterar programaticamente essa configuração chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="a3a86-360">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |

<span data-ttu-id="a3a86-361">Para obter mais informações sobre configurações de reconhecimento de DPI, consulte [comparação de níveis de reconhecimento de DPI](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="a3a86-361">For more information about dpi awareness settings, see [Comparison of DPI Awareness Levels](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

<span data-ttu-id="a3a86-362">**dpiAware** não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-362">**dpiAware** has no attributes.</span></span>

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

### <a name="dpiawareness"></a><span data-ttu-id="a3a86-363">dpiAwareness</span><span class="sxs-lookup"><span data-stu-id="a3a86-363">dpiAwareness</span></span>

<span data-ttu-id="a3a86-364">Especifica se o processo atual tem reconhecimento de pontos por polegada (DPI).</span><span class="sxs-lookup"><span data-stu-id="a3a86-364">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="a3a86-365">A versão mínima do sistema operacional que dá suporte ao elemento **dpiAwareness** é Windows 10, versão 1607.</span><span class="sxs-lookup"><span data-stu-id="a3a86-365">The minimum version of the operating system that supports the **dpiAwareness** element is Windows 10, version 1607.</span></span> <span data-ttu-id="a3a86-366">Para versões que dão suporte ao elemento **dpiAwareness** , o **dpiAwareness** substitui o elemento **dpiAware** .</span><span class="sxs-lookup"><span data-stu-id="a3a86-366">For versions that support the **dpiAwareness** element, the **dpiAwareness** overrides the **dpiAware** element.</span></span> <span data-ttu-id="a3a86-367">Você pode incluir os dois elementos em um manifesto se quiser especificar um comportamento diferente para o Windows 10, versão 1607 do que para uma versão anterior do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a3a86-367">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="a3a86-368">O elemento **dpiAwareness** pode conter um único item ou uma lista de itens separados por vírgula.</span><span class="sxs-lookup"><span data-stu-id="a3a86-368">The **dpiAwareness** element can contain a single item or a list of comma-separated items.</span></span> <span data-ttu-id="a3a86-369">No último caso, o primeiro item (mais à esquerda) na lista reconhecida pelo sistema operacional é usado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-369">In the latter case, the first (leftmost) item in the list recognized by the operating system is used.</span></span> <span data-ttu-id="a3a86-370">Dessa forma, você pode especificar diferentes comportamentos com suporte em versões futuras do sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="a3a86-370">In this way, you can specify different behaviors supported in future Windows operating system versions.</span></span>

<span data-ttu-id="a3a86-371">A tabela a seguir descreve o comportamento que resulta com base na presença do elemento **dpiAwareness** e no texto que ele contém em seu item reconhecido mais à esquerda.</span><span class="sxs-lookup"><span data-stu-id="a3a86-371">The following table describes the behavior that results based upon the presence of the **dpiAwareness** element and the text that it contains in its leftmost recognized item.</span></span> <span data-ttu-id="a3a86-372">O texto dentro do elemento não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a3a86-372">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="a3a86-373">status do elemento **dpiAwareness** :</span><span class="sxs-lookup"><span data-stu-id="a3a86-373">**dpiAwareness** element status:</span></span>        | <span data-ttu-id="a3a86-374">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3a86-374">Description</span></span>                          |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="a3a86-375">Elemento ausente</span><span class="sxs-lookup"><span data-stu-id="a3a86-375">Element is absent</span></span>                       | <span data-ttu-id="a3a86-376">O elemento **dpiAware** especifica se o processo tem reconhecimento de DPI.</span><span class="sxs-lookup"><span data-stu-id="a3a86-376">The **dpiAware** element specifies whether the process is dpi aware.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="a3a86-377">Não contém itens reconhecidos</span><span class="sxs-lookup"><span data-stu-id="a3a86-377">Contains no recognized items</span></span>            | <span data-ttu-id="a3a86-378">O processo atual é DPI sem reconhecimento por padrão.</span><span class="sxs-lookup"><span data-stu-id="a3a86-378">The current process is dpi unaware by default.</span></span> <span data-ttu-id="a3a86-379">Você pode alterar programaticamente essa configuração chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="a3a86-379">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span> |
| <span data-ttu-id="a3a86-380">O primeiro item reconhecido é "System"</span><span class="sxs-lookup"><span data-stu-id="a3a86-380">First recognized item is "system"</span></span>       | <span data-ttu-id="a3a86-381">O processo atual reconhece o DPI do sistema.</span><span class="sxs-lookup"><span data-stu-id="a3a86-381">The current process is system dpi aware.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="a3a86-382">O primeiro item reconhecido é "permonitor"</span><span class="sxs-lookup"><span data-stu-id="a3a86-382">First recognized item is "permonitor"</span></span>   | <span data-ttu-id="a3a86-383">O processo atual tem reconhecimento de DPI por monitor.</span><span class="sxs-lookup"><span data-stu-id="a3a86-383">The current process is per-monitor dpi aware.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="a3a86-384">O primeiro item reconhecido é "permonitorv2"</span><span class="sxs-lookup"><span data-stu-id="a3a86-384">First recognized item is "permonitorv2"</span></span> | <span data-ttu-id="a3a86-385">O processo atual usa o contexto de reconhecimento de DPI por monitor v2.</span><span class="sxs-lookup"><span data-stu-id="a3a86-385">The current process uses the per-monitor-v2 dpi awareness context.</span></span> <span data-ttu-id="a3a86-386">Este item só será reconhecido no Windows 10 versão 1703 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a3a86-386">This item will only be recognized on Windows 10 version 1703 or later.</span></span>                                                                                              |
| <span data-ttu-id="a3a86-387">O primeiro item reconhecido é "sem reconhecimento"</span><span class="sxs-lookup"><span data-stu-id="a3a86-387">First recognized item is "unaware"</span></span>      | <span data-ttu-id="a3a86-388">O processo atual não reconhece dpi.</span><span class="sxs-lookup"><span data-stu-id="a3a86-388">The current process is dpi unaware.</span></span> <span data-ttu-id="a3a86-389">Você **não pode** alterar essa configuração programaticamente chamando a função [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="a3a86-389">You **cannot** programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>      |

<span data-ttu-id="a3a86-390">Para obter mais informações sobre configurações de reconhecimento de DPI com suporte neste elemento, consulte [ \_ reconhecimento de DPI](/windows/desktop/api/windef/ne-windef-dpi_awareness) e [contexto de \_ reconhecimento \_ de DPI](/windows/desktop/hidpi/dpi-awareness-context).</span><span class="sxs-lookup"><span data-stu-id="a3a86-390">For more information about dpi awareness settings supported by this element, see [DPI\_AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) and [DPI\_AWARENESS\_CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).</span></span>

<span data-ttu-id="a3a86-391">**dpiAwareness** não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-391">**dpiAwareness** has no attributes.</span></span>

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

### <a name="gdiscaling"></a><span data-ttu-id="a3a86-392">gdiScaling</span><span class="sxs-lookup"><span data-stu-id="a3a86-392">gdiScaling</span></span>

<span data-ttu-id="a3a86-393">Especifica se o dimensionamento GDI está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-393">Specifies whether GDI scaling is enabled.</span></span> <span data-ttu-id="a3a86-394">A versão mínima do sistema operacional que dá suporte ao elemento **gdiScaling** é Windows 10 versão 1703.</span><span class="sxs-lookup"><span data-stu-id="a3a86-394">The minimum version of the operating system that supports the **gdiScaling** element is Windows 10 version 1703.</span></span>

<span data-ttu-id="a3a86-395">A estrutura GDI (Graphics Device Interface) pode aplicar o dimensionamento de DPI a primitivos e texto por monitor sem atualizações para o próprio aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-395">The GDI (graphics device interface) framework can apply DPI scaling to primitives and text on a per-monitor basis without updates to the application itself.</span></span> <span data-ttu-id="a3a86-396">Isso pode ser útil para aplicativos GDI que não estão mais sendo atualizados ativamente.</span><span class="sxs-lookup"><span data-stu-id="a3a86-396">This can be useful for GDI applications no longer being actively updated.</span></span>

<span data-ttu-id="a3a86-397">Elementos gráficos não vetoriais (como bitmaps, ícones ou barras de ferramentas) não podem ser dimensionados por este elemento.</span><span class="sxs-lookup"><span data-stu-id="a3a86-397">Non-vector graphics (such as bitmaps, icons, or toolbars) cannot be scaled by this element.</span></span> <span data-ttu-id="a3a86-398">Além disso, elementos gráficos e texto que aparecem em bitmaps construídos dinamicamente por aplicativos também não podem ser dimensionados por esse elemento.</span><span class="sxs-lookup"><span data-stu-id="a3a86-398">In addition, graphics and text appearing within bitmaps dynamically constructed by applications also cannot be scaled by this element.</span></span>

<span data-ttu-id="a3a86-399">**Verdadeiro** indica que esse elemento está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-399">**TRUE** indicates that this element is enabled.</span></span> <span data-ttu-id="a3a86-400">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-400">It has no attributes.</span></span>


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

### <a name="highresolutionscrollingaware"></a><span data-ttu-id="a3a86-401">highResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="a3a86-401">highResolutionScrollingAware</span></span>

<span data-ttu-id="a3a86-402">Especifica se o reconhecimento da rolagem de alta resolução está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-402">Specifies whether high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="a3a86-403">**Verdadeiro** indica que está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-403">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="a3a86-404">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-404">It has no attributes.</span></span>

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a><span data-ttu-id="a3a86-405">longPathAware</span><span class="sxs-lookup"><span data-stu-id="a3a86-405">longPathAware</span></span>

<span data-ttu-id="a3a86-406">Habilita caminhos longos que excedem **MAX_PATH** de comprimento.</span><span class="sxs-lookup"><span data-stu-id="a3a86-406">Enables long paths that exceed **MAX_PATH** in length.</span></span> <span data-ttu-id="a3a86-407">Esse elemento tem suporte no Windows 10, versão 1607 e posterior.</span><span class="sxs-lookup"><span data-stu-id="a3a86-407">This element is supported in Windows 10, version 1607, and later.</span></span> <span data-ttu-id="a3a86-408">Para obter mais informações, consulte [este artigo](../fileio/maximum-file-path-limitation.md).</span><span class="sxs-lookup"><span data-stu-id="a3a86-408">For more information, see [this article](../fileio/maximum-file-path-limitation.md).</span></span>

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

### <a name="printerdriverisolation"></a><span data-ttu-id="a3a86-409">printerDriverIsolation</span><span class="sxs-lookup"><span data-stu-id="a3a86-409">printerDriverIsolation</span></span>

<span data-ttu-id="a3a86-410">Especifica se o isolamento de driver de impressora está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-410">Specifies whether printer driver isolation is enabled.</span></span> <span data-ttu-id="a3a86-411">**Verdadeiro** indica que está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-411">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="a3a86-412">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-412">It has no attributes.</span></span> <span data-ttu-id="a3a86-413">O isolamento do driver de impressora melhora a confiabilidade do serviço de impressão do Windows permitindo que os drivers de impressora sejam executados em processos separados do processo no qual o spooler de impressão é executado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-413">Printer driver isolation improves the reliability of the Windows print service by enabling printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="a3a86-414">Suporte para isolamento de driver de impressora iniciado no Windows 7 e no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="a3a86-414">Support for printer driver isolation started in Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="a3a86-415">Um aplicativo pode declarar o isolamento do driver de impressora em seu manifesto de aplicativo para se isolar do driver de impressora e melhorar sua confiabilidade.</span><span class="sxs-lookup"><span data-stu-id="a3a86-415">An app can declare printer driver isolation in its app manifest to isolate itself from the printer driver and improve its reliability.</span></span> <span data-ttu-id="a3a86-416">Ou seja, o aplicativo não falhará se o driver de impressora tiver um erro.</span><span class="sxs-lookup"><span data-stu-id="a3a86-416">That is, the app won't crash if the printer driver has an error.</span></span>


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

### <a name="ultrahighresolutionscrollingaware"></a><span data-ttu-id="a3a86-417">ultraHighResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="a3a86-417">ultraHighResolutionScrollingAware</span></span>

<span data-ttu-id="a3a86-418">Especifica se o reconhecimento de rolagem de resolução extremamente alta está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-418">Specifies whether ultra-high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="a3a86-419">**Verdadeiro** indica que está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-419">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="a3a86-420">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-420">It has no attributes.</span></span>

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a><span data-ttu-id="a3a86-421">MSIX</span><span class="sxs-lookup"><span data-stu-id="a3a86-421">msix</span></span>

<span data-ttu-id="a3a86-422">Especifica as informações de identidade de um [pacote MSIX esparso](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) para o aplicativo atual.</span><span class="sxs-lookup"><span data-stu-id="a3a86-422">Specifies the identity info of a [sparse MSIX package](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) for the current application.</span></span> <span data-ttu-id="a3a86-423">Esse elemento tem suporte no Windows 10, versão 2004 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="a3a86-423">This element is supported in Windows 10, version 2004, and later versions.</span></span>

<span data-ttu-id="a3a86-424">O elemento **msix** deve estar no namespace `urn:schemas-microsoft-com:msix.v1` .</span><span class="sxs-lookup"><span data-stu-id="a3a86-424">The **msix** element must be in the namespace `urn:schemas-microsoft-com:msix.v1`.</span></span> <span data-ttu-id="a3a86-425">Ele tem os atributos mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a3a86-425">It has the attributes shown in the following table.</span></span>

| <span data-ttu-id="a3a86-426">Atributo</span><span class="sxs-lookup"><span data-stu-id="a3a86-426">Attribute</span></span>   | <span data-ttu-id="a3a86-427">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3a86-427">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a86-428">**programa**</span><span class="sxs-lookup"><span data-stu-id="a3a86-428">**publisher**</span></span>    | <span data-ttu-id="a3a86-429">Descreve as informações do Publicador.</span><span class="sxs-lookup"><span data-stu-id="a3a86-429">Describes the publisher information.</span></span> <span data-ttu-id="a3a86-430">Esse valor deve corresponder ao atributo **Publisher** no elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) em seu manifesto de pacote esparso.</span><span class="sxs-lookup"><span data-stu-id="a3a86-430">This value must match the **Publisher** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span> |
| <span data-ttu-id="a3a86-431">**packageName**</span><span class="sxs-lookup"><span data-stu-id="a3a86-431">**packageName**</span></span> | <span data-ttu-id="a3a86-432">Descreve o conteúdo do pacote.</span><span class="sxs-lookup"><span data-stu-id="a3a86-432">Describes the contents of the package.</span></span> <span data-ttu-id="a3a86-433">Esse valor deve corresponder ao atributo **Name** no elemento [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) em seu manifesto de pacote esparso.</span><span class="sxs-lookup"><span data-stu-id="a3a86-433">This value must match the **Name** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span>    |
| <span data-ttu-id="a3a86-434">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="a3a86-434">**applicationId**</span></span>    | <span data-ttu-id="a3a86-435">O identificador exclusivo do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3a86-435">The unique identifier of the application.</span></span> <span data-ttu-id="a3a86-436">Esse valor deve corresponder ao atributo **ID** no elemento [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) em seu manifesto de pacote esparso.</span><span class="sxs-lookup"><span data-stu-id="a3a86-436">This value must match the **Id** attribute in the [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) element in your sparse package manifest.</span></span>  |

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

### <a name="heaptype"></a><span data-ttu-id="a3a86-437">heaptype</span><span class="sxs-lookup"><span data-stu-id="a3a86-437">heapType</span></span>

<span data-ttu-id="a3a86-438">Substitui a implementação de heap padrão para as [APIs de heap do Win32](../Memory/heap-functions.md) a serem usadas.</span><span class="sxs-lookup"><span data-stu-id="a3a86-438">Overrides the default heap implementation for the [Win32 heap APIs](../Memory/heap-functions.md) to use.</span></span>

* <span data-ttu-id="a3a86-439">O valor **SegmentHeap** indica que o heap de segmento será usado.</span><span class="sxs-lookup"><span data-stu-id="a3a86-439">The value **SegmentHeap** indicates that segment heap will be used.</span></span> <span data-ttu-id="a3a86-440">O heap de segmento é uma implementação de heap moderna que geralmente reduzirá o uso geral da memória.</span><span class="sxs-lookup"><span data-stu-id="a3a86-440">Segment heap is a modern heap implementation that will generally reduce your overall memory usage.</span></span> <span data-ttu-id="a3a86-441">Esse elemento tem suporte no Windows 10, versão 2004 (Build 19041) e posterior.</span><span class="sxs-lookup"><span data-stu-id="a3a86-441">This element is supported in Windows 10, version 2004 (build 19041) and later.</span></span>
* <span data-ttu-id="a3a86-442">Todos os outros valores são ignorados.</span><span class="sxs-lookup"><span data-stu-id="a3a86-442">All other values are ignored.</span></span>

<span data-ttu-id="a3a86-443">Esse elemento não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="a3a86-443">This element has no attributes.</span></span>

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

## <a name="example"></a><span data-ttu-id="a3a86-444">Exemplo</span><span class="sxs-lookup"><span data-stu-id="a3a86-444">Example</span></span>

<span data-ttu-id="a3a86-445">Veja a seguir um exemplo de um manifesto de aplicativo para um aplicativo chamado MySampleApp.exe.</span><span class="sxs-lookup"><span data-stu-id="a3a86-445">The following is an example of an application manifest for an application named MySampleApp.exe.</span></span> <span data-ttu-id="a3a86-446">O aplicativo consome o assembly lado a lado do SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="a3a86-446">The application consumes the SampleAssembly side-by-side assembly.</span></span>

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
