---
title: Identificadores de texto explicativo interno (Fwpmu. h)
description: Os identificadores para as funções de texto explicativo que são internas para a WFP (Windows Filtering Platform) são representadas por um GUID. Esses identificadores são definidos da seguinte maneira.
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
ms.openlocfilehash: c21d0428953d8b3e27590b186d931a7d902db377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919119"
---
# <a name="built-in-callout-identifiers"></a>Identificadores de texto explicativo internos

Os identificadores para as funções de texto explicativo que são internas para a WFP (Windows Filtering Platform) são representadas por um GUID. Esses identificadores são definidos da seguinte maneira.

Os sufixos v4 e V6 no final dos identificadores de texto explicativo indicam se o texto explicativo é para a pilha de rede IPv4 ou para a pilha de rede IPv6.

<dl> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**\_Texto explicativo de FWPM de \_ protocolo IPsec \_ \_ \_ v4/FWPM \_ texto explicativo de \_ entrada IP V6 de transporte de \_ saída \_ \_** 
</dt> <dd> <dl> <dt>



Verifica se cada pacote recebido que deve chegar em uma associação de segurança do modo de transporte chega com segurança.

Esse texto explicativo é aplicável na camada de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM \_ balão \_ de \_ transporte de saída IPSec \_ \_ v4/FWPM de \_ transporte de saída do \_ IPSec \_ \_ \_ V6** 
</dt> <dd> <dl> <dt>



Indica ao IPsec o tráfego de saída que deve ser protegido em associações de segurança do modo de transporte.

Esse texto explicativo é aplicável na camada de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**\_Texto explicativo IPSec de entrada do FWPM em balão \_ \_ \_ \_ v4/FWPM de \_ limite de entrada do \_ IPSec \_ \_ \_ V6** 
</dt> <dd> <dl> <dt>



Verifica se cada pacote recebido que deve chegar em uma associação de segurança do modo de túnel chega com segurança.

Esse texto explicativo é aplicável na camada de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**FWPM \_ balão \_ de \_ saída \_ IPSec \_ v4/FWPM \_ de \_ \_ túnel de saída IPSec \_ \_ V6** 
</dt> <dd> <dl> <dt>



Indica ao IPsec o tráfego de saída que deve ser protegido em relação às associações de segurança do modo de túnel.

Esse texto explicativo é aplicável na camada de transporte.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**\_Texto explicativo de \_ encaminhamento IPSec enFWPM \_ Tunnel de \_ entrada \_ \_ v4/FWPM \_ balão de \_ \_ encaminhamento do túnel de \_ entrada \_ \_ V6 do IPSec**
</dt> <dd> <dl> <dt>



Verifica se cada pacote recebido que deve chegar em uma associação de segurança do modo de túnel chega com segurança.

Esse texto explicativo é aplicável na camada de encaminhamento.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**\_Balão de \_ saída de \_ encaminhamento IPSec \_ v4/FWPM de túnel de saída de \_ \_ \_ \_ \_ encaminhamento IPSec \_ \_ \_ V6 do FWPM**
</dt> <dd> <dl> <dt>



Indica ao IPsec o tráfego de saída que deve ser protegido em uma associação de segurança do modo de túnel.

Esse texto explicativo é aplicável na camada de encaminhamento.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM \_ texto explicativo \_ IPSec de \_ entrada \_ Iniciar \_ segurança \_ v4/FWPM \_ texto explicativo \_ IPSec de \_ entrada \_ Iniciar \_ \_ V6 de segurança** 
</dt> <dd> <dl> <dt>



Verifica se cada conexão de entrada que deve chegar à segurança chega segura.

Esse texto explicativo é aplicável na camada de aceitação ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM \_ texto explicativo \_ IPSec de \_ túnel de entrada \_ \_ Ale \_ Accept \_ v4/FWPM \_ texto EXPLICAtivo de \_ \_ entrada Ale de túnel de saída do IPSec \_ \_ \_ \_**
</dt> <dd> <dl> <dt>



Permite os pacotes IP-in-IP do modo de túnel IPsec quando eles são classificados na camada de aceitação ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**\_Texto explicativo FWPM de \_ \_ conexão Ale de IPSec \_ \_ /FWPM \_ texto explicativo de \_ \_ conexão Ale IPSec \_ \_ V6**
</dt> <dd> <dl> <dt>



Aplica modificadores de política IPsec a aplicativos cliente.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM \_ balão \_ IPSec \_ DOSP \_ Forward \_ v4/FWPM \_ balão \_ IPSec \_ DOSP \_ Forward \_ V6**
</dt> <dd> <dl> <dt>



Sinaliza à proteção de DoS IPsec que o tráfego precisa ser verificado quanto ao DoS possíveis e pode precisar ter uma taxa limitada.

> [!Note]  
> Disponível somente no Windows 7 e no Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**\_Texto explicativo FWPM \_ camada de \_ transporte WFP \_ \_ v4 \_ \_ soltar/FWPM \_ balão de camada de \_ \_ transporte WFP \_ \_ V6 \_ \_ drop silencioso**
</dt> <dd> <dl> <dt>



Implementa a filtragem de modo furtivo descartando silenciosamente todos os pacotes de entrada para os quais o TCP não tem um ponto de extremidade de escuta.

Esse texto explicativo é aplicável na camada de descarte de transporte de entrada.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**\_Texto explicativo FWPM \_ TCP \_ Chimney \_ \_ Layer \_ v4/FWPM \_ texto explicativo \_ TCP \_ Chimney \_ Connect \_ camada \_ V6**
</dt> <dd> <dl> <dt>



Habilita ou desabilita o descarregamento de Chimney TCP para cada conexão de saída.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM \_ balão \_ TCP \_ Chimney \_ Accept da \_ camada \_ v4/FWPM \_ texto explicativo \_ TCP \_ Chimney \_ aceito \_ camada \_ V6**
</dt> <dd> <dl> <dt>



Habilita ou desabilita o descarregamento de Chimney TCP para cada conexão de entrada.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM \_ balão \_ set \_ opções \_ auth \_ Connect \_ Layer \_ v4/FWPM \_ texto explicativo \_ definir \_ opções \_ auth \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Define as opções de classificação em fluxos de saída.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM \_ callout \_ define \_ opções \_ auth \_ recv \_ Accept \_ camada \_ v4/FWPM \_ texto explicativo \_ definir \_ opções \_ auth \_ recv \_ aceitar \_ camada \_ V6**
</dt> <dd> <dl> <dt>



Define opções de classificação em fluxos de entrada.

> [!Note]  
> Disponível somente no Windows 8 e no Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM \_ balão \_ reservado \_ auth \_ Connect \_ Layer \_ v4/FWPM \_ called \_ \_ auth \_ Connect \_ Layer \_ V6**
</dt> <dd> <dl> <dt>



Esse identificador é reservado para uso interno.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**\_Texto explicativo de borda transversal de chamada Ale de FWPM Call \_ \_ \_ \_ \_ V6/FWPM \_ balão de \_ \_ escuta Ale TEREDO \_ \_ V6**
</dt> <dd> <dl> <dt>



Sinaliza para o serviço Teredo que um aplicativo requer um endereço Teredo.

> [!Note]  
> Para o Windows 7 e versões posteriores, use **FWPM \_ callout de chamada \_ Ale de borda \_ transversal \_ \_ \_**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM \_ balão \_ de \_ atribuição de recurso Ale de borda transversal \_ \_ \_ \_ V6/FWPM \_ balão de atribuição de \_ \_ recursos Ale TEREDO \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Sinaliza para o serviço Teredo que um aplicativo requer um endereço Teredo.

> [!Note]  
> Para o Windows 7 e posterior, use **FWPM \_ called \_ \_ Ale Edge Traversal de \_ \_ atribuição de recursos \_ \_**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM \_ de \_ \_ atribuição de recursos Ale de borda transversal de chamada de texto para o \_ \_ \_ \_ v4** 
</dt> <dd> <dl> <dt>



Esse identificador é reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM \_ texto explicativo de \_ passagem Ale de borda de chamada \_ \_ \_ \_ v4**
</dt> <dd> <dl> <dt>



Esse identificador é reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM \_ balão \_ TCP \_ modelos de \_ conexão de \_ camada \_ v4/FWPM de \_ texto explicativo \_ modelos TCP de camada de \_ \_ conexão \_ \_ V6**
</dt> <dd> <dl> <dt>



Aplica configurações de modelo TCP para conexões de saída correspondentes.

> [!Note]  
> Disponível somente no Windows 8 e no Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**\_Modelos de TCP de texto explicativo FWPM \_ \_ \_ aceitar \_ camada \_ v4/FWPM os \_ \_ \_ modelos TCP \_ aceitam \_ camada \_ V6**
</dt> <dd> <dl> <dt>



Aplica configurações de modelo TCP para conexões de entrada correspondentes.

> [!Note]  
> Disponível somente no Windows 8 e no Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





