---
description: No Windows Server 2003, o WinHTTP é implementado como um assembly lado a lado e deve ser vinculado a tal como tal. Observe que isso não se aplica ao Windows Vista e posterior.
ms.assetid: 524d926d-4d8a-4576-96fd-c533517ba28e
title: Usando o WinHTTP como um assembly lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a74a0e5cf842fdd1e20c6d6d271de482e361c4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647152"
---
# <a name="using-winhttp-as-a-side-by-side-assembly"></a><span data-ttu-id="c7eab-104">Usando o WinHTTP como um assembly lado a lado</span><span class="sxs-lookup"><span data-stu-id="c7eab-104">Using WinHTTP as a Side-by-side Assembly</span></span>

<span data-ttu-id="c7eab-105">No Windows Server 2003, o WinHTTP é implementado como um assembly lado a lado e deve ser vinculado a tal como tal.</span><span class="sxs-lookup"><span data-stu-id="c7eab-105">On Windows Server 2003, WinHTTP is implemented as a side-by-side assembly, and must be linked to as such.</span></span> <span data-ttu-id="c7eab-106">Observe que isso não se aplica ao Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="c7eab-106">Note that this does not apply to Windows Vista and later.</span></span>

## <a name="side-by-side-assemblies"></a><span data-ttu-id="c7eab-107">Assemblies lado a lado</span><span class="sxs-lookup"><span data-stu-id="c7eab-107">Side-by-side Assemblies</span></span>

<span data-ttu-id="c7eab-108">A partir do Microsoft Windows XP, um mecanismo de assemblies lado a lado foi fornecido para controlar a vinculação de tempo de execução para evitar conflitos de controle de versão da DLL (biblioteca de vínculos dinâmicos).</span><span class="sxs-lookup"><span data-stu-id="c7eab-108">Starting with Microsoft Windows XP, a side-by-side assemblies mechanism was provided to control run-time linking to avoid dynamic-link-library (DLL) versioning conflicts.</span></span> <span data-ttu-id="c7eab-109">Para obter informações sobre assemblies lado a lado, consulte [sobre aplicativos isolados e assemblies](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies)lado a lado.</span><span class="sxs-lookup"><span data-stu-id="c7eab-109">For information about side-by-side assemblies, see [About Isolated Applications and Side-by-side Assemblies](/windows/desktop/SbsCs/about-isolated-applications-and-side-by-side-assemblies).</span></span>

<span data-ttu-id="c7eab-110">Para usar esse mecanismo para vincular o WinHTTP versão 5,1 no Windows Server 2003, um aplicativo deve incorporar um manifesto que especifica o WinHTTP como um assembly dependente.</span><span class="sxs-lookup"><span data-stu-id="c7eab-110">To use this mechanism to link to WinHTTP version 5.1 on Windows Server 2003, an application must incorporate a manifest that specifies WinHTTP as a dependent assembly.</span></span> <span data-ttu-id="c7eab-111">Consulte [usando assemblies lado a lado](/windows/desktop/SbsCs/using-side-by-side-assemblies) para obter mais informações sobre como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="c7eab-111">See [Using Side-by-side Assemblies](/windows/desktop/SbsCs/using-side-by-side-assemblies) for more information about how to do this.</span></span>

## <a name="a-sample-winhttp-application-manifest"></a><span data-ttu-id="c7eab-112">Um manifesto de aplicativo do WinHTTP de exemplo</span><span class="sxs-lookup"><span data-stu-id="c7eab-112">A Sample WinHTTP Application Manifest</span></span>

<span data-ttu-id="c7eab-113">O manifesto de exemplo a seguir ilustra um manifesto de aplicativo que pode ser usado para vincular ao WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c7eab-113">The sample manifest below illustrates an application manifest that can be used for linking to WinHTTP.</span></span>

<span data-ttu-id="c7eab-114">Todos os atributos, exceto "Type" de " <assembly> <assemblyIdentity> ", devem ser modificados conforme apropriado para seu aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="c7eab-114">All attributes except "type" of the "<assembly><assemblyIdentity>" must be modified as appropriate for your particular application.</span></span> <span data-ttu-id="c7eab-115">O mesmo vale para o conteúdo do elemento " &lt; Description &gt; ".</span><span class="sxs-lookup"><span data-stu-id="c7eab-115">The same goes for the contents of the "&lt;description&gt;" element.</span></span>

<span data-ttu-id="c7eab-116">Além disso, certifique-se de que o atributo "processorArchitecture" de " <dependentAssembly> <assemblyIdentity> " corresponda ao atributo "processorArchitecture" de " <assembly> <assemblyIdentity> ".</span><span class="sxs-lookup"><span data-stu-id="c7eab-116">In addition, make sure that the "processorArchitecture" attribute of the "<dependentAssembly><assemblyIdentity>" matches the "processorArchitecture" attribute of the "<assembly><assemblyIdentity>".</span></span> <span data-ttu-id="c7eab-117">Abaixo, por exemplo, ambos estão definidos como "x86".</span><span class="sxs-lookup"><span data-stu-id="c7eab-117">Below, for example, both are set to "x86".</span></span>

<span data-ttu-id="c7eab-118">Todos os valores não específicos do seu aplicativo devem seguir os formulários mostrados abaixo.</span><span class="sxs-lookup"><span data-stu-id="c7eab-118">All values not specific to your application should take the forms shown below.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity
                    version="1.0.0.0"
                    processorArchitecture="x86"
                    name="Microsoft.Windows.Sample"
                    type="win32" />
  <description>Sample WinHttp Application</description>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity 
                    type="win32" 
                    name="Microsoft.Windows.WinHTTP" 
                    version="5.1.0.0"
                    processorArchitecture="x86" 
                    publicKeyToken="6595b64144ccf1df"
                    language="*" />
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
