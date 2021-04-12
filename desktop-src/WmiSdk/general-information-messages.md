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
# <a name="general-information-messages"></a>Mensagens de informações gerais

As mensagens de informações a seguir descrevem a operação do compilador.

<dl> <dt>

<span id="smi2smir__Version__version____MIB_definitions_compiled_from__file_name_"></span><span id="smi2smir__version__version____mib_definitions_compiled_from__file_name_"></span><span id="SMI2SMIR__VERSION__VERSION____MIB_DEFINITIONS_COMPILED_FROM__FILE_NAME_"></span>**smi2smir: versão <versão \#> definições de MIB compiladas de <file name>**
</dt> <dd>

Essa mensagem aparece no início de cada compilação de arquivo. Isso significa que o arquivo pode ter sido explicitamente especificado na linha de comando pelo usuário ou pode ter sido puxado pelo compilador dos diretórios de inclusão do registro ou dos diretórios de inclusão mencionados na linha de comando.

</dd> <dt>

<span id="smi2smir__Syntax_check_failed_on__file_name_"></span><span id="smi2smir__syntax_check_failed_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: falha na verificação de sintaxe em <file name>**
</dt> <dd>

As mensagens de erro específicas que precedem essa mensagem fornecem a natureza dos erros de sintaxe.

</dd> <dt>

<span id="smi2smir__Semantic_check_failed_on__file_name_"></span><span id="smi2smir__semantic_check_failed_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_FAILED_ON__FILE_NAME_"></span>**smi2smir: a verificação semântica falhou em <file name>**
</dt> <dd>

As mensagens de erro específicas que precedem essa mensagem fornecem a natureza dos erros semânticos.

</dd> <dt>

<span id="smi2smir__Could_not_load__file_name__into_the_smir"></span><span id="smi2smir__could_not_load__file_name__into_the_smir"></span><span id="SMI2SMIR__COULD_NOT_LOAD__FILE_NAME__INTO_THE_SMIR"></span>**smi2smir: não foi possível carregar <file name> no Smir**
</dt> <dd>

Falha na verificação de sintaxe ou semântica no módulo ou a interação SMIR não foi concluída.

</dd> <dt>

<span id="smi2smir__Syntax_check_successful_on__file_name_"></span><span id="smi2smir__syntax_check_successful_on__file_name_"></span><span id="SMI2SMIR__SYNTAX_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: verificação de sintaxe bem-sucedida em <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Semantic_check_successful_on__file_name_"></span><span id="smi2smir__semantic_check_successful_on__file_name_"></span><span id="SMI2SMIR__SEMANTIC_CHECK_SUCCESSFUL_ON__FILE_NAME_"></span>**smi2smir: verificação semântica bem-sucedida em <file name>**
</dt> <dd></dd> <dt>

<span id="smi2smir__Loaded__file_name__successfully_into_the_smir"></span><span id="smi2smir__loaded__file_name__successfully_into_the_smir"></span><span id="SMI2SMIR__LOADED__FILE_NAME__SUCCESSFULLY_INTO_THE_SMIR"></span>**smi2smir: carregado <file name> com êxito no Smir**
</dt> <dd></dd> <dt>

<span id="smi2smir__Could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="smi2smir__could_not_resolve_one_or_more_symbols_in__module_name_"></span><span id="SMI2SMIR__COULD_NOT_RESOLVE_ONE_OR_MORE_SYMBOLS_IN__MODULE_NAME_"></span>**smi2smir: não foi possível resolver um ou mais símbolos em <module name>**
</dt> <dd>

Os módulos correspondentes a um ou mais dos símbolos importados no módulo especificado não foram encontrados ou não puderam ser compilados.

</dd> <dt>

<span id="smi2smir__Could_not_connect_to_the_SMIR"></span><span id="smi2smir__could_not_connect_to_the_smir"></span><span id="SMI2SMIR__COULD_NOT_CONNECT_TO_THE_SMIR"></span>**smi2smir: não foi possível conectar-se ao SMIR**
</dt> <dd>

Verifique se o Smir.dll existe, se foi registrado usando o comando regsvr32 e se o servidor de Instrumentação de Gerenciamento do Windows (WMI) está ativo e em execução.

</dd> <dt>

<span id="smi2smir__Modules_in_the_SMIR___list_of_modules__1_on_each_line_"></span><span id="smi2smir__modules_in_the_smir___list_of_modules__1_on_each_line_"></span><span id="SMI2SMIR__MODULES_IN_THE_SMIR___LIST_OF_MODULES__1_ON_EACH_LINE_"></span>**smi2smir: modules no SMIR: <lista de módulos, 1 em cada linha>**
</dt> <dd>

Esta é a saída da opção **/l** .

</dd> <dt>

<span id="smi2smir_Could_not_list_the_modules_in_the_SMIR"></span><span id="smi2smir_could_not_list_the_modules_in_the_smir"></span><span id="SMI2SMIR_COULD_NOT_LIST_THE_MODULES_IN_THE_SMIR"></span>**smi2smir não pôde listar os módulos no SMIR**
</dt> <dd>

Isso indica uma falha da opção **/l** devido a nenhuma conexão Smir.

</dd> <dt>

<span id="smi2smir__Deleted_module__module_name__successfully"></span><span id="smi2smir__deleted_module__module_name__successfully"></span><span id="SMI2SMIR__DELETED_MODULE__MODULE_NAME__SUCCESSFULLY"></span>**smi2smir: módulo excluído <module name> com êxito**
</dt> <dd>

A opção **/d** foi bem-sucedida.

</dd> <dt>

<span id="smi2smir__Could_not_delete_module__module_name_"></span><span id="smi2smir__could_not_delete_module__module_name_"></span><span id="SMI2SMIR__COULD_NOT_DELETE_MODULE__MODULE_NAME_"></span>**smi2smir: não foi possível excluir o módulo <module name>**
</dt> <dd>

Isso indica uma falha da opção **/d** devido a nenhuma conexão Smir.

</dd> <dt>

<span id="smi2smir__Deleted_all_the_modules_in_the_SMIR"></span><span id="smi2smir__deleted_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__DELETED_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: excluiu todos os módulos no SMIR**
</dt> <dd>

A opção **/p** foi bem-sucedida.

</dd> <dt>

<span id="smi2smir__Could_not_delete_all_the_modules_in_the_SMIR"></span><span id="smi2smir__could_not_delete_all_the_modules_in_the_smir"></span><span id="SMI2SMIR__COULD_NOT_DELETE_ALL_THE_MODULES_IN_THE_SMIR"></span>**smi2smir: não foi possível excluir todos os módulos no SMIR**
</dt> <dd>

A opção **/p** falhou porque não há conexão Smir.

</dd> <dt>

<span id="smi2smir__Module__module_name__does_not_exist_in_the_SMIR"></span><span id="smi2smir__module__module_name__does_not_exist_in_the_smir"></span><span id="SMI2SMIR__MODULE__MODULE_NAME__DOES_NOT_EXIST_IN_THE_SMIR"></span>**smi2smir: <module name> o módulo não existe no Smir**
</dt> <dd>

A opção **/d** falhou porque o módulo especificado não está no Smir.

</dd> <dt>

<span id="smi2smir__Generated_MOF_successfully"></span><span id="smi2smir__generated_mof_successfully"></span><span id="SMI2SMIR__GENERATED_MOF_SUCCESSFULLY"></span>**smi2smir: MOF gerado com êxito**
</dt> <dd>

A opção **/g** ou **/GC** funcionou com êxito.

</dd> <dt>

<span id="smi2smir__Could_not_generate_MOF"></span><span id="smi2smir__could_not_generate_mof"></span><span id="SMI2SMIR__COULD_NOT_GENERATE_MOF"></span>**smi2smir: não foi possível gerar o MOF**
</dt> <dd>

A opção **/g** ou **/GC** não funcionou com êxito devido a nenhuma conexão Smir.

</dd> <dt>

<span id="smi2smir__Name_of_the_module___module_name_"></span><span id="smi2smir__name_of_the_module___module_name_"></span><span id="SMI2SMIR__NAME_OF_THE_MODULE___MODULE_NAME_"></span>**smi2smir: nome do módulo: <module name>**
</dt> <dd>

Esta é a saída bem-sucedida da opção **/n** .

</dd> <dt>

<span id="smi2smir__Could_not_parse__file_name__successfully"></span><span id="smi2smir__could_not_parse__file_name__successfully"></span><span id="SMI2SMIR__COULD_NOT_PARSE__FILE_NAME__SUCCESSFULLY"></span>**smi2smir: não foi possível analisar <file name> com êxito**
</dt> <dd>

Isso indica falha da opção **/n** ou **/Ni** porque o arquivo especificado não é um arquivo MIB válido.

</dd> <dt>

<span id="smi2smir__Processed__number__files_successfully"></span><span id="smi2smir__processed__number__files_successfully"></span><span id="SMI2SMIR__PROCESSED__NUMBER__FILES_SUCCESSFULLY"></span>**smi2smir: arquivos processados <number> com êxito**
</dt> <dd>

Isso especifica o número de arquivos que foram analisados com êxito quando a opção **/r** ou **/auto** foi usada.

</dd> <dt>

<span id="smi2smir__Repeated_files_in_the_input_for_module__module_name_._Only_the_file__file_name__will_be_compiled"></span><span id="smi2smir__repeated_files_in_the_input_for_module__module_name_._only_the_file__file_name__will_be_compiled"></span><span id="SMI2SMIR__REPEATED_FILES_IN_THE_INPUT_FOR_MODULE__MODULE_NAME_._ONLY_THE_FILE__FILE_NAME__WILL_BE_COMPILED"></span>**smi2smir: arquivos repetidos na entrada para o módulo <module name> . Somente o arquivo <file name> será compilado**
</dt> <dd>

O usuário especificou explicitamente mais de um arquivo na linha de comando e dois ou mais desses arquivos têm o mesmo módulo MIB.

</dd> <dt>

<span id="smi2smir__Added_directory__directory_name__to_the_registry"></span><span id="smi2smir__added_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__ADDED_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: diretório adicionado <directory name> ao registro**
</dt> <dd>

Êxito do comutador **/PA** .

</dd> <dt>

<span id="smi2smir__Could_not_add_directory__directory_name__to_the_registry"></span><span id="smi2smir__could_not_add_directory__directory_name__to_the_registry"></span><span id="SMI2SMIR__COULD_NOT_ADD_DIRECTORY__DIRECTORY_NAME__TO_THE_REGISTRY"></span>**smi2smir: não foi possível adicionar <directory name> o diretório ao registro**
</dt> <dd>

Falha do comutador **/PA** , que ocorre somente se a API do registro falhar.

</dd> <dt>

<span id="smi2smir__Deleted_directory__directory_name__from_the_registry"></span><span id="smi2smir__deleted_directory__directory_name__from_the_registry"></span><span id="SMI2SMIR__DELETED_DIRECTORY__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: diretório excluído <directory name> do registro**
</dt> <dd>

Êxito do comutador **/PD** .

</dd> <dt>

<span id="smi2smir__Could_not_delete__directory_name__from_the_registry"></span><span id="smi2smir__could_not_delete__directory_name__from_the_registry"></span><span id="SMI2SMIR__COULD_NOT_DELETE__DIRECTORY_NAME__FROM_THE_REGISTRY"></span>**smi2smir: não foi possível excluir <directory name> do registro**
</dt> <dd>

Falha do comutador **/PD** . O diretório especificado não existe na lista de diretórios no registro.

</dd> <dt>

<span id="smi2smir___file_name__is_not_a_valid_mib_file"></span><span id="SMI2SMIR___FILE_NAME__IS_NOT_A_VALID_MIB_FILE"></span>**smi2smir: <file name> não é um arquivo MIB válido**
</dt> <dd>

Mais de um arquivo foi especificado na linha de comando, um dos quais não é um arquivo MIB válido.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md)
</dt> </dl>

 

 



