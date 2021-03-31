---
description: Se você quiser que os usuários do seu aplicativo, ou a DLL principal, sejam capazes de alterar o idioma da interface do usuário, considere colocar recursos de idioma em DLLs de recurso satélite separadas.
ms.assetid: fcadd7e8-cab8-43cb-9c67-af8ebe0e3a5b
title: Usando assemblies com uma interface de usuário multilíngüe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f501f40715dc2335f02c044aa48ada9741411d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647011"
---
# <a name="using-assemblies-with-a-multilanguage-user-interface"></a><span data-ttu-id="b4b69-103">Usando assemblies com uma interface de usuário multilíngüe</span><span class="sxs-lookup"><span data-stu-id="b4b69-103">Using Assemblies with a Multilanguage User Interface</span></span>

<span data-ttu-id="b4b69-104">Se você quiser que os usuários do seu aplicativo, ou a DLL principal, sejam capazes de alterar o idioma da interface do usuário, considere colocar recursos de idioma em DLLs de recurso satélite separadas.</span><span class="sxs-lookup"><span data-stu-id="b4b69-104">If you want users of your application, or core DLL, to be capable of changing the language of the user interface, you should consider placing language resources into separate satellite resource DLLs.</span></span> <span data-ttu-id="b4b69-105">Para obter mais informações sobre como usar DLLs de recursos de satélite, consulte [Multilingual User interface (MUI)](/windows/desktop/Intl/multilingual-user-interface).</span><span class="sxs-lookup"><span data-stu-id="b4b69-105">For more information about using satellite resource DLLs, see [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface).</span></span>

<span data-ttu-id="b4b69-106">Cada DLL satélite contém os recursos para um idioma diferente.</span><span class="sxs-lookup"><span data-stu-id="b4b69-106">Each satellite DLL contains the resources for a different language.</span></span> <span data-ttu-id="b4b69-107">A DLL principal pode ser fornecida como um assembly e cada uma das DLLs satélite pode ser fornecida como assemblies satélites separados.</span><span class="sxs-lookup"><span data-stu-id="b4b69-107">The core DLL may be provided as an assembly and each of the satellite DLLs may be provided as separate satellite assemblies.</span></span> <span data-ttu-id="b4b69-108">Nesse caso, cada assembly satélite deve ter seu próprio manifesto de assembly autodescritivo.</span><span class="sxs-lookup"><span data-stu-id="b4b69-108">In this case, each satellite assembly should have its own self-describing assembly manifest.</span></span> <span data-ttu-id="b4b69-109">O manifesto do assembly satélite não deve descrever nenhuma dependência em outros assemblies.</span><span class="sxs-lookup"><span data-stu-id="b4b69-109">The satellite assembly's manifest should not describe any dependency on other assemblies.</span></span> <span data-ttu-id="b4b69-110">Qualquer dependência de assemblies satélite em outros assemblies deve ser descrita no manifesto do assembly principal.</span><span class="sxs-lookup"><span data-stu-id="b4b69-110">Any dependency of satellite assemblies on other assemblies should instead be described in the core assembly's manifest.</span></span>

<span data-ttu-id="b4b69-111">A versão [MUI (interface do usuário multilíngüe)](/windows/desktop/Intl/multilingual-user-interface) do Windows permite que os usuários especifiquem o idioma da interface do usuário de acordo com suas preferências, desde que o idioma necessário tenha sido adicionado ao sistema.</span><span class="sxs-lookup"><span data-stu-id="b4b69-111">The [Multilanguage User Interface (MUI)](/windows/desktop/Intl/multilingual-user-interface) version of Windows enables users to specify the user-interface language according to their preferences, provided the required language has been added to the system.</span></span> <span data-ttu-id="b4b69-112">Um assembly principal pode dar suporte a vários idiomas usando vários assemblies MUI.</span><span class="sxs-lookup"><span data-stu-id="b4b69-112">A core assembly can support multiple languages by using multiple MUI assemblies.</span></span> <span data-ttu-id="b4b69-113">Nesse caso, cada assembly MUI deve ter seu próprio manifesto e qualquer dependência em relação a outros assemblies deve ser descrita apenas no manifesto do assembly principal.</span><span class="sxs-lookup"><span data-stu-id="b4b69-113">In this case, each MUI assembly should have its own manifest and any dependencies on other assemblies should only be described in the core assembly's manifest.</span></span>

<span data-ttu-id="b4b69-114">Por exemplo, o proseware. Sample. pop pode ser um assembly lado a lado principal, que é dependente do assembly proseware. Research. SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="b4b69-114">For example, Proseware.Sample.Pop may be a core side-by-side assembly which happens to be dependent on the Proseware.Research.SampleAssembly assembly.</span></span> <span data-ttu-id="b4b69-115">Se o proseware. Sample. pop usar o MUI para dar suporte a vários idiomas, poderão ser fornecidos assemblies de MUI separados para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="b4b69-115">If Proseware.Sample.Pop uses MUI to support multiple languages, separate MUI assemblies can be provided for each language.</span></span> <span data-ttu-id="b4b69-116">Cada assembly do MUI deve ter seu próprio manifesto descrevendo essa DLL de recurso satélite específica.</span><span class="sxs-lookup"><span data-stu-id="b4b69-116">Each MUI assembly should have its own manifest describing this particular satellite resource DLL.</span></span> <span data-ttu-id="b4b69-117">Os manifestos do assembly MUI não devem incluir nenhuma referência a dependências em outros assemblies.</span><span class="sxs-lookup"><span data-stu-id="b4b69-117">The MUI assembly manifests should not include any reference to dependencies on other assemblies.</span></span> <span data-ttu-id="b4b69-118">O manifesto que descreve o assembly principal, proseware. Sample. pop, deve descrever a dependência de Proseware. Sample. pop no assembly proseware. Research. SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="b4b69-118">The manifest describing the core assembly, Proseware.Sample.Pop, should describe the dependency of Proseware.Sample.Pop on the Proseware.Research.SampleAssembly assembly.</span></span>

<span data-ttu-id="b4b69-119">Os atributos do elemento **AssemblyIdentity** de um assembly satélite são semelhantes àqueles no manifesto do assembly de base.</span><span class="sxs-lookup"><span data-stu-id="b4b69-119">The attributes of the **assemblyIdentity** element of a satellite assembly are similar to those in the manifest of the base assembly.</span></span> <span data-ttu-id="b4b69-120">O atributo **Name** deve ser o mesmo que o assembly base com a adição de "Resources".</span><span class="sxs-lookup"><span data-stu-id="b4b69-120">The **name** attribute should be the same as the base assembly with the addition of "Resources."</span></span> <span data-ttu-id="b4b69-121">Por exemplo, se o nome for "proseware. Tools. Verification. Runtime-Libraries" no assembly base, o nome no assembly de recursos seria "proseware. Tools. Verification. Runtime-Libraries. resources".</span><span class="sxs-lookup"><span data-stu-id="b4b69-121">For example, if the name is "Proseware.Tools.SpellCheck.Runtime-Libraries" in the base assembly, the name in the resource assembly would be "Proseware.Tools.SpellCheck.Runtime-Libraries.Resources."</span></span> <span data-ttu-id="b4b69-122">O atributo **Language** deve identificar o idioma do assembly de recursos.</span><span class="sxs-lookup"><span data-stu-id="b4b69-122">The **language** attribute should identify the language of the resource assembly.</span></span> <span data-ttu-id="b4b69-123">O atributo de **arquivo** deve incluir a lista de arquivos que são DLLs de recurso.</span><span class="sxs-lookup"><span data-stu-id="b4b69-123">The **file** attribute should include the list of files that are resource DLLs.</span></span>

<span data-ttu-id="b4b69-124">Veja a seguir um exemplo do manifesto para o assembly de recursos do proseware. Tools. Verification. Runtime-Libraries.</span><span class="sxs-lookup"><span data-stu-id="b4b69-124">The following is an example of the manifest for Proseware.Tools.SpellCheck.Runtime-Libraries resources assembly.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        type="win32"
        name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources"
        version="6.0.0.0"
        processorArchitecture="X86"
        language="DE"
        publicKeyToken="0000000000000000"
    />
    <file name="sample.dll"/>
</assembly>
```

<span data-ttu-id="b4b69-125">O assembly base descreve uma dependência opcional no assembly de recurso.</span><span class="sxs-lookup"><span data-stu-id="b4b69-125">The base assembly describes an optional dependency on the resource assembly.</span></span> <span data-ttu-id="b4b69-126">Neste exemplo, se um usuário estiver executando o Windows com a localidade designada como alemão, um aplicativo que usa o assembly proseware. Tools. verificador ortográfico exibiria texto em alemão.</span><span class="sxs-lookup"><span data-stu-id="b4b69-126">In this example, if a user is running Windows with the locale designated as German, an application using the Proseware.Tools.SpellCheck assembly would display text in German.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32" 
    name="Proseware.Tools.SpellCheck.Runtime-Libraries"
    version="6.0.0.0" processorArchitecture="x86"
    publicKeyToken="0000000000000000"/>
    <dependency optional="yes">
        <dependentAssembly>
            <assemblyIdentity type="win32" 
                              name="Proseware.Tools.SpellCheck.Runtime-Libraries.Resources" 
                              version="6.0.0.0" 
                              processorArchitecture="x86" 
                              publicKeyToken="0000000000000000" 
                              language="*"
            />
        </dependentAssembly>
    </dependency>
```

 

 
