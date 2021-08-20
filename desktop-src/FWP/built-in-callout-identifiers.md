---
title: Identificadores de callout integrados (Fwpmu.h)
description: Os identificadores para as funções de chamada que são criadas na WFP (plataforma de filtragem Windows) são representados por um GUID. Esses identificadores são definidos da seguinte forma.
ms.assetid: b283cb2e-7f82-4d44-982a-38499504e3bc
topic_type:
- apiref
api_name:
- FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4 / FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6
- FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4 / FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6
- FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4 / FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6
- FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP / FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP
- FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6
- FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6 / FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4
- FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d430f44e6e72f575d5e2ff0fd30681c04e81892f0438f0508be994d53c1643e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151422"
---
# <a name="built-in-callout-identifiers"></a>Identificadores de callout integrados

Os identificadores para as funções de chamada que são criadas na WFP (plataforma de filtragem Windows) são representados por um GUID. Esses identificadores são definidos da seguinte forma.

Os sufixos V4 e V6 no final dos identificadores de chamada indicam se o callout é para a pilha de rede IPv4 ou para a pilha de rede IPv6.

<dl> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ TRANSPORT \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ INBOUND TRANSPORT \_ \_ V6** 
</dt> <dd> <dl> <dt>



Verifica se cada pacote recebido que deve chegar em uma associação de segurança do modo de transporte chega com segurança.

Esse texto explicação é aplicável na camada de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND \_ TRANSPORT \_ V4 /FWPM \_ CALLOUT \_ IPSEC \_ \_ OUTBOUND TRANSPORT \_ V6** 
</dt> <dd> <dl> <dt>



Indica para IPsec o tráfego de saída que deve ser protegido por associações de segurança do modo de transporte.

Esse texto explicação é aplicável na camada de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ TUNNEL \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ INBOUND TUNNEL \_ \_ V6** 
</dt> <dd> <dl> <dt>



Verifica se cada pacote recebido que deve chegar em uma associação de segurança no modo de túnel chega com segurança.

Esse texto explicação é aplicável na camada de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**TÚNEL DE SAÍDA \_ \_ IPSEC DE SAÍDA \_ \_ \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ \_ \_ V6** 
</dt> <dd> <dl> <dt>



Indica para IPsec o tráfego de saída que deve ser protegido por associações de segurança no modo de túnel.

Esse texto explicação é aplicável na camada de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ FORWARD \_ INBOUND TUNNEL \_ \_ V4/FWPM \_ CALLOUT \_ IPSEC FORWARD \_ \_ INBOUND TUNNEL \_ \_ V6**
</dt> <dd> <dl> <dt>



Verifica se cada pacote recebido que deve chegar em uma associação de segurança no modo de túnel chega com segurança.

Esse texto explicação é aplicável na camada de encaminhamento.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ FORWARD \_ OUTBOUND TUNNEL \_ \_ V4/FWPM \_ CALLOUT \_ IPSEC FORWARD \_ \_ \_ OUTBOUND TUNNEL \_ V6**
</dt> <dd> <dl> <dt>



Indica para IPsec o tráfego de saída que deve ser protegido por uma associação de segurança no modo de túnel.

Esse texto explicação é aplicável na camada de encaminhamento.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ INITIATE SECURE \_ \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ INBOUND INITIATE SECURE \_ \_ \_ V6** 
</dt> <dd> <dl> <dt>



Verifica se cada conexão de entrada que deve chegar segura chega com segurança.

Esse texto explicação é aplicável na camada de aceitação ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ INBOUND \_ TUNNEL \_ ALE ACCEPT \_ \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ INBOUND TUNNEL \_ \_ ALE ACCEPT \_ \_ V6**
</dt> <dd> <dl> <dt>



Permite os pacotes IP no IP do modo de túnel IPsec quando eles são classificados na camada de aceitação ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ ALE \_ CONNECT \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ ALE CONNECT \_ \_ V6**
</dt> <dd> <dl> <dt>



Aplica modificadores de política IPsec a aplicativos cliente.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM \_ CALLOUT \_ IPSEC \_ DOSP \_ FORWARD \_ V4/FWPM \_ CALLOUT \_ IPSEC \_ DOSP FORWARD \_ \_ V6**
</dt> <dd> <dl> <dt>



Sinaliza à Proteção contra DoS IPsec que o tráfego precisa ser verificado quanto a possíveis DoS e pode precisar ser limitado por taxa.

> [!Note]  
> Disponível somente no Windows 7 e Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM \_ CALLOUT \_ WFP \_ TRANSPORT LAYER \_ \_ V4 SILENT DROP \_ \_ /FWPM \_ CALLOUT \_ WFP TRANSPORT LAYER \_ \_ \_ V6 SILENT \_ \_ DROP**
</dt> <dd> <dl> <dt>



Implementa a filtragem de modo furtivo, soltando silenciosamente todos os pacotes de entrada para os quais o TCP não tem um ponto de extremidade de escuta.

Esse texto explicação é aplicável na camada de descarte de transporte de entrada.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM \_ CALLOUT \_ TCP \_ LAYER CONNECT \_ \_ LAYER \_ V4/FWPM \_ CALLOUT \_ TCP LAYER CONNECT LAYER \_ \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Habilita ou desabilita o descarregaamento de conexões TCP para cada conexão de saída.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM \_ CALLOUT \_ TCP \_ LAYER ACCEPT LAYER \_ \_ \_ V4/FWPM \_ CALLOUT \_ TCP LAYER ACCEPT \_ LAYER \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Habilita ou desabilita o descarregado de suáb TCP para cada conexão de entrada.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**OPÇÕES DO CONJUNTO DE TEXTO DE CHAMADA DO FWPM \_ \_ \_ \_ AUTH \_ CONNECT \_ LAYER \_ V4/FWPM \_ \_ \_ \_ \_ \_ \_ OPÇÕES DO CONJUNTO DE CHAMADA DA CAMADA DE CONEXÃO DE AUTH V6**
</dt> <dd> <dl> <dt>



Define as opções de classificação em fluxos de saída.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**OPÇÕES DO CONJUNTO DE TEXTO DE CHAMADA DO FWPM \_ \_ \_ \_ AUTH \_ RECV \_ ACCEPT LAYER \_ \_ V4/FWPM \_ OPÇÕES \_ \_ \_ \_ \_ \_ \_ DO CONJUNTO DE CHAMADA AUTH RECV ACCEPT LAYER V6**
</dt> <dd> <dl> <dt>



Define as opções de classificação em fluxos de entrada.

> [!Note]  
> Disponível somente em Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM \_ CALLOUT \_ RESERVED \_ AUTH \_ CONNECT LAYER \_ \_ V4/FWPM \_ CALLOUT \_ RESERVED \_ AUTH \_ CONNECT LAYER \_ \_ V6**
</dt> <dd> <dl> <dt>



Esse identificador é reservado para uso interno.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE LISTEN \_ \_ V6/FWPM \_ CALLOUT \_ TEREDO \_ ALE LISTEN \_ \_ V6**
</dt> <dd> <dl> <dt>



Sinaliza ao serviço Teredo que um aplicativo requer um endereço Teredo.

> [!Note]  
> Para Windows 7 e posterior, use **FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ LISTEN \_ V6**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V6/FWPM \_ CALLOUT \_ TEREDO \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Sinaliza ao serviço Teredo que um aplicativo requer um endereço Teredo.

> [!Note]  
> Para Windows 7 e posterior, use **FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ RESOURCE ASSIGNMENT \_ \_ V6**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ RESOURCE \_ ASSIGNMENT \_ V4** 
</dt> <dd> <dl> <dt>



Esse identificador é reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM \_ CALLOUT \_ EDGE \_ TRAVERSAL \_ ALE \_ LISTEN \_ V4**
</dt> <dd> <dl> <dt>



Esse identificador é reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**MODELOS DE TCP DO \_ \_ FWPM CALLOUT CONNECT \_ LAYER \_ \_ \_ V4/FWPM \_ CALLOUT \_ TCP \_ TEMPLATES CONNECT LAYER \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Aplica as configurações de modelo TCP para correspondência de conexões de saída.

> [!Note]  
> Disponível somente em Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**MODELOS TCP DE TEXTO FWPM ACEITAM MODELOS TCP DE CAMADA \_ \_ \_ \_ \_ \_ V4/FWPM \_ \_ \_ \_ \_ QUE ACEITAM CAMADA \_ V6**
</dt> <dd> <dl> <dt>



Aplica as configurações de modelo TCP para correspondência de conexões de entrada.

> [!Note]  
> Disponível somente em Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Fwpmu.h</dt> </dl> |



 

 





