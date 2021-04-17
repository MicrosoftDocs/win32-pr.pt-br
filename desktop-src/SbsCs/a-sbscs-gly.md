---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0D537FD1-AD5C-43CB-989F-4B5B7C0A1208
title: A (aplicativos isolados e assemblies lado a lado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41a925d83cf602f5d23c7d043102927748da14a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780183"
---
# <a name="a-isolated-applications-and-side-by-side-assemblies"></a><span data-ttu-id="92c11-103">A (aplicativos isolados e assemblies lado a lado)</span><span class="sxs-lookup"><span data-stu-id="92c11-103">A (Isolated Applications and Side-by-side Assemblies)</span></span>

<span data-ttu-id="92c11-104">A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [i](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span><span class="sxs-lookup"><span data-stu-id="92c11-104">A B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="92c11-105"><span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**contexto de ativação**</span><span class="sxs-lookup"><span data-stu-id="92c11-105"><span id="_win32_activation_context_gly"></span><span id="_WIN32_ACTIVATION_CONTEXT_GLY"></span>**activation context**</span></span>
</dt> <dd>

<span data-ttu-id="92c11-106">Uma estrutura de dados na memória.</span><span class="sxs-lookup"><span data-stu-id="92c11-106">A data structure in memory.</span></span> <span data-ttu-id="92c11-107">Cada seção dessa estrutura contém metadados para funções de API com reconhecimento lado a lado.</span><span class="sxs-lookup"><span data-stu-id="92c11-107">Each section of this structure contains metadata for side-by-side-aware API functions.</span></span> <span data-ttu-id="92c11-108">Por exemplo, uma seção pode ter dados de redirecionamento de DLL, que são usados pelo carregador de DLL e outro pode ter dados de servidor COM.</span><span class="sxs-lookup"><span data-stu-id="92c11-108">For example, one section may have DLL redirection data, which is used by the DLL loader, and another may have COM server data.</span></span> <span data-ttu-id="92c11-109">Esses dados podem ser usados para redirecionar o carregamento de uma DLL para uma versão específica, a criação de um objeto COM ou a criação de uma janela para uma versão mais compatível para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92c11-109">This data may be used to redirect the loading of a DLL to a specific version, the creation of a COM object, or the creation of a window to a version that is most compatible for the application.</span></span>

</dd> <dt>

<span data-ttu-id="92c11-110"><span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**configuração do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="92c11-110"><span id="_win32_application_configuration_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_GLY"></span>**application configuration**</span></span>
</dt> <dd>

<span data-ttu-id="92c11-111">Nomes e versões de assemblies lado a lado necessários para executar um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92c11-111">Names and versions of side-by-side assemblies required to run an application.</span></span> <span data-ttu-id="92c11-112">Quando um aplicativo é implantado com um manifesto, as dependências em versões específicas de assemblies compartilhados lado a lado são explicitamente definidas.</span><span class="sxs-lookup"><span data-stu-id="92c11-112">When an application is deployed with a manifest, dependencies on specific versions of shared side-by-side assemblies are explicitly defined.</span></span> <span data-ttu-id="92c11-113">Por padrão, a versão do assembly especificado no manifesto é a versão que é usada na ativação.</span><span class="sxs-lookup"><span data-stu-id="92c11-113">By default, the version of the assembly specified in the manifest is the version that is used upon activation.</span></span> <span data-ttu-id="92c11-114">Configuração de aplicativo global especifica a configuração de todos os aplicativos no sistema.</span><span class="sxs-lookup"><span data-stu-id="92c11-114">Global application configuration specifies the configuration of all applications on the system.</span></span> <span data-ttu-id="92c11-115">A configuração por aplicativo pode substituir a configuração de aplicativo global em uma base por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92c11-115">Per-application configuration can override the global application configuration on a per-application basis.</span></span>

</dd> <dt>

<span data-ttu-id="92c11-116"><span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**manifesto de configuração do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="92c11-116"><span id="_win32_application_configuration_manifest_gly"></span><span id="_WIN32_APPLICATION_CONFIGURATION_MANIFEST_GLY"></span>**application configuration manifest**</span></span>
</dt> <dd>

<span data-ttu-id="92c11-117">Arquivo que especifica assemblies lado a lado a serem usados por um aplicativo totalmente ou parcialmente isolado.</span><span class="sxs-lookup"><span data-stu-id="92c11-117">File that specifies side-by-side assemblies to be used by a fully or partially isolated application.</span></span> <span data-ttu-id="92c11-118">Os arquivos de manifesto de configuração do aplicativo são instalados na mesma pasta que o arquivo executável do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92c11-118">Application configuration manifest files are installed in the same folder as the application's executable file.</span></span>

</dd> <dt>

<span data-ttu-id="92c11-119"><span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**manifesto do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="92c11-119"><span id="_win32_application_manifest_gly"></span><span id="_WIN32_APPLICATION_MANIFEST_GLY"></span>**application manifest**</span></span>
</dt> <dd>

<span data-ttu-id="92c11-120">Arquivo que descreve um aplicativo isolado.</span><span class="sxs-lookup"><span data-stu-id="92c11-120">File that describes an isolated application.</span></span> <span data-ttu-id="92c11-121">Ele especifica as informações necessárias para executar o aplicativo, incluindo dependências em assemblies privados, versões específicas de assemblies compartilhados e metadados para assemblies privados.</span><span class="sxs-lookup"><span data-stu-id="92c11-121">It specifies the information required to run the application, including dependencies on private assemblies, specific versions of shared assemblies and metadata for private assemblies.</span></span> <span data-ttu-id="92c11-122">O nome de um arquivo de manifesto do aplicativo é o nome do executável do aplicativo seguido pela extensão. manifest.</span><span class="sxs-lookup"><span data-stu-id="92c11-122">The name of an application manifest file is the name of the application executable followed by the extension .manifest.</span></span> <span data-ttu-id="92c11-123">Por exemplo, para MySampleApp.exe, o arquivo de manifesto seria MySampleApp.exe. manifest.</span><span class="sxs-lookup"><span data-stu-id="92c11-123">For example, for MySampleApp.exe, the manifest file would be MySampleApp.exe.manifest.</span></span>

</dd> <dt>

<span data-ttu-id="92c11-124"><span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**)**</span><span class="sxs-lookup"><span data-stu-id="92c11-124"><span id="_win32_assembly_gly"></span><span id="_WIN32_ASSEMBLY_GLY"></span>**assembly**</span></span>
</dt> <dd>

<span data-ttu-id="92c11-125">Unidade fundamental para nomeação, vinculação, controle de versão, implantação ou configuração de um bloco de código de programação.</span><span class="sxs-lookup"><span data-stu-id="92c11-125">Fundamental unit for naming, binding, versioning, deploying, or configuring a block of programming code.</span></span> <span data-ttu-id="92c11-126">Esses assemblies de código podem ser colocados em DLLs ou assemblies COM.</span><span class="sxs-lookup"><span data-stu-id="92c11-126">These code assemblies may be placed in DLLs or COM assemblies.</span></span> <span data-ttu-id="92c11-127">Aplicativos com funcionalidade comum podem executar blocos compartilhados de código de programação que são chamados de módulos ou assemblies de código.</span><span class="sxs-lookup"><span data-stu-id="92c11-127">Applications with common functionality may run shared blocks of programming code which are referred to as modules or code assemblies.</span></span> <span data-ttu-id="92c11-128">A infraestrutura para o compartilhamento seguro de assemblies é conhecida como compartilhamento de assembly lado a lado.</span><span class="sxs-lookup"><span data-stu-id="92c11-128">The infrastructure for the safe sharing of assemblies is referred to as side-by-side assembly sharing.</span></span>

</dd> <dt>

<span data-ttu-id="92c11-129"><span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**manifesto do assembly**</span><span class="sxs-lookup"><span data-stu-id="92c11-129"><span id="_win32_assembly_manifest_gly"></span><span id="_WIN32_ASSEMBLY_MANIFEST_GLY"></span>**assembly manifest**</span></span>
</dt> <dd>

<span data-ttu-id="92c11-130">Descrição de um assembly lado a lado.</span><span class="sxs-lookup"><span data-stu-id="92c11-130">Description of a side-by-side assembly.</span></span> <span data-ttu-id="92c11-131">Ele especifica o nome, a versão, os arquivos, os recursos do assembly, os dados de associação para os itens do assembly e as dependências em outros assemblies lado a lado.</span><span class="sxs-lookup"><span data-stu-id="92c11-131">It specifies the name, version, files, resources of the assembly, binding data for items of the assembly, and dependencies on other side-by-side assemblies.</span></span> <span data-ttu-id="92c11-132">Um arquivo de manifesto do assembly pode ter qualquer nome de arquivo válido, desde que seja seguido pela extensão. manifest.</span><span class="sxs-lookup"><span data-stu-id="92c11-132">An assembly manifest file can have any valid file name, as long as it is followed by the extension .manifest.</span></span>

</dd> </dl>

 

 



