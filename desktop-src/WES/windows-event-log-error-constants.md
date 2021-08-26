---
title: Windows Constantes de erro do log de eventos (WinError. h)
description: a seguir estão os códigos de erro que Windows Log de eventos define.
ms.assetid: 889ea4ae-dede-45d5-9293-cec85d81f010
topic_type:
- apiref
api_name:
- ERROR_EVT_INVALID_CHANNEL_PATH
- ERROR_EVT_INVALID_QUERY
- ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND
- ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND
- ERROR_EVT_INVALID_PUBLISHER_NAME
- ERROR_EVT_INVALID_EVENT_DATA
- ERROR_EVT_CHANNEL_NOT_FOUND
- ERROR_EVT_MALFORMED_XML_TEXT
- ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL
- ERROR_EVT_CONFIGURATION_ERROR
- ERROR_EVT_QUERY_RESULT_STALE
- ERROR_EVT_QUERY_RESULT_INVALID_POSITION
- ERROR_EVT_NON_VALIDATING_MSXML
- ERROR_EVT_FILTER_ALREADYSCOPED
- ERROR_EVT_FILTER_NOTELTSET
- ERROR_EVT_FILTER_INVARG
- ERROR_EVT_FILTER_INVTEST
- ERROR_EVT_FILTER_INVTYPE
- ERROR_EVT_FILTER_PARSEERR
- ERROR_EVT_FILTER_UNSUPPORTEDOP
- ERROR_EVT_FILTER_UNEXPECTEDTOKEN
- ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL
- ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE
- ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE
- ERROR_EVT_CHANNEL_CANNOT_ACTIVATE
- ERROR_EVT_FILTER_TOO_COMPLEX
- ERROR_EVT_MESSAGE_NOT_FOUND
- ERROR_EVT_MESSAGE_ID_NOT_FOUND
- ERROR_EVT_UNRESOLVED_VALUE_INSERT
- ERROR_EVT_UNRESOLVED_PARAMETER_INSERT
- ERROR_EVT_MAX_INSERTS_REACHED
- ERROR_EVT_EVENT_DEFINITION_NOT_FOUND
- ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND
- ERROR_EVT_VERSION_TOO_OLD
- ERROR_EVT_VERSION_TOO_NEW
- ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY
- ERROR_EVT_PUBLISHER_DISABLED
- ERROR_EVT_FILTER_OUT_OF_RANGE
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f6f0bd3e2805c02dad78c064b56a443bfbb596cf42f25e9b52ac7ba584f123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031936"
---
# <a name="windows-event-log-error-constants"></a>Windows Constantes de erro do log de eventos

a seguir estão os códigos de erro que Windows Log de eventos define.

<dl> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERRO \_ EVT \_ \_ caminho de canal inválido \_**
</dt> <dd> <dl> <dt>

15000
</dt> <dt>



O caminho de canal especificado não é válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERRO \_ EVT \_ de \_ consulta inválida**
</dt> <dd> <dl> <dt>

15001
</dt> <dt>



A consulta especificada não é válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERRO \_ EVT \_ metadados do Publicador \_ \_ não \_ encontrados**
</dt> <dd> <dl> <dt>

15002
</dt> <dt>



Os metadados do provedor não podem ser encontrados no recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERRO \_ de \_ modelo de evento EVT \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

15003
</dt> <dt>



O modelo para uma definição de evento não pode ser encontrado no recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERRO \_ EVT \_ \_ nome de editor inválido \_**
</dt> <dd> <dl> <dt>

15004
</dt> <dt>



O nome do provedor especificado não é válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERRO \_ EVT \_ \_ dados de eventos inválidos \_**
</dt> <dd> <dl> <dt>

15005
</dt> <dt>



Os dados de evento gerados pelo provedor não são compatíveis com a definição do modelo de evento no manifesto do provedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERRO \_ EVT \_ canal \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

15007
</dt> <dt>



O canal especificado não pode ser encontrado. Verifique a configuração do canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERRO \_ EVT \_ de \_ texto XML malformado \_**
</dt> <dd> <dl> <dt>

15008
</dt> <dt>



O texto XML especificado não estava bem formado. Para obter mais informações, chame a função [**EvtGetExtendedStatus**](/windows/desktop/api/WinEvt/nf-winevt-evtgetextendedstatus) .


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**\_ \_ assinatura de erro \_ EVT \_ para \_ canal direto**
</dt> <dd> <dl> <dt>

15009
</dt> <dt>



Não é possível assinar um canal analítico ou de depuração; os eventos de um canal analítico ou de depuração vão diretamente para um arquivo de log e não podem ser assinados.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**erro \_ de \_ configuração de EVT \_**
</dt> <dd> <dl> <dt>

15010
</dt> <dt>



Ocorreu um erro de configuração.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERRO \_ EVT \_ do \_ resultado da consulta \_ obsoleto**
</dt> <dd> <dl> <dt>

15011
</dt> <dt>



O resultado da consulta não é válido. Isso pode ser devido ao log ser limpo ou revertida depois que o resultado da consulta foi criado. Libere o objeto de resultado da consulta e emita novamente a consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERRO \_ EVT do \_ resultado da consulta \_ \_ posição inválida \_**
</dt> <dd> <dl> <dt>

15012
</dt> <dt>



O cursor do resultado da consulta não está apontando para uma posição válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERRO \_ EVT \_ não \_ Validando \_ MSXML**
</dt> <dd> <dl> <dt>

15013
</dt> <dt>



o analisador de MSXML registrado não oferece suporte à validação.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERRO \_ EVT \_ filtro \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014
</dt> <dt>



Uma expressão pode ser seguida por uma alteração de operação de escopo somente se a expressão for avaliada como um conjunto de nós e ainda não fizer parte de alguma outra alteração de operação de escopo.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERRO \_ EVT \_ filtro \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015
</dt> <dt>



Não é possível executar uma operação de etapa a partir de um termo que não representa um conjunto de elementos.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERRO \_ EVT \_ filtro \_ INVARG**
</dt> <dd> <dl> <dt>

15016
</dt> <dt>



Os argumentos no lado esquerdo de um operador binário devem ser atributos, nós ou variáveis, e os argumentos no lado direito devem ser constantes.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERRO \_ EVT \_ filtro \_ INVTEST**
</dt> <dd> <dl> <dt>

15017
</dt> <dt>



Uma operação de etapa deve envolver um teste de nó ou, no caso de um predicado, uma expressão algébricas para testar cada nó no conjunto de nós identificado pelo conjunto de nós anterior pode ser avaliada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERRO \_ EVT \_ filtro \_ INVTYPE**
</dt> <dd> <dl> <dt>

15018
</dt> <dt>



Não há suporte para esse tipo de dados.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERRO \_ EVT \_ filtro \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019
</dt> <dt>



Ocorreu um erro de sintaxe na posição especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERRO \_ EVT \_ filtro \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020
</dt> <dt>



Este operador não tem suporte nesta implementação do filtro.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERRO \_ EVT \_ filtro \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021
</dt> <dt>



O token encontrado era inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERRO \_ EVT \_ de \_ operação inválida sobre o \_ \_ \_ canal direto habilitado \_**
</dt> <dd> <dl> <dt>

15022
</dt> <dt>



A operação solicitada não pode ser executada em um canal analítico ou de depuração habilitado. Você deve desabilitar o canal antes de executar a operação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERRO \_ EVT \_ \_ valor de propriedade de canal inválido \_ \_**
</dt> <dd> <dl> <dt>

15023
</dt> <dt>



A propriedade Channel contém um valor que não é válido. O tipo do valor não pode ser válido, o valor pode estar fora do intervalo ou o valor não pode ser atualizado ou não tem suporte para esse tipo de canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERRO \_ EVT \_ \_ valor de \_ propriedade de Publicador inválido \_**
</dt> <dd> <dl> <dt>

15024
</dt> <dt>



A propriedade Provider contém um valor que não é válido. O tipo do valor pode não ser válido, o valor pode estar fora do intervalo ou o valor não pode ser atualizado ou não tem suporte para esse tipo de provedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERRO \_ EVT de \_ canal \_ não pode \_ Ativar**
</dt> <dd> <dl> <dt>

15025
</dt> <dt>



Falha ao ativar o canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**filtro de erro \_ EVT \_ \_ muito \_ complexo**
</dt> <dd> <dl> <dt>

15026
</dt> <dt>



A expressão XPath excedeu a complexidade com suporte. Simplifique a expressão ou divida-a em duas ou mais expressões simples.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**mensagem de erro \_ EVT \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

15027
</dt> <dt>



O recurso de mensagem está presente, mas a mensagem não foi encontrada na cadeia de caracteres ou na tabela de mensagens.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ID de mensagem de erro \_ EVT \_ \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

15028
</dt> <dt>



O identificador de mensagem não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERRO \_ EVT de \_ inserção de \_ valor não resolvido \_**
</dt> <dd> <dl> <dt>

15029
</dt> <dt>



Não é possível encontrar a cadeia de caracteres de substituição para o índice de inserção.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERRO \_ EVT de \_ inserção de \_ parâmetro não resolvido \_**
</dt> <dd> <dl> <dt>

15030
</dt> <dt>



Não é possível encontrar a cadeia de caracteres de descrição para a referência de parâmetro (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERRO \_ EVT \_ máximo de \_ inserções \_ atingido**
</dt> <dd> <dl> <dt>

15031
</dt> <dt>



O número máximo de substituições foi atingido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**\_definição de evento EVT de erro \_ \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

15032
</dt> <dt>



A definição de evento não pode ser encontrada para o identificador de evento.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERRO \_ EVT \_ localidade de mensagem \_ \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

15033
</dt> <dt>



O recurso específico da localidade para a mensagem desejada não está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**versão de erro \_ EVT \_ \_ muito \_ antiga**
</dt> <dd> <dl> <dt>

15034
</dt> <dt>



O recurso é muito antigo para ser compatível.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**versão de erro \_ EVT \_ \_ muito \_ nova**
</dt> <dd> <dl> <dt>

15035
</dt> <dt>



O recurso é muito novo para ser compatível.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**o erro \_ EVT \_ não pode \_ abrir o \_ canal \_ de \_ consulta**
</dt> <dd> <dl> <dt>

15036
</dt> <dt>



O canal no índice especificado da consulta não pode ser aberto.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERRO \_ EVT \_ Editor \_ desabilitado**
</dt> <dd> <dl> <dt>

15037
</dt> <dt>



O provedor foi desabilitado e seus recursos não estão disponíveis. Isso pode ocorrer quando o provedor é desinstalado ou atualizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**\_ \_ filtro de erro EVT \_ fora \_ do \_ intervalo**
</dt> <dd> <dl> <dt>

15038
</dt> <dt>



Tentativa de criar um tipo numérico que está fora de seu intervalo válido.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



 

 





