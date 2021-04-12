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
ms.openlocfilehash: 4a0e7ee1ab0364a31f136f0c0cdbf87f459225b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455519"
---
# <a name="wfp-error-codes"></a>Códigos de erro WFP

Os códigos de erro específicos da WFP (Windows Filtering Platform) são os seguintes.

<dl> <dt>

<span id="FWP_E_CALLOUT_NOT_FOUND"></span><span id="fwp_e_callout_not_found"></span>**FWP \_ E \_ texto explicativo \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

0x80320001
</dt> <dt>



O texto explicativo não existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONDITION_NOT_FOUND"></span><span id="fwp_e_condition_not_found"></span>**FWP \_ E \_ condição \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

0x80320002
</dt> <dt>



A condição de filtro não existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_FILTER_NOT_FOUND"></span><span id="fwp_e_filter_not_found"></span>**\_filtro fwp \_ E \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

0x80320003
</dt> <dt>



O filtro não existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LAYER_NOT_FOUND"></span><span id="fwp_e_layer_not_found"></span>**FWP \_ E \_ camada \_ não \_ encontrada**
</dt> <dd> <dl> <dt>

0x80320004
</dt> <dt>



A camada não existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_NOT_FOUND"></span><span id="fwp_e_provider_not_found"></span>**\_provedor fwp \_ E \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

0x80320005
</dt> <dt>



O provedor não existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_NOT_FOUND"></span><span id="fwp_e_provider_context_not_found"></span>**o \_ contexto do provedor fwp E \_ \_ \_ não \_ foi encontrado**
</dt> <dd> <dl> <dt>

0x80320006
</dt> <dt>



O contexto do provedor não existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SUBLAYER_NOT_FOUND"></span><span id="fwp_e_sublayer_not_found"></span>**a \_ \_ subcamada de fwp E \_ não \_ foi encontrada**
</dt> <dd> <dl> <dt>

0x80320007
</dt> <dt>



A subcamada não existe.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOT_FOUND"></span><span id="fwp_e_not_found"></span>**FWP \_ E \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

0x80320008
</dt> <dt>



O objeto não existe.

As [funções \* IPsecSaContext](fwp-ipsec-functions.md) retornarão esse erro se a ID de contexto SA não for encontrada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ALREADY_EXISTS"></span><span id="fwp_e_already_exists"></span>**FWP \_ E \_ já \_ existe**
</dt> <dd> <dl> <dt>

0x80320009
</dt> <dt>



Já existe um objeto com esse GUID ou LUID.


</dt> </dl> </dd> <dt>

<span id="FWP_E_IN_USE"></span><span id="fwp_e_in_use"></span>**FWP \_ E \_ em \_ uso**
</dt> <dd> <dl> <dt>

0x8032000A
</dt> <dt>



O objeto é referenciado por outros objetos, portanto, não pode ser excluído.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DYNAMIC_SESSION_IN_PROGRESS"></span><span id="fwp_e_dynamic_session_in_progress"></span>**FWP \_ E \_ \_ sessão dinâmica \_ em \_ andamento**
</dt> <dd> <dl> <dt>

0x8032000B
</dt> <dt>



A chamada não é permitida de dentro de uma sessão dinâmica.


</dt> </dl> </dd> <dt>

<span id="FWP_E_WRONG_SESSION"></span><span id="fwp_e_wrong_session"></span>**FWP \_ E \_ sessão incorreta \_**
</dt> <dd> <dl> <dt>

0x8032000C
</dt> <dt>



A chamada foi feita da sessão errada, portanto, ela não pode ser concluída.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NO_TXN_IN_PROGRESS"></span><span id="fwp_e_no_txn_in_progress"></span>**FWP \_ E \_ nenhum \_ TXN \_ em \_ andamento**
</dt> <dd> <dl> <dt>

0x8032000D
</dt> <dt>



A chamada deve ser feita de dentro de uma transação explícita.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_IN_PROGRESS"></span><span id="fwp_e_txn_in_progress"></span>**FWP \_ E \_ TXN \_ em \_ andamento**
</dt> <dd> <dl> <dt>

0x8032000E
</dt> <dt>



A chamada não é permitida de dentro de uma transação explícita.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TXN_ABORTED"></span><span id="fwp_e_txn_aborted"></span>**FWP \_ E \_ TXN \_ anulados**
</dt> <dd> <dl> <dt>

0x8032000F
</dt> <dt>



A transação explícita foi cancelada forçosamente.


</dt> </dl> </dd> <dt>

<span id="FWP_E_SESSION_ABORTED"></span><span id="fwp_e_session_aborted"></span>**\_sessão fwp \_ E \_ abortada**
</dt> <dd> <dl> <dt>

0x80320010
</dt> <dt>



A sessão foi cancelada.

O identificador de sessão precisa ser fechado chamando [**FwpmEngineClose0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineclose0), mesmo que não seja mais válido; caso contrário, o estado do lado do cliente será vazado. Uma nova sessão deve ser criada chamando [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_TXN"></span><span id="fwp_e_incompatible_txn"></span>**FWP \_ E \_ incompatível \_ TXN**
</dt> <dd> <dl> <dt>

0x80320011
</dt> <dt>



A chamada não é permitida de dentro de uma transação somente leitura.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TIMEOUT"></span><span id="fwp_e_timeout"></span>**FWP \_ E \_ tempo limite**
</dt> <dd> <dl> <dt>

0x80320012
</dt> <dt>



A chamada atingiu o tempo limite enquanto aguardava para adquirir o bloqueio de transação.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NET_EVENTS_DISABLED"></span><span id="fwp_e_net_events_disabled"></span>**\_eventos fwp \_ E \_ net \_ desabilitados**
</dt> <dd> <dl> <dt>

0x80320013
</dt> <dt>



A coleção de eventos de diagnóstico de rede está desabilitada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_LAYER"></span><span id="fwp_e_incompatible_layer"></span>**FWP \_ E \_ camada incompatível \_**
</dt> <dd> <dl> <dt>

0x80320014
</dt> <dt>



A camada especificada não dá suporte para a operação.


</dt> </dl> </dd> <dt>

<span id="FWP_E_KM_CLIENTS_ONLY"></span><span id="fwp_e_km_clients_only"></span>**\_os clientes do fwp E \_ km \_ \_ somente**
</dt> <dd> <dl> <dt>

0x80320015
</dt> <dt>



A chamada é permitida somente para chamadores de modo kernel.


</dt> </dl> </dd> <dt>

<span id="FWP_E_LIFETIME_MISMATCH"></span><span id="fwp_e_lifetime_mismatch"></span>**Não \_ \_ correspondência de vida \_ de fwp E**
</dt> <dd> <dl> <dt>

0x80320016
</dt> <dt>



A chamada tentou associar dois objetos a tempos de vida incompatíveis.

Consulte [Gerenciamento de objetos](object-management.md) para obter mais informações sobre a vida útil de objetos e a associação de objetos.


</dt> </dl> </dd> <dt>

<span id="FWP_E_BUILTIN_OBJECT"></span><span id="fwp_e_builtin_object"></span>**\_objeto fwp E \_ BuiltIn \_**
</dt> <dd> <dl> <dt>

0x80320017
</dt> <dt>



O objeto é interno e, portanto, não pode ser excluído.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_CALLOUTS"></span><span id="fwp_e_too_many_callouts"></span>**FWP \_ E \_ \_ muitos \_ textos explicativos**
</dt> <dd> <dl> <dt>

0x80320018
</dt> <dt>



O número máximo de textos explicativos foi atingido.

No máximo, os textos explicativos 100.000 podem ser registrados ao mesmo tempo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NOTIFICATION_DROPPED"></span><span id="fwp_e_notification_dropped"></span>**FWP \_ E \_ notificação \_ eliminada**
</dt> <dd> <dl> <dt>

0x80320019
</dt> <dt>



Não foi possível entregar uma notificação porque uma fila de mensagens está em sua capacidade máxima.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TRAFFIC_MISMATCH"></span><span id="fwp_e_traffic_mismatch"></span>**FWP \_ E \_ \_ incompatibilidade de tráfego**
</dt> <dd> <dl> <dt>

0x8032001A
</dt> <dt>



Os parâmetros de tráfego de rede não correspondem aos do contexto de associação de segurança.

[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) pode ser chamado várias vezes, mas o chamador deve especificar o mesmo [**\_ TRAFFIC0 de IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0) a cada vez. Esse erro será retornado se uma chamada subsequente fornecer um **\_ TRAFFIC0 IPSec** diferente.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_SA_STATE"></span><span id="fwp_e_incompatible_sa_state"></span>**FWP \_ E \_ estado de \_ SA incompatível \_**
</dt> <dd> <dl> <dt>

0x8032001B
</dt> <dt>



A chamada não é permitida para o estado atual da Associação de segurança (SA).

As funções de contexto SA devem ser chamadas em uma ordem específica:

-   [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)
-   [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)
-   [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)
-   [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)

Esse erro será retornado se eles forem chamados fora de ordem.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_POINTER"></span><span id="fwp_e_null_pointer"></span>**\ \_ fwp \_ E \_ ponteiro nulo**
</dt> <dd> <dl> <dt>

0x8032001C
</dt> <dt>



Um ponteiro necessário é nulo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ENUMERATOR"></span><span id="fwp_e_invalid_enumerator"></span>**FWP \_ E \_ \_ enumerador inválido**
</dt> <dd> <dl> <dt>

0x8032001D
</dt> <dt>



Um valor de enumerador em uma estrutura está fora do intervalo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_FLAGS"></span><span id="fwp_e_invalid_flags"></span>**FWP \_ E \_ Sinalizadores inválidos \_**
</dt> <dd> <dl> <dt>

0x8032001E
</dt> <dt>



O campo de sinalizadores contém um valor inválido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_NET_MASK"></span><span id="fwp_e_invalid_net_mask"></span>**FWP \_ E \_ \_ máscara de rede inválida \_**
</dt> <dd> <dl> <dt>

0x8032001F
</dt> <dt>



Uma máscara de rede não é válida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_RANGE"></span><span id="fwp_e_invalid_range"></span>**FWP \_ E \_ \_ intervalo inválido**
</dt> <dd> <dl> <dt>

0x80320020
</dt> <dt>



Uma estrutura [**fwp \_ RANGE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_range0) não é válida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_INTERVAL"></span><span id="fwp_e_invalid_interval"></span>**FWP \_ E \_ \_ intervalo inválido**
</dt> <dd> <dl> <dt>

0x80320021
</dt> <dt>



O intervalo de tempo não é válido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ZERO_LENGTH_ARRAY"></span><span id="fwp_e_zero_length_array"></span>**a \_ matriz de comprimento de fwp E \_ zero \_ \_**
</dt> <dd> <dl> <dt>

0x80320022
</dt> <dt>



Uma matriz que deve conter pelo menos um elemento tem comprimento zero.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NULL_DISPLAY_NAME"></span><span id="fwp_e_null_display_name"></span>**FWP \_ E \_ \_ nome de exibição nulo \_**
</dt> <dd> <dl> <dt>

0x80320023
</dt> <dt>



O campo **displayData.Name** não pode ser nulo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_ACTION_TYPE"></span><span id="fwp_e_invalid_action_type"></span>**FWP \_ E \_ \_ tipo de ação inválido \_**
</dt> <dd> <dl> <dt>

0x80320024
</dt> <dt>



O tipo de ação não é um dos tipos de ação permitidos para um filtro.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_WEIGHT"></span><span id="fwp_e_invalid_weight"></span>**FWP \_ E \_ \_ peso inválido**
</dt> <dd> <dl> <dt>

0x80320025
</dt> <dt>



O peso do filtro não é válido.

Consulte [atribuição de peso de filtro](filter-weight-assignment.md) para obter mais informações.


</dt> </dl> </dd> <dt>

<span id="FWP_E_MATCH_TYPE_MISMATCH"></span><span id="fwp_e_match_type_mismatch"></span>**o \_ tipo de correspondência fwp E não \_ \_ \_ corresponde**
</dt> <dd> <dl> <dt>

0x80320026
</dt> <dt>



Uma condição de filtro contém um tipo de correspondência que não é compatível com os operandos.

Confira [**\_ \_ tipo de correspondência fwp**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_match_type) para obter mais informações.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TYPE_MISMATCH"></span><span id="fwp_e_type_mismatch"></span>**FWP \_ E \_ tipo \_ incompatível**
</dt> <dd> <dl> <dt>

0x80320027
</dt> <dt>



Uma estrutura [**fwp \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_value0) ou uma estrutura [**FWPM \_ condição \_ VALUE0**](/windows/desktop/api/Fwptypes/ns-fwptypes-fwp_condition_value0) é do tipo errado.


</dt> </dl> </dd> <dt>

<span id="FWP_E_OUT_OF_BOUNDS"></span><span id="fwp_e_out_of_bounds"></span>**FWP \_ E \_ fora \_ dos \_ limites**
</dt> <dd> <dl> <dt>

0x80320028
</dt> <dt>



Um valor inteiro está fora do intervalo permitido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_RESERVED"></span><span id="fwp_e_reserved"></span>**FWP \_ E \_ reservado**
</dt> <dd> <dl> <dt>

0x80320029
</dt> <dt>



Um campo reservado é diferente de zero.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_CONDITION"></span><span id="fwp_e_duplicate_condition"></span>**FWP \_ E \_ condição duplicada \_**
</dt> <dd> <dl> <dt>

0x8032002A
</dt> <dt>



Um filtro não pode conter várias condições operando em um único campo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_DUPLICATE_KEYMOD"></span><span id="fwp_e_duplicate_keymod"></span>**FWP \_ E \_ duplicar \_ KEYMOD**
</dt> <dd> <dl> <dt>

0x8032002B
</dt> <dt>



Uma política não pode conter o mesmo módulo de chaveamento mais de uma vez.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_action_incompatible_with_layer"></span>**\_ação fwp \_ E \_ incompatível \_ com \_ camada**
</dt> <dd> <dl> <dt>

0x8032002C
</dt> <dt>



O tipo de ação não é compatível com a camada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_ACTION_INCOMPATIBLE_WITH_SUBLAYER"></span><span id="fwp_e_action_incompatible_with_sublayer"></span>**\_ação fwp \_ E \_ incompatível \_ com \_ subcamada**
</dt> <dd> <dl> <dt>

0x8032002D
</dt> <dt>



O tipo de ação não é compatível com a subcamada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_LAYER"></span><span id="fwp_e_context_incompatible_with_layer"></span>**o \_ contexto fwp E é \_ \_ incompatível \_ com a \_ camada**
</dt> <dd> <dl> <dt>

0x8032002E
</dt> <dt>



O contexto bruto ou o contexto do provedor não é compatível com a camada.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CONTEXT_INCOMPATIBLE_WITH_CALLOUT"></span><span id="fwp_e_context_incompatible_with_callout"></span>**o \_ contexto fwp E é \_ \_ incompatível \_ com o \_ texto explicativo**
</dt> <dd> <dl> <dt>

0x8032002F
</dt> <dt>



O contexto bruto ou o contexto do provedor não é compatível com o texto explicativo.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_AUTH_METHOD"></span><span id="fwp_e_incompatible_auth_method"></span>**FWP \_ E \_ método de \_ autenticação incompatível \_**
</dt> <dd> <dl> <dt>

0x80320030
</dt> <dt>



O método de autenticação não é compatível com o tipo de política.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INCOMPATIBLE_DH_GROUP"></span><span id="fwp_e_incompatible_dh_group"></span>**FWP \_ E \_ \_ grupo DH incompatível \_**
</dt> <dd> <dl> <dt>

0x80320031L
</dt> <dt>



O grupo de Diffie-Hellman não é compatível com o tipo de política.


</dt> </dl> </dd> <dt>

<span id="FWP_E_EM_NOT_SUPPORTED"></span><span id="fwp_e_em_not_supported"></span>**FWP \_ E \_ \_ não \_ tem suporte**
</dt> <dd> <dl> <dt>

0x80320032
</dt> <dt>



Uma política IKE não pode conter uma política de modo estendido.


</dt> </dl> </dd> <dt>

<span id="FWP_E_NEVER_MATCH"></span><span id="fwp_e_never_match"></span>**FWP \_ E \_ nunca \_ corresponde**
</dt> <dd> <dl> <dt>

0x80320033
</dt> <dt>



O modelo ou assinatura de enumeração nunca corresponderá a nenhum objeto.


</dt> </dl> </dd> <dt>

<span id="FWP_E_PROVIDER_CONTEXT_MISMATCH"></span><span id="fwp_e_provider_context_mismatch"></span>**Não \_ há \_ \_ correspondência de contexto do provedor fwp E \_**
</dt> <dd> <dl> <dt>

0x80320034
</dt> <dt>



O contexto do provedor é do tipo incorreto.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_PARAMETER"></span><span id="fwp_e_invalid_parameter"></span>**FWP \_ E \_ \_ parâmetro inválido**
</dt> <dd> <dl> <dt>

0x80320035
</dt> <dt>



O parâmetro está incorreto.

Possíveis motivos para esse erro:

-   [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) foi chamado sem definir o sinalizador **FWPM de \_ sinalizador de túnel \_ \_ \_ para \_ ponto** e com condições diferentes de endereço local/remoto.
-   Uma cadeia de caracteres Unicode inválida ou uma cadeia de caracteres Unicode que contém caracteres não imprimíveis.


</dt> </dl> </dd> <dt>

<span id="FWP_E_TOO_MANY_SUBLAYERS"></span><span id="fwp_e_too_many_sublayers"></span>**FWP \_ E \_ \_ muitas \_ subcamadas**
</dt> <dd> <dl> <dt>

0x80320036
</dt> <dt>



O número máximo de subcamadas foi atingido.

A WFP oferece suporte a no máximo 2 6 subcamadas.


</dt> </dl> </dd> <dt>

<span id="FWP_E_CALLOUT_NOTIFICATION_FAILED"></span><span id="fwp_e_callout_notification_failed"></span>**a \_ \_ notificação de texto explicativo fwp E \_ \_ falhou**
</dt> <dd> <dl> <dt>

0x80320037
</dt> <dt>



A função de notificação para um texto explicativo retornou um erro.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_AUTH_TRANSFORM"></span><span id="fwp_e_invalid_auth_transform"></span>**FWP \_ E \_ \_ transformação de autenticação inválida \_**
</dt> <dd> <dl> <dt>

0x80320038
</dt> <dt>



A transformação de autenticação IPsec não é válida.


</dt> </dl> </dd> <dt>

<span id="FWP_E_INVALID_CIPHER_TRANSFORM"></span><span id="fwp_e_invalid_cipher_transform"></span>**FWP \_ E \_ \_ transformação de codificação inválida \_**
</dt> <dd> <dl> <dt>

0x80320039
</dt> <dt>



A transformação de criptografia IPsec não é válida.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Winerror. h</dt> </dl> |



 

 





