---
description: Um arquivo de configuração do Publicador redireciona globalmente os aplicativos e assemblies com uma dependência em uma versão de um assembly lado a lado para usar outra versão do mesmo assembly.
ms.assetid: 9146c81e-8f43-4854-bbc4-1daaeb5fdda8
title: Configuração do Publicador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50ceb5263830cb1778aaaede673974cd7faca75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171281"
---
# <a name="publisher-configuration"></a><span data-ttu-id="6a6ea-103">Configuração do Publicador</span><span class="sxs-lookup"><span data-stu-id="6a6ea-103">Publisher Configuration</span></span>

<span data-ttu-id="6a6ea-104">Um [arquivo de configuração do Publicador](publisher-configuration-files.md) redireciona globalmente os aplicativos e assemblies com uma dependência em uma versão de um assembly lado a lado para usar outra versão do mesmo assembly.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-104">A [publisher configuration file](publisher-configuration-files.md) globally redirects applications and assemblies having a dependence on one version of a side-by-side assembly to use another version of the same assembly.</span></span> <span data-ttu-id="6a6ea-105">Isso permite que os aplicativos e assemblies usem o assembly atualizado sem precisar recompilar todos os aplicativos afetados.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-105">This enables applications and assemblies to use the updated assembly without having to rebuild all of the affected applications.</span></span>

<span data-ttu-id="6a6ea-106">Os [arquivos de configuração do Publicador](publisher-configuration-files.md) podem ser fornecidos pelo editor de um assembly ao emitir uma nova versão do assembly com correções de bugs ou atualizações de segurança compatíveis.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-106">[Publisher configuration files](publisher-configuration-files.md) may be provided by the publisher of an assembly when issuing a new version of the assembly with compatible bug fixes or security updates.</span></span> <span data-ttu-id="6a6ea-107">A versão atualizada deve ser totalmente compatível com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-107">The updated version should be fully backward compatible.</span></span> <span data-ttu-id="6a6ea-108">Um arquivo de configuração do Publicador nunca deve ser usado para adicionar novos recursos, a menos que a atualização seja totalmente compatível com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-108">A publisher configuration file should never be used to add new features unless the update is fully backward compatible.</span></span> <span data-ttu-id="6a6ea-109">Os arquivos de configuração do Publicador nunca devem ser usados para incrementar a versão principal ou secundária de um assembly.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-109">Publisher configuration files should never be used to increment the major or minor version of an assembly.</span></span> <span data-ttu-id="6a6ea-110">Por exemplo, não redirecione a versão do assembly 6.0.0.0 para 7.0.0.0 ou para 6.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-110">For example, do not redirect assembly version 6.0.0.0 to 7.0.0.0 or to 6.1.0.0.</span></span>

<span data-ttu-id="6a6ea-111">Os arquivos de configuração do Publicador só devem ser emitidos pelo Publicador do assembly.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-111">Publisher configuration files should only be issued by the publisher of the assembly.</span></span> <span data-ttu-id="6a6ea-112">Os desenvolvedores de assembly devem assinar assemblies lado a lado e arquivos de configuração do Publicador.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-112">Assembly developers should sign shared side-by-side assemblies and publisher configuration files.</span></span> <span data-ttu-id="6a6ea-113">Use a mesma chave para assinar o assembly e os arquivos de configuração do Publicador associados.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-113">Use the same key to sign the assembly and the associated publisher configuration files.</span></span> <span data-ttu-id="6a6ea-114">Os arquivos de configuração do Publicador devem ser assinados usando as mesmas ferramentas usadas para assemblies, consulte [exemplo de assinatura de assembly](assembly-signing-example.md) e [criando arquivos e catálogos assinados](creating-signed-files-and-catalogs.md).</span><span class="sxs-lookup"><span data-stu-id="6a6ea-114">Publisher configuration files should be signed using the same tools as used for assemblies, see [Assembly Signing Example](assembly-signing-example.md) and [Creating Signed Files and Catalogs](creating-signed-files-and-catalogs.md).</span></span>

<span data-ttu-id="6a6ea-115">Normalmente, a nova versão de um assembly e o arquivo de configuração do Publicador associado serão instalados em uma atualização service pack.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-115">Typically, the new version of an assembly and the associated publisher configuration file will be installed in a service pack update.</span></span> <span data-ttu-id="6a6ea-116">Os arquivos de configuração do Publicador nunca devem ser fornecidos com aplicativos como um redistribuível porque a instalação de um arquivo de configuração do Publicador redireciona globalmente os assemblies no sistema.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-116">Publisher configuration files should never be provided with applications as a redistributable because installing a publisher configuration file globally redirects assemblies on the system.</span></span> <span data-ttu-id="6a6ea-117">Se o assembly que está sendo atualizado for fornecido como um redistribuível, o Publicador deverá fornecer os dois procedimentos a seguir.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-117">If the assembly being updated is provided as a redistributable, the publisher should provide both of the following.</span></span>

-   <span data-ttu-id="6a6ea-118">Um pacote Windows Installer (arquivo. msi) que inclui a nova versão do assembly com a configuração do Publicador.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-118">A Windows Installer package (.msi file) that includes the new version of the assembly with publisher configuration.</span></span> <span data-ttu-id="6a6ea-119">Isso pode ser instalado como um service pack ou um QFE porque, nesse caso, o cliente optou por atualizar globalmente o sistema.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-119">This may be installed as a service pack or QFE because in this case the customer has chosen to globally update the system.</span></span> <span data-ttu-id="6a6ea-120">Essa versão do pacote nunca deve ser instalada por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-120">This version of the package should never be installed by applications.</span></span>
-   <span data-ttu-id="6a6ea-121">Um módulo de mesclagem Windows Installer (arquivo. msm) que inclui apenas a nova versão do assembly.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-121">A Windows Installer merge module (.msm file) that only includes the new version of the assembly.</span></span> <span data-ttu-id="6a6ea-122">Essa versão pode ser incluída em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-122">This version may be included with applications.</span></span>

<span data-ttu-id="6a6ea-123">Aplicativos que exigem uma versão mínima do assembly devem declarar sua dependência na versão mínima, se a versão mínima não estiver disponível em um sistema, o aplicativo não será iniciado.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-123">Applications requiring a minimum version of the assembly should state their dependency on the minimum version, if the minimum version is unavailable on a system then the application will fail to start.</span></span> <span data-ttu-id="6a6ea-124">Se ele estiver disponível como um redistribuível, ele deverá ser incluído na instalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-124">If it is available as a redistributable then it should be included in the application setup.</span></span>

<span data-ttu-id="6a6ea-125">Por exemplo, a instalação do seguinte [arquivo de configuração do Publicador](publisher-configuration-files.md) redireciona a associação da versão 2.0.0.0 do Microsoft. Windows. SampleAssembly para a versão 2.0.1.0.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-125">For example, installing the following [publisher configuration file](publisher-configuration-files.md) redirects binding from version 2.0.0.0 of the Microsoft.Windows.SampleAssembly to version 2.0.1.0.</span></span> <span data-ttu-id="6a6ea-126">Isso adiciona uma nova política, chamada 1.1.0.0. Policy, em% systemDrive% \\ Windows \\ winsxs \\ Policies \\ \_ Policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-WW \_ < *HashValue*>.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-126">This adds a new policy, named 1.1.0.0.Policy, under %systemDrive%\\windows\\winsxs\\policies\\x86\_policy.2.0.Microsoft.Windows.SampleAssembly\_75e377300ab7b886\_x-ww\_<*hashvalue*>.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="1.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

<span data-ttu-id="6a6ea-127">A instalação do arquivo de configuração do Publicador a seguir para o mesmo assembly redireciona a associação da versão 2.0.0.0 do Microsoft. Windows. SampleAssembly para a versão 2.0.3.0.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-127">Installing the following publisher configuration file for the same assembly redirects binding from version 2.0.0.0 of the Microsoft.Windows.SampleAssembly to version 2.0.3.0.</span></span> <span data-ttu-id="6a6ea-128">Isso adiciona outra política, chamada 2.1.0.0. Policy, em% systemDrive% \\ Windows \\ winsxs \\ Policies \\ \_ Policy. 2.0. Microsoft. Windows. SampleAssembly \_ 75e377300ab7b886 \_ x-WW \_ < *HashValue*>.</span><span class="sxs-lookup"><span data-stu-id="6a6ea-128">This adds another policy, named 2.1.0.0.Policy, under %systemDrive%\\windows\\winsxs\\policies\\x86\_policy.2.0.Microsoft.Windows.SampleAssembly\_75e377300ab7b886\_x-ww\_<*hashvalue*>.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
   <assemblyIdentity type="win32-policy" publicKeyToken="0000000000000000" name="policy.2.0.Microsoft.Windows.SampleAssembly" version="2.1.0.0" processorArchitecture="x86"/>
   <dependency>
      <dependentAssembly>
         <assemblyIdentity type="win32" name="Microsoft.Windows.SampleAssembly"  processorArchitecture="x86" publicKeyToken="75e377300ab7b886"/>
         <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.3.0"/>
      </dependentAssembly>
   </dependency>
</assembly>
```

 

 



