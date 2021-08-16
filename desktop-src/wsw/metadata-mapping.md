---
title: Mapeamento de metadados
description: O conteúdo de um documento de metadados é mapeado para a API de metadados das maneiras explicadas nas seções a seguir.
ms.assetid: 266f8319-b7ac-497f-8eb7-8e2c7bcede33
keywords:
- Serviços Web de mapeamento de metadados para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57e6577e05f1d51ec13cc917465c306b94c403827149b086f252a38964997ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841486"
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

As seções subsequentes descrevem constructos de API juntamente com quais constructos de metadados (WSDL ou Política) eles correspondem.

A familiaridade com especificações de metadados, como WSDL e Política, auxiliará no entendimento desta seção.

## <a name="endpoint-address"></a>Endereço do ponto de extremidade

O endereço de um ponto de extremidade (consulte ENDEREÇO DO PONTO DE EXTREMIDADE do [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) é obtido de um elemento de extensibilidade dentro do elemento wsdl:port do documento WSDL. Os seguintes elementos de extensibilidade têm suporte para especificar o endereço:

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

## <a name="ws_channel_binding"></a>ASSOCIAÇÃO DE \_ CANAL \_ WS

A associação de canal (consulte [**WS \_ CHANNEL \_ BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) é determinada pelo transporte da associação de soap usada, da seguinte forma:

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a>VERSÃO DO ENVELOPE DA \_ \_ PROPRIEDADE DO CANAL \_ \_ WS

A versão do envelope (consulte [**WS \_ CHANNEL PROPERTY ENVELOPE \_ \_ \_ VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) é determinada pela qual a associação de soap é usada, da seguinte forma:

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

A versão de endereçamento (consulte VERSÃO DE ENDEREÇAMENTO DE PROPRIEDADE DO CANAL DO WS ) é determinada pelas seguintes declarações na política de ponto de extremidade: [**\_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)

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

Se uma declaração de endereçamento não estiver presente, o [**WS \_ ADDRESSING VERSION \_ \_ TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) será assumido.

## <a name="message-encoding"></a>Decodificador de mensagens

A codificação da mensagem (consulte CODIFICAÇÃO DE PROPRIEDADE DO [**CANAL WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) é determinada pelas seguintes declarações na política de ponto de extremidade:

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

Observe que a declaração de política de codificação binária não inclui informações sobre se a codificação binária é com sessão ou sem sessão. Isso é determinado pela restrição de propriedade de codificação (que deve ser apropriada de acordo com se o TIPO de [**\_ CANAL \_ do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) que está sendo usado é com sessão ou não).

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

Se nenhuma das declarações acima estiver presente, uma codificação de texto será usada: [**WS \_ ENCODING \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS \_ ENCODING \_ XML \_ UTF16LE**, **WS \_ ENCODING \_ XML \_ UTF16BE**.

Observe que a política não inclui informações sobre o conjunto de caracteres para codificações MTOM ou de texto (seja UTF8, UTF16LE ou UTF16BE). O valor real do conjunto de caracteres usado é determinado pela restrição de propriedade de codificação.

## <a name="constraints-with-http-header-authentication"></a>Restrições com autenticação de cabeçalho HTTP

Esta seção se aplica quando a restrição de associação de segurança DE ASSOCIAÇÃO DE SEGURANÇA DE AUTENTICAÇÃO DE CABEÇALHO HTTP do WS é especificada. [**\_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

Essa associação de segurança é indicada na política por diferentes declarações que declaram que a autenticação de cabeçalho HTTP deve ser usada e que um esquema de autenticação específico deve ser usado. As declarações de política correspondem aos valores do ESQUEMA DE AUTENTICAÇÃO DE CABEÇALHO HTTP DA PROPRIEDADE DE ASSOCIAÇÃO DE SEGURANÇA do WS da seguinte forma: [**\_ \_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id)

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

## <a name="constraints-with-sll-transport-security"></a>Restrições com segurança de transporte de SLL

Esta seção se aplica quando a restrição de associação de segurança DE RESTRIÇÃO DE SEGURANÇA DE TRANSPORTE [**DO SSL do \_ WS \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) é especificada. As seguintes declarações de política são usadas nesse caso:

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

Esta seção se aplica quando a restrição de associação de [**\_ segurança TCP \_ SSPI TRANSPORT \_ SECURITY BINDING \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) do WS é especificada. As seguintes declarações de política são usadas nesse caso:

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

A [**restrição de propriedade WS \_ SECURITY PROPERTY TRANSPORT PROTECTION \_ \_ \_ \_ LEVEL**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) poderá ser especificada se qualquer uma das restrições de associação de segurança for especificada:

-   [**RESTRIÇÃO DE \_ ASSOCIAÇÃO DE SEGURANÇA DE TRANSPORTE SSL \_ \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    O valor da política é sempre [**WS \_ PROTECTION LEVEL SIGN AND \_ \_ \_ \_ ENCRYPT.**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)

-   [**RESTRIÇÃO DE ASSOCIAÇÃO DE SEGURANÇA DE TRANSPORTE \_ \_ TCP SSPI \_ \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    O valor da política é especificado como parte da declaração WindowsTransportSecurity, da seguinte forma:

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [**RESTRIÇÃO DE ASSOCIAÇÃO DE SEGURANÇA \_ \_ DE \_ AUTENTICAÇÃO DE \_ \_ CABEÇALHO HTTP \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    O valor da política é sempre [**WS \_ PROTECTION LEVEL \_ \_ NONE.**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)

## <a name="constraints-with-kerberos-apreq-security-binding"></a>Restrições com associação de segurança kerberos APREQ

Esta seção se aplica quando a restrição de associação de segurança [**\_ WS KERBEROS \_ APREQ \_ MESSAGE SECURITY \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) é especificada. As seguintes declarações de política são usadas nesse caso:

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

Esta seção se aplica quando a restrição de associação de segurança DE ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE NOME DE USUÁRIO do WS é especificada. [**\_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) As seguintes declarações de política são usadas nesse caso:

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a>RESTRIÇÃO DE ASSOCIAÇÃO DE \_ SEGURANÇA DE MENSAGEM DE \_ \_ \_ CERTIFICADO DO \_ WS

Esta seção se aplica quando a restrição de associação de segurança DE RESTRIÇÃO DE SEGURANÇA DE MENSAGEM DE CERTIFICADO do WS é especificada. [**\_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) As seguintes declarações de política são usadas nesse caso:

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a>RESTRIÇÃO DE ASSOCIAÇÃO DE SEGURANÇA DE \_ MENSAGEM DE TOKEN EMITIDA \_ \_ \_ \_ PELO \_ WS

Esta seção se aplica quando a restrição de associação de [**segurança \_ WS ISSUED \_ TOKEN MESSAGE SECURITY BINDING \_ \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) é especificada. As seguintes declarações de política são usadas nesse caso:

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

O exemplo a seguir descreve o mapeamento de campos da RESTRIÇÃO DE ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE TOKEN EMITIDO PELO WS para a política acima: [**\_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

-   O campo claimConstraints é usado para verificar o conjunto de URIs do tipo de declaração que aparecem dentro do elemento wsi:ClaimType acima.

-   O campo issuerAddress corresponde ao elemento wsp:Issuer acima, que é o ENDEREÇO [**\_ DO PONTO \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) DE EXTREMIDADE do WS do serviço que pode emitir o token.

-   O campo requestSecurityTokenTemplate corresponde aos elementos filho do elemento wsp:RequestSecurityTokenTemplate.

## <a name="ws_security_context_message_security_binding_constraint"></a>RESTRIÇÃO DE ASSOCIAÇÃO DE SEGURANÇA DA MENSAGEM \_ \_ DE CONTEXTO DE \_ \_ \_ SEGURANÇA DO \_ WS

Esta seção se aplica quando a restrição de associação de segurança RESTRIÇÃO DE ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM DE CONTEXTO DE SEGURANÇA do WS é especificada. [**\_ \_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) As seguintes declarações de política são usadas nesse caso:

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

O modo de entropia é determinado pelo <sp:Trust10> declaração. <sp:RequireClientEntropy/> e <sp:RequireServerEntropy/> => MODO [**\_ \_ \_ ENTROPY \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) DE CHAVE DE SEGURANÇA do WS COMBINADO <sp:RequireClientEntropy/> => WS SECURITY KEY **\_ \_ \_ ENTROPY \_ MODE CLIENT \_ ONLY \_** <sp:RequireServerEntropy/> => **WS SECURITY KEY \_ \_ \_ ENTROPY MODE SERVER \_ \_ \_ ONLY**

## <a name="ws_request_security_token_property_trust_version"></a>VERSÃO DE CONFIANÇA \_ DA PROPRIEDADE DO TOKEN DE SEGURANÇA DE \_ \_ \_ \_ \_ SOLICITAÇÃO DO WS

Esta seção se aplica quando a restrição de associação de [**segurança \_ WS ISSUED \_ TOKEN MESSAGE SECURITY BINDING \_ \_ \_ \_ CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) é especificada. As declarações de política a seguir são usadas para identificar a VERSÃO CONFIÁVEL do [**WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) e as opções associadas.

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

A versão de confiança pode ser especificada usando a RESTRIÇÃO DE PROPRIEDADE DO TOKEN DE SEGURANÇA DE SOLICITAÇÃO do WS com uma ID de propriedade da VERSÃO CONFIÁVEL DA PROPRIEDADE DO [**\_ \_ \_ \_ \_ TOKEN**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) DE SEGURANÇA DE SOLICITAÇÃO [**\_ \_ \_ \_ \_ \_ do WS.**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)

## <a name="ws_security_property_security_header_version"></a>VERSÃO DO TÍTULO DE \_ SEGURANÇA DA PROPRIEDADE DE SEGURANÇA \_ \_ \_ DO \_ WS

Esta seção se aplica quando qualquer uma das seguintes restrições de associação é usada:

-   [**RESTRIÇÃO DE ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM \_ \_ KERBEROS APREQ \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**RESTRIÇÃO DE ASSOCIAÇÃO \_ DE SEGURANÇA DE MENSAGEM DE NOME DE USUÁRIO \_ \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**RESTRIÇÃO DE ASSOCIAÇÃO DE \_ SEGURANÇA DE MENSAGEM DE \_ \_ \_ CERTIFICADO DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**RESTRIÇÃO DE ASSOCIAÇÃO DE SEGURANÇA DE \_ MENSAGEM DE TOKEN EMITIDA \_ \_ \_ \_ PELO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

A versão de segurança do título (conforme especificado por [**WS \_ SECURITY PROPERTY SECURITY \_ \_ \_ HEADER \_ VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) é determinada por uma das seguintes declarações de política:

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a>Restrições com layout de segurança de título

Esta seção se aplica quando qualquer uma das seguintes restrições de associação é usada:

-   [**RESTRIÇÃO DE ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM \_ \_ KERBEROS APREQ \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**RESTRIÇÃO DE ASSOCIAÇÃO \_ DE SEGURANÇA DE MENSAGEM DE NOME DE USUÁRIO \_ \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**RESTRIÇÃO DE ASSOCIAÇÃO DE \_ SEGURANÇA DE MENSAGEM DE \_ \_ \_ CERTIFICADO DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**RESTRIÇÃO DE ASSOCIAÇÃO DE SEGURANÇA DE \_ MENSAGEM DE TOKEN EMITIDA \_ \_ \_ \_ PELO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

O layout do título de segurança (conforme especificado pelo LAYOUT DO [**\_ \_ \_ \_ HEADER \_ DE**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)SEGURANÇA DA PROPRIEDADE DE SEGURANÇA do WS) é determinado por uma das seguintes declarações de política:

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

## <a name="constraints-with-timestamp-security"></a>Restrições com segurança de data/hora

Esta seção se aplica quando qualquer uma das seguintes restrições de associação é usada:

-   [**RESTRIÇÃO DE ASSOCIAÇÃO DE SEGURANÇA DE MENSAGEM \_ \_ KERBEROS APREQ \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [**RESTRIÇÃO DE ASSOCIAÇÃO \_ DE SEGURANÇA DE MENSAGEM DE NOME DE USUÁRIO \_ \_ \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [**RESTRIÇÃO DE ASSOCIAÇÃO DE \_ SEGURANÇA DE MENSAGEM DE \_ \_ \_ CERTIFICADO DO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [**RESTRIÇÃO DE ASSOCIAÇÃO DE SEGURANÇA DE \_ MENSAGEM DE TOKEN EMITIDA \_ \_ \_ \_ PELO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

Se um timestamp está incluído ou não no título de segurança (conforme especificado por USO DE [**\_ \_ \_ TIMESTAMP \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)DA PROPRIEDADE DE SEGURANÇA do WS) é determinado pela presença do sp:IncludeTimestamp no seguinte local:

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

Se a declaração sp:IncludeTimestamp estiver presente, o valor da política será [**WS \_ SECURITY \_ TIMESTAMP \_ USAGE \_ ALWAYS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

Se a declaração sp:IncludeTimestamp não estiver presente, o valor da política será [**WS \_ SECURITY \_ TIMESTAMP \_ USAGE \_ NEVER**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).

 

 




