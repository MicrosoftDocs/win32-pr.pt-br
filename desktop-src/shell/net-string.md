---
description: Representar tipos de endereço de rede. Use uma ou mais (como uma combinação bit a bit) das constantes a seguir para criar uma máscara de endereço de rede a ser usada com a macro NetAddr \_ SetAllowType.
title: NET_STRING (Iphlpapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4144dac9-772c-49cb-b924-e852fb4c81c7
api_name:
- NET_STRING_IPV4_ADDRESS
- NET_STRING_IPV4_SERVICE
- NET_STRING_IPV4_NETWORK
- NET_STRING_IPV6_ADDRESS
- NET_STRING_IPV6_ADDRESS_NO_SCOPE
- NET_STRING_IPV6_SERVICE
- NET_STRING_IPV6_SERVICE_NO_SCOPE
- NET_STRING_IPV6_NETWORK
- NET_STRING_NAMED_ADDRESS
- NET_STRING_NAMED_SERVICE
- NET_STRING_IP_ADDRESS
- NET_STRING_IP_ADDRESS_NO_SCOPE
- NET_STRING_IP_SERVICE
- NET_STRING_IP_SERVICE_NO_SCOPE
- NET_STRING_IP_NETWORK
- NET_STRING_ANY_ADDRESS
- NET_STRING_ANY_ADDRESS_NO_SCOPE
- NET_STRING_ANY_SERVICE
- NET_STRING_ANY_SERVICE_NO_SCOPE
api_type:
- HeaderDef
api_location:
- Iphlpapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a7d1a09e6165e77ee5419da47419a65e3995ce0ffedb8a6fb71f01fb9c63dde5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111216"
---
# <a name="net_string"></a>CADEIA DE \_ CARACTERES NET

Representar tipos de endereço de rede. Use uma ou mais (como uma combinação bit a bit) das constantes a seguir para criar uma máscara de endereço de rede a ser usada com a macro [**NetAddr \_ SetAllowType**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype).



| Constante                                                                                                                                                                                                                   | Descrição                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NET_STRING_IPV4_ADDRESS"></span><span id="net_string_ipv4_address"></span><dl> <dt>**ENDEREÇO \_ IPV4 DA CADEIA \_ DE \_ CARACTERES NET**</dt> </dl>                              | A cadeia de caracteres identifica um host/roteador IPv4 usando o endereço literal (porta ou prefixo não permitido).<br/>                                                                       |
| <span id="NET_STRING_IPV4_SERVICE"></span><span id="net_string_ipv4_service"></span><dl> <dt>**NET \_ STRING \_ IPV4 \_ SERVICE**</dt> </dl>                              | A cadeia de caracteres identifica um serviço IPv4 usando o endereço literal (porta necessária; prefixo não permitido).<br/>                                                                    |
| <span id="NET_STRING_IPV4_NETWORK"></span><span id="net_string_ipv4_network"></span><dl> <dt>**REDE \_ NET STRING \_ IPV4 \_**</dt> </dl>                              | A cadeia de caracteres identifica uma rede IPv4 (prefixo obrigatório; porta não permitida).<br/>                                                                                          |
| <span id="NET_STRING_IPV6_ADDRESS"></span><span id="net_string_ipv6_address"></span><dl> <dt>**ENDEREÇO \_ IPV6 DA CADEIA \_ DE \_ CARACTERES NET**</dt> </dl>                              | A cadeia de caracteres identifica um host/roteador IPv6 usando o endereço literal (porta ou prefixo não permitido; scope-id permitido.)<br/>                                                     |
| <span id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></span><span id="net_string_ipv6_address_no_scope"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ ADDRESS \_ NO \_ SCOPE**</dt> </dl> | A cadeia de caracteres identifica um host/roteador IPv6 usando o endereço literal em que o contexto da interface já é conhecido (porta ou prefixo não permitido; scope-id não permitido).<br/>    |
| <span id="NET_STRING_IPV6_SERVICE"></span><span id="net_string_ipv6_service"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ SERVICE**</dt> </dl>                              | A cadeia de caracteres identifica um serviço IPv6 usando o endereço literal (porta necessária; prefixo não permitido; scope-id permitido).<br/>                                                  |
| <span id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></span><span id="net_string_ipv6_service_no_scope"></span><dl> <dt>**NET \_ STRING \_ IPV6 \_ SERVICE \_ NO \_ SCOPE**</dt> </dl> | A cadeia de caracteres identifica um serviço IPv6 usando o endereço literal em que o contexto da interface já é conhecido (porta necessária; prefixo não permitido; id de escopo não permitida).<br/> |
| <span id="NET_STRING_IPV6_NETWORK"></span><span id="net_string_ipv6_network"></span><dl> <dt>**REDE \_ \_ IPV6 DE CADEIA DE \_ CARACTERES NET**</dt> </dl>                              | A cadeia de caracteres identifica uma rede IPv6 (prefixo obrigatório; porta ou id de escopo não permitido).<br/>                                                                              |
| <span id="NET_STRING_NAMED_ADDRESS"></span><span id="net_string_named_address"></span><dl> <dt>**NET \_ STRING \_ NAMED \_ ADDRESS**</dt> </dl>                           | A cadeia de caracteres identifica um Host da Internet usando o DNS (porta ou prefixo ou id de escopo não permitido).<br/>                                                                       |
| <span id="NET_STRING_NAMED_SERVICE"></span><span id="net_string_named_service"></span><dl> <dt>**NET \_ STRING \_ NAMED \_ SERVICE**</dt> </dl>                           | A cadeia de caracteres identifica um serviço de Internet usando DNS (porta necessária; prefixo ou id de escopo não permitido).<br/>                                                                |
| <span id="NET_STRING_IP_ADDRESS"></span><span id="net_string_ip_address"></span><dl> <dt>**ENDEREÇO IP \_ DA CADEIA \_ DE \_ CARACTERES NET**</dt> </dl>                                    | ENDEREÇO \_ NET STRING \_ IPV4 \_ NET STRING \| \_ \_ IPV6. \_<br/>                                                                                                           |
| <span id="NET_STRING_IP_ADDRESS_NO_SCOPE"></span><span id="net_string_ip_address_no_scope"></span><dl> <dt>**ENDEREÇO \_ IP DA CADEIA DE \_ \_ CARACTERES NET SEM \_ \_ ESCOPO**</dt> </dl>       | NET \_ STRING \_ IPV4 \_ ENDEREÇO NET STRING \| \_ \_ IPV6 \_ ENDEREÇO IPV6 SEM \_ \_ ESCOPO. <br/>                                                                                               |
| <span id="NET_STRING_IP_SERVICE"></span><span id="net_string_ip_service"></span><dl> <dt>**NET \_ STRING \_ IP \_ SERVICE**</dt> </dl>                                    | NET \_ STRING \_ IPV4 \_ SERVICE \| NET \_ STRING \_ IPV6 \_ SERVICE.<br/>                                                                                                           |
| <span id="NET_STRING_IP_SERVICE_NO_SCOPE"></span><span id="net_string_ip_service_no_scope"></span><dl> <dt>**NET \_ STRING \_ IP \_ SERVICE \_ NO \_ SCOPE**</dt> </dl>       | CADEIA DE \_ CARACTERES NET \_ CHAMADA ENDEREÇO NET STRING ENDEREÇO IP SEM \_ \| \_ \_ \_ \_ \_ ESCOPO.<br/>                                                                                                 |
| <span id="NET_STRING_IP_NETWORK"></span><span id="net_string_ip_network"></span><dl> <dt>**REDE IP \_ DA CADEIA \_ DE \_ CARACTERES NET**</dt> </dl>                                    | NET \_ STRING \_ IPV4 \_ NETWORK \| NET \_ STRING \_ IPV6 \_ NETWORK.<br/>                                                                                                           |
| <span id="NET_STRING_ANY_ADDRESS"></span><span id="net_string_any_address"></span><dl> <dt>**NET \_ STRING \_ ANY \_ ADDRESS**</dt> </dl>                                 | CADEIA DE \_ CARACTERES NET \_ CHAMADA ENDEREÇO ENDEREÇO IP DA CADEIA DE \_ \| \_ \_ \_ CARACTERES NET.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></span><span id="net_string_any_address_no_scope"></span><dl> <dt>**NET \_ STRING \_ ANY \_ ADDRESS \_ NO \_ SCOPE**</dt> </dl>    | CADEIA DE \_ CARACTERES NET \_ CHAMADA ENDEREÇO NET STRING ENDEREÇO IP SEM \_ \| \_ \_ \_ \_ \_ ESCOPO.<br/>                                                                                                 |
| <span id="NET_STRING_ANY_SERVICE"></span><span id="net_string_any_service"></span><dl> <dt>**NET \_ STRING \_ ANY \_ SERVICE**</dt> </dl>                                 | CADEIA DE \_ CARACTERES NET \_ CHAMADA SERVIÇO IP DA CADEIA DE \_ \| \_ \_ \_ CARACTERES DO SERVIÇO.<br/>                                                                                                            |
| <span id="NET_STRING_ANY_SERVICE_NO_SCOPE"></span><span id="net_string_any_service_no_scope"></span><dl> <dt>**NET \_ STRING \_ ANY \_ SERVICE \_ NO \_ SCOPE**</dt> </dl>    | CADEIA DE \_ CARACTERES NET \_ CHAMADA ENDEREÇO NET STRING ENDEREÇO IP SEM \_ \| \_ \_ \_ \_ \_ ESCOPO.<br/>                                                                                                 |



## <a name="remarks"></a>Comentários

Esses valores são definidos em Iphlpapi.h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Iphlpapi.h</dt> </dl> |



 

 




