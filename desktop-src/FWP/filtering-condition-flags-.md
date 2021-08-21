---
title: Filtrando sinalizadores de condição (Fwptypes. h)
description: os sinalizadores de condição de filtragem da WFP (plataforma de filtragem Windows) são representados por um campo de bits.
ms.assetid: fe879479-331d-42ef-ac2f-634f0c13c21d
topic_type:
- apiref
api_name:
- FWP_CONDITION_FLAG_IS_LOOPBACK
- FWP_CONDITION_FLAG_IS_IPSEC_SECURED
- FWP_CONDITION_FLAG_IS_REAUTHORIZE
- FWP_CONDITION_FLAG_IS_WILDCARD_BIND
- FWP_CONDITION_FLAG_IS_RAW_ENDPOINT
- FWP_CONDITION_FLAG_IS_FRAGMENT
- FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP
- FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY
- FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY
- FWP_CONDITION_FLAG_IS_IMPLICIT_BIND
- FWP_CONDITION_FLAG_IS_REASSEMBLED
- FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED
- FWP_CONDITION_FLAG_IS_PROMISCUOUS
- FWP_CONDITION_FLAG_IS_AUTH_FW
- FWP_CONDITION_FLAG_IS_RECLASSIFY
- FWP_CONDITION_FLAG_IS_PROXY_CONNECTION
- FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_RESERVED
- FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE
- FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING
- FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION
- FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION
- FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC
- FWP_CONDITION_L2_IS_NATIVE_ETHERNET
- FWP_CONDITION_L2_IS_WIFI
- FWP_CONDITION_L2_IS_MOBILE_BROADBAND
- FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA
- FWP_CONDITION_L2_IS_VM2VM
- FWP_CONDITION_L2_IS_MALFORMED_PACKET
- FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP
- FWP_CONDITION_L2_IF_CONNECTOR_PRESENT
api_location:
- fwptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a43ae080a9ef1c17baa262cc1154f9ae89a837f0ec6f6919d80c22376f3b995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150889"
---
# <a name="filtering-condition-flags"></a>Filtrando sinalizadores de condição

os sinalizadores de condição de filtragem da WFP (plataforma de filtragem Windows) são representados por um campo de bits.

Esses sinalizadores e as camadas de filtragem em que podem ser usados são definidos da seguinte maneira.

<dl> <dt>

<span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ loopback**
</dt> <dd> <dl> <dt>



Testa se o tráfego de rede é tráfego de loopback.

Filtrando camadas:

-   FWPM de \_ entrada da camada de \_ \_ IPPACKET \_ V {4 \| 6}
-   FWPM de \_ saída da camada de \_ \_ IPPACKET \_ V {4 \| 6}
-   \_Transporte de entrada da camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Transporte de saída da camada FWPM \_ \_ \_ V {4 \| 6}
-   Fluxo da camada de FWPM \_ \_ \_ {v4 \| 6}
    > [!Note]  
    > disponível somente no Windows Server 2008, Windows Vista com SP1 e posterior.

     

-   \_Erro de ICMP de entrada na camada FWPM \_ \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > disponível somente no Windows Server 2008, Windows Vista com SP1 e posterior.

     

-   Erro de ICMP de saída de camada de FWPM \_ \_ \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > disponível somente no Windows Server 2008, Windows Vista com SP1 e posterior.

     

-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}
-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > disponível somente no Windows Server 2008, Windows Vista com SP1 e posterior.

     

-   O \_ fluxo Ale da camada FWPM foi \_ \_ \_ estabelecido \_ V {4 \| 6}
    > [!Note]  
    > disponível somente no Windows Server 2008, Windows Vista com SP1 e posterior.

     


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ protegido por IPsec \_**
</dt> <dd> <dl> <dt>



Testa se o tráfego de rede é protegido pelo IPsec.

Filtrando camadas:

-   FWPM de \_ entrada da camada de \_ \_ IPPACKET \_ V {4 \| 6}
-   \_Transporte de entrada da camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}
-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ reautorizado**
</dt> <dd> <dl> <dt>



Os testes de uma política mudam em oposição a uma nova conexão.

Filtrando camadas:

-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}
-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**o \_ sinalizador de condição fwp \_ é uma \_ \_ \_ Associação curinga**
</dt> <dd> <dl> <dt>



Testa se o aplicativo especificou um endereço curinga ao ligar a um endereço de rede local.

Camada de filtragem:

-   \_Atribuição de \_ recursos Ale de camada FWPM \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**o \_ sinalizador de condição fwp \_ é um ponto de \_ \_ \_ extremidade bruto**
</dt> <dd> <dl> <dt>



Testa se o ponto de extremidade local que está enviando e recebendo tráfego é um ponto de extremidade bruto.

Filtrando camadas:

-   \_Transporte de entrada da camada FWPM \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > disponível somente no Windows Server 2008, Windows Vista com SP1 e posterior.

     

-   \_Transporte de saída da camada FWPM \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > disponível somente no Windows Server 2008, Windows Vista com SP1 e posterior.

     

-   \_Dados de \_ datagrama de camada FWPM \_ \_ {v4 \| 6}
    > [!Note]  
    > disponível somente no Windows Server 2008, Windows Vista com SP1 e posterior.

     

-   \_Atribuição de \_ recursos Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}
-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ fragmento**
</dt> <dd> <dl> <dt>



Testa se a \_ estrutura da lista de buffers líquida \_ passada para um driver de texto explicativo é um fragmento de pacote IP.

Filtrando camadas:

-   FWPM de \_ entrada da camada de \_ \_ IPPACKET \_ V {4 \| 6}
-   FWPM da \_ camada de \_ entrada \_ IPPACKET \_ V {4 \| 6} \_ descartar


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**o \_ sinalizador de condição fwp \_ é um \_ \_ grupo de fragmentos \_**
</dt> <dd> <dl> <dt>



Testa se a \_ estrutura de lista de buffers de rede \_ passada para um driver de texto explicativo descreve uma lista vinculada de fragmentos de pacote.

Camada de filtragem:

-   \_Camada FWPM \_ IPFORWARD \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**o \_ sinalizador de condição fwp \_ é o \_ \_ IPSec \_ NATT \_ reclassificar**
</dt> <dd> <dl> <dt>



Indica que o mesmo pacote está sendo reclassificado na camada de transporte, quando a Shim de NAT do IPsec traduz o valor da porta remota.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**o \_ sinalizador de condição fwp \_ \_ requer \_ \_ classificação Ale**
</dt> <dd> <dl> <dt>



Indica que o pacote será reclassificado na camada de recepção/aceitação ALE.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**o \_ sinalizador de condição fwp \_ é uma \_ \_ \_ associação implícita**
</dt> <dd> <dl> <dt>



testa se Windows soquetes está executando uma associação implícita.

disponível somente no Windows Vista e no Windows Server 2008.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ remontado**
</dt> <dd> <dl> <dt>



Testa se o pacote foi remontado.

> [!Note]  
> disponível somente no Windows Server 2008, Windows Vista com SP1 e posterior.

 

Camada de filtragem:

-   FWPM de \_ entrada da camada de \_ \_ IPPACKET \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**o \_ sinalizador de condição fwp \_ é um nome de \_ \_ \_ aplicativo \_ especificado**
</dt> <dd> <dl> <dt>



Testa se o nome do computador par ao qual o aplicativo está esperando se conectar foi recebido por meio de uma API como [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) e não obtido por meio da heurística de cache.

> [!Note]  
> disponível somente no Windows Server 2008 R2, Windows 7 e posterior.

 

Camada de filtragem:

-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ promíscuo**
</dt> <dd> <dl> <dt>



Reservado.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ FW de autenticação \_**
</dt> <dd> <dl> <dt>



Testa se a conexão é autenticada de ponta a ponta, mesmo que os pacotes individuais não tenham sido verificados.

> [!Note]  
> disponível somente no Windows Server 2008 R2, Windows 7 e posterior.

 

Camada de filtragem:

-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ reclassificado**
</dt> <dd> <dl> <dt>



Testa se o mecanismo de filtragem está reclassificando uma associação ou solicitação de escuta anterior.

> [!Note]  
> disponível somente no Windows Server 2008 R2, Windows 7 e posterior.

 

Camada de filtragem:

-   \_Escuta de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Atribuição de \_ recursos Ale de camada FWPM \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**o \_ sinalizador de condição fwp \_ é uma \_ \_ \_ conexão proxy**
</dt> <dd> <dl> <dt>



Testa se a conexão usa um proxy.

> [!Note]  
> disponível somente em Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**o \_ sinalizador de condição fwp \_ é o \_ \_ loopback do APPCONTAINER \_**
</dt> <dd> <dl> <dt>



Testa se o tráfego de rede é o tráfego de loopback do contêiner de aplicativo.

> [!Note]  
> disponível somente em Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**o \_ sinalizador de condição fwp não \_ é um \_ \_ \_ loopback de APPCONTAINER \_**
</dt> <dd> <dl> <dt>



Testa se o tráfego de rede é um tráfego de loopback de contêiner não aplicativo.

> [!Note]  
> disponível somente em Windows 8 e Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**O SINALIZADOR DE CONDIÇÃO FWP \_ \_ ESTÁ \_ \_ RESERVADO**
</dt> <dd> <dl> <dt>



Reservado.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**O SINALIZADOR DE \_ CONDIÇÃO FWP \_ ESTÁ \_ \_ ACANDO A \_ AUTORIZAÇÃO DA \_ POLÍTICA**
</dt> <dd> <dl> <dt>



Indica que a classificação atual está sendo executada para manter a intenção de um aplicativo redirecionado Windows Store para se conectar a um host especificado. Essa classificação conterá os mesmos valores de campo classificáveis como se o aplicativo nunca tivesse sido redirecionado. O sinalizador também indica que uma classificação futura será invocada para corresponder ao destino redirecionado efetivo. Se o aplicativo for redirecionado para um serviço proxy para inspeção, isso também significa que uma classificação futura será invocada na conexão de proxy. Os drivers de chamada geralmente devem permitir essa classificação.

> [!Note]  
> Disponível somente em Windows 8 e Windows Server 2012.

 

Camada de filtragem:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}


</dt> </dl> </dd> </dl>

Os sinalizadores a seguir especificam o motivo para autorizar uma conexão autorizada anteriormente. Esses sinalizadores e as camadas de filtragem em que podem ser usados são definidos da seguinte forma.

> [!Note]  
> Essas condições de filtragem estão disponíveis somente no Windows Server 2008 R2, Windows 7 e posterior.

 

<dl> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**FWP \_ CONDITION \_ REAUTHORIZE \_ REASON \_ POLICY \_ CHANGE**
</dt> <dd> <dl> <dt>



Indica que a conexão foi autorizada de acordo com a adoção ou remoção dos filtros.

Camada de filtragem:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**FWP \_ CONDITION \_ REAUTHORIZE \_ REASON \_ NEW \_ ARRIVAL \_ INTERFACE**
</dt> <dd> <dl> <dt>



Indica que o pacote chegou de uma interface desconhecida.

Camada de filtragem:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**FWP \_ CONDITION \_ REAUTHORIZE \_ REASON \_ NEW \_ NEXTHOP \_ INTERFACE**
</dt> <dd> <dl> <dt>



Indica que o pacote partirá de uma interface desconhecida.

Camada de filtragem:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**PASSAGEM DE PERFIL DE MOTIVO \_ \_ DE AUTORIZAÇÃO DE \_ \_ CONDIÇÃO FWP \_**
</dt> <dd> <dl> <dt>



Indica que o pacote passou por interfaces de mais de uma categoria de rede.

Camada de filtragem:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**FWP \_ CONDITION \_ REAUTHORIZE \_ REASON \_ CLASSIFY \_ COMPLETION**
</dt> <dd> <dl> <dt>



Indica que uma conexão mantida anteriormente agora está sendo permitida para ser concluída.

Camada de filtragem:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**FWP \_ CONDITION \_ REAUTHORIZE \_ REASON \_ IPSEC \_ PROPERTIES \_ CHANGED**
</dt> <dd> <dl> <dt>



Indica que as propriedades IPsec foram alteradas ou que a conexão foi alterada de texto não claro para uma conexão segura.

Camada de filtragem:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**FWP \_ CONDITION \_ REAUTHORIZE \_ REASON \_ MID \_ STREAM \_ INSPECTION**
</dt> <dd> <dl> <dt>



Indica que uma conexão TCP estabelecida anteriormente agora está sendo inspecionada.

Camada de filtragem:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**FWP \_ CONDITION \_ REAUTHORIZE \_ REASON \_ SOCKET \_ PROPERTY \_ CHANGED**
</dt> <dd> <dl> <dt>



Indica que as propriedades de soquete foram definidas depois que uma conexão foi autorizada e estabelecida.

Camada de filtragem:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**FWP \_ CONDITION \_ REAUTHORIZE \_ REASON \_ NEW \_ INBOUND \_ MCAST \_ BCAST \_ PACKET**
</dt> <dd> <dl> <dt>



Indica que novos pacotes de multicast ou difusão de entrada estão sendo autorizados de novo em callouts ALE \_ RECV \_ ACCEPT.

Camada de filtragem:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 \| 6}


</dt> </dl> </dd> </dl>

Os sinalizadores a seguir especificam propriedades de soquete que estão relacionadas a se um aplicativo deseja receber o tráfego de Travessia de Borda. Esses sinalizadores e as camadas de filtragem em que podem ser usados são definidos da seguinte forma.

> [!Note]  
> Essas condições de filtragem estão disponíveis somente no Windows Server 2008 R2, Windows 7 e posterior.

 

<dl> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**O SINALIZADOR DE PROPRIEDADE DE SOQUETE DE CONDIÇÃO FWP \_ \_ É \_ \_ \_ \_ \_ RPC DE PORTA DO \_ SISTEMA**
</dt> <dd> <dl> <dt>



Indica que o aplicativo está se comunicando com uma porta RPC dinâmica.

Camada de filtragem:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ LISTEN \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**SINALIZADOR DE PROPRIEDADE \_ DE \_ SOQUETE DE CONDIÇÃO FWP \_ PERMITIR TRÁFEGO DE \_ \_ \_ \_ BORDA**
</dt> <dd> <dl> <dt>



Indica que o aplicativo deseja receber tráfego específico da borda.

Camada de filtragem:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ LISTEN \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**SINALIZADOR DE PROPRIEDADE \_ DE \_ SOQUETE DE CONDIÇÃO FWP \_ NEGAR TRÁFEGO DE \_ \_ \_ \_ BORDA**
</dt> <dd> <dl> <dt>



Indica que o aplicativo não deseja receber ou processar tráfego específico da borda.

Camada de filtragem:

-   FWPM \_ LAYER \_ ALE \_ AUTH \_ LISTEN \_ V{4 \| 6}
-   FWPM \_ LAYER \_ ALE RESOURCE ASSIGNMENT \_ \_ \_ V{4 \| 6}


</dt> </dl> </dd> </dl>

Os sinalizadores a seguir especificam detalhes de conexão relacionados à filtragem L2.

> [!Note]  
> Essas condições de filtragem estão disponíveis somente Windows 8 e Windows Server 2012.

 

<dl> <dt>

<span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**A CONDIÇÃO DE FWP \_ \_ L2 \_ É ETHERNET \_ \_ NATIVA**
</dt> <dd> <dl> <dt>



Indica que a conexão é Ethernet nativa.

Camada de filtragem:

-   ETHERNET DE QUADRO \_ MAC DE \_ ENTRADA DA \_ \_ CAMADA FWPM \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   ETHERNET DE QUADRO \_ MAC DE SAÍDA DA \_ CAMADA \_ \_ FWPM \_
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**FWP \_ CONDITION \_ L2 \_ IS \_ WIFI**
</dt> <dd> <dl> <dt>



Indica que a conexão é Wi-Fi.

Camada de filtragem:

-   ETHERNET DE QUADRO \_ MAC DE \_ ENTRADA DA \_ \_ CAMADA FWPM \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   ETHERNET DE QUADRO \_ MAC DE SAÍDA DA \_ CAMADA \_ \_ FWPM \_
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**A CONDIÇÃO FWP \_ \_ L2 \_ É BANDA \_ LARGA \_ MÓVEL**
</dt> <dd> <dl> <dt>



Indica que a conexão é de banda larga móvel.

Camada de filtragem:

-   ETHERNET DE QUADRO \_ MAC DE \_ ENTRADA DA \_ \_ CAMADA FWPM \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   ETHERNET DE QUADRO \_ MAC DE SAÍDA DA \_ CAMADA \_ \_ FWPM \_
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**FWP \_ CONDITION \_ L2 \_ IS \_ WIFI \_ DIRECT \_ DATA**
</dt> <dd> <dl> <dt>



Indica que a conexão é Wi-Fi Direct.

Camada de filtragem:

-   ETHERNET DE QUADRO \_ MAC DE \_ ENTRADA DA \_ \_ CAMADA FWPM \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   ETHERNET DE QUADRO \_ MAC DE SAÍDA DA \_ CAMADA \_ \_ FWPM \_
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**FWP \_ CONDITION \_ L2 \_ IS \_ VM2VM**
</dt> <dd> <dl> <dt>



Indica que a conexão está entre máquinas virtuais.

Camada de filtragem:

-   ETHERNET DE QUADRO \_ MAC DE \_ ENTRADA DA \_ \_ CAMADA FWPM \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   ETHERNET DE QUADRO \_ MAC DE SAÍDA DA \_ CAMADA \_ \_ FWPM \_
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**A CONDIÇÃO DE FWP \_ \_ L2 \_ É UM PACOTE \_ \_ MALFORMADO**
</dt> <dd> <dl> <dt>



Indica que um pacote parece estar malformado.

Camada de filtragem:

-   ETHERNET DE QUADRO \_ MAC DE \_ ENTRADA DA \_ \_ CAMADA FWPM \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   ETHERNET DE QUADRO \_ MAC DE SAÍDA DA \_ CAMADA \_ \_ FWPM \_
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**FWP \_ CONDITION \_ L2 \_ IS \_ IP \_ FRAGMENT \_ GROUP**
</dt> <dd> <dl> <dt>



Indica um grupo de fragmentos de pacote IP.

Camada de filtragem:

-   ETHERNET DE QUADRO \_ MAC DE \_ ENTRADA DA \_ \_ CAMADA FWPM \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   ETHERNET DE QUADRO \_ MAC DE SAÍDA DA \_ CAMADA \_ \_ FWPM \_
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**CONDIÇÃO FWP \_ \_ L2 \_ SE O CONECTOR \_ ESTIVER \_ PRESENTE**
</dt> <dd> <dl> <dt>



Indica que um conector está presente.

Camada de filtragem:

-   ETHERNET DE QUADRO \_ MAC DE \_ ENTRADA DA \_ \_ CAMADA FWPM \_
-   FWPM \_ LAYER \_ INBOUND \_ MAC \_ FRAME \_ NATIVE
-   ETHERNET DE QUADRO \_ MAC DE SAÍDA DA \_ CAMADA \_ \_ FWPM \_
-   FWPM \_ LAYER \_ OUTBOUND \_ MAC \_ FRAME \_ NATIVE


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Fwptypes.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Filtrando identificadores de camada**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

