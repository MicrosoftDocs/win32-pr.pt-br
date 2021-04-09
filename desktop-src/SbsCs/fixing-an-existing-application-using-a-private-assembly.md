---
description: A partir do Windows XP, você pode criar um assembly privado e torná-lo disponível para um aplicativo específico.
ms.assetid: 08cebffc-6856-4dac-8600-5e7fecb5c69b
title: Corrigir um aplicativo existente usando um assembly privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 095c3eefc5f166ad09643a363ec4308d190e6586
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010432"
---
# <a name="fixing-an-existing-application-using-a-private-assembly"></a><span data-ttu-id="b844c-103">Corrigindo um aplicativo existente usando um assembly privado</span><span class="sxs-lookup"><span data-stu-id="b844c-103">Fixing an Existing Application Using a Private Assembly</span></span>

<span data-ttu-id="b844c-104">A partir do Windows XP, você pode criar um assembly privado e torná-lo disponível para um aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="b844c-104">Beginning with Windows XP, you can create a private assembly and make it available to a specific application.</span></span> <span data-ttu-id="b844c-105">Esse recurso pode ser usado para corrigir um aplicativo que se torna incompatível com uma atualização.</span><span class="sxs-lookup"><span data-stu-id="b844c-105">This capability can be used to fix an application that becomes incompatible with an update.</span></span> <span data-ttu-id="b844c-106">Um exemplo seria um aplicativo que se torna incompatível com a versão mais recente do MSVCRT.DLL após a atualização do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b844c-106">An example would be an application that becomes incompatible with the latest version of MSVCRT.DLL after upgrading the operating system.</span></span> <span data-ttu-id="b844c-107">Nesse caso, você não tem a opção de substituir a versão do sistema porque MSVCRT.DLL é um arquivo protegido do Windows.</span><span class="sxs-lookup"><span data-stu-id="b844c-107">In this case, you do not have the option of replacing the system version because MSVCRT.DLL is a Windows Protected File.</span></span> <span data-ttu-id="b844c-108">Em vez de ter que reescrever o aplicativo para funcionar com a nova versão do MSVCRT, você pode criar um assembly privado para o MSVCRT e instalá-lo na pasta do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b844c-108">Rather than having to rewrite the application to work with the new version of MSVCRT, you can create a private assembly for MSVCRT and install this in your application folder.</span></span> <span data-ttu-id="b844c-109">Observe que nem todo componente compartilhado é um candidato adequado para um assembly lado a lado privado, e alguns componentes têm restrições de licenciamento sobre onde seus componentes podem ser instalados.</span><span class="sxs-lookup"><span data-stu-id="b844c-109">Note that not every shared component is a suitable candidate for a private side-by-side assembly, and some components have licensing restrictions about where their components can be installed.</span></span> <span data-ttu-id="b844c-110">O componente precisa atender aos critérios para um componente lado a lado.</span><span class="sxs-lookup"><span data-stu-id="b844c-110">The component needs to meet the criteria for a side-by-side component.</span></span> <span data-ttu-id="b844c-111">Pergunte ao editor do componente se ele pode fornecer um assembly adequado.</span><span class="sxs-lookup"><span data-stu-id="b844c-111">Ask the publisher of the component if they can provide a suitable assembly.</span></span>

<span data-ttu-id="b844c-112">O manifesto do assembly privado e o manifesto do aplicativo devem ser instalados na mesma pasta que o executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b844c-112">The private assembly's manifest and the application's manifest should both be installed in the same folder as the application's executable.</span></span> <span data-ttu-id="b844c-113">Quando o aplicativo é executado, ele consulta o manifesto do aplicativo e carrega a versão do MSVCRT que é privada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b844c-113">When the application runs, it consults the application manifest and load the version of MSVCRT that is private to the application.</span></span>

<span data-ttu-id="b844c-114">Para este exemplo, o assembly privado incluiria MSVCRT.DLL e MSVCIRT.DLL como no seguinte manifesto do assembly:</span><span class="sxs-lookup"><span data-stu-id="b844c-114">For this example, the private assembly would include both MSVCRT.DLL and MSVCIRT.DLL as in the following assembly manifest:</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity type="win32"
      name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
version="6.0.0.0" 
processorArchitecture="x86"/>
    <file name="msvcrt.dll"/>
    <file name="msvcirt.dll"/>
</assembly>
```

<span data-ttu-id="b844c-115">Veja a seguir um exemplo de um possível manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b844c-115">The following is an example of a possible application manifest.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<assemblyIdentity 
    version="1.0.0.0" 
    processorArchitecture="x86" 
    name="APPLICATION" 
    type="win32" 
/> 
<description>Description of Application</description> 
<dependency> 
    <dependentAssembly> 
       <assemblyIdentity 
           type="win32"
           name="Microsoft.Windows.PrivateCPlusPlusRuntime" 
           version="6.0.0.0" 
           processorArchitecture="x86"/> 
    </dependentAssembly> 
</dependency> 
</assembly>
```

 

 



