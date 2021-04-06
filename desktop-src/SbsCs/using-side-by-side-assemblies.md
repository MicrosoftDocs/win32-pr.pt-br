---
description: Use o procedimento a seguir para desenvolver um novo aplicativo ou atualizar um aplicativo existente, para usar os assemblies lado a lado disponíveis da Microsoft ou de outros publicadores de assembly lado a lado.
ms.assetid: da6b6767-8a30-4a76-a030-615067a2cb17
title: Usando assemblies lado a lado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1992562a0868918de2901a7ca88033784af6ef1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826995"
---
# <a name="using-side-by-side-assemblies"></a><span data-ttu-id="cdfe4-103">Usando assemblies lado a lado</span><span class="sxs-lookup"><span data-stu-id="cdfe4-103">Using Side-by-side Assemblies</span></span>

<span data-ttu-id="cdfe4-104">Use o procedimento a seguir para desenvolver um novo aplicativo ou atualizar um aplicativo existente, para usar os [assemblies](about-side-by-side-assemblies-.md) lado a lado disponíveis da Microsoft ou de outros publicadores de assembly lado a lado.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-104">Use the following procedure to develop a new application, or update an existing application, to use the [side-by-side assemblies](about-side-by-side-assemblies-.md) available from Microsoft or other side-by-side assembly publishers.</span></span> <span data-ttu-id="cdfe4-105">Para obter uma lista dos assemblies lado a lado fornecidos atualmente pela Microsoft, consulte [assemblies lado a lado da Microsoft com suporte](supported-microsoft-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="cdfe4-105">For a list of the side-by-side assemblies currently provided by Microsoft, see [Supported Microsoft Side-by-side Assemblies](supported-microsoft-side-by-side-assemblies.md).</span></span> <span data-ttu-id="cdfe4-106">Observe que o aplicativo deve ser executado em pelo menos o Windows XP para instalar os assemblies como assemblies lado a lado.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-106">Note that the application must be run on at least Windows XP to install the assemblies as side-by-side assemblies.</span></span> <span data-ttu-id="cdfe4-107">Para obter mais informações, consulte [diretrizes para criar assemblies lado a lado](guidelines-for-creating-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="cdfe4-107">For more information, see [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md).</span></span>

<span data-ttu-id="cdfe4-108">**Para adicionar um assembly lado a lado a um aplicativo**</span><span class="sxs-lookup"><span data-stu-id="cdfe4-108">**To add a side-by-side assembly to an application**</span></span>

1.  <span data-ttu-id="cdfe4-109">Identifique os assemblies lado a lado que seu aplicativo requer.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-109">Identify the side-by-side assemblies that your application requires.</span></span> <span data-ttu-id="cdfe4-110">A partir do Windows XP, esses assemblies lado a lado e seus manifestos de assembly são instalados com o sistema operacional, mas não são registrados globalmente.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-110">Starting with Windows XP, these side-by-side assemblies and their assembly manifests are installed with the operating system but are not globally registered.</span></span>
2.  <span data-ttu-id="cdfe4-111">Use um editor de XML para criar um [manifesto de aplicativo](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="cdfe4-111">Use an XML editor to create an [application manifest](application-manifests.md).</span></span> <span data-ttu-id="cdfe4-112">Consulte o exemplo de manifesto do aplicativo abaixo.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-112">See the example application manifest below.</span></span> <span data-ttu-id="cdfe4-113">Para obter mais informações, consulte [manifestos do aplicativo](application-manifests.md) na [referência de arquivos de manifesto](manifest-files-reference.md).</span><span class="sxs-lookup"><span data-stu-id="cdfe4-113">For more information, see [Application Manifests](application-manifests.md) in the [Manifest Files Reference](manifest-files-reference.md).</span></span>
3.  <span data-ttu-id="cdfe4-114">Insira valores de atributo no subelemento [*AssemblyIdentity do contexto def*](d-sbscs-gly.md) do manifesto do aplicativo que define exclusivamente o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-114">Enter attribute values in the [*DEF-context assemblyIdentity*](d-sbscs-gly.md) subelement of the application manifest that uniquely defines the application.</span></span> <span data-ttu-id="cdfe4-115">Para obter mais informações sobre o **AssemblyIdentity** de contexto def, consulte [manifestos do aplicativo](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="cdfe4-115">For more information about the DEF-context **assemblyIdentity**, see [Application Manifests](application-manifests.md).</span></span>
4.  <span data-ttu-id="cdfe4-116">Se o assembly contiver assemblies dependentes, insira valores de atributo nos subelementos de [*AssemblyIdentity de contexto de referência*](r-sbscs-gly.md) correspondente do manifesto do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-116">If the assembly contains any dependent assemblies, enter attribute values into the corresponding [*REF-context assemblyIdentity*](r-sbscs-gly.md) subelements of the application manifest.</span></span> <span data-ttu-id="cdfe4-117">Para obter mais informações sobre o **AssemblyIdentity** de contexto de referência, consulte [manifestos de aplicativo](application-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="cdfe4-117">For more information about the REF-context **assemblyIdentity**, see [Application Manifests](application-manifests.md).</span></span>

    ``` syntax
    <dependentAssembly>
      <assemblyIdentity type="win32"
                        name="Microsoft.Windows.SampleAssembly"
                        version="6.0.0.0" processorArchitecture="x86"
                        publicKeyToken="a5aaf5ba15723d5"/>
    ```

5.  <span data-ttu-id="cdfe4-118">Você pode incluir o manifesto do aplicativo no arquivo de cabeçalho executável binário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-118">You may include the application manifest in the application's binary executable header file.</span></span>

    <span data-ttu-id="cdfe4-119">Nesse caso, adicione também a seguinte linha ao arquivo de cabeçalho do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="cdfe4-119">In this case, also add the following line to the application header file:</span></span>

    <dl> <span data-ttu-id="cdfe4-120">Manifesto de ID de recurso de manifesto de CREATEPROCESS \_ \_ \_ \_ "YourApp.exe. manifest"</span><span class="sxs-lookup"><span data-stu-id="cdfe4-120">CREATEPROCESS\_MANIFEST\_RESOURCE\_ID RT\_MANIFEST "YourApp.exe.manifest"</span></span>  
    </dl>

    <span data-ttu-id="cdfe4-121">Como alternativa, você pode posicionar um arquivo de manifesto separado no mesmo diretório que o arquivo executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-121">As an alternative, you can place a separate manifest file in the same directory as your application's executable file.</span></span> <span data-ttu-id="cdfe4-122">O sistema operacional carrega o manifesto do sistema de arquivos primeiro e, em seguida, verifica a seção de recursos do executável.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-122">The operating system loads the manifest from the file system first, and then checks the resource section of the executable.</span></span> <span data-ttu-id="cdfe4-123">A versão do sistema de arquivos tem precedência.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-123">The file system version takes precedence.</span></span>

6.  <span data-ttu-id="cdfe4-124">Os [assemblies compartilhados](/windows/desktop/Msi/shared-assemblies) devem ser instalados usando o [Windows Installer](../msi/windows-installer-portal.md) versão 2,0.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-124">[Shared assemblies](/windows/desktop/Msi/shared-assemblies) should be installed using the [Windows Installer](../msi/windows-installer-portal.md) version 2.0.</span></span> <span data-ttu-id="cdfe4-125">Crie um pacote de Windows Installer conforme descrito em [como instalar assemblies do Win32 para compartilhamento lado a lado no Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfe4-125">Author a Windows Installer package as described in [How Do I Install Win32 Assemblies for Side-by-side Sharing on Windows XP?](../msi/installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md).</span></span>
7.  <span data-ttu-id="cdfe4-126">Os [assemblies privados](/windows/desktop/Msi/private-assemblies) podem ser instalados usando o [Windows Installer](../msi/windows-installer-portal.md) versão 2,0.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-126">[Private assemblies](/windows/desktop/Msi/private-assemblies) can be installed using the [Windows Installer](../msi/windows-installer-portal.md) version 2.0.</span></span> <span data-ttu-id="cdfe4-127">Crie um pacote de Windows Installer conforme descrito em [como instalar assemblies do Win32 para o uso particular de um aplicativo no Windows XP?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md).</span><span class="sxs-lookup"><span data-stu-id="cdfe4-127">Author a Windows Installer package as described in [How Do I Install Win32 Assemblies for the Private Use of an Application on Windows XP?](../msi/installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md).</span></span> <span data-ttu-id="cdfe4-128">Você também pode usar qualquer outro instalador para copiar um assembly privado e seu manifesto na mesma pasta que o arquivo executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-128">You can also use any other installer to copy a private assembly and its manifest into the same folder as the application's executable file.</span></span>
8.  <span data-ttu-id="cdfe4-129">Teste seu aplicativo para garantir os resultados.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-129">Test your application to ensure the results.</span></span> <span data-ttu-id="cdfe4-130">Observe que seu computador de teste não deve ter o assembly lado a lado registrado.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-130">Note that your test computer should not have the side-by-side assembly registered.</span></span>
9.  <span data-ttu-id="cdfe4-131">Implante seu aplicativo ou atualize-o como um pacote Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cdfe4-131">Deploy your application or update as a Windows Installer package.</span></span>

## <a name="example-application-manifest"></a><span data-ttu-id="cdfe4-132">Exemplo de manifesto do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cdfe4-132">Example Application Manifest</span></span>

<span data-ttu-id="cdfe4-133">Veja a seguir um exemplo de um manifesto de aplicativo:</span><span class="sxs-lookup"><span data-stu-id="cdfe4-133">The following is an example of an application manifest:</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
  <assemblyIdentity type="win32" name="Microsoft.Windows.mysampleapp" version="1.0.0.0" processorArchitecture="x86"/>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly" version="6.0.0.0" processorArchitecture="x86" publicKeyToken="a5aaf5ba15723d5"/>
    </dependentAssembly>
  </dependency>
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" name="Microsoft.Tools.MyPrivateDll" version="2.5.0.0" processorArchitecture="x86"/>
    </dependentAssembly>
  </dependency>
</assembly>
```

 

 
