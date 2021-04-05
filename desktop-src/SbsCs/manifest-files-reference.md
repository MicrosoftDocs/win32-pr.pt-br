---
description: Os assemblies lado a lado são usados com os seguintes tipos de arquivos de manifesto e de configuração. Manifestos e configurações são arquivos XML.
ms.assetid: 8b969a8f-586c-4556-87be-92db6c61e8ce
title: Referência de arquivos de manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea9915ba8e5e0c43b7e9c96e62ea46c3f0061b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090206"
---
# <a name="manifest-files-reference"></a><span data-ttu-id="687cb-104">Referência de arquivos de manifesto</span><span class="sxs-lookup"><span data-stu-id="687cb-104">Manifest Files Reference</span></span>

<span data-ttu-id="687cb-105">Os assemblies lado a lado são usados com os seguintes tipos de arquivos de manifesto e de configuração.</span><span class="sxs-lookup"><span data-stu-id="687cb-105">Side-by-side assemblies are used with the following types of manifest and configuration files.</span></span> <span data-ttu-id="687cb-106">Manifestos e configurações são arquivos XML.</span><span class="sxs-lookup"><span data-stu-id="687cb-106">Manifests and configurations are XML files.</span></span>



| <span data-ttu-id="687cb-107">Manifest</span><span class="sxs-lookup"><span data-stu-id="687cb-107">Manifest</span></span>                                                               | <span data-ttu-id="687cb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="687cb-108">Description</span></span>                                                                                                                                                                                                   |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="687cb-109">Manifestos de assembly</span><span class="sxs-lookup"><span data-stu-id="687cb-109">Assembly manifests</span></span>](assembly-manifests.md)                           | <span data-ttu-id="687cb-110">Descreve os nomes, as versões, os recursos e as dependências de assembly de assemblies lado a lado.</span><span class="sxs-lookup"><span data-stu-id="687cb-110">Describes the names, versions, resources, and assembly dependencies of side-by-side assemblies.</span></span>                                                                                                               |
| [<span data-ttu-id="687cb-111">Manifestos do aplicativo</span><span class="sxs-lookup"><span data-stu-id="687cb-111">Application manifests</span></span>](application-manifests.md)                     | <span data-ttu-id="687cb-112">Descreve os nomes e as versões de assemblies compartilhados lado a lado que o aplicativo deve associar em tempo de execução e também pode conter metadados para assemblies particulares lado a lado usados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="687cb-112">Describes the names and versions of shared side-by-side assemblies that the application should bind to at run time and may also contain metadata for private side-by-side assemblies used by the application.</span></span> |
| [<span data-ttu-id="687cb-113">Arquivos de configuração de aplicativo</span><span class="sxs-lookup"><span data-stu-id="687cb-113">Application Configuration Files</span></span>](application-configuration-files.md) | <span data-ttu-id="687cb-114">Redireciona as versões de assembly das dependências de assembly usando [a configuração por aplicativo](per-application-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="687cb-114">Redirects the assembly versions of assembly dependencies using [per-application configuration](per-application-configuration.md).</span></span>                                                                            |
| [<span data-ttu-id="687cb-115">Arquivos de configuração do Publicador</span><span class="sxs-lookup"><span data-stu-id="687cb-115">Publisher Configuration Files</span></span>](publisher-configuration-files.md)     | <span data-ttu-id="687cb-116">Redireciona as versões de assembly de dependências de assembly em uma base por assembly usando uma [configuração de Publicador](publisher-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="687cb-116">Redirects the assembly versions of assembly dependencies on a per-assembly basis using a [publisher configuration](publisher-configuration.md).</span></span>                                                              |



 

<span data-ttu-id="687cb-117">Para obter uma lista do esquema do arquivo de manifesto, consulte [manifesto do arquivo de manifest](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="687cb-117">For a listing of the manifest file schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="687cb-118">Para obter uma lista do esquema de arquivo de configuração de aplicativo, consulte [esquema de arquivo de configuração de aplicativo](application-configuration-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="687cb-118">For a listing of the application configuration file schema, see [Application Configuration File Schema](application-configuration-file-schema.md).</span></span>

<span data-ttu-id="687cb-119">Para obter uma lista do esquema do arquivo de configuração do Publicador, consulte [esquema do arquivo de configuração do Publicador](publisher-configuration-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="687cb-119">For a listing of the publisher configuration file schema, see [Publisher Configuration File Schema](publisher-configuration-file-schema.md).</span></span>

<span data-ttu-id="687cb-120">Outras tecnologias estendem o formato usado pelos manifestos de configuração e controle de versão do Windows.</span><span class="sxs-lookup"><span data-stu-id="687cb-120">Other technologies extend the format used by Windows versioning and configuration manifests.</span></span> <span data-ttu-id="687cb-121">Os desenvolvedores devem consultar a documentação específica da tecnologia que está sendo usada para obter informações sobre o formato do manifesto.</span><span class="sxs-lookup"><span data-stu-id="687cb-121">Developers should refer to the documentation that is specific to the technology being used for information about the manifest format.</span></span> <span data-ttu-id="687cb-122">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="687cb-122">For example:</span></span>

-   [<span data-ttu-id="687cb-123">ClickOnce</span><span class="sxs-lookup"><span data-stu-id="687cb-123">ClickOnce</span></span>](/visualstudio/deployment/clickonce-reference?view=vs-2015)
-   [<span data-ttu-id="687cb-124">Common Language Runtime</span><span class="sxs-lookup"><span data-stu-id="687cb-124">Common Language Runtime</span></span>](/dotnet/standard/clr)
-   <span data-ttu-id="687cb-125">[UAC (Controle de Conta de Usuário)](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="687cb-125">[User Account Control (UAC)](/previous-versions/bb756929(v=msdn.10))</span></span>

 

 
