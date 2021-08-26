---
title: Associações de segurança
description: Uma associação de segurança é a especificação de um token de segurança e informa ao tempo de execução como obter e usar um token de segurança para segurança de canal.
ms.assetid: 3e50e0fb-a7ca-4615-ac4c-5d93988e6460
keywords:
- Serviços Web de associações de segurança para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4afc668e6dc6ab42e2d57066ecfb47ce337603bcadeccfb6b12a14a0e0550381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054536"
---
# <a name="security-bindings"></a>Associações de segurança

Uma associação de segurança é a especificação de um token de segurança e informa ao tempo de execução como obter e usar um token de segurança para segurança de canal. O token de segurança contém informações que comprovam o direito de acessar recursos. Ele também pode ter uma chave de criptografia associada para executar assinaturas e criptografia.


Cada associação de segurança contém sua própria coleção de [configurações de associação de segurança](security-binding-settings.md) opcionais que têm como escopo o token de segurança definido por ele. Ele também contém [credenciais de segurança](security-credentials.md), que representam as evidências de segurança (como nome de usuário e senhas ou certificados) necessários para criar tokens de segurança.

As seguintes chamadas de retorno fazem parte da Associação de segurança:

-   [**\_retorno de \_ \_ chamada SAML do WS Validate**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)

As seguintes enumerações fazem parte da Associação de segurança:

-   [**uso de segurança do WS \_ Message \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_message_security_usage)
-   [**\_tipo de \_ autenticador SAML do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_saml_authenticator_type)
-   [**\_tipo de \_ Associação de segurança do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_type)
-   [**\_tipo de \_ identificador de chave de segurança WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_handle_type)

As funções a seguir fazem parte da Associação de segurança:

-   [**WsCreateXmlSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlsecuritytoken)
-   [**WsFreeSecurityToken**](/windows/desktop/api/WebServices/nf-webservices-wsfreesecuritytoken)
-   

As seguintes estruturas fazem parte da Associação de segurança:

-   [**\_identificador de \_ \_ chave de segurança assimétrica do WS \_ CAPI \_**](/windows/desktop/api/WebServices/ns-webservices-ws_capi_asymmetric_security_key_handle)
-   [**\_ \_ \_ autenticador SAML assinado por certificado WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_signed_saml_authenticator)
-   [**\_Associação de \_ \_ segurança de autenticação de cabeçalho http \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding)
-   [**\_Associação de \_ \_ segurança de mensagem APREQ \_ \_ do WS Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding)
-   [**\_Associação de \_ \_ segurança de transporte SSPI \_ \_ do WS NAMEDPIPE**](/windows/desktop/api/WebServices/ns-webservices-ws_namedpipe_sspi_transport_security_binding)
-   [**\_identificador de \_ chave de segurança assimétrica WS NCRYPT \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ncrypt_asymmetric_security_key_handle)
-   [**\_identificador de \_ \_ chave de segurança simétrica \_ \_ WS-RAW**](/windows/desktop/api/WebServices/ns-webservices-ws_raw_symmetric_security_key_handle)
-   [**\_autenticador SAML do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_authenticator)
-   [**\_Associação de \_ segurança de mensagem SAML \_ do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_saml_message_security_binding)
-   [**\_Associação de segurança WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding)
-   [**\_Associação de \_ segurança de mensagem de contexto de segurança WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding)
-   [**\_identificador de \_ chave de segurança do WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_key_handle)
-   [**\_Associação de \_ segurança de transporte WS SSL \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding)
-   [**Associação de segurança de transporte do WS \_ TCP \_ SSPI \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding)
-   [**\_Associação de \_ segurança de mensagem WS username \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding)
-   [**\_Associação de \_ \_ segurança de mensagem de token XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_token_message_security_binding)

 

 




