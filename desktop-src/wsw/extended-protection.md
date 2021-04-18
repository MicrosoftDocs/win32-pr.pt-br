---
title: Proteção Estendida
description: A proteção estendida é um mecanismo para associar um canal seguro externo, como SSL a protocolos de autenticação de canal interno, como Kerberos-APREQ e autenticação de cabeçalho HTTP.
ms.assetid: 35e48846-05e5-4db9-a3b5-098b62815b66
keywords:
- Proteção estendida nativa-Web-Services
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 895bdfecf994f6673c2ed7e7367bc3a7b5bd70c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105767703"
---
# <a name="extended-protection"></a>Proteção Estendida

A proteção estendida é um mecanismo para associar um canal seguro externo, como SSL a protocolos de autenticação de canal interno, como Kerberos-APREQ e autenticação de cabeçalho HTTP.

O conceito de proteção estendida é definido em RFC2743.

A proteção estendida, quando disponível, é configurada automaticamente no cliente, mas pode exigir configuração no servidor para cenários não padrão.

## <a name="supported-configurations"></a>Configurações com suporte

Há suporte para a proteção estendida ao usar a [**\_ \_ \_ Associação de canal http do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) com associações de segurança usando protocolos de autenticação integrada do Windows, como associação de [**\_ segurança de autenticação de \_ cabeçalho \_ \_ \_ WS http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) e [**Associação de segurança de \_ mensagem WS Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding). Ele é configurado por meio das seguintes [**Propriedades de segurança**](/windows/desktop/api/WebServices/ns-webservices-ws_security_property):

-   [**\_política de \_ \_ proteção estendida da propriedade de \_ segurança WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_cenário de \_ \_ proteção estendida da propriedade de \_ segurança do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [**\_ \_ \_ identidades do serviço de propriedade de segurança WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)

As seguintes configurações que envolvem a proteção estendida são possíveis:

Cliente

-   [**WS \_ A \_ \_ \_ Associação de segurança de transporte SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) é usada com associação de segurança de [**\_ \_ \_ mensagem \_ \_ APREQ WS Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) ou associação de [**segurança de autenticação de \_ \_ cabeçalho WS \_ \_ \_ http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding). Nessa configuração, a associação de autenticação é associada à conexão SSL por meio de um token de proteção estendido que é extraído automaticamente da conexão SSL.
-   Nenhum SSL é usado e [**a \_ \_ Associação de \_ \_ segurança de \_ autenticação de cabeçalho HTTP do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) está definida. A associação de autenticação é associada por meio do SPN (nome principal do servidor), que é autonatically determinado do [**\_ \_ endereço do ponto de extremidade do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address).

Servidor

-   [**WS \_ A \_ \_ \_ Associação de segurança de transporte SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) é usada com associação de segurança de [**\_ \_ \_ mensagem \_ \_ APREQ WS Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) ou associação de [**segurança de autenticação de \_ \_ cabeçalho WS \_ \_ \_ http**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding). Nessa configuração, a associação de autenticação é associada à conexão SSL por meio de um token de proteção estendido que é extraído da conexão SSL e validado automaticamente.
-   Nenhum SSL é usado e [**a \_ \_ Associação de \_ \_ segurança de \_ autenticação de cabeçalho HTTP do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) está definida. A associação de autenticação é associada por meio do SPN (nome principal do servidor), que deve ser fornecido por meio de [**\_ \_ \_ \_ identidades do serviço de propriedade de segurança WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id). Quando uma mensagem é recebida, o SPN é extraído e validado para uma correspondência exata com os nomes de serviço fornecidos. Não fornecer SPNs é o equivalente de definir [**a \_ política de proteção estendida do WS \_ \_ \_ nunca**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy).
-   Nenhum SSL é usado, [**o \_ \_ \_ \_ \_ servidor associado do cenário de proteção estendida do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) é especificado e a [**\_ \_ \_ \_ \_ Associação de segurança de mensagem APREQ do WS Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) é usada. Nesta configuração, as [**\_ \_ \_ \_ identidades do serviço de propriedade de segurança WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) não devem ser definidas. Nenhuma verificação de SPN é executada além do que é feito como parte do protocolo Kerberos.
-   [**WS \_ O uso do cenário de proteção ESTENDIda \_ \_ \_ \_ SSL**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario) foi especificado e a associação de [**segurança de mensagem do WS \_ Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) ou a associação de [**segurança de autenticação de \_ \_ cabeçalho \_ \_ \_ http WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding) é usada. [**WS \_ As \_ \_ \_ identidades do serviço de propriedade de segurança**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) devem ser definidas.

## <a name="supported-platforms"></a>Plataformas compatíveis

Há suporte para proteção estendida em plataformas com suporte para ela no sistema operacional. O Windows 7 e o Windows Server 2008 R2 fornecem suporte interno. Outras plataformas podem exigir uma atualização.

Se o sistema operacional do servidor não fornecer tal suporte, todas as informações de proteção estendidas enviadas pelo cliente serão ignoradas. Como resultado, os clientes que usam a proteção estendida podem se comunicar com um servidor desse tipo, mas o benefício de segurança é perdido. No cliente, a [**\_ Associação de \_ \_ segurança de \_ \_ mensagem APREQ do WS Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) combinada com a associação de segurança de [**\_ \_ transporte \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding) só dá suporte à proteção estendida no Vista e superior.

Observação: a proteção estendida que está sendo indisponível não impede que nenhuma configuração específica seja usada.

## <a name="interoperability"></a>Interoperabilidade

Um servidor configurado por padrão pode se comunicar com clientes SOAP, independentemente se eles usam proteção estendida ou não. A única exceção sendo o Windows XP e o Windows Server 2003 WWSAPI clientes que foram atualizados para oferecer suporte à proteção estendida e usam a [**Associação de segurança de mensagem do WS \_ Kerberos \_ APREQ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding) e a [**\_ \_ \_ \_ Associação de segurança de transporte WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding). Para dar suporte a tais clientes, a [**\_ política de proteção estendida do WS \_ \_ \_ nunca**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy) deve ser especificada pelo servidor. Os servidores configurados com a **\_ política de proteção estendida do WS \_ \_ \_ sempre** rejeitarão a comunicação de clientes que não usam a proteção estendida. No cliente, a **\_ Associação de \_ \_ segurança de \_ \_ mensagem APREQ do WS Kerberos** combinada com a associação de segurança de **\_ \_ transporte \_ \_ WS SSL** resultará na mensagem que está sendo enviada usando a codificação de transferência em partes de http no Vista e superior. Isso pode causar problemas de interoperabilidade com servidores que não dão suporte à transferência em partes.

As seguintes enumerações/constantes fazem parte da proteção estendida:

-   [**\_política de \_ proteção estendida do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_policy)
-   [**\_cenário de \_ proteção estendida do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_extended_protection_scenario)

Os stuctures a seguir fazem parte da proteção estendida:

-   [**\_ \_ identidades de segurança do serviço WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_security_identities)

 

 




