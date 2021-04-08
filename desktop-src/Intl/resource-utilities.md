---
description: Este tópico descreve dois utilitários usados para criar aplicativos MUI.
ms.assetid: 8ba94001-fc46-41e0-a071-0dc500a20753
title: Utilitários de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550cf283779a57bc5ca35f88d336646b061c3f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922335"
---
# <a name="resource-utilities"></a><span data-ttu-id="2eab8-103">Utilitários de recursos</span><span class="sxs-lookup"><span data-stu-id="2eab8-103">Resource Utilities</span></span>

<span data-ttu-id="2eab8-104">Este tópico descreve dois utilitários usados para criar aplicativos MUI.</span><span class="sxs-lookup"><span data-stu-id="2eab8-104">This topic describes two utilities used to build MUI applications.</span></span> <span data-ttu-id="2eab8-105">Embora o MUIRCT seja uma ferramenta específica de MUI, o MUI também utiliza o utilitário de compilador padrão do Windows RC.</span><span class="sxs-lookup"><span data-stu-id="2eab8-105">While MUIRCT is a MUI-specific tool, MUI also makes use of the standard Windows RC Compiler utility.</span></span> <span data-ttu-id="2eab8-106">As instruções para usar esses utilitários são fornecidas em [localizando recursos e compilando o aplicativo](localizing-resources-and-building-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="2eab8-106">Instructions for using these utilities are provided in [Localizing Resources and Building the Application](localizing-resources-and-building-the-application.md).</span></span>

## <a name="muirct-utility"></a><span data-ttu-id="2eab8-107">Utilitário MUIRCT</span><span class="sxs-lookup"><span data-stu-id="2eab8-107">MUIRCT Utility</span></span>

<span data-ttu-id="2eab8-108">MUIRCT (Muirct.exe) é um utilitário de linha de comando para dividir um arquivo executável padrão em um arquivo LN e arquivos de recurso específicos a um idioma (ou seja, localizável).</span><span class="sxs-lookup"><span data-stu-id="2eab8-108">MUIRCT (Muirct.exe) is a command line utility for splitting a standard executable file into an LN file and language-specific (that is, localizable) resource files.</span></span> <span data-ttu-id="2eab8-109">Cada um dos arquivos resultantes contém dados de configuração de recursos para a associação de arquivos.</span><span class="sxs-lookup"><span data-stu-id="2eab8-109">Each of the resulting files contains resource configuration data for file association.</span></span> <span data-ttu-id="2eab8-110">O MUIRCT está incluído no SDK do Microsoft Windows para o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2eab8-110">MUIRCT is included in the Microsoft Windows SDK for Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="2eab8-111">A partir do Windows Vista, o carregador de recursos do Win32 é atualizado para carregar recursos de arquivos específicos do idioma, bem como de arquivos LN.</span><span class="sxs-lookup"><span data-stu-id="2eab8-111">Starting with Windows Vista, the Win32 resource loader is updated to load resources from language-specific files as well as from LN files.</span></span>

 

### <a name="muirct-usages"></a><span data-ttu-id="2eab8-112">Usos de MUIRCT</span><span class="sxs-lookup"><span data-stu-id="2eab8-112">MUIRCT Usages</span></span>

1.  <span data-ttu-id="2eab8-113">Dividir Binary em arquivo binário principal e mui com base no \_ arquivo de configuração RC.</span><span class="sxs-lookup"><span data-stu-id="2eab8-113">Split binary into main binary and mui file based on rc\_config file.</span></span>

    `Muirct -q rc_config [-c checksum_file [-b LangID]] [-x LangID] [-g LangId]     [-f] [-m] [-v level] source_file [output_LN_file] [output_MUI_file]`

2.  <span data-ttu-id="2eab8-114">Extrair soma de verificação do arquivo de soma de verificação \_ e inseri-la no arquivo de saída \_ .</span><span class="sxs-lookup"><span data-stu-id="2eab8-114">Extract checksum from checksum\_file and insert it in output\_file.</span></span>

    `Muirct -c checksum_file [-b LangID] -e output_file`

3.  <span data-ttu-id="2eab8-115">Calcule soma de verificação com base no arquivo de soma de verificação \_ e insira-a no arquivo de saída \_ .</span><span class="sxs-lookup"><span data-stu-id="2eab8-115">Calculate checksum based on checksum\_file and insert it in output\_file.</span></span>

    `Muirct  -c checksum_file [-b LangID] -q rc_config  -z output_file`

4.  <span data-ttu-id="2eab8-116">Despeja o conteúdo dos dados de configuração do recurso do arquivo de entrada \_ .</span><span class="sxs-lookup"><span data-stu-id="2eab8-116">Dump resource configuration data contents from input\_file.</span></span>

    `Muirct -d input_file`

### <a name="muirct-syntax"></a><span data-ttu-id="2eab8-117">Sintaxe de MUIRCT</span><span class="sxs-lookup"><span data-stu-id="2eab8-117">MUIRCT Syntax</span></span>

<span data-ttu-id="2eab8-118">MUIRCT pode tomar a direção das opções de linha de comando e/ou de um arquivo de configuração de recurso, especificado usando a opção-q.</span><span class="sxs-lookup"><span data-stu-id="2eab8-118">MUIRCT can take direction from command line switches and/or from a resource configuration file, specified using the -q switch.</span></span>


```C++
muirct [-h|-?] [ -c checksum_file] [-b langid]  ]
     [-g langid] [-q resource configuration file<RCF>] [-v level] [-x langid]
     [-e output_file]  [-z output_file] [-f] [-d MUI'ized file] [-m file_version]

source_filename [language_neutral_filename] [mui_filename]
```



<span data-ttu-id="2eab8-119">**Opções e argumentos**</span><span class="sxs-lookup"><span data-stu-id="2eab8-119">**Switches and Arguments**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2eab8-120">-h |-?</span><span class="sxs-lookup"><span data-stu-id="2eab8-120">-h|-?</span></span></td>
<td><span data-ttu-id="2eab8-121">Mostra a tela de ajuda.</span><span class="sxs-lookup"><span data-stu-id="2eab8-121">Shows help screen.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2eab8-122">-c</span><span class="sxs-lookup"><span data-stu-id="2eab8-122">-c</span></span></td>
<td><span data-ttu-id="2eab8-123">Especifica o checksum_file de entrada do qual extrair ou calcular a soma de verificação do recurso.</span><span class="sxs-lookup"><span data-stu-id="2eab8-123">Specifies the input checksum_file from which to extract or calculate the resource checksum.</span></span> <span data-ttu-id="2eab8-124">Checksum_file deve ser um arquivo binário Win32 contendo recursos localizáveis.</span><span class="sxs-lookup"><span data-stu-id="2eab8-124">Checksum_file must be a Win32 binary file containing localizable resources.</span></span> <span data-ttu-id="2eab8-125">Se checksum_file contiver recursos para mais de um idioma, a opção-b deverá ser usada para especificar quais deles devem ser usados caso contrário, MUIRCT falhará.</span><span class="sxs-lookup"><span data-stu-id="2eab8-125">If checksum_file contains resources for more than one language, the -b switch must be used to specify which of these should be used otherwise MUIRCT fails.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2eab8-126">-b</span><span class="sxs-lookup"><span data-stu-id="2eab8-126">-b</span></span></td>
<td><span data-ttu-id="2eab8-127">Especifica o idioma a ser usado quando o checksum_file especificado com-c contém recursos em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="2eab8-127">Specifies the language to be used when the checksum_file specified with -c contains resources in multiple languages.</span></span> <span data-ttu-id="2eab8-128">Essa opção só pode ser usada em conjunto com a opção-c.</span><span class="sxs-lookup"><span data-stu-id="2eab8-128">This switch can only be used in conjunction with the -c switch.</span></span> <span data-ttu-id="2eab8-129">O identificador de idioma pode estar no formato decimal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="2eab8-129">The language identifier can be in decimal or hexadecimal format.</span></span> <span data-ttu-id="2eab8-130">MUIRCT falhará se o checksum_file contiver recursos em vários idiomas e-b não for especificado ou se o idioma especificado pela opção-b não puder ser encontrado no checksum_file.</span><span class="sxs-lookup"><span data-stu-id="2eab8-130">MUIRCT fails if the checksum_file contains resources in multiple language and the -b is not specified or if the language specified by the -b switch cannot be found in the checksum_file.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2eab8-131">-g</span><span class="sxs-lookup"><span data-stu-id="2eab8-131">-g</span></span></td>
<td><span data-ttu-id="2eab8-132">Especifica a ID de idioma a ser incluída como o idioma de fallback final na seção de dados de configuração de recurso do arquivo LN.</span><span class="sxs-lookup"><span data-stu-id="2eab8-132">Specifies the language ID to be included as the ultimate fallback language in the resource configuration data section of the LN file.</span></span> <span data-ttu-id="2eab8-133">Se o carregador de recursos não carregar um arquivo. mui solicitado dos idiomas de interface do usuário preferenciais do thread, ele usará o idioma de fallback final como sua última tentativa.</span><span class="sxs-lookup"><span data-stu-id="2eab8-133">If the resource loader fails to load a requested .mui file from the thread preferred UI languages, it uses the ultimate fallback language as its last attempt.</span></span> <span data-ttu-id="2eab8-134">O valor de LangID pode ser especificado em formato decimal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="2eab8-134">The LangID value can be specified in decimal or hexadecimal format.</span></span> <span data-ttu-id="2eab8-135">Por exemplo, inglês (Estados Unidos) pode ser especificado por-g 0x409 ou-g 1033.</span><span class="sxs-lookup"><span data-stu-id="2eab8-135">For example English (United States) can be specified by -g 0x409 or -g 1033.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2eab8-136">-Q</span><span class="sxs-lookup"><span data-stu-id="2eab8-136">-q</span></span></td>
<td><span data-ttu-id="2eab8-137">Especifica que o source_file deve ser dividido no output_LN_file e o output_MUI_file de acordo com o layout do arquivo de rc_config.</span><span class="sxs-lookup"><span data-stu-id="2eab8-137">Specifies that the source_file is to be split into the output_LN_file and the output_MUI_file according to the rc_config file layout.</span></span> <span data-ttu-id="2eab8-138">O arquivo de rc_config é um arquivo formatado XML que especifica quais recursos serão extraídos para o arquivo. mui e que serão deixados no arquivo LN.</span><span class="sxs-lookup"><span data-stu-id="2eab8-138">The rc_config file is an XML formatted file that specifies which resources will be extracted to the .mui file and which will be left in the LN file.</span></span> <span data-ttu-id="2eab8-139">O rc_config pode especificar a distribuição de tipos de recursos e itens nomeados individuais entre o output_LN_file e output_MUI_file.</span><span class="sxs-lookup"><span data-stu-id="2eab8-139">The rc_config can specify the distribution of resource types and individual named items between the output_LN_file and output_MUI_file.</span></span> <span data-ttu-id="2eab8-140">O source_file deve ser um binário do Win32 que contém recursos em um único idioma, caso contrário, o MUIRCT falhará.</span><span class="sxs-lookup"><span data-stu-id="2eab8-140">The source_file must be a Win32 binary that contains resources in a single language otherwise MUIRCT fails.</span></span> <span data-ttu-id="2eab8-141">MUIRCT não dividirá o arquivo se for um idioma neutro, que é indicado por ter apenas o valor de ID de idioma 0 no arquivo.</span><span class="sxs-lookup"><span data-stu-id="2eab8-141">MUIRCT does not split the file if it is language neutral which is indicated by having only language ID value 0 in the file.</span></span> <span data-ttu-id="2eab8-142">O output_LN_file e output_mui_file são os nomes do arquivo de idioma neutro e. mui no qual o source_file é dividido.</span><span class="sxs-lookup"><span data-stu-id="2eab8-142">The output_LN_file and output_mui_file are the names of the language neutral and .mui file into which the source_file is split.</span></span> <span data-ttu-id="2eab8-143">Esses nomes de arquivo são opcionais.</span><span class="sxs-lookup"><span data-stu-id="2eab8-143">These file names are optional.</span></span> <span data-ttu-id="2eab8-144">Se eles não forem especificados, o MUIRCT acrescentará as extensões. ln e. mui a source_file.</span><span class="sxs-lookup"><span data-stu-id="2eab8-144">If they are not specified, MUIRCT appends the extensions .ln and .mui to source_file.</span></span> <span data-ttu-id="2eab8-145">Normalmente, você deve remover a &quot; extensão. ln &quot; antes de implantar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="2eab8-145">Typically you should remove the &quot;.ln&quot; extension before deploying the file.</span></span> <span data-ttu-id="2eab8-146">MUIRCT associa a output_LN_file e output_MUI_file calculando uma soma de verificação com base no nome do source_file e na versão do arquivo e inserindo o resultado na seção de configuração do recurso de cada arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="2eab8-146">MUIRCT associates the output_LN_file and output_MUI_file by calculating a checksum based on the source_file name and file version and inserting the result into the resource configuration section of each output file.</span></span> <span data-ttu-id="2eab8-147">Quando usado em conjunto com a opção-c, a opção-q tem precedência.</span><span class="sxs-lookup"><span data-stu-id="2eab8-147">When used in conjunction with the -c switch, the -q switch takes precedence.</span></span> <span data-ttu-id="2eab8-148">Se o arquivo de rc_config fornecido com a opção-q contiver uma soma de verificação, MUIRCT ignorará a opção-c e inserirá o valor da soma de verificação do valor, rc_config arquivo nos arquivos LN e. mui.</span><span class="sxs-lookup"><span data-stu-id="2eab8-148">If the rc_config file supplied with the -q switch contains a checksum MUIRCT ignores the -c switch and inserts the checksum value from the value, rc_config file into the LN and.mui files.</span></span> <span data-ttu-id="2eab8-149">Se nenhum valor de soma de verificação for encontrado no rc_config, MUIRCT calculará a soma de verificação do recurso com base no comportamento da opção-c.</span><span class="sxs-lookup"><span data-stu-id="2eab8-149">If no checksum value is found in the rc_config, MUIRCT calculates the resource checksum based on the behavior of the -c switch.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2eab8-150">-v</span><span class="sxs-lookup"><span data-stu-id="2eab8-150">-v</span></span></td>
<td><span data-ttu-id="2eab8-151">Especifica o nível de detalhamento para registro em log.</span><span class="sxs-lookup"><span data-stu-id="2eab8-151">Specifies the level of verboseness for logging.</span></span> <span data-ttu-id="2eab8-152">Especifique 1 para imprimir todas as mensagens de erro e os resultados de operação básicos.</span><span class="sxs-lookup"><span data-stu-id="2eab8-152">Specify 1 to print all basic error messages and operation results.</span></span> <span data-ttu-id="2eab8-153">Especifique 2 para incluir também as informações de recurso (tipo, nome, identificador de idioma) incluídas no arquivo. mui e no arquivo LN.</span><span class="sxs-lookup"><span data-stu-id="2eab8-153">Specify 2 to also include the resource information (type, name, language identifier) included in the .mui file and LN file.</span></span> <span data-ttu-id="2eab8-154">O padrão é-v 1</span><span class="sxs-lookup"><span data-stu-id="2eab8-154">The default is -v 1</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2eab8-155">-X</span><span class="sxs-lookup"><span data-stu-id="2eab8-155">-x</span></span></td>
<td><span data-ttu-id="2eab8-156">Especifica a ID de idioma com a qual MUIRCT marca todos os tipos de recursos adicionados à seção de recursos do arquivo. mui.</span><span class="sxs-lookup"><span data-stu-id="2eab8-156">Specifies the language ID with which MUIRCT marks all resource types added to the resource section of the .mui file.</span></span> <span data-ttu-id="2eab8-157">O valor de LangID pode ser especificado em formato decimal ou hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="2eab8-157">The LangID value can be specified in decimal or hexadecimal format.</span></span> <span data-ttu-id="2eab8-158">Por exemplo, inglês (Estados Unidos) pode ser especificado por-x 0x409 ou-x 1033.</span><span class="sxs-lookup"><span data-stu-id="2eab8-158">For example English (United States) can be specified by -x 0x409 or -x 1033.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2eab8-159">-E</span><span class="sxs-lookup"><span data-stu-id="2eab8-159">-e</span></span></td>
<td><span data-ttu-id="2eab8-160">Extrai a soma de verificação de recurso contida na checksum_file fornecida com a opção-c e a insere no output_file especificado.</span><span class="sxs-lookup"><span data-stu-id="2eab8-160">Extracts the resource checksum contained in the checksum_file provided with the -c switch and inserts it in the specified output_file.</span></span> <span data-ttu-id="2eab8-161">Quando-e é especificado, o MUIRCT ignora todas as opções diferentes da opção-c.</span><span class="sxs-lookup"><span data-stu-id="2eab8-161">When -e is specified, MUIRCT ignores all switches other than the -c switch.</span></span> <span data-ttu-id="2eab8-162">Nesse caso, o checksum_file deve ser um arquivo binário Win32 que contém uma seção de dados de configuração de recurso com um valor de soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="2eab8-162">In this case the checksum_file must be a Win32 binary file that contains a resource configuration data section with a checksum value.</span></span> <span data-ttu-id="2eab8-163">O output_file deve ser um arquivo LN ou. mui existente.</span><span class="sxs-lookup"><span data-stu-id="2eab8-163">The output_file must be an existing LN file or .mui file.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2eab8-164">-Z</span><span class="sxs-lookup"><span data-stu-id="2eab8-164">-z</span></span></td>
<td><span data-ttu-id="2eab8-165">Calcula e insere os dados de soma de verificação do recurso no arquivo de saída especificado.</span><span class="sxs-lookup"><span data-stu-id="2eab8-165">Calculates and inserts resource checksum data in the specified output file.</span></span> <span data-ttu-id="2eab8-166">MUIRCT baseia o cálculo da soma de verificação na entrada fornecida com a opção-c e a opção-b opcional.</span><span class="sxs-lookup"><span data-stu-id="2eab8-166">MUIRCT bases checksum calculation on the input provided with the -c switch, and the optional -b switch.</span></span> <span data-ttu-id="2eab8-167">Se você especificar um arquivo de saída para a opção-z que não existe, o MUIRCT será fechado com uma falha.</span><span class="sxs-lookup"><span data-stu-id="2eab8-167">If you specify an output file for the -z switch that does not exist, MUIRCT exits with a failure.</span></span><br/> <span data-ttu-id="2eab8-168">Exemplo: calcula a soma de verificação com base em recursos localizáveis em Notepad.exe e insere a soma de verificação no arquivo de saída Notepad2.exe.</span><span class="sxs-lookup"><span data-stu-id="2eab8-168">Example: Calculates the checksum based on localizable resources in Notepad.exe and inserts the checksum into the output file Notepad2.exe.</span></span><br/> <code>muirct -c notepad.exe -q myprog.rcconfig -z notepad2.exe</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2eab8-169">-f</span><span class="sxs-lookup"><span data-stu-id="2eab8-169">-f</span></span></td>
<td><span data-ttu-id="2eab8-170">Habilita a criação de um arquivo. mui com o recurso de versão que é o único recurso localizável.</span><span class="sxs-lookup"><span data-stu-id="2eab8-170">Enables creating a .mui file with the version resource being the only localizable resource.</span></span> <span data-ttu-id="2eab8-171">Por padrão, o MUIRCT não permite isso.</span><span class="sxs-lookup"><span data-stu-id="2eab8-171">By default, MUIRCT does not allow this.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2eab8-172">-d</span><span class="sxs-lookup"><span data-stu-id="2eab8-172">-d</span></span></td>
<td><span data-ttu-id="2eab8-173">Localiza e exibe dados de configuração de recursos inseridos no arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="2eab8-173">Locates and displays embedded resource configuration data in the source file.</span></span> <span data-ttu-id="2eab8-174">Quando você especifica essa opção, o MUIRCT ignora todas as outras opções de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="2eab8-174">When you specify this switch, MUIRCT ignores all other command line options.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2eab8-175">-M</span><span class="sxs-lookup"><span data-stu-id="2eab8-175">-m</span></span></td>
<td><span data-ttu-id="2eab8-176">Especifica o número de versão a ser usado ao calcular a soma de verificação para associar o output_LN_file e output_MUI_file.</span><span class="sxs-lookup"><span data-stu-id="2eab8-176">Specifies the version number to use when calculating the checksum for associating the output_LN_file and output_MUI_file.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2eab8-177">source_filename</span><span class="sxs-lookup"><span data-stu-id="2eab8-177">source_filename</span></span></td>
<td><span data-ttu-id="2eab8-178">Nome do arquivo de origem binário localizado; caracteres curinga não podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="2eab8-178">Name of the localized binary source file; wildcards cannot be used.</span></span> <span data-ttu-id="2eab8-179">Este arquivo só pode conter recursos em um idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-179">This file can only contain resources in one language.</span></span> <span data-ttu-id="2eab8-180">Se houver recursos em vários idiomas no arquivo, MUIRCT falhará, a menos que a opção-b seja usada.</span><span class="sxs-lookup"><span data-stu-id="2eab8-180">If there are resources in multiple languages in the file, MUIRCT fails, unless the -b switch is used.</span></span> <span data-ttu-id="2eab8-181">Se o arquivo contiver recursos com identificadores de idioma com somente o valor 0, o MUIRCT não dividirá o arquivo porque um identificador de idioma 0 indica uma linguagem neutra.</span><span class="sxs-lookup"><span data-stu-id="2eab8-181">If the file contains resources with language identifiers having value 0 only, MUIRCT does not split the file because a language identifier of 0 indicates a neutral language.</span></span><br/> <span data-ttu-id="2eab8-182">Para a opção-d, source_filename é um arquivo LN ou um arquivo de recurso específico a um idioma para o qual MUIRCT é para exibir dados de configuração de recurso.</span><span class="sxs-lookup"><span data-stu-id="2eab8-182">For the -d switch, source_filename is either an LN file or a language-specific resource file for which MUIRCT is to display resource configuration data.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2eab8-183">language_neutral_filename</span><span class="sxs-lookup"><span data-stu-id="2eab8-183">language_neutral_filename</span></span></td>
<td><span data-ttu-id="2eab8-184">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2eab8-184">Optional.</span></span> <span data-ttu-id="2eab8-185">Nome do arquivo LN.</span><span class="sxs-lookup"><span data-stu-id="2eab8-185">Name of LN file.</span></span> <span data-ttu-id="2eab8-186">Se você não especificar o nome desse arquivo, o MUIRCT acrescentará uma segunda extensão &quot; . ln &quot; ao nome do arquivo de origem a ser usado como o nome do arquivo com neutralidade de idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-186">If you do not specify the name of this file, MUIRCT appends a second extension &quot;.ln&quot; to the source file name to use as the language-neutral file name.</span></span> <span data-ttu-id="2eab8-187">Normalmente, você deve remover a &quot; extensão. ln &quot; antes de implantar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="2eab8-187">Typically you should remove the &quot;.ln&quot; extension before deploying the file.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="2eab8-188">O arquivo LN não deve conter cadeias de caracteres ou menus.</span><span class="sxs-lookup"><span data-stu-id="2eab8-188">The LN file should not contain strings or menus.</span></span> <span data-ttu-id="2eab8-189">Você deve removê-los manualmente.</span><span class="sxs-lookup"><span data-stu-id="2eab8-189">You should remove them manually.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2eab8-190">mui_filename</span><span class="sxs-lookup"><span data-stu-id="2eab8-190">mui_filename</span></span></td>
<td><span data-ttu-id="2eab8-191">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2eab8-191">Optional.</span></span> <span data-ttu-id="2eab8-192">Nome do arquivo de recurso específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-192">Name of language-specific resource file.</span></span> <span data-ttu-id="2eab8-193">Se você não especificar um nome, o MUIRCT acrescentará uma segunda extensão &quot; . mui &quot; ao nome do arquivo de origem a ser usado como o nome do arquivo. Normalmente, o MUIRCT cria um arquivo de recursos específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-193">If you do not specify a name, MUIRCT appends a second extension &quot;.mui&quot; to the source file name to use as the file name.Normally, MUIRCT creates a language-specific resource file.</span></span> <span data-ttu-id="2eab8-194">No entanto, ele não cria um arquivo de recurso se alguma das seguintes condições existir:</span><span class="sxs-lookup"><span data-stu-id="2eab8-194">However, it does not create a resource file if any of the following conditions exist:</span></span><br/>
<ul>
<li><span data-ttu-id="2eab8-195">Não há recursos localizáveis no arquivo binário original.</span><span class="sxs-lookup"><span data-stu-id="2eab8-195">No localizable resources are in the original binary file.</span></span></li>
<li><span data-ttu-id="2eab8-196">O único idioma de recurso encontrado no arquivo binário original é o idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="2eab8-196">The only resource language found in the original binary file is the neutral language.</span></span></li>
<li><span data-ttu-id="2eab8-197">O arquivo binário original tem recursos para mais de um idioma, não contando a linguagem neutra.</span><span class="sxs-lookup"><span data-stu-id="2eab8-197">The original binary file has resources for more than one language, not counting the neutral language.</span></span> <span data-ttu-id="2eab8-198">Se o arquivo binário contiver recursos para dois idiomas, e um deles for o idioma neutro, o utilitário considerará o arquivo como multilíngue e criará um arquivo de recursos específico do idioma se houver recursos localizáveis.</span><span class="sxs-lookup"><span data-stu-id="2eab8-198">If the binary file contains resources for two languages, and one of them is the neutral language, the utility considers the file to be monolingual and creates a language-specific resource file if there are localizable resources.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="muirct-language-output"></a><span data-ttu-id="2eab8-199">Saída da linguagem MUIRCT</span><span class="sxs-lookup"><span data-stu-id="2eab8-199">MUIRCT Language Output</span></span>

<span data-ttu-id="2eab8-200">MUIRCT escolhe o valor do atributo "UltimateFallbackLanguage" para inserir nos dados de configuração de recursos do arquivo LN com base na seguinte ordem, da prioridade mais alta para a mais baixa:</span><span class="sxs-lookup"><span data-stu-id="2eab8-200">MUIRCT chooses the "UltimateFallbackLanguage" attribute value to insert in the LN file resource configuration data based on the following order, from highest priority to lowest:</span></span>

1.  <span data-ttu-id="2eab8-201">O atributo "UltimateFallbackLanguage" no arquivo de configuração de recurso de origem, se um for passado como entrada.</span><span class="sxs-lookup"><span data-stu-id="2eab8-201">"UltimateFallbackLanguage" attribute in the source resource configuration file, if one is passed in as input.</span></span>
2.  <span data-ttu-id="2eab8-202">O idioma especificado com a opção-g.</span><span class="sxs-lookup"><span data-stu-id="2eab8-202">The language specified with the -g switch.</span></span>
3.  <span data-ttu-id="2eab8-203">Idioma do arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="2eab8-203">Input file language.</span></span>

<span data-ttu-id="2eab8-204">MUIRCT escolhe o valor do atributo "Language" para inserir nos dados de configuração do recurso de arquivo. mui com base na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="2eab8-204">MUIRCT picks the "language" attribute value to insert in the .mui file resource configuration data based on the following order:</span></span>

1.  <span data-ttu-id="2eab8-205">atributo "Language" no arquivo de configuração de recurso de origem, se um for passado como entrada.</span><span class="sxs-lookup"><span data-stu-id="2eab8-205">"language" attribute in the source resource configuration file, if one is passed in as input.</span></span>
2.  <span data-ttu-id="2eab8-206">O idioma especificado pela opção-x (forçar idioma).</span><span class="sxs-lookup"><span data-stu-id="2eab8-206">The language specified by the -x switch (force language).</span></span>
3.  <span data-ttu-id="2eab8-207">Idioma do arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="2eab8-207">Input file language.</span></span>

### <a name="muirct-checksum-handling"></a><span data-ttu-id="2eab8-208">Manipulação de soma de verificação MUIRCT</span><span class="sxs-lookup"><span data-stu-id="2eab8-208">MUIRCT Checksum Handling</span></span>

<span data-ttu-id="2eab8-209">O sistema operacional normalmente calcula a soma de verificação sobre os recursos específicos do idioma em um arquivo, a menos que você especifique a soma de verificação por meio de um arquivo de configuração de recurso.</span><span class="sxs-lookup"><span data-stu-id="2eab8-209">The operating system normally calculates the checksum over the language-specific resources in a file unless you specify the checksum through a resource configuration file.</span></span> <span data-ttu-id="2eab8-210">Contanto que a soma de verificação seja a mesma para o arquivo LN e todos os arquivos de recursos específicos de idioma associados, e o atributo language na configuração de recurso no LN e a correspondência dependente de idioma, o carregador de recursos poderá carregar recursos com êxito.</span><span class="sxs-lookup"><span data-stu-id="2eab8-210">As long as the checksum is the same for the LN file and all associated language-specific resource files, and the language attribute in the resource configuration in the LN and language dependent match, the resource loader can successfully load resources.</span></span>

<span data-ttu-id="2eab8-211">O MUIRCT dá suporte a vários métodos para colocar as somas de verificação apropriadas nos dados de configuração do recurso:</span><span class="sxs-lookup"><span data-stu-id="2eab8-211">MUIRCT supports several methods for placing appropriate checksums in the resource configuration data:</span></span>

1.  <span data-ttu-id="2eab8-212">Crie um executável para cada idioma, contendo código e recursos.</span><span class="sxs-lookup"><span data-stu-id="2eab8-212">Build an executable for each language, containing both code and resources.</span></span> <span data-ttu-id="2eab8-213">Depois disso, use MUIRCT para dividir cada um desses arquivos em um arquivo LN e um arquivo de recurso específico a um idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-213">After this, use MUIRCT to split each of these files into an LN file and a language-specific resource file.</span></span> <span data-ttu-id="2eab8-214">MUIRCT é executado várias vezes, uma vez para gerar um arquivo de recurso para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-214">MUIRCT runs multiple times, once to generate a resource file for each language.</span></span> <span data-ttu-id="2eab8-215">Você pode executar a compilação das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="2eab8-215">You can perform the build in the following ways:</span></span>
    1.  <span data-ttu-id="2eab8-216">Use a opção-q para especificar um valor de soma de verificação no arquivo de configuração de recurso.</span><span class="sxs-lookup"><span data-stu-id="2eab8-216">Use the -q switch to specify a checksum value in the resource configuration file.</span></span> <span data-ttu-id="2eab8-217">MUIRCT coloca esse valor em todos os arquivos LN e arquivos de recursos específicos de idioma produzidos.</span><span class="sxs-lookup"><span data-stu-id="2eab8-217">MUIRCT places this value in all the LN files and language-specific resource files produced.</span></span> <span data-ttu-id="2eab8-218">Você precisa adotar uma estratégia para escolher esse valor, conforme descrito posteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="2eab8-218">You need to adopt a strategy for choosing this value, as described later in this topic.</span></span>
    2.  <span data-ttu-id="2eab8-219">Use a opção-c (e, opcionalmente, a opção-b) para escolher um único idioma com recursos dos quais o MUIRCT Extraia a soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="2eab8-219">Use the -c switch (and, optionally, the -b switch) to choose a single language having resources from which MUIRCT extracts the checksum.</span></span>
    3.  <span data-ttu-id="2eab8-220">Use a opção-z para escolher um único idioma com recursos dos quais o MUIRCT sempre extrai a soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="2eab8-220">Use the -z switch to choose a single language having resources from which MUIRCT always extracts the checksum.</span></span> <span data-ttu-id="2eab8-221">Aplique essa soma de verificação depois que os arquivos tiverem sido criados usando outros métodos.</span><span class="sxs-lookup"><span data-stu-id="2eab8-221">Apply this checksum after the files have been built using other methods.</span></span>
2.  <span data-ttu-id="2eab8-222">Crie um executável contendo código e recursos para uma única linguagem.</span><span class="sxs-lookup"><span data-stu-id="2eab8-222">Build an executable containing both code and resources for a single language.</span></span> <span data-ttu-id="2eab8-223">Depois disso, use MUIRCT para dividir os recursos entre o arquivo LN e o arquivo de recursos específicos do idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-223">After this, use MUIRCT to split the resources between the LN file and the language-specific resource file.</span></span> <span data-ttu-id="2eab8-224">Por fim, use uma ferramenta de localização binária para modificar o arquivo de recurso resultante para cada idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-224">Finally, use a binary localization tool to modify the resulting resource file for each language.</span></span>

<span data-ttu-id="2eab8-225">A Convenção mais comum para manipulação de soma de verificação é basear a soma de verificação nos recursos em inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="2eab8-225">The most common convention for checksum handling is to base the checksum on the English (United States) resources.</span></span> <span data-ttu-id="2eab8-226">Você tem a liberdade de adotar uma convenção diferente, desde que seja consistente para cada arquivo LN.</span><span class="sxs-lookup"><span data-stu-id="2eab8-226">You are free to adopt a different convention, as long as it is consistent for each LN file.</span></span> <span data-ttu-id="2eab8-227">Por exemplo, é perfeitamente aceitável que uma empresa de desenvolvimento de software baseie suas somas de verificação no software que ele cria em recursos franceses (França) em vez de recursos em inglês (Estados Unidos), desde que todos os aplicativos tenham recursos franceses (França) nos quais basear as somas de verificação.</span><span class="sxs-lookup"><span data-stu-id="2eab8-227">For example, it is perfectly acceptable for a software development enterprise to base its checksums in the software it builds on French (France) resources instead of English (United States) resources, as long as all the applications have French (France) resources on which to base the checksums.</span></span> <span data-ttu-id="2eab8-228">Também é aceitável usar o arquivo de configuração de recurso para atribuir um valor hexadecimal arbitrário de até 16 dígitos hexadecimais como uma soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="2eab8-228">It is also acceptable to use the resource configuration file to assign an arbitrary hexadecimal value of up to 16 hexadecimal digits as a checksum.</span></span> <span data-ttu-id="2eab8-229">Essa última estratégia impede o uso efetivo das opções-z,-c e-b de MUIRCT.</span><span class="sxs-lookup"><span data-stu-id="2eab8-229">This last strategy precludes the effective use of the -z, -c, and -b switches of MUIRCT.</span></span> <span data-ttu-id="2eab8-230">Ele requer a adoção de um método usando o [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) ou alguma outra ferramenta para gerar valores de soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="2eab8-230">It requires adoption of a method using either [**GuidGen**](/previous-versions/windows/embedded/ms924300(v=msdn.10)) or some other tool to generate checksum values.</span></span> <span data-ttu-id="2eab8-231">Essa estratégia também exige que você configure uma política para determinar quando modificar o valor ao adicionar novos recursos localizáveis.</span><span class="sxs-lookup"><span data-stu-id="2eab8-231">This strategy also requires you to set up a policy for determining when to modify the value when adding new localizable resources.</span></span>

<span data-ttu-id="2eab8-232">Para aplicar a soma de verificação em inglês (Estados Unidos) a todos os arquivos, você pode usar qualquer um dos métodos de manipulação de soma de verificação descritos acima.</span><span class="sxs-lookup"><span data-stu-id="2eab8-232">To apply the English (United States) checksum to all files, you can use any of the checksum handling methods described above.</span></span> <span data-ttu-id="2eab8-233">Por exemplo, você pode gerar o arquivo LN e o arquivo de recursos específicos do idioma para inglês (Estados Unidos) e, em seguida, usar a opção MUIRCT-d para obter a soma de verificação resultante.</span><span class="sxs-lookup"><span data-stu-id="2eab8-233">For example, you can generate the LN file and language-specific resource file for English (United States), then use the MUIRCT -d switch to obtain the resulting checksum.</span></span> <span data-ttu-id="2eab8-234">Você pode copiar essa soma de verificação em seu arquivo de configuração de recurso e usar a opção-q com MUIRCT para aplicar a soma de verificação a todos os outros arquivos.</span><span class="sxs-lookup"><span data-stu-id="2eab8-234">You can copy this checksum into your resource configuration file and use the -q switch with MUIRCT to apply the checksum to all other files.</span></span>

### <a name="use-of-a-resource-configuration-file-with-muirct"></a><span data-ttu-id="2eab8-235">Uso de um arquivo de configuração de recurso com MUIRCT</span><span class="sxs-lookup"><span data-stu-id="2eab8-235">Use of a Resource Configuration File with MUIRCT</span></span>

<span data-ttu-id="2eab8-236">Você pode especificar os dados de configuração do recurso ao usar o MUIRCT.</span><span class="sxs-lookup"><span data-stu-id="2eab8-236">You can specify resource configuration data when using MUIRCT.</span></span> <span data-ttu-id="2eab8-237">Se você fornecer ou não explicitamente um arquivo de configuração de recurso, cada arquivo de recurso específico de idioma tem dados de configuração de recursos, assim como qualquer arquivo LN com um arquivo de recurso associado.</span><span class="sxs-lookup"><span data-stu-id="2eab8-237">Whether or not you explicitly supply a resource configuration file, every language-specific resource file has resource configuration data, as does any LN file with an associated resource file.</span></span> <span data-ttu-id="2eab8-238">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="2eab8-238">For example:</span></span>

-   <span data-ttu-id="2eab8-239">Se você usar a opção-q para especificar um arquivo de configuração de recurso, mas não houver recursos localizáveis no arquivo de origem de entrada, nenhum arquivo de recurso específico de idioma será gerado e o arquivo LN resultante não conterá dados de configuração de recursos.</span><span class="sxs-lookup"><span data-stu-id="2eab8-239">If you use the -q switch to specify a resource configuration file, but there are no localizable resources in your input source file, no language-specific resource file is generated and the resulting LN file does not contain resource configuration data.</span></span> <span data-ttu-id="2eab8-240">Além disso, se o arquivo de origem de entrada tiver recursos multilíngües, o MUIRCT não dividirá o arquivo.</span><span class="sxs-lookup"><span data-stu-id="2eab8-240">Also, if the input source file has multilingual resources, then MUIRCT won't split the file.</span></span>

> [!Note]  
> <span data-ttu-id="2eab8-241">Atualmente, o comportamento de MUIRCT é inconsistente quando o elemento neutralResources do arquivo de configuração de recurso não contém nenhum elemento resourceType e o elemento localizedResources contém cadeias de caracteres e menus, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="2eab8-241">Currently the behavior of MUIRCT is inconsistent when the neutralResources element of the resource configuration file contains no resourceType elements and the localizedResources element contains strings and menus, for example.</span></span> <span data-ttu-id="2eab8-242">Nesse caso, o MUIRCT divide os recursos da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="2eab8-242">In such a case, MUIRCT splits the resources as follows:</span></span>
>
> -   <span data-ttu-id="2eab8-243">Todos os recursos no binário original (incluindo cadeias de caracteres e menus), além dos recursos do MUI, são colocados no arquivo LN.</span><span class="sxs-lookup"><span data-stu-id="2eab8-243">All resources in the original binary (including strings and menus), plus the MUI resources, are placed in the LN file.</span></span>
> -   <span data-ttu-id="2eab8-244">As cadeias de caracteres, os menus e os recursos do MUI são colocados no arquivo de recursos específico do idioma apropriado.</span><span class="sxs-lookup"><span data-stu-id="2eab8-244">Strings, menus, and MUI resources are placed in the appropriate language-specific resource file.</span></span>

 

### <a name="examples-for-using-muirct"></a><span data-ttu-id="2eab8-245">Exemplos de uso de MUIRCT</span><span class="sxs-lookup"><span data-stu-id="2eab8-245">Examples for Using MUIRCT</span></span>

<span data-ttu-id="2eab8-246">**Exemplos de uso padrão**</span><span class="sxs-lookup"><span data-stu-id="2eab8-246">**Examples of Standard Usage**</span></span>


```C++
muirct -q mui.MMF bar.exe barnew.exe barnew.exe.mui

muirct -d myprog.exe.mui
```



<span data-ttu-id="2eab8-247">**Exemplo de saída de arquivo LN usando a opção-d**</span><span class="sxs-lookup"><span data-stu-id="2eab8-247">**Example of LN File Output Using -d Switch**</span></span>

<span data-ttu-id="2eab8-248">Aqui está um exemplo da saída de dados de configuração de recurso de um arquivo LN, Shell32.dll, usando a opção-d com MUIRCT:</span><span class="sxs-lookup"><span data-stu-id="2eab8-248">Here is an example of the resource configuration data output from an LN file, Shell32.dll, using the -d switch with MUIRCT:</span></span>


```C++
Signature          -    fecdfecd
Length             -    148
RC Config Version  -    10000
FileType           -    11
SystemAttributes   -    100
UltimateFallback location    -  external
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    AVI FTR ORDERSTREAM TYPELIB UIFILE XML MUI
MainIDTypes        -    1 2 3 12 14 16 24
MuiNameTypes       -    MUI
MuiIDTypes         -    2 3 4 5 6 9 14 16
UltimateFallbackLanguage   -   en-US
```



<span data-ttu-id="2eab8-249">**Exemplo de saída de arquivo de recurso de Language-Specific usando a opção-d**</span><span class="sxs-lookup"><span data-stu-id="2eab8-249">**Example of Language-Specific Resource File Output Using -d Switch**</span></span>

<span data-ttu-id="2eab8-250">Aqui está um exemplo da saída de dados de configuração de recurso de um arquivo. mui, Shell32.dll. mui, usando a opção-d para MUIRCT:</span><span class="sxs-lookup"><span data-stu-id="2eab8-250">Here is an example of the resource configuration data output from a .mui file, Shell32.dll.mui, using the -d switch for MUIRCT:</span></span>


```C++
Signature          -    fecdfecd
Length             -     c8
RC Config Version  -    10000
FileType           -    12
SystemAttributes   -    100
Service Checksum   -    14f44a8d86bef14af26d9a885964c935
Checksum           -    f5b3b7ab330439d6fcc07582c3afb613
MainNameTypes      -    MUI
MainIDTypes        -    2 3 4 5 6 9 14 16
Language           -    en-US
```



## <a name="rc-compiler-utility"></a><span data-ttu-id="2eab8-251">Utilitário de compilador RC</span><span class="sxs-lookup"><span data-stu-id="2eab8-251">RC Compiler Utility</span></span>

<span data-ttu-id="2eab8-252">O compilador RC (Rc.exe) é um utilitário de linha de comando para compilar um arquivo de script de definição de recurso (extensão. rc) em arquivos de recurso (extensão. res).</span><span class="sxs-lookup"><span data-stu-id="2eab8-252">RC Compiler (Rc.exe) is a command line utility for compiling a resource definition script file (.rc extension) into resource files (.res extension).</span></span> <span data-ttu-id="2eab8-253">O compilador RC está incluído no SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="2eab8-253">RC Compiler is included in the Windows SDK.</span></span> <span data-ttu-id="2eab8-254">Este documento explica apenas o uso do compilador RC com recursos relacionados ao MUI do carregador de recursos.</span><span class="sxs-lookup"><span data-stu-id="2eab8-254">This document only explains the use of RC Compiler with MUI-related capabilities of the resource loader.</span></span> <span data-ttu-id="2eab8-255">Para obter informações completas sobre o compilador, consulte [About Resource files](../menurc/about-resource-files.md).</span><span class="sxs-lookup"><span data-stu-id="2eab8-255">For complete information about the compiler, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

<span data-ttu-id="2eab8-256">O compilador RC permite que você crie, de um único conjunto de fontes, um arquivo LN e um arquivo de recursos específico de idioma separado.</span><span class="sxs-lookup"><span data-stu-id="2eab8-256">RC Compiler allows you to build, from a single set of sources, an LN file and a separate language-specific resource file.</span></span> <span data-ttu-id="2eab8-257">Para MUIRCT, os arquivos são associados pelos dados de configuração do recurso.</span><span class="sxs-lookup"><span data-stu-id="2eab8-257">As for MUIRCT, the files are associated by resource configuration data.</span></span>

### <a name="rc-compiler-syntax-as-used-for-mui-resources"></a><span data-ttu-id="2eab8-258">Sintaxe do compilador RC como usada para recursos MUI</span><span class="sxs-lookup"><span data-stu-id="2eab8-258">RC Compiler Syntax as Used for MUI Resources</span></span>

<span data-ttu-id="2eab8-259">As opções do compilador RC são definidas em detalhes no [uso do RC](../menurc/using-rc-the-rc-command-line-.md).</span><span class="sxs-lookup"><span data-stu-id="2eab8-259">RC Compiler switches are defined in detail in [Using RC](../menurc/using-rc-the-rc-command-line-.md).</span></span> <span data-ttu-id="2eab8-260">Esta seção define apenas as opções usadas para criar recursos do MUI.</span><span class="sxs-lookup"><span data-stu-id="2eab8-260">This section only defines the switches used to build MUI resources.</span></span> <span data-ttu-id="2eab8-261">Lembre-se de que cada opção não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2eab8-261">Remember that each switch is case-insensitive.</span></span> <span data-ttu-id="2eab8-262">Os tipos de recursos são considerados neutros à língua, a menos que indicado em contrário.</span><span class="sxs-lookup"><span data-stu-id="2eab8-262">Resource types are assumed to be language-neutral unless otherwise indicated.</span></span>


```C++
rc [-h|-?] -fm mui_res_name [-q rc_config_file_name] [-g langid] [-g1 ] [-g2 version]
```



<span data-ttu-id="2eab8-263">**Opções e argumentos**</span><span class="sxs-lookup"><span data-stu-id="2eab8-263">**Switches and Arguments**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2eab8-264">-h |-?</span><span class="sxs-lookup"><span data-stu-id="2eab8-264">-h|-?</span></span></td>
<td><span data-ttu-id="2eab8-265">Mostra a tela de ajuda.</span><span class="sxs-lookup"><span data-stu-id="2eab8-265">Shows help screen.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2eab8-266">-FM</span><span class="sxs-lookup"><span data-stu-id="2eab8-266">-fm</span></span></td>
<td><span data-ttu-id="2eab8-267">Usa o arquivo de recurso especificado para recursos específicos do idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-267">Uses the specified resource file for language-specific resources.</span></span> <span data-ttu-id="2eab8-268">Normalmente, o compilador de recurso cria um arquivo de recurso específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-268">Normally the resource compiler creates a language-specific resource file.</span></span> <span data-ttu-id="2eab8-269">No entanto, ele não cria o arquivo se alguma das seguintes condições existir:</span><span class="sxs-lookup"><span data-stu-id="2eab8-269">However, it does not create the file if any of the following conditions exist:</span></span><br/>
<ul>
<li><span data-ttu-id="2eab8-270">Não há recursos localizáveis no arquivo. rc.</span><span class="sxs-lookup"><span data-stu-id="2eab8-270">There are no localizable resources in the .rc file.</span></span></li>
<li><span data-ttu-id="2eab8-271">O único idioma de recurso encontrado no arquivo. rc é o idioma neutro.</span><span class="sxs-lookup"><span data-stu-id="2eab8-271">The only resource language found in the .rc file is the neutral language.</span></span></li>
<li><span data-ttu-id="2eab8-272">O arquivo. RC tem recursos para mais de um idioma, não contando a linguagem neutra.</span><span class="sxs-lookup"><span data-stu-id="2eab8-272">The .rc file has resources for more than one language, not counting the neutral language.</span></span> <span data-ttu-id="2eab8-273">Se o arquivo. rc contiver recursos para dois idiomas, e um deles for o idioma neutro, o compilador considerará o arquivo como multilíngue.</span><span class="sxs-lookup"><span data-stu-id="2eab8-273">If the .rc file contains resources for two languages, and one of them is the neutral language, the compiler considers the file to be monolingual.</span></span> <span data-ttu-id="2eab8-274">Se houver recursos localizáveis, o compilador criará um arquivo de recursos específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-274">If there are any localizable resources, the compiler creates a language-specific resource file.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2eab8-275">-Q</span><span class="sxs-lookup"><span data-stu-id="2eab8-275">-q</span></span></td>
<td><span data-ttu-id="2eab8-276">Usa o arquivo de configuração de recurso especificado para obter os tipos de recurso a serem colocados no arquivo de recurso específico do idioma e no arquivo LN.</span><span class="sxs-lookup"><span data-stu-id="2eab8-276">Uses the specified resource configuration file to obtain the resource types to place in the language-specific resource file and the LN file.</span></span> <span data-ttu-id="2eab8-277">Para obter mais informações, consulte <a href="preparing-a-resource-configuration-file.md">preparando um arquivo de configuração de recurso</a>.</span><span class="sxs-lookup"><span data-stu-id="2eab8-277">For more information, see <a href="preparing-a-resource-configuration-file.md">Preparing a Resource Configuration File</a>.</span></span> <span data-ttu-id="2eab8-278">Como alternativa a essa opção, você pode usar as opções-j e-k, mas é preferível usar um arquivo de configuração de recurso.</span><span class="sxs-lookup"><span data-stu-id="2eab8-278">As an alternative to this switch, you can use the -j and -k switches, but it is preferred to use a resource configuration file.</span></span> <br/> <span data-ttu-id="2eab8-279">Usando a opção-q com um arquivo de configuração de recurso, você pode implementar uma divisão baseada em item e fornecer atributos que acabarão com a configuração de recursos binários no LN e no arquivo de recurso específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-279">By using the -q switch with a resource configuration file, you can implement an item-based split and provide attributes that will end up with the binary resource configuration in the LN and language-specific resource file.</span></span> <span data-ttu-id="2eab8-280">Essa divisão não é possível usando as opções-j e-k.</span><span class="sxs-lookup"><span data-stu-id="2eab8-280">This split is not possible using the -j and -k switches.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="2eab8-281">O processo de divisão do compilador RC não funcionará corretamente se você armazenar recursos e informações de versão em arquivos de configuração de recurso diferentes.</span><span class="sxs-lookup"><span data-stu-id="2eab8-281">The RC Compiler split process does not work properly if you store resources and version information in different resource configuration files.</span></span> <span data-ttu-id="2eab8-282">Nesse caso, o compilador RC não divide as informações de versão.</span><span class="sxs-lookup"><span data-stu-id="2eab8-282">In this case, RC Compiler does not split the version information.</span></span> <span data-ttu-id="2eab8-283">Portanto, um erro de vinculador ocorre durante a vinculação do arquivo de recursos específico do idioma porque o arquivo não tem recursos de versão.</span><span class="sxs-lookup"><span data-stu-id="2eab8-283">Therefore a linker error occurs during linking of the language-specific resource file because the file does not have version resources.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2eab8-284">-g</span><span class="sxs-lookup"><span data-stu-id="2eab8-284">-g</span></span></td>
<td><span data-ttu-id="2eab8-285">Especifica o identificador de <a href="language-identifiers.md">idioma de fallback</a> final em hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="2eab8-285">Specifies the ultimate <a href="language-identifiers.md">fallback language</a> identifier in hexadecimal.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2eab8-286">-G1</span><span class="sxs-lookup"><span data-stu-id="2eab8-286">-g1</span></span></td>
<td><span data-ttu-id="2eab8-287">Cria um arquivo MUI. res mesmo que o recurso de versão seja o único conteúdo localizável.</span><span class="sxs-lookup"><span data-stu-id="2eab8-287">Creates a MUI .res file even if the VERSION resource is the only localizable content.</span></span> <span data-ttu-id="2eab8-288">Por padrão, o compilador RC não produzirá um arquivo. res se a versão for o único recurso localizável.</span><span class="sxs-lookup"><span data-stu-id="2eab8-288">By default, RC Compiler does not produce a .res file if VERSION is the only localizable resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2eab8-289">-g2</span><span class="sxs-lookup"><span data-stu-id="2eab8-289">-g2</span></span></td>
<td><span data-ttu-id="2eab8-290">Especifica o número de versão personalizado a ser usado ao calcular a soma de verificação.</span><span class="sxs-lookup"><span data-stu-id="2eab8-290">Specifies the custom version number to use when calculating the checksum.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2eab8-291">mui_res_name</span><span class="sxs-lookup"><span data-stu-id="2eab8-291">mui_res_name</span></span></td>
<td><span data-ttu-id="2eab8-292">Arquivo de recurso para recursos específicos do idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-292">Resource file for language-specific resources.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2eab8-293">rc_config_file_name</span><span class="sxs-lookup"><span data-stu-id="2eab8-293">rc_config_file_name</span></span></td>
<td><span data-ttu-id="2eab8-294">Arquivo de configuração de recurso.</span><span class="sxs-lookup"><span data-stu-id="2eab8-294">Resource configuration file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2eab8-295">langid</span><span class="sxs-lookup"><span data-stu-id="2eab8-295">langid</span></span></td>
<td><span data-ttu-id="2eab8-296">Identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-296">Language identifier.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2eab8-297">version</span><span class="sxs-lookup"><span data-stu-id="2eab8-297">version</span></span></td>
<td><span data-ttu-id="2eab8-298">Número de versão personalizado, em um formato como &quot; 6.2.0.0 &quot; .</span><span class="sxs-lookup"><span data-stu-id="2eab8-298">Custom version number, in a format such as &quot;6.2.0.0&quot;.</span></span><br/></td>
</tr>
</tbody>
</table>



 

### <a name="example-for-using-rc-compiler-to-build-mui-resources"></a><span data-ttu-id="2eab8-299">Exemplo de uso do compilador RC para criar recursos MUI</span><span class="sxs-lookup"><span data-stu-id="2eab8-299">Example for Using RC Compiler to Build MUI Resources</span></span>

<span data-ttu-id="2eab8-300">Para ilustrar a operação do compilador RC com recursos do MUI, vamos examinar a seguinte linha de comando para o arquivo de recurso MyFile. rc:</span><span class="sxs-lookup"><span data-stu-id="2eab8-300">To illustrate RC Compiler operation with MUI resources, let's examine the following command line, for the resource file Myfile.rc:</span></span>


```C++
rc -fm myfile_res.res -q myfile.rcconfig myfile.rc
```



<span data-ttu-id="2eab8-301">Essa linha de comando faz com que o compilador RC faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2eab8-301">This command line causes RC Compiler to do the following:</span></span>

-   <span data-ttu-id="2eab8-302">Crie o arquivo de recurso específico do idioma MyFile \_ res. res e um arquivo de recurso neutro de idioma que assume o padrão de MyFile. res, com base no nome do arquivo. rc.</span><span class="sxs-lookup"><span data-stu-id="2eab8-302">Create the language-specific resource file Myfile\_res.res and a language-neutral resource file that defaults to Myfile.res, based on the name of the .rc file.</span></span>
-   <span data-ttu-id="2eab8-303">Adicione os dois (item 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 meus \_ tipos de recursos de tipo ao arquivo. res específico ao idioma se eles estiverem no arquivo. rc.</span><span class="sxs-lookup"><span data-stu-id="2eab8-303">Add the 2 (item 5 6 7 8 9 10 11 12), 4, 5, 6, 9, 11, 16, 23, 240, 1024 MY\_TYPE resource types to the language-specific .res file if they are in the .rc file.</span></span>
-   <span data-ttu-id="2eab8-304">Adicione o tipo de recurso 16, juntamente com quaisquer outros tipos de recursos descritos no arquivo de recurso ao arquivo. res de idioma neutro e ao arquivo. res específico do idioma.</span><span class="sxs-lookup"><span data-stu-id="2eab8-304">Add resource type 16, along with any other resource types described in the resource file to the language-neutral .res file and to the language-specific .res file.</span></span> <span data-ttu-id="2eab8-305">Observe que, neste exemplo, o tipo de recurso 16 está sendo adicionado em dois lugares.</span><span class="sxs-lookup"><span data-stu-id="2eab8-305">Note that, in this example, resource type 16 is being added in two places.</span></span>
-   <span data-ttu-id="2eab8-306">Escolha o valor do atributo "UltimateFallbackLanguage" para inserir nos dados de configuração de recurso do arquivo LN com base nos critérios a seguir, ordenados da prioridade mais alta para a mais baixa:</span><span class="sxs-lookup"><span data-stu-id="2eab8-306">Choose the "UltimateFallbackLanguage" attribute value to insert into the LN file resource configuration data based on the following criteria, ordered from highest priority to lowest:</span></span>
    -   <span data-ttu-id="2eab8-307">O atributo "UltimateFallbackLanguage" no arquivo de configuração de recurso se um for passado como entrada.</span><span class="sxs-lookup"><span data-stu-id="2eab8-307">"UltimateFallbackLanguage" attribute in the resource configuration file if one is passed in as input.</span></span>
    -   <span data-ttu-id="2eab8-308">O valor do atributo de idioma a ser inserido nos dados de configuração de recurso com base na ordem de linguagem do compilador RC (linguagem de arquivo de recurso de linguagem neutra e específica de idioma).</span><span class="sxs-lookup"><span data-stu-id="2eab8-308">Language attribute value to insert in the resource configuration data based on the RC Compiler language order (language-neutral and language-specific resource file language).</span></span> <span data-ttu-id="2eab8-309">As considerações incluem o idioma no arquivo. rc, o valor de idioma da opção-GL e o identificador 0x0409 para inglês (Estados Unidos).</span><span class="sxs-lookup"><span data-stu-id="2eab8-309">Considerations include language in the .rc file, language value of the -gl switch, and identifier 0x0409 for English (United States).</span></span>

## <a name="remarks"></a><span data-ttu-id="2eab8-310">Comentários</span><span class="sxs-lookup"><span data-stu-id="2eab8-310">Remarks</span></span>

<span data-ttu-id="2eab8-311">Se você incluir qualquer ícone (3), caixa de diálogo (5), Cadeia de caracteres (6) ou tipo de recurso de versão (16) no elemento neutralResources, terá que duplicar essa entrada no elemento localizedResources no arquivo de configuração de recurso.</span><span class="sxs-lookup"><span data-stu-id="2eab8-311">If you include any ICON(3), DIALOG(5), STRING(6), or VERSION(16) resource type in the neutralResources element, then you have to duplicate that entry in the localizedResources element in the resource configuration file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2eab8-312">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2eab8-312">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eab8-313">Referência de interface do usuário multilíngue</span><span class="sxs-lookup"><span data-stu-id="2eab8-313">Multilingual User Interface Reference</span></span>](multilingual-user-interface-reference.md)
</dt> <dt>

[<span data-ttu-id="2eab8-314">Gerenciamento de recursos do MUI</span><span class="sxs-lookup"><span data-stu-id="2eab8-314">MUI Resource Management</span></span>](mui-resource-management.md)
</dt> <dt>

[<span data-ttu-id="2eab8-315">Localizando recursos e compilando o aplicativo</span><span class="sxs-lookup"><span data-stu-id="2eab8-315">Localizing Resources and Building the Application</span></span>](localizing-resources-and-building-the-application.md)
</dt> </dl>

 

 
