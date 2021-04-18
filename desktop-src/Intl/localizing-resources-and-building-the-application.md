---
description: Este tópico descreve como criar um aplicativo MUI típico.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Localizando recursos e compilando o aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74262499b20836ee4860f1c0fc1a1bf80e19d58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810333"
---
# <a name="localizing-resources-and-building-the-application"></a><span data-ttu-id="21cc2-103">Localizando recursos e compilando o aplicativo</span><span class="sxs-lookup"><span data-stu-id="21cc2-103">Localizing Resources and Building the Application</span></span>

<span data-ttu-id="21cc2-104">Este tópico descreve como criar um aplicativo MUI típico.</span><span class="sxs-lookup"><span data-stu-id="21cc2-104">This topic describes how to build a typical MUI application.</span></span> <span data-ttu-id="21cc2-105">Supõe-se que você esteja usando Microsoft Visual Studio para codificação e Microsoft Visual Studio ou a linha de comando do Visual Studio para compilação.</span><span class="sxs-lookup"><span data-stu-id="21cc2-105">It is assumed that you are using Microsoft Visual Studio for coding and either Microsoft Visual Studio or the Visual Studio command line for building.</span></span> <span data-ttu-id="21cc2-106">Você deve usar um arquivo de solução. sln para seu aplicativo e dar suporte a um arquivo Resource. h para refletir o arquivo de recurso de idioma base.</span><span class="sxs-lookup"><span data-stu-id="21cc2-106">You are assumed to use an .sln solution file for your application and support a Resource.h file to reflect the base language resource file.</span></span>

> [!Note]  
> <span data-ttu-id="21cc2-107">Se estiver usando a linha de comando do Visual Studio para a compilação, você usará o comando **VCBuild** para compilar o arquivo de solução.</span><span class="sxs-lookup"><span data-stu-id="21cc2-107">If using the Visual Studio command line for the build, you will use the **vcbuild** command to build the solution file.</span></span>

 

<span data-ttu-id="21cc2-108">Os arquivos de aplicativo são criados separadamente para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="21cc2-108">Application files are built separately for each language.</span></span> <span data-ttu-id="21cc2-109">Cada compilação cria arquivos. exe idênticos de idioma e. exe. mui específicos do idioma.</span><span class="sxs-lookup"><span data-stu-id="21cc2-109">Each build creates identical language-neutral .exe and language-specific .exe.mui files.</span></span> <span data-ttu-id="21cc2-110">Além disso, vários outros arquivos são copiados para as pastas de liberação apropriadas.</span><span class="sxs-lookup"><span data-stu-id="21cc2-110">In addition, various other files are copied to the appropriate release folders.</span></span>

<span data-ttu-id="21cc2-111">A compilação do aplicativo depende do tipo de recursos e do tipo de localização que você está usando.</span><span class="sxs-lookup"><span data-stu-id="21cc2-111">The application build depends on the type of resources and the type of localization that you are using.</span></span> <span data-ttu-id="21cc2-112">Para a localização de pré-compilação, você tem uma cópia do arquivo de idioma base localizado para cada idioma com suporte.</span><span class="sxs-lookup"><span data-stu-id="21cc2-112">For pre-build localization, you have one copy of the base language file localized for each supported language.</span></span> <span data-ttu-id="21cc2-113">Para a localização após a compilação, você pode copiar o arquivo. mui resultante da compilação do módulo executável e do recurso e fornecer as cópias para os localizadores.</span><span class="sxs-lookup"><span data-stu-id="21cc2-113">For post-build localization, you can copy the .mui file resulting from the build of the executable and resource module, and provide the copies to the localizers.</span></span>

> [!Note]  
> <span data-ttu-id="21cc2-114">O procedimento a seguir pressupõe recursos Win32 PE com um projeto do Visual Studio criado para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="21cc2-114">The following procedure assumes Win32 PE resources with one Visual Studio project built for each language.</span></span> <span data-ttu-id="21cc2-115">Os recursos de idioma base são fornecidos em um arquivo. rc e carregados usando um módulo de DLL.</span><span class="sxs-lookup"><span data-stu-id="21cc2-115">The base language resources are provided in an .rc file and loaded using a DLL module.</span></span> <span data-ttu-id="21cc2-116">Você pode repetir o procedimento conforme necessário para compilar para todos os idiomas com suporte.</span><span class="sxs-lookup"><span data-stu-id="21cc2-116">You can repeat the procedure as needed to build for all languages supported.</span></span>

 

<span data-ttu-id="21cc2-117">**Para compilar o aplicativo**</span><span class="sxs-lookup"><span data-stu-id="21cc2-117">**To build the application**</span></span>

1.  <span data-ttu-id="21cc2-118">Configure um projeto do Visual Studio para o idioma base.</span><span class="sxs-lookup"><span data-stu-id="21cc2-118">Set up a Visual Studio project for the base language.</span></span>
2.  <span data-ttu-id="21cc2-119">Se estiver interessado em usar um arquivo de configuração de recurso com as ferramentas de recurso, defina um conforme descrito em [preparando um arquivo de configuração de recurso](preparing-a-resource-configuration-file.md).</span><span class="sxs-lookup"><span data-stu-id="21cc2-119">If interested in using a resource configuration file with the resource tools, set one up as described in [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>
3.  <span data-ttu-id="21cc2-120">Defina os parâmetros exigidos pelo utilitário de compilador RC nas páginas de propriedades do projeto em **Propriedades de configuração → recursos → linha de comando → opções adicionais**.</span><span class="sxs-lookup"><span data-stu-id="21cc2-120">Set parameters required by the RC Compiler utility in the property pages for the project under **Configuration Properties → Resources → Command Line → Additional options**.</span></span>
4.  <span data-ttu-id="21cc2-121">Execute o compilador RC.</span><span class="sxs-lookup"><span data-stu-id="21cc2-121">Run RC Compiler.</span></span> <span data-ttu-id="21cc2-122">O utilitário compila e divide os recursos não localizáveis e localizáveis em dois arquivos de objeto diferentes, usando dados de configuração de recursos.</span><span class="sxs-lookup"><span data-stu-id="21cc2-122">The utility compiles and splits the non-localizable and localizable resources into two different object files, using resource configuration data.</span></span> <span data-ttu-id="21cc2-123">Nesta etapa, os recursos neutros à linguagem são vinculados a um arquivo LN.</span><span class="sxs-lookup"><span data-stu-id="21cc2-123">In this step the language-neutral resources are linked into an LN file.</span></span> <span data-ttu-id="21cc2-124">Para obter mais informações, consulte a descrição do utilitário em [utilitários de recursos](resource-utilities.md).</span><span class="sxs-lookup"><span data-stu-id="21cc2-124">For more information, see the utility description in [Resource Utilities](resource-utilities.md).</span></span>
5.  <span data-ttu-id="21cc2-125">Para vincular os recursos específicos do idioma a um arquivo. mui específico de idioma, defina um evento de pós-compilação para o projeto nas páginas de propriedade em **Propriedades de configuração → eventos de compilação → evento de pós-compilação → linha de comando**.</span><span class="sxs-lookup"><span data-stu-id="21cc2-125">To link the language-specific resources into a language-specific .mui file, set a post-build event for the project in the property pages under **Configuration Properties → Build Events → Post-Build Event → Command Line**.</span></span>
6.  <span data-ttu-id="21cc2-126">Defina um evento de pós-compilação para aplicar o valor da soma de verificação do arquivo LN ao arquivo. mui para o idioma.</span><span class="sxs-lookup"><span data-stu-id="21cc2-126">Set a post-build event to apply the checksum value from the LN file to the .mui file for the language.</span></span> <span data-ttu-id="21cc2-127">Você pode usar o utilitário MUIRCT para esta etapa.</span><span class="sxs-lookup"><span data-stu-id="21cc2-127">You can use the MUIRCT utility for this step.</span></span> <span data-ttu-id="21cc2-128">Para obter mais informações, consulte a descrição do utilitário em [utilitários de recursos](resource-utilities.md).</span><span class="sxs-lookup"><span data-stu-id="21cc2-128">For more information, see the utility description in [Resource Utilities](resource-utilities.md).</span></span>
7.  <span data-ttu-id="21cc2-129">Use a linha de comando de evento de pós-compilação para adicionar comandos para copiar os arquivos na estrutura de pastas de liberação apropriada.</span><span class="sxs-lookup"><span data-stu-id="21cc2-129">Use the post-build event command line to add commands to copy the files into the appropriate release folder structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21cc2-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="21cc2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21cc2-131">Usando a interface do usuário multilíngue</span><span class="sxs-lookup"><span data-stu-id="21cc2-131">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="21cc2-132">Preparando um arquivo de configuração de recurso</span><span class="sxs-lookup"><span data-stu-id="21cc2-132">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="21cc2-133">Utilitários de recursos</span><span class="sxs-lookup"><span data-stu-id="21cc2-133">Resource Utilities</span></span>](resource-utilities.md)
</dt> </dl>

 

 



