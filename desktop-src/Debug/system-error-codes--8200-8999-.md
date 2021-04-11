---
description: Descreve os códigos de erro 8200-8999 definidos no arquivo de cabeçalho WinError. h e destina-se a desenvolvedores.
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: Códigos de erro do sistema (8200-8999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7500ae4c178999de8052b0858089604652dc5237
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164035"
---
# <a name="system-error-codes-8200-8999"></a>Códigos de erro do sistema (8200-8999)

> [!NOTE]
> Essas informações destinam-se a desenvolvedores Depurando erros do sistema. Para outros erros, como problemas com Windows Update, há uma lista de recursos na página códigos de [erro](system-error-codes.md) .

A lista a seguir descreve os [códigos de erro do sistema](system-error-codes.md) para erros 8200 a 8999. Elas são retornadas pela função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando muitas funções falham. Para recuperar o texto de descrição do erro em seu aplicativo, use a função [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) com a **mensagem de formato \_ \_ do sinalizador do \_ sistema** .

<dl> <dt>

<span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERRO \_ DS \_ não \_ instalado**
</dt> <dd> <dl> <dt>

8200 (0x2008)
</dt> <dt>



Ocorreu um erro ao instalar o serviço de diretório. Para obter mais informações, consulte o log de eventos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERRO \_ de \_ Associação DS \_ avaliada \_ localmente**
</dt> <dd> <dl> <dt>

8201 (0x2009)
</dt> <dt>



O serviço de diretório avaliou associações de grupo localmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERRO \_ DS \_ sem \_ atributo \_ ou \_ valor**
</dt> <dd> <dl> <dt>

8202 (0x200A)
</dt> <dt>



O atributo ou o valor do serviço de diretório especificado não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERRO \_ de \_ \_ sintaxe de atributo inválido DS \_**
</dt> <dd> <dl> <dt>

8203 (0x200B)
</dt> <dt>



A sintaxe de atributo especificada para o serviço de diretório é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERRO \_ de \_ tipo de atributo DS \_ \_ indefinido**
</dt> <dd> <dl> <dt>

8204 (0x200C)
</dt> <dt>



O tipo de atributo especificado para o serviço de diretório não está definido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**ERRO \_ o \_ atributo \_ ou o valor do DS \_ \_ existe**
</dt> <dd> <dl> <dt>

8205 (0x200D)
</dt> <dt>



O atributo ou o valor do serviço de diretório especificado já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERRO \_ DS \_ ocupado**
</dt> <dd> <dl> <dt>

8206 (0x200E)
</dt> <dt>



O serviço de diretório está ocupado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERRO \_ DS \_ não disponível**
</dt> <dd> <dl> <dt>

8207 (0x200F)
</dt> <dt>



O serviço de diretório não está disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERRO \_ DS \_ nenhum \_ RIDs \_ alocado**
</dt> <dd> <dl> <dt>

8208 (0x2010)
</dt> <dt>



O serviço de diretório não pôde alocar um identificador relativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERRO \_ DS \_ não \_ mais \_ RIDs**
</dt> <dd> <dl> <dt>

8209 (0x2011)
</dt> <dt>



O serviço de diretório esgotou o pool de identificadores relativos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERRO \_ \_ proprietário da \_ função incorreta do DS \_**
</dt> <dd> <dl> <dt>

8210 (0x2012)
</dt> <dt>



A operação solicitada não pôde ser executada porque o serviço de diretório não é o mestre para esse tipo de operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**ERRO \_ DS \_ RIDMGR \_ erro de inicialização \_**
</dt> <dd> <dl> <dt>

8211 (0x2013)
</dt> <dt>



O serviço de diretório não pôde inicializar o subsistema que aloca identificadores relativos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERRO \_ de \_ \_ violação de classe DS obj \_**
</dt> <dd> <dl> <dt>

8212 (0x2014)
</dt> <dt>



A operação solicitada não satisfez uma ou mais restrições associadas à classe do objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERRO \_ DS \_ \_ não consegue \_ em \_ folha**
</dt> <dd> <dl> <dt>

8213 (0x2015)
</dt> <dt>



O serviço de diretório pode executar a operação solicitada somente em um objeto folha.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERRO \_ DS não \_ consegue \_ no \_ RDN**
</dt> <dd> <dl> <dt>

8214 (0x2016)
</dt> <dt>



O serviço de diretório não pode executar a operação solicitada no atributo RDN de um objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERRO DS não é possível \_ \_ \_ \_ \_ classe obj**
</dt> <dd> <dl> <dt>

8215 (0x2017)
</dt> <dt>



O serviço de diretório detectou uma tentativa de modificar a classe de objeto de um objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**erro ao mover o erro \_ \_ entre \_ dom do \_ DS \_**
</dt> <dd> <dl> <dt>

8216 (0x2018)
</dt> <dt>



Não foi possível executar a operação de movimentação entre domínios solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERRO \_ DS \_ GC \_ não \_ disponível**
</dt> <dd> <dl> <dt>

8217 (0x2019)
</dt> <dt>



Não é possível contatar o servidor de catálogo global.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**ERRO \_ de \_ política compartilhada**
</dt> <dd> <dl> <dt>

8218 (0x201A)
</dt> <dt>



O objeto de política é compartilhado e só pode ser modificado na raiz.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**objeto de política de erro \_ \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

8219 (0x201B)
</dt> <dt>



O objeto de política não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**\_política \_ de erro somente \_ no \_ DS**
</dt> <dd> <dl> <dt>

8220 (0x201C)
</dt> <dt>



As informações de política solicitadas só estão no serviço de diretório.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**promoção de erros \_ \_ ativa**
</dt> <dd> <dl> <dt>

8221 (0x201D)
</dt> <dt>



Uma promoção do controlador de domínio está ativa no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERRO \_ sem \_ promoção \_ ativa**
</dt> <dd> <dl> <dt>

8222 (0x201E)
</dt> <dt>



Uma promoção do controlador de domínio não está ativa no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**erro \_ de \_ operações \_ DS**
</dt> <dd> <dl> <dt>

8224 (0x2020)
</dt> <dt>



Ocorreu um erro de operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**erro \_ de \_ erro de protocolo DS \_**
</dt> <dd> <dl> <dt>

8225 (0x2021)
</dt> <dt>



Erro de protocolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERRO \_ de \_ limite de DS \_ excedido**
</dt> <dd> <dl> <dt>

8226 (0x2022)
</dt> <dt>



O limite de tempo para esta solicitação foi excedido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERRO \_ \_ SIZELIMIT DS \_ excedido**
</dt> <dd> <dl> <dt>

8227 (0x2023)
</dt> <dt>



O limite de tamanho para esta solicitação foi excedido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**ERRO \_ de \_ limite de administrador DS \_ \_ excedido**
</dt> <dd> <dl> <dt>

8228 (0x2024)
</dt> <dt>



O limite administrativo para esta solicitação foi excedido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERRO \_ de \_ comparação de DS \_ falso**
</dt> <dd> <dl> <dt>

8229 (0x2025)
</dt> <dt>



A resposta de comparação foi falsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERRO \_ de \_ comparação de DS \_ verdadeiro**
</dt> <dd> <dl> <dt>

8230 (0x2026)
</dt> <dt>



A resposta de comparação foi verdadeira.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**ERRO \_ \_ \_ \_ não \_ há suporte para o método de autenticação DS**
</dt> <dd> <dl> <dt>

8231 (0x2027)
</dt> <dt>



O servidor não dá suporte ao método de autenticação solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERRO \_ de \_ autenticação forte de DS \_ \_ necessária**
</dt> <dd> <dl> <dt>

8232 (0x2028)
</dt> <dt>



Um método de autenticação mais seguro é necessário para este servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERRO \_ de \_ autenticação inadequada de DS \_**
</dt> <dd> <dl> <dt>

8233 (0x2029)
</dt> <dt>



Autenticação inadequada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERRO \_ de \_ autenticação DS \_ desconhecido**
</dt> <dd> <dl> <dt>

8234 (0x202A)
</dt> <dt>



O mecanismo de autenticação é desconhecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**ERRO \_ de \_ referência DS**
</dt> <dd> <dl> <dt>

8235 (0x202B)
</dt> <dt>



Uma referência foi retornada do servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERRO \_ de \_ extensão de crit não disponível DS \_ \_**
</dt> <dd> <dl> <dt>

8236 (0x202C)
</dt> <dt>



O servidor não oferece suporte à extensão crítica solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERRO \_ de \_ confidencialidade de DS \_ necessária**
</dt> <dd> <dl> <dt>

8237 (0x202D)
</dt> <dt>



Essa solicitação requer uma conexão segura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERRO \_ de \_ correspondência inadequada ao DS \_**
</dt> <dd> <dl> <dt>

8238 (0x202E)
</dt> <dt>



Correspondência inadequada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERRO \_ de \_ violação de restrição DS \_**
</dt> <dd> <dl> <dt>

8239 (0x202F)
</dt> <dt>



Ocorreu uma violação de restrição.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERRO \_ DS \_ não é \_ tal \_ objeto**
</dt> <dd> <dl> <dt>

8240 (0x2030)
</dt> <dt>



Esse objeto não existe no servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**ERRO \_ de \_ alias de DS \_**
</dt> <dd> <dl> <dt>

8241 (0x2031)
</dt> <dt>



Há um problema de alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERRO \_ de \_ \_ sintaxe DN inválida DS \_**
</dt> <dd> <dl> <dt>

8242 (0x2032)
</dt> <dt>



Uma sintaxe de DN inválida foi especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**ERRO \_ DS \_ é \_ folha**
</dt> <dd> <dl> <dt>

8243 (0x2033)
</dt> <dt>



O objeto é um objeto folha.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERRO \_ do \_ alias DS \_ DEREF \_ problema**
</dt> <dd> <dl> <dt>

8244 (0x2034)
</dt> <dt>



Há um problema de desreferenciamento de alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERRO \_ DS não \_ funcionado \_ para \_ executar**
</dt> <dd> <dl> <dt>

8245 (0x2035)
</dt> <dt>



O servidor não vai processar a solicitação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERRO \_ de \_ detecção de loop DS \_**
</dt> <dd> <dl> <dt>

8246 (0x2036)
</dt> <dt>



Um loop foi detectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERRO \_ de \_ violação de nomenclatura de DS \_**
</dt> <dd> <dl> <dt>

8247 (0x2037)
</dt> <dt>



Há uma violação de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERRO \_ de \_ objeto \_ DS \_ muito \_ grande**
</dt> <dd> <dl> <dt>

8248 (0x2038)
</dt> <dt>



O conjunto de resultados é muito grande.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**ERRO o \_ DS \_ afeta \_ vários \_ DSAs**
</dt> <dd> <dl> <dt>

8249 (0x2039)
</dt> <dt>



A operação afeta vários DSAs.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERRO \_ de \_ servidor DS \_ inoperante**
</dt> <dd> <dl> <dt>

8250 (0x203A)
</dt> <dt>



O servidor não está operacional.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**erro \_ de \_ local \_ DS**
</dt> <dd> <dl> <dt>

8251 (0x203B)
</dt> <dt>



Ocorreu um erro local.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**erro \_ de \_ codificação \_ DS**
</dt> <dd> <dl> <dt>

8252 (0x203C)
</dt> <dt>



Ocorreu um erro de codificação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**erro \_ ao \_ decodificar \_ DS**
</dt> <dd> <dl> <dt>

8253 (0x203D)
</dt> <dt>



Ocorreu um erro de decodificação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERRO \_ de \_ filtro DS \_ desconhecido**
</dt> <dd> <dl> <dt>

8254 (0x203E)
</dt> <dt>



Não é possível reconhecer o filtro de pesquisa.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**erro \_ de \_ erro de parâmetro DS \_**
</dt> <dd> <dl> <dt>

8255 (0x203F)
</dt> <dt>



Um ou mais parâmetros são ilegais.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERRO \_ DS \_ sem \_ suporte**
</dt> <dd> <dl> <dt>

8256 (0x2040)
</dt> <dt>



Não há suporte para o método especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERRO \_ DS \_ nenhum \_ resultado \_ retornado**
</dt> <dd> <dl> <dt>

8257 (0x2041)
</dt> <dt>



Nenhum resultado foi retornado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**ERRO \_ de \_ controle DS \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

8258 (0x2042)
</dt> <dt>



O servidor não dá suporte ao controle especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERRO \_ de \_ loop de cliente DS \_**
</dt> <dd> <dl> <dt>

8259 (0x2043)
</dt> <dt>



Um loop de referência foi detectado pelo cliente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**ERRO \_ \_ limite de referências DS \_ \_ excedido**
</dt> <dd> <dl> <dt>

8260 (0x2044)
</dt> <dt>



O limite de referência predefinido foi excedido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERRO \_ de \_ controle de classificação DS \_ \_ ausente**
</dt> <dd> <dl> <dt>

8261 (0x2045)
</dt> <dt>



A pesquisa requer um controle SORT.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**erro \_ \_ ao intervalo de deslocamento DS \_ \_**
</dt> <dd> <dl> <dt>

8262 (0x2046)
</dt> <dt>



Os resultados da pesquisa excedem o intervalo de deslocamento especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERRO \_ \_ RIDMGR DS \_ desabilitado**
</dt> <dd> <dl> <dt>

8263 (0x2047)
</dt> <dt>



O serviço de diretório detectou que o subsistema que aloca identificadores relativos está desabilitado. Isso pode ocorrer como um mecanismo de proteção quando o sistema determina que uma parte significativa de RIDs (identificadores relativos) foi esgotada. Consulte <https://go.microsoft.com/fwlink/p/?linkid=228610> para obter as etapas de diagnóstico recomendadas e o procedimento para reabilitar a criação da conta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**ERRO \_ a \_ raiz DS \_ deve \_ ser \_ NC**
</dt> <dd> <dl> <dt>

8301 (0x206D)
</dt> <dt>



O objeto raiz deve ser o cabeçalho de um contexto de nomenclatura. O objeto raiz não pode ter um pai instanciado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERRO \_ DS \_ Adicionar \_ réplica \_ inibido**
</dt> <dd> <dl> <dt>

8302 (0x206E)
</dt> <dt>



Não é possível executar a operação de adição de réplica. O contexto de nomenclatura deve ser gravável para criar a réplica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERRO \_ DS \_ ATT \_ não \_ Def \_ no \_ esquema**
</dt> <dd> <dl> <dt>

8303 (0x206F)
</dt> <dt>



Ocorreu uma referência a um atributo que não está definido no esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**ERRO \_ de \_ tamanho máximo de obj de DS \_ \_ \_ excedido**
</dt> <dd> <dl> <dt>

8304 (0x2070)
</dt> <dt>



O tamanho máximo de um objeto foi excedido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERRO \_ o \_ nome da cadeia de caracteres DS obj \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

8305 (0x2071)
</dt> <dt>



Foi feita uma tentativa de adicionar um objeto ao diretório com um nome que já está em uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERRO \_ DS \_ nenhum \_ RDN \_ definido \_ no \_ esquema**
</dt> <dd> <dl> <dt>

8306 (0x2072)
</dt> <dt>



Foi feita uma tentativa de adicionar um objeto de uma classe que não tem um RDN definido no esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERRO o \_ RDN de DS não \_ \_ \_ corresponde ao \_ esquema**
</dt> <dd> <dl> <dt>

8307 (0x2073)
</dt> <dt>



Foi feita uma tentativa de adicionar um objeto usando um RDN que não é o RDN definido no esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERRO \_ DS \_ nenhum \_ \_ atts solicitado \_ encontrado**
</dt> <dd> <dl> <dt>

8308 (0x2074)
</dt> <dt>



Nenhum dos atributos solicitados foi encontrado nos objetos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERRO \_ \_ \_ de buffer de usuário DS \_ para \_ pequeno**
</dt> <dd> <dl> <dt>

8309 (0x2075)
</dt> <dt>



O buffer do usuário é muito pequeno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERRO \_ DS \_ ATT \_ \_ não está \_ em \_ obj**
</dt> <dd> <dl> <dt>

8310 (0x2076)
</dt> <dt>



O atributo especificado na operação não está presente no objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERRO \_ DS \_ de \_ operação mod ilegal \_**
</dt> <dd> <dl> <dt>

8311 (0x2077)
</dt> <dt>



Operação de modificação inválida. Não é permitido algum aspecto da modificação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**ERRO \_ DS \_ obj \_ muito \_ grande**
</dt> <dd> <dl> <dt>

8312 (0x2078)
</dt> <dt>



O objeto especificado é muito grande.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERRO \_ \_ tipo de \_ instância inválido DS \_**
</dt> <dd> <dl> <dt>

8313 (0x2079)
</dt> <dt>



O tipo de instância especificado não é válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERRO \_ \_ MASTERDSA DS \_ necessário**
</dt> <dd> <dl> <dt>

8314 (0x207A)
</dt> <dt>



A operação deve ser executada em um DSA mestre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**ERRO \_ de \_ classe de objeto DS \_ \_ necessária**
</dt> <dd> <dl> <dt>

8315 (0x207B)
</dt> <dt>



O atributo de classe de objeto deve ser especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERRO \_ DS \_ ausente \_ na \_ ATT necessária**
</dt> <dd> <dl> <dt>

8316 (0x207C)
</dt> <dt>



Um atributo necessário está ausente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERRO \_ DS \_ ATT \_ não \_ Def \_ para \_ classe**
</dt> <dd> <dl> <dt>

8317 (0x207D)
</dt> <dt>



Foi feita uma tentativa de modificar um objeto para incluir um atributo que não é válido para sua classe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**ERRO o \_ DS \_ ATT \_ já \_ existe**
</dt> <dd> <dl> <dt>

8318 (0x207E)
</dt> <dt>



O atributo especificado já está presente no objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERRO \_ DS \_ não \_ consegue \_ Adicionar \_ valores de ATT**
</dt> <dd> <dl> <dt>

8320 (0x2080)
</dt> <dt>



O atributo especificado não está presente ou não tem nenhum valor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERRO \_ de \_ \_ restrição de valor único DS \_**
</dt> <dd> <dl> <dt>

8321 (0x2081)
</dt> <dt>



Vários valores foram especificados para um atributo que pode ter apenas um valor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**ERRO \_ de \_ restrição de intervalo DS \_**
</dt> <dd> <dl> <dt>

8322 (0x2082)
</dt> <dt>



Um valor para o atributo não estava no intervalo de valores aceitável.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**ERRO o \_ Val de ATT de DS \_ \_ \_ já \_ existe**
</dt> <dd> <dl> <dt>

8323 (0x2083)
</dt> <dt>



O valor especificado já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERRO \_ DS \_ \_ não consegue REM \_ faltando \_ ATT**
</dt> <dd> <dl> <dt>

8324 (0x2084)
</dt> <dt>



O atributo não pode ser removido porque não está presente no objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERRO \_ DS \_ \_ não consegue REM \_ falta de \_ ATT \_ Val**
</dt> <dd> <dl> <dt>

8325 (0x2085)
</dt> <dt>



O valor do atributo não pode ser removido porque ele não está presente no objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**o \_ erro \_ raiz \_ DS \_ não é \_ SUBREF**
</dt> <dd> <dl> <dt>

8326 (0x2086)
</dt> <dt>



O objeto raiz especificado não pode ser um subref.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERRO \_ DS \_ sem \_ encadeamento**
</dt> <dd> <dl> <dt>

8327 (0x2087)
</dt> <dt>



O encadeamento não é permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERRO \_ DS \_ sem \_ avaliação encadeada \_**
</dt> <dd> <dl> <dt>

8328 (0x2088)
</dt> <dt>



A avaliação encadeada não é permitida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERRO \_ DS \_ sem \_ \_ objeto pai**
</dt> <dd> <dl> <dt>

8329 (0x2089)
</dt> <dt>



A operação não pôde ser executada porque o pai do objeto está não instanciado ou foi excluído.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERRO \_ \_ o pai do DS \_ é \_ um \_ alias**
</dt> <dd> <dl> <dt>

8330 (0x208A)
</dt> <dt>



Não é permitido ter um pai que seja um alias. Os aliases são objetos folha.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERRO \_ DS não \_ consegue \_ misturar \_ mestre \_ e \_ representantes**
</dt> <dd> <dl> <dt>

8331 (0x208B)
</dt> <dt>



O objeto e o pai devem ser do mesmo tipo, tanto os mestres quanto as duas réplicas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERRO \_ os \_ filhos do DS \_ existem**
</dt> <dd> <dl> <dt>

8332 (0x208C)
</dt> <dt>



A operação não pode ser executada porque existem objetos filho. Esta operação só pode ser executada em um objeto folha.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERRO \_ \_ obj DS \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

8333 (0x208D)
</dt> <dt>



Objeto de diretório não encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**ERRO \_ \_ obj. alias \_ DS \_ ausente**
</dt> <dd> <dl> <dt>

8334 (0x208E)
</dt> <dt>



O objeto com alias está ausente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**ERRO \_ de \_ \_ sintaxe de nome insatisfatório DS \_**
</dt> <dd> <dl> <dt>

8335 (0x208F)
</dt> <dt>



O nome do objeto tem uma sintaxe inadequada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**ERRO \_ \_ \_ de pontos de alias DS \_ para \_ alias**
</dt> <dd> <dl> <dt>

8336 (0x2090)
</dt> <dt>



Não é permitido que um alias faça referência a outro alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERRO DS não é possível \_ \_ \_ DEREF \_ alias**
</dt> <dd> <dl> <dt>

8337 (0x2091)
</dt> <dt>



Não é possível desreferenciar o alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERRO \_ DS \_ fora \_ do \_ escopo**
</dt> <dd> <dl> <dt>

8338 (0x2092)
</dt> <dt>



A operação está fora do escopo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERRO \_ de \_ objeto DS \_ sendo \_ removido**
</dt> <dd> <dl> <dt>

8339 (0x2093)
</dt> <dt>



A operação não pode continuar porque o objeto está no processo de ser removido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERRO \_ DS não \_ consegue \_ excluir \_ DSA \_ obj**
</dt> <dd> <dl> <dt>

8340 (0x2094)
</dt> <dt>



O objeto DSA não pode ser excluído.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**erro \_ genérico erro de DS \_ \_**
</dt> <dd> <dl> <dt>

8341 (0x2095)
</dt> <dt>



Ocorreu um erro de serviço de diretório.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERRO \_ DSA de DS \_ \_ deve \_ ser um \_ \_ mestre int**
</dt> <dd> <dl> <dt>

8342 (0x2096)
</dt> <dt>



A operação só pode ser executada em um objeto DSA mestre interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERRO \_ de \_ classe DS \_ não \_ DSA**
</dt> <dd> <dl> <dt>

8343 (0x2097)
</dt> <dt>



O objeto deve ser da classe DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**ERRO \_ ao \_ DS \_ INSUFF \_ direitos de acesso**
</dt> <dd> <dl> <dt>

8344 (0x2098)
</dt> <dt>



Direitos de acesso insuficientes para executar a operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERRO \_ DS \_ inválido \_ superior**
</dt> <dd> <dl> <dt>

8345 (0x2099)
</dt> <dt>



O objeto não pode ser adicionado porque o pai não está na lista de superiores possíveis.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**ERRO \_ \_ de atributo DS \_ pertencente \_ a \_ Sam**
</dt> <dd> <dl> <dt>

8346 (0x209A)
</dt> <dt>



O acesso ao atributo não é permitido porque o atributo pertence ao SAM (Gerenciador de contas de segurança).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERRO o nome DS é um número \_ \_ excessivo de \_ \_ \_ partes**
</dt> <dd> <dl> <dt>

8347 (0x209B)
</dt> <dt>



O nome tem muitas partes.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERRO \_ de \_ nome DS \_ muito \_ longo**
</dt> <dd> <dl> <dt>

8348 (0x209C)
</dt> <dt>



O nome é muito longo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**ERRO \_ \_ nome DS \_ valor \_ muito \_ longo**
</dt> <dd> <dl> <dt>

8349 (0x209D)
</dt> <dt>



O valor do nome é muito longo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERRO \_ de \_ nome DS não \_ analisável**
</dt> <dd> <dl> <dt>

8350 (0x209E)
</dt> <dt>



O serviço de diretório encontrou um erro ao analisar um nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERRO \_ \_ tipo de nome DS \_ \_ desconhecido**
</dt> <dd> <dl> <dt>

8351 (0x209F)
</dt> <dt>



O serviço de diretório não pode obter o tipo de atributo para um nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERRO \_ DS \_ não é \_ um \_ objeto**
</dt> <dd> <dl> <dt>

8352 (0x20A0)
</dt> <dt>



O nome não identifica um objeto; o nome identifica um fantasma.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERRO \_ DS \_ s \_ desc \_ muito \_ curto**
</dt> <dd> <dl> <dt>

8353 (0x20A1)
</dt> <dt>



O descritor de segurança é muito curto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERRO \_ DS \_ SEC \_ desc \_ inválido**
</dt> <dd> <dl> <dt>

8354 (0x20A2)
</dt> <dt>



O descritor de segurança é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERRO \_ DS \_ sem \_ \_ nome excluído**
</dt> <dd> <dl> <dt>

8355 (0x20A3)
</dt> <dt>



Falha ao criar o nome para o objeto excluído.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**ERRO \_ \_ SUBREF DS \_ deve \_ ter \_ pai**
</dt> <dd> <dl> <dt>

8356 (0x20A4)
</dt> <dt>



O pai de um novo subref deve existir.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERRO \_ o \_ NCName do DS \_ deve \_ ser \_ NC**
</dt> <dd> <dl> <dt>

8357 (0x20A5)
</dt> <dt>



O objeto deve ser um contexto de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERRO \_ DS \_ não \_ consegue \_ Adicionar \_ somente sistema**
</dt> <dd> <dl> <dt>

8358 (0x20A6)
</dt> <dt>



Não é permitido adicionar um atributo que pertence ao sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**a \_ classe DS de erro \_ \_ deve \_ ser \_ concreta**
</dt> <dd> <dl> <dt>

8359 (0x20A7)
</dt> <dt>



A classe do objeto deve ser estrutural; Não é possível criar uma instância de uma classe abstrata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERRO \_ DS \_ \_ DMD inválido**
</dt> <dd> <dl> <dt>

8360 (0x20A8)
</dt> <dt>



O objeto de esquema não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**ERRO \_ o \_ GUID do obj DS \_ \_ existe**
</dt> <dd> <dl> <dt>

8361 (0x20A9)
</dt> <dt>



Já existe um objeto local com este GUID (Dead ou vivo).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERRO \_ DS \_ não \_ em \_ BACKLINK**
</dt> <dd> <dl> <dt>

8362 (0x20AA)
</dt> <dt>



A operação não pode ser executada em um vínculo regressivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERRO \_ DS \_ sem \_ CROSSREF \_ para \_ NC**
</dt> <dd> <dl> <dt>

8363 (0x20AB)
</dt> <dt>



Não foi possível encontrar a referência cruzada para o contexto de nomenclatura especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERRO \_ ao \_ desligar \_ DS**
</dt> <dd> <dl> <dt>

8364 (0x20AC)
</dt> <dt>



A operação não pôde ser executada porque o serviço de diretório está sendo desligado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERRO \_ de \_ operação desconhecida de DS \_**
</dt> <dd> <dl> <dt>

8365 (0x20AD)
</dt> <dt>



A solicitação de serviço de diretório é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERRO \_ \_ proprietário da \_ função \_ inválido DS**
</dt> <dd> <dl> <dt>

8366 (0x20AE)
</dt> <dt>



Não foi possível ler o atributo proprietário da função.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERRO \_ DS \_ não foi possível \_ contatar \_ FSMO**
</dt> <dd> <dl> <dt>

8367 (0x20AF)
</dt> <dt>



Falha na operação FSMO solicitada. O atual titular do FSMO não pôde ser contatado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERRO \_ DS \_ Cross \_ NC \_ DN \_ renomear**
</dt> <dd> <dl> <dt>

8368 (0x20B0)
</dt> <dt>



Não é permitido modificar um DN em um contexto de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERRO \_ DS \_ \_ somente no \_ sistema \_ mod**
</dt> <dd> <dl> <dt>

8369 (0x20B1)
</dt> <dt>



O atributo não pode ser modificado porque pertence ao sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERRO \_ \_ somente replicador \_ DS**
</dt> <dd> <dl> <dt>

8370 (0x20B2)
</dt> <dt>



Somente o replicador pode executar essa função.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERRO \_ de \_ classe de obj DS \_ \_ não \_ definida**
</dt> <dd> <dl> <dt>

8371 (0x20B3)
</dt> <dt>



A classe especificada não está definida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERRO \_ de \_ classe DS obj \_ \_ não \_ subclasse**
</dt> <dd> <dl> <dt>

8372 (0x20B4)
</dt> <dt>



A classe especificada não é uma subclasse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERRO \_ de \_ referência de nome DS \_ \_ inválido**
</dt> <dd> <dl> <dt>

8373 (0x20B5)
</dt> <dt>



A referência de nome é inválida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERRO \_ de \_ referência cruzada de DS \_ \_**
</dt> <dd> <dl> <dt>

8374 (0x20B6)
</dt> <dt>



Já existe uma referência cruzada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERRO DS não é possível \_ \_ excluir o \_ \_ \_ CROSSREF mestre**
</dt> <dd> <dl> <dt>

8375 (0x20B7)
</dt> <dt>



Não é permitido excluir uma referência cruzada mestre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERRO \_ na \_ subárvore DS de \_ notificação \_ não \_ NC \_ cabeçalho**
</dt> <dd> <dl> <dt>

8376 (0x20B8)
</dt> <dt>



As notificações de subárvore só têm suporte em cabeçalhos NC.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERRO \_ do \_ filtro de notificação DS \_ \_ muito \_ complexo**
</dt> <dd> <dl> <dt>

8377 (0x20B9)
</dt> <dt>



O filtro de notificação é muito complexo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERRO \_ \_ RDN de Dup de DS \_**
</dt> <dd> <dl> <dt>

8378 (0x20BA)
</dt> <dt>



Falha na atualização do esquema: RDN duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERRO \_ \_ OID de Dup de DS \_**
</dt> <dd> <dl> <dt>

8379 (0x20BB)
</dt> <dt>



Falha na atualização do esquema: OID duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**ERRO \_ de \_ \_ ID MAPI do Dup de DS \_**
</dt> <dd> <dl> <dt>

8380 (0x20BC)
</dt> <dt>



Falha na atualização do esquema: identificador MAPI duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERRO \_ \_ GUID de \_ ID de esquema do DUP \_ DS \_**
</dt> <dd> <dl> <dt>

8381 (0x20BD)
</dt> <dt>



Falha na atualização do esquema: GUID de ID de esquema duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERRO \_ \_ nome de \_ exibição LDAP de DUP \_ de DS \_**
</dt> <dd> <dl> <dt>

8382 (0x20BE)
</dt> <dt>



Falha na atualização do esquema: nome de exibição LDAP duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERRO \_ de \_ teste semântico de \_ ATT de DS \_**
</dt> <dd> <dl> <dt>

8383 (0x20BF)
</dt> <dt>



Falha na atualização do esquema: intervalo inferior menor que intervalo superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERRO \_ de \_ incompatibilidade de sintaxe DS \_**
</dt> <dd> <dl> <dt>

8384 (0x20C0)
</dt> <dt>



Falha na atualização do esquema: incompatibilidade de sintaxe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**o erro \_ DS \_ existe \_ em \_ deve \_ ter**
</dt> <dd> <dl> <dt>

8385 (0x20C1)
</dt> <dt>



Falha na exclusão do esquema: o atributo é usado em deve-conter.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**o erro \_ DS \_ existe \_ em \_ pode \_ ter**
</dt> <dd> <dl> <dt>

8386 (0x20C2)
</dt> <dt>



Falha na exclusão do esquema: o atributo é usado em maio-conter.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**ERRO o \_ DS não \_ existente \_ pode \_ ter**
</dt> <dd> <dl> <dt>

8387 (0x20C3)
</dt> <dt>



Falha na atualização do esquema: o atributo em pode-conter não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**o erro \_ DS não \_ existente \_ deve \_ ter**
</dt> <dd> <dl> <dt>

8388 (0x20C4)
</dt> <dt>



Falha na atualização do esquema: o atributo em deve-conter não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERRO \_ \_ falha no \_ teste de CLS auxiliar \_ DS \_**
</dt> <dd> <dl> <dt>

8389 (0x20C5)
</dt> <dt>



Falha na atualização do esquema: a classe na lista de classes auxiliares não existe ou não é uma classe auxiliar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERRO \_ DS não \_ existente \_ poss \_ sup**
</dt> <dd> <dl> <dt>

8390 (0x20C6)
</dt> <dt>



Falha na atualização do esquema: a classe em poss-superiors não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERRO \_ \_ falha no \_ teste de subcls do \_ DS \_**
</dt> <dd> <dl> <dt>

8391 (0x20C7)
</dt> <dt>



Falha na atualização do esquema: a classe na lista listas SubClassOf não existe ou não satisfaz as regras de hierarquia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERRO \_ DS \_ insatisfatório \_ \_ \_ ID de \_ sintaxe do RDN**
</dt> <dd> <dl> <dt>

8392 (0x20C8)
</dt> <dt>



Falha na atualização do esquema: RDN-ATT-ID tem sintaxe incorreta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**ERRO \_ o \_ DS \_ existe \_ no \_ CLS auxiliar**
</dt> <dd> <dl> <dt>

8393 (0x20C9)
</dt> <dt>



Falha na exclusão do esquema: a classe é usada como classe auxiliar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**ERRO \_ DS \_ existe \_ em \_ sub \_ CLS**
</dt> <dd> <dl> <dt>

8394 (0x20CA)
</dt> <dt>



Falha na exclusão do esquema: a classe é usada como subclasse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**ERRO o \_ DS \_ existe \_ no \_ poss \_ sup**
</dt> <dd> <dl> <dt>

8395 (0x20CB)
</dt> <dt>



Falha na exclusão do esquema: a classe é usada como poss superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERRO \_ \_ RECALCSCHEMA DS \_ falhou**
</dt> <dd> <dl> <dt>

8396 (0x20CC)
</dt> <dt>



Falha na atualização do esquema ao recalcular o cache de validação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERRO \_ ao \_ excluir árvore de DS \_ \_ não \_ concluído**
</dt> <dd> <dl> <dt>

8397 (0x20CD)
</dt> <dt>



A exclusão de árvore não foi concluída. A solicitação deve ser feita novamente para continuar a excluir a árvore.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERRO o \_ DS não \_ consegue \_ excluir**
</dt> <dd> <dl> <dt>

8398 (0x20CE)
</dt> <dt>



Não foi possível executar a operação de exclusão solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**ERRO \_ ID de req. de \_ esquema DS ATT \_ \_ \_**
</dt> <dd> <dl> <dt>

8399 (0x20CF)
</dt> <dt>



Não é possível ler o identificador de classe de controle para o registro de esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERRO \_ de \_ \_ sintaxe de \_ esquema \_ ATT Bad insatisfatório**
</dt> <dd> <dl> <dt>

8400 (0x20D0)
</dt> <dt>



O esquema de atributo tem uma sintaxe inadequada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERRO \_ DS não \_ consegue \_ cache \_ ATT**
</dt> <dd> <dl> <dt>

8401 (0x20D1)
</dt> <dt>



Não foi possível armazenar o atributo em cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERRO \_ DS não \_ consegue \_ armazenar \_ classe**
</dt> <dd> <dl> <dt>

8402 (0x20D2)
</dt> <dt>



Não foi possível armazenar a classe em cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERRO \_ DS não \_ consegue \_ remover o \_ cache de ATT \_**
</dt> <dd> <dl> <dt>

8403 (0x20D3)
</dt> <dt>



Não foi possível remover o atributo do cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERRO \_ DS \_ não \_ consegue \_ Remover \_ cache de classe**
</dt> <dd> <dl> <dt>

8404 (0x20D4)
</dt> <dt>



A classe não pôde ser removida do cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERRO \_ DS não \_ consegue \_ recuperar \_ DN**
</dt> <dd> <dl> <dt>

8405 (0x20D5)
</dt> <dt>



Não foi possível ler o atributo de nome distinto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERRO \_ DS \_ ausente \_ SUPREF**
</dt> <dd> <dl> <dt>

8406 (0x20D6)
</dt> <dt>



Nenhuma referência superior foi configurada para o serviço de diretório. Portanto, o serviço de diretório não pode emitir referências a objetos fora desta floresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERRO \_ DS não \_ consegue \_ recuperar \_ instância**
</dt> <dd> <dl> <dt>

8407 (0x20D7)
</dt> <dt>



Não foi possível recuperar o atributo de tipo de instância.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERRO \_ de \_ inconsistência de código DS \_**
</dt> <dd> <dl> <dt>

8408 (0x20D8)
</dt> <dt>



Ocorreu um erro interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**erro \_ de \_ banco de dados DS \_**
</dt> <dd> <dl> <dt>

8409 (0x20D9)
</dt> <dt>



Ocorreu um erro de banco de dados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERRO \_ DS \_ GOVERNSID \_ ausente**
</dt> <dd> <dl> <dt>

8410 (0x20DA)
</dt> <dt>



O atributo GOVERNSID está ausente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERRO \_ DS \_ faltando \_ \_ ATT esperado**
</dt> <dd> <dl> <dt>

8411 (0x20DB)
</dt> <dt>



Um atributo esperado está ausente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERRO \_ de \_ NCName de DS ausente na \_ \_ referência de Cr \_**
</dt> <dd> <dl> <dt>

8412 (0x20DC)
</dt> <dt>



O contexto de nomenclatura especificado não tem uma referência cruzada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**erro \_ \_ ao verificar a segurança do DS \_ \_**
</dt> <dd> <dl> <dt>

8413 (0x20DD)
</dt> <dt>



Ocorreu um erro de verificação de segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERRO \_ de \_ esquema DS \_ não \_ carregado**
</dt> <dd> <dl> <dt>

8414 (0x20DE)
</dt> <dt>



O esquema não está carregado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERRO \_ \_ \_ falha na alocação de esquema DS \_**
</dt> <dd> <dl> <dt>

8415 (0x20DF)
</dt> <dt>



Falha na alocação de esquema. Verifique se o computador está com pouca memória.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERRO \_ de \_ \_ sintaxe de req de esquema DS ATT \_ \_**
</dt> <dd> <dl> <dt>

8416 (0x20E0)
</dt> <dt>



Falha ao obter a sintaxe necessária para o esquema de atributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**erro erro de \_ \_ GCVERIFY DS \_**
</dt> <dd> <dl> <dt>

8417 (0x20E1)
</dt> <dt>



Falha na verificação do catálogo global. O catálogo global não está disponível ou não oferece suporte à operação. Parte do diretório não está disponível no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de esquema Dra DS \_**
</dt> <dd> <dl> <dt>

8418 (0x20E2)
</dt> <dt>



A operação de replicação falhou devido a uma incompatibilidade de esquema entre os servidores envolvidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERRO \_ DS não \_ consegue \_ encontrar \_ DSA \_ obj**
</dt> <dd> <dl> <dt>

8419 (0x20E3)
</dt> <dt>



Não foi possível encontrar o objeto DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERRO \_ DS não \_ consegue \_ localizar o \_ \_ NC esperado**
</dt> <dd> <dl> <dt>

8420 (0x20E4)
</dt> <dt>



Não foi possível encontrar o contexto de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERRO \_ DS não \_ consegue \_ localizar \_ NC \_ no \_ cache**
</dt> <dd> <dl> <dt>

8421 (0x20E5)
</dt> <dt>



Não foi possível encontrar o contexto de nomenclatura no cache.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERRO \_ DS não \_ consegue \_ recuperar \_ filho**
</dt> <dd> <dl> <dt>

8422 (0x20E6)
</dt> <dt>



Não foi possível recuperar o objeto filho.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERRO \_ de \_ \_ modificação ilegal de segurança DS \_**
</dt> <dd> <dl> <dt>

8423 (0x20E7)
</dt> <dt>



A modificação não foi permitida por motivos de segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERRO \_ DS não \_ consegue \_ substituir o \_ \_ REC oculto**
</dt> <dd> <dl> <dt>

8424 (0x20E8)
</dt> <dt>



A operação não pode substituir o registro oculto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERRO \_ de \_ \_ arquivo de hierarquia insatisfatório DS \_**
</dt> <dd> <dl> <dt>

8425 (0x20E9)
</dt> <dt>



O arquivo de hierarquia é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERRO \_ \_ \_ \_ falha na tabela de hierarquia de compilação DS \_**
</dt> <dd> <dl> <dt>

8426 (0x20EA)
</dt> <dt>



Falha na tentativa de criar a tabela de hierarquia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERRO \_ \_ parâmetro DS \_ config \_ ausente**
</dt> <dd> <dl> <dt>

8427 (0x20EB)
</dt> <dt>



O parâmetro de configuração de diretório está ausente no registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERRO de \_ contagem de DS de \_ \_ \_ índices AB \_ com falha**
</dt> <dd> <dl> <dt>

8428 (0x20EC)
</dt> <dt>



Falha na tentativa de contagem dos índices do catálogo de endereços.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERRO \_ \_ \_ \_ falha ao alocar tabela de hierarquia DS \_**
</dt> <dd> <dl> <dt>

8429 (0x20ED)
</dt> <dt>



Falha na alocação da tabela de hierarquia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERRO \_ interno de DS \_ \_**
</dt> <dd> <dl> <dt>

8430 (0x20EE)
</dt> <dt>



O serviço de diretório encontrou uma falha interna.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**erro \_ desconhecido ao DS \_ \_**
</dt> <dd> <dl> <dt>

8431 (0x20EF)
</dt> <dt>



O serviço de diretório encontrou uma falha desconhecida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**ERRO \_ a \_ raiz DS \_ requer a \_ classe \_ Top**
</dt> <dd> <dl> <dt>

8432 (0x20F0)
</dt> <dt>



Um objeto raiz requer uma classe de ' top '.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERRO \_ ao \_ recusar as \_ \_ funções FSMO do DS**
</dt> <dd> <dl> <dt>

8433 (0x20F1)
</dt> <dt>



Este servidor de diretório está sendo desligado e não é possível apropriar-se de novas funções de operação de mestre único flutuante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERRO \_ DS \_ ausente \_ \_ configurações FSMO**
</dt> <dd> <dl> <dt>

8434 (0x20F2)
</dt> <dt>



O serviço de diretório não tem informações de configuração obrigatórias e não é possível determinar a propriedade de funções de operação de mestre único flutuante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERRO \_ DS \_ incapaz \_ de despartir de \_ \_ funções**
</dt> <dd> <dl> <dt>

8435 (0x20F3)
</dt> <dt>



O serviço de diretório não pôde transferir a propriedade de uma ou mais funções de operação de mestre único flutuantes para outros servidores.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERRO \_ de \_ Dra \_ genérico de DS**
</dt> <dd> <dl> <dt>

8436 (0x20F4)
</dt> <dt>



Falha na operação de replicação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERRO \_ de \_ \_ parâmetro inválido de Dra DS \_**
</dt> <dd> <dl> <dt>

8437 (0x20F5)
</dt> <dt>



Um parâmetro inválido foi especificado para esta operação de replicação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERRO \_ DS \_ Dra \_ ocupado**
</dt> <dd> <dl> <dt>

8438 (0x20F6)
</dt> <dt>



O serviço de diretório está muito ocupado para concluir a operação de replicação no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERRO \_ \_ DN DS Dra \_ insatisfatório \_**
</dt> <dd> <dl> <dt>

8439 (0x20F7)
</dt> <dt>



O nome distinto especificado para esta operação de replicação é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERRO \_ \_ NC DS Dra \_ insatisfatório \_**
</dt> <dd> <dl> <dt>

8440 (0x20F8)
</dt> <dt>



O contexto de nomenclatura especificado para esta operação de replicação é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERRO \_ o \_ DN DS Dra \_ \_ existe**
</dt> <dd> <dl> <dt>

8441 (0x20F9)
</dt> <dt>



O nome distinto especificado para esta operação de replicação já existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**erro \_ \_ interno de Dra DS \_ \_**
</dt> <dd> <dl> <dt>

8442 (0x20FA)
</dt> <dt>



O sistema de replicação encontrou um erro interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERRO \_ de \_ dit de Dra \_ inconsistente DS \_**
</dt> <dd> <dl> <dt>

8443 (0x20FB)
</dt> <dt>



A operação de replicação encontrou uma inconsistência de banco de dados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERRO \_ \_ \_ falha na conexão Dra DS \_**
</dt> <dd> <dl> <dt>

8444 (0x20FC)
</dt> <dt>



O servidor especificado para esta operação de replicação não pôde ser contatado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERRO \_ de \_ \_ tipo de \_ instância inválido DS Dra \_**
</dt> <dd> <dl> <dt>

8445 (0x20FD)
</dt> <dt>



A operação de replicação encontrou um objeto com um tipo de instância inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERRO \_ DS \_ Dra \_ fora \_ do \_ mem**
</dt> <dd> <dl> <dt>

8446 (0x20FE)
</dt> <dt>



Falha na operação de replicação ao alocar memória.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERRO \_ de \_ email Dra DS \_ \_**
</dt> <dd> <dl> <dt>

8447 (0x20FF)
</dt> <dt>



A operação de replicação encontrou um erro com o sistema de email.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**ERRO o \_ DS \_ Dra \_ ref \_ já \_ existe**
</dt> <dd> <dl> <dt>

8448 (0x2100)
</dt> <dt>



As informações de referência de replicação para o servidor de destino já existem.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERRO \_ de \_ ref Dra DS \_ \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

8449 (0x2101)
</dt> <dt>



As informações de referência de replicação para o servidor de destino não existem.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERRO \_ DS \_ Dra \_ obj \_ is \_ origem do representante \_**
</dt> <dd> <dl> <dt>

8450 (0x2102)
</dt> <dt>



Não é possível remover o contexto de nomenclatura porque ele é replicado em outro servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**erro \_ erro de banco de domínio DS \_ Dra \_ \_**
</dt> <dd> <dl> <dt>

8451 (0x2103)
</dt> <dt>



A operação de replicação encontrou um erro de banco de dados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERRO \_ DS \_ Dra \_ sem \_ réplica**
</dt> <dd> <dl> <dt>

8452 (0x2104)
</dt> <dt>



O contexto de nomenclatura está no processo de ser removido ou não é replicado do servidor especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERRO \_ \_ acesso ao Dra DS \_ \_ negado**
</dt> <dd> <dl> <dt>

8453 (0x2105)
</dt> <dt>



O acesso à replicação foi negado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERRO \_ DS \_ Dra \_ não \_ suportado**
</dt> <dd> <dl> <dt>

8454 (0x2106)
</dt> <dt>



Esta versão do serviço de diretório não dá suporte para a operação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERRO \_ \_ RPC de Dra DS \_ \_ cancelado**
</dt> <dd> <dl> <dt>

8455 (0x2107)
</dt> <dt>



A chamada de procedimento remoto de replicação foi cancelada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERRO \_ \_ origem de Dra DS \_ \_ desabilitada**
</dt> <dd> <dl> <dt>

8456 (0x2108)
</dt> <dt>



O servidor de origem está rejeitando solicitações de replicação no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERRO \_ de \_ coletor de Dra DS \_ \_ desabilitado**
</dt> <dd> <dl> <dt>

8457 (0x2109)
</dt> <dt>



O servidor de destino está rejeitando solicitações de replicação no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERRO \_ de \_ \_ colisão de nome Dra DS \_**
</dt> <dd> <dl> <dt>

8458 (0x210A)
</dt> <dt>



Falha na operação de replicação devido a uma colisão de nomes de objetos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERRO \_ de \_ origem de Dra DS \_ \_ reinstalado**
</dt> <dd> <dl> <dt>

8459 (0x210B)
</dt> <dt>



A origem da replicação foi reinstalada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERRO \_ DS \_ Dra \_ ausente \_ pai**
</dt> <dd> <dl> <dt>

8460 (0x210C)
</dt> <dt>



Falha na operação de replicação porque um objeto pai necessário está ausente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERRO \_ de \_ Dra DS \_ preempção**
</dt> <dd> <dl> <dt>

8461 (0x210D)
</dt> <dt>



A operação de replicação foi antecipada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERRO \_ DS \_ Dra \_ ABANDON \_ Sync**
</dt> <dd> <dl> <dt>

8462 (0x210E)
</dt> <dt>



A tentativa de sincronização de replicação foi abandonada devido à falta de atualizações.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERRO \_ de \_ \_ desligamento de Dra DS**
</dt> <dd> <dl> <dt>

8463 (0x210F)
</dt> <dt>



A operação de replicação foi encerrada porque o sistema está sendo desligado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERRO \_ de \_ \_ \_ conjunto parcial incompatível de Dra DS \_**
</dt> <dd> <dl> <dt>

8464 (0x2110)
</dt> <dt>



Falha na tentativa de sincronização porque o DC de destino está aguardando a sincronização de novos atributos parciais da origem no momento. Essa condição será normal se uma alteração de esquema recente tiver modificado o conjunto de atributos parciais. O conjunto de atributos parciais de destino não é um subconjunto do conjunto de atributos parciais de origem.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERRO \_ a \_ origem do Dra DS \_ é uma \_ \_ \_ réplica parcial**
</dt> <dd> <dl> <dt>

8465 (0x2111)
</dt> <dt>



Falha na tentativa de sincronização de replicação porque uma réplica mestre tentou sincronizar a partir de uma réplica parcial.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERRO \_ \_ \_ \_ falha na conexão de EXTN Dra DS \_**
</dt> <dd> <dl> <dt>

8466 (0x2112)
</dt> <dt>



O servidor especificado para esta operação de replicação foi contatado, mas esse servidor não pôde contatar um servidor adicional necessário para concluir a operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de esquema de instalação DS \_**
</dt> <dd> <dl> <dt>

8467 (0x2113)
</dt> <dt>



A versão do esquema de serviço de diretório da floresta de origem não é compatível com a versão do serviço de diretório neste computador.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**ERRO \_ \_ ID de \_ link de DUP DS \_**
</dt> <dd> <dl> <dt>

8468 (0x2114)
</dt> <dt>



Falha na atualização do esquema: já existe um atributo com o mesmo identificador de link.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERRO \_ ao \_ \_ resolver erro de nome DS \_**
</dt> <dd> <dl> <dt>

8469 (0x2115)
</dt> <dt>



Conversão de nomes: erro de processamento genérico.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**erro \_ de \_ nome \_ DS \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

8470 (0x2116)
</dt> <dt>



Conversão de nomes: não foi possível encontrar o nome ou o direito insuficiente para ver o nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**ERRO \_ \_ nome DS \_ erro \_ não \_ exclusivo**
</dt> <dd> <dl> <dt>

8471 (0x2117)
</dt> <dt>



Conversão de nomes: nome de entrada mapeado para mais de um nome de saída.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**erro \_ \_ nome DS \_ erro \_ sem \_ mapeamento**
</dt> <dd> <dl> <dt>

8472 (0x2118)
</dt> <dt>



Conversão de nomes: nome de entrada encontrado, mas não o formato de saída associado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERRO \_ \_ nome DS \_ \_ somente domínio \_**
</dt> <dd> <dl> <dt>

8473 (0x2119)
</dt> <dt>



Conversão de nomes: não é possível resolver completamente, somente o domínio foi encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**erro \_ de \_ nome DS \_ erro \_ sem \_ \_ mapeamento sintático**
</dt> <dd> <dl> <dt>

8474 (0x211A)
</dt> <dt>



Conversão de nomes: não é possível executar um mapeamento puramente sintático no cliente sem sair da conexão.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERRO \_ DS \_ construído \_ ATT \_ mod**
</dt> <dd> <dl> <dt>

8475 (0x211B)
</dt> <dt>



A modificação de um atributo construído não é permitida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERRO \_ DS \_ de \_ classe do OM incorreto \_ \_**
</dt> <dd> <dl> <dt>

8476 (0x211C)
</dt> <dt>



A classe de objeto OM especificada está incorreta para um atributo com a sintaxe especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERRO \_ de \_ replicação de Dra DS \_ \_ pendente**
</dt> <dd> <dl> <dt>

8477 (0x211D)
</dt> <dt>



A solicitação de replicação foi postada; aguardando resposta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERRO DS DS \_ \_ \_ necessário**
</dt> <dd> <dl> <dt>

8478 (0x211E)
</dt> <dt>



A operação solicitada requer um serviço de diretório e nenhuma estava disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERRO \_ \_ nome de \_ \_ exibição LDAP \_ inválido do DS**
</dt> <dd> <dl> <dt>

8479 (0x211F)
</dt> <dt>



O nome de exibição LDAP da classe ou do atributo contém caracteres não ASCII.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERRO \_ de \_ \_ pesquisa não \_ básica de DS**
</dt> <dd> <dl> <dt>

8480 (0x2120)
</dt> <dt>



A operação de pesquisa solicitada só tem suporte para pesquisas base.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERRO \_ DS não \_ consegue \_ recuperar \_ atts**
</dt> <dd> <dl> <dt>

8481 (0x2121)
</dt> <dt>



A pesquisa não pôde recuperar os atributos do banco de dados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERRO \_ DS \_ BACKLINK \_ sem \_ link**
</dt> <dd> <dl> <dt>

8482 (0x2122)
</dt> <dt>



A operação de atualização de esquema tentou adicionar um atributo de vínculo regressivo que não tem nenhum link de encaminhamento correspondente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERRO \_ de \_ incompatibilidade de época DS \_**
</dt> <dd> <dl> <dt>

8483 (0x2123)
</dt> <dt>



A origem e o destino de uma movimentação entre domínios não aceitam o número de época do objeto. A origem ou o destino não tem a versão mais recente do objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de nome src DS \_**
</dt> <dd> <dl> <dt>

8484 (0x2124)
</dt> <dt>



A origem e o destino de uma movimentação entre domínios não aceitam o nome atual do objeto. A origem ou o destino não tem a versão mais recente do objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERRO \_ DS \_ src \_ e \_ DST \_ NC \_ idênticos**
</dt> <dd> <dl> <dt>

8485 (0x2125)
</dt> <dt>



A origem e o destino da operação de movimentação entre domínios são idênticos. O chamador deve usar a operação de movimentação local em vez da operação de movimentação entre domínios.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de NC de DST de DS \_**
</dt> <dd> <dl> <dt>

8486 (0x2126)
</dt> <dt>



A origem e o destino de uma movimentação entre domínios não estão em acordo com os contextos de nomenclatura na floresta. A origem ou o destino não tem a versão mais recente do contêiner de partições.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERRO \_ DS \_ não \_ AUTHORITIVE \_ para o \_ DST \_ NC**
</dt> <dd> <dl> <dt>

8487 (0x2127)
</dt> <dt>



O destino de uma movimentação entre domínios não é autoritativo para o contexto de nomenclatura de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERRO \_ de \_ \_ incompatibilidade de GUID src DS \_**
</dt> <dd> <dl> <dt>

8488 (0x2128)
</dt> <dt>



A origem e o destino de uma movimentação entre domínios não aceitam a identidade do objeto de origem. A origem ou o destino não tem a versão mais recente do objeto de origem.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERRO \_ DS \_ impossível \_ mover \_ \_ objeto excluído**
</dt> <dd> <dl> <dt>

8489 (0x2129)
</dt> <dt>



O objeto que está sendo movido entre domínios já é conhecido como excluído pelo servidor de destino. O servidor de origem não tem a versão mais recente do objeto de origem.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERRO \_ \_ \_ \_ na operação de PDC do DS em \_ andamento**
</dt> <dd> <dl> <dt>

8490 (0x212A)
</dt> <dt>



Outra operação que requer acesso exclusivo ao PDC FSMO já está em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERRO \_ \_ REQD de \_ limpeza entre domínios \_ \_ DS**
</dt> <dd> <dl> <dt>

8491 (0x212B)
</dt> <dt>



Uma operação de movimentação entre domínios falhou, de modo que duas versões do objeto movido existam-uma a cada nos domínios de origem e de destino. O objeto de destino precisa ser removido para restaurar o sistema para um estado consistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERRO \_ DS \_ inválido \_ ao \_ mover \_ operação de XDOM**
</dt> <dd> <dl> <dt>

8492 (0x212C)
</dt> <dt>



Esse objeto não pode ser movido entre limites de domínio porque as movimentações entre domínios dessa classe não são permitidas ou o objeto tem algumas características especiais, por exemplo: conta de confiança ou RID restrito, o que impede sua movimentação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERRO \_ DS não \_ consegue \_ com o \_ \_ grupo acct \_ MEMBERSHPS**
</dt> <dd> <dl> <dt>

8493 (0x212D)
</dt> <dt>



Não é possível mover objetos com associações entre limites de domínio assim que forem movidos, isso violaria as condições de associação do grupo de contas. Remova o objeto de qualquer associação de grupo de conta e tente novamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**ERRO \_ o \_ NC DS \_ deve \_ ter o \_ NC \_ pai**
</dt> <dd> <dl> <dt>

8494 (0x212E)
</dt> <dt>



Uma cabeça de contexto de nomenclatura deve ser o filho imediato de outro cabeçalho de contexto de nomenclatura, não de um nó interior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERRO \_ \_ de DS CR \_ impossível \_ de \_ validar**
</dt> <dd> <dl> <dt>

8495 (0x212F)
</dt> <dt>



O diretório não pode validar o nome de contexto de nomenclatura proposto porque não contém uma réplica do contexto de nomenclatura acima do contexto de nomenclatura proposto. Verifique se a função mestre de nomeação de domínio é mantida por um servidor configurado como um servidor de catálogo global e se o servidor está atualizado com seus parceiros de replicação. (Aplica-se somente aos mestres de nomenclatura de domínio do Windows 2000.)


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERRO \_ DS \_ DST \_ Domain \_ não \_ nativo**
</dt> <dd> <dl> <dt>

8496 (0x2130)
</dt> <dt>



O domínio de destino deve estar no modo nativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERRO \_ DS \_ - \_ contêiner de infraestrutura ausente \_**
</dt> <dd> <dl> <dt>

8497 (0x2131)
</dt> <dt>



A operação não pode ser executada porque o servidor não tem um contêiner de infraestrutura no domínio de interesse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERRO \_ DS \_ impossível \_ mover \_ grupo de contas \_**
</dt> <dd> <dl> <dt>

8498 (0x2132)
</dt> <dt>



A movimentação entre domínios de grupos de contas não vazios não é permitida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERRO \_ DS não \_ consegue \_ mover o \_ grupo de recursos \_**
</dt> <dd> <dl> <dt>

8499 (0x2133)
</dt> <dt>



A movimentação entre domínios de grupos de recursos não vazios não é permitida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERRO \_ de \_ \_ sinalizador de pesquisa inválido de DS \_**
</dt> <dd> <dl> <dt>

8500 (0x2134)
</dt> <dt>



Os sinalizadores de pesquisa para o atributo são inválidos. O bit ANR é válido somente em atributos de cadeias de caracteres Unicode ou Teletex.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERRO \_ DS \_ sem \_ exclusão de árvore \_ \_ acima do \_ NC**
</dt> <dd> <dl> <dt>

8501 (0x2135)
</dt> <dt>



As exclusões de árvore que começam em um objeto que tem um cabeçalho NC como descendente não são permitidas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERRO \_ \_ \_ \_ de árvore de bloqueio \_ de não foi possível DS para \_ exclusão**
</dt> <dd> <dl> <dt>

8502 (0x2136)
</dt> <dt>



O serviço de diretório não pôde bloquear uma árvore na preparação para uma exclusão de árvore porque a árvore estava em uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERRO \_ DS \_ não foi possível \_ identificar \_ objetos \_ para \_ exclusão de árvore \_**
</dt> <dd> <dl> <dt>

8503 (0x2137)
</dt> <dt>



O serviço de diretório não identificou a lista de objetos a serem excluídos ao tentar uma exclusão de árvore.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERRO \_ \_ \_ falha na inicialização de Sam do DS \_**
</dt> <dd> <dl> <dt>

8504 (0x2138)
</dt> <dt>



Falha na inicialização do Gerenciador de contas de segurança devido ao seguinte erro: %1. Status do erro: 0x %2. Desligue o sistema e reinicialize o Modo de Restauração dos Serviços de Diretório, verifique o log de eventos para obter informações mais detalhadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERRO \_ de \_ \_ violação de grupo confidencial de DS \_**
</dt> <dd> <dl> <dt>

8505 (0x2139)
</dt> <dt>



Somente um administrador pode modificar a lista de membros de um grupo administrativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERRO \_ DS não \_ puder \_ mod \_ PRIMARYGROUPID**
</dt> <dd> <dl> <dt>

8506 (0x213A)
</dt> <dt>



Não é possível alterar a ID do grupo primário de uma conta do controlador de domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERRO \_ DS \_ do \_ esquema base ilegal \_ \_**
</dt> <dd> <dl> <dt>

8507 (0x213B)
</dt> <dt>



É feita uma tentativa de modificar o esquema base.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERRO \_ de \_ alteração de esquema não confiável DS \_ \_**
</dt> <dd> <dl> <dt>

8508 (0x213C)
</dt> <dt>



Adicionar um novo atributo obrigatório a uma classe existente, excluir um atributo obrigatório de uma classe existente ou adicionar um atributo opcional à classe especial Top que não é um atributo backlink (diretamente ou por meio de herança, por exemplo, adicionando ou excluindo uma classe auxiliar) não é permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERRO \_ de \_ atualização do esquema DS não \_ \_ permitido**
</dt> <dd> <dl> <dt>

8509 (0x213D)
</dt> <dt>



A atualização do esquema não é permitida neste controlador de domínio porque o controlador de domínio não é o proprietário da função FSMO do esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERRO \_ DS não \_ consegue \_ criar \_ em \_ esquema**
</dt> <dd> <dl> <dt>

8510 (0x213E)
</dt> <dt>



Um objeto desta classe não pode ser criado no contêiner de esquema. Você só pode criar objetos de esquema de atributo e de esquema de classe no contêiner de esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERRO \_ DS \_ instalação \_ sem \_ src \_ SCH \_ versão**
</dt> <dd> <dl> <dt>

8511 (0x213F)
</dt> <dt>



A instalação de réplica/filho não pôde obter o atributo objectVersion no contêiner de esquema no controlador de domínio de origem. O atributo está ausente no contêiner de esquema ou as credenciais fornecidas não têm permissão para lê-lo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERRO \_ DS \_ instalar \_ nenhuma \_ \_ versão \_ do SCH no \_ inifile**
</dt> <dd> <dl> <dt>

8512 (0x2140)
</dt> <dt>



A instalação de réplica/filho não pôde ler o atributo objectVersion na seção de esquema do arquivo schema.ini no diretório system32.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERRO \_ DS \_ \_ tipo de grupo inválido \_**
</dt> <dd> <dl> <dt>

8513 (0x2141)
</dt> <dt>



O tipo de grupo especificado é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERRO \_ DS \_ nenhum \_ aninhamento \_ global \_ em \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8514 (0x2142)
</dt> <dt>



Você não poderá aninhar grupos globais em um domínio misto se o grupo estiver habilitado para segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERRO \_ DS \_ sem \_ aninhar \_ localgroup \_ em \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8515 (0x2143)
</dt> <dt>



Você não poderá aninhar grupos locais em um domínio misto se o grupo estiver habilitado para segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERRO \_ \_ global DS \_ não \_ tem \_ \_ membro local**
</dt> <dd> <dl> <dt>

8516 (0x2144)
</dt> <dt>



Um grupo global não pode ter um grupo local como membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERRO \_ \_ global DS \_ não \_ tem \_ \_ membro universal**
</dt> <dd> <dl> <dt>

8517 (0x2145)
</dt> <dt>



Um grupo global não pode ter um grupo universal como membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERRO \_ DS \_ Universal \_ não \_ tem \_ \_ membro local**
</dt> <dd> <dl> <dt>

8518 (0x2146)
</dt> <dt>



Um grupo universal não pode ter um grupo local como membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERRO \_ \_ global DS \_ não \_ tem \_ \_ membro CROSSDOMAIN**
</dt> <dd> <dl> <dt>

8519 (0x2147)
</dt> <dt>



Um grupo global não pode ter um membro entre domínios.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERRO \_ \_ local DS \_ não \_ pode ter o \_ \_ membro local CROSSDOMAIN \_**
</dt> <dd> <dl> <dt>

8520 (0x2148)
</dt> <dt>



Um grupo local não pode ter outro grupo local entre domínios como um membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**ERRO \_ DS \_ tem \_ Membros primários \_**
</dt> <dd> <dl> <dt>

8521 (0x2149)
</dt> <dt>



Um grupo com membros primários não pode ser alterado para um grupo desabilitado para segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERRO \_ \_ \_ \_ na conversão SD da cadeia de caracteres DS \_**
</dt> <dd> <dl> <dt>

8522 (0x214A)
</dt> <dt>



O carregamento do cache de esquema falhou ao converter o SD padrão da cadeia de caracteres em um objeto de esquema de classe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERRO \_ DS \_ do \_ mestre de nomeação \_**
</dt> <dd> <dl> <dt>

8523 (0x214B)
</dt> <dt>



Somente os DSAs configurados para serem servidores de catálogo global devem ter permissão para manter a função FSMO do mestre de nomeação de domínio. (Aplica-se somente a servidores Windows 2000.)


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERRO \_ de \_ \_ falha na pesquisa de DNS DS \_**
</dt> <dd> <dl> <dt>

8524 (0x214C)
</dt> <dt>



A operação DSA não pode continuar devido a uma falha de pesquisa de DNS.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERRO \_ de \_ \_ SPNs de atualização de não foi possível DS \_**
</dt> <dd> <dl> <dt>

8525 (0x214D)
</dt> <dt>



Ao processar uma alteração no nome de host DNS de um objeto, os valores de nome da entidade de serviço não puderam ser mantidos em sincronia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERRO \_ DS não \_ consegue \_ recuperar \_ SD**
</dt> <dd> <dl> <dt>

8526 (0x214E)
</dt> <dt>



Não foi possível ler o atributo do descritor de segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERRO \_ de \_ chave DS \_ não \_ exclusiva**
</dt> <dd> <dl> <dt>

8527 (0x214F)
</dt> <dt>



O objeto solicitado não foi encontrado, mas foi encontrado um objeto com essa chave.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERRO \_ de \_ \_ sintaxe de \_ ATT vinculada incorreta de DS \_**
</dt> <dd> <dl> <dt>

8528 (0x2150)
</dt> <dt>



A sintaxe do atributo vinculado que está sendo adicionado está incorreta. Os links de encaminhamento só podem ter sintaxe 2.5.5.1, 2.5.5.7 e 2.5.5.14, e os backlinks só podem ter a sintaxe 2.5.5.1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERRO \_ DS \_ Sam \_ precisa de \_ BOOTKEY \_ senha**
</dt> <dd> <dl> <dt>

8529 (0x2151)
</dt> <dt>



O Gerenciador de contas de segurança precisa obter a senha de inicialização.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERRO \_ DS \_ Sam \_ necessário \_ \_ disquete BOOTKEY**
</dt> <dd> <dl> <dt>

8530 (0x2152)
</dt> <dt>



O Gerenciador de contas de segurança precisa obter a chave de inicialização do disquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERRO o \_ DS não \_ consegue \_ Iniciar**
</dt> <dd> <dl> <dt>

8531 (0x2153)
</dt> <dt>



Não é possível iniciar o serviço de diretório.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERRO \_ de \_ falha de inicialização DS \_**
</dt> <dd> <dl> <dt>

8532 (0x2154)
</dt> <dt>



Os serviços de diretório não puderam ser iniciados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERRO \_ DS \_ sem \_ \_ privacidade \_ de PKT na \_ conexão**
</dt> <dd> <dl> <dt>

8533 (0x2155)
</dt> <dt>



A conexão entre o cliente e o servidor requer a privacidade do pacote ou melhor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERRO \_ \_ \_ \_ de domínio de origem do DS na \_ floresta**
</dt> <dd> <dl> <dt>

8534 (0x2156)
</dt> <dt>



O domínio de origem pode não estar na mesma floresta que o destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERRO \_ \_ \_ domínio de destino DS não está \_ \_ na \_ floresta**
</dt> <dd> <dl> <dt>

8535 (0x2157)
</dt> <dt>



O domínio de destino deve estar na floresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**ERRO \_ de \_ auditoria de destino DS \_ \_ não \_ habilitada**
</dt> <dd> <dl> <dt>

8536 (0x2158)
</dt> <dt>



A operação requer que a auditoria de domínio de destino esteja habilitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERRO \_ DS não \_ consegue \_ encontrar o \_ DC para o \_ \_ \_ domínio src**
</dt> <dd> <dl> <dt>

8537 (0x2159)
</dt> <dt>



A operação não pôde localizar um DC para o domínio de origem.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERRO \_ DS \_ src \_ obj \_ não \_ grupo \_ ou \_ usuário**
</dt> <dd> <dl> <dt>

8538 (0x215A)
</dt> <dt>



O objeto de origem deve ser um grupo ou um usuário.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERRO \_ o \_ Sid src DS \_ \_ existe \_ na \_ floresta**
</dt> <dd> <dl> <dt>

8539 (0x215B)
</dt> <dt>



O SID do objeto de origem já existe na floresta de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERRO \_ \_ \_ de \_ \_ \_ incompatibilidade de classe de objeto DS src e DST \_**
</dt> <dd> <dl> <dt>

8540 (0x215C)
</dt> <dt>



O objeto de origem e de destino deve ser do mesmo tipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERRO \_ Sam \_ init \_ falha**
</dt> <dd> <dl> <dt>

8541 (0x215D)
</dt> <dt>



Falha na inicialização do Gerenciador de contas de segurança devido ao seguinte erro: %1. Status do erro: 0x %2. Clique em OK para desligar o sistema e reinicializar no modo de segurança. Verifique o log de eventos para obter informações detalhadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERRO \_ de \_ \_ remessa de informações de esquema Dra \_ DS \_**
</dt> <dd> <dl> <dt>

8542 (0x215E)
</dt> <dt>



Não foi possível incluir as informações de esquema na solicitação de replicação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERRO \_ de \_ \_ conflito de esquema Dra DS \_**
</dt> <dd> <dl> <dt>

8543 (0x215F)
</dt> <dt>



A operação de replicação não pôde ser concluída devido a uma incompatibilidade de esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERRO \_ DS \_ Dra \_ anterior \_ conflito de esquema \_**
</dt> <dd> <dl> <dt>

8544 (0x2160)
</dt> <dt>



A operação de replicação não pôde ser concluída devido a uma incompatibilidade de esquema anterior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERRO \_ DS \_ Dra \_ obj \_ NC \_ incompatível**
</dt> <dd> <dl> <dt>

8545 (0x2161)
</dt> <dt>



Não foi possível aplicar a atualização de replicação porque a origem ou o destino ainda não recebeu informações sobre uma operação de movimentação entre domínios recente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**o \_ erro \_ NC DS \_ ainda \_ tem \_ DSAs**
</dt> <dd> <dl> <dt>

8546 (0x2162)
</dt> <dt>



Não foi possível excluir o domínio solicitado porque existem controladores de domínio que ainda hospedam esse domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERRO \_ de \_ GC de DS \_ necessário**
</dt> <dd> <dl> <dt>

8547 (0x2163)
</dt> <dt>



A operação solicitada pode ser executada somente em um servidor de catálogo global.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERRO \_ \_ local \_ de membro \_ do \_ DS \_ somente local**
</dt> <dd> <dl> <dt>

8548 (0x2164)
</dt> <dt>



Um grupo local só pode ser um membro de outros grupos locais no mesmo domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERRO \_ DS \_ sem \_ FPO \_ em \_ grupos universais \_**
</dt> <dd> <dl> <dt>

8549 (0x2165)
</dt> <dt>



Entidades de segurança externas não podem ser membros de grupos universais.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERRO \_ DS não \_ consegue \_ Adicionar \_ ao \_ GC**
</dt> <dd> <dl> <dt>

8550 (0x2166)
</dt> <dt>



O atributo não pode ser replicado para o GC devido a motivos de segurança.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERRO \_ DS \_ sem \_ ponto \_ de verificação com \_ PDC**
</dt> <dd> <dl> <dt>

8551 (0x2167)
</dt> <dt>



O ponto de verificação com o PDC não pôde ser obtido porque há muitas modificações sendo processadas no momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERRO \_ de \_ auditoria de origem DS \_ \_ não \_ habilitado**
</dt> <dd> <dl> <dt>

8552 (0x2168)
</dt> <dt>



A operação requer que a auditoria de domínio de origem esteja habilitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERRO \_ DS não \_ consegue \_ criar \_ no \_ \_ NC não domínio**
</dt> <dd> <dl> <dt>

8553 (0x2169)
</dt> <dt>



Os objetos de entidade de segurança só podem ser criados dentro de contextos de nomenclatura de domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERRO \_ \_ \_ nome de DS inválido \_ para \_ SPN**
</dt> <dd> <dl> <dt>

8554 (0x216A)
</dt> <dt>



Não foi possível construir um SPN (nome da entidade de serviço) porque o nome do host fornecido não está no formato necessário.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**ERRO \_ o \_ filtro DS \_ usa \_ construído \_ ATTRS**
</dt> <dd> <dl> <dt>

8555 (0x216B)
</dt> <dt>



Foi passado um filtro que usa atributos construídos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERRO o \_ DS \_ UNICODEPWD não está \_ \_ entre \_ aspas**
</dt> <dd> <dl> <dt>

8556 (0x216C)
</dt> <dt>



O valor do atributo unicodePwd deve ser colocado entre aspas duplas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERRO \_ de \_ cota de conta de computador DS \_ \_ \_ excedida**
</dt> <dd> <dl> <dt>

8557 (0x216D)
</dt> <dt>



Seu computador não pôde ingressar no domínio. Você excedeu o número máximo de contas de computador que você tem permissão para criar nesse domínio. Contate o administrador do sistema para que esse limite seja redefinido ou aumentado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**o erro \_ DS \_ deve \_ ser \_ executado \_ no \_ \_ DC do DST**
</dt> <dd> <dl> <dt>

8558 (0x216E)
</dt> <dt>



Por motivos de segurança, a operação deve ser executada no DC de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERRO \_ DS \_ src \_ DC \_ deve \_ ser \_ SP4 \_ ou \_ superior**
</dt> <dd> <dl> <dt>

8559 (0x216F)
</dt> <dt>



Por motivos de segurança, o DC de origem deve ser NT4SP4 ou superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERRO DS não é possível \_ \_ excluir a \_ árvore \_ \_ crítica \_ obj**
</dt> <dd> <dl> <dt>

8560 (0x2170)
</dt> <dt>



Os objetos do sistema de serviço de diretório crítico não podem ser excluídos durante operações de exclusão de árvore. A exclusão de árvore pode ter sido parcialmente executada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERRO \_ do \_ \_ console de falha de inicialização DS \_**
</dt> <dd> <dl> <dt>

8561 (0x2171)
</dt> <dt>



Os serviços de diretório não puderam ser iniciados devido ao seguinte erro: %1. Status do erro: 0x %2. Clique em OK para desligar o sistema. Você pode usar o console de recuperação para diagnosticar o sistema mais profundamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERRO \_ DS \_ Sam \_ init \_ falha no \_ console**
</dt> <dd> <dl> <dt>

8562 (0x2172)
</dt> <dt>



Falha na inicialização do Gerenciador de contas de segurança devido ao seguinte erro: %1. Status do erro: 0x %2. Clique em OK para desligar o sistema. Você pode usar o console de recuperação para diagnosticar o sistema mais profundamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERRO \_ de \_ versão de floresta DS \_ \_ muito \_ alta**
</dt> <dd> <dl> <dt>

8563 (0x2173)
</dt> <dt>



A versão do sistema operacional é incompatível com o nível funcional da floresta AD DS atual ou AD LDS nível funcional do conjunto de configuração. Você deve atualizar para uma nova versão do sistema operacional antes que este servidor possa se tornar um AD DS controlador de domínio ou adicionar uma instância de AD LDS neste AD DS floresta ou AD LDS conjunto de configurações.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERRO \_ de \_ versão de domínio DS \_ \_ muito \_ alta**
</dt> <dd> <dl> <dt>

8564 (0x2174)
</dt> <dt>



A versão do sistema operacional instalado é incompatível com o nível funcional do domínio atual. Você deve atualizar para uma nova versão do sistema operacional antes que este servidor possa se tornar um controlador de domínio nesse domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERRO \_ de \_ versão de floresta DS \_ \_ muito \_ baixa**
</dt> <dd> <dl> <dt>

8565 (0x2175)
</dt> <dt>



A versão do sistema operacional instalado neste servidor não dá mais suporte ao nível funcional da floresta AD DS atual ou AD LDS nível funcional do conjunto de configurações. Você deve aumentar o nível funcional da floresta AD DS ou AD LDS o nível funcional do conjunto de configuração antes que este servidor possa se tornar um controlador de domínio AD DS ou uma instância de AD LDS nesta floresta ou conjunto de configuração.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERRO \_ de \_ versão de domínio DS \_ \_ muito \_ baixo**
</dt> <dd> <dl> <dt>

8566 (0x2176)
</dt> <dt>



A versão do sistema operacional instalado neste servidor não dá mais suporte ao nível funcional do domínio atual. Você deve aumentar o nível funcional do domínio para que este servidor possa se tornar um controlador de domínio nesse domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERRO \_ de \_ versão incompatível DS \_**
</dt> <dd> <dl> <dt>

8567 (0x2177)
</dt> <dt>



A versão do sistema operacional instalado neste servidor é incompatível com o nível funcional do domínio ou da floresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERRO \_ de \_ versão mínima de \_ DSA de DS \_**
</dt> <dd> <dl> <dt>

8568 (0x2178)
</dt> <dt>



O nível funcional do domínio (ou floresta) não pode ser gerado para o valor solicitado, pois existe um ou mais controladores de domínio no domínio (ou floresta) que estão em um nível funcional inferior incompatível.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERRO \_ DS \_ sem \_ \_ versão \_ de comportamento em \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8569 (0x2179)
</dt> <dt>



O nível funcional da floresta não pode ser aumentado para o valor solicitado, pois um ou mais domínios ainda estão no modo de domínio misto. Todos os domínios na floresta devem estar no modo nativo para que você aumente o nível funcional da floresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERRO \_ DS \_ sem \_ suporte \_ \_ para ordem de classificação**
</dt> <dd> <dl> <dt>

8570 (0x217A)
</dt> <dt>



Não há suporte para a ordem de classificação solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERRO \_ \_ nome DS \_ não \_ exclusivo**
</dt> <dd> <dl> <dt>

8571 (0x217B)
</dt> <dt>



O nome solicitado já existe como um identificador exclusivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERRO \_ \_ conta do computador DS \_ \_ criada \_ PRENT4**
</dt> <dd> <dl> <dt>

8572 (0x217C)
</dt> <dt>



A conta da máquina foi criada antes do NT4. A conta precisa ser recriada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERRO \_ DS \_ fora \_ do \_ repositório de versão \_**
</dt> <dd> <dl> <dt>

8573 (0x217D)
</dt> <dt>



O banco de dados está fora do repositório de versão.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERRO \_ de \_ controles incompatíveis DS \_ \_ usados**
</dt> <dd> <dl> <dt>

8574 (0x217E)
</dt> <dt>



Não é possível continuar a operação porque vários controles conflitantes foram usados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERRO \_ DS \_ sem \_ referência de \_ domínio**
</dt> <dd> <dl> <dt>

8575 (0x217F)
</dt> <dt>



Não é possível localizar um domínio de referência de descritor de segurança válido para esta partição.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**ERRO \_ \_ ID de \_ link \_ reservado DS**
</dt> <dd> <dl> <dt>

8576 (0x2180)
</dt> <dt>



Falha na atualização do esquema: o identificador de link está reservado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**ERRO \_ \_ ID de link DS \_ \_ não \_ disponível**
</dt> <dd> <dl> <dt>

8577 (0x2181)
</dt> <dt>



Falha na atualização do esquema: não há identificadores de link disponíveis.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERRO \_ AG do DS não \_ \_ \_ pode ter \_ \_ membro universal**
</dt> <dd> <dl> <dt>

8578 (0x2182)
</dt> <dt>



Um grupo de contas não pode ter um grupo universal como membro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERRO \_ MODIFYDN DS não \_ \_ permitido \_ por \_ tipo de instância \_**
</dt> <dd> <dl> <dt>

8579 (0x2183)
</dt> <dt>



As operações de renomeação ou movimentação em cabeçalhos de contexto de nomenclatura ou objetos somente leitura não são permitidas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERRO \_ DS \_ sem \_ \_ movimentação \_ de objeto \_ no \_ NC de esquema**
</dt> <dd> <dl> <dt>

8580 (0x2184)
</dt> <dt>



As operações de movimentação em objetos no contexto de nomenclatura de esquema não são permitidas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERRO \_ MODIFYDN DS não \_ \_ permitido \_ por \_ sinalizador**
</dt> <dd> <dl> <dt>

8581 (0x2185)
</dt> <dt>



Um sinalizador do sistema foi definido no objeto e não permite que o objeto seja movido ou renomeado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERRO \_ DS \_ MODIFYDN \_ avô incorreto \_**
</dt> <dd> <dl> <dt>

8582 (0x2186)
</dt> <dt>



Este objeto não tem permissão para alterar seu contêiner avô. As movimentações não são proibidas nesse objeto, mas são restritas a contêineres irmãos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERRO \_ \_ nome DS \_ erro \_ referência de confiança \_**
</dt> <dd> <dl> <dt>

8583 (0x2187)
</dt> <dt>



Não é possível resolver completamente, uma referência a outra floresta é gerada.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERRO \_ sem \_ suporte \_ no \_ \_ servidor Standard**
</dt> <dd> <dl> <dt>

8584 (0x2188)
</dt> <dt>



Não há suporte para a ação solicitada no servidor padrão.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERRO \_ DS \_ não \_ consegue \_ acessar \_ parte remota \_ do \_ AD**
</dt> <dd> <dl> <dt>

8585 (0x2189)
</dt> <dt>



Não foi possível acessar uma partição do serviço de diretório localizado em um servidor remoto. Verifique se pelo menos um servidor está em execução para a partição em questão.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERRO \_ \_ de DS CR \_ impossível \_ para \_ validar \_ v2**
</dt> <dd> <dl> <dt>

8586 (0x218A)
</dt> <dt>



O diretório não pode validar o nome de contexto (ou partição) de nomenclatura proposto porque ele não contém uma réplica nem pode entrar em contato com uma réplica do contexto de nomenclatura acima do contexto de nomenclatura proposto. Verifique se o contexto de nomenclatura pai está registrado corretamente no DNS e se pelo menos uma réplica desse contexto de nomenclatura pode ser acessada pelo mestre de nomeação de domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**ERRO \_ \_ limite de thread DS \_ \_ excedido**
</dt> <dd> <dl> <dt>

8587 (0x218B)
</dt> <dt>



O limite de thread para esta solicitação foi excedido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERRO \_ DS \_ não \_ mais próximo**
</dt> <dd> <dl> <dt>

8588 (0x218C)
</dt> <dt>



O servidor de catálogo global não está no site mais próximo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERRO \_ DS não \_ consegue \_ derivar \_ SPN \_ sem \_ ref do servidor \_**
</dt> <dd> <dl> <dt>

8589 (0x218D)
</dt> <dt>



O DS não pode derivar um SPN (nome da entidade de serviço) com o qual autenticar mutuamente o servidor de destino porque o objeto de servidor correspondente no banco de dados DS local não tem nenhum atributo serverReference.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERRO \_ \_ \_ no modo de usuário único \_ DS \_**
</dt> <dd> <dl> <dt>

8590 (0x218E)
</dt> <dt>



O serviço de diretório não pôde entrar no modo de usuário único.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**erro \_ de \_ \_ erro de sintaxe DS NTDSCRIPT \_**
</dt> <dd> <dl> <dt>

8591 (0x218F)
</dt> <dt>



O serviço de diretório não pode analisar o script devido a um erro de sintaxe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**ERRO \_ de \_ processo de NTDSCRIPT DS \_ \_**
</dt> <dd> <dl> <dt>

8592 (0x2190)
</dt> <dt>



O serviço de diretório não pode processar o script devido a um erro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERRO \_ de \_ \_ épocas de repl diferentes de DS \_**
</dt> <dd> <dl> <dt>

8593 (0x2191)
</dt> <dt>



O serviço de diretório não pode executar a operação solicitada porque os servidores envolvidos são de épocas de replicação diferentes (que geralmente estão relacionadas a uma renomeação de domínio em andamento).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERRO \_ nas \_ extensões DS DRS \_ \_ alteradas**
</dt> <dd> <dl> <dt>

8594 (0x2192)
</dt> <dt>



A associação de serviço de diretório deve ser renegociada devido a uma alteração nas informações de extensões de servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERRO \_ \_ \_ \_ de alteração de conjunto \_ de réplica DS não \_ permitido \_ em \_ CR desabilitado \_**
</dt> <dd> <dl> <dt>

8595 (0x2193)
</dt> <dt>



Operação não permitida em uma referência cruzada desabilitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERRO \_ DS \_ sem \_ msDS \_ inicial**
</dt> <dd> <dl> <dt>

8596 (0x2194)
</dt> <dt>



Falha na atualização do esquema: nenhum valor para o msDS-inicial está disponível.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERRO de Dup de DS inicial de \_ \_ \_ msDS \_**
</dt> <dd> <dl> <dt>

8597 (0x2195)
</dt> <dt>



Falha na atualização do esquema: msDS-inicial duplicado. Repita a operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**ERRO \_ DS \_ existente \_ em \_ RDNATTID**
</dt> <dd> <dl> <dt>

8598 (0x2196)
</dt> <dt>



Falha na exclusão do esquema: o atributo é usado em rDNAttID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERRO \_ de \_ autorização DS \_ falhou**
</dt> <dd> <dl> <dt>

8599 (0x2197)
</dt> <dt>



O serviço de diretório não pôde autorizar a solicitação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERRO \_ de \_ script DS inválido \_**
</dt> <dd> <dl> <dt>

8600 (0x2198)
</dt> <dt>



O serviço de diretório não pode processar o script porque ele é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERRO \_ \_ \_ \_ falha no operação do CROSSREF remoto do DS \_**
</dt> <dd> <dl> <dt>

8601 (0x2199)
</dt> <dt>



A operação de referência cruzada de criação remota falhou no mestre de nomeação de domínio FSMO. O erro da operação está nos dados estendidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERRO \_ de \_ referência cruzada DS \_ \_ ocupado**
</dt> <dd> <dl> <dt>

8602 (0x219A)
</dt> <dt>



Uma referência cruzada está em uso localmente com o mesmo nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERRO \_ DS não \_ consegue \_ derivar \_ SPN \_ para \_ \_ domínio excluído**
</dt> <dd> <dl> <dt>

8603 (0x219B)
</dt> <dt>



O DS não pode derivar um SPN (nome da entidade de serviço) com o qual autenticar mutuamente o servidor de destino porque o domínio do servidor foi excluído da floresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERRO \_ DS \_ impossível \_ rebaixar \_ com \_ NC gravável \_**
</dt> <dd> <dl> <dt>

8604 (0x219C)
</dt> <dt>



NCs graváveis impedem que este DC rebaixe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERRO \_ \_ Id duplicada de DS \_ \_ encontrada**
</dt> <dd> <dl> <dt>

8605 (0x219D)
</dt> <dt>



O objeto solicitado tem um identificador não exclusivo e não pode ser recuperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERRO \_ \_ \_ de attr insuficiente de DS \_ para \_ criar \_ objeto**
</dt> <dd> <dl> <dt>

8606 (0x219E)
</dt> <dt>



Atributos insuficientes foram fornecidos para criar um objeto. Este objeto pode não existir porque pode ter sido excluído e já ter sido coletado como lixo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**erro \_ de \_ conversão de grupo DS \_ \_**
</dt> <dd> <dl> <dt>

8607 (0x219F)
</dt> <dt>



O grupo não pode ser convertido devido a restrições de atributo no tipo de grupo solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERRO \_ DS não \_ consegue \_ mover o \_ \_ grupo básico do aplicativo \_**
</dt> <dd> <dl> <dt>

8608 (0x21A0)
</dt> <dt>



A movimentação entre domínios de grupos de aplicativos básicos não vazios não é permitida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERRO \_ DS não \_ consegue mover o grupo de \_ consultas de \_ aplicativo \_ \_**
</dt> <dd> <dl> <dt>

8609 (0x21A1)
</dt> <dt>



Não é permitida a movimentação entre domínios de grupos de aplicativos baseados em consultas não vazias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**ERRO \_ de \_ função DS \_ não \_ verificada**
</dt> <dd> <dl> <dt>

8610 (0x21A2)
</dt> <dt>



A propriedade da função FSMO não pôde ser verificada porque sua partição de diretório não foi replicada com êxito com pelo menos um parceiro de replicação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERRO \_ o \_ contêiner WKO DS \_ \_ não pode \_ ser \_ especial**
</dt> <dd> <dl> <dt>

8611 (0x21A3)
</dt> <dt>



O contêiner de destino para um redirecionamento de um contêiner de objeto bem conhecido não pode já ser um contêiner especial.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERRO \_ \_ \_ de renomeação de domínio DS \_ em \_ andamento**
</dt> <dd> <dl> <dt>

8612 (0x21A4)
</dt> <dt>



O serviço de diretório não pode executar a operação solicitada porque uma operação de renomeação de domínio está em andamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERRO \_ \_ NC DS \_ filho do AD existente \_ \_**
</dt> <dd> <dl> <dt>

8613 (0x21A5)
</dt> <dt>



O serviço de diretório detectou uma partição filho abaixo do nome da partição solicitada. A hierarquia de partição deve ser criada em um método de cima para baixo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**ERRO \_ de \_ tempo de vida de repl DS \_ \_ excedido**
</dt> <dd> <dl> <dt>

8614 (0x21A6)
</dt> <dt>



O serviço de diretório não pode replicar com este servidor porque o tempo desde a última replicação com este servidor excedeu a vida útil da marca para exclusão.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERRO \_ DS não \_ permitido \_ no \_ contêiner do sistema \_**
</dt> <dd> <dl> <dt>

8615 (0x21A7)
</dt> <dt>



A operação solicitada não é permitida em um objeto no contêiner do sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERRO \_ de \_ fila de envio de LDAP DS \_ \_ \_ cheio**
</dt> <dd> <dl> <dt>

8616 (0x21A8)
</dt> <dt>



A fila de envio de rede dos servidores LDAP foi preenchida porque o cliente não está processando os resultados de suas solicitações com rapidez suficiente. Nenhuma solicitação será processada até que o cliente seja atualizado. Se o cliente não for atualizado, ele será desconectado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**ERRO \_ na \_ \_ janela de \_ agendamento de saída \_ DS**
</dt> <dd> <dl> <dt>

8617 (0x21A9)
</dt> <dt>



A replicação agendada não foi realizada porque o sistema estava muito ocupado para executar a solicitação dentro da janela de agendamento. A fila de replicação está sobrecarregada. Considere a redução do número de parceiros ou a redução da frequência de replicação agendada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERRO \_ de \_ política DS \_ não \_ conhecida**
</dt> <dd> <dl> <dt>

8618 (0x21AA)
</dt> <dt>



Neste momento, não será possível determinar se a política de replicação de ramificação está disponível no controlador de domínio do Hub. Tente novamente mais tarde para considerar as latências de replicação.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERRO \_ nenhum \_ \_ objeto de configurações de site \_**
</dt> <dd> <dl> <dt>

8619 (0x21AB)
</dt> <dt>



O objeto de configurações de site para o site especificado não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERRO \_ sem \_ segredos**
</dt> <dd> <dl> <dt>

8620 (0x21AC)
</dt> <dt>



O repositório de conta local não contém material secreto para a conta especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERRO \_ nenhum \_ \_ DC gravável \_ encontrado**
</dt> <dd> <dl> <dt>

8621 (0x21AD)
</dt> <dt>



Não foi possível encontrar um controlador de domínio gravável no domínio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERRO \_ DS \_ nenhum \_ objeto de servidor \_**
</dt> <dd> <dl> <dt>

8622 (0x21AE)
</dt> <dt>



O objeto de servidor para o controlador de domínio não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERRO \_ DS \_ sem \_ objeto NTDSA \_**
</dt> <dd> <dl> <dt>

8623 (0x21AF)
</dt> <dt>



O objeto de configurações NTDS para o controlador de domínio não existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERRO \_ de \_ \_ pesquisa não \_ ASQ de DS**
</dt> <dd> <dl> <dt>

8624 (0x21B0)
</dt> <dt>



A operação de pesquisa solicitada não tem suporte para pesquisas de ASQ.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERRO \_ de \_ falha de auditoria de DS \_**
</dt> <dd> <dl> <dt>

8625 (0x21B1)
</dt> <dt>



Um evento de auditoria necessário não pôde ser gerado para a operação.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERRO \_ na \_ \_ \_ subárvore do sinalizador de pesquisa inválido do DS \_**
</dt> <dd> <dl> <dt>

8626 (0x21B2)
</dt> <dt>



Os sinalizadores de pesquisa para o atributo são inválidos. O bit de índice de subárvore é válido somente em atributos com valor único.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERRO \_ de \_ \_ tupla de \_ sinalizador de pesquisa inválido \_ de DS**
</dt> <dd> <dl> <dt>

8627 (0x21B3)
</dt> <dt>



Os sinalizadores de pesquisa para o atributo são inválidos. O bit de índice de tupla é válido somente em atributos de cadeias de caracteres Unicode.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERRO \_ na \_ tabela de hierarquia DS \_ \_ muito \_ profunda**
</dt> <dd> <dl> <dt>

8628 (0x21B4)
</dt> <dt>



Os catálogos de endereços estão aninhados muito profundamente. Falha ao criar a tabela de hierarquia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERRO \_ de \_ \_ vetor de \_ Utd corrompido de Dra DS \_**
</dt> <dd> <dl> <dt>

8629 (0x21B5)
</dt> <dt>



O vetor de atualização de qualidade especificado está corrompido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERRO \_ de \_ segredos de Dra DS \_ \_ negado**
</dt> <dd> <dl> <dt>

8630 (0x21B6)
</dt> <dt>



A solicitação para replicar segredos foi negada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**ERRO \_ \_ ID de \_ MAPI reservada para DS \_**
</dt> <dd> <dl> <dt>

8631 (0x21B7)
</dt> <dt>



Falha na atualização do esquema: o identificador MAPI está reservado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERRO a \_ ID de MAPI do DS \_ \_ \_ não \_ está disponível**
</dt> <dd> <dl> <dt>

8632 (0x21B8)
</dt> <dt>



Falha na atualização do esquema: não há identificadores MAPI disponíveis.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERRO \_ DS \_ Dra \_ faltando \_ segredo de krbtgt \_**
</dt> <dd> <dl> <dt>

8633 (0x21B9)
</dt> <dt>



Falha na operação de replicação porque os atributos necessários do objeto krbtgt local estão ausentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERRO \_ o \_ \_ nome de domínio DS \_ existe \_ na \_ floresta**
</dt> <dd> <dl> <dt>

8634 (0x21BA)
</dt> <dt>



O nome de domínio do domínio confiável já existe na floresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERRO \_ o \_ \_ nome simples \_ do DS existe \_ na \_ floresta**
</dt> <dd> <dl> <dt>

8635 (0x21BB)
</dt> <dt>



O nome simples do domínio confiável já existe na floresta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**\_nome da \_ entidade de usuário \_ \_ do erro inválido**
</dt> <dd> <dl> <dt>

8636 (0x21BC)
</dt> <dt>



O UPN (nome principal do usuário) é inválido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERRO \_ o \_ grupo mapeado de OID DS não \_ \_ \_ \_ pode ter \_ Membros**
</dt> <dd> <dl> <dt>

8637 (0x21BD)
</dt> <dt>



Os grupos mapeados por OID não podem ter membros.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERRO \_ de \_ OID DS \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

8638 (0x21BE)
</dt> <dt>



O OID especificado não pode ser encontrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERRO \_ de \_ \_ destino reciclado do Dra DS \_**
</dt> <dd> <dl> <dt>

8639 (0x21BF)
</dt> <dt>



Falha na operação de replicação porque o objeto de destino referenciado por um valor de link foi reciclado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERRO \_ de \_ \_ redirecionamento NC não permitido de DS \_**
</dt> <dd> <dl> <dt>

8640 (0x21C0)
</dt> <dt>



A operação de redirecionamento falhou porque o objeto de destino está em um NC diferente do NC de domínio do controlador de domínio atual.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERRO \_ DS \_ High \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8641 (0x21C1)
</dt> <dt>



O nível funcional do conjunto de configuração AD LDS não pode ser reduzido para o valor solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERRO \_ de \_ versão alta do \_ DSA de DS \_**
</dt> <dd> <dl> <dt>

8642 (0x21C2)
</dt> <dt>



O nível funcional do domínio (ou floresta) não pode ser reduzido para o valor solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERRO \_ DS \_ baixo de \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8643 (0x21C3)
</dt> <dt>



O nível funcional do conjunto de configuração AD LDS não pode ser gerado para o valor solicitado, pois existe uma ou mais instâncias do ADLDS que estão em um nível funcional inferior incompatível.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**ERRO \_ \_ de SID \_ de domínio \_ como \_ estação de \_ trabalho local**
</dt> <dd> <dl> <dt>

8644 (0x21C4)
</dt> <dt>



O ingresso no domínio não pode ser concluído porque o SID do domínio que você tentou ingressar era idêntico ao SID deste computador. Esse é um sintoma de uma instalação de sistema operacional clonado incorretamente. Você deve executar o Sysprep neste computador para gerar um novo SID de máquina. Consulte <https://go.microsoft.com/fwlink/p/?linkid=168895> para obter mais informações.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERRO \_ \_ \_ \_ ao restaurar \_ falha na validação do Sam do DS**
</dt> <dd> <dl> <dt>

8645 (0x21C5)
</dt> <dt>



Falha na operação de reexclusão porque o nome da conta Sam ou o nome da conta Sam adicional do objeto que está sendo inexcluído está em conflito com um objeto dinâmico existente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERRO \_ \_ tipo de conta incorreto \_**
</dt> <dd> <dl> <dt>

8646 (0x21C6)
</dt> <dt>



O sistema não é autoritativo para a conta especificada e, portanto, não pode concluir a operação. Repita a operação usando o provedor associado a esta conta. Se este for um provedor online, use o site online do provedor.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de erro do sistema](system-error-codes.md)
</dt> </dl>

 

 




