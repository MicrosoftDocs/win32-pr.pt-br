---
description: Representa tipos de endereço de rede. Use uma ou mais (como uma combinação de bits) das constantes a seguir para criar uma máscara de endereço de rede a ser usada com a macro \_ Myallowtype.
title: NET_STRING (Iphlpapi. h)
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
ms.openlocfilehash: 41ebe1cb844ec36ef13c8f8fe143d46dd9ac51b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988756"
---
# <a name="net_string"></a>Cadeia de caracteres LÍQUIda \_

Representa tipos de endereço de rede. Use uma ou mais (como uma combinação de bits) das constantes a seguir para criar uma máscara de endereço de rede a ser usada com a macro [**\_ myallowtype**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_setallowtype).



| Constante                                                                                                                                                                                                                   | Descrição                                                                                                                                                                    |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NET_STRING_IPV4_ADDRESS"></span><span id="net_string_ipv4_address"></span><dl> <dt>**\_Endereço IPv4 da cadeia de caracteres NET \_ \_**</dt> </dl>                              | A cadeia de caracteres identifica um host/roteador IPv4 usando o endereço literal (porta ou prefixo não permitido).<br/>                                                                       |
| <span id="NET_STRING_IPV4_SERVICE"></span><span id="net_string_ipv4_service"></span><dl> <dt>**\_Serviço IPv4 de cadeia de caracteres .NET \_ \_**</dt> </dl>                              | A cadeia de caracteres identifica um serviço IPv4 usando o endereço literal (porta necessária; prefixo não permitido).<br/>                                                                    |
| <span id="NET_STRING_IPV4_NETWORK"></span><span id="net_string_ipv4_network"></span><dl> <dt>**\_Rede IPv4 de cadeia de caracteres líquida \_ \_**</dt> </dl>                              | A cadeia de caracteres identifica uma rede IPv4 (prefixo necessário; porta não permitida).<br/>                                                                                          |
| <span id="NET_STRING_IPV6_ADDRESS"></span><span id="net_string_ipv6_address"></span><dl> <dt>**\_Endereço IPv6 da cadeia de caracteres NET \_ \_**</dt> </dl>                              | A cadeia de caracteres identifica um host/roteador IPv6 usando o endereço literal (porta ou prefixo não permitido; ID de escopo permitido.)<br/>                                                     |
| <span id="NET_STRING_IPV6_ADDRESS_NO_SCOPE"></span><span id="net_string_ipv6_address_no_scope"></span><dl> <dt>**\_Endereço IPv6 de cadeia de caracteres de rede \_ \_ \_ sem \_ escopo**</dt> </dl> | A cadeia de caracteres identifica um host/roteador IPv6 usando o endereço literal em que o contexto de interface já é conhecido (porta ou prefixo não permitido; ID de escopo não permitido).<br/>    |
| <span id="NET_STRING_IPV6_SERVICE"></span><span id="net_string_ipv6_service"></span><dl> <dt>**\_Serviço IPv6 de cadeia de caracteres .NET \_ \_**</dt> </dl>                              | A cadeia de caracteres identifica um serviço IPv6 usando o endereço literal (porta necessária; prefixo não permitido; ID de escopo permitido).<br/>                                                  |
| <span id="NET_STRING_IPV6_SERVICE_NO_SCOPE"></span><span id="net_string_ipv6_service_no_scope"></span><dl> <dt>**\_Serviço IPv6 de cadeia de caracteres .NET \_ \_ \_ sem \_ escopo**</dt> </dl> | A cadeia de caracteres identifica um serviço IPv6 usando o endereço literal em que o contexto de interface já é conhecido (porta necessária; prefixo não permitido; Scope-ID não permitido).<br/> |
| <span id="NET_STRING_IPV6_NETWORK"></span><span id="net_string_ipv6_network"></span><dl> <dt>**\_Rede IPv6 de cadeia de caracteres .NET \_ \_**</dt> </dl>                              | A cadeia de caracteres identifica uma rede IPv6 (prefixo necessário; porta ou escopo-ID não permitido).<br/>                                                                              |
| <span id="NET_STRING_NAMED_ADDRESS"></span><span id="net_string_named_address"></span><dl> <dt>**\_endereço de cadeia de caracteres .NET \_ nomeado \_**</dt> </dl>                           | A cadeia de caracteres identifica um host da Internet usando o DNS (porta ou prefixo ou escopo-ID não permitido).<br/>                                                                       |
| <span id="NET_STRING_NAMED_SERVICE"></span><span id="net_string_named_service"></span><dl> <dt>**NET \_ String \_ denominado \_ serviço**</dt> </dl>                           | A cadeia de caracteres identifica um serviço de Internet usando DNS (porta necessária; prefixo ou ID de escopo não permitido).<br/>                                                                |
| <span id="NET_STRING_IP_ADDRESS"></span><span id="net_string_ip_address"></span><dl> <dt>**\_endereço IP da cadeia de caracteres NET \_ \_**</dt> </dl>                                    | Endereço IPv4 da cadeia de caracteres de rede net de \_ \_ \_ endereços \| \_ \_ IPv6 \_ .<br/>                                                                                                           |
| <span id="NET_STRING_IP_ADDRESS_NO_SCOPE"></span><span id="net_string_ip_address_no_scope"></span><dl> <dt>**\_endereço IP da cadeia de caracteres .NET \_ \_ \_ sem \_ escopo**</dt> </dl>       | Endereço IPv4 da cadeia de caracteres .net endereço \_ \_ \_ \| \_ \_ IPv6 \_ \_ sem \_ escopo. <br/>                                                                                               |
| <span id="NET_STRING_IP_SERVICE"></span><span id="net_string_ip_service"></span><dl> <dt>**serviço de IP de cadeia de \_ caracteres NET \_ \_**</dt> </dl>                                    | Serviço IPv6 de cadeia de caracteres net do \_ \_ \_ serviço IPv4 \| \_ \_ \_ .<br/>                                                                                                           |
| <span id="NET_STRING_IP_SERVICE_NO_SCOPE"></span><span id="net_string_ip_service_no_scope"></span><dl> <dt>**\_Serviço IP de cadeia de caracteres NET \_ \_ \_ sem \_ escopo**</dt> </dl>       | Cadeia de caracteres de rede \_ \_ chamada \_ endereço \| net \_ String \_ \_ endereço IP \_ sem \_ escopo.<br/>                                                                                                 |
| <span id="NET_STRING_IP_NETWORK"></span><span id="net_string_ip_network"></span><dl> <dt>**\_rede IP de cadeia de caracteres NET \_ \_**</dt> </dl>                                    | Rede IPv6 de cadeia de caracteres de \_ \_ \_ rede IPv4 \| net \_ \_ \_ .<br/>                                                                                                           |
| <span id="NET_STRING_ANY_ADDRESS"></span><span id="net_string_any_address"></span><dl> <dt>**NET \_ String \_ qualquer \_ Endereço**</dt> </dl>                                 | Cadeia de caracteres de rede \_ \_ denominada \_ endereço \| IP de cadeia de \_ caracteres .NET \_ \_ .<br/>                                                                                                            |
| <span id="NET_STRING_ANY_ADDRESS_NO_SCOPE"></span><span id="net_string_any_address_no_scope"></span><dl> <dt>**\_cadeia de caracteres NET \_ qualquer \_ endereço \_ sem \_ escopo**</dt> </dl>    | Cadeia de caracteres de rede \_ \_ chamada \_ endereço \| net \_ String \_ \_ endereço IP \_ sem \_ escopo.<br/>                                                                                                 |
| <span id="NET_STRING_ANY_SERVICE"></span><span id="net_string_any_service"></span><dl> <dt>**NET \_ String \_ qualquer \_ serviço**</dt> </dl>                                 | Cadeia de caracteres de rede chamada serviço de \_ \_ IP de cadeia de caracteres de \_ serviço \| \_ \_ \_ .<br/>                                                                                                            |
| <span id="NET_STRING_ANY_SERVICE_NO_SCOPE"></span><span id="net_string_any_service_no_scope"></span><dl> <dt>**\_cadeia de caracteres NET \_ qualquer \_ serviço \_ sem \_ escopo**</dt> </dl>    | Cadeia de caracteres de rede \_ \_ chamada \_ endereço \| net \_ String \_ \_ endereço IP \_ sem \_ escopo.<br/>                                                                                                 |



## <a name="remarks"></a>Comentários

Esses valores são definidos em Iphlpapi. h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Iphlpapi. h</dt> </dl> |



 

 




