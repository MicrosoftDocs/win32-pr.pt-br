---
title: Códigos de erro de roteamento e acesso remoto
description: Os seguintes códigos de erro de API de Roteamento e Acesso Remoto (RRAS) são definidos em raserror.h.
ms.assetid: 1fa41438-7c93-4e9c-851c-652fba23da4f
topic_type:
- apiref
api_name:
- Routing and Remote Access Error Codes
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7bd68c31ef2b92cce75059d5d86ee68dc65d1151
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624322"
---
# <a name="routing-and-remote-access-error-codes"></a>Códigos de erro de roteamento e acesso remoto

Os seguintes códigos de erro de API de Roteamento e Acesso Remoto (RRAS) são definidos em raserror.h. Todos os códigos de erro têm suporte no Windows 2000 ou versões posteriores do Windows a menos que especificado de outra forma.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valor/código de retorno</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="PENDING"></span><span id="pending"></span><dl> <dt><strong>PENDENTE</strong></dt> <dt>600</dt> </dl></td>
<td>Uma operação está pendente.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PORT_HANDLE"></span><span id="error_invalid_port_handle"></span><dl> <dt><strong>ERROR_INVALID_PORT_HANDLE</strong></dt> <dt>601</dt> </dl></td>
<td>O alça de porta fornecido não é válido.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_ALREADY_OPEN"></span><span id="error_port_already_open"></span><dl> <dt><strong>ERROR_PORT_ALREADY_OPEN</strong></dt> <dt>602</dt> </dl></td>
<td>A porta especificada já está aberta.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BUFFER_TOO_SMALL"></span><span id="error_buffer_too_small"></span><dl> <dt><strong>ERROR_BUFFER_TOO_SMALL</strong></dt> <dt>603</dt> </dl></td>
<td>O buffer fornecido é muito pequeno.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_INFO_SPECIFIED"></span><span id="error_wrong_info_specified"></span><dl> <dt><strong>ERROR_WRONG_INFO_SPECIFIED</strong></dt> <dt>604</dt> </dl></td>
<td>As informações de porta especificadas estão incorretas.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SET_PORT_INFO"></span><span id="error_cannot_set_port_info"></span><dl> <dt><strong>ERROR_CANNOT_SET_PORT_INFO</strong></dt> <dt>605</dt> </dl></td>
<td>As informações de porta especificadas não podem ser definidas.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_CONNECTED"></span><span id="error_port_not_connected"></span><dl> <dt><strong>ERROR_PORT_NOT_CONNECTED</strong></dt> <dt>606</dt> </dl></td>
<td>A porta especificada não está conectada.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EVENT_INVALID"></span><span id="error_event_invalid"></span><dl> <dt><strong>ERROR_EVENT_INVALID</strong></dt> <dt>607</dt> </dl></td>
<td>Um evento que não é válido foi detectado.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_DOES_NOT_EXIST"></span><span id="error_device_does_not_exist"></span><dl> <dt><strong>ERROR_DEVICE_DOES_NOT_EXIST</strong></dt> <dt>608</dt> </dl></td>
<td>O dispositivo especificado não existe.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICETYPE_DOES_NOT_EXIST"></span><span id="error_devicetype_does_not_exist"></span><dl> <dt><strong>ERROR_DEVICETYPE_DOES_NOT_EXIST</strong></dt> <dt>609</dt> </dl></td>
<td>O tipo de dispositivo especificado não existe.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUFFER_INVALID"></span><span id="error_buffer_invalid"></span><dl> <dt><strong>ERROR_BUFFER_INVALID</strong></dt> <dt>610</dt> </dl></td>
<td>O buffer fornecido não é válido.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTE_NOT_AVAILABLE"></span><span id="error_route_not_available"></span><dl> <dt><strong>ERROR_ROUTE_NOT_AVAILABLE</strong></dt> <dt>611</dt> </dl></td>
<td>Foi especificada uma rota que não está disponível.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ROUTE_NOT_ALLOCATED"></span><span id="error_route_not_allocated"></span><dl> <dt><strong>ERROR_ROUTE_NOT_ALLOCATED</strong></dt> <dt>612</dt> </dl></td>
<td>A rota especificada não está alocada.<br/></td>
</tr>
<tr class="even">
<td><span id="ERRERROR_INVALID_COMPRESSION_SPECIFIED"></span><span id="errerror_invalid_compression_specified"></span><dl> <dt><strong>ERRERROR_INVALID_COMPRESSION_SPECIFIED</strong></dt> <dt>613</dt> </dl></td>
<td>A compactação especificada não é válida.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OUT_OF_BUFFERS"></span><span id="error_out_of_buffers"></span><dl> <dt><strong>ERROR_OUT_OF_BUFFERS</strong></dt> <dt>614</dt> </dl></td>
<td>Não havia buffers suficientes disponíveis.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_FOUND_"></span><span id="error_port_not_found_"></span><dl> <dt> <strong>ERROR_PORT_NOT_FOUND</strong> </dt> <dt>615</dt> </dl></td>
<td>A porta especificada não foi encontrada.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ASYNC_REQUEST_PENDING"></span><span id="error_async_request_pending"></span><dl> <dt><strong>ERROR_ASYNC_REQUEST_PENDING</strong></dt> <dt>616</dt> </dl></td>
<td>Uma solicitação assíncrona está pendente.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_DISCONNECTING"></span><span id="error_already_disconnecting"></span><dl> <dt><strong>ERROR_ALREADY_DISCONNECTING</strong></dt> <dt>617</dt> </dl></td>
<td>A porta ou o dispositivo especificado já está desconectando.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_NOT_OPEN"></span><span id="error_port_not_open"></span><dl> <dt><strong>ERROR_PORT_NOT_OPEN</strong></dt> <dt>618</dt> </dl></td>
<td>A porta especificada não está aberta.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_DISCONNECTED"></span><span id="error_port_disconnected"></span><dl> <dt><strong>ERROR_PORT_DISCONNECTED</strong></dt> <dt>619</dt> </dl></td>
<td>A porta especificada está desconectada.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ENDPOINTS"></span><span id="error_no_endpoints"></span><dl> <dt><strong>ERROR_NO_ENDPOINTS</strong></dt> <dt>620</dt> </dl></td>
<td>Nenhum ponto de extremidade pode ser determinado.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_OPEN_PHONEBOOK"></span><span id="error_cannot_open_phonebook"></span><dl> <dt><strong>ERROR_CANNOT_OPEN_PHONEBOOK</strong></dt> <dt>621</dt> </dl></td>
<td>Não é possível abrir o arquivo de agenda telefônica especificado.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_PHONEBOOK"></span><span id="error_cannot_load_phonebook"></span><dl> <dt><strong>ERROR_CANNOT_LOAD_PHONEBOOK</strong></dt> <dt>622</dt> </dl></td>
<td>Não é possível carregar o arquivo de agenda telefônica especificado.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_FIND_PHONEBOOK_ENTRY"></span><span id="error_cannot_find_phonebook_entry"></span><dl> <dt><strong>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</strong></dt> <dt>623</dt> </dl></td>
<td>Não é possível encontrar a entrada de lista telefônica especificada.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_WRITE_PHONEBOOK"></span><span id="error_cannot_write_phonebook"></span><dl> <dt><strong>ERROR_CANNOT_WRITE_PHONEBOOK</strong></dt> <dt>624</dt> </dl></td>
<td>Não é possível gravar no arquivo de lista telefônica especificado.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CORRUPT_PHONEBOOK"></span><span id="error_corrupt_phonebook"></span><dl> <dt><strong>ERROR_CORRUPT_PHONEBOOK</strong></dt> <dt>625</dt> </dl></td>
<td>As informações encontradas na lista telefônica especificada não são válidas.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_LOAD_STRING"></span><span id="error_cannot_load_string"></span><dl> <dt><strong>ERROR_CANNOT_LOAD_STRING</strong></dt> <dt>626</dt> </dl></td>
<td>Não foi possível carregar uma cadeia de caracteres.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_KEY_NOT_FOUND"></span><span id="error_key_not_found"></span><dl> <dt><strong>ERROR_KEY_NOT_FOUND</strong></dt> <dt>627</dt> </dl></td>
<td>Não é possível encontrar a chave especificada.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DISCONNECTION"></span><span id="error_disconnection"></span><dl> <dt><strong>ERROR_DISCONNECTION</strong></dt> <dt>628</dt> </dl></td>
<td>A porta especificada foi desconectada.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_DISCONNECTION"></span><span id="error_remote_disconnection"></span><dl> <dt><strong>ERROR_REMOTE_DISCONNECTION</strong></dt> <dt>629</dt> </dl></td>
<td>A porta especificada foi desconectada pelo computador remoto.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HARDWARE_FAILURE"></span><span id="error_hardware_failure"></span><dl> <dt><strong>ERROR_HARDWARE_FAILURE</strong></dt> <dt>630</dt> </dl></td>
<td>A porta especificada foi desconectada devido a uma falha de hardware.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_DISCONNECTION"></span><span id="error_user_disconnection"></span><dl> <dt><strong>ERROR_USER_DISCONNECTION</strong></dt> <dt>631</dt> </dl></td>
<td>A porta especificada foi desconectada pelo usuário.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIZE"></span><span id="error_invalid_size"></span><dl> <dt><strong>ERROR_INVALID_SIZE</strong></dt> <dt>632</dt> </dl></td>
<td>Tamanho incorreto da estrutura.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_AVAILABLE"></span><span id="error_port_not_available"></span><dl> <dt><strong>ERROR_PORT_NOT_AVAILABLE</strong></dt> <dt>633</dt> </dl></td>
<td>A porta especificada já está em uso ou não está configurada para discagem de acesso remoto.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_PROJECT_CLIENT"></span><span id="error_cannot_project_client"></span><dl> <dt><strong>ERROR_CANNOT_PROJECT_CLIENT</strong></dt> <dt>634</dt> </dl></td>
<td>Não foi possível registrar seu computador na rede remota.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN"></span><span id="error_unknown"></span><dl> <dt><strong>ERROR_UNKNOWN</strong></dt> <dt>635</dt> </dl></td>
<td>Ocorreu um erro desconhecido.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_DEVICE_ATTACHED"></span><span id="error_wrong_device_attached"></span><dl> <dt><strong>ERROR_WRONG_DEVICE_ATTACHED</strong></dt> <dt>636</dt> </dl></td>
<td>O dispositivo errado está anexado à porta especificada.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_STRING"></span><span id="error_bad_string"></span><dl> <dt><strong>ERROR_BAD_STRING</strong></dt> <dt>637</dt> </dl></td>
<td>Foi detectada uma cadeia de caracteres que não pôde ser convertida.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REQUEST_TIMEOUT"></span><span id="error_request_timeout"></span><dl> <dt><strong>ERROR_REQUEST_TIMEOUT</strong></dt> <dt>638</dt> </dl></td>
<td>O tempo limite da solicitação foi atingido.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_GET_LANA"></span><span id="error_cannot_get_lana"></span><dl> <dt><strong>ERROR_CANNOT_GET_LANA</strong></dt> <dt>639</dt> </dl></td>
<td>Nenhuma rede assíncrona está disponível.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NETBIOS_ERROR"></span><span id="error_netbios_error"></span><dl> <dt><strong>ERROR_NETBIOS_ERROR</strong></dt> <dt>640</dt> </dl></td>
<td>Ocorreu um erro envolvendo NetBIOS.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_OUT_OF_RESOURCES"></span><span id="error_server_out_of_resources"></span><dl> <dt><strong>ERROR_SERVER_OUT_OF_RESOURCES</strong></dt> <dt>641</dt> </dl></td>
<td>o servidor de ti não pode alocar os recursos de NetBIOS necessários para dar suporte ao cliente.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NAME_EXISTS_ON_NET"></span><span id="error_name_exists_on_net"></span><dl> <dt><strong>ERROR_NAME_EXISTS_ON_NET</strong></dt> <dt>642</dt> </dl></td>
<td>Um dos nomes NetBIOS do seu computador já está registrado na rede remota.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SERVER_GENERAL_NET_FAILURE"></span><span id="error_server_general_net_failure"></span><dl> <dt><strong>ERROR_SERVER_GENERAL_NET_FAILURE</strong></dt> <dt>643</dt> </dl></td>
<td>Falha em um adaptador de rede no servidor.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_MSG_ALIAS_NOT_ADDED"></span><span id="warning_msg_alias_not_added"></span><dl> <dt><strong>WARNING_MSG_ALIAS_NOT_ADDED</strong></dt> <dt>644</dt> </dl></td>
<td>Você não receberá pop-ups de mensagem de rede.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_INTERNAL"></span><span id="error_auth_internal"></span><dl> <dt><strong>ERROR_AUTH_INTERNAL</strong></dt> <dt>645</dt> </dl></td>
<td>Ocorreu um erro interno de autenticação.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RESTRICTED_LOGON_HOURS"></span><span id="error_restricted_logon_hours"></span><dl> <dt><strong>ERROR_RESTRICTED_LOGON_HOURS</strong></dt> <dt>646</dt> </dl></td>
<td>A conta especificada não tem permissão para fazer logon nesta hora do dia.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCT_DISABLED"></span><span id="error_acct_disabled"></span><dl> <dt><strong>ERROR_ACCT_DISABLED</strong></dt> <dt>647</dt> </dl></td>
<td>A conta especificada está desabilitada.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PASSWD_EXPIRED"></span><span id="error_passwd_expired"></span><dl> <dt><strong>ERROR_PASSWD_EXPIRED</strong></dt> <dt>648</dt> </dl></td>
<td>A senha especificada expirou.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_DIALIN_PERMISSION"></span><span id="error_no_dialin_permission"></span><dl> <dt><strong>ERROR_NO_DIALIN_PERMISSION</strong></dt> <dt>649</dt> </dl></td>
<td>A conta especificada não tem permissões de acesso remoto.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_NOT_RESPONDING"></span><span id="error_server_not_responding"></span><dl> <dt><strong>ERROR_SERVER_NOT_RESPONDING</strong></dt> <dt>650</dt> </dl></td>
<td>O servidor de acesso remoto não está respondendo.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FROM_DEVICE"></span><span id="error_from_device"></span><dl> <dt><strong>ERROR_FROM_DEVICE</strong></dt> <dt>651</dt> </dl></td>
<td>O modem ou outro dispositivo de conexão relatou um erro.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNRECOGNIZED_RESPONSE"></span><span id="error_unrecognized_response"></span><dl> <dt><strong>ERROR_UNRECOGNIZED_RESPONSE</strong></dt> <dt>652</dt> </dl></td>
<td>Uma resposta não reconhecida foi retornada pelo dispositivo.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MACRO_NOT_FOUND"></span><span id="error_macro_not_found"></span><dl> <dt><strong>ERROR_MACRO_NOT_FOUND</strong></dt> <dt>653</dt> </dl></td>
<td>Uma macro exigida pelo dispositivo não foi encontrada no dispositivo. Seção de arquivo INF.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MACRO_NOT_DEFINED"></span><span id="error_macro_not_defined"></span><dl> <dt><strong>ERROR_MACRO_NOT_DEFINED</strong></dt> <dt>654</dt> </dl></td>
<td>Um comando ou resposta no dispositivo. A seção arquivo INF refere-se a uma macro indefinida.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MESSAGE_MACRO_NOT_FOUND"></span><span id="error_message_macro_not_found"></span><dl> <dt><strong>ERROR_MESSAGE_MACRO_NOT_FOUND</strong></dt> <dt>655</dt> </dl></td>
<td>A <message> macro não foi encontrada no dispositivo. Seção de arquivo INF.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEFAULTOFF_MACRO_NOT_FOUND"></span><span id="error_defaultoff_macro_not_found"></span><dl> <dt><strong>ERROR_DEFAULTOFF_MACRO_NOT_FOUND</strong></dt> <dt>656</dt> </dl></td>
<td>A <defaultoff> macro no dispositivo. A seção arquivo INF contém uma macro indefinida.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FILE_COULD_NOT_BE_OPENED"></span><span id="error_file_could_not_be_opened"></span><dl> <dt><strong>ERROR_FILE_COULD_NOT_BE_OPENED</strong></dt> <dt>657</dt> </dl></td>
<td>O dispositivo. Não foi possível abrir o arquivo INF.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICENAME_TOO_LONG"></span><span id="error_devicename_too_long"></span><dl> <dt><strong>ERROR_DEVICENAME_TOO_LONG</strong></dt> <dt>658</dt> </dl></td>
<td>O nome do dispositivo no dispositivo. INF ou o arquivo de .INI de mídia é muito longo. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DEVICENAME_NOT_FOUND"></span><span id="error_devicename_not_found"></span><dl> <dt><strong>ERROR_DEVICENAME_NOT_FOUND</strong></dt> <dt>659</dt> </dl></td>
<td>O arquivo de .INI de mídia refere-se a um nome de dispositivo desconhecido.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RESPONSES"></span><span id="error_no_responses"></span><dl> <dt><strong>ERROR_NO_RESPONSES</strong></dt> <dt>660</dt> </dl></td>
<td>O dispositivo. O arquivo INF não contém nenhuma resposta para o comando.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_COMMAND_FOUND"></span><span id="error_no_command_found"></span><dl> <dt><strong>ERROR_NO_COMMAND_FOUND</strong></dt> <dt>661</dt> </dl></td>
<td>O dispositivo. O arquivo INF não tem um comando.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_KEY_SPECIFIED"></span><span id="error_wrong_key_specified"></span><dl> <dt><strong>ERROR_WRONG_KEY_SPECIFIED</strong></dt> <dt>662</dt> </dl></td>
<td>Tentativa de definir uma macro não listada no dispositivo. Seção de arquivo INF.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNKNOWN_DEVICE_TYPE"></span><span id="error_unknown_device_type"></span><dl> <dt><strong>ERROR_UNKNOWN_DEVICE_TYPE</strong></dt> <dt>663</dt> </dl></td>
<td>O arquivo de .INI de mídia refere-se a um tipo de dispositivo desconhecido.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALLOCATING_MEMORY"></span><span id="error_allocating_memory"></span><dl> <dt><strong>ERROR_ALLOCATING_MEMORY</strong></dt> <dt>664</dt> </dl></td>
<td>Não é possível alocar memória.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_NOT_CONFIGURED"></span><span id="error_port_not_configured"></span><dl> <dt><strong>ERROR_PORT_NOT_CONFIGURED</strong></dt> <dt>665</dt> </dl></td>
<td>A porta não está configurada para acesso remoto.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DEVICE_NOT_READY"></span><span id="error_device_not_ready"></span><dl> <dt><strong>ERROR_DEVICE_NOT_READY</strong></dt> <dt>666</dt> </dl></td>
<td>Seu modem ou outro dispositivo de conexão não está funcionando.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_INI_FILE"></span><span id="error_reading_ini_file"></span><dl> <dt><strong>ERROR_READING_INI_FILE</strong></dt> <dt>667</dt> </dl></td>
<td>Não é possível ler o arquivo de .INI de mídia.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CONNECTION"></span><span id="error_no_connection"></span><dl> <dt><strong>ERROR_NO_CONNECTION</strong></dt> <dt>668</dt> </dl></td>
<td>A conexão foi eliminada.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_USAGE_IN_INI_FILE"></span><span id="error_bad_usage_in_ini_file"></span><dl> <dt><strong>ERROR_BAD_USAGE_IN_INI_FILE</strong></dt> <dt>669</dt> </dl></td>
<td>O parâmetro de uso no arquivo de .ini de mídia não é válido.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SECTIONNAME"></span><span id="error_reading_sectionname"></span><dl> <dt><strong>ERROR_READING_SECTIONNAME</strong></dt> <dt>670</dt> </dl></td>
<td>Não é possível ler o nome da seção do arquivo de .INI de mídia.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEVICETYPE"></span><span id="error_reading_devicetype"></span><dl> <dt><strong>ERROR_READING_DEVICETYPE</strong></dt> <dt>671</dt> </dl></td>
<td>Não é possível ler o tipo de dispositivo do arquivo de .INI de mídia.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_DEVICENAME"></span><span id="error_reading_devicename"></span><dl> <dt><strong>ERROR_READING_DEVICENAME</strong></dt> <dt>672</dt> </dl></td>
<td>Não é possível ler o nome do dispositivo do arquivo de .INI de mídia.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_USAGE"></span><span id="error_reading_usage"></span><dl> <dt><strong>ERROR_READING_USAGE</strong></dt> <dt>673</dt> </dl></td>
<td>Não é possível ler o uso do arquivo de .INI de mídia.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_MAXCONNECTBPS"></span><span id="error_reading_maxconnectbps"></span><dl> <dt><strong>ERROR_READING_MAXCONNECTBPS</strong></dt> <dt>674</dt> </dl></td>
<td>O sistema não pôde ler a velocidade máxima de conexão da operadora do arquivo de .INI de mídia.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_MAXCARRIERBPS"></span><span id="error_reading_maxcarrierbps"></span><dl> <dt><strong>ERROR_READING_MAXCARRIERBPS</strong></dt> <dt>675</dt> </dl></td>
<td>Não é possível ler o uso do arquivo de .INI de mídia.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_LINE_BUSY"></span><span id="error_line_busy"></span><dl> <dt><strong>ERROR_LINE_BUSY</strong></dt> <dt>676</dt> </dl></td>
<td>A linha está ocupada.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VOICE_ANSWER"></span><span id="error_voice_answer"></span><dl> <dt><strong>ERROR_VOICE_ANSWER</strong></dt> <dt>677</dt> </dl></td>
<td>Uma pessoa respondeu em vez de um modem.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ANSWER"></span><span id="error_no_answer"></span><dl> <dt><strong>ERROR_NO_ANSWER</strong></dt> <dt>678</dt> </dl></td>
<td>Não há resposta.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_CARRIER"></span><span id="error_no_carrier"></span><dl> <dt><strong>ERROR_NO_CARRIER</strong></dt> <dt>679</dt> </dl></td>
<td>Não é possível detectar um sinal de operador.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIALTONE"></span><span id="error_no_dialtone"></span><dl> <dt><strong>ERROR_NO_DIALTONE</strong></dt> <dt>680</dt> </dl></td>
<td>Não há nenhum tom de discagem.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IN_COMMAND"></span><span id="error_in_command"></span><dl> <dt><strong>ERROR_IN_COMMAND</strong></dt> <dt>681</dt> </dl></td>
<td>O modem (ou outro dispositivo de conexão) relatou um erro geral.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_SECTIONNAME"></span><span id="error_writing_sectionname"></span><dl> <dt><strong>ERROR_WRITING_SECTIONNAME</strong></dt> <dt>682</dt> </dl></td>
<td>Erro ao gravar o nome da seção.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_DEVICETYPE"></span><span id="error_writing_devicetype"></span><dl> <dt><strong>ERROR_WRITING_DEVICETYPE</strong></dt> <dt>683</dt> </dl></td>
<td>Erro ao gravar o tipo de dispositivo.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEVICENAME"></span><span id="error_writing_devicename"></span><dl> <dt><strong>ERROR_WRITING_DEVICENAME</strong></dt> <dt>684</dt> </dl></td>
<td>Erro ao gravar o nome do dispositivo.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_MAXCONNECTBPS"></span><span id="error_writing_maxconnectbps"></span><dl> <dt><strong>ERROR_WRITING_MAXCONNECTBPS</strong></dt> <dt>685</dt> </dl></td>
<td>Erro ao gravar a velocidade de conexão máxima.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_MAXCARRIERBPS"></span><span id="error_writing_maxcarrierbps"></span><dl> <dt><strong>ERROR_WRITING_MAXCARRIERBPS</strong></dt> <dt>686</dt> </dl></td>
<td>Erro ao gravar a velocidade máxima da operadora.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRITING_USAGE"></span><span id="error_writing_usage"></span><dl> <dt><strong>ERROR_WRITING_USAGE</strong></dt> <dt>687</dt> </dl></td>
<td>Ocorreu um erro ao gravar o uso.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_DEFAULTOFF"></span><span id="error_writing_defaultoff"></span><dl> <dt><strong>ERROR_WRITING_DEFAULTOFF</strong></dt> <dt>688</dt> </dl></td>
<td>Ocorreu um erro ao escrever o padrão off.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_READING_DEFAULTOFF"></span><span id="error_reading_defaultoff"></span><dl> <dt><strong>ERROR_READING_DEFAULTOFF</strong></dt> <dt>689</dt> </dl></td>

</tr>
<tr class="odd">
<td><span id="ERROR_EMPTY_INI_FILE"></span><span id="error_empty_ini_file"></span><dl> <dt><strong>ERROR_EMPTY_INI_FILE</strong></dt> <dt>690</dt> </dl></td>
<td>O arquivo .INI mídia está vazio.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTHENTICATION_FAILURE"></span><span id="error_authentication_failure"></span><dl> <dt><strong>ERROR_AUTHENTICATION_FAILURE</strong></dt> <dt>691</dt> </dl></td>
<td>Acesso negado porque o nome de usuário, a senha ou ambos não são válidos no domínio.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PORT_OR_DEVICE"></span><span id="error_port_or_device"></span><dl> <dt><strong>ERROR_PORT_OR_DEVICE</strong></dt> <dt>692</dt> </dl></td>
<td>Ocorreu uma falha de hardware na porta ou no dispositivo anexado<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_BINARY_MACRO"></span><span id="error_not_binary_macro"></span><dl> <dt><strong>ERROR_NOT_BINARY_MACRO</strong></dt> <dt>693</dt> </dl></td>
<td>A macro não é uma macro binária.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DCB_NOT_FOUND"></span><span id="error_dcb_not_found"></span><dl> <dt><strong>ERROR_DCB_NOT_FOUND</strong></dt> <dt>694</dt> </dl></td>
<td>DCB não encontrado.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_STATE_MACHINES_NOT_STARTED"></span><span id="error_state_machines_not_started"></span><dl> <dt><strong>ERROR_STATE_MACHINES_NOT_STARTED</strong></dt> <dt>695</dt> </dl></td>
<td>As máquinas de estado não são iniciadas.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_STATE_MACHINES_ALREADY_STARTED"></span><span id="error_state_machines_already_started"></span><dl> <dt><strong>ERROR_STATE_MACHINES_ALREADY_STARTED</strong></dt> <dt>696</dt> </dl></td>
<td>As máquinas de estado já foram iniciadas.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PARTIAL_RESPONSE_LOOPING"></span><span id="error_partial_response_looping"></span><dl> <dt><strong>ERROR_PARTIAL_RESPONSE_LOOPING</strong></dt> <dt>697</dt> </dl></td>
<td>Loop de resposta parcial.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_RESPONSE_KEY"></span><span id="error_unknown_response_key"></span><dl> <dt><strong>ERROR_UNKNOWN_RESPONSE_KEY</strong></dt> <dt>698</dt> </dl></td>
<td>Um nome de chave de resposta no dispositivo . O arquivo INF não está no formato esperado.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RECV_BUF_FULL"></span><span id="error_recv_buf_full"></span><dl> <dt><strong>ERROR_RECV_BUF_FULL</strong></dt> <dt>699</dt> </dl></td>
<td>A resposta do dispositivo causou um estouro de buffer.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CMD_TOO_LONG"></span><span id="error_cmd_too_long"></span><dl> <dt><strong>ERROR_CMD_TOO_LONG</strong></dt> <dt>700</dt> </dl></td>
<td>O comando expandido no dispositivo . O arquivo INF é muito longo.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UNSUPPORTED_BPS"></span><span id="error_unsupported_bps"></span><dl> <dt><strong>ERROR_UNSUPPORTED_BPS</strong></dt> <dt>701</dt> </dl></td>
<td>O dispositivo foi movido para uma velocidade de conexão que não é suportada pelo driver COM.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNEXPECTED_RESPONSE"></span><span id="error_unexpected_response"></span><dl> <dt><strong>ERROR_UNEXPECTED_RESPONSE</strong></dt> <dt>702</dt> </dl></td>
<td>Resposta do dispositivo recebida quando nenhuma esperada.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERACTIVE_MODE"></span><span id="error_interactive_mode"></span><dl> <dt><strong>ERROR_INTERACTIVE_MODE</strong></dt> <dt>703</dt> </dl></td>
<td>Ocorreu um erro porque o modo interativo está habilitado.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAD_CALLBACK_NUMBER"></span><span id="error_bad_callback_number"></span><dl> <dt><strong>ERROR_BAD_CALLBACK_NUMBER</strong></dt> <dt>704</dt> </dl></td>
<td>Um número de retorno de chamada ruim foi especificado.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_AUTH_STATE"></span><span id="error_invalid_auth_state"></span><dl> <dt><strong>ERROR_INVALID_AUTH_STATE</strong></dt> <dt>705</dt> </dl></td>
<td>O estado de autenticação especificado não é válido.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRITING_INITBPS"></span><span id="error_writing_initbps"></span><dl> <dt><strong>ERROR_WRITING_INITBPS</strong></dt> <dt>706</dt> </dl></td>
<td>Ocorreu um erro ao escrever a velocidade de conexão inicial.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_X25_DIAGNOSTIC"></span><span id="error_x25_diagnostic"></span><dl> <dt><strong>ERROR_X25_DIAGNOSTIC</strong></dt> <dt>707</dt> </dl></td>
<td>Uma indicação de diagnóstico X.25 foi recebida.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ACCT_EXPIRED"></span><span id="error_acct_expired"></span><dl> <dt><strong>ERROR_ACCT_EXPIRED</strong></dt> <dt>708</dt> </dl></td>
<td>A conta especificada expirou.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CHANGING_PASSWORD"></span><span id="error_changing_password"></span><dl> <dt><strong>ERROR_CHANGING_PASSWORD</strong></dt> <dt>709</dt> </dl></td>
<td>Ocorreu um erro ao tentar alterar a senha no domínio.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OVERRUN"></span><span id="error_overrun"></span><dl> <dt><strong>ERROR_OVERRUN</strong></dt> <dt>710</dt> </dl></td>
<td>Erros de estouros seriais foram detectados durante a comunicação com o modem.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASMAN_CANNOT_INITIALIZE"></span><span id="error_rasman_cannot_initialize"></span><dl> <dt><strong>ERROR_RASMAN_CANNOT_INITIALIZE</strong></dt> <dt>711</dt> </dl></td>
<td>Falha na inicialização do RasMan. Verifique o log de eventos.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BIPLEX_PORT_NOT_AVAILABLE"></span><span id="error_biplex_port_not_available"></span><dl> <dt><strong>ERROR_BIPLEX_PORT_NOT_AVAILABLE</strong></dt> <dt>712</dt> </dl></td>
<td>A porta de duas vias está sendo inicializada. Aguarde alguns segundos e redial.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_ACTIVE_ISDN_LINES"></span><span id="error_no_active_isdn_lines"></span><dl> <dt><strong>ERROR_NO_ACTIVE_ISDN_LINES</strong></dt> <dt>713</dt> </dl></td>
<td>Nenhuma linha ISDN ativa está disponível.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_ISDN_CHANNELS_AVAILABLE"></span><span id="error_no_isdn_channels_available"></span><dl> <dt><strong>ERROR_NO_ISDN_CHANNELS_AVAILABLE</strong></dt> <dt>714</dt> </dl></td>
<td>Nenhum canal ISDN está disponível para fazer a chamada.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_TOO_MANY_LINE_ERRORS"></span><span id="error_too_many_line_errors"></span><dl> <dt><strong>ERROR_TOO_MANY_LINE_ERRORS</strong></dt> <dt>715</dt> </dl></td>
<td>Ocorreu muitos erros devido à baixa qualidade da linha de telefone.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IP_CONFIGURATION"></span><span id="error_ip_configuration"></span><dl> <dt><strong>ERROR_IP_CONFIGURATION</strong></dt> <dt>716</dt> </dl></td>
<td>A configuração de IP de acesso remoto é inutilizável.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_IP_ADDRESSES"></span><span id="error_no_ip_addresses"></span><dl> <dt><strong>ERROR_NO_IP_ADDRESSES</strong></dt> <dt>717</dt> </dl></td>
<td>Nenhum endereço IP está disponível no pool estático de endereços IP de acesso remoto.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_TIMEOUT"></span><span id="error_ppp_timeout"></span><dl> <dt><strong>ERROR_PPP_TIMEOUT</strong></dt> <dt>718</dt> </dl></td>
<td>Ocorreu um tempo de tempo de PPP.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REMOTE_TERMINATED"></span><span id="error_ppp_remote_terminated"></span><dl> <dt><strong>ERROR_PPP_REMOTE_TERMINATED</strong></dt> <dt>719</dt> </dl></td>
<td>A conexão foi encerrada pelo computador remoto.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_PROTOCOLS_CONFIGURED"></span><span id="error_ppp_no_protocols_configured"></span><dl> <dt><strong>ERROR_PPP_NO_PROTOCOLS_CONFIGURED</strong></dt> <dt>720</dt> </dl></td>
<td>Nenhum protocolo de controle PPP está configurado.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_NO_RESPONSE"></span><span id="error_ppp_no_response"></span><dl> <dt><strong>ERROR_PPP_NO_RESPONSE</strong></dt> <dt>721</dt> </dl></td>
<td>O par PPP remoto não está respondendo.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_INVALID_PACKET"></span><span id="error_ppp_invalid_packet"></span><dl> <dt><strong>ERROR_PPP_INVALID_PACKET</strong></dt> <dt>722</dt> </dl></td>
<td>O pacote PPP não é válido.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PHONE_NUMBER_TOO_LONG"></span><span id="error_phone_number_too_long"></span><dl> <dt><strong>ERROR_PHONE_NUMBER_TOO_LONG</strong></dt> <dt>723</dt> </dl></td>
<td>O número de telefone, incluindo o prefixo e o sufixo, é muito longo.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NO_DIALOUT_CONFIGURED"></span><span id="error_ipxcp_no_dialout_configured"></span><dl> <dt><strong>ERROR_IPXCP_NO_DIALOUT_CONFIGURED</strong></dt> <dt>724</dt> </dl></td>
<td>O protocolo IPX não pode discar no modem (ou em outro dispositivo de conexão) porque esse computador não está configurado para discar (é um roteador IPX).<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPXCP_NO_DIALIN_CONFIGURED"></span><span id="error_ipxcp_no_dialin_configured"></span><dl> <dt><strong>ERROR_IPXCP_NO_DIALIN_CONFIGURED</strong></dt> <dt>725</dt> </dl></td>
<td>O protocolo IPX não pode discar no modem (ou em outro dispositivo de conexão) porque esse computador não está configurado para discagem no (o roteador IPX não está instalado).<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE"></span><span id="error_ipxcp_dialout_already_active"></span><dl> <dt><strong>ERROR_IPXCP_DIALOUT_ALREADY_ACTIVE</strong></dt> <dt>726</dt> </dl></td>
<td>O protocolo IPX não pode ser usado para discagem em mais de uma porta por vez.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ACCESSING_TCPCFGDLL"></span><span id="error_accessing_tcpcfgdll"></span><dl> <dt><strong>ERROR_ACCESSING_TCPCFGDLL</strong></dt> <dt>727</dt> </dl></td>
<td>Não é possível acessar TCPCFG.DLL.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_IP_RAS_ADAPTER"></span><span id="error_no_ip_ras_adapter"></span><dl> <dt><strong>ERROR_NO_IP_RAS_ADAPTER</strong></dt> <dt>728</dt> </dl></td>
<td>Não é possível encontrar um adaptador IP vinculado ao acesso remoto.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SLIP_REQUIRES_IP"></span><span id="error_slip_requires_ip"></span><dl> <dt><strong>ERROR_SLIP_REQUIRES_IP</strong></dt> <dt>729</dt> </dl></td>
<td>O SLIP não pode ser usado, a menos que o protocolo IP esteja instalado.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PROJECTION_NOT_COMPLETE"></span><span id="error_projection_not_complete"></span><dl> <dt><strong>ERROR_PROJECTION_NOT_COMPLETE</strong></dt> <dt>730</dt> </dl></td>
<td>O registro do computador não foi concluído.<br/>
<blockquote>
[!Note]<br />
Preterido no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_NOT_CONFIGURED"></span><span id="error_protocol_not_configured"></span><dl> <dt><strong>ERROR_PROTOCOL_NOT_CONFIGURED</strong></dt> <dt>731</dt> </dl></td>
<td>O protocolo especificado não está configurado.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NOT_CONVERGING"></span><span id="error_ppp_not_converging"></span><dl> <dt><strong>ERROR_PPP_NOT_CONVERGING</strong></dt> <dt>732</dt> </dl></td>
<td>A negociação PPP não está convergindo.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_CP_REJECTED"></span><span id="error_ppp_cp_rejected"></span><dl> <dt><strong>ERROR_PPP_CP_REJECTED</strong></dt> <dt>733</dt> </dl></td>
<td>o protocolo de controle PPP para o protocolo de rede especificado não está disponível no servidor.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_LCP_TERMINATED"></span><span id="error_ppp_lcp_terminated"></span><dl> <dt><strong>ERROR_PPP_LCP_TERMINATED</strong></dt> <dt>734</dt> </dl></td>
<td>O protocolo de controle de link PPP foi encerrado.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_REQUIRED_ADDRESS_REJECTED"></span><span id="error_ppp_required_address_rejected"></span><dl> <dt><strong>ERROR_PPP_REQUIRED_ADDRESS_REJECTED</strong></dt> <dt>735</dt> </dl></td>
<td>O endereço solicitado foi rejeitado pelo servidor.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NCP_TERMINATED"></span><span id="error_ppp_ncp_terminated"></span><dl> <dt><strong>ERROR_PPP_NCP_TERMINATED</strong></dt> <dt>736</dt> </dl></td>
<td>O computador remoto terminou o protocolo de controle.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PPP_LOOPBACK_DETECTED"></span><span id="error_ppp_loopback_detected"></span><dl> <dt><strong>ERROR_PPP_LOOPBACK_DETECTED</strong></dt> <dt>737</dt> </dl></td>
<td>Loopback detectado.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_NO_ADDRESS_ASSIGNED"></span><span id="error_ppp_no_address_assigned"></span><dl> <dt><strong>ERROR_PPP_NO_ADDRESS_ASSIGNED</strong></dt> <dt>738</dt> </dl></td>
<td>O servidor não atribuiu um endereço.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_USE_LOGON_CREDENTIALS"></span><span id="error_cannot_use_logon_credentials"></span><dl> <dt><strong>ERROR_CANNOT_USE_LOGON_CREDENTIALS</strong></dt> <dt>739</dt> </dl></td>
<td>o servidor remoto não pode usar a Windows NT senha criptografada.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TAPI_CONFIGURATION"></span><span id="error_tapi_configuration"></span><dl> <dt><strong>ERROR_TAPI_CONFIGURATION</strong></dt> <dt>740</dt> </dl></td>
<td>Os dispositivos TAPI configurados para acesso remoto falharam ao inicializar ou não foram instalados corretamente.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_LOCAL_ENCRYPTION"></span><span id="error_no_local_encryption"></span><dl> <dt><strong>ERROR_NO_LOCAL_ENCRYPTION</strong></dt> <dt>741</dt> </dl></td>
<td>O computador local não dá suporte à criptografia.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_REMOTE_ENCRYPTION"></span><span id="error_no_remote_encryption"></span><dl> <dt><strong>ERROR_NO_REMOTE_ENCRYPTION</strong></dt> <dt>742</dt> </dl></td>
<td>O servidor remoto não dá suporte à criptografia.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_REQUIRES_ENCRYPTION"></span><span id="error_remote_requires_encryption"></span><dl> <dt><strong>ERROR_REMOTE_REQUIRES_ENCRYPTION</strong></dt> <dt>743</dt> </dl></td>
<td>O computador remoto requer criptografia de dados.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IPXCP_NET_NUMBER_CONFLICT"></span><span id="error_ipxcp_net_number_conflict"></span><dl> <dt><strong>ERROR_IPXCP_NET_NUMBER_CONFLICT</strong></dt> <dt>744</dt> </dl></td>
<td>O sistema não pode usar o número de rede IPX atribuído pelo computador remoto. Informações adicionais são fornecidas no log de eventos.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SMM"></span><span id="error_invalid_smm"></span><dl> <dt><strong>ERROR_INVALID_SMM</strong></dt> <dt>745</dt> </dl></td>
<td>O módulo de gerenciamento de sessão (SMM) não é válido.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_UNINITIALIZED"></span><span id="error_smm_uninitialized"></span><dl> <dt><strong>ERROR_SMM_UNINITIALIZED</strong></dt> <dt>746</dt> </dl></td>
<td>O SMM não foi inicializado.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_MAC_FOR_PORT"></span><span id="error_no_mac_for_port"></span><dl> <dt><strong>ERROR_NO_MAC_FOR_PORT</strong></dt> <dt>747</dt> </dl></td>
<td>Sem MAC para a porta.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SMM_TIMEOUT"></span><span id="error_smm_timeout"></span><dl> <dt><strong>ERROR_SMM_TIMEOUT</strong></dt> <dt>748</dt> </dl></td>
<td>O SMM atingiu o tempo limite.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_PHONE_NUMBER"></span><span id="error_bad_phone_number"></span><dl> <dt><strong>ERROR_BAD_PHONE_NUMBER</strong></dt> <dt>749</dt> </dl></td>
<td>Foi especificado um número de telefone insatisfatório.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_WRONG_MODULE"></span><span id="error_wrong_module"></span><dl> <dt><strong>ERROR_WRONG_MODULE</strong></dt> <dt>750</dt> </dl></td>
<td>O SMM errado foi especificado.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_CALLBACK_NUMBER"></span><span id="error_invalid_callback_number"></span><dl> <dt><strong>ERROR_INVALID_CALLBACK_NUMBER</strong></dt> <dt>751</dt> </dl></td>
<td>O número de retorno de chamada contém um caractere que não é válido. Somente os 18 caracteres a seguir são permitidos: 0 a 9, T, P, W, (,),-, @ e espaço.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SCRIPT_SYNTAX"></span><span id="error_script_syntax"></span><dl> <dt><strong>ERROR_SCRIPT_SYNTAX</strong></dt> <dt>752</dt> </dl></td>
<td>Foi encontrado um erro de sintaxe durante o processamento de um script.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_HANGUP_FAILED"></span><span id="error_hangup_failed"></span><dl> <dt><strong>ERROR_HANGUP_FAILED</strong></dt> <dt>753</dt> </dl></td>
<td>Não foi possível desconectar a conexão porque ela foi criada pelo roteador de vários protocolos.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BUNDLE_NOT_FOUND"></span><span id="error_bundle_not_found"></span><dl> <dt><strong>ERROR_BUNDLE_NOT_FOUND</strong></dt> <dt>754</dt> </dl></td>
<td>O sistema não pôde localizar o pacote de vários vínculos.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DO_CUSTOMDIAL"></span><span id="error_cannot_do_customdial"></span><dl> <dt><strong>ERROR_CANNOT_DO_CUSTOMDIAL</strong></dt> <dt>755</dt> </dl></td>
<td>O sistema não pode executar a discagem automática porque essa conexão tem um discador personalizado especificado.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIAL_ALREADY_IN_PROGRESS"></span><span id="error_dial_already_in_progress"></span><dl> <dt><strong>ERROR_DIAL_ALREADY_IN_PROGRESS</strong></dt> <dt>756</dt> </dl></td>
<td>Esta conexão já está sendo discada.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASAUTO_CANNOT_INITIALIZE"></span><span id="error_rasauto_cannot_initialize"></span><dl> <dt><strong>ERROR_RASAUTO_CANNOT_INITIALIZE</strong></dt> <dt>757</dt> </dl></td>
<td>Não foi possível iniciar o RAS automaticamente. Informações adicionais são fornecidas no log de eventos.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_ALREADY_SHARED"></span><span id="error_connection_already_shared"></span><dl> <dt><strong>ERROR_CONNECTION_ALREADY_SHARED</strong></dt> <dt>758</dt> </dl></td>
<td>O ICS (compartilhamento de conexão com a Internet) já está habilitado na conexão.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_CHANGE_FAILED"></span><span id="error_sharing_change_failed"></span><dl> <dt><strong>ERROR_SHARING_CHANGE_FAILED</strong></dt> <dt>759</dt> </dl></td>
<td>Ocorreu um erro enquanto as configurações de compartilhamento de conexão com a Internet existentes estavam sendo alteradas.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_ROUTER_INSTALL"></span><span id="error_sharing_router_install"></span><dl> <dt><strong>ERROR_SHARING_ROUTER_INSTALL</strong></dt> <dt>760</dt> </dl></td>
<td>Ocorreu um erro enquanto os recursos de roteamento estavam sendo habilitados.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARE_CONNECTION_FAILED"></span><span id="error_share_connection_failed"></span><dl> <dt><strong>ERROR_SHARE_CONNECTION_FAILED</strong></dt> <dt>761</dt> </dl></td>
<td>Ocorreu um erro enquanto o compartilhamento de conexão com a Internet estava sendo habilitado para a conexão.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="7ERROR_SHARING_PRIVATE_INSTALL64"></span><span id="7error_sharing_private_install64"></span><dl> <dt><strong>7ERROR_SHARING_PRIVATE_INSTALL64</strong></dt> <dt>762</dt> </dl></td>
<td>Ocorreu um erro enquanto a rede local estava sendo configurada para compartilhamento.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_SHARE_CONNECTION"></span><span id="error_cannot_share_connection"></span><dl> <dt><strong>ERROR_CANNOT_SHARE_CONNECTION</strong></dt> <dt>763</dt> </dl></td>
<td>O compartilhamento de conexão com a Internet não pode ser habilitado. Há mais de uma conexão de LAN diferente da conexão a ser compartilhada.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SMART_CARD_READER"></span><span id="error_no_smart_card_reader"></span><dl> <dt><strong>ERROR_NO_SMART_CARD_READER</strong></dt> <dt>764</dt> </dl></td>
<td>Nenhum leitor de cartão inteligente está instalado.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_ADDRESS_EXISTS"></span><span id="error_sharing_address_exists"></span><dl> <dt><strong>ERROR_SHARING_ADDRESS_EXISTS</strong></dt> <dt>765</dt> </dl></td>
<td>O compartilhamento de conexão com a Internet não pode ser habilitado. Uma conexão de LAN já está configurada com o endereço IP necessário para o endereçamento IP automático. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_CERTIFICATE"></span><span id="error_no_certificate"></span><dl> <dt><strong>ERROR_NO_CERTIFICATE</strong></dt> <dt>766</dt> </dl></td>
<td>Não foi possível encontrar um certificado. As conexões que usam o protocolo L2TP sobre IPSec exigem a instalação de um certificado de máquina, também conhecido como certificado de computador. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_MULTIPLE_ADDRESSES"></span><span id="error_sharing_multiple_addresses"></span><dl> <dt><strong>ERROR_SHARING_MULTIPLE_ADDRESSES</strong></dt> <dt>767</dt> </dl></td>
<td>O compartilhamento de conexão com a Internet não pode ser habilitado. A conexão LAN selecionada como a rede privada tem mais de um endereço IP configurado. Reconfigure a conexão LAN com um único endereço IP antes de habilitar o compartilhamento de conexão com a Internet. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FAILED_TO_ENCRYPT"></span><span id="error_failed_to_encrypt"></span><dl> <dt><strong>ERROR_FAILED_TO_ENCRYPT</strong></dt> <dt>768</dt> </dl></td>
<td>Falha na tentativa de conexão devido à falha na criptografia de dados. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAD_ADDRESS_SPECIFIED"></span><span id="error_bad_address_specified"></span><dl> <dt><strong>ERROR_BAD_ADDRESS_SPECIFIED</strong></dt> <dt>769</dt> </dl></td>
<td>O destino especificado não está acessível. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CONNECTION_REJECT"></span><span id="error_connection_reject"></span><dl> <dt><strong>ERROR_CONNECTION_REJECT</strong></dt> <dt>770</dt> </dl></td>
<td>O computador remoto rejeitou a tentativa de conexão. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONGESTION"></span><span id="error_congestion"></span><dl> <dt><strong>ERROR_CONGESTION</strong></dt> <dt>771</dt> </dl></td>
<td>Falha na tentativa de conexão porque a rede está ocupada. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INCOMPATIBLE"></span><span id="error_incompatible"></span><dl> <dt><strong>ERROR_INCOMPATIBLE</strong></dt> <dt>772</dt> </dl></td>
<td>O hardware de rede do computador remoto é incompatível com o tipo de chamada solicitada. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NUMBERCHANGED"></span><span id="error_numberchanged"></span><dl> <dt><strong>ERROR_NUMBERCHANGED</strong></dt> <dt>773</dt> </dl></td>
<td>Falha na tentativa de conexão porque o número de destino foi alterado. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TEMPFAILURE"></span><span id="error_tempfailure"></span><dl> <dt><strong>ERROR_TEMPFAILURE</strong></dt> <dt>774</dt> </dl></td>
<td>Falha na tentativa de conexão devido a uma falha temporária. Tente se conectar novamente.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BLOCKED"></span><span id="error_blocked"></span><dl> <dt><strong>ERROR_BLOCKED</strong></dt> <dt>775</dt> </dl></td>
<td>A chamada foi bloqueada pelo computador remoto. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DONOTDISTURB"></span><span id="error_donotdisturb"></span><dl> <dt><strong>ERROR_DONOTDISTURB</strong></dt> <dt>776</dt> </dl></td>
<td>Não foi possível conectar a chamada porque o computador remoto invocou o recurso não incomodar. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OUTOFORDER"></span><span id="error_outoforder"></span><dl> <dt><strong>ERROR_OUTOFORDER</strong></dt> <dt>777</dt> </dl></td>
<td>Falha na tentativa de conexão porque o modem ou outro dispositivo de conexão no computador remoto está fora de ordem. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNABLE_TO_AUTHENTICATE_SERVER"></span><span id="error_unable_to_authenticate_server"></span><dl> <dt><strong>ERROR_UNABLE_TO_AUTHENTICATE_SERVER</strong></dt> <dt>778</dt> </dl></td>
<td>Não foi possível verificar a identidade do servidor. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SMART_CARD_REQUIRED"></span><span id="error_smart_card_required"></span><dl> <dt><strong>ERROR_SMART_CARD_REQUIRED</strong></dt> <dt>779</dt> </dl></td>
<td>Para discar usando essa conexão, você deve usar um cartão inteligente.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_FUNCTION_FOR_ENTRY"></span><span id="error_invalid_function_for_entry"></span><dl> <dt><strong>ERROR_INVALID_FUNCTION_FOR_ENTRY</strong></dt> <dt>780</dt> </dl></td>
<td>Uma função tentada não é válida para esta conexão. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND"></span><span id="error_cert_for_encryption_not_found"></span><dl> <dt><strong>ERROR_CERT_FOR_ENCRYPTION_NOT_FOUND</strong></dt> <dt>781</dt> </dl></td>
<td>Falha na tentativa de criptografia porque nenhum certificado válido foi encontrado.<br/>
<blockquote>
[!Note]<br />
preterido no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SHARING_RRAS_CONFLICT"></span><span id="error_sharing_rras_conflict"></span><dl> <dt><strong>ERROR_SHARING_RRAS_CONFLICT</strong></dt> <dt>782</dt> </dl></td>
<td>O compartilhamento de conexão (NAT) está instalado atualmente como um protocolo de roteamento e deve ser removido antes de habilitar o compartilhamento de conexão com a Internet.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_NO_PRIVATE_LAN"></span><span id="error_sharing_no_private_lan"></span><dl> <dt><strong>ERROR_SHARING_NO_PRIVATE_LAN</strong></dt> <dt>783</dt> </dl></td>
<td>O compartilhamento de conexão com a Internet não pode ser habilitado. A conexão LAN selecionada como a rede privada não está presente ou está desconectada da rede. Verifique se o adaptador de LAN está conectado antes de habilitar o compartilhamento de conexão com a Internet. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_DIFF_USER_AT_LOGON"></span><span id="error_no_diff_user_at_logon"></span><dl> <dt><strong>ERROR_NO_DIFF_USER_AT_LOGON</strong></dt> <dt>784</dt> </dl></td>
<td>Não é possível discar usando essa conexão no momento do logon porque ela está configurada para usar um nome de usuário diferente daquele no cartão inteligente. Se você quiser usar essa conexão no momento do logon, deverá configurá-la para usar o nome de usuário no cartão inteligente. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_REG_CERT_AT_LOGON"></span><span id="error_no_reg_cert_at_logon"></span><dl> <dt><strong>ERROR_NO_REG_CERT_AT_LOGON</strong></dt> <dt>785</dt> </dl></td>
<td>Não é possível discar usando essa conexão no momento do logon porque ela não está configurada para usar um cartão inteligente. Se você quiser usá-lo no momento do logon, deverá editar as propriedades dessa conexão para que ele use um cartão inteligente. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_CERT"></span><span id="error_oakley_no_cert"></span><dl> <dt><strong>ERROR_OAKLEY_NO_CERT</strong></dt> <dt>786</dt> </dl></td>
<td>A tentativa de conexão L2TP falhou porque não há um certificado de máquina válido no computador para autenticação de segurança. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_AUTH_FAIL"></span><span id="error_oakley_auth_fail"></span><dl> <dt><strong>ERROR_OAKLEY_AUTH_FAIL</strong></dt> <dt>787</dt> </dl></td>
<td>A tentativa de conexão L2TP falhou porque a camada de segurança não pôde autenticar o computador remoto. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_ATTRIB_FAIL"></span><span id="error_oakley_attrib_fail"></span><dl> <dt><strong>ERROR_OAKLEY_ATTRIB_FAIL</strong></dt> <dt>788</dt> </dl></td>
<td>A tentativa de conexão L2TP falhou porque a camada de segurança não pôde negociar parâmetros compatíveis com o computador remoto. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_GENERAL_PROCESSING"></span><span id="error_oakley_general_processing"></span><dl> <dt><strong>ERROR_OAKLEY_GENERAL_PROCESSING</strong></dt> <dt>789</dt> </dl></td>
<td>A tentativa de conexão L2TP falhou porque a camada de segurança encontrou um erro de processamento durante as negociações iniciais com o computador remoto. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_NO_PEER_CERT"></span><span id="error_oakley_no_peer_cert"></span><dl> <dt><strong>ERROR_OAKLEY_NO_PEER_CERT</strong></dt> <dt>790</dt> </dl></td>
<td>Falha na tentativa de conexão L2TP porque a validação de certificado no computador remoto falhou. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_NO_POLICY"></span><span id="error_oakley_no_policy"></span><dl> <dt><strong>ERROR_OAKLEY_NO_POLICY</strong></dt> <dt>791</dt> </dl></td>
<td>Falha na tentativa de conexão L2TP porque a política de segurança para a conexão não foi encontrada. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_OAKLEY_TIMED_OUT"></span><span id="error_oakley_timed_out"></span><dl> <dt><strong>ERROR_OAKLEY_TIMED_OUT</strong></dt> <dt>792</dt> </dl></td>
<td>Falha na tentativa de conexão L2TP porque a negociação de segurança atingiu o tempo limite. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_OAKLEY_ERROR"></span><span id="error_oakley_error"></span><dl> <dt><strong>ERROR_OAKLEY_ERROR</strong></dt> <dt>793</dt> </dl></td>
<td>A tentativa de conexão L2TP falhou porque ocorreu um erro ao negociar a segurança. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_FRAMED_PROTOCOL"></span><span id="error_unknown_framed_protocol"></span><dl> <dt><strong>ERROR_UNKNOWN_FRAMED_PROTOCOL</strong></dt> <dt>794</dt> </dl></td>
<td>O atributo de raio do protocolo Framed para este usuário não é PPP. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_WRONG_TUNNEL_TYPE"></span><span id="error_wrong_tunnel_type"></span><dl> <dt><strong>ERROR_WRONG_TUNNEL_TYPE</strong></dt> <dt>795</dt> </dl></td>
<td>o atributo RADIUS do tipo Tunnel para este usuário não está correto. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_SERVICE_TYPE"></span><span id="error_unknown_service_type"></span><dl> <dt><strong>ERROR_UNKNOWN_SERVICE_TYPE</strong></dt> <dt>796</dt> </dl></td>
<td>O atributo RADIUS do tipo de serviço para este usuário não é Framed nem retorno de chamada Framed. <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CONNECTING_DEVICE_NOT_FOUND"></span><span id="error_connecting_device_not_found"></span><dl> <dt><strong>ERROR_CONNECTING_DEVICE_NOT_FOUND</strong></dt> <dt>797</dt> </dl></td>
<td>Não foi possível estabelecer uma conexão com o computador remoto porque o modem não foi encontrado ou estava ocupado. <br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_EAPTLS_CERTIFICATE"></span><span id="error_no_eaptls_certificate"></span><dl> <dt><strong>ERROR_NO_EAPTLS_CERTIFICATE</strong></dt> <dt>798</dt> </dl></td>
<td>Não foi possível encontrar um certificado que possa ser usado com o EAP (Extensible Authentication Protocol). <br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SHARING_HOST_ADDRESS_CONFLICT"></span><span id="error_sharing_host_address_conflict"></span><dl> <dt><strong>ERROR_SHARING_HOST_ADDRESS_CONFLICT</strong></dt> <dt>799</dt> </dl></td>
<td>O ICS (compartilhamento de conexão com a Internet) não pode ser habilitado devido a um conflito de endereço IP na rede. O ICS requer que o host seja configurado para usar <strong>192.168.0.1</strong>. Certifique-se de que nenhum outro cliente na rede esteja configurado para usar <strong>192.168.0.1</strong>.<br/>
<blockquote>
[!Note]<br />
com suporte no Windows XP e em versões posteriores do Windows.
</blockquote>
<br/>
<blockquote>
[!Note]<br />
Windows 7 e posterior: o host deve ser configurado para usar <strong>192.168.137.1</strong>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTOMATIC_VPN_FAILED"></span><span id="error_automatic_vpn_failed"></span><dl> <dt><strong>ERROR_AUTOMATIC_VPN_FAILED</strong></dt> <dt>800</dt> </dl></td>
<td>Não é possível estabelecer a conexão VPN. O servidor VPN pode estar inacessível ou os parâmetros de segurança podem não estar configurados corretamente para essa conexão. <br/>
<blockquote>
[!Note]<br />
com suporte no Windows XP e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VALIDATING_SERVER_CERT"></span><span id="error_validating_server_cert"></span><dl> <dt><strong>ERROR_VALIDATING_SERVER_CERT</strong></dt> <dt>801</dt> </dl></td>
<td>essa conexão é configurada para validar a identidade do servidor de acesso, mas Windows não pode verificar o certificado digital enviado pelo servidor.<br/>
<blockquote>
[!Note]<br />
com suporte no Windows XP e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_READING_SCARD"></span><span id="error_reading_scard"></span><dl> <dt><strong>ERROR_READING_SCARD</strong></dt> <dt>802</dt> </dl></td>
<td>O cartão fornecido não foi reconhecido. Verifique se o cartão foi inserido corretamente e se adapta com segurança.<br/>
<blockquote>
[!Note]<br />
com suporte no Windows XP com SP1 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_CONFIG"></span><span id="error_invalid_peap_cookie_config"></span><dl> <dt><strong>ERROR_INVALID_PEAP_COOKIE_CONFIG</strong></dt> <dt>803</dt> </dl></td>
<td>A configuração de PEAP armazenada no cookie de sessão não corresponde à configuração de sessão atual.<br/>
<blockquote>
[!Note]<br />
com suporte no Windows XP com SP1 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PEAP_COOKIE_USER"></span><span id="error_invalid_peap_cookie_user"></span><dl> <dt><strong>ERROR_INVALID_PEAP_COOKIE_USER</strong></dt> <dt>804</dt> </dl></td>
<td>A identidade de PEAP armazenada no cookie de sessão não corresponde à identidade atual.<br/>
<blockquote>
[!Note]<br />
com suporte no Windows XP com SP1 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_MSCHAPV2_CONFIG"></span><span id="error_invalid_mschapv2_config"></span><dl> <dt><strong>ERROR_INVALID_MSCHAPV2_CONFIG</strong></dt> <dt>805</dt> </dl></td>
<td>Não é possível discar usando essa conexão no momento do logon porque ela está configurada para usar as credenciais do usuário conectado no momento.<br/>
<blockquote>
[!Note]<br />
com suporte no Windows XP com SP1 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_GRE_BLOCKED"></span><span id="error_vpn_gre_blocked"></span><dl> <dt><strong>ERROR_VPN_GRE_BLOCKED</strong></dt> <dt>806</dt> </dl></td>
<td>Uma conexão entre o computador e o servidor VPN foi iniciada, mas a conexão VPN não pode ser concluída. A causa mais comum para isso é que pelo menos um dispositivo de Internet (por exemplo, um firewall ou um roteador) entre o computador e o servidor VPN não está configurado para permitir pacotes de protocolo GRE (encapsulamento de roteamento genérico).<br/>
<blockquote>
[!Note]<br />
com suporte no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_DISCONNECT"></span><span id="error_vpn_disconnect"></span><dl> <dt><strong>ERROR_VPN_DISCONNECT</strong></dt> <dt>807</dt> </dl></td>
<td>A conexão de rede entre o computador e o servidor VPN foi interrompida. Isso pode ser causado por um problema na transmissão de VPN e é normalmente o resultado da latência da Internet ou simplesmente que o servidor VPN atingiu a capacidade. Tente se reconectar ao servidor VPN.<br/>
<blockquote>
[!Note]<br />
com suporte no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_REFUSED"></span><span id="error_vpn_refused"></span><dl> <dt><strong>ERROR_VPN_REFUSED</strong></dt> <dt>808</dt> </dl></td>
<td>A conexão de rede entre o computador e o servidor VPN não pôde ser estabelecida porque o servidor remoto recusou a conexão. Isso geralmente é causado por uma incompatibilidade entre a configuração do servidor e suas configurações de conexão.<br/>
<blockquote>
[!Note]<br />
com suporte no Windows Vista e em versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_TIMEOUT"></span><span id="error_vpn_timeout"></span><dl> <dt><strong>ERROR_VPN_TIMEOUT</strong></dt> <dt>809</dt> </dl></td>
<td>Não foi possível estabelecer a conexão de rede entre o computador e o servidor VPN porque o servidor remoto não está respondendo. Isso pode ser porque um dos dispositivos de rede (por exemplo, firewalls, NAT, roteadores) entre o computador e o servidor remoto não está configurado para permitir conexões VPN.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_VPN_BAD_CERT"></span><span id="error_vpn_bad_cert"></span><dl> <dt><strong>ERROR_VPN_BAD_CERT</strong></dt> <dt>810</dt> </dl></td>
<td>Uma conexão de rede entre o computador e o servidor VPN foi iniciada, mas a conexão VPN não foi concluída. Normalmente, isso é causado pelo uso de um certificado incorreto ou expirado para autenticação entre o cliente e o servidor.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_VPN_BAD_PSK"></span><span id="error_vpn_bad_psk"></span><dl> <dt><strong>ERROR_VPN_BAD_PSK</strong></dt> <dt>811</dt> </dl></td>
<td>Não foi possível estabelecer a conexão de rede entre o computador e o servidor VPN porque o servidor remoto não está respondendo. Normalmente, isso é causado por um problema de chave pré-compartilhada entre o cliente e o servidor. Uma chave pré-compartilhada é usada para garantir que você seja quem diz ser em um ciclo de comunicação de IPSec (Ip Security).<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVER_POLICY"></span><span id="error_server_policy"></span><dl> <dt><strong>ERROR_SERVER_POLICY</strong></dt> <dt>812</dt> </dl></td>
<td>a conexão foi impedida devido a uma política configurada no servidor RAS/VPN. Especificamente, o método de autenticação usado pelo servidor para verificar seu nome de usuário e senha pode não corresponder ao método de autenticação configurado em seu perfil de conexão.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_ACTIVE"></span><span id="error_broadband_active"></span><dl> <dt><strong>ERROR_BROADBAND_ACTIVE</strong></dt> <dt>813</dt> </dl></td>
<td>Você tentou estabelecer uma segunda conexão de banda larga enquanto uma conexão de banda larga anterior já está estabelecida usando o mesmo dispositivo ou porta.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BROADBAND_NO_NIC"></span><span id="error_broadband_no_nic"></span><dl> <dt><strong>ERROR_BROADBAND_NO_NIC</strong></dt> <dt>814</dt> </dl></td>
<td>A conectividade Ethernet subjacente necessária para a conexão de banda larga não foi encontrada.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BROADBAND_TIMEOUT"></span><span id="error_broadband_timeout"></span><dl> <dt><strong>ERROR_BROADBAND_TIMEOUT</strong></dt> <dt>815</dt> </dl></td>
<td>Não foi possível estabelecer a conexão de rede de banda larga no computador porque o servidor remoto não está respondendo. Isso pode ser causado por um valor que não é válido para o campo 'Nome do Serviço' para essa conexão.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_FEATURE_DEPRECATED"></span><span id="error_feature_deprecated"></span><dl> <dt><strong>ERROR_FEATURE_DEPRECATED</strong></dt> <dt>816</dt> </dl></td>
<td>Não há mais suporte para um recurso ou configuração que você tentou habilitar pelo serviço de acesso remoto.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CANNOT_DELETE"></span><span id="error_cannot_delete"></span><dl> <dt><strong>ERROR_CANNOT_DELETE</strong></dt> <dt>817</dt> </dl></td>
<td>Não é possível excluir uma conexão enquanto ela está conectada.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_RESOURCE_CREATION_FAILED"></span><span id="error_rasqec_resource_creation_failed"></span><dl> <dt><strong>ERROR_RASQEC_RESOURCE_CREATION_FAILED</strong></dt> <dt>818</dt> </dl></td>
<td>O cliente de imposição da NAP (Proteção de Acesso à Rede) não pôde criar recursos do sistema para conexões de acesso remoto. Alguns serviços de rede ou recursos podem não estar disponíveis.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_ENABLED"></span><span id="error_rasqec_napagent_not_enabled"></span><dl> <dt><strong>ERROR_RASQEC_NAPAGENT_NOT_ENABLED</strong></dt> <dt>819</dt> </dl></td>
<td>O serviço agente NAP (Agente de Proteção de Acesso à Rede) foi desabilitado ou não está instalado neste computador. Alguns serviços de rede ou recursos podem não estar disponíveis.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_NAPAGENT_NOT_CONNECTED"></span><span id="error_rasqec_napagent_not_connected"></span><dl> <dt><strong>ERROR_RASQEC_NAPAGENT_NOT_CONNECTED</strong></dt> <dt>820</dt> </dl></td>
<td>O cliente de imposição nap (proteção de acesso à rede) falhou ao se registrar no serviço agente nap de proteção de acesso à rede. Alguns serviços de rede ou recursos podem não estar disponíveis.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_RASQEC_CONN_DOESNOTEXIST"></span><span id="error_rasqec_conn_doesnotexist"></span><dl> <dt><strong>ERROR_RASQEC_CONN_DOESNOTEXIST</strong></dt> <dt>821</dt> </dl></td>
<td>O cliente de imposição da NAP (Proteção de Acesso à Rede) não pôde processar a solicitação porque a conexão de acesso remoto não existe.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASQEC_TIMEOUT"></span><span id="error_rasqec_timeout"></span><dl> <dt><strong>ERROR_RASQEC_TIMEOUT</strong></dt> <dt>822</dt> </dl></td>
<td>O cliente de imposição da NAP (Proteção de Acesso à Rede) não respondeu. Alguns serviços de rede ou recursos podem não estar disponíveis.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_CRYPTOBINDING_INVALID"></span><span id="error_peap_cryptobinding_invalid"></span><dl> <dt><strong>ERROR_PEAP_CRYPTOBINDING_INVALID</strong></dt> <dt>823</dt> </dl></td>
<td>O Crypto-Binding TLV (type-length-value) recebido não é válido.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED"></span><span id="error_peap_cryptobinding_notreceived"></span><dl> <dt><strong>ERROR_PEAP_CRYPTOBINDING_NOTRECEIVED</strong></dt> <dt>824</dt> </dl></td>
<td>Crypto-Binding TLV não foi recebido.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_VPNSTRATEGY"></span><span id="error_invalid_vpnstrategy"></span><dl> <dt><strong>ERROR_INVALID_VPNSTRATEGY</strong></dt> <dt>825</dt> </dl></td>
<td>O PPTP (Protocolo de Túnel Ponto a Ponto) é incompatível com o IPv6. Altere o tipo de rede virtual privada para Protocolo de Túnel de Camada Dois (L2TP).<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_cache_credentials_invalid"></span><dl> <dt><strong>ERROR_EAPTLS_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>826</dt> </dl></td>
<td>Falha na validação de EAPTLS das credenciais armazenadas em cache. Descartar credenciais armazenadas em cache.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_IPSEC_SERVICE_STOPPED"></span><span id="error_ipsec_service_stopped"></span><dl> <dt><strong>ERROR_IPSEC_SERVICE_STOPPED</strong></dt> <dt>827</dt> </dl></td>
<td>A conexão L2TP/IPsec não pode ser concluída porque o serviço Módulos de Chave IKE e IPSec do AuthIP e/ou o serviço Mecanismo de Filtragem Base não está em execução. Esses serviços são necessários para estabelecer uma conexão L2TP/IPSec.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_TIMEOUT"></span><span id="error_idle_timeout"></span><dl> <dt><strong>ERROR_IDLE_TIMEOUT</strong></dt> <dt>828</dt> </dl></td>
<td>A conexão foi encerrada devido ao tempo de ociosidade.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_LINK_FAILURE"></span><span id="error_link_failure"></span><dl> <dt><strong>ERROR_LINK_FAILURE</strong></dt> <dt>829</dt> </dl></td>
<td>O modem (ou outro dispositivo de conexão) foi desconectado devido a uma falha de link.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_USER_LOGOFF"></span><span id="error_user_logoff"></span><dl> <dt><strong>ERROR_USER_LOGOFF</strong></dt> <dt>830</dt> </dl></td>
<td>A conexão foi encerrada porque o usuário fez logo off.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAST_USER_SWITCH"></span><span id="error_fast_user_switch"></span><dl> <dt><strong>ERROR_FAST_USER_SWITCH</strong></dt> <dt>831</dt> </dl></td>
<td>A conexão foi encerrada porque a opção de usuário ocorreu.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_HIBERNATION"></span><span id="error_hibernation"></span><dl> <dt><strong>ERROR_HIBERNATION</strong></dt> <dt>832</dt> </dl></td>
<td>A conexão foi encerrada devido à hibernação.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_SYSTEM_SUSPENDED"></span><span id="error_system_suspended"></span><dl> <dt><strong>ERROR_SYSTEM_SUSPENDED</strong></dt> <dt>833</dt> </dl></td>
<td>A conexão foi encerrada porque o sistema foi suspenso.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_RASMAN_SERVICE_STOPPED"></span><span id="error_rasman_service_stopped"></span><dl> <dt><strong>ERROR_RASMAN_SERVICE_STOPPED</strong></dt> <dt>834</dt> </dl></td>
<td>A conexão foi encerrada porque o Gerenciador de Conexões de Acesso Remoto parou.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SERVER_CERT"></span><span id="error_invalid_server_cert"></span><dl> <dt><strong>ERROR_INVALID_SERVER_CERT</strong></dt> <dt>835</dt> </dl></td>
<td>Falha na tentativa de conexão L2TP porque a camada de segurança não pôde autenticar o computador remoto. Isso pode ser porque um ou mais campos do certificado apresentado pelo servidor remoto não puderam ser validados como pertencentes ao destino de destino.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_NAP_CAPABLE"></span><span id="error_not_nap_capable"></span><dl> <dt><strong>ERROR_NOT_NAP_CAPABLE</strong></dt> <dt>836</dt> </dl></td>
<td>O computador não é capaz de NAP.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows Vista e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_TUNNELID"></span><span id="error_invalid_tunnelid"></span><dl> <dt><strong>ERROR_INVALID_TUNNELID</strong></dt> <dt>837</dt> </dl></td>
<td>ID Tunnel inválida.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows 7 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS"></span><span id="error_updateconnection_request_in_process"></span><dl> <dt><strong>ERROR_UPDATECONNECTION_REQUEST_IN_PROCESS</strong></dt> <dt>838</dt> </dl></td>
<td>Outra solicitação de conexão de atualização está em andamento. O RAS permite apenas uma solicitação de conexão de atualização por vez.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows 7 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ENGINE_DISABLED"></span><span id="error_protocol_engine_disabled"></span><dl> <dt><strong>ERROR_PROTOCOL_ENGINE_DISABLED</strong></dt> <dt>839</dt> </dl></td>
<td>A negociação usando o protocolo configurado é desabilitada. Edite as propriedades de conexão, selecione um protocolo diferente para negociação e tente novamente.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows 7 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERNAL_ADDRESS_FAILURE"></span><span id="error_internal_address_failure"></span><dl> <dt><strong>ERROR_INTERNAL_ADDRESS_FAILURE</strong></dt> <dt>840</dt> </dl></td>
<td>Falha na negociação de endereço interno.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows 7 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_FAILED_CP_REQUIRED"></span><span id="error_failed_cp_required"></span><dl> <dt><strong>ERROR_FAILED_CP_REQUIRED</strong></dt> <dt>841</dt> </dl></td>
<td>O cliente precisa solicitar um endereço IPv4 ou IPv6 interno.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows 7 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_TS_UNACCEPTABLE"></span><span id="error_ts_unacceptable"></span><dl> <dt><strong>ERROR_TS_UNACCEPTABLE</strong></dt> <dt>842</dt> </dl></td>
<td>Falha na negociação dos Seletores de Tráfego.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows 7 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MOBIKE_DISABLED"></span><span id="error_mobike_disabled"></span><dl> <dt><strong>ERROR_MOBIKE_DISABLED</strong></dt> <dt>843</dt> </dl></td>
<td>A mobilidade está desabilitada para essa conexão.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows 7 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_CANNOT_INITIATE_MOBIKE_UPDATE"></span><span id="error_cannot_initiate_mobike_update"></span><dl> <dt><strong>ERROR_CANNOT_INITIATE_MOBIKE_UPDATE</strong></dt> <dt>844</dt> </dl></td>
<td>A Conexão VPN ainda está se conectando ou autenticando-se de forma reentrnte devido à alteração de estado de quarentena. Inicie a atualização móvel somente quando o estado da conexão for 'Conectado'.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows 7 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV"></span><span id="error_peap_server_rejected_client_tlv"></span><dl> <dt><strong>ERROR_PEAP_SERVER_REJECTED_CLIENT_TLV</strong></dt> <dt>845</dt> </dl></td>
<td>O servidor rejeitou a autenticação de cliente devido a uma incompatibilidade inesperada de TLV ou valor para um TLV.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows 7 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_PREFERENCES"></span><span id="error_invalid_preferences"></span><dl> <dt><strong>ERROR_INVALID_PREFERENCES</strong></dt> <dt>846</dt> </dl></td>
<td>A preferência de destino vpn não é selecionada pelo usuário ou não é mais válida.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows 7 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID"></span><span id="error_eaptls_scard_cache_credentials_invalid"></span><dl> <dt><strong>ERROR_EAPTLS_SCARD_CACHE_CREDENTIALS_INVALID</strong></dt> <dt>847</dt> </dl></td>
<td>A credencial de cartão inteligente armazenada em cache é inválida.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows 7 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SSTP_COOKIE_SET_FAILURE"></span><span id="error_sstp_cookie_set_failure"></span><dl> <dt><strong>ERROR_SSTP_COOKIE_SET_FAILURE</strong></dt> <dt>848</dt> </dl></td>
<td>Falha na tentativa de conexão VPN devido a um erro interno ao adicionar cookies ao protocolo SSTP. Consulte o Log de Eventos do Sistema para obter as informações detalhadas.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES"></span><span id="error_invalid_peap_cookie_attributes"></span><dl> <dt><strong>ERROR_INVALID_PEAP_COOKIE_ATTRIBUTES</strong></dt> <dt>849</dt> </dl></td>
<td>Os atributos de método interno PEAP armazenados no cookie são/são inválidos.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_NOT_INSTALLED"></span><span id="error_eap_method_not_installed"></span><dl> <dt><strong>ERROR_EAP_METHOD_NOT_INSTALLED</strong></dt> <dt>850</dt> </dl></td>
<td>O tipo de Protocolo de Autenticação Extensível necessário para autenticação da conexão de acesso remoto não está instalado no computador.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO"></span><span id="error_eap_method_does_not_support_sso"></span><dl> <dt><strong>ERROR_EAP_METHOD_DOES_NOT_SUPPORT_SSO</strong></dt> <dt>851</dt> </dl></td>
<td>O tipo de Protocolo de Autenticação Extensível configurado na conexão de acesso remoto não dá suporte ao login único.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED"></span><span id="error_eap_method_operation_not_supported"></span><dl> <dt><strong>ERROR_EAP_METHOD_OPERATION_NOT_SUPPORTED</strong></dt> <dt>852</dt> </dl></td>
<td>O tipo de Protocolo de Autenticação Extensível configurado na conexão de acesso remoto não dá suporte à operação solicitada.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_INVALID"></span><span id="error_eap_user_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_INVALID</strong></dt> <dt>853</dt> </dl></td>
<td>A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado que autentica o cliente no servidor não é válido. Verifique se o certificado usado para autenticação é válido.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_EXPIRED"></span><span id="error_eap_user_cert_expired"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_EXPIRED</strong></dt> <dt>854</dt> </dl></td>
<td>A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado que autentica o cliente no servidor expirou. Renove o certificado.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_CERT_REVOKED"></span><span id="error_eap_user_cert_revoked"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_REVOKED</strong></dt> <dt>855</dt> </dl></td>
<td>A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado que autentica o cliente no servidor foi revogado. Use um certificado que não foi revogado.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_CERT_OTHER_ERROR"></span><span id="error_eap_user_cert_other_error"></span><dl> <dt><strong>ERROR_EAP_USER_CERT_OTHER_ERROR</strong></dt> <dt>856</dt> </dl></td>
<td>A conexão de acesso remoto foi concluída, mas a autenticação falhou devido a um erro no certificado que autentica o cliente no servidor.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_INVALID"></span><span id="error_eap_server_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_INVALID</strong></dt> <dt>857</dt> </dl></td>
<td>A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado que o cliente usa para autenticar o servidor não é válido.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_EXPIRED"></span><span id="error_eap_server_cert_expired"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_EXPIRED</strong></dt> <dt>858</dt> </dl></td>
<td>A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado que o cliente usa para autenticar o servidor expirou.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_CERT_REVOKED"></span><span id="error_eap_server_cert_revoked"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_REVOKED</strong></dt> <dt>859</dt> </dl></td>
<td>A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado que o cliente usa para autenticar o servidor foi revogado.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_CERT_OTHER_ERROR"></span><span id="error_eap_server_cert_other_error"></span><dl> <dt><strong>ERROR_EAP_SERVER_CERT_OTHER_ERROR</strong></dt> <dt>860</dt> </dl></td>
<td>A conexão de acesso remoto foi concluída, mas a autenticação falhou devido a um erro no certificado que o cliente usa para autenticar o servidor.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_user_root_cert_not_found"></span><dl> <dt><strong>ERROR_EAP_USER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>861</dt> </dl></td>
<td>A conexão de acesso remoto foi concluída, mas a autenticação falhou porque um certificado raiz confiável que valida o certificado de usuário não foi encontrado no armazenamento de certificados de Autoridades de Certificação Confiáveis.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_USER_ROOT_CERT_INVALID"></span><span id="error_eap_user_root_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_USER_ROOT_CERT_INVALID</strong></dt> <dt>862</dt> </dl></td>
<td>A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado raiz confiável usado para validar o certificado de usuário não é válido.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_USER_ROOT_CERT_EXPIRED"></span><span id="error_eap_user_root_cert_expired"></span><dl> <dt><strong>ERROR_EAP_USER_ROOT_CERT_EXPIRED</strong></dt> <dt>863</dt> </dl></td>
<td>A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado no armazenamento de certificados autoridades de certificação confiáveis que autentica o certificado de usuário expirou. Renove o certificado.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND"></span><span id="error_eap_server_root_cert_not_found"></span><dl> <dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NOT_FOUND</strong></dt> <dt>864</dt> </dl></td>
<td>A conexão de acesso remoto foi concluída, mas a autenticação falhou porque um certificado que valida o certificado do servidor não foi encontrado no armazenamento de certificados autoridades de certificação confiáveis.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_INVALID"></span><span id="error_eap_server_root_cert_invalid"></span><dl> <dt><strong>ERROR_EAP_SERVER_ROOT_CERT_INVALID</strong></dt> <dt>865</dt> </dl></td>
<td>A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado no armazenamento de certificados autoridades de certificação confiáveis que valida o certificado do servidor não é válido.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED"></span><span id="error_eap_server_root_cert_name_required"></span><dl> <dt><strong>ERROR_EAP_SERVER_ROOT_CERT_NAME_REQUIRED</strong></dt> <dt>866</dt> </dl></td>
<td>A conexão de acesso remoto foi concluída, mas a autenticação falhou porque o certificado no computador do servidor não tem um nome de servidor especificado.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEAP_IDENTITY_MISMATCH"></span><span id="error_peap_identity_mismatch"></span><dl> <dt><strong>ERROR_PEAP_IDENTITY_MISMATCH</strong></dt> <dt>867</dt> </dl></td>
<td>A identidade externa peap não é igual à identidade interna quando a privacidade da identidade é desligada.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DNSNAME_NOT_RESOLVABLE"></span><span id="error_dnsname_not_resolvable"></span><dl> <dt><strong>ERROR_DNSNAME_NOT_RESOLVABLE</strong></dt> <dt>868</dt> </dl></td>
<td>A conexão remota não foi feita porque o nome do servidor de acesso remoto não foi resolvido.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_EAPTLS_PASSWD_INVALID"></span><span id="error_eaptls_passwd_invalid"></span><dl> <dt><strong>ERROR_EAPTLS_PASSWD_INVALID</strong></dt> <dt>869</dt> </dl></td>
<td>A senha fornecida para o certificado não é válida.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS"></span><span id="error_ikev2_psk_interface_already_exists"></span><dl> <dt><strong>ERROR_IKEV2_PSK_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>870</dt> </dl></td>
<td>A interface não pôde ser habilitada porque mais de uma interface com o mesmo destino foi criada com o método de autenticação de chave pré-compartilhada. Altere o método de destino/auth e habilita a interface .<br/></td>
</tr>
</tbody>
</table>



 

Os seguintes códigos de erro de API de Roteamento e Acesso Remoto (RRAS) são definidos em mprerror.h. Todos os códigos de erro têm suporte no Windows 2000 ou versões posteriores do Windows a menos que especificado de outra forma.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valor/código de retorno</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="ERROR_ROUTER_STOPPED"></span><span id="error_router_stopped"></span><dl> <dt><strong>ERROR_ROUTER_STOPPED</strong></dt> <dt>900</dt> </dl></td>
<td>O roteador não está em execução.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALREADY_CONNECTED"></span><span id="error_already_connected"></span><dl> <dt><strong>ERROR_ALREADY_CONNECTED</strong></dt> <dt>901</dt> </dl></td>
<td>A interface já está conectada.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_UNKNOWN_PROTOCOL_ID"></span><span id="error_unknown_protocol_id"></span><dl> <dt><strong>ERROR_UNKNOWN_PROTOCOL_ID</strong></dt> <dt>902</dt> </dl></td>
<td>O identificador de protocolo especificado não é conhecido pelo roteador.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_DDM_NOT_RUNNING"></span><span id="error_ddm_not_running"></span><dl> <dt><strong>ERROR_DDM_NOT_RUNNING</strong></dt> <dt>903</dt> </dl></td>
<td>O DDM (Gerenciador de Interface discada por demanda) não está em execução.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_ALREADY_EXISTS"></span><span id="error_interface_already_exists"></span><dl> <dt><strong>ERROR_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>904</dt> </dl></td>
<td>Uma interface com esse nome já está registrada com o roteador.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_SUCH_INTERFACE"></span><span id="error_no_such_interface"></span><dl> <dt><strong>ERROR_NO_SUCH_INTERFACE</strong></dt> <dt>905</dt> </dl></td>
<td>Uma interface com esse nome não está registrada com o roteador.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_NOT_CONNECTED"></span><span id="error_interface_not_connected"></span><dl> <dt><strong>ERROR_INTERFACE_NOT_CONNECTED</strong></dt> <dt>906</dt> </dl></td>
<td>A interface não está conectada.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_STOP_PENDING"></span><span id="error_protocol_stop_pending"></span><dl> <dt><strong>ERROR_PROTOCOL_STOP_PENDING</strong></dt> <dt>907</dt> </dl></td>
<td>O protocolo especificado está parando.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONNECTED"></span><span id="error_interface_connected"></span><dl> <dt><strong>ERROR_INTERFACE_CONNECTED</strong></dt> <dt>908</dt> </dl></td>
<td>A interface está conectada e, portanto, não pode ser excluída.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NO_INTERFACE_CREDENTIALS_SET"></span><span id="error_no_interface_credentials_set"></span><dl> <dt><strong>ERROR_NO_INTERFACE_CREDENTIALS_SET</strong></dt> <dt>909</dt> </dl></td>
<td>As credenciais da interface não foram definidas.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_ALREADY_CONNECTING"></span><span id="error_already_connecting"></span><dl> <dt><strong>ERROR_ALREADY_CONNECTING</strong></dt> <dt>910</dt> </dl></td>
<td>Essa interface já está no processo de conexão.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_UPDATE_IN_PROGRESS"></span><span id="error_update_in_progress"></span><dl> <dt><strong>ERROR_UPDATE_IN_PROGRESS</strong></dt> <dt>911</dt> </dl></td>
<td>Uma atualização das informações de roteamento nessa interface já está em andamento.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_CONFIGURATION"></span><span id="error_interface_configuration"></span><dl> <dt><strong>ERROR_INTERFACE_CONFIGURATION</strong></dt> <dt>912</dt> </dl></td>
<td>A configuração da interface não é válida. Já há outra interface conectada à mesma interface no roteador remoto.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_NOT_CLIENT_PORT"></span><span id="error_not_client_port"></span><dl> <dt><strong>ERROR_NOT_CLIENT_PORT</strong></dt> <dt>913</dt> </dl></td>
<td>Um Cliente de Acesso Remoto tentou se conectar por uma porta reservada somente para roteadores.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NOT_ROUTER_PORT"></span><span id="error_not_router_port"></span><dl> <dt><strong>ERROR_NOT_ROUTER_PORT</strong></dt> <dt>914</dt> </dl></td>
<td>Um roteador de discagem de demanda tentou se conectar por uma porta reservada somente para clientes de acesso remoto.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_CLIENT_INTERFACE_ALREADY_EXISTS"></span><span id="error_client_interface_already_exists"></span><dl> <dt><strong>ERROR_CLIENT_INTERFACE_ALREADY_EXISTS</strong></dt> <dt>915</dt> </dl></td>
<td>A interface do cliente com esse nome já existe e está conectada no momento.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INTERFACE_DISABLED"></span><span id="error_interface_disabled"></span><dl> <dt><strong>ERROR_INTERFACE_DISABLED</strong></dt> <dt>916</dt> </dl></td>
<td>A interface está em um estado desabilitado.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_AUTH_PROTOCOL_REJECTED"></span><span id="error_auth_protocol_rejected"></span><dl> <dt><strong>ERROR_AUTH_PROTOCOL_REJECTED</strong></dt> <dt>917</dt> </dl></td>
<td>O protocolo de autenticação foi rejeitado pelo par remoto.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_AUTH_PROTOCOL_AVAILABLE"></span><span id="error_no_auth_protocol_available"></span><dl> <dt><strong>ERROR_NO_AUTH_PROTOCOL_AVAILABLE</strong></dt> <dt>918</dt> </dl></td>
<td>Não há nenhum protocolo de autenticação disponível para uso.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PEER_REFUSED_AUTH"></span><span id="error_peer_refused_auth"></span><dl> <dt><strong>ERROR_PEER_REFUSED_AUTH</strong></dt> <dt>919</dt> </dl></td>
<td>Não foi possível estabelecer a conexão porque o protocolo de autenticação usado pelo servidor RAS/VPN para verificar seu nome de usuário e senha não pôde ser correspondente às configurações em seu perfil de conexão.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_NO_DIALIN_PERMISSION"></span><span id="error_remote_no_dialin_permission"></span><dl> <dt><strong>ERROR_REMOTE_NO_DIALIN_PERMISSION</strong></dt> <dt>920</dt> </dl></td>
<td>A conta remota não tem permissão de Acesso Remoto.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_PASSWD_EXPIRED"></span><span id="error_remote_passwd_expired"></span><dl> <dt><strong>ERROR_REMOTE_PASSWD_EXPIRED</strong></dt> <dt>921</dt> </dl></td>
<td>A conta remota expirou.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_ACCT_DISABLED"></span><span id="error_remote_acct_disabled"></span><dl> <dt><strong>ERROR_REMOTE_ACCT_DISABLED</strong></dt> <dt>922</dt> </dl></td>
<td>A conta remota está desabilitada.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTE_RESTRICTED_LOGON_HOURS"></span><span id="error_remote_restricted_logon_hours"></span><dl> <dt><strong>ERROR_REMOTE_RESTRICTED_LOGON_HOURS</strong></dt> <dt>923</dt> </dl></td>
<td>A conta remota não tem permissão para fazer logon neste momento do dia.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_REMOTE_AUTHENTICATION_FAILURE"></span><span id="error_remote_authentication_failure"></span><dl> <dt><strong>ERROR_REMOTE_AUTHENTICATION_FAILURE</strong></dt> <dt>924</dt> </dl></td>
<td>O acesso foi negado ao par remoto porque o nome de usuário, a senha ou ambos não são válidos no domínio.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_HAS_NO_DEVICES"></span><span id="error_interface_has_no_devices"></span><dl> <dt><strong>ERROR_INTERFACE_HAS_NO_DEVICES</strong></dt> <dt>925</dt> </dl></td>
<td>Não há portas habilitadas para roteamento disponíveis para uso por essa interface discada de demanda.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_IDLE_DISCONNECTED"></span><span id="error_idle_disconnected"></span><dl> <dt><strong>ERROR_IDLE_DISCONNECTED</strong></dt> <dt>926</dt> </dl></td>
<td>A porta foi desconectada devido à inatividade.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_UNREACHABLE"></span><span id="error_interface_unreachable"></span><dl> <dt><strong>ERROR_INTERFACE_UNREACHABLE</strong></dt> <dt>927</dt> </dl></td>
<td>A interface não está acessível no momento.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_SERVICE_IS_PAUSED"></span><span id="error_service_is_paused"></span><dl> <dt><strong>ERROR_SERVICE_IS_PAUSED</strong></dt> <dt>928</dt> </dl></td>
<td>O serviço Discagem de Demanda está em um estado de pausa.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INTERFACE_DISCONNECTED"></span><span id="error_interface_disconnected"></span><dl> <dt><strong>ERROR_INTERFACE_DISCONNECTED</strong></dt> <dt>929</dt> </dl></td>
<td>A interface foi desconectada pelo administrador.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_SERVER_TIMEOUT"></span><span id="error_auth_server_timeout"></span><dl> <dt><strong>ERROR_AUTH_SERVER_TIMEOUT</strong></dt> <dt>930</dt> </dl></td>
<td>O servidor de autenticação não respondeu às solicitações de autenticação em tempo hábil.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PORT_LIMIT_REACHED"></span><span id="error_port_limit_reached"></span><dl> <dt><strong>ERROR_PORT_LIMIT_REACHED</strong></dt> <dt>931</dt> </dl></td>
<td>O número máximo de portas permitidas para uso na conexão multi-vinculada foi atingido.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_PPP_SESSION_TIMEOUT"></span><span id="error_ppp_session_timeout"></span><dl> <dt><strong>ERROR_PPP_SESSION_TIMEOUT</strong></dt> <dt>932</dt> </dl></td>
<td>O limite de tempo de conexão para o usuário foi atingido.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_LAN_INTERFACE_LIMIT"></span><span id="error_max_lan_interface_limit"></span><dl> <dt><strong>ERROR_MAX_LAN_INTERFACE_LIMIT</strong></dt> <dt>933</dt> </dl></td>
<td>O limite máximo no número de interfaces LAN com suporte foi atingido.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_MAX_WAN_INTERFACE_LIMIT"></span><span id="error_max_wan_interface_limit"></span><dl> <dt><strong>ERROR_MAX_WAN_INTERFACE_LIMIT</strong></dt> <dt>934</dt> </dl></td>
<td>O limite máximo no número de interfaces discadas de demanda com suporte foi atingido.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_MAX_CLIENT_INTERFACE_LIMIT"></span><span id="error_max_client_interface_limit"></span><dl> <dt><strong>ERROR_MAX_CLIENT_INTERFACE_LIMIT</strong></dt> <dt>935</dt> </dl></td>
<td>O limite máximo no número de Clientes de Acesso Remoto com suporte foi atingido.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_BAP_DISCONNECTED"></span><span id="error_bap_disconnected"></span><dl> <dt><strong>ERROR_BAP_DISCONNECTED</strong></dt> <dt>936</dt> </dl></td>
<td>A porta foi desconectada devido à política BAP (Protocolo de Alocação de Largura de Banda).<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_USER_LIMIT"></span><span id="error_user_limit"></span><dl> <dt><strong>ERROR_USER_LIMIT</strong></dt> <dt>937</dt> </dl></td>
<td>Como outra conexão do seu tipo está em uso, a conexão de entrada não pode aceitar sua solicitação de conexão.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_RADIUS_SERVERS"></span><span id="error_no_radius_servers"></span><dl> <dt><strong>ERROR_NO_RADIUS_SERVERS</strong></dt> <dt>938</dt> </dl></td>
<td>Nenhum servidor RADIUS foi localizado na rede.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_RADIUS_RESPONSE"></span><span id="error_invalid_radius_response"></span><dl> <dt><strong>ERROR_INVALID_RADIUS_RESPONSE</strong></dt> <dt>939</dt> </dl></td>
<td>A resposta recebida do servidor de autenticação RADIUS não era válida. Certifique-se de que a senha secreta com valor de minúsculas para o servidor RADIUS está definida corretamente.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALIN_HOURS_RESTRICTION"></span><span id="error_dialin_hours_restriction"></span><dl> <dt><strong>ERROR_DIALIN_HOURS_RESTRICTION</strong></dt> <dt>940</dt> </dl></td>
<td>Você não tem permissão para se conectar no momento.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ALLOWED_PORT_TYPE_RESTRICTION"></span><span id="error_allowed_port_type_restriction"></span><dl> <dt><strong>ERROR_ALLOWED_PORT_TYPE_RESTRICTION</strong></dt> <dt>941</dt> </dl></td>
<td>Você não tem permissão para se conectar usando o tipo de dispositivo atual.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTH_PROTOCOL_RESTRICTION"></span><span id="error_auth_protocol_restriction"></span><dl> <dt><strong>ERROR_AUTH_PROTOCOL_RESTRICTION</strong></dt> <dt>942</dt> </dl></td>
<td>Não foi possível estabelecer a conexão porque o método de autenticação usado pelo seu perfil de conexão não é permitido para uso por uma política de acesso configurada no servidor RAS/VPN. Especificamente, isso pode ser devido a diferenças de configuração entre o método de autenticação selecionado no servidor RAS/VPN e a política de acesso configurada para ele.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_BAP_REQUIRED"></span><span id="error_bap_required"></span><dl> <dt><strong>ERROR_BAP_REQUIRED</strong></dt> <dt>943</dt> </dl></td>
<td>O BAP é necessário para esse usuário.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_DIALOUT_HOURS_RESTRICTION"></span><span id="error_dialout_hours_restriction"></span><dl> <dt><strong>ERROR_DIALOUT_HOURS_RESTRICTION</strong></dt> <dt>944</dt> </dl></td>
<td>A interface não tem permissão para se conectar no momento.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_ROUTER_CONFIG_INCOMPATIBLE"></span><span id="error_router_config_incompatible"></span><dl> <dt><strong>ERROR_ROUTER_CONFIG_INCOMPATIBLE</strong></dt> <dt>945</dt> </dl></td>
<td>A configuração do roteador salvo é incompatível com o roteador atual.<br/></td>
</tr>
<tr class="odd">
<td><span id="WARNING_NO_MD5_MIGRATION"></span><span id="warning_no_md5_migration"></span><dl> <dt><strong>WARNING_NO_MD5_MIGRATION</strong></dt> <dt>946</dt> </dl></td>
<td>O Acesso Remoto detectou contas de usuário de formato mais antigo que não serão migradas automaticamente.<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_PROTOCOL_ALREADY_INSTALLED"></span><span id="error_protocol_already_installed"></span><dl> <dt><strong>ERROR_PROTOCOL_ALREADY_INSTALLED</strong></dt> <dt>948</dt> </dl></td>
<td>O transporte já está instalado com o roteador.<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_SIGNATURE_LENGTH"></span><span id="error_invalid_signature_length"></span><dl> <dt><strong>ERROR_INVALID_SIGNATURE_LENGTH</strong></dt> <dt>949</dt> </dl></td>
<td>O comprimento da assinatura recebido em um pacote do servidor RADIUS não é válido.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows XP e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_SIGNATURE"></span><span id="error_invalid_signature"></span><dl> <dt><strong>ERROR_INVALID_SIGNATURE</strong></dt> <dt>950</dt> </dl></td>
<td>A assinatura recebida em um pacote do servidor RADIUS não é válida.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows XP e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_NO_SIGNATURE"></span><span id="error_no_signature"></span><dl> <dt><strong>ERROR_NO_SIGNATURE</strong></dt> <dt>951</dt> </dl></td>
<td>Não recebeu assinatura junto com EAPMessage do servidor RADIUS.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows XP e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET_LENGTH_OR_ID"></span><span id="error_invalid_packet_length_or_id"></span><dl> <dt><strong>ERROR_INVALID_PACKET_LENGTH_OR_ID</strong></dt> <dt>952</dt> </dl></td>
<td>O comprimento ou a ID recebida em um pacote do servidor RADIUS não é válido.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows XP e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_INVALID_ATTRIBUTE_LENGTH"></span><span id="error_invalid_attribute_length"></span><dl> <dt><strong>ERROR_INVALID_ATTRIBUTE_LENGTH</strong></dt> <dt>953</dt> </dl></td>
<td>O comprimento recebido em um pacote com o atributo do servidor RADIUS não é válido.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows XP e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_INVALID_PACKET"></span><span id="error_invalid_packet"></span><dl> <dt><strong>ERROR_INVALID_PACKET</strong></dt> <dt>954</dt> </dl></td>
<td>O pacote recebido do servidor RADIUS não é válido.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows XP e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span id="ERROR_AUTHENTICATOR_MISMATCH"></span><span id="error_authenticator_mismatch"></span><dl> <dt><strong>ERROR_AUTHENTICATOR_MISMATCH</strong></dt> <dt>955</dt> </dl></td>
<td>Authenticator não corresponder no pacote do servidor RADIUS.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows XP e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="ERROR_REMOTEACCESS_NOT_CONFIGURED"></span><span id="error_remoteaccess_not_configured"></span><dl> <dt><strong>ERROR_REMOTEACCESS_NOT_CONFIGURED</strong></dt> <dt>956</dt> </dl></td>
<td>O roteamento e o servidor de acesso remoto não estão configurados ou não estão em execução.<br/>
<blockquote>
[!Note]<br />
Com suporte no Windows 7 e versões posteriores do Windows.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



 

 





