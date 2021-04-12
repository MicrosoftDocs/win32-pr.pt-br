---
title: O que há de novo na plataforma de filtragem do Windows
description: O Windows 8 e o Windows Server 2012 apresentam novos elementos de programação da plataforma de filtragem do Windows.
ms.assetid: 7529F155-3DBC-4C22-A780-B6311C455E85
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b5e441eff3242b530401235b085a1486527b98
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104294659"
---
# <a name="whats-new-in-windows-filtering-platform"></a>O que há de novo na plataforma de filtragem do Windows

O Windows 8 e o Windows Server 2012 apresentam novos elementos de programação da plataforma de filtragem do Windows. A nova funcionalidade inclui o seguinte:

-   *Filtragem de camada 2*: fornece acesso à camada L2 (Mac), permitindo a filtragem de tráfego nessa camada.
-   *filtragem de vSwitch*: permite que os pacotes que atravessam um vSwitch sejam inspecionados e/ou modificados. Os filtros WFP ou os textos explicativos podem ser usados na entrada e saída do vSwitch.
-   *Gerenciamento de contêiner de aplicativos*: permite o acesso a informações sobre os contêineres de aplicativos e problemas de conectividade de isolamento de rede.
-   *Atualizações de IPSec*: funcionalidade de IPSec estendida, incluindo monitoramento de estado de conexão, seleção de certificado e gerenciamento de chaves.

O Windows Driver Kit também inclui informações sobre [alterações de WFP para o Windows 8](/windows-hardware/drivers/network/wfp-changes-for-windows-8).

## <a name="windows-8-api-updates"></a>Atualizações de API do Windows 8

Muitas novas APIs foram adicionadas para o Windows 8 e o Windows Server 2012.

## <a name="new-functions"></a>Novas funções

-   [**FWPM \_ net \_ Event \_ CALLBACK1**](/windows/desktop/api/fwpmu/nc-fwpmu-fwpm_net_event_callback1)
-   [**FwpmConnectionCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectioncreateenumhandle0)
-   [**FwpmConnectionDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiondestroyenumhandle0)
-   [**FwpmConnectionEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionenum0)
-   [**FwpmConnectionGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetbyid0)
-   [**FwpmConnectionGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectiongetsecurityinfo0)
-   [**FwpmConnectionSetSecurityInfo0**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmconnectionsetsecurityinfo0)
-   [**FwpmConnectionSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscribe0)
-   [**FwpmConnectionSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionsubscriptionsget0)
-   [**FwpmConnectionUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmconnectionunsubscribe0)
-   [**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2)
-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2)
-   [**FwpmNetEventSubscribe1**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmneteventsubscribe1)
-   [**FwpmProviderContextAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextadd2)
-   [**FwpmProviderContextEnum2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextenum2)
-   [**FwpmProviderContextGetById2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmprovidercontextgetbyid2)
-   [**FwpmProviderContextGetByKey2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextgetbykey2)
-   [**FwpmvSwitchEventsGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsgetsecurityinfo0)
-   [**FwpmvSwitchEventsSetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventssetsecurityinfo0)
-   [**FwpmvSwitchEventSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventsubscribe0)
-   [**FwpmvSwitchEventUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmvswitcheventunsubscribe0)
-   [**IkeextSaEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsaenum2)
-   [**IkeextSaGetById2**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid2)
-   [**\_Chave do Gerenciador de chaves IPSec \_ \_ \_ ditado \_ CHECK0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [**\_Gerenciador de chaves IPSec \_ \_ ditar \_ Key0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [**\_Gerenciador de chaves IPSec \_ \_ notificar \_ Key0**](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [**\_CALLBACK0 de \_ contexto \_ SA IPsec**](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [**IPsecKeyManagerAddAndRegister0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [**IPsecKeyManagerGetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [**IPsecKeyManagerSetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [**IPsecKeyManagersGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [**IPsecKeyManagerUnregisterAndDelete0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   [**IPsecSaContextSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [**IPsecSaContextSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [**IPsecSaContextUnsubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextunsubscribe0)
-   [**NetworkIsolationDiagnoseConnectFailureAndGetInfo**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationdiagnoseconnectfailureandgetinfo)
-   [**NetworkIsolationEnumAppContainers**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumappcontainers)
-   [**NetworkIsolationEnumerateAppContainerRules**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationenumerateappcontainerrules)
-   [**NetworkIsolationFreeAppContainers**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationfreeappcontainers)
-   [**NetworkIsolationGetAppContainerConfig**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationgetappcontainerconfig)
-   [**NetworkIsolationRegisterForAppContainerChanges**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationregisterforappcontainerchanges)
-   [**NetworkIsolationSetAppContainerConfig**](/previous-versions/windows/desktop/api/netfw/nf-netfw-networkisolationsetappcontainerconfig)
-   [**NetworkIsolationSetupAppContainerBinaries**](/windows/desktop/api/networkisolation/nf-networkisolation-networkisolationsetupappcontainerbinaries)
-   [**retorno de chamada de alterações de PAC \_ \_ \_ FN**](/windows/desktop/api/networkisolation/nc-networkisolation-pac_changes_callback_fn)

## <a name="new-structures"></a>Novas estruturas

-   [**\_METHOD2 de autenticação IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_authentication_method2)
-   [**\_EKUS0 do certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_ekus0)
-   [**\_NAME0 do certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_cert_name0)
-   [**\_AUTHENTICATION2 do certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication2)
-   [**\_CRITERIA0 do certificado IKEEXT \_**](/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_criteria0)
-   [**IKEEXT \_ em \_ POLICY2**](/windows/win32/api/iketypes/ns-iketypes-ikeext_em_policy2)
-   [**\_AUTHENTICATION1 Kerberos \_ IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_kerberos_authentication1)
-   [**\_POLICY2 IKEEXT**](/windows/win32/api/iketypes/ns-iketypes-ikeext_policy2)
-   [**\_MANAGER0 de chave IPSec \_**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**\_Gerenciador de chaves IPSec \_ \_ CALLBACKS0**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**Chave do IPSEC \_ \_ POLICY1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**\_CHANGE0 de \_ contexto \_ SA IPsec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**\_SUBSCRIPTION0 de \_ contexto \_ SA IPsec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**\_POLICY2 de transporte IPSec \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**\_ENDPOINT0 de túnel IPSec \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**\_ENDPOINTS2 de túnel IPSec \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**\_POLICY2 de túnel IPSec \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**FWPM \_ CONNECTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection0)
-   [**\_TEMPLATE0 de \_ enumeração de conexão FWPM \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_enum_template0)
-   [**FWPM de \_ conexão \_ SUBSCRIPTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_connection_subscription0)
-   [**FWPM \_ net \_ EVENT2**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event2)
-   [**\_Funcionalidade de \_ evento FWPM NET \_ \_ ALLOW0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_allow0)
-   [**\_Funcionalidade de \_ evento FWPM NET \_ \_ DROP0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_capability_drop0)
-   [**\_ALLOW0 de \_ classificação de evento FWPM NET \_ \_**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_allow0)
-   [**\_DROP2 de \_ classificação de evento FWPM NET \_ \_**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop2)
-   [**\_MAC0 de \_ remoção de evento FWPM NET \_ \_ \_**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_classify_drop_mac0)
-   [**FWPM \_ net \_ Event \_ HEADER2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_net_event_header2)
-   [**\_Provedor FWPM \_ CONTEXT2**](/windows/win32/api/fwpmtypes/ns-fwpmtypes-fwpm_provider_context2)
-   [**FWPM \_ VSWITCH \_ EVENT0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event0)
-   [**\_ \_ Evento \_ SUBSCRIPTION0 do FWPM VSWITCH**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_vswitch_event_subscription0)

## <a name="new-enumerated-types"></a>Novos tipos enumerados

-   [**\_tipo de \_ rede fwp VSWITCH \_**](/windows/win32/api/fwptypes/ne-fwptypes-fwp_vswitch_network_type)
-   [**\_tipo de \_ recurso de rede FWPM APPC \_ \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_appc_network_capability_type)
-   [**\_tipo de \_ evento de conexão FWPM \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_connection_event_type)
-   [**\_tipo de \_ evento FWPM VSWITCH \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_vswitch_event_type)
-   [**\_tipo de \_ nome de critérios de certificado IKEEXT \_ \_**](/windows/win32/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)
-   [**\_Evento de contexto SA de IPSec \_ \_ \_ TYPE0**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_sa_context_event_type0)

## <a name="new-filtering-layer-identifiers"></a>Novos identificadores de camada de filtragem

[**Filtrando identificadores de camada:**](management-filtering-layer-identifiers-.md)

-   \_ \_ \_ Mac \_ frame \_ Ethernet de entrada da camada FWPM
-   quadro de Mac de saída da camada do FWPM \_ \_ \_ \_ \_ Ethernet
-   \_quadro de Mac de entrada da camada FWPM \_ \_ \_ \_ nativa
-   \_quadro do Mac de saída da camada FWPM \_ \_ \_ \_ nativa
-   \_ \_ Ethernet VSWITCH de entrada de camada \_ FWPM \_
-   \_ \_ Ethernet VSWITCH de egresso de camada FWPM \_ \_
-   Transporte de \_ vSwitch de entrada de camada \_ \_ \_ \_ v4/FWPM de \_ entrada da camada \_ \_ \_ \_ do FWPM de ingresso do vSwitch V6
-   Transporte do \_ vSwitch de saída de camada FWPM \_ \_ \_ \_ v4/FWPM de \_ saída de camada de egresso do \_ \_ vSwitch \_ \_ V6

## <a name="new-filtering-condition-identifiers"></a>Novos identificadores de condição de filtragem

[**Filtrando identificadores de condição:**](filtering-condition-identifiers-.md)

-   \_ \_ endereço MAC da interface de condição FWPM \_ \_
-   \_ \_ \_ endereço local Mac do FWPM Condition \_
-   \_ \_ \_ endereço remoto Mac do FWPM Condition \_
-   \_tipo de \_ ether \_ Condition FWPM
-   \_ID de \_ VLAN da condição FWPM \_
-   \_ \_ porta NDIS da condição FWPM \_
-   \_tipo de \_ \_ mídia NDIS da condição \_ FWPM
-   \_tipo de \_ \_ mídia física \_ de NDIS da condição FWPM \_
-   \_Sinalizadores de \_ L2 da condição FWPM \_
-   \_tipo de \_ \_ endereço local \_ Mac \_ do FWPM Condition
-   \_tipo de \_ \_ endereço remoto \_ Mac \_ da condição FWPM
-   \_ID do \_ pacote de Ale da condição FWPM \_ \_
-   \_endereço de \_ origem do Mac da condição FWPM \_ \_
-   \_endereço de \_ \_ destino Mac da condição \_ FWPM
-   \_tipo de \_ endereço de origem do Mac da condição FWPM \_ \_ \_
-   \_tipo de \_ \_ endereço de destino Mac da condição \_ FWPM \_
-   \_porta de \_ \_ origem IP da condição \_ FWPM
-   \_porta de \_ \_ destino IP da condição \_ FWPM
-   \_ID do \_ VSWITCH da condição FWPM \_
-   \_tipo de \_ rede do VSWITCH da condição FWPM \_ \_
-   ID da interface de origem do FWPM \_ condição \_ VSWITCH \_ \_ \_
-   ID da interface de destino do FWPM \_ Condition \_ VSWITCH \_ \_ \_
-   ID da VM de origem do FWPM \_ condição \_ VSWITCH \_ \_ \_
-   ID da VM de destino do FWPM \_ Condition \_ VSWITCH \_ \_ \_
-   tipo de interface de origem do FWPM \_ condição \_ VSWITCH \_ \_ \_
-   ID de rede do locatário do FWPM \_ Condition \_ VSWITCH \_ \_ \_

## <a name="new-filtering-condition-flags"></a>Novos sinalizadores de condição de filtragem

[**Filtrando sinalizadores de condição:**](filtering-condition-flags-.md)

-   o \_ sinalizador de condição fwp \_ é uma \_ \_ \_ conexão proxy
-   o \_ sinalizador de condição fwp \_ é o \_ \_ loopback do APPCONTAINER \_
-   o \_ sinalizador de condição fwp não \_ é um \_ \_ \_ loopback de APPCONTAINER \_
-   o \_ sinalizador de condição fwp \_ \_ está \_ respeitando a \_ política de \_ autorização
-   FWP \_ condição \_ L2 \_ é \_ \_ Ethernet nativa
-   FWP \_ condição \_ L2 \_ é \_ WiFi
-   FWP \_ condição \_ L2 \_ é \_ \_ banda larga móvel
-   FWP \_ condição \_ L2 \_ são \_ \_ dados diretos de WiFi \_
-   FWP \_ condição \_ L2 \_ é \_ VM2VM
-   FWP \_ condição \_ L2 \_ é um \_ pacote malformado \_
-   FWP \_ condição \_ L2 \_ é \_ \_ grupo de fragmentos IP \_
-   FWP \_ condição \_ L2 \_ se o \_ conector \_ estiver presente

## <a name="windows-7-updates-to-the-windows-filtering-platform"></a>Atualizações do Windows 7 para a plataforma de filtragem do Windows

O documento [novidades na plataforma de filtragem do Windows]() detalha muitas das atualizações feitas para o Windows 7. As informações também estão disponíveis no kit de driver do Windows em [alterações de WFP para o Windows 7](/windows-hardware/drivers/network/wfp-changes-for-windows-7).

 

 