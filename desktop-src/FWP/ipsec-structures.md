---
title: Estruturas IPsec
description: Estruturas IPsec
ms.assetid: FF1FE626-B9F9-4091-8B82-BEB9D229B93D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beaf3b1f01a445538f06abe49fac71813e395e437d26b4f9792ce01b610b3125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068986"
---
# <a name="ipsec-structures"></a>Estruturas IPsec

## <a name="in-this-section"></a>Nesta seção

-   [**\_INFO0 de endereço IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_address_info0)
-   [**\_STATISTICS0 de \_ descarte de \_ pacote \_ agregado IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics0)
-   [**\_STATISTICS1 de \_ descarte de \_ pacote \_ agregado IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_drop_packet_statistics1)
-   [**\_STATISTICS0 SA de agregação IPSec \_ \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_aggregate_sa_statistics0)
-   [**\_STATISTICS0 de \_ descarte de \_ pacote \_ IPSec Ah**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_ah_drop_packet_statistics0)
-   [**\_Autenticação IPsec \_ e \_ codificação \_ TRANSFORM0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_and_cipher_transform0)
-   [**\_TRANSFORM0 de autenticação IPsec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform0)
-   [**\_Id0 de \_ transformação de autenticação IPsec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_auth_transform_id0)
-   [**\_TRANSFORM0 de codificação IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform0)
-   [**\_Id0 de \_ transformação de criptografia IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_cipher_transform_id0)
-   [**\_OPTIONS0 DOSP \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_options0)
-   [**\_STATE0 DOSP \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state0)
-   [**\_TEMPLATE0 de \_ estado de DOSP \_ IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_state_enum_template0)
-   [**\_STATISTICS0 DOSP \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_dosp_statistics0)
-   [**\_STATISTICS0 de \_ descarte de \_ pacote \_ IPSec ESP**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_esp_drop_packet_statistics0)
-   [**\_GETSPI0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi0)
-   [**\_GETSPI1 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_getspi1)
-   [**\_Id0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_id0)
-   [**\_MANAGER0 de chave IPSec \_**](/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_key_manager0)
-   [**\_Gerenciador de chaves IPSec \_ \_ CALLBACKS0**](/windows/desktop/api/fwpmu/ns-fwpmu-ipsec_key_manager_callbacks0)
-   [**\_POLICY0 de chave IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keying_policy0)
-   [**Chave do IPSEC \_ \_ POLICY1**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_keying_policy1)
-   [**STATE0 de módulo de IPSEC \_ \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_keymodule_state0)
-   [**\_PROPOSAL0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_proposal0)
-   [**\_SA0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa0)
-   [**\_Autenticação SA \_ IPSec \_ e \_ codificação \_ INFORMATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_and_cipher_information0)
-   [**\_INFORMATION0 de \_ autenticação \_ SA IPsec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_auth_information0)
-   [**\_BUNDLE0 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle0)
-   [**\_BUNDLE1 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_bundle1)
-   [**\_INFORMATION0 de \_ criptografia \_ SA IPsec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_cipher_information0)
-   [**\_CONTEXT0 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context0)
-   [**\_CONTEXT1 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context1)
-   [**\_CHANGE0 de \_ contexto \_ SA IPsec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_change0)
-   [**\_TEMPLATE0 de \_ enumeração de contexto SA \_ IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_enum_template0)
-   [**\_SUBSCRIPTION0 de \_ contexto \_ SA IPsec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_context_subscription0)
-   [**\_DETAILS0 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details0)
-   [**\_DETAILS1 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_details1)
-   [**\_TEMPLATE0 de \_ enumeração \_ SA IPsec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_enum_template0)
-   [**\_TIMEOUT0 de \_ ociosidade de SA IPsec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_idle_timeout0)
-   [**\_LIFETIME0 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_lifetime0)
-   [**\_STATISTICS0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics0)
-   [**\_STATISTICS1 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_statistics1)
-   [**\_TRANSFORM0 SA \_ IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_sa_transform0)
-   [**\_TOKEN0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_token0)
-   [**\_TRAFFIC0 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic0)
-   [**\_TRAFFIC1 IPSec**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic1)
-   [**\_STATISTICS0 de tráfego IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics0)
-   [**\_STATISTICS1 de tráfego IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_traffic_statistics1)
-   [**\_POLICY0 de transporte IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0)
-   [**\_Transporte IPSec \_ POLICY1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy1)
-   [**\_POLICY2 de transporte IPSec \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_transport_policy2)
-   [**\_ENDPOINT0 de túnel IPSec \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoint0)
-   [**\_ENDPOINTS0 de túnel IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints0)
-   [**\_ENDPOINTS1 de túnel IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints1)
-   [**\_ENDPOINTS2 de túnel IPSec \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_endpoints2)
-   [**\_POLICY0 de túnel IPSec \_**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy0)
-   [**\_Túnel IPSec \_ POLICY1**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_tunnel_policy1)
-   [**\_POLICY2 de túnel IPSec \_**](/windows/win32/api/ipsectypes/ns-ipsectypes-ipsec_tunnel_policy2)
-   [**IPSEC \_ v4 \_ UDP \_ ENCAPSULATION0**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_v4_udp_encapsulation0)
-   [**IPSEC \_ virtual \_ se o \_ túnel \_ INFO0**](/windows/win32/api/fwptypes/ns-fwptypes-ipsec_virtual_if_tunnel_info0)

 

 




