---
description: Um arquivo de configuração do Publicador é um arquivo XML que redireciona globalmente os aplicativos e assemblies do usando uma versão de um assembly lado a lado para outra versão do mesmo assembly.
ms.assetid: b10752af-80a7-4027-b525-90333d0d010a
title: Arquivos de configuração do Publicador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc5d7d7b7ffdad3d1179a7f8c66a347d91e0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829774"
---
# <a name="publisher-configuration-files"></a><span data-ttu-id="b1d16-103">Arquivos de configuração do Publicador</span><span class="sxs-lookup"><span data-stu-id="b1d16-103">Publisher Configuration Files</span></span>

<span data-ttu-id="b1d16-104">Um arquivo de configuração do Publicador é um arquivo XML que redireciona globalmente os aplicativos e assemblies do usando uma versão de um assembly lado a lado para outra versão do mesmo assembly.</span><span class="sxs-lookup"><span data-stu-id="b1d16-104">A publisher configuration file is an XML file that globally redirects applications and assemblies from using one version of a side-by-side assembly to another version of the same assembly.</span></span> <span data-ttu-id="b1d16-105">Normalmente, o editor do assembly emite uma correção de atualização ou de segurança compatível por assembly, emitindo um arquivo de configuração de editor para ser instalado junto com uma atualização de service pack.</span><span class="sxs-lookup"><span data-stu-id="b1d16-105">Typically, the publisher of the assembly issues a compatible update or security fix on a per-assembly basis by issuing a publisher configuration file to be installed along with a service pack update.</span></span> <span data-ttu-id="b1d16-106">Isso é conhecido como [configuração do Publicador](publisher-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="b1d16-106">This is referred to as [publisher configuration](publisher-configuration.md).</span></span> <span data-ttu-id="b1d16-107">Para obter mais informações sobre esse tipo de [configuração](configuration.md) , consulte configuração do editor.</span><span class="sxs-lookup"><span data-stu-id="b1d16-107">For more information about this type of [configuration](configuration.md) see Publisher Configuration.</span></span>

<span data-ttu-id="b1d16-108">Os arquivos de configuração do Publicador têm os seguintes elementos e atributos.</span><span class="sxs-lookup"><span data-stu-id="b1d16-108">Publisher configuration files have the following elements and attributes.</span></span> <span data-ttu-id="b1d16-109">Para obter uma lista completa do esquema XML, consulte [esquema do arquivo de configuração do Publicador](publisher-configuration-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="b1d16-109">For a complete listing of the XML schema, see [Publisher Configuration File Schema](publisher-configuration-file-schema.md).</span></span>



| <span data-ttu-id="b1d16-110">Elemento</span><span class="sxs-lookup"><span data-stu-id="b1d16-110">Element</span></span>               | <span data-ttu-id="b1d16-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="b1d16-111">Attributes</span></span>                | <span data-ttu-id="b1d16-112">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b1d16-112">Required</span></span> |
|-----------------------|---------------------------|----------|
| <span data-ttu-id="b1d16-113">**)**</span><span class="sxs-lookup"><span data-stu-id="b1d16-113">**assembly**</span></span>          |                           | <span data-ttu-id="b1d16-114">Yes</span><span class="sxs-lookup"><span data-stu-id="b1d16-114">Yes</span></span>      |
|                       | <span data-ttu-id="b1d16-115">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="b1d16-115">**manifestVersion**</span></span>       | <span data-ttu-id="b1d16-116">Yes</span><span class="sxs-lookup"><span data-stu-id="b1d16-116">Yes</span></span>      |
| <span data-ttu-id="b1d16-117">**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="b1d16-117">**assemblyIdentity**</span></span>  |                           | <span data-ttu-id="b1d16-118">Yes</span><span class="sxs-lookup"><span data-stu-id="b1d16-118">Yes</span></span>      |
|                       | <span data-ttu-id="b1d16-119">**tipo**</span><span class="sxs-lookup"><span data-stu-id="b1d16-119">**type**</span></span>                  | <span data-ttu-id="b1d16-120">Sim</span><span class="sxs-lookup"><span data-stu-id="b1d16-120">Yes</span></span>      |
|                       | <span data-ttu-id="b1d16-121">**name**</span><span class="sxs-lookup"><span data-stu-id="b1d16-121">**name**</span></span>                  | <span data-ttu-id="b1d16-122">Sim</span><span class="sxs-lookup"><span data-stu-id="b1d16-122">Yes</span></span>      |
|                       | <span data-ttu-id="b1d16-123">**linguagem**</span><span class="sxs-lookup"><span data-stu-id="b1d16-123">**language**</span></span>              | <span data-ttu-id="b1d16-124">No</span><span class="sxs-lookup"><span data-stu-id="b1d16-124">No</span></span>       |
|                       | <span data-ttu-id="b1d16-125">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="b1d16-125">**processorArchitecture**</span></span> | <span data-ttu-id="b1d16-126">No</span><span class="sxs-lookup"><span data-stu-id="b1d16-126">No</span></span>       |
|                       | <span data-ttu-id="b1d16-127">**version**</span><span class="sxs-lookup"><span data-stu-id="b1d16-127">**version**</span></span>               | <span data-ttu-id="b1d16-128">Yes</span><span class="sxs-lookup"><span data-stu-id="b1d16-128">Yes</span></span>      |
|                       | <span data-ttu-id="b1d16-129">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="b1d16-129">**publicKeyToken**</span></span>        | <span data-ttu-id="b1d16-130">No</span><span class="sxs-lookup"><span data-stu-id="b1d16-130">No</span></span>       |
| <span data-ttu-id="b1d16-131">**Estados**</span><span class="sxs-lookup"><span data-stu-id="b1d16-131">**dependency**</span></span>        |                           | <span data-ttu-id="b1d16-132">No</span><span class="sxs-lookup"><span data-stu-id="b1d16-132">No</span></span>       |
| <span data-ttu-id="b1d16-133">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="b1d16-133">**dependentAssembly**</span></span> |                           | <span data-ttu-id="b1d16-134">No</span><span class="sxs-lookup"><span data-stu-id="b1d16-134">No</span></span>       |
| <span data-ttu-id="b1d16-135">**bindingRedirect**</span><span class="sxs-lookup"><span data-stu-id="b1d16-135">**bindingRedirect**</span></span>   |                           | <span data-ttu-id="b1d16-136">Yes</span><span class="sxs-lookup"><span data-stu-id="b1d16-136">Yes</span></span>      |
|                       | <span data-ttu-id="b1d16-137">**oldVersion**</span><span class="sxs-lookup"><span data-stu-id="b1d16-137">**oldVersion**</span></span>            | <span data-ttu-id="b1d16-138">Yes</span><span class="sxs-lookup"><span data-stu-id="b1d16-138">Yes</span></span>      |
|                       | <span data-ttu-id="b1d16-139">**newVersion**</span><span class="sxs-lookup"><span data-stu-id="b1d16-139">**newVersion**</span></span>            | <span data-ttu-id="b1d16-140">Yes</span><span class="sxs-lookup"><span data-stu-id="b1d16-140">Yes</span></span>      |



 

## <a name="file-location"></a><span data-ttu-id="b1d16-141">Local do arquivo</span><span class="sxs-lookup"><span data-stu-id="b1d16-141">File Location</span></span>

<span data-ttu-id="b1d16-142">Os arquivos de configuração do Publicador devem ser instalados na pasta WinSxS.</span><span class="sxs-lookup"><span data-stu-id="b1d16-142">Publisher configuration files must be installed in the WinSxS folder.</span></span> <span data-ttu-id="b1d16-143">Normalmente, eles são instalados como um arquivo separado, mas os arquivos de configuração do Publicador também podem ser incluídos como um recurso em uma DLL.</span><span class="sxs-lookup"><span data-stu-id="b1d16-143">They are commonly installed as a separate file but publisher configuration files can also be included as a resource in a DLL.</span></span> <span data-ttu-id="b1d16-144">Um arquivo de configuração do Publicador não pode ser incluído como um recurso em um arquivo EXE.</span><span class="sxs-lookup"><span data-stu-id="b1d16-144">A publisher configuration file cannot be included as a resource in an EXE file.</span></span> <span data-ttu-id="b1d16-145">Um arquivo EXE pode incluir um [manifesto do aplicativo](application-manifests.md) como um recurso.</span><span class="sxs-lookup"><span data-stu-id="b1d16-145">An EXE file may include an [application manifest](application-manifests.md) as a resource.</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="b1d16-146">Sintaxe de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="b1d16-146">File Name Syntax</span></span>

<span data-ttu-id="b1d16-147">O nome de arquivo de um arquivo de configuração do Publicador tem a *política* de formulário. *principal*. *secundária*. *AssemblyName* onde *Major* e *Minor* referem-se às partes principais e secundárias da [versão do assembly](assembly-versions.md) que está sendo afetada.</span><span class="sxs-lookup"><span data-stu-id="b1d16-147">The file name of a publisher configuration file has the form *policy*.*major*.*minor*.*assemblyname* where *major* and *minor* refer to the major and minor parts of the [assembly version](assembly-versions.md) that is being affected.</span></span> <span data-ttu-id="b1d16-148">O *AssemblyName* refere-se ao nome do assembly.</span><span class="sxs-lookup"><span data-stu-id="b1d16-148">The *assemblyname* refers to the name of the assembly.</span></span>

<span data-ttu-id="b1d16-149">Por exemplo, um arquivo de configuração de Publicador para a versão 6,0 do assembly Microsoft. Windows. Common-Controls teria o seguinte nome:</span><span class="sxs-lookup"><span data-stu-id="b1d16-149">For example, a publisher configuration file for version 6.0 of the Microsoft.Windows.Common-Controls assembly would have the following name:</span></span>

<dl> <span data-ttu-id="b1d16-150">Policy. 6.0. Microsoft. Windows. Common – Controls</span><span class="sxs-lookup"><span data-stu-id="b1d16-150">policy.6.0.Microsoft.Windows.Common-Controls</span></span>  
</dl>

<span data-ttu-id="b1d16-151">Não use arquivos de configuração de política para incrementar a versão principal ou secundária de um assembly.</span><span class="sxs-lookup"><span data-stu-id="b1d16-151">Do not use policy configuration files to increment the major or minor version of an assembly.</span></span> <span data-ttu-id="b1d16-152">Por exemplo, não redirecione a versão 6.0.0.0 para 7.0.0.0 ou 6.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="b1d16-152">For example, do not redirect version 6.0.0.0 to 7.0.0.0 or 6.1.0.0.</span></span> <span data-ttu-id="b1d16-153">Quando um aplicativo faz referência a uma versão de assembly, como 6.0.0.0, o lado a lado verifica a presença de quaisquer arquivos de configuração de política com as versões primárias e secundárias especificadas, por exemplo, 6,0.</span><span class="sxs-lookup"><span data-stu-id="b1d16-153">When an application references an assembly version, such as 6.0.0.0, side-by-side checks for the presence of any policy configuration files with the specified major and minor versions, e.g. 6.0.</span></span> <span data-ttu-id="b1d16-154">O aplicativo é então Redirecionado para outra versão do assembly, por exemplo, 6.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="b1d16-154">The application is then redirected to another version of the assembly, for example 6.0.1.0.</span></span> <span data-ttu-id="b1d16-155">Se um arquivo de configuração do Publicador incrementar a versão principal ou secundária de um assembly, o redirecionamento subsequente do assembly poderá exigir a emissão de vários arquivos de configuração de política.</span><span class="sxs-lookup"><span data-stu-id="b1d16-155">If a publisher configuration file increments the major or minor version of an assembly, subsequent redirection of the assembly may require issuing multiple policy configuration files.</span></span>

## <a name="elements"></a><span data-ttu-id="b1d16-156">Elementos</span><span class="sxs-lookup"><span data-stu-id="b1d16-156">Elements</span></span>

<dl> <dt>

<span data-ttu-id="b1d16-157"><span id="assembly"></span><span id="ASSEMBLY"></span>**)**</span><span class="sxs-lookup"><span data-stu-id="b1d16-157"><span id="assembly"></span><span id="ASSEMBLY"></span>**assembly**</span></span>
</dt> <dd>

<span data-ttu-id="b1d16-158">Um elemento de contêiner.</span><span class="sxs-lookup"><span data-stu-id="b1d16-158">A container element.</span></span> <span data-ttu-id="b1d16-159">Seu primeiro subelemento deve ser um **AssemblyIdentity**.</span><span class="sxs-lookup"><span data-stu-id="b1d16-159">Its first subelement must be an **assemblyIdentity**.</span></span> <span data-ttu-id="b1d16-160">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="b1d16-160">Required.</span></span>

<span data-ttu-id="b1d16-161">O elemento assembly deve estar no namespace **urn: schemas-microsoft-com: asm. v1**.</span><span class="sxs-lookup"><span data-stu-id="b1d16-161">The assembly element must be in the namespace **urn:schemas-microsoft-com:asm.v1**.</span></span> <span data-ttu-id="b1d16-162">Os elementos filho do assembly também devem estar nesse namespace, por herança ou por marcação.</span><span class="sxs-lookup"><span data-stu-id="b1d16-162">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="b1d16-163">O elemento **assembly** tem os atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1d16-163">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="b1d16-164">Atributo</span><span class="sxs-lookup"><span data-stu-id="b1d16-164">Attribute</span></span>           | <span data-ttu-id="b1d16-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1d16-165">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="b1d16-166">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="b1d16-166">**manifestVersion**</span></span> | <span data-ttu-id="b1d16-167">O atributo **manifestVersion** deve ser definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="b1d16-167">The **manifestVersion** attribute must be set to 1.0.</span></span> |



 

</dd> <dt>

<span data-ttu-id="b1d16-168"><span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="b1d16-168"><span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>**assemblyIdentity**</span></span>
</dt> <dd>

<span data-ttu-id="b1d16-169">Descreve e identifica exclusivamente um assembly lado a lado.</span><span class="sxs-lookup"><span data-stu-id="b1d16-169">Describes and uniquely identifies a side-by-side assembly.</span></span>

<span data-ttu-id="b1d16-170">Como o primeiro subelemento de um elemento de **assembly** , o **AssemblyIdentity** descreve o assembly lado a lado que está tendo uma ou mais de suas dependências de assembly alteradas.</span><span class="sxs-lookup"><span data-stu-id="b1d16-170">As the first subelement of an **assembly** element, the **assemblyIdentity** describes the side-by-side assembly that is having one or more of its assembly dependencies changed.</span></span> <span data-ttu-id="b1d16-171">O arquivo de configuração do Publicador redireciona as dependências do assembly identificado.</span><span class="sxs-lookup"><span data-stu-id="b1d16-171">The publisher configuration file redirects the dependencies of the assembly identified.</span></span> <span data-ttu-id="b1d16-172">Por exemplo, o **AssemblyIdentity** a seguir indica que o arquivo de configuração do Publicador afeta as dependências do assembly x86 Microsoft. Windows. pop 6.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="b1d16-172">For example, the following **assemblyIdentity** indicates that the publisher configuration file affects the dependencies of the x86 Microsoft.Windows.Pop 6.0.0.0 assembly.</span></span>

``` syntax
<assemblyIdentity 
     type="win32-policy" 
     publicKeyToken="0000000000000000" 
     name="policy.6.0.Microsoft.Windows.Pop" 
     version="2.1.0.0" 
     processorArchitecture="x86"/>
```

<span data-ttu-id="b1d16-173">Como o primeiro subelemento de um elemento **dependentAssembly** , **AssemblyIdentity** descreve uma dependência de assembly lado a lado.</span><span class="sxs-lookup"><span data-stu-id="b1d16-173">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly dependency.</span></span> <span data-ttu-id="b1d16-174">O arquivo de configuração do Publicador reconfigura a identidade desse assembly lado a lado necessário.</span><span class="sxs-lookup"><span data-stu-id="b1d16-174">The publisher configuration file reconfigures the identity of this required side-by-side assembly.</span></span> <span data-ttu-id="b1d16-175">A alteração é especificada em um **bindingRedirect**.</span><span class="sxs-lookup"><span data-stu-id="b1d16-175">The change is specified in a **bindingRedirect**.</span></span> <span data-ttu-id="b1d16-176">Por exemplo, o **AssemblyIdentity** a seguir altera qualquer dependência em Microsoft. Windows. SampleAssembly versão 2.0.0.0 para uma dependência em Microsoft. Windows. SampleAssembly versão 2.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="b1d16-176">For example, the following **assemblyIdentity** changes any dependency on Microsoft.Windows.SampleAssembly version 2.0.0.0 to a dependency on Microsoft.Windows.SampleAssembly version 2.0.1.0.</span></span>

``` syntax
<dependency>
      <dependentAssembly>
         <assemblyIdentity 
type="win32" 
name="Microsoft.Windows.SampleAssembly"  
processorArchitecture="x86"
publicKeyToken="0000000000000000"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
</dependency>
```

<span data-ttu-id="b1d16-177">O elemento **AssemblyIdentity** tem os atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1d16-177">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="b1d16-178">Ele não tem subelementos.</span><span class="sxs-lookup"><span data-stu-id="b1d16-178">It has no sub-elements.</span></span>



| <span data-ttu-id="b1d16-179">Atributo</span><span class="sxs-lookup"><span data-stu-id="b1d16-179">Attribute</span></span>                 | <span data-ttu-id="b1d16-180">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1d16-180">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d16-181">**tipo**</span><span class="sxs-lookup"><span data-stu-id="b1d16-181">**type**</span></span>                  | <span data-ttu-id="b1d16-182">Especifica o tipo de assembly.</span><span class="sxs-lookup"><span data-stu-id="b1d16-182">Specifies the assembly type.</span></span> <span data-ttu-id="b1d16-183">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="b1d16-183">Required.</span></span> <span data-ttu-id="b1d16-184">No **AssemblyIdentity** para o assembly que está sendo afetado, o valor do atributo **Type** deve ser definido como Win32-Policy.</span><span class="sxs-lookup"><span data-stu-id="b1d16-184">In the **assemblyIdentity** for the assembly being affected, the value of the **type** attribute must be set to win32-policy.</span></span> <span data-ttu-id="b1d16-185">O valor Win32-Policy deve estar em todas as letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b1d16-185">The value win32-policy must be in all lowercase letters.</span></span><br/> <span data-ttu-id="b1d16-186">No **AssemblyIdentity** para a dependência de alteração do assembly, o valor do atributo **Type** deve ser definido como Win32.</span><span class="sxs-lookup"><span data-stu-id="b1d16-186">In the **assemblyIdentity** for the changing assembly dependency, the value of the **type** attribute must be set to win32.</span></span> <span data-ttu-id="b1d16-187">O valor Win32 deve estar em todas as letras minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b1d16-187">The value win32 must be in all lowercase letters.</span></span><br/>                                                                                                                                                                                                             |
| <span data-ttu-id="b1d16-188">**name**</span><span class="sxs-lookup"><span data-stu-id="b1d16-188">**name**</span></span>                  | <span data-ttu-id="b1d16-189">Nomeia exclusivamente um assembly.</span><span class="sxs-lookup"><span data-stu-id="b1d16-189">Uniquely names an assembly.</span></span> <span data-ttu-id="b1d16-190">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="b1d16-190">Required.</span></span> <span data-ttu-id="b1d16-191">No **AssemblyIdentity** para o assembly que está sendo afetado, Name tem a *política* de formulário. *principal*. *secundária*. *AssemblyName* em que *Major* e *Minor* se referem às partes principal e secundária da [versão do assembly](assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="b1d16-191">In the **assemblyIdentity** for the assembly being affected, name has the form *policy*.*major*.*minor*.*assemblyname* where *major* and *minor* refer to the major and minor parts of the [assembly version](assembly-versions.md).</span></span><br/> <span data-ttu-id="b1d16-192">No **AssemblyIdentity** para a dependência de alteração de assembly, Name tem o formato Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="b1d16-192">In the **assemblyIdentity** for the changing assembly dependency, name has the form Organization.Division.Name.</span></span> <span data-ttu-id="b1d16-193">Por exemplo, Microsoft. Windows. MysampleApp.</span><span class="sxs-lookup"><span data-stu-id="b1d16-193">For example, Microsoft.Windows.MysampleApp.</span></span><br/>                                                                                                                                                                                 |
| <span data-ttu-id="b1d16-194">**linguagem**</span><span class="sxs-lookup"><span data-stu-id="b1d16-194">**language**</span></span>              | <span data-ttu-id="b1d16-195">Identifica o idioma do assembly.</span><span class="sxs-lookup"><span data-stu-id="b1d16-195">Identifies the language of the assembly.</span></span> <span data-ttu-id="b1d16-196">Opcional.</span><span class="sxs-lookup"><span data-stu-id="b1d16-196">Optional.</span></span> <span data-ttu-id="b1d16-197">No **AssemblyIdentity** para o assembly que está sendo afetado, se o assembly for específico a um idioma, especifique o código de linguagem DHTML.</span><span class="sxs-lookup"><span data-stu-id="b1d16-197">In the **assemblyIdentity** for the assembly being affected, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="b1d16-198">Se o assembly for para uso mundial (neutro à linguagem), omita esse atributo.</span><span class="sxs-lookup"><span data-stu-id="b1d16-198">If the assembly is for worldwide use (language neutral), omit this attribute.</span></span><br/> <span data-ttu-id="b1d16-199">No **AssemblyIdentity** para a dependência de alteração de assembly, se o assembly for específico de idioma, especifique o código de linguagem DHTML.</span><span class="sxs-lookup"><span data-stu-id="b1d16-199">In the **assemblyIdentity** for the changing assembly dependency, if the assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="b1d16-200">Se o assembly for para uso mundial (com neutralidade de idioma), defina o valor como " \* ".</span><span class="sxs-lookup"><span data-stu-id="b1d16-200">If the assembly is for worldwide use (language neutral) set the value as "\*".</span></span><br/>                                                                                                                            |
| <span data-ttu-id="b1d16-201">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="b1d16-201">**processorArchitecture**</span></span> | <span data-ttu-id="b1d16-202">Especifica o processador que executa o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b1d16-202">Specifies the processor running the application.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="b1d16-203">**version**</span><span class="sxs-lookup"><span data-stu-id="b1d16-203">**version**</span></span>               | <span data-ttu-id="b1d16-204">Especifica a versão do assembly.</span><span class="sxs-lookup"><span data-stu-id="b1d16-204">Specifies the assembly version.</span></span> <span data-ttu-id="b1d16-205">Use a sintaxe de versão de quatro partes: mmmm. nnnn. Oooo. PPPP</span><span class="sxs-lookup"><span data-stu-id="b1d16-205">Use four-part version syntax: mmmm.nnnn.oooo.pppp</span></span> <span data-ttu-id="b1d16-206">Necessário somente no **AssemblyIdentity** de contexto def.</span><span class="sxs-lookup"><span data-stu-id="b1d16-206">Required only in the DEF-context **assemblyIdentity**.</span></span> <span data-ttu-id="b1d16-207">Não especifique o atributo Version no **AssemblyIdentity** de contexto de referência.</span><span class="sxs-lookup"><span data-stu-id="b1d16-207">Do not specify the version attribute in the REF-context **assemblyIdentity**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="b1d16-208">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="b1d16-208">**publicKeyToken**</span></span>        | <span data-ttu-id="b1d16-209">Uma cadeia de caracteres hexadecimal de 16 caracteres que representa os últimos 8 bytes do hash SHA-1 da chave pública sob a qual o assembly está assinado.</span><span class="sxs-lookup"><span data-stu-id="b1d16-209">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the assembly is signed.</span></span> <span data-ttu-id="b1d16-210">A chave pública usada para assinar o catálogo deve ter 2048 bits ou mais.</span><span class="sxs-lookup"><span data-stu-id="b1d16-210">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="b1d16-211">Um publicKeyToken é necessário para todos os assemblies compartilhados lado a lado.</span><span class="sxs-lookup"><span data-stu-id="b1d16-211">A publicKeyToken is required for all shared side-by-side assemblies.</span></span> <span data-ttu-id="b1d16-212">O publicKeyToken usado para o arquivo de configuração do Publicador deve ser a mesma chave usada para o assembly assinado.</span><span class="sxs-lookup"><span data-stu-id="b1d16-212">The publicKeyToken used for the publisher configuration file should be the same key used for the signed assembly.</span></span> <span data-ttu-id="b1d16-213">Os arquivos de configuração do Publicador podem ser assinados usando as mesmas ferramentas usadas com assemblies, consulte [exemplo de assinatura de assembly](assembly-signing-example.md) e [criando arquivos e catálogos assinados](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="b1d16-213">Publisher configuration files can be signed using the same tools as used with assemblies, see [Assembly Signing Example](assembly-signing-example.md) and [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span> |



 

</dd> <dt>

<span data-ttu-id="b1d16-214"><span id="dependency"></span><span id="DEPENDENCY"></span>**Estados**</span><span class="sxs-lookup"><span data-stu-id="b1d16-214"><span id="dependency"></span><span id="DEPENDENCY"></span>**dependency**</span></span>
</dt> <dd>

<span data-ttu-id="b1d16-215">Um elemento de contêiner opcional para pelo menos um **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="b1d16-215">An optional container element for at least one **dependentAssembly**.</span></span> <span data-ttu-id="b1d16-216">Ele não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="b1d16-216">It has no attributes.</span></span>

</dd> <dt>

<span data-ttu-id="b1d16-217"><span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="b1d16-217"><span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>**dependentAssembly**</span></span>
</dt> <dd>

<span data-ttu-id="b1d16-218">Cada **dependentAssembly** deve estar dentro de exatamente uma **dependência**.</span><span class="sxs-lookup"><span data-stu-id="b1d16-218">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="b1d16-219">Um **dependentAssembly** não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="b1d16-219">A **dependentAssembly** has no attributes.</span></span> <span data-ttu-id="b1d16-220">O primeiro subelemento de **dependentAssembly** deve ser um **AssemblyIdentity** para o assembly lado a lado que está sendo reconfigurado pela configuração do Publicador.</span><span class="sxs-lookup"><span data-stu-id="b1d16-220">The first subelement of **dependentAssembly** must be an **assemblyIdentity** for the side-by-side assembly being reconfigured by the publisher configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b1d16-221"><span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**</span><span class="sxs-lookup"><span data-stu-id="b1d16-221"><span id="bindingRedirect"></span><span id="bindingredirect"></span><span id="BINDINGREDIRECT"></span>**bindingRedirect**</span></span>
</dt> <dd>

<span data-ttu-id="b1d16-222">O elemento **bindingRedirect** contém informações de redirecionamento para a associação do assembly.</span><span class="sxs-lookup"><span data-stu-id="b1d16-222">The **bindingRedirect** element contains redirection information for the binding of the assembly.</span></span>

<span data-ttu-id="b1d16-223">Esse elemento tem os atributos mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b1d16-223">This element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="b1d16-224">Atributo</span><span class="sxs-lookup"><span data-stu-id="b1d16-224">Attribute</span></span>      | <span data-ttu-id="b1d16-225">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1d16-225">Description</span></span>                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d16-226">**oldVersion**</span><span class="sxs-lookup"><span data-stu-id="b1d16-226">**oldVersion**</span></span> | <span data-ttu-id="b1d16-227">Especifica a versão do assembly que está sendo substituída e redirecionada.</span><span class="sxs-lookup"><span data-stu-id="b1d16-227">Specifies the assembly version being overridden and redirected.</span></span> <span data-ttu-id="b1d16-228">Use a sintaxe de versão de quatro partes nnnnn. NNNNN. NNNNN. NNNNN.</span><span class="sxs-lookup"><span data-stu-id="b1d16-228">Use the four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span> <span data-ttu-id="b1d16-229">Especifique um intervalo de versões por um traço sem espaços.</span><span class="sxs-lookup"><span data-stu-id="b1d16-229">Specify a range of versions by a dash with no spaces.</span></span> <span data-ttu-id="b1d16-230">Por exemplo, 2.14.3.0 ou 2.14.3.0 2.16.0.0.</span><span class="sxs-lookup"><span data-stu-id="b1d16-230">For example, 2.14.3.0 or 2.14.3.0 2.16.0.0.</span></span> <span data-ttu-id="b1d16-231">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="b1d16-231">Required.</span></span> |
| <span data-ttu-id="b1d16-232">**newVersion**</span><span class="sxs-lookup"><span data-stu-id="b1d16-232">**newVersion**</span></span> | <span data-ttu-id="b1d16-233">Especifica a versão do assembly de substituição.</span><span class="sxs-lookup"><span data-stu-id="b1d16-233">Specifies the replacement assembly version.</span></span> <span data-ttu-id="b1d16-234">Use a sintaxe de versão de quatro partes nnnnn. NNNNN. NNNNN. NNNNN.</span><span class="sxs-lookup"><span data-stu-id="b1d16-234">Use four-part version syntax nnnnn.nnnnn.nnnnn.nnnnn.</span></span>                                                                                                                                     |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1d16-235">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1d16-235">Remarks</span></span>

<span data-ttu-id="b1d16-236">Os arquivos de configuração do Publicador não especificam arquivos.</span><span class="sxs-lookup"><span data-stu-id="b1d16-236">Publisher configuration files do not specify files.</span></span> <span data-ttu-id="b1d16-237">Observe que os arquivos de política específicos do idioma são separados do arquivo de configuração do Publicador.</span><span class="sxs-lookup"><span data-stu-id="b1d16-237">Note that language-specific policy files are separate from the publisher configuration file.</span></span>

## <a name="example"></a><span data-ttu-id="b1d16-238">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b1d16-238">Example</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.6.0.Proseware.Research.SampleAssembly" version="1.0.1.0" language="en-us" processorArchitecture="x86"/>
<dependency>
<dependentAssembly>
<assemblyIdentity type="win32" publicKeyToken="0000000000000000" name="Proseware.Research.SampleAssembly" language="en-us" processorArchitecture="x86"/>
<bindingRedirect oldVersion="1.0.0.0" newVersion="1.0.1.0"/>
</dependentAssembly>
</dependency>
</assembly>
```

 

 




