---
title: Filtrando sinalizadores de condição (Fwptypes. h)
description: Os sinalizadores de condição de filtragem da WFP (Windows Filtering Platform) são representados por um campo de bits.
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
ms.openlocfilehash: 6c88fa56f37332d52ed31f5ef042c5064a82ac4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645062"
---
# <a name="filtering-condition-flags"></a>Filtrando sinalizadores de condição

Os sinalizadores de condição de filtragem da WFP (Windows Filtering Platform) são representados por um campo de bits.

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
    > Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.

     

-   \_Erro de ICMP de entrada na camada FWPM \_ \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.

     

-   Erro de ICMP de saída de camada de FWPM \_ \_ \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.

     

-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}
-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.

     

-   O \_ fluxo Ale da camada FWPM foi \_ \_ \_ estabelecido \_ V {4 \| 6}
    > [!Note]  
    > Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.

     


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
    > Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.

     

-   \_Transporte de saída da camada FWPM \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.

     

-   \_Dados de \_ datagrama de camada FWPM \_ \_ {v4 \| 6}
    > [!Note]  
    > Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.

     

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



Testa se o Windows Sockets está executando uma ligação implícita.

Disponível apenas no Windows Vista e no Windows Server 2008.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ remontado**
</dt> <dd> <dl> <dt>



Testa se o pacote foi remontado.

> [!Note]  
> Disponível apenas no Windows Server 2008, Windows Vista com SP1 e posterior.

 

Camada de filtragem:

-   FWPM de \_ entrada da camada de \_ \_ IPPACKET \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**o \_ sinalizador de condição fwp \_ é um nome de \_ \_ \_ aplicativo \_ especificado**
</dt> <dd> <dl> <dt>



Testa se o nome do computador par ao qual o aplicativo está esperando se conectar foi recebido por meio de uma API como [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) e não obtido por meio da heurística de cache.

> [!Note]  
> Disponível apenas no Windows Server 2008 R2, Windows 7 e posterior.

 

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
> Disponível apenas no Windows Server 2008 R2, Windows 7 e posterior.

 

Camada de filtragem:

-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**o \_ sinalizador de condição fwp \_ \_ é \_ reclassificado**
</dt> <dd> <dl> <dt>



Testa se o mecanismo de filtragem está reclassificando uma associação ou solicitação de escuta anterior.

> [!Note]  
> Disponível apenas no Windows Server 2008 R2, Windows 7 e posterior.

 

Camada de filtragem:

-   \_Escuta de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Atribuição de \_ recursos Ale de camada FWPM \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**o \_ sinalizador de condição fwp \_ é uma \_ \_ \_ conexão proxy**
</dt> <dd> <dl> <dt>



Testa se a conexão usa um proxy.

> [!Note]  
> Disponível somente no Windows 8 e no Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**o \_ sinalizador de condição fwp \_ é o \_ \_ loopback do APPCONTAINER \_**
</dt> <dd> <dl> <dt>



Testa se o tráfego de rede é o tráfego de loopback do contêiner de aplicativo.

> [!Note]  
> Disponível somente no Windows 8 e no Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**o \_ sinalizador de condição fwp não \_ é um \_ \_ \_ loopback de APPCONTAINER \_**
</dt> <dd> <dl> <dt>



Testa se o tráfego de rede é um tráfego de loopback de contêiner não aplicativo.

> [!Note]  
> Disponível somente no Windows 8 e no Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**o \_ sinalizador de condição fwp \_ \_ está \_ reservado**
</dt> <dd> <dl> <dt>



Reservado.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**o \_ sinalizador de condição fwp \_ \_ está \_ respeitando a \_ política de \_ autorização**
</dt> <dd> <dl> <dt>



Indica que a classificação atual está sendo executada para honrar a intenção de um aplicativo Redirecionado da Windows Store para se conectar a um host especificado. Essa classificação conterá os mesmos valores de campo classificáveis como se o aplicativo nunca fosse Redirecionado. O sinalizador também indica que uma classificação futura será invocada para corresponder ao destino Redirecionado efetivo. Se o aplicativo for Redirecionado para um serviço de proxy para inspeção, isso também significará que uma classificação futura será invocada na conexão de proxy. Os drivers de texto explicativo geralmente devem permitir essa classificação.

> [!Note]  
> Disponível somente no Windows 8 e no Windows Server 2012.

 

Camada de filtragem:

-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

Os sinalizadores a seguir especificam o motivo para a Reautorização de uma conexão autorizada anteriormente. Esses sinalizadores e as camadas de filtragem em que podem ser usados são definidos da seguinte maneira.

> [!Note]  
> Essas condições de filtragem estão disponíveis apenas no Windows Server 2008 R2, Windows 7 e posterior.

 

<dl> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**FWP \_ condição de \_ reautorizar \_ alteração de política de motivo \_ \_**
</dt> <dd> <dl> <dt>



Indica que a conexão foi reautorizada devido a filtros sendo adicionados ou removidos.

Camada de filtragem:

-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**FWP \_ condição de \_ reautorizar \_ motivo \_ nova \_ interface de chegada \_**
</dt> <dd> <dl> <dt>



Indica que o pacote chegou de uma interface desconhecida.

Camada de filtragem:

-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**FWP \_ condição de \_ reautorizar \_ motivo \_ nova \_ \_ interface NEXTHOP**
</dt> <dd> <dl> <dt>



Indica que o pacote será desparte de uma interface desconhecida.

Camada de filtragem:

-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**FWP \_ condição de \_ Reautorização de \_ perfil de motivo \_ \_ cruzado**
</dt> <dd> <dl> <dt>



Indica que o pacote passou por interfaces de mais de uma categoria de rede.

Camada de filtragem:

-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**FWP \_ condição de \_ reautorizar \_ motivo \_ classificar \_ conclusão**
</dt> <dd> <dl> <dt>



Indica que uma conexão anteriormente armazenada agora está sendo permitida para ser concluída.

Camada de filtragem:

-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**FWP \_ condição de \_ reautorização do \_ motivo da \_ \_ alteração das propriedades de IPSec \_**
</dt> <dd> <dl> <dt>



Indica que as propriedades de IPsec foram alteradas ou que a conexão foi alterada de texto não criptografado para uma conexão segura.

Camada de filtragem:

-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**FWP \_ condição de \_ reautorizar \_ motivo \_ médio \_ inspeção de fluxo \_**
</dt> <dd> <dl> <dt>



Indica que uma conexão TCP estabelecida anteriormente agora está sendo inspecionada.

Camada de filtragem:

-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**FWP \_ condição de \_ reautorizar a \_ propriedade de soquete de motivo \_ \_ \_ alterada**
</dt> <dd> <dl> <dt>



Indica que as propriedades de soquete foram definidas depois que uma conexão foi autorizada e estabelecida.

Camada de filtragem:

-   \_Conexão de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**FWP \_ condição de \_ reautorizar \_ motivo \_ novo \_ \_ pacote mcast \_ BCAST \_ de entrada**
</dt> <dd> <dl> <dt>



Indica que novos pacotes multicast de entrada ou difusão estão sendo autorizados novamente em \_ \_ textos explicativos de aceitação Ale de recepção.

Camada de filtragem:

-   \_Aceitação da autenticação Ale de camada FWPM de \_ \_ \_ recebimento \_ \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

Os sinalizadores a seguir especificam as propriedades de soquete que estão relacionadas a se um aplicativo deseja receber o tráfego de percurso de borda. Esses sinalizadores e as camadas de filtragem em que podem ser usados são definidos da seguinte maneira.

> [!Note]  
> Essas condições de filtragem estão disponíveis apenas no Windows Server 2008 R2, Windows 7 e posterior.

 

<dl> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**o \_ sinalizador de propriedade de soquete de condição fwp \_ \_ \_ \_ é \_ RPC de porta do sistema \_ \_**
</dt> <dd> <dl> <dt>



Indica que o aplicativo está se comunicando com uma porta RPC dinâmica.

Camada de filtragem:

-   \_Escuta de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Atribuição de \_ recursos Ale de camada FWPM \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**\_sinalizador de propriedade de soquete de condição fwp \_ \_ \_ \_ permitir \_ tráfego de borda \_**
</dt> <dd> <dl> <dt>



Indica que o aplicativo deseja receber tráfego específico de passagem de borda.

Camada de filtragem:

-   \_Escuta de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Atribuição de \_ recursos Ale de camada FWPM \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**\_sinalizador de Propriedade do soquete de condição fwp \_ \_ \_ \_ negar \_ tráfego de borda \_**
</dt> <dd> <dl> <dt>



Indica que o aplicativo não deseja receber ou processar o tráfego específico de passagem de borda.

Camada de filtragem:

-   \_Escuta de \_ autenticação Ale de camada FWPM \_ \_ \_ V {4 \| 6}
-   \_Atribuição de \_ recursos Ale de camada FWPM \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

Os sinalizadores a seguir especificam detalhes de conexão relacionados à filtragem de L2.

> [!Note]  
> Essas condições de filtragem estão disponíveis apenas no Windows 8 e no Windows Server 2012.

 

<dl> <dt>

<span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**FWP \_ condição \_ L2 \_ é \_ \_ Ethernet nativa**
</dt> <dd> <dl> <dt>



Indica que a conexão é Ethernet nativa.

Camada de filtragem:

-   \_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM
-   \_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa
-   quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet
-   \_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**FWP \_ condição \_ L2 \_ é \_ WiFi**
</dt> <dd> <dl> <dt>



Indica que a conexão é Wi-Fi.

Camada de filtragem:

-   \_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM
-   \_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa
-   quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet
-   \_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**FWP \_ condição \_ L2 \_ é \_ \_ banda larga móvel**
</dt> <dd> <dl> <dt>



Indica que a conexão é de banda larga móvel.

Camada de filtragem:

-   \_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM
-   \_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa
-   quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet
-   \_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**FWP \_ condição \_ L2 \_ são \_ \_ dados diretos de WiFi \_**
</dt> <dd> <dl> <dt>



Indica que a conexão é Wi-Fi direta.

Camada de filtragem:

-   \_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM
-   \_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa
-   quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet
-   \_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**FWP \_ condição \_ L2 \_ é \_ VM2VM**
</dt> <dd> <dl> <dt>



Indica que a conexão está entre máquinas virtuais.

Camada de filtragem:

-   \_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM
-   \_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa
-   quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet
-   \_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**FWP \_ condição \_ L2 \_ é um \_ pacote malformado \_**
</dt> <dd> <dl> <dt>



Indica que um pacote parece estar malformado.

Camada de filtragem:

-   \_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM
-   \_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa
-   quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet
-   \_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**FWP \_ condição \_ L2 \_ é \_ \_ grupo de fragmentos IP \_**
</dt> <dd> <dl> <dt>



Indica um grupo de fragmentos de pacotes IP.

Camada de filtragem:

-   \_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM
-   \_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa
-   quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet
-   \_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**FWP \_ condição \_ L2 \_ se o \_ conector \_ estiver presente**
</dt> <dd> <dl> <dt>



Indica que um conector está presente.

Camada de filtragem:

-   \_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM
-   \_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa
-   quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet
-   \_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Fwptypes. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Filtrando identificadores de camada**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

