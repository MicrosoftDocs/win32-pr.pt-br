---
description: Identifica uma entrada no banco de dados Shim.
ms.assetid: c092592d-a4f4-4b2f-9b03-c07951ed214a
title: MARCA (Exposeenums2managed. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacbd3c8d29e1f41d7aaabc989848c561415ae4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752566"
---
# <a name="tag"></a>TAG

Identifica uma entrada no banco de dados Shim.

As entradas a seguir são do **tipo \_ \_ lista de tipos de marca** (0x7000).



| Constante/valor                                                                                                                                                                                                                                                             | Descrição                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span id="TAG_DATABASE"></span><span id="tag_database"></span><dl> <dt>**Marca \_ de BANCO de dados**</dt> <dt>( \| **\_ \_ lista de tipos de marca** 0x1)</dt> </dl>                               | Entrada do banco de dados.<br/>                                                |
| <span id="TAG_LIBRARY"></span><span id="tag_library"></span><dl> <dt>**Marca \_ de BIBLIOTECA**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x2)</dt> </dl>                                  | Entrada de biblioteca.<br/>                                                 |
| <span id="TAG_INEXCLUDE"></span><span id="tag_inexclude"></span><dl> <dt>**Marca \_ de Inexclude**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x3)</dt> </dl>                            | Incluir e excluir a entrada.<br/>                                     |
| <span id="TAG_SHIM"></span><span id="tag_shim"></span><dl> <dt>**Marca \_ de SHIM**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x4)</dt> </dl>                                           | Entrada de Shim que contém as informações de nome e finalidade.<br/>     |
| <span id="TAG_PATCH"></span><span id="tag_patch"></span><dl> <dt>**Marca \_ de PATCH**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x5)</dt> </dl>                                        | Entrada de patch que contém as informações de patch na memória.<br/>  |
| <span id="TAG_APP"></span><span id="tag_app"></span><dl> <dt>**Marca \_ de APLICATIVO**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x6)</dt> </dl>                                              | Entrada do aplicativo.<br/>                                             |
| <span id="TAG_EXE"></span><span id="tag_exe"></span><dl> <dt>**Marca \_ de EXE**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x7)</dt> </dl>                                              | Entrada executável.<br/>                                              |
| <span id="TAG_MATCHING_FILE"></span><span id="tag_matching_file"></span><dl> <dt>**Marca \_ de \_Arquivo de correspondência**</dt> <dt>( \| **\_ \_ lista de tipos de marca** 0x8)</dt> </dl>               | Entrada de arquivo correspondente.<br/>                                           |
| <span id="TAG_SHIM_REF"></span><span id="tag_shim_ref"></span><dl> <dt>**Marca \_ de SHIM \_ ref**</dt> <dt>( \| lista de tipos de marca 0x9 \_ \_ )</dt> </dl>                                   | Entrada de definição de Shim.<br/>                                         |
| <span id="TAG_PATCH_REF"></span><span id="tag_patch_ref"></span><dl> <dt>**Marca \_ de \_Referência de patch**</dt> <dt>( \| **\_ \_ lista de tipos de marca** 0xA)</dt> </dl>                           | Entrada de definição de patch.<br/>                                        |
| <span id="TAG_LAYER"></span><span id="tag_layer"></span><dl> <dt>**Marca \_ de CAMADA**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0xB)</dt> </dl>                                        | Entrada de Shim de camada.<br/>                                              |
| <span id="TAG_FILE"></span><span id="tag_file"></span><dl> <dt>**Marca \_ de ARQUIVO**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0xc)</dt> </dl>                                           | Atributo de arquivo usado em uma entrada de Shim.<br/>                           |
| <span id="TAG_APPHELP"></span><span id="tag_apphelp"></span><dl> <dt>**Marca \_ de APPHELP**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0xD)</dt> </dl>                                  | Entrada de informações de AppHelp.<br/>                                     |
| <span id="TAG_LINK"></span><span id="tag_link"></span><dl> <dt>**Marca \_ de LINK**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0xE)</dt> </dl>                                           | Entrada de informações de link online AppHelp.<br/>                         |
| <span id="TAG_DATA"></span><span id="tag_data"></span><dl> <dt>**Marca \_ de DADOS**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0xF)</dt> </dl>                                           | Entrada de mapeamento de nome-valor.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM"></span><span id="tag_msi_transform"></span><dl> <dt>**Marca \_ de \_Transformação de MSI**</dt> <dt>( \| **\_ \_ lista de tipos de marca** 0x10)</dt> </dl>              | Entrada de transformação MSI.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM_REF"></span><span id="tag_msi_transform_ref"></span><dl> <dt>**Marca \_ de MSI \_ Transform \_ ref**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x11)</dt> </dl> | Entrada de definição de transformação MSI.<br/>                           |
| <span id="TAG_MSI_PACKAGE"></span><span id="tag_msi_package"></span><dl> <dt>**Marca \_ de \_Pacote MSI**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x12)</dt> </dl>                    | Entrada do pacote MSI.<br/>                                             |
| <span id="TAG_FLAG"></span><span id="tag_flag"></span><dl> <dt>**Marca \_ de FLAG**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x13)</dt> </dl>                                          | Entrada de sinalizador.<br/>                                                    |
| <span id="TAG_MSI_CUSTOM_ACTION"></span><span id="tag_msi_custom_action"></span><dl> <dt>**Marca \_ de \_ \_ Ação personalizada de MSI**</dt> <dt>( \| **\_ \_ lista de tipos de marca** 0x14)</dt> </dl> | Entrada de ação personalizada do MSI.<br/>                                       |
| <span id="TAG_FLAG_REF"></span><span id="tag_flag_ref"></span><dl> <dt>**Marca \_ de FLAG \_ ref**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x15)</dt> </dl>                             | Entrada de definição de sinalizador.<br/>                                         |
| <span id="TAG_ACTION"></span><span id="tag_action"></span><dl> <dt>**Marca \_ de AÇÃO**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x16)</dt> </dl>                                    | Não utilizado.<br/>                                                        |
| <span id="TAG_LOOKUP"></span><span id="tag_lookup"></span><dl> <dt>**Marca \_ de LOOKUP**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x17)</dt> </dl>                                    | Entrada de pesquisa usada para pesquisa em um banco de dados de driver.<br/>             |
| <span id="TAG_STRINGTABLE"></span><span id="tag_stringtable"></span><dl> <dt>**Marca \_ de STRINGTABLE**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x801)</dt> </dl>                    | Entrada da tabela de cadeia de caracteres.<br/>                                            |
| <span id="TAG_INDEXES"></span><span id="tag_indexes"></span><dl> <dt>**Marca \_ de ÍNDICES**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x802)</dt> </dl>                                | A entrada de índices que define todos os índices em um banco de dados de Shim.<br/> |
| <span id="TAG_INDEX"></span><span id="tag_index"></span><dl> <dt>**Marca \_ de ÍNDICE**</dt> <dt>( \| **lista de \_ tipos \_ de marca** 0x803)</dt> </dl>                                      | Entrada de índice que define um índice em um banco de dados de Shim.<br/>          |



As entradas a seguir são do tipo **tag \_ Type \_ STRINGREF** (0x6000).



| Constante/valor                                                                                                                                                                                                                                                                     | Descrição                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="TAG_NAME"></span><span id="tag_name"></span><dl> <dt>**Marca \_ de NAME**</dt> <dt>( \| **tipo de marca 0x1 \_ \_ STRINGREF**)</dt> </dl>                                              | Atributo de nome.<br/>                                                                    |
| <span id="TAG_DESCRIPTION"></span><span id="tag_description"></span><dl> <dt>**Marca \_ de Descrição**</dt> <dt>( \| **tipo de marca 0x2 \_ \_ STRINGREF**)</dt> </dl>                         | Entrada de descrição.<br/>                                                                 |
| <span id="TAG_MODULE"></span><span id="tag_module"></span><dl> <dt>**Marca \_ de MÓDULO**</dt> <dt>( \| **tipo de marca 0x3 \_ \_ STRINGREF**)</dt> </dl>                                        | Atributo de módulo.<br/>                                                                  |
| <span id="TAG_API"></span><span id="tag_api"></span><dl> <dt>**Marca \_ de API**</dt> <dt>( \| **tipo de marca 0x4 \_ \_ STRINGREF**)</dt> </dl>                                                 | Entrada de API.<br/>                                                                         |
| <span id="TAG_VENDOR"></span><span id="tag_vendor"></span><dl> <dt>**Marca \_ de FORNECEDOR**</dt> <dt>( \| **tipo de marca 0x5 \_ \_ STRINGREF**)</dt> </dl>                                        | Atributo de nome do fornecedor.<br/>                                                             |
| <span id="TAG_APP_NAME"></span><span id="tag_app_name"></span><dl> <dt>**Marca \_ de \_Nome do aplicativo**</dt> <dt>( \| **tipo de marca 0x6 \_ \_ STRINGREF**)</dt> </dl>                                 | Atributo de nome do aplicativo que descreve uma entrada de aplicativo em um banco de dados de Shim.<br/> |
| <span id="TAG_COMMAND_LINE"></span><span id="tag_command_line"></span><dl> <dt>**Marca \_ de \_Linha de comando**</dt> <dt>( \| **tipo de marca 0x8 \_ \_ STRINGREF**)</dt> </dl>                     | Atributo de linha de comando usado ao passar argumentos para um Shim, por exemplo.<br/> |
| <span id="TAG_COMPANY_NAME"></span><span id="tag_company_name"></span><dl> <dt>**Marca \_ de \_Nome da empresa**</dt> <dt>( \| **tipo de marca 0x9 \_ \_ STRINGREF**)</dt> </dl>                     | Atributo de nome da empresa.<br/>                                                            |
| <span id="TAG_DLLFILE"></span><span id="tag_dllfile"></span><dl> <dt>**Marca \_ de DLLFILE**</dt> <dt>( \| **tipo de marca 0xA \_ \_ STRINGREF**)</dt> </dl>                                     | Atributo de arquivo DLL para uma entrada de Shim.<br/>                                               |
| <span id="TAG_WILDCARD_NAME"></span><span id="tag_wildcard_name"></span><dl> <dt>**Marca \_ de \_Nome do curinga**</dt> <dt>( \| **tipo de marca 0xB \_ \_ STRINGREF**)</dt> </dl>                  | Atributo de nome curinga para uma entrada executável com um curinga como o nome do arquivo.<br/>  |
| <span id="TAG_PRODUCT_NAME"></span><span id="tag_product_name"></span><dl> <dt>**Marca \_ de \_Nome do produto**</dt> <dt>( \| **tipo de marca 0x10 \_ \_ STRINGREF**)</dt> </dl>                    | Atributo de nome do produto.<br/>                                                            |
| <span id="TAG_PRODUCT_VERSION"></span><span id="tag_product_version"></span><dl> <dt>**Marca \_ de \_Versão do produto**</dt> <dt>( \| **tipo de marca 0x11 \_ \_ STRINGREF**)</dt> </dl>           | Atributo de versão do produto.<br/>                                                         |
| <span id="TAG_FILE_DESCRIPTION"></span><span id="tag_file_description"></span><dl> <dt>**Marca \_ de \_Descrição do arquivo**</dt> <dt>( \| **tipo de marca 0x12 \_ \_ STRINGREF**)</dt> </dl>        | Atributo de descrição do arquivo.<br/>                                                        |
| <span id="TAG_FILE_VERSION"></span><span id="tag_file_version"></span><dl> <dt>**Marca \_ de \_Versão do arquivo**</dt> <dt>( \| **tipo de marca 0x13 \_ \_ STRINGREF**)</dt> </dl>                    | Atributo de versão do arquivo.<br/>                                                            |
| <span id="TAG_ORIGINAL_FILENAME"></span><span id="tag_original_filename"></span><dl> <dt>**Marca \_ de \_Nome do arquivo original**</dt> <dt>( \| **tipo de marca 0x14 \_ \_ STRINGREF**)</dt> </dl>     | Atributo de nome de arquivo original.<br/>                                                      |
| <span id="TAG_INTERNAL_NAME"></span><span id="tag_internal_name"></span><dl> <dt>**Marca \_ de \_Nome interno**</dt> <dt>( \| **tipo de marca 0x15 \_ \_ STRINGREF**)</dt> </dl>                 | Atributo de nome de arquivo interno.<br/>                                                      |
| <span id="TAG_LEGAL_COPYRIGHT"></span><span id="tag_legal_copyright"></span><dl> <dt>**Marca \_ de \_Copyright legal**</dt> <dt>( \| **tipo de marca 0x16 \_ \_ STRINGREF**)</dt> </dl>           | Atributo de direitos autorais.<br/>                                                               |
| <span id="TAG_16BIT_DESCRIPTION"></span><span id="tag_16bit_description"></span><dl> <dt>**Tag \_ 16 bits \_ Description**</dt> <dt>(0x17 \| **tag \_ tipo \_ STRINGREF**)</dt> </dl>     | atributo de descrição de 16 bits.<br/>                                                      |
| <span id="TAG_APPHELP_DETAILS"></span><span id="tag_apphelp_details"></span><dl> <dt>**Marca \_ de \_Detalhes de APPHELP**</dt> <dt>( \| **tipo de marca 0x18 \_ \_ STRINGREF**)</dt> </dl>           | Atributo de informações de mensagem de detalhes AppHelp.<br/>                                     |
| <span id="TAG_LINK_URL"></span><span id="tag_link_url"></span><dl> <dt>**Marca \_ de \_URL do link**</dt> <dt>( \| **tipo de marca 0x19 \_ \_ STRINGREF**)</dt> </dl>                                | Atributo de URL de link online AppHelp.<br/>                                                 |
| <span id="TAG_LINK_TEXT"></span><span id="tag_link_text"></span><dl> <dt>**Marca \_ de \_Texto do link**</dt> <dt>( \| **tipo de marca 0x1A \_ \_ STRINGREF**)</dt> </dl>                             | Atributo de texto de link online AppHelp.<br/>                                                |
| <span id="TAG_APPHELP_TITLE"></span><span id="tag_apphelp_title"></span><dl> <dt>**Marca \_ de \_Título APPHELP**</dt> <dt>( \| **tipo de marca 0x1B \_ \_ STRINGREF**)</dt> </dl>                 | Atributo de título AppHelp.<br/>                                                           |
| <span id="TAG_APPHELP_CONTACT"></span><span id="tag_apphelp_contact"></span><dl> <dt>**Marca \_ de \_Contato APPHELP**</dt> <dt>( \| **tipo de marca 0x1C \_ \_ STRINGREF**)</dt> </dl>           | Atributo de contato de fornecedor de AppHelp.<br/>                                                  |
| <span id="TAG_SXS_MANIFEST"></span><span id="tag_sxs_manifest"></span><dl> <dt>**Marca \_ de \_Manifesto SxS**</dt> <dt>( \| **tipo de marca 0x1D \_ \_ STRINGREF**)</dt> </dl>                    | Entrada de manifesto lado a lado.<br/>                                                       |
| <span id="TAG_DATA_STRING"></span><span id="tag_data_string"></span><dl> <dt>**Marca \_ de \_Cadeia de dados**</dt> <dt>( \| **tipo de marca 0x1E \_ \_ STRINGREF**)</dt> </dl>                       | Atributo de cadeia de caracteres para uma entrada de dados.<br/>                                                 |
| <span id="TAG_MSI_TRANSFORM_FILE"></span><span id="tag_msi_transform_file"></span><dl> <dt>**Marca \_ de \_ \_ Arquivo de transformação MSI**</dt> <dt>( \| **tipo de marca 0x1F \_ \_ STRINGREF**)</dt> </dl> | Atributo de nome de arquivo de uma entrada de transformação MSI.<br/>                                |
| <span id="TAG_16BIT_MODULE_NAME"></span><span id="tag_16bit_module_name"></span><dl> <dt>**Tag \_ \_ \_ nome do módulo 16 bits**</dt> <dt>( \| **tipo de marca 0x20 \_ \_ STRINGREF**)</dt> </dl>    | atributo de nome de módulo de 16 bits.<br/>                                                      |
| <span id="TAG_LAYER_DISPLAYNAME"></span><span id="tag_layer_displayname"></span><dl> <dt>**Marca \_ de \_DISPLAYNAME da camada**</dt> <dt>( \| **tipo de marca 0x21 \_ \_ STRINGREF**)</dt> </dl>     | Não utilizado.<br/>                                                                            |
| <span id="TAG_COMPILER_VERSION"></span><span id="tag_compiler_version"></span><dl> <dt>**Marca \_ de \_Versão do compilador**</dt> <dt>( \| **tipo de marca 0x22 \_ \_ STRINGREF**)</dt> </dl>        | Versão do compilador do banco de dados Shim.<br/>                                                    |
| <span id="TAG_ACTION_TYPE"></span><span id="tag_action_type"></span><dl> <dt>**Marca \_ de \_Tipo de ação**</dt> <dt>( \| **tipo de marca 0x23 \_ \_ STRINGREF**)</dt> </dl>                       | Não utilizado.<br/>                                                                            |
| <span id="TAG_EXPORT_NAME"></span><span id="tag_export_name"></span><dl> <dt>**Marca \_ de \_Nome de exportação**</dt> <dt>( \| **tipo de marca 0x24 \_ \_ STRINGREF**)</dt> </dl>                       | Atributo de nome de arquivo de exportação.<br/>                                                        |



As entradas a seguir são do tipo **tag \_ Type \_ DWORD** (0x4000).



| Constante/valor                                                                                                                                                                                                                                                                    | Descrição                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| <span id="TAG_SIZE"></span><span id="tag_size"></span><dl> <dt>**Marca \_ de SIZE**</dt> <dt>( \| **tipo de marca 0x1 \_ \_ DWORD**)</dt> </dl>                                                 | Atributo de tamanho do arquivo.<br/>                                                                                  |
| <span id="TAG_OFFSET"></span><span id="tag_offset"></span><dl> <dt>**Marca \_ de OFFSET**</dt> <dt>( \| **tipo de marca 0x2 \_ \_ DWORD**)</dt> </dl>                                           | Não utilizado.<br/>                                                                                               |
| <span id="TAG_CHECKSUM"></span><span id="tag_checksum"></span><dl> <dt>**Marca \_ de CHECKSUM**</dt> <dt>( \| **tipo de marca 0x3 \_ \_ DWORD**)</dt> </dl>                                     | Atributo de soma de verificação do arquivo.<br/>                                                                              |
| <span id="TAG_SHIM_TAGID"></span><span id="tag_shim_tagid"></span><dl> <dt>**Marca \_ de SHIM \_ TagId**</dt> <dt>( \| **tipo de marca 0x4 \_ \_ DWORD**)</dt> </dl>                              | Atributo **TagId** de Shim.<br/>                                                                             |
| <span id="TAG_PATCH_TAGID"></span><span id="tag_patch_tagid"></span><dl> <dt>**Marca \_ de PATCH \_ TagId**</dt> <dt>( \| **tipo de marca 0x5 \_ \_ DWORD**)</dt> </dl>                           | Atributo **TagId** do patch.<br/>                                                                            |
| <span id="TAG_MODULE_TYPE"></span><span id="tag_module_type"></span><dl> <dt>**Marca \_ de \_Tipo de módulo**</dt> <dt>( \| **tipo de marca 0x6 \_ \_ DWORD**)</dt> </dl>                           | Atributo de tipo de módulo.<br/>                                                                                |
| <span id="TAG_VERDATEHI"></span><span id="tag_verdatehi"></span><dl> <dt>**Marca \_ de VERDATEHI**</dt> <dt>( \| **tipo de marca 0x7 \_ \_ DWORD**)</dt> </dl>                                  | Parte de ordem superior do atributo de data de versão do arquivo.<br/>                                                |
| <span id="TAG_VERDATELO"></span><span id="tag_verdatelo"></span><dl> <dt>**Marca \_ de VERDATELO**</dt> <dt>( \| **tipo de marca 0x8 \_ \_ DWORD**)</dt> </dl>                                  | Parte de ordem inferior do atributo de data de versão do arquivo.<br/>                                                 |
| <span id="TAG_VERFILEOS"></span><span id="tag_verfileos"></span><dl> <dt>**Marca \_ de VERFILEOS**</dt> <dt>( \| **tipo de marca 0x9 \_ \_ DWORD**)</dt> </dl>                                  | Atributo de versão do arquivo do sistema operacional.<br/>                                                              |
| <span id="TAG_VERFILETYPE"></span><span id="tag_verfiletype"></span><dl> <dt>**Marca \_ de VERFILETYPE**</dt> <dt>( \| **tipo de marca 0xA \_ \_ DWORD**)</dt> </dl>                            | Atributo de tipo de arquivo.<br/>                                                                                  |
| <span id="TAG_PE_CHECKSUM"></span><span id="tag_pe_checksum"></span><dl> <dt>**Marca \_ de \_Soma de verificação PE**</dt> <dt>( \| **tipo de marca 0xB \_ \_ DWORD**)</dt> </dl>                           | Atributo de soma de verificação do arquivo PE.<br/>                                                                           |
| <span id="TAG_PREVOSMAJORVER"></span><span id="tag_prevosmajorver"></span><dl> <dt>**Marca \_ de PREVOSMAJORVER**</dt> <dt>( \| **tipo de marca 0xc \_ \_ DWORD**)</dt> </dl>                   | Atributo de versão principal do sistema operacional.<br/>                                                             |
| <span id="TAG_PREVOSMINORVER"></span><span id="tag_prevosminorver"></span><dl> <dt>**Marca \_ de PREVOSMINORVER**</dt> <dt>( \| **tipo de marca 0xD \_ \_ DWORD**)</dt> </dl>                   | Atributo de versão do sistema operacional secundário.<br/>                                                             |
| <span id="TAG_PREVOSPLATFORMID"></span><span id="tag_prevosplatformid"></span><dl> <dt>**Marca \_ de PREVOSPLATFORMID**</dt> <dt>( \| **tipo de marca 0xE \_ \_ DWORD**)</dt> </dl>             | Atributo de identificador da plataforma do sistema operacional.<br/>                                                       |
| <span id="TAG_PREVOSBUILDNO"></span><span id="tag_prevosbuildno"></span><dl> <dt>**Marca \_ de PREVOSBUILDNO**</dt> <dt>( \| **tipo de marca 0xF \_ \_ DWORD**)</dt> </dl>                      | Atributo de número de compilação do sistema operacional.<br/>                                                              |
| <span id="TAG_PROBLEMSEVERITY"></span><span id="tag_problemseverity"></span><dl> <dt>**Marca \_ de PROBLEMSEVERITY**</dt> <dt>( \| **tipo de marca 0x10 \_ \_ DWORD**)</dt> </dl>               | Atributo Block de uma entrada AppHelp. Isso determina se o aplicativo é de bloqueio de hardware ou soft.<br/> |
| <span id="TAG_LANGID"></span><span id="tag_langid"></span><dl> <dt>**Marca \_ de LANGid**</dt> <dt>( \| **tipo de marca 0x11 \_ \_ DWORD**)</dt> </dl>                                          | Identificador de idioma de uma entrada AppHelp.<br/>                                                              |
| <span id="TAG_VER_LANGUAGE"></span><span id="tag_ver_language"></span><dl> <dt>**Marca \_ de \_Linguagem ver**</dt> <dt>( \| **tipo de marca 0x12 \_ \_ DWORD**)</dt> </dl>                       | Atributo de versão de idioma de um arquivo.<br/>                                                                 |
| <span id="TAG_ENGINE"></span><span id="tag_engine"></span><dl> <dt>**Marca \_ de MECANISMO**</dt> <dt>( \| **tipo de marca 0x14 \_ \_ DWORD**)</dt> </dl>                                          | Não utilizado.<br/>                                                                                               |
| <span id="TAG_HTMLHELPID"></span><span id="tag_htmlhelpid"></span><dl> <dt>**Marca \_ de HTMLHELPid**</dt> <dt>( \| **tipo de marca 0x15 \_ \_ DWORD**)</dt> </dl>                              | Atributo de identificador de ajuda para uma entrada AppHelp.<br/>                                                       |
| <span id="TAG_INDEX_FLAGS"></span><span id="tag_index_flags"></span><dl> <dt>**Marca \_ de \_Sinalizadores de índice**</dt> <dt>( \| **tipo de marca 0x16 \_ \_ DWORD**)</dt> </dl>                          | O atributo flags para uma entrada de índice.<br/>                                                                   |
| <span id="TAG_FLAGS"></span><span id="tag_flags"></span><dl> <dt>**Marca \_ de FLAGS**</dt> <dt>( \| **tipo de marca 0x17 \_ \_ DWORD**)</dt> </dl>                                             | Atributo flags para uma entrada AppHelp.<br/>                                                                 |
| <span id="TAG_DATA_VALUETYPE"></span><span id="tag_data_valuetype"></span><dl> <dt>**Marca \_ de \_ValueType de dados**</dt> <dt>( \| **tipo de marca 0x18 \_ \_ DWORD**)</dt> </dl>                 | Atributo de tipo de dados para uma entrada de dados.<br/>                                                                 |
| <span id="TAG_DATA_DWORD"></span><span id="tag_data_dword"></span><dl> <dt>**Marca \_ de DATA \_ DWORD**</dt> <dt>( \| **tipo de marca 0x19 \_ \_ DWORD**)</dt> </dl>                             | Atributo de valor **DWORD** para uma entrada de dados.<br/>                                                           |
| <span id="TAG_LAYER_TAGID"></span><span id="tag_layer_tagid"></span><dl> <dt>**Marca \_ de CAMADA \_ TagId**</dt> <dt>( \| **tipo de marca 0x1A \_ \_ DWORD**)</dt> </dl>                          | Atributo **TagId** de Shim de camada.<br/>                                                                       |
| <span id="TAG_MSI_TRANSFORM_TAGID"></span><span id="tag_msi_transform_tagid"></span><dl> <dt>**Marca \_ de MSI \_ Transform \_ TagId**</dt> <dt>( \| **tipo de marca 0x1B \_ \_ DWORD**)</dt> </dl> | Atributo **TagId** de transformação msi.<br/>                                                                    |
| <span id="TAG_LINKER_VERSION"></span><span id="tag_linker_version"></span><dl> <dt>**Marca \_ de \_Versão do vinculador**</dt> <dt>( \| **tipo de marca 0x1C \_ \_ DWORD**)</dt> </dl>                 | Atributo de versão do vinculador de um arquivo.<br/>                                                                   |
| <span id="TAG_LINK_DATE"></span><span id="tag_link_date"></span><dl> <dt>**Marca \_ de \_Data do link**</dt> <dt>( \| **tipo de marca 0x1D \_ \_ DWORD**)</dt> </dl>                                | Atributo de data de vinculação de um arquivo.<br/>                                                                        |
| <span id="TAG_UPTO_LINK_DATE"></span><span id="tag_upto_link_date"></span><dl> <dt>**Marca \_ de \_ \_ Data do vínculo até**</dt> a <dt>( \| **tipo de marca 0x1E \_ \_ DWORD**)</dt> </dl>                | Atributo de data de vinculação de um arquivo. A correspondência é feita até e inclui essa data de vínculo.<br/>                   |
| <span id="TAG_OS_SERVICE_PACK"></span><span id="tag_os_service_pack"></span><dl> <dt>**Marca \_ de \_Service \_ Pack do so**</dt> <dt>( \| **tipo de marca 0x1F \_ \_ DWORD**)</dt> </dl>             | O sistema operacional service pack atributo para uma entrada executável.<br/>                                      |
| <span id="TAG_FLAG_TAGID"></span><span id="tag_flag_tagid"></span><dl> <dt>**Marca \_ de FLAG \_ TagId**</dt> <dt>( \| **tipo de marca 0x20 \_ \_ DWORD**)</dt> </dl>                             | Sinaliza o atributo **TagId** .<br/>                                                                            |
| <span id="TAG_RUNTIME_PLATFORM"></span><span id="tag_runtime_platform"></span><dl> <dt>**Marca \_ de \_Plataforma de tempo de execução**</dt> <dt>( \| **tipo de marca 0x21 \_ \_ DWORD**)</dt> </dl>           | Atributo de plataforma de tempo de execução de um arquivo.<br/>                                                                |
| <span id="TAG_OS_SKU"></span><span id="tag_os_sku"></span><dl> <dt>**Marca \_ de \_SKU do so**</dt> <dt>( \| **tipo de marca 0x22 \_ \_ DWORD**)</dt> </dl>                                         | Atributo SKU do sistema operacional para uma entrada executável.<br/>                                               |
| <span id="TAG_OS_PLATFORM"></span><span id="tag_os_platform"></span><dl> <dt>**Marca \_ de \_Plataforma do sistema operacional**</dt> <dt>( \| **tipo de marca 0x23 \_ \_ DWORD**)</dt> </dl>                          | Atributo de plataforma do sistema operacional.<br/>                                                                  |
| <span id="TAG_APP_NAME_RC_ID"></span><span id="tag_app_name_rc_id"></span><dl> <dt>**Marca \_ de \_Nome do \_ aplicativo \_ ID RC**</dt> <dt>( \| **tipo de marca 0x24 \_ \_ DWORD**)</dt> </dl>               | Nome do aplicativo atributo do identificador de recurso para entradas AppHelp.<br/>                                   |
| <span id="TAG_VENDOR_NAME_RC_ID"></span><span id="tag_vendor_name_rc_id"></span><dl> <dt>**Marca \_ de \_ \_ \_ ID RC do nome do fornecedor**</dt> <dt>( \| **tipo de marca 0x25 \_ \_ DWORD**)</dt> </dl>      | Nome do fornecedor atributo de identificador de recurso para entradas AppHelp.<br/>                                        |
| <span id="TAG_SUMMARY_MSG_RC_ID"></span><span id="tag_summary_msg_rc_id"></span><dl> <dt>**Marca \_ de \_ \_ \_ ID RC do resumo msg**</dt> <dt>( \| **tipo de marca 0x26 \_ \_ DWORD**)</dt> </dl>      | Atributo de identificador de recurso de mensagem de resumo para entradas AppHelp.<br/>                                    |
| <span id="TAG_VISTA_SKU"></span><span id="tag_vista_sku"></span><dl> <dt>**Marca \_ de \_SKU do vista**</dt> <dt>( \| **tipo de marca 0x27 \_ \_ DWORD**)</dt> </dl>                                | Atributo SKU do Windows Vista.<br/>                                                                          |
| <span id="TAG_DESCRIPTION_RC_ID"></span><span id="tag_description_rc_id"></span><dl> <dt>**Marca \_ de Descrição \_ RC \_ ID**</dt> <dt>( \| **tipo de marca 0x28 \_ \_ DWORD**)</dt> </dl>       | Atributo de identificador de recurso de descrição para entradas de AppHelp.<br/>                                        |
| <span id="TAG_PARAMETER1_RC_ID"></span><span id="tag_parameter1_rc_id"></span><dl> <dt>**Marca \_ de \_ \_ ID do parâmetro1 RC**</dt> <dt>( \| **tipo de marca 0x29 \_ \_ DWORD**)</dt> </dl>          | Atributo de identificador de recurso parâmetro1 para entradas AppHelp.<br/>                                         |
| <span id="TAG_TAGID"></span><span id="tag_tagid"></span><dl> <dt>**Marca \_ de TAGID**</dt> <dt>( \| **tipo de marca 0x801 \_ \_ DWORD**)</dt> </dl>                                            | Atributo **TagId** .<br/>                                                                                  |



A entrada a seguir é do tipo **tag \_ Type \_ String** (0x8000).



| Constante/valor                                                                                                                                                                                                                                                            | Descrição                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------|
| <span id="TAG_STRINGTABLE_ITEM"></span><span id="tag_stringtable_item"></span><dl> <dt>**Marca \_ de \_Item STRINGTABLE**</dt> <dt>( \| **cadeia de \_ \_ caracteres de tipo de marca** 0x801)</dt> </dl> | Entrada de item de tabela de cadeia de caracteres.<br/> |



As entradas a seguir são do tipo **marca \_ tipo \_ NULL** (0x1000).



| Constante/valor                                                                                                                                                                                                                                                                            | Descrição                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span id="TAG_INCLUDE"></span><span id="tag_include"></span><dl> <dt>**Marca \_ de INCLUDE**</dt> <dt>( \| **tipo de marca 0x1 \_ \_ nulo**)</dt> </dl>                                                 | Incluir entrada de lista.<br/>                           |
| <span id="TAG_GENERAL"></span><span id="tag_general"></span><dl> <dt>**Marca \_ de GERAL**</dt> <dt>( \| **tipo de marca 0x2 \_ \_ nulo**)</dt> </dl>                                                 | Entrada de correção de uso geral.<br/>                   |
| <span id="TAG_MATCH_LOGIC_NOT"></span><span id="tag_match_logic_not"></span><dl> <dt>**Marca \_ de Lógica de correspondência \_ \_ não**</dt> <dt>( \| **tipo de marca 0x3 \_ \_ nulo**)</dt> </dl>                       | Não é uma entrada de lógica correspondente.<br/>                  |
| <span id="TAG_APPLY_ALL_SHIMS"></span><span id="tag_apply_all_shims"></span><dl> <dt>**Marca \_ de APLICAR \_ todos os \_ shims**</dt> <dt>( \| **tipo de marca 0x4 \_ \_ nulo**)</dt> </dl>                       | Não utilizado.<br/>                                       |
| <span id="TAG_USE_SERVICE_PACK_FILES"></span><span id="tag_use_service_pack_files"></span><dl> <dt>**Marca \_ de USAR \_ \_ \_ arquivos do Service Pack**</dt> <dt>( \| **tipo de marca 0x5 \_ \_ nulo**)</dt> </dl> | Informações do Service Pack para entradas AppHelp.<br/> |
| <span id="TAG_MITIGATION_OS"></span><span id="tag_mitigation_os"></span><dl> <dt>**Marca \_ de \_Sistema operacional de mitigação**</dt> <dt>( \| **tipo de marca 0x6 \_ \_ nulo**)</dt> </dl>                              | Mitigação na entrada de escopo do sistema operacional.<br/>   |
| <span id="TAG_BLOCK_UPGRADE"></span><span id="tag_block_upgrade"></span><dl> <dt>**Marca \_ de BLOQUEAR \_ atualização**</dt> <dt>( \| **tipo de marca 0x7 \_ \_ nulo**)</dt> </dl>                              | Atualizar entrada de bloco.<br/>                          |
| <span id="TAG_INCLUDEEXCLUDEDLL"></span><span id="tag_includeexcludedll"></span><dl> <dt>**Marca \_ de INCLUDEEXCLUDEDLL**</dt> <dt>( \| **tipo de marca 0x8 \_ \_ nulo**)</dt> </dl>                   | Entrada de inclusão/exclusão de DLL.<br/>                    |



As entradas a seguir são do tipo **marca \_ tipo \_ QWORD** (0x5000).



| Constante/valor                                                                                                                                                                                                                                                                                   | Descrição                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TAG_TIME"></span><span id="tag_time"></span><dl> <dt>**Marca \_ de TIME**</dt> <dt>( \| **tipo de marca 0x1 \_ \_ QWORD**)</dt> </dl>                                                                | Atributo de tempo.<br/>                                                                                     |
| <span id="TAG_BIN_FILE_VERSION"></span><span id="tag_bin_file_version"></span><dl> <dt>**Marca \_ de \_ \_ Versão do arquivo bin**</dt> <dt>( \| **tipo de marca 0x2 \_ \_ QWORD**)</dt> </dl>                          | Atributo de versão do arquivo bin para entradas de arquivo.<br/>                                                        |
| <span id="TAG_BIN_PRODUCT_VERSION"></span><span id="tag_bin_product_version"></span><dl> <dt>**Marca \_ de \_ \_ Versão do produto bin**</dt> <dt>( \| **tipo de marca 0x3 \_ \_ QWORD**)</dt> </dl>                 | Atributo de versão do produto bin para entradas de arquivo.<br/>                                                     |
| <span id="TAG_MODTIME"></span><span id="tag_modtime"></span><dl> <dt>**Marca \_ de MODTIME**</dt> <dt>( \| **tipo de marca 0x4 \_ \_ QWORD**)</dt> </dl>                                                       | Não utilizado.<br/>                                                                                             |
| <span id="TAG_FLAG_MASK_KERNEL"></span><span id="tag_flag_mask_kernel"></span><dl> <dt>**Marca \_ de \_ \_ Kernel de máscara de sinalizador**</dt> <dt>( \| **tipo de marca 0x5 \_ \_ QWORD**)</dt> </dl>                          | Atributo de máscara do sinalizador do kernel.<br/>                                                                         |
| <span id="TAG_UPTO_BIN_PRODUCT_VERSION"></span><span id="tag_upto_bin_product_version"></span><dl> <dt>**Marca \_ de \_Versão do \_ produto \_**</dt> de no-bin <dt>( \| **tipo de marca 0x6 \_ \_ QWORD**)</dt> </dl> | Atributo de versão do produto bin de um arquivo. A correspondência é feita até e incluindo esta versão do produto.<br/> |
| <span id="TAG_DATA_QWORD"></span><span id="tag_data_qword"></span><dl> <dt>**Marca \_ de DADOS \_ QWORD**</dt> <dt>( \| **tipo de marca 0x7 \_ \_ QWORD**)</dt> </dl>                                             | Atributo de valor **ULONGLONG** para uma entrada de dados.<br/>                                                     |
| <span id="TAG_FLAG_MASK_USER"></span><span id="tag_flag_mask_user"></span><dl> <dt>**Marca \_ de SINALIZADOR \_ de \_ usuário de máscara**</dt> <dt>(tipo de \| **marca 0x8 \_ \_ QWORD**)</dt> </dl>                                | Atributo de máscara de sinalizador do usuário.<br/>                                                                           |
| <span id="TAG_FLAGS_NTVDM1"></span><span id="tag_flags_ntvdm1"></span><dl> <dt>**Marca \_ de FLAGS \_ NTVDM1**</dt> <dt>( \| **tipo de marca 0x9 \_ \_ QWORD**)</dt> </dl>                                       | Atributo de máscara de sinalizador NTVDM1.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM2"></span><span id="tag_flags_ntvdm2"></span><dl> <dt>**Marca \_ de FLAGS \_ NTVDM2**</dt> <dt>( \| **tipo de marca 0xA \_ \_ QWORD**)</dt> </dl>                                       | Atributo de máscara de sinalizador NTVDM2.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM3"></span><span id="tag_flags_ntvdm3"></span><dl> <dt>**Marca \_ de FLAGS \_ NTVDM3**</dt> <dt>( \| **tipo de marca 0xB \_ \_ QWORD**)</dt> </dl>                                       | Atributo de máscara de sinalizador NTVDM3.<br/>                                                                         |
| <span id="TAG_FLAG_MASK_SHELL"></span><span id="tag_flag_mask_shell"></span><dl> <dt>**Marca \_ de \_ \_ Shell de máscara de sinalizador**</dt> <dt>( \| **tipo de marca 0xc \_ \_ QWORD**)</dt> </dl>                             | Atributo de máscara do sinalizador do Shell.<br/>                                                                          |
| <span id="TAG_UPTO_BIN_FILE_VERSION"></span><span id="tag_upto_bin_file_version"></span><dl> <dt>**Marca \_ de \_Versão do \_ arquivo \_ de até o compartimento**</dt> <dt>( \| **tipo de marca 0xD \_ \_ QWORD**)</dt> </dl>          | Atributo de versão do arquivo bin de um arquivo. A correspondência é feita até e incluindo essa versão de arquivo.<br/>       |
| <span id="TAG_FLAG_MASK_FUSION"></span><span id="tag_flag_mask_fusion"></span><dl> <dt>**Marca \_ de Máscara de sinalizador \_ \_ Fusion**</dt> <dt>( \| **tipo de marca 0xE \_ \_ QWORD**)</dt> </dl>                          | Atributo de máscara do sinalizador de fusão.<br/>                                                                         |
| <span id="TAG_FLAG_PROCESSPARAM"></span><span id="tag_flag_processparam"></span><dl> <dt>**Marca \_ de FLAG \_ PROCESSPARAM**</dt> <dt>( \| **tipo de marca 0xF \_ \_ QWORD**)</dt> </dl>                        | Atributo de sinalizador de parâmetro de processo.<br/>                                                                       |
| <span id="TAG_FLAG_LUA"></span><span id="tag_flag_lua"></span><dl> <dt>**Marca \_ de FLAG \_ lua**</dt> <dt>( \| **tipo de marca 0x10 \_ \_ QWORD**)</dt> </dl>                                                  | Atributo de sinalizador de LUA.<br/>                                                                                 |
| <span id="TAG_FLAG_INSTALL"></span><span id="tag_flag_install"></span><dl> <dt>**Marca \_ de SINALIZAr \_ instalação**</dt> <dt>( \| **tipo de marca 0x11 \_ \_ QWORD**)</dt> </dl>                                      | Instalar o atributo de sinalizador.<br/>                                                                             |



As entradas a seguir são do **tipo \_ tipo \_ de marca Binary** (0x9000).



| Constante/valor                                                                                                                                                                                                                                                     | Descrição                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="TAG_PATCH_BITS"></span><span id="tag_patch_bits"></span><dl> <dt>**Marca \_ de PATCH \_ bits**</dt> <dt>( \| **tipo de marca 0x2 \_ \_ Binary**)</dt> </dl>              | Atributo bits do arquivo de patch.<br/>                          |
| <span id="TAG_FILE_BITS"></span><span id="tag_file_bits"></span><dl> <dt>**Marca \_ de \_Bits de arquivo**</dt> <dt>( \| **tipo de marca 0x3 \_ \_ Binary**)</dt> </dl>                 | Atributo bits de arquivo.<br/>                                |
| <span id="TAG_EXE_ID"></span><span id="tag_exe_id"></span><dl> <dt>**Marca \_ de \_ID exe**</dt> <dt>( \| **tipo de marca 0x4 \_ \_ Binary**)</dt> </dl>                          | Atributo **GUID** de uma entrada executável.<br/>          |
| <span id="TAG_DATA_BITS"></span><span id="tag_data_bits"></span><dl> <dt>**Marca \_ de \_Bits de dados**</dt> <dt>( \| **tipo de marca 0x5 \_ \_ Binary**)</dt> </dl>                 | Atributo de bits de dados.<br/>                                |
| <span id="TAG_MSI_PACKAGE_ID"></span><span id="tag_msi_package_id"></span><dl> <dt>**Marca \_ de \_ \_ ID do pacote MSI**</dt> <dt>( \| **tipo de marca 0x6 \_ \_ Binary**)</dt> </dl> | Atributo de identificador de pacote MSI de um pacote MSI.<br/> |
| <span id="TAG_DATABASE_ID"></span><span id="tag_database_id"></span><dl> <dt>**Marca \_ de \_ID do banco de dados**</dt> <dt>( \| **tipo de marca 0x7 \_ \_ Binary**)</dt> </dl>           | Atributo de **GUID** de um banco de dados.<br/>                   |
| <span id="TAG_INDEX_BITS"></span><span id="tag_index_bits"></span><dl> <dt>**Marca \_ de \_Bits de índice**</dt> <dt>( \| **tipo de marca 0x801 \_ \_ Binary**)</dt> </dl>            | Atributo de bits de índice.<br/>                               |



As entradas a seguir são do **tipo \_ tipo \_ de marca Word** (0x3000).



| Constante/valor                                                                                                                                                                                                                                      | Descrição                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="TAG_MATCH_MODE"></span><span id="tag_match_mode"></span><dl> <dt>**Marca \_ de \_Modo de correspondência**</dt> <dt>( \| **tipo de marca 0x1 \_ \_ palavra**)</dt> </dl> | Atributo de modo de correspondência.<br/>                   |
| <span id="TAG_TAG"></span><span id="tag_tag"></span><dl> <dt>**Marca \_ de TAG**</dt> <dt>( \| **tipo de marca 0x801 \_ \_ Word**)</dt> </dl>                     | Entrada de marca.<br/>                              |
| <span id="TAG_INDEX_TAG"></span><span id="tag_index_tag"></span><dl> <dt>**Marca \_ de \_Marca de índice**</dt> <dt>( \| **tipo de marca 0x802 \_ \_ palavra**)</dt> </dl>  | Atributo de marca de índice para uma entrada de índice.<br/> |
| <span id="TAG_INDEX_KEY"></span><span id="tag_index_key"></span><dl> <dt>**Marca \_ de \_Chave de índice**</dt> <dt>( \| **tipo de marca 0x803 \_ \_ Word**)</dt> </dl>  | Atributo de chave de índice para uma entrada de índice.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Exposeenums2managed. h (incluir Axextendenums. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos de marca](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




