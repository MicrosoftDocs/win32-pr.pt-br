---
description: O método recomendado para gerar um pacote de patch é usar ferramentas de criação de patch, como Msimsp.exe e Patchwiz.dll. A ferramenta de Msimsp.exe só está disponível nos componentes SDK do Windows para desenvolvedores de Windows Installer.
ms.assetid: fa8e9d68-3db1-4d17-aa99-2ca0ed421c7a
title: Msimsp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1810fd0c544695742273bbb0e63b22138529c129
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105759212"
---
# <a name="msimspexe"></a><span data-ttu-id="a8a3c-104">Msimsp.exe</span><span class="sxs-lookup"><span data-stu-id="a8a3c-104">Msimsp.exe</span></span>

<span data-ttu-id="a8a3c-105">O método recomendado para gerar um pacote de patch é usar ferramentas de criação de patch, como Msimsp.exe e [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="a8a3c-105">The recommended method for generating a patch package is to use patch creation tools such as Msimsp.exe and [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="a8a3c-106">A ferramenta de Msimsp.exe só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="a8a3c-106">The Msimsp.exe tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="a8a3c-107">Msimsp.exe é um arquivo executável que chama [Patchwiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="a8a3c-107">Msimsp.exe is a executable file that calls [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="a8a3c-108">A ferramenta pode ser usada para criar um pacote de patch passando o caminho para um arquivo de propriedades de criação de patch (arquivo. PCP) e o caminho para o pacote de patch que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-108">The tool can be used to create a patch package by passing in the path to a patch creation properties file (.pcp file) and the path to the patch package that is being created.</span></span> <span data-ttu-id="a8a3c-109">Msimsp. ex também pode ser usado para criar um arquivo de log e especificar uma pasta temporária na qual as transformações, os gabinetes e os arquivos usados para criar o pacote de patch são salvos.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-109">Msimsp.ex can also be used to create a log file and to specify a temporary folder in which the transforms, cabinets, and files that are used to create the patch package are saved.</span></span>

<span data-ttu-id="a8a3c-110">A sintaxe de linha de comando para Msimsp.exe é:</span><span class="sxs-lookup"><span data-stu-id="a8a3c-110">The command-line syntax for Msimsp.exe is:</span></span>

<span data-ttu-id="a8a3c-111">Caminho do **Msimsp.exe-s** *\[ para o arquivo \] . PCP* **-p** *\[ caminho para o \] arquivo. msp* **{Options}**</span><span class="sxs-lookup"><span data-stu-id="a8a3c-111">**Msimsp.exe -s** *\[path to .pcp file\]* **-p** *\[path to .msp file\]* **{options}**</span></span>

<span data-ttu-id="a8a3c-112">As opções de linha de comando não diferenciam maiúsculas de minúsculas e os delimitadores de barra podem ser usados em vez de um traço.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-112">The command-line options are not case-sensitive, and slash delimiters can be used instead of a dash.</span></span> <span data-ttu-id="a8a3c-113">Se nenhuma opção for especificada, Msimsp.exe exibirá os valores atuais das propriedades de informações de resumo.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-113">If no options are specified, Msimsp.exe displays the current values of the summary Information properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8a3c-114"><span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[ caminho para o arquivo \] . PCP_</span><span class="sxs-lookup"><span data-stu-id="a8a3c-114"><span id="-s_path_to_.pcp_file_"></span><span id="-S_PATH_TO_.PCP_FILE_"></span>**-s**_\[path to .pcp file\]_</span></span>
</dt> <dd>

<span data-ttu-id="a8a3c-115">Isso é necessário e deve ser seguido pelo caminho para o arquivo de propriedades de criação de patch (extensão. PCP).</span><span class="sxs-lookup"><span data-stu-id="a8a3c-115">This is required and must be followed by the path to the patch creation properties file (.pcp extension).</span></span> <span data-ttu-id="a8a3c-116">Para obter mais informações, consulte [PatchWiz.dll](patchwiz-dll.md).</span><span class="sxs-lookup"><span data-stu-id="a8a3c-116">For more information, see [PatchWiz.dll](patchwiz-dll.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8a3c-117"><span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_caminho para o arquivo. msp_</span><span class="sxs-lookup"><span data-stu-id="a8a3c-117"><span id="-ppath_to_.msp_file"></span><span id="-PPATH_TO_.MSP_FILE"></span>**-p**_path to .msp file_</span></span>
</dt> <dd>

<span data-ttu-id="a8a3c-118">Isso é necessário e seguido pelo caminho para o pacote de patches que está sendo criado (extensão. msp).</span><span class="sxs-lookup"><span data-stu-id="a8a3c-118">This is required and followed by the path to patch package that is being created (.msp extension).</span></span>

</dd> <dt>

<span data-ttu-id="a8a3c-119"><span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_caminho para a pasta temporária_</span><span class="sxs-lookup"><span data-stu-id="a8a3c-119"><span id="-fpath_to_temporary_folder"></span><span id="-FPATH_TO_TEMPORARY_FOLDER"></span>**-f**_path to temporary folder_</span></span>
</dt> <dd>

<span data-ttu-id="a8a3c-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-120">Optional.</span></span> <span data-ttu-id="a8a3c-121">Seguido pelo caminho para a pasta temporária.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-121">Followed by path to temporary folder.</span></span> <span data-ttu-id="a8a3c-122">O local padrão é% TMP% \\ ~ PCW \_ tmp. tmp \\ .</span><span class="sxs-lookup"><span data-stu-id="a8a3c-122">The default location is %TMP%\\~pcw\_tmp.tmp\\.</span></span>

</dd> <dt>

<span data-ttu-id="a8a3c-123"><span id="-k"></span><span id="-K"></span>**-k**</span><span class="sxs-lookup"><span data-stu-id="a8a3c-123"><span id="-k"></span><span id="-K"></span>**-k**</span></span>
</dt> <dd>

<span data-ttu-id="a8a3c-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-124">Optional.</span></span> <span data-ttu-id="a8a3c-125">Falha se a pasta temporária já existir.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-125">Fail if the temporary folder already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a8a3c-126"><span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_caminho para o arquivo de log_</span><span class="sxs-lookup"><span data-stu-id="a8a3c-126"><span id="-lpath_to_log_file"></span><span id="-LPATH_TO_LOG_FILE"></span>**-l**_path to log file_</span></span>
</dt> <dd>

<span data-ttu-id="a8a3c-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-127">Optional.</span></span> <span data-ttu-id="a8a3c-128">Seguido pelo caminho para o arquivo de log que descreve o processo e os erros de criação de patch.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-128">Followed by the path to the log file that describes the patch creation process and errors.</span></span> <span data-ttu-id="a8a3c-129">Para obter mais informações, consulte [valores de retorno para UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span><span class="sxs-lookup"><span data-stu-id="a8a3c-129">For more information, see [Return Values for UiCreatePatchPackage](return-values-for-uicreatepatchpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8a3c-130"><span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-caminho LP**_para arquivo de log com dados de desempenho_</span><span class="sxs-lookup"><span data-stu-id="a8a3c-130"><span id="-lppath_to_log_file_with_performance_data"></span><span id="-LPPATH_TO_LOG_FILE_WITH_PERFORMANCE_DATA"></span>**-lp**_path to log file with performance data_</span></span>
</dt> <dd>

<span data-ttu-id="a8a3c-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-131">Optional.</span></span> <span data-ttu-id="a8a3c-132">Seguido pelo caminho para o arquivo de log que descreve o processo e os erros de criação de patch.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-132">Followed by the path to the log file that describes the patch creation process and errors.</span></span> <span data-ttu-id="a8a3c-133">Essa opção grava dados de desempenho no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-133">This option writes performance data to log file.</span></span> <span data-ttu-id="a8a3c-134">Esta opção requer a versão 4,0 de Patchwiz.dll.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-134">This option requires version 4.0 of Patchwiz.dll.</span></span>

</dd> <dt>

<span data-ttu-id="a8a3c-135"><span id="-d"></span><span id="-D"></span>**-d**</span><span class="sxs-lookup"><span data-stu-id="a8a3c-135"><span id="-d"></span><span id="-D"></span>**-d**</span></span>
</dt> <dd>

<span data-ttu-id="a8a3c-136">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-136">Optional.</span></span> <span data-ttu-id="a8a3c-137">Exibe uma caixa de diálogo se a criação do patch for concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-137">Displays a dialog if the patch creation completes successfully.</span></span>

</dd> <dt>

<span data-ttu-id="a8a3c-138"><span id="-_"></span>**-?**</span><span class="sxs-lookup"><span data-stu-id="a8a3c-138"><span id="-_"></span>**-?**</span></span>
</dt> <dd>

<span data-ttu-id="a8a3c-139">Exibe a ajuda de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-139">Displays command-line help.</span></span>

</dd> </dl>

> [!Note]
> <span data-ttu-id="a8a3c-140">Msimsp.exe pode falhar ao chamar Makecab.exe se houver valores na coluna arquivo da [tabela de arquivos](file-table.md) do pacote de instalação que diferem apenas por maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-140">Msimsp.exe can fail when it calls Makecab.exe if there are values in the File column of the [File table](file-table.md) of the installation package that differ only by case.</span></span> <span data-ttu-id="a8a3c-141">Windows Installer diferencia maiúsculas de minúsculas e permite um pacote de instalação, como na tabela a seguir, somente quando comp1 e Comp2 são instalados em diretórios diferentes.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-141">Windows Installer is case-sensitive and allows an installation package such as in the table below only when Comp1 and Comp2 are installed into different directories.</span></span> <span data-ttu-id="a8a3c-142">No entanto, nesse cenário, você não pode usar Msimsp.exe ou [Patchwiz.dll](patchwiz-dll.md) para gerar um patch para o pacote, pois Msimsp.exe e Patchwiz.dll chamada Makecab.exe, que não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-142">However, in this scenario you cannot use Msimsp.exe or [Patchwiz.dll](patchwiz-dll.md) to generate a patch for the package, because Msimsp.exe and Patchwiz.dll call Makecab.exe, which is case-insensitive.</span></span>
> 
> <span data-ttu-id="a8a3c-143">Evite criar um pacote de instalação, como a seguinte [tabela de arquivos](file-table.md)parcial.</span><span class="sxs-lookup"><span data-stu-id="a8a3c-143">Avoid authoring an installation package such as the following partial [File table](file-table.md).</span></span>
> 
> | <span data-ttu-id="a8a3c-144">Arquivo</span><span class="sxs-lookup"><span data-stu-id="a8a3c-144">File</span></span>       | <span data-ttu-id="a8a3c-145">Componente\_</span><span class="sxs-lookup"><span data-stu-id="a8a3c-145">Component\_</span></span> | <span data-ttu-id="a8a3c-146">FileName</span><span class="sxs-lookup"><span data-stu-id="a8a3c-146">FileName</span></span>   |
> |------------|-------------|------------|
> | <span data-ttu-id="a8a3c-147">readme.txt</span><span class="sxs-lookup"><span data-stu-id="a8a3c-147">readme.txt</span></span> | <span data-ttu-id="a8a3c-148">Comp1</span><span class="sxs-lookup"><span data-stu-id="a8a3c-148">Comp1</span></span>       | <span data-ttu-id="a8a3c-149">readme.txt</span><span class="sxs-lookup"><span data-stu-id="a8a3c-149">readme.txt</span></span> |
> | <span data-ttu-id="a8a3c-150">ReadMe.txt</span><span class="sxs-lookup"><span data-stu-id="a8a3c-150">ReadMe.txt</span></span> | <span data-ttu-id="a8a3c-151">Comp2</span><span class="sxs-lookup"><span data-stu-id="a8a3c-151">Comp2</span></span>       | <span data-ttu-id="a8a3c-152">readme.txt</span><span class="sxs-lookup"><span data-stu-id="a8a3c-152">readme.txt</span></span> |


## <a name="related-topics"></a><span data-ttu-id="a8a3c-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8a3c-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8a3c-154">Criando um pacote de patch</span><span class="sxs-lookup"><span data-stu-id="a8a3c-154">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> <dt>

[<span data-ttu-id="a8a3c-155">Um exemplo de aplicação de patch de atualização pequena</span><span class="sxs-lookup"><span data-stu-id="a8a3c-155">A Small Update Patching Example</span></span>](a-small-update-patching-example.md)
</dt> <dt>

[<span data-ttu-id="a8a3c-156">Ferramentas de desenvolvimento Windows Installer</span><span class="sxs-lookup"><span data-stu-id="a8a3c-156">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="a8a3c-157">Versões, ferramentas e redistribuíveis liberados</span><span class="sxs-lookup"><span data-stu-id="a8a3c-157">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



