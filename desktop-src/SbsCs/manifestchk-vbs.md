---
description: O arquivo VBScript Manifestchk.vbs é uma ferramenta de validação fornecida no SDK (Software Development Kit) do Microsoft Windows que valida os arquivos de manifesto do aplicativo e do assembly.
ms.assetid: 8269cb92-bd3f-411f-8395-fe06ed550cc5
title: Manifestchk.vbs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09aff347fbd8b6f44c4e38f123870fa5ee8df572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370688"
---
# <a name="manifestchkvbs"></a><span data-ttu-id="030f8-103">Manifestchk.vbs</span><span class="sxs-lookup"><span data-stu-id="030f8-103">Manifestchk.vbs</span></span>

<span data-ttu-id="030f8-104">O arquivo VBScript Manifestchk.vbs é uma ferramenta de validação fornecida no SDK (Software Development Kit) do Microsoft Windows que valida os arquivos de manifesto do aplicativo e do assembly.</span><span class="sxs-lookup"><span data-stu-id="030f8-104">The VBScript file Manifestchk.vbs is a validation tool provided in the Microsoft Windows Software Development Kit (SDK) that validates application and assembly manifest files.</span></span>

<span data-ttu-id="030f8-105">A execução deste exemplo requer o Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="030f8-105">Running this sample requires Windows Script Host.</span></span> <span data-ttu-id="030f8-106">Para obter mais informações sobre o Windows Script Host, consulte a seção Windows Script Host do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="030f8-106">For more information about Windows Script Host, see the Windows Script Host section of the Windows SDK.</span></span> <span data-ttu-id="030f8-107">O Windows Script Host é, na verdade, dois hosts.</span><span class="sxs-lookup"><span data-stu-id="030f8-107">Windows Script Host is actually two hosts.</span></span> <span data-ttu-id="030f8-108">CScript.exe é a versão que permite executar scripts no prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="030f8-108">CScript.exe is the version that enables you to run scripts from the command prompt.</span></span> <span data-ttu-id="030f8-109">CScript.exe fornece opções de linha de comando para definir propriedades de script.</span><span class="sxs-lookup"><span data-stu-id="030f8-109">CScript.exe provides command-line switches for setting script properties.</span></span>

<span data-ttu-id="030f8-110">O formato de linha de comando é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="030f8-110">The command-line format is the following:</span></span>

<span data-ttu-id="030f8-111">**Cscript//nologo manifestchk.vbs/s:** *\[ unidade: \] \[ caminho \] schemafilename* **/m:** *\[ unidade: \] \[ caminho \] ManifestFileName* **\[ /q \] /t:** *Option*</span><span class="sxs-lookup"><span data-stu-id="030f8-111">**Cscript //nologo manifestchk.vbs /s:** *\[drive:\]\[path\]schemafilename* **/m:** *\[drive:\]\[path\]manifestfilename* **\[/q\] /t:** *option*</span></span>

<span data-ttu-id="030f8-112">Os sinalizadores definidos para Manifestchk.vbs são descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="030f8-112">The flags defined for Manifestchk.vbs are described in the following table.</span></span>



| <span data-ttu-id="030f8-113">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="030f8-113">Flag</span></span> | <span data-ttu-id="030f8-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="030f8-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="030f8-115">/s</span><span class="sxs-lookup"><span data-stu-id="030f8-115">/s</span></span>   | <span data-ttu-id="030f8-116">Especifica o nome do arquivo do esquema de manifesto no qual validar os manifestos.</span><span class="sxs-lookup"><span data-stu-id="030f8-116">Specifies the manifest schema file name to validate manifests against.</span></span> <span data-ttu-id="030f8-117">Consulte o esquema no [esquema do arquivo de manifesto](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="030f8-117">See the schema at [Manifest File Schema](manifest-file-schema.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="030f8-118">/m</span><span class="sxs-lookup"><span data-stu-id="030f8-118">/m</span></span>   | <span data-ttu-id="030f8-119">Especifica o nome do arquivo de manifesto a ser validado.</span><span class="sxs-lookup"><span data-stu-id="030f8-119">Specifies the manifest file name to validate.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="030f8-120">/q</span><span class="sxs-lookup"><span data-stu-id="030f8-120">/q</span></span>   | <span data-ttu-id="030f8-121">Suprime toda a saída para o console.</span><span class="sxs-lookup"><span data-stu-id="030f8-121">Suppresses all output to the console.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="030f8-122">/t</span><span class="sxs-lookup"><span data-stu-id="030f8-122">/t</span></span>   | <span data-ttu-id="030f8-123">Especifica o tipo de arquivo de manifesto.</span><span class="sxs-lookup"><span data-stu-id="030f8-123">Specifies the type of manifest file.</span></span> <span data-ttu-id="030f8-124">Os valores válidos são: é validar o [esquema do arquivo de manifesto](manifest-file-schema.md) de um [manifesto do assembly](assembly-manifests.md) ou do [manifesto do aplicativo](application-manifests.md)</span><span class="sxs-lookup"><span data-stu-id="030f8-124">The valid values are: AM   Validate the [manifest file schema](manifest-file-schema.md) of an [assembly manifest](assembly-manifests.md) or [application manifest](application-manifests.md)</span></span><br/> <span data-ttu-id="030f8-125">PC valida o [esquema do arquivo de configuração do Publicador](publisher-configuration-file-schema.md) de um [arquivo de configuração do Publicador](publisher-configuration-files.md)</span><span class="sxs-lookup"><span data-stu-id="030f8-125">PC   Validate the [publisher configuration file schema](publisher-configuration-file-schema.md) of a [publisher configuration file](publisher-configuration-files.md)</span></span><br/> <span data-ttu-id="030f8-126">AC valide o esquema do arquivo de configuração de aplicativo de um [arquivo de configuração de aplicativo](application-configuration-files.md).</span><span class="sxs-lookup"><span data-stu-id="030f8-126">AC   Validate the application configuration file schema of an [application configuration file](application-configuration-files.md).</span></span><br/> |



 

<span data-ttu-id="030f8-127">Se o sinalizador/q não for especificado, Manifestchk.vbs exibirá informações detalhadas sobre o primeiro erro encontrado no arquivo e exibirá uma mensagem informando se o processo de validação foi bem-sucedido ou não.</span><span class="sxs-lookup"><span data-stu-id="030f8-127">If the /q flag is not specified, Manifestchk.vbs displays detailed information about the first error encountered in the file, and displays a message stating whether the validation process was successful or not.</span></span>

<span data-ttu-id="030f8-128">Este utilitário verifica o seguinte:</span><span class="sxs-lookup"><span data-stu-id="030f8-128">This utility checks for the following:</span></span>

-   <span data-ttu-id="030f8-129">Uma linha de comando válida.</span><span class="sxs-lookup"><span data-stu-id="030f8-129">A valid command line.</span></span>
-   <span data-ttu-id="030f8-130">A versão 3 do MSXML está instalada.</span><span class="sxs-lookup"><span data-stu-id="030f8-130">That MSXML version 3 is installed.</span></span>
-   <span data-ttu-id="030f8-131">Se o manifesto usa XML bem formado.</span><span class="sxs-lookup"><span data-stu-id="030f8-131">That the manifest uses well-formed XML.</span></span>
-   <span data-ttu-id="030f8-132">O manifesto concorda com o esquema fornecido.</span><span class="sxs-lookup"><span data-stu-id="030f8-132">That the manifest agrees with the provided schema.</span></span> <span data-ttu-id="030f8-133">Observe que Manifestchk.vbs verifica o arquivo de manifesto com base apenas no que é especificado no esquema fornecido.</span><span class="sxs-lookup"><span data-stu-id="030f8-133">Note that Manifestchk.vbs verifies the manifest file based only on what is specified in the provided schema.</span></span> <span data-ttu-id="030f8-134">Para obter um exemplo de um esquema de manifesto, consulte o [esquema do arquivo de manifesto](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="030f8-134">For an example of a manifest schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="030f8-135">Cscript.exe retornará um valor de 0 se o processo de validação tiver sido bem-sucedido e 1 se não tiver sido bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="030f8-135">Cscript.exe returns a value of 0 if the validation process was successful and 1 if it was not successful.</span></span> <span data-ttu-id="030f8-136">Ele retornará 2 se houver um erro em um argumento de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="030f8-136">It returns 2 if there is an error in a command line argument.</span></span>

## <a name="related-topics"></a><span data-ttu-id="030f8-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="030f8-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="030f8-138">Ferramentas de desenvolvimento lado a lado do assembly</span><span class="sxs-lookup"><span data-stu-id="030f8-138">Side-by-Side Assembly Development Tools</span></span>](side-by-side-assembly-development-tools.md)
</dt> </dl>

 

 




