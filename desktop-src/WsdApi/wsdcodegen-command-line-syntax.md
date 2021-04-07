---
description: 'O WsdCodeGen tem duas funções: geração de arquivos de configuração e geração de código-fonte para aplicativos de cliente e host do WSDAPI.'
ms.assetid: 75f5071c-040b-4e65-a80e-e1fea63535b0
title: Sintaxe de linha de comando WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7db3afe9b13286833f8563c0cacb41919d77bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827705"
---
# <a name="wsdcodegen-command-line-syntax"></a><span data-ttu-id="d7174-103">Sintaxe de linha de comando WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="d7174-103">WsdCodeGen Command Line Syntax</span></span>

<span data-ttu-id="d7174-104">O WsdCodeGen tem duas funções: geração de arquivos de configuração e geração de código-fonte para aplicativos de cliente e host do WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="d7174-104">WsdCodeGen has two functions: generating configuration files and generating source code for WSDAPI client and host applications.</span></span> <span data-ttu-id="d7174-105">Este tópico fornece a sintaxe de linha de comando usada para executar cada tarefa.</span><span class="sxs-lookup"><span data-stu-id="d7174-105">This topic gives the command line syntax used to perform each task.</span></span>

## <a name="generating-a-configuration-file"></a><span data-ttu-id="d7174-106">Gerando um arquivo de configuração</span><span class="sxs-lookup"><span data-stu-id="d7174-106">Generating a Configuration File</span></span>

### <a name="syntax"></a><span data-ttu-id="d7174-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7174-107">Syntax</span></span>

<span data-ttu-id="d7174-108">**WSDCODEGEN.EXE** **/generateconfig:**{host do **cliente** \|  \| **All**} **\[ /OutputFile:**_nome_arquivo_config_ *_\]_* *WSDLFileNameList*</span><span class="sxs-lookup"><span data-stu-id="d7174-108">**WSDCODEGEN.EXE** **/generateconfig:**{**client**\|**host**\|**all**} **\[/outputfile:**_ConfigFileName_*_\]_* *WSDLFileNameList*</span></span>

### <a name="parameters"></a><span data-ttu-id="d7174-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7174-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7174-110"><span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig: {host do cliente \| \| todos}**</span><span class="sxs-lookup"><span data-stu-id="d7174-110"><span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig:{client \| host \| all}**</span></span>
</dt> <dd>

<span data-ttu-id="d7174-111">O tipo de código que o arquivo de configuração de saída irá gerar.</span><span class="sxs-lookup"><span data-stu-id="d7174-111">The type of code that the output configuration file will generate.</span></span> <span data-ttu-id="d7174-112">**/generateconfig: o cliente** é usado para gerar um arquivo de configuração para gerar o código do cliente, **/generateconfig: o host** é usado para gerar um arquivo de configuração para gerar o código de host e **/generateconfig: ALL** é usado para gerar um arquivo de configuração para gerar o código do cliente e do host.</span><span class="sxs-lookup"><span data-stu-id="d7174-112">**/generateconfig:client** is used to generate a configuration file for generating client code, **/generateconfig:host** is used to generate a configuration file for generating host code, and **/generateconfig:all** is used to generate a configuration file for generating both client and host code.</span></span>

</dd> <dt>

<span data-ttu-id="d7174-113"><span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/OutputFile:**_nome_arquivo_config_</span><span class="sxs-lookup"><span data-stu-id="d7174-113"><span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/outputfile:**_ConfigFileName_</span></span>
</dt> <dd>

<span data-ttu-id="d7174-114">Esse parâmetro opcional é usado para especificar o nome do arquivo de configuração de saída.</span><span class="sxs-lookup"><span data-stu-id="d7174-114">This optional parameter is used to specify the file name of the output configuration file.</span></span> <span data-ttu-id="d7174-115">Se esse parâmetro for excluído, o nome do arquivo de configuração de saída será codegen.config.</span><span class="sxs-lookup"><span data-stu-id="d7174-115">If this parameter is excluded, the name of the output configuration file is codegen.config.</span></span>

</dd> <dt>

<span data-ttu-id="d7174-116"><span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*</span><span class="sxs-lookup"><span data-stu-id="d7174-116"><span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*</span></span>
</dt> <dd>

<span data-ttu-id="d7174-117">Inclua um modelo PnP-X no arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="d7174-117">Include a PnP-X template in the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="d7174-118"><span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*</span><span class="sxs-lookup"><span data-stu-id="d7174-118"><span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*</span></span>
</dt> <dd>

<span data-ttu-id="d7174-119">Uma lista delimitada por espaço dos arquivos WSDL a serem processados pelo WsdCodeGen.</span><span class="sxs-lookup"><span data-stu-id="d7174-119">A space-delimited list of the WSDL file(s) to be processed by WsdCodeGen.</span></span>

</dd> </dl>

## <a name="generating-source-code"></a><span data-ttu-id="d7174-120">Gerando código-fonte</span><span class="sxs-lookup"><span data-stu-id="d7174-120">Generating Source Code</span></span>

### <a name="syntax"></a><span data-ttu-id="d7174-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7174-121">Syntax</span></span>

<span data-ttu-id="d7174-122">**WSDCODEGEN.EXE** **/GenerateCode** **\[ /Download \]** **\[ /GBC \]** **\[ outputroot:**_caminho_ *_\]_* **\[ /WriteAccess:**_comando_ *_\]_* *nome_arquivo_config*</span><span class="sxs-lookup"><span data-stu-id="d7174-122">**WSDCODEGEN.EXE** **/generatecode** **\[/download\]** **\[/gbc\]** **\[outputroot:**_path_*_\]_* **\[/writeaccess:**_command_*_\]_* *ConfigFileName*</span></span>

### <a name="parameters"></a><span data-ttu-id="d7174-123">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7174-123">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7174-124"><span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**</span><span class="sxs-lookup"><span data-stu-id="d7174-124"><span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**</span></span>
</dt> <dd>

<span data-ttu-id="d7174-125">Direciona o WsdCodeGen para gerar o código-fonte.</span><span class="sxs-lookup"><span data-stu-id="d7174-125">Directs WsdCodeGen to generate source code.</span></span> <span data-ttu-id="d7174-126">Esse será o modo padrão se nenhum modo for especificado.</span><span class="sxs-lookup"><span data-stu-id="d7174-126">This is the default mode if no mode is specified.</span></span>

</dd> <dt>

<span data-ttu-id="d7174-127"><span id="_download"></span><span id="_DOWNLOAD"></span>**/download**</span><span class="sxs-lookup"><span data-stu-id="d7174-127"><span id="_download"></span><span id="_DOWNLOAD"></span>**/download**</span></span>
</dt> <dd>

<span data-ttu-id="d7174-128">Baixa documentos importados referenciados pelo arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="d7174-128">Downloads imported documents referenced by the configuration file.</span></span> <span data-ttu-id="d7174-129">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d7174-129">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="d7174-130"><span id="_gbc"></span><span id="_GBC"></span>**/gbc**</span><span class="sxs-lookup"><span data-stu-id="d7174-130"><span id="_gbc"></span><span id="_GBC"></span>**/gbc**</span></span>
</dt> <dd>

<span data-ttu-id="d7174-131">Adiciona comentários ao código-fonte que indica que o código foi gerado.</span><span class="sxs-lookup"><span data-stu-id="d7174-131">Adds comments to the source code that indicates the code was generated.</span></span> <span data-ttu-id="d7174-132">Esses comentários são prefixados com a frase "gerada por".</span><span class="sxs-lookup"><span data-stu-id="d7174-132">These comments are prefixed with the phrase "Generated by".</span></span> <span data-ttu-id="d7174-133">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d7174-133">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="d7174-134"><span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot:**_caminho_</span><span class="sxs-lookup"><span data-stu-id="d7174-134"><span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot:**_path_</span></span>
</dt> <dd>

<span data-ttu-id="d7174-135">O local de saída para os arquivos gerados.</span><span class="sxs-lookup"><span data-stu-id="d7174-135">The output location for generated files.</span></span> <span data-ttu-id="d7174-136">o *caminho* pode ser um caminho absoluto ou relativo.</span><span class="sxs-lookup"><span data-stu-id="d7174-136">*path* can be an absolute or relative path.</span></span> <span data-ttu-id="d7174-137">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="d7174-137">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="d7174-138"><span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/WriteAccess:**_comando_</span><span class="sxs-lookup"><span data-stu-id="d7174-138"><span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/writeaccess:**_command_</span></span>
</dt> <dd>

<span data-ttu-id="d7174-139">Direciona o WsdCodeGen para executar o comando especificado antes que ele modifique os arquivos existentes no disco.</span><span class="sxs-lookup"><span data-stu-id="d7174-139">Directs WsdCodeGen to execute the specified command before it modifies any existing files on disk.</span></span> <span data-ttu-id="d7174-140">Os arquivos de saída idênticos àqueles no disco não receberão esse comando, nem eles serão gravados no.</span><span class="sxs-lookup"><span data-stu-id="d7174-140">Output files that are identical to those on disk will not receive this command, nor will they be written to.</span></span> <span data-ttu-id="d7174-141">Se o comando contiver a sequência " {0} ", essa sequência será substituída pelo nome do arquivo a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="d7174-141">If the command contains the sequence "{0}", this sequence will be replaced with the filename of the file to be modified.</span></span> <span data-ttu-id="d7174-142">Caso contrário, o nome do arquivo será anexado ao comando.</span><span class="sxs-lookup"><span data-stu-id="d7174-142">If not, the filename will be appended to the command.</span></span>

<span data-ttu-id="d7174-143">Exemplos:</span><span class="sxs-lookup"><span data-stu-id="d7174-143">Examples:</span></span>

<span data-ttu-id="d7174-144">**/WriteAccess: "attrib-r"**</span><span class="sxs-lookup"><span data-stu-id="d7174-144">**/writeaccess:"attrib -r"**</span></span>

<span data-ttu-id="d7174-145">**/WriteAccess: "attrib-r {0} "**</span><span class="sxs-lookup"><span data-stu-id="d7174-145">**/writeaccess:"attrib -r {0}"**</span></span>

<span data-ttu-id="d7174-146">**/WriteAccess: "copiar {0} .. \\ backup \\ "**</span><span class="sxs-lookup"><span data-stu-id="d7174-146">**/writeaccess:"copy {0} ..\\backup\\"**</span></span>

</dd> <dt>

<span data-ttu-id="d7174-147"><span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*Nome_arquivo_config*</span><span class="sxs-lookup"><span data-stu-id="d7174-147"><span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*ConfigFileName*</span></span>
</dt> <dd>

<span data-ttu-id="d7174-148">O nome do arquivo de configuração a ser processado antes de gerar o código.</span><span class="sxs-lookup"><span data-stu-id="d7174-148">The name of the configuration file to process before generating code.</span></span>

</dd> </dl>

## <a name="formatting-legend"></a><span data-ttu-id="d7174-149">Legenda de formatação</span><span class="sxs-lookup"><span data-stu-id="d7174-149">Formatting Legend</span></span>



| <span data-ttu-id="d7174-150">Formatar</span><span class="sxs-lookup"><span data-stu-id="d7174-150">Format</span></span>                                                                    | <span data-ttu-id="d7174-151">Significado</span><span class="sxs-lookup"><span data-stu-id="d7174-151">Meaning</span></span>                                                 |
|---------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d7174-152">*Itálico*</span><span class="sxs-lookup"><span data-stu-id="d7174-152">*Italic*</span></span>                                                                  | <span data-ttu-id="d7174-153">Informações que o usuário deve fornecer</span><span class="sxs-lookup"><span data-stu-id="d7174-153">Information that the user must provide</span></span>                  |
| <span data-ttu-id="d7174-154">**Negrito**</span><span class="sxs-lookup"><span data-stu-id="d7174-154">**Bold**</span></span>                                                                  | <span data-ttu-id="d7174-155">Elementos devem ser digitados pelo usuário exatamente como mostrados</span><span class="sxs-lookup"><span data-stu-id="d7174-155">Elements that the user must type exactly as shown</span></span>       |
| <span data-ttu-id="d7174-156">Entre colchetes ( \[ \] )</span><span class="sxs-lookup"><span data-stu-id="d7174-156">Between brackets (\[\])</span></span>                                                   | <span data-ttu-id="d7174-157">Itens opcionais</span><span class="sxs-lookup"><span data-stu-id="d7174-157">Optional items</span></span>                                          |
| <span data-ttu-id="d7174-158">Entre chaves ( {} ); opções separadas por pipe ( \| ).</span><span class="sxs-lookup"><span data-stu-id="d7174-158">Between braces ({}); choices separated by pipe (\|).</span></span> <span data-ttu-id="d7174-159">Exemplo: {par \| ímpar}</span><span class="sxs-lookup"><span data-stu-id="d7174-159">Example: {even\|odd}</span></span> | <span data-ttu-id="d7174-160">Conjunto de opções do qual o usuário deve escolher apenas um</span><span class="sxs-lookup"><span data-stu-id="d7174-160">Set of choices from which the user must choose only one</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d7174-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7174-161">Requirements</span></span>



| <span data-ttu-id="d7174-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7174-162">Requirement</span></span> | <span data-ttu-id="d7174-163">Valor</span><span class="sxs-lookup"><span data-stu-id="d7174-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d7174-164">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7174-164">Minimum supported client</span></span><br/> | <span data-ttu-id="d7174-165">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7174-165">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d7174-166">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7174-166">Minimum supported server</span></span><br/> | <span data-ttu-id="d7174-167">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d7174-167">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7174-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7174-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7174-169">Arquivo de configuração WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="d7174-169">WsdCodeGen Configuration File</span></span>](wsdcodegen-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="d7174-170">Usando WsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="d7174-170">Using WsdCodeGen</span></span>](using-wsdcodegen.md)
</dt> </dl>

 

 




