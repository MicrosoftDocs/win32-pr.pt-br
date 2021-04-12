---
description: As mensagens de informações a seguir descrevem a operação do compilador.
ms.assetid: 838e598d-871d-4015-a372-4d94cacf8048
ms.tgt_platform: multiple
title: Mensagens de informações gerais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0997fad497299c7598fc1130edace49c20d7bb76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296631"
---
# <a name="general-information-messages"></a><span data-ttu-id="7bdc8-103">Mensagens de informações gerais</span><span class="sxs-lookup"><span data-stu-id="7bdc8-103">General Information Messages</span></span>

<span data-ttu-id="7bdc8-104">As mensagens de informações a seguir descrevem a operação do compilador.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-104">The following information messages describe the compiler operation.</span></span>

<dl> <dt>

<span data-ttu-id="7bdc8-105"><span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: versão <versão \#> definições de MIB compiladas de <file name>**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-105"><span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: Version <version \#> MIB definitions compiled from <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-106">Essa mensagem aparece no início de cada compilação de arquivo.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-106">This message appears at the beginning of every file compilation.</span></span> <span data-ttu-id="7bdc8-107">Isso significa que o arquivo pode ter sido explicitamente especificado na linha de comando pelo usuário ou pode ter sido puxado pelo compilador dos diretórios de inclusão do registro ou dos diretórios de inclusão mencionados na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-107">It means the file may have been explicitly specified on the command line by the user, or it may have been pulled in by the compiler from the registry include directories or the include directories mentioned on the command line.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-108"><span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: falha na verificação de sintaxe em <file name>**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-108"><span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Syntax check failed on <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-109">As mensagens de erro específicas que precedem essa mensagem fornecem a natureza dos erros de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-109">The specific error messages that precede this message give the nature of the syntax errors.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-110"><span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: a verificação semântica falhou em <file name>**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-110"><span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: Semantic check failed on <file name>**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-111">As mensagens de erro específicas que precedem essa mensagem fornecem a natureza dos erros semânticos.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-111">The specific error messages that precede this message give the nature of the semantic errors.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-112"><span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: não foi possível carregar <file name> no Smir**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-112"><span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: Could not load <file name> into the smir**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-113">Falha na verificação de sintaxe ou semântica no módulo ou a interação SMIR não foi concluída.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-113">Syntax or semantic check failed on the module, or SMIR interaction was not complete.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-114"><span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: verificação de sintaxe bem-sucedida em <file name>**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-114"><span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Syntax check successful on <file name>**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bdc8-115"><span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: verificação semântica bem-sucedida em <file name>**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-115"><span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: Semantic check successful on <file name>**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bdc8-116"><span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: carregado <file name> com êxito no Smir**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-116"><span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: Loaded <file name> successfully into the smir**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="7bdc8-117"><span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: não foi possível resolver um ou mais símbolos em <module name>**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-117"><span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: Could not resolve one or more symbols in <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-118">Os módulos correspondentes a um ou mais dos símbolos importados no módulo especificado não foram encontrados ou não puderam ser compilados.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-118">The modules corresponding to one or more of the imported symbols in the specified module were not found or could not be compiled.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-119"><span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: não foi possível conectar-se ao SMIR**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-119"><span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: Could not connect to the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-120">Verifique se o Smir.dll existe, se foi registrado usando o comando regsvr32 e se o servidor de Instrumentação de Gerenciamento do Windows (WMI) está ativo e em execução.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-120">Ensure that Smir.dll exists, has been registered using the regsvr32 command, and that the Windows Management Instrumentation (WMI) server is up and running.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-121"><span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: modules no SMIR: <lista de módulos, 1 em cada linha>**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-121"><span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: Modules in the SMIR: <list of modules, 1 on each line>**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-122">Esta é a saída da opção **/l** .</span><span class="sxs-lookup"><span data-stu-id="7bdc8-122">This is the output of the **/l** switch.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-123"><span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir não pôde listar os módulos no SMIR**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-123"><span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir Could not list the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-124">Isso indica uma falha da opção **/l** devido a nenhuma conexão Smir.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-124">This indicates a failure of the **/l** switch due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-125"><span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: módulo excluído <module name> com êxito**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-125"><span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: Deleted module <module name> successfully**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-126">A opção **/d** foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-126">The **/d** switch succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-127"><span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: não foi possível excluir o módulo <module name>**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-127"><span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: Could not delete module <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-128">Isso indica uma falha da opção **/d** devido a nenhuma conexão Smir.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-128">This indicates a failure of the **/d** switch due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-129"><span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: excluiu todos os módulos no SMIR**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-129"><span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Deleted all the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-130">A opção **/p** foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-130">The **/p** switch succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-131"><span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: não foi possível excluir todos os módulos no SMIR**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-131"><span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: Could not delete all the modules in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-132">A opção **/p** falhou porque não há conexão Smir.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-132">The **/p** switch failed because there is no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-133"><span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: <module name> o módulo não existe no Smir**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-133"><span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: Module <module name> does not exist in the SMIR**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-134">A opção **/d** falhou porque o módulo especificado não está no Smir.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-134">The **/d** switch failed because the specified module is not in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-135"><span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: MOF gerado com êxito**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-135"><span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: Generated MOF successfully**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-136">A opção **/g** ou **/GC** funcionou com êxito.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-136">The **/g** or **/gc** switch worked successfully.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-137"><span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: não foi possível gerar o MOF**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-137"><span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: Could not generate MOF**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-138">A opção **/g** ou **/GC** não funcionou com êxito devido a nenhuma conexão Smir.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-138">The **/g** or **/gc** switch did not work successfully due to no SMIR connection.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-139"><span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: nome do módulo: <module name>**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-139"><span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: Name of the module: <module name>**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-140">Esta é a saída bem-sucedida da opção **/n** .</span><span class="sxs-lookup"><span data-stu-id="7bdc8-140">This is the successful output of the **/n** switch.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-141"><span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: não foi possível analisar <file name> com êxito**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-141"><span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: Could not parse <file name> successfully**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-142">Isso indica falha da opção **/n** ou **/Ni** porque o arquivo especificado não é um arquivo MIB válido.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-142">This indicates failure of the **/n** or **/ni** switch because the specified file is not a valid MIB file.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-143"><span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: arquivos processados <number> com êxito**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-143"><span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: Processed <number> files successfully**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-144">Isso especifica o número de arquivos que foram analisados com êxito quando a opção **/r** ou **/auto** foi usada.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-144">This specifies the number of files that were successfully parsed when the **/r** or the **/auto** switch were used.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-145"><span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: arquivos repetidos na entrada para o módulo <module name> . Somente o arquivo <file name> será compilado**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-145"><span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: Repeated files in the input for module <module name>. Only the file <file name> will be compiled**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-146">O usuário especificou explicitamente mais de um arquivo na linha de comando e dois ou mais desses arquivos têm o mesmo módulo MIB.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-146">The user has explicitly specified more than one file on the command line, and two or more of these files have the same MIB module.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-147"><span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: diretório adicionado <directory name> ao registro**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-147"><span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Added directory <directory name> to the registry**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-148">Êxito do comutador **/PA** .</span><span class="sxs-lookup"><span data-stu-id="7bdc8-148">Success of the **/pa** switch.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-149"><span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: não foi possível adicionar <directory name> o diretório ao registro**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-149"><span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: Could not add directory <directory name> to the registry**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-150">Falha do comutador **/PA** , que ocorre somente se a API do registro falhar.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-150">Failure of the **/pa** switch, which happens only if the registry API fails.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-151"><span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: diretório excluído <directory name> do registro**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-151"><span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Deleted directory <directory name> from the registry**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-152">Êxito do comutador **/PD** .</span><span class="sxs-lookup"><span data-stu-id="7bdc8-152">Success of the **/pd** switch.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-153"><span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: não foi possível excluir <directory name> do registro**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-153"><span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: Could not delete <directory name> from the registry**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-154">Falha do comutador **/PD** .</span><span class="sxs-lookup"><span data-stu-id="7bdc8-154">Failure of the **/pd** switch.</span></span> <span data-ttu-id="7bdc8-155">O diretório especificado não existe na lista de diretórios no registro.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-155">The specified directory does not exist in the list of directories in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="7bdc8-156"><span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> não é um arquivo MIB válido**</span><span class="sxs-lookup"><span data-stu-id="7bdc8-156"><span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> is not a valid mib file**</span></span>
</dt> <dd>

<span data-ttu-id="7bdc8-157">Mais de um arquivo foi especificado na linha de comando, um dos quais não é um arquivo MIB válido.</span><span class="sxs-lookup"><span data-stu-id="7bdc8-157">More than one file has been specified on the command line, one of which is not a valid MIB file.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="7bdc8-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7bdc8-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bdc8-159">Configurando o ambiente SNMP WMI</span><span class="sxs-lookup"><span data-stu-id="7bdc8-159">Setting up the WMI SNMP Environment</span></span>](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



