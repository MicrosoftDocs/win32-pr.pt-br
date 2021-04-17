---
title: Mapeamento de metadados
description: O conteúdo de um documento de metadados é mapeado para a API de metadados das maneiras explicadas nas seções a seguir.
ms.assetid: 266f8319-b7ac-497f-8eb7-8e2c7bcede33
keywords:
- Serviços Web de mapeamento de metadados para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb9da067768569e78ba6bb98ee219e11917d3201
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "105784946"
---
# <a name="metadata-mapping"></a>Mapeamento de metadados

O conteúdo de um documento de metadados é mapeado para a API de metadados das maneiras explicadas nas seções a seguir.


Os seguintes prefixos de namespace são usados em toda esta documentação:

``` syntax
wsdl   => http://schemas.xmlsoap.org/wsdl/
soap11 => http://schemas.xmlsoap.org/wsdl/soap/
soap12 => http://schemas.xmlsoap.org/wsdl/soap12/
wsa09  => http://schemas.xmlsoap.org/ws/2004/08/addressing
wsa10  => http://www.w3.org/2005/08/addressing
wsa09p => http://schemas.xmlsoap.org/ws/2004/08/addressing/policy
wsa10p => http://www.w3.org/2006/05/addressing/wsdl
binp   => http://schemas.microsoft.com/ws/06/2004/mspolicy/netbinary1
mtomp  => http://schemas.xmlsoap.org/ws/2004/09/policy/optimizedmimeserialization
sp     => http://schemas.xmlsoap.org/ws/2005/07/securitypolicy
wsp    => http://schemas.xmlsoap.org/ws/2004/09/policy
netf   => http://schemas.microsoft.com/ws/2006/05/framing/policy
httpp  => http://schemas.microsoft.com/ws/06/2004/policy/http
wst10  => http://schemas.xmlsoap.org/ws/2005/02/trust
wsi    => http://schemas.xmlsoap.org/ws/2005/05/identity
```

As seções subsequentes descrevem as construções de API junto com quais construções de metadados (WSDL ou política) correspondem.

A familiaridade com especificações de metadados como WSDL e política ajudará a entender esta seção.

## <a name="endpoint-address"></a>Endereço do ponto de extremidade

O endereço de um ponto de extremidade (consulte o [**\_ \_ endereço do ponto de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) é obtido de um elemento de extensibilidade dentro do elemento wsdl: Port do documento WSDL. Os seguintes elementos de extensibilidade têm suporte para especificar o endereço:

``` syntax
<wsdl:port...>
    <soap11:address.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <soap12:address.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <wsa09:EndpointReference.../>
</wsdl:port>
```

``` syntax
<wsdl:port...>
    <wsa10:EndpointReference.../>
</wsdl:port>
```

## <a name="ws_channel_binding"></a>Associação de WS \_ Channel \_

A associação de canal ( [**consulte \_ \_ Associação de WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) é determinada pelo transporte da Associação SOAP usada, da seguinte maneira:

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a>\_versão do \_ envelope da propriedade \_ \_ do WS Channel

A versão do envelope (consulte a [**versão do envelope da Propriedade do WS \_ Channel \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) é determinada pela qual a associação SOAP é usada, da seguinte maneira:

``` syntax
<wsdl:binding...>
    <soap11:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_1
</wsdl:binding>
```

``` syntax
<wsdl:binding...>
    <soap12:binding.../> => WS_ENVELOPE_VERSION_SOAP_1_2
</wsdl:binding>
```

## <a name="addressing-version"></a>Versão de endereçamento

A versão de endereçamento (consulte [**\_ \_ \_ \_ versão de endereçamento de Propriedade do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) é determinada pelas seguintes asserções na política de ponto de extremidade:

``` syntax
<wsp:Policy...>
    <wsa09p:UsingAddressing.../> => WS_ADDRESSING_VERSION_0_9
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <wsa10p:UsingAddressing.../> => WS_ADDRESSING_VERSION_1_0
</wsp:Policy>
```

Se uma declaração de endereçamento não estiver presente, o [**\_ transporte da \_ versão \_ de endereçamento do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) será assumido.

## <a name="message-encoding"></a>Decodificador de mensagens

A codificação da mensagem (consulte [**codificação de \_ \_ propriedade \_ de WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) é determinada pelas seguintes asserções na política de ponto de extremidade:

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

Observe que a declaração de diretiva de codificação binária não inclui informações sobre se a codificação binária é sessão ou sem sessão. Isso é determinado pela restrição de propriedade de codificação (que deve ser apropriada de acordo com o [**tipo de \_ canal \_ do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) ou não que está sendo usado é sessão ou não).

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

Se nenhuma das declarações acima estiver presente, uma codificação de texto será usada: [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS \_ Encoding \_ XML \_ UTF16LE**, **WS \_ Encoding \_ XML \_ UTF16BE**.

Observe que a política não inclui informações sobre o conjunto de caracteres para MTOM ou codificações de texto (seja UTF8, UTF16LE ou UTF16BE). O valor do conjunto de caracteres real usado é determinado pela restrição de propriedade de codificação.

## <a name="constraints-with-http-header-authentication"></a>Restrições com autenticação de cabeçalho HTTP

Esta seção se aplica quando a restrição de associação de segurança de [**\_ restrição de \_ \_ \_ \_ Associação \_ de segurança do cabeçalho HTTP do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) é especificada.

Essa associação de segurança é indicada na política por asserções diferentes que afirma que a autenticação do cabeçalho HTTP deve ser usada e que um esquema de autenticação específico deve ser usado. As declarações de política correspondem aos valores do esquema de [**\_ autenticação do \_ \_ \_ \_ cabeçalho \_ \_ http da propriedade de associação de segurança do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) da seguinte maneira:

``` syntax
<wsp:Policy...>
    <httpp:BasicAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_BASIC
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:NegotiateAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_NEGOTIATE
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:NtlmAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_NTLM
</wsp:Policy>
```

``` syntax
<wsp:Policy...>
    <httpp:DigestAuthentication.../> => WS_HTTP_HEADER_AUTH_SCHEME_DIGEST
</wsp:Policy>
```

## <a name="constraints-with-sll-transport-security"></a>Restrições com segurança de transporte SLL

Esta seção se aplica quando a restrição de associação de segurança de [**restrição de associação de \_ segurança de \_ transporte \_ \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) é especificada. As seguintes declarações de política são usadas neste caso:

``` syntax
<wsp:Policy...>
    <sp:TransportBinding...>
        <wsp:Policy...>
            <sp:TransportToken...>
                <wsp:Policy...>
                    <sp:HttpsToken.../>
            </wsp:Policy...>
        </wsp:Policy>
    </sp:TransportBinding...>
</wsp:Policy>
```

## <a name="constraints-with-sspi-transport-security"></a>Restrições com segurança de transporte SSPI

Esta seção se aplica quando a restrição de associação de segurança de [**restrição de associação de segurança de transporte do WS \_ TCP \_ SSPI \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) é especificada. As seguintes declarações de política são usadas neste caso:

``` syntax
<wsp:Policy...>
    <sp:TransportBinding...>
        <wsp:Policy...>
            <sp:TransportToken...>
                <wsp:Policy...>
                    <netf:WindowsTransportSecurity.../>
            </wsp:Policy...>
        </wsp:Policy>
    </sp:TransportBinding...>
</wsp:Policy>
```

## <a name="constrains-with-transport-security"></a>Restrições com segurança de transporte

A restrição de Propriedade do [**\_ \_ \_ \_ \_ nível de proteção da propriedade de segurança WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) pode ser especificada se qualquer uma das restrições de associação de segurança for especificada:

-   [**\_restrição de \_ Associação de segurança de transporte WS SSL \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    O valor da política sempre é [**o \_ nível de proteção WS \_ \_ -Sign \_ e \_ Encrypt**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

-   [**restrição de associação de segurança de transporte do WS \_ TCP \_ SSPI \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    O valor da política é especificado como parte da asserção WindowsTransportSecurity, da seguinte maneira:

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [**\_restrição de \_ \_ Associação de segurança de autenticação de cabeçalho \_ http \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    O valor da política sempre é [**o \_ \_ nível de \_ proteção WS**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).

## <a name="constraints-with-kerberos-apreq-security-binding"></a>Restrições com a associação de segurança APREQ Kerberos

Esta seção se aplica quando a restrição de associação de segurança de restrição de associação de segurança de [**mensagem de APREQ do WS \_ \_ \_ \_ \_ \_ Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) é especificada. As seguintes declarações de política são usadas neste caso:

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a>Restrições com associação de segurança de mensagem

Esta seção se aplica quando a restrição de associação de segurança de [**\_ \_ \_ \_ \_ restrição**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) de segurança de mensagem do WS-nomedeusuário é especificada. As seguintes declarações de política são usadas neste caso:

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a>\_restrição de \_ Associação de segurança de mensagem de certificado WS \_ \_ \_

Esta seção se aplica quando a restrição de associação de segurança de [**restrição de associação de segurança de \_ mensagem de certificado \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) é especificada. As seguintes declarações de política são usadas neste caso:

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a>\_restrição de \_ \_ Associação de segurança de mensagem de token emitida \_ WS \_ \_

Esta seção se aplica quando a restrição de associação de segurança de [**\_ mensagem de token de \_ segurança de mensagens de símbolo \_ \_ \_ \_ emitida WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) é especificada. As seguintes declarações de política são usadas neste caso:

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:IssuedToken sp:IncludeToken=&quot;xs:anyURI&quot;? ...=&quot;&quot; >
            <wsp:Issuer>...</wsp:Issuer>?
            <wsp:RequestSecurityTokenTemplate TrustVersion='xs:anyURI&quot;?>
                ...
                <wst10:Claims>
                    <wsi:ClaimType Optional='xs:boolean'?>xs:anyURI<wt:ClaimType>*
                </wst10:Claims>
                ...
            </wsp:RequestSecurityTokenTemplate>
            <wsp:Policy>
                <sp:RequireDerivedKeys/> ?
                <sp:RequireExternalReference/> ?
                <sp:RequireInternalReference/> ?
            </wsp:Policy> ?
        </sp:IssuedToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

O seguinte descreve o mapeamento de campos da [**restrição de \_ \_ Associação de \_ \_ segurança de \_ \_ mensagem de token emitida pelo WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) para a política acima:

-   O campo claimConstraints é usado para verificar o conjunto de URIs de tipo de declaração que aparecem dentro do elemento WSI: ClaimType acima.

-   O campo issuerAddress corresponde ao elemento WSP: emissor acima, que é o endereço do [**\_ ponto de \_ extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) do serviço que pode emitir o token.

-   O campo requestSecurityTokenTemplate corresponde aos elementos filho do elemento WSP: RequestSecurityTokenTemplate.

## <a name="ws_security_context_message_security_binding_constraint"></a>\_restrição de \_ \_ Associação de segurança de mensagem de contexto \_ de \_ segurança WS \_

Esta seção se aplica quando a restrição de associação de segurança da [**\_ \_ mensagem de contexto \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) de segurança do WS Security é especificada. As seguintes declarações de política são usadas neste caso:

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:SecureConversationToken sp:IncludeToken=&quot;xs:anyURI&quot;? ...=&quot;&quot; >
            <wsp:Issuer>...</wsp:Issuer>?
            <wsp:Policy>
                <sp:RequireDerivedKeys.../>?
                <sp:RequireExternalUriReference.../>?
                <sp:SC10SecurityContextToken.../>? => WS_SECURE_CONVERSATION_VERSION_FEBRUARY_2005
                <sp:BootstrapPolicy... >?
                   <wsp:Policy> ...  </wsp:Policy> => WS_SECURITY_CONSTRAINTS
                </sp:BootstrapPolicy>
            </wsp:Policy>
        </wsp:SecureConversationToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

O modo de entropia é determinado pela asserção <SP: Trust10>. <SP: RequireClientEntropy/> e <SP: RequireServerEntropy/> => [**\_ modo de entropia de chave de segurança ws \_ \_ \_ \_ combinado**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <SP: RequireClientEntropy/> => modo de entropia de chave de **segurança WS \_ \_ \_ \_ \_ \_ somente** <SP: RequireServerEntropy/> => **\_ \_ \_ \_ \_ \_ somente servidor do modo de entropia de chave de segurança WS**

## <a name="ws_request_security_token_property_trust_version"></a>\_versão de \_ \_ confiança da Propriedade do token de segurança \_ da \_ solicitação WS \_

Esta seção se aplica quando a restrição de associação de segurança de [**\_ mensagem de token de \_ segurança de mensagens de símbolo \_ \_ \_ \_ emitida WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) é especificada. As seguintes declarações de política são usadas para identificar a [**\_ \_ versão de confiança do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) e as opções associadas.

``` syntax
<sp:Trust10> => WS_TRUST_VERSION_FEBRUARY_2005
    <sp:Policy>
        <sp:MustSupportClientChallenge/> ?
        <sp:MustSupportServerChallenge/> ?
        <sp:RequireClientEntropy/> ?
        <sp:RequireServerEntropy/> ?
        <sp:MustSupportIssuedTokens/> ?
    </sp:Policy>
</sp:Trust10>
```

A versão de confiança pode ser especificada usando [**a \_ \_ restrição de \_ \_ Propriedade do \_ token de segurança de solicitação WS**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) com uma ID de propriedade da [**\_ \_ \_ \_ \_ \_ versão de confiança da propriedade de token de segurança de solicitação do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).

## <a name="ws_security_property_security_header_version"></a>\_versão do \_ cabeçalho de segurança da propriedade de segurança WS \_ \_ \_

Esta seção se aplica quando qualquer uma das seguintes restrições de associação é usada:

-   [**\_restrição de \_ \_ Associação de segurança de mensagem APREQ \_ \_ do WS Kerberos \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_restrição de \_ Associação de segurança de mensagem WS username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_restrição de \_ Associação de segurança de mensagem de certificado WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_restrição de \_ \_ Associação de segurança de mensagem de token emitida \_ WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

A versão de segurança do cabeçalho (conforme especificado pela versão do cabeçalho de segurança da propriedade de segurança do WS) é determinada por uma das seguintes declarações de política: [**\_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a>Restrições com layout de segurança de cabeçalho

Esta seção se aplica quando qualquer uma das seguintes restrições de associação é usada:

-   [**\_restrição de \_ \_ Associação de segurança de mensagem APREQ \_ \_ do WS Kerberos \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_restrição de \_ Associação de segurança de mensagem WS username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_restrição de \_ Associação de segurança de mensagem de certificado WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_restrição de \_ \_ Associação de segurança de mensagem de token emitida \_ WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

O layout do cabeçalho de segurança (conforme especificado pelo layout do cabeçalho de segurança da propriedade de segurança do WS) é determinado por uma das seguintes declarações de política: [**\_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:Lax.../> => WS_SECURITY_HEADER_LAYOUT_LAX
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:Strict.../> => WS_SECURITY_HEADER_LAYOUT_STRICT
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:LaxTsFirst.../> => WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_FIRST
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:Layout>
            <sp:LaxTsLast.../> => WS_SECURITY_HEADER_LAYOUT_LAX_WITH_TIMESTAMP_LAST
        </sp:Layout>
    </wsp:Policy>
</sp:TransportBinding>
```

## <a name="constraints-with-timestamp-security"></a>Restrições com segurança de carimbo de data/hora

Esta seção se aplica quando qualquer uma das seguintes restrições de associação é usada:

-   [**\_restrição de \_ \_ Associação de segurança de mensagem APREQ \_ \_ do WS Kerberos \_**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**\_restrição de \_ Associação de segurança de mensagem WS username \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**\_restrição de \_ Associação de segurança de mensagem de certificado WS \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**\_restrição de \_ \_ Associação de segurança de mensagem de token emitida \_ WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Se um carimbo de data/hora está ou não incluído no cabeçalho de segurança (conforme especificado pelo [**\_ uso de carimbo de \_ \_ data/hora \_ da propriedade de segurança do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)), é determinado pela presença do SP: IncludeTimestamp no seguinte local:

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

Se a declaração SP: IncludeTimestamp estiver presente, o valor da política será [**o \_ uso do carimbo de \_ data/hora do WS Security \_ \_ sempre**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

Se a declaração SP: IncludeTimestamp não estiver presente, o valor da política será [**o \_ uso do carimbo de \_ data/hora do WS Security \_ \_ nunca**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

 

 




