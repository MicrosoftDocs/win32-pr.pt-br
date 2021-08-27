---
title: Códigos de erro de WFP (Winerror h)
description: (WFP) códigos de erro específicos.
ms.assetid: 11f3085a-f044-4a78-b47a-59b9086562bf
topic_type:
- apiref
api_name:
- FWP_E_CALLOUT_NOT_FOUND
- FWP_E_CONDITION_NOT_FOUND
- FWP_E_FILTER_NOT_FOUND
- FWP_E_LAYER_NOT_FOUND
- FWP_E_PROVIDER_NOT_FOUND
- FWP_E_PROVIDER_CONTEXT_NOT_FOUND
- FWP_E_SUBLAYER_NOT_FOUND
- FWP_E_NOT_FOUND
- FWP_E_ALREADY_EXISTS
- FWP_E_IN_USE
- FWP_E_DYNAMIC_SESSION_IN_PROGRESS
- FWP_E_WRONG_SESSION
- FWP_E_NO_TXN_IN_PROGRESS
- FWP_E_TXN_IN_PROGRESS
- FWP_E_TXN_ABORTED
- FWP_E_SESSION_ABORTED
- FWP_E_INCOMPATIBLE_TXN
- FWP_E_TIMEOUT
- FWP_E_NET_EVENTS_DISABLED
- FWP_E_INCOMPATIBLE_LAYER
- FWP_E_KM_CLIENTS_ONLY
- FWP_E_LIFETIME_MISMATCH
- FWP_E_BUILTIN_OBJECT
- FWP_E_TOO_MANY_CALLOUTS
- FWP_E_NOTIFICATION_DROPPED
- FWP_E_TRAFFIC_MISMATCH
- FWP_E_INCOMPATIBLE_SA_STATE
- FWP_E_NULL_POINTER
- FWP_E_INVALID_ENUMERATOR
- FWP_E_INVALID_FLAGS
- FWP_E_INVALID_NET_MASK
- FWP_E_INVALID_RANGE
- FWP_E_INVALID_INTERVAL
- FWP_E_ZERO_LENGTH_ARRAY
- FWP_E_NULL_DISPLAY_NAME
- FWP_E_INVALID_ACTION_TYPE
- FWP_E_INVALID_WEIGHT
- FWP_E_MATCH_TYPE_MISMATCH
- FWP_E_TYPE_MISMATCH
- FWP_E_OUT_OF_BOUNDS
- FWP_E_RESERVED
- FWP_E_DUPLICATE_CONDITION
- FWP_E_DUPLICATE_KEYMOD
- FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER
- FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER
- FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT
- FWP_E_INCOMPATIBLE_AUTH_METHOD
- FWP_E_INCOMPATIBLE_DH_GROUP
- FWP_E_EM_NOT_SUPPORTED
- FWP_E_NEVER_MATCH
- FWP_E_PROVIDER_CONTEXT_MISMATCH
- FWP_E_INVALID_PARAMETER
- FWP_E_TOO_MANY_SUBLAYERS
- FWP_E_CALLOUT_NOTIFICATION_FAILED
- FWP_E_INVALID_AUTH_TRANSFORM
- FWP_E_INVALID_CIPHER_TRANSFORM
api_location:
- winerror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21550e0c8872f0d0f8c067b38044a946f10f452d06ca213dea414d34756ce7ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083196"
---
# <a name="wfp-error-codes"></a>Códigos de erro do WFP

Windows Os códigos de erro específicos da WFP (Plataforma de Filtragem) são os a seguir.

<dl> <dt>

<span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**FWP \_ E \_ CALLOUT NÃO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

0x80320001
</dt> <dt>



O callout não existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**CONDIÇÃO FWP \_ E \_ NÃO \_ \_ ENCONTRADA**
</dt> <dd> <dl> <dt>

0x80320002
</dt> <dt>



A condição de filtro não existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**FILTRO FWP \_ E \_ NÃO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

0x80320003
</dt> <dt>



O filtro não existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**CAMADA FWP \_ E \_ NÃO \_ \_ ENCONTRADA**
</dt> <dd> <dl> <dt>

0x80320004
</dt> <dt>



A camada não existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**PROVEDOR FWP \_ E \_ NÃO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

0x80320005
</dt> <dt>



O provedor não existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**CONTEXTO DO PROVEDOR \_ FWP E \_ NÃO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

0x80320006
</dt> <dt>



O contexto do provedor não existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**FWP \_ E \_ SUBLAYER \_ NÃO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

0x80320007
</dt> <dt>



A sub-camada não existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**FWP \_ E \_ NÃO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

0x80320008
</dt> <dt>



O objeto não existe.

As [funções IPsecSaContext retornarão \* ](fwp-ipsec-functions.md) esse erro se a ID de contexto sa não for encontrada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**FWP \_ E \_ JÁ \_ EXISTE**
</dt> <dd> <dl> <dt>

0x80320009
</dt> <dt>



Já existe um objeto com esse GUID ou LUID.


</dt> </dl> </dd> <dt>

<span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**FWP \_ E \_ EM \_ USO**
</dt> <dd> <dl> <dt>

0x8032000A
</dt> <dt>



O objeto é referenciado por outros objetos, portanto, ele não pode ser excluído.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**FWP \_ E SESSÃO DINÂMICA EM \_ \_ \_ \_ ANDAMENTO**
</dt> <dd> <dl> <dt>

0x8032000B
</dt> <dt>



A chamada não é permitida de dentro de uma sessão dinâmica.


</dt> </dl> </dd> <dt>

<span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**FWP \_ E \_ SESSÃO \_ ERRADA**
</dt> <dd> <dl> <dt>

0x8032000C
</dt> <dt>



A chamada foi feita da sessão errada, portanto, ela não pode ser concluída.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP \_ E \_ NENHUM \_ TXN \_ EM \_ ANDAMENTO**
</dt> <dd> <dl> <dt>

0x8032000D
</dt> <dt>



A chamada deve ser feita de dentro de uma transação explícita.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**FWP \_ E \_ TXN \_ EM \_ ANDAMENTO**
</dt> <dd> <dl> <dt>

0x8032000E
</dt> <dt>



A chamada não é permitida de dentro de uma transação explícita.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**FWP \_ E \_ TXN \_ ANULADO**
</dt> <dd> <dl> <dt>

0x8032000F
</dt> <dt>



A transação explícita foi cancelada à força.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**SESSÃO FWP \_ E \_ \_ ANULADA**
</dt> <dd> <dl> <dt>

0x80320010
</dt> <dt>



A sessão foi cancelada.

O handle de sessão precisa ser fechado chamando [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0), mesmo que ele não seja mais válido; caso contrário, o estado do lado do cliente será vazado. Uma nova sessão deve ser criada chamando [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**FWP \_ E \_ \_ TXN INCOMPATÍVEL**
</dt> <dd> <dl> <dt>

0x80320011
</dt> <dt>



A chamada não é permitida de dentro de uma transação somente leitura.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**FWP \_ E \_ TIMEOUT**
</dt> <dd> <dl> <dt>

0x80320012
</dt> <dt>



A chamada tempou ao aguardar para adquirir o bloqueio de transação.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**EVENTOS FWP \_ E \_ NET \_ \_ DESABILITADOS**
</dt> <dd> <dl> <dt>

0x80320013
</dt> <dt>



A coleção de eventos de diagnóstico de rede está desabilitada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**CAMADA INCOMPATÍVEL \_ FWP E \_ \_**
</dt> <dd> <dl> <dt>

0x80320014
</dt> <dt>



A operação não é suportada pela camada especificada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**SOMENTE CLIENTES FWP \_ E \_ KM \_ \_**
</dt> <dd> <dl> <dt>

0x80320015
</dt> <dt>



A chamada é permitida somente para chamadores de modo kernel.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**INCOMPATIBILIDADE DE TEMPO DE VIDA DO FWP \_ E \_ \_**
</dt> <dd> <dl> <dt>

0x80320016
</dt> <dt>



A chamada tentou associar dois objetos a tempo de vida incompatíveis.

Consulte [Gerenciamento de Objetos](object-management.md) para obter mais informações sobre o tempo de vida do objeto e a associação de objeto.


</dt> </dl> </dd> <dt>

<span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**OBJETO FWP \_ E \_ \_ BUILTIN**
</dt> <dd> <dl> <dt>

0x80320017
</dt> <dt>



O objeto é integrado, portanto, não pode ser excluído.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**FWP \_ E \_ MUITOS \_ \_ CALLOUTS**
</dt> <dd> <dl> <dt>

0x80320018
</dt> <dt>



O número máximo de callouts foi atingido.

No máximo, 100.000 callouts podem ser registrados ao mesmo tempo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**NOTIFICAÇÃO DE FWP \_ E \_ \_ DESCARTADO**
</dt> <dd> <dl> <dt>

0x80320019
</dt> <dt>



Não foi possível entregar uma notificação porque uma fila de mensagens está em sua capacidade máxima.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**INCOMPATIBILIDADE DE \_ TRÁFEGO FWP E \_ \_**
</dt> <dd> <dl> <dt>

0x8032001A
</dt> <dt>



Os parâmetros de tráfego de rede não são os que são de acordo com o contexto de associação de segurança.

[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) pode ser chamado várias vezes, mas o chamador deve especificar o mesmo [**\_ IPSEC TRAFFIC0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) a cada vez. Esse erro será retornado se uma chamada subsequente fornece um **IPSEC \_ TRAFFIC0 diferente.**


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**FWP \_ E ESTADO SA \_ \_ \_ INCOMPATÍVEL**
</dt> <dd> <dl> <dt>

0x8032001B
</dt> <dt>



A chamada não é permitida para o estado sa (associação de segurança) atual.

As funções de contexto SA devem ser chamadas em uma ordem específica:

-   [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)
-   [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)
-   [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)
-   [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)

Esse erro será retornado se eles são chamados fora de ordem.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**FWP \_ E \_ PONTEIRO \_ NULO**
</dt> <dd> <dl> <dt>

0x8032001C
</dt> <dt>



Um ponteiro necessário é nulo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**ENUMERADOR FWP \_ E \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

0x8032001D
</dt> <dt>



Um valor de enumerador em uma estrutura está fora do intervalo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**SINALIZADORES FWP \_ E \_ \_ INVÁLIDOS**
</dt> <dd> <dl> <dt>

0x8032001E
</dt> <dt>



O campo sinalizadores contém um valor inválido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**FWP \_ E MÁSCARA DE REDE \_ \_ \_ INVÁLIDA**
</dt> <dd> <dl> <dt>

0x8032001F
</dt> <dt>



Uma máscara de rede não é válida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**FWP \_ E \_ INTERVALO \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

0x80320020
</dt> <dt>



Uma [**estrutura \_ RANGE0 FWP**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) não é válida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**FWP \_ E \_ INTERVALO \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

0x80320021
</dt> <dt>



O intervalo de tempo não é válido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**FWP \_ E MATRIZ DE COMPRIMENTO \_ \_ \_ ZERO**
</dt> <dd> <dl> <dt>

0x80320022
</dt> <dt>



Uma matriz que deve conter pelo menos um elemento tem comprimento zero.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**FWP \_ E NOME DE \_ \_ EXIBIÇÃO \_ NULO**
</dt> <dd> <dl> <dt>

0x80320023
</dt> <dt>



O **displayData.name** campo não pode ser nulo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**FWP \_ E TIPO DE AÇÃO \_ \_ \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

0x80320024
</dt> <dt>



O tipo de ação não é um dos tipos de ação permitidos para um filtro.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**FWP \_ E \_ PESO \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

0x80320025
</dt> <dt>



O peso do filtro não é válido.

Consulte [Filtrar a atribuição de peso](filter-weight-assignment.md) para obter mais informações.


</dt> </dl> </dd> <dt>

<span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**FWP \_ E \_ MATCH \_ TYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

0x80320026
</dt> <dt>



Uma condição de filtro contém um tipo de combinação que não é compatível com os operadores.

Consulte [**FWP \_ MATCH TYPE \_ para**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) obter mais informações.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**INCOMPATIBILIDADE DE TIPO \_ FWP E \_ \_**
</dt> <dd> <dl> <dt>

0x80320027
</dt> <dt>



Uma [**estrutura FWP \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) ou uma [**estrutura FWPM CONDITION \_ \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) é do tipo errado.


</dt> </dl> </dd> <dt>

<span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP \_ E FORA DOS \_ \_ \_ LIMITES**
</dt> <dd> <dl> <dt>

0x80320028
</dt> <dt>



Um valor inteiro está fora do intervalo permitido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP \_ E \_ RESERVADO**
</dt> <dd> <dl> <dt>

0x80320029
</dt> <dt>



Um campo reservado é não zero.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**FWP \_ E \_ CONDIÇÃO \_ DUPLICADA**
</dt> <dd> <dl> <dt>

0x8032002A
</dt> <dt>



Um filtro não pode conter várias condições operando em um único campo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**FWP \_ E \_ \_ KEYMOD DUPLICADO**
</dt> <dd> <dl> <dt>

0x8032002B
</dt> <dt>



Uma política não pode conter o mesmo módulo de chave mais de uma vez.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**AÇÃO FWP \_ E \_ \_ INCOMPATÍVEL \_ COM \_ CAMADA**
</dt> <dd> <dl> <dt>

0x8032002C
</dt> <dt>



O tipo de ação não é compatível com a camada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**AÇÃO FWP \_ E \_ \_ INCOMPATÍVEL \_ COM \_ SUBCAMADA**
</dt> <dd> <dl> <dt>

0x8032002D
</dt> <dt>



O tipo de ação não é compatível com a sub-camada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**CONTEXTO FWP \_ E \_ \_ INCOMPATÍVEL \_ COM \_ CAMADA**
</dt> <dd> <dl> <dt>

0x8032002E
</dt> <dt>



O contexto bruto ou o contexto do provedor não é compatível com a camada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**CONTEXTO FWP \_ E \_ \_ INCOMPATÍVEL \_ COM O \_ CALLOUT**
</dt> <dd> <dl> <dt>

0x8032002F
</dt> <dt>



O contexto bruto ou o contexto do provedor não é compatível com o callout.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**MÉTODO DE \_ \_ \_ AUTH INCOMPATÍVEL COM FWP \_ E**
</dt> <dd> <dl> <dt>

0x80320030
</dt> <dt>



O método de autenticação não é compatível com o tipo de política.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**FWP \_ E \_ GRUPO \_ DH \_ INCOMPATÍVEL**
</dt> <dd> <dl> <dt>

0x80320031L
</dt> <dt>



O Diffie-Hellman grupo não é compatível com o tipo de política.


</dt> </dl> </dd> <dt>

<span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**NÃO HÁ SUPORTE PARA FWP \_ E \_ EM \_ \_**
</dt> <dd> <dl> <dt>

0x80320032
</dt> <dt>



Uma política IKE não pode conter uma política de Modo Estendido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP \_ E \_ NUNCA \_ CORRESPONDER**
</dt> <dd> <dl> <dt>

0x80320033
</dt> <dt>



O modelo de enumeração ou a assinatura nunca corresponderá a nenhum objeto.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**INCOMPATIBILIDADE DE CONTEXTO \_ DO PROVEDOR FWP E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80320034
</dt> <dt>



O contexto do provedor é do tipo errado.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**FWP \_ E \_ PARÂMETRO \_ INVÁLIDO**
</dt> <dd> <dl> <dt>

0x80320035
</dt> <dt>



O parâmetro está incorreto.

Possíveis motivos para esse erro:

-   [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) foi chamado sem definir o sinalizador **FWPM \_ TUNNEL FLAG POINT TO \_ \_ \_ \_ POINT** e com condições diferentes do endereço local/remoto.
-   Uma cadeia de caracteres Unicode inválida ou uma cadeia de caracteres Unicode que contém caracteres não imprimíveis.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**FWP \_ E \_ MUITOS \_ \_ SUBCAMADORES**
</dt> <dd> <dl> <dt>

0x80320036
</dt> <dt>



O número máximo de subcamdas foi atingido.

O WFP dá suporte a no máximo 2 6 subcamas.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**FALHA NA NOTIFICAÇÃO \_ DE CHAMADA FWP E \_ \_ \_**
</dt> <dd> <dl> <dt>

0x80320037
</dt> <dt>



A função de notificação de um callout retornou um erro.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**FWP \_ E TRANSFORMAÇÃO DE \_ \_ AUTH \_ INVÁLIDA**
</dt> <dd> <dl> <dt>

0x80320038
</dt> <dt>



A transformação de autenticação IPsec não é válida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**FWP \_ E TRANSFORMAÇÃO DE CRIPTOGRAFIA \_ \_ \_ INVÁLIDA**
</dt> <dd> <dl> <dt>

0x80320039
</dt> <dt>



A transformação de criptografia IPsec não é válida.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Winerror.h</dt> </dl> |



 

 





