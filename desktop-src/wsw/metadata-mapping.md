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
# <a name="metadata-mapping"></a><span data-ttu-id="63772-106">Mapeamento de metadados</span><span class="sxs-lookup"><span data-stu-id="63772-106">Metadata Mapping</span></span>

<span data-ttu-id="63772-107">O conteúdo de um documento de metadados é mapeado para a API de metadados das maneiras explicadas nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="63772-107">The contents of a metadata document map to the metadata API in the ways explained in the following sections.</span></span>


<span data-ttu-id="63772-108">Os seguintes prefixos de namespace são usados em toda esta documentação:</span><span class="sxs-lookup"><span data-stu-id="63772-108">The following namespace prefixes are used throughout this documentation:</span></span>

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

<span data-ttu-id="63772-109">As seções subsequentes descrevem as construções de API junto com quais construções de metadados (WSDL ou política) correspondem.</span><span class="sxs-lookup"><span data-stu-id="63772-109">The subsequent sections describe API constructs along with what metadata constructs (WSDL or Policy) they correspond to.</span></span>

<span data-ttu-id="63772-110">A familiaridade com especificações de metadados como WSDL e política ajudará a entender esta seção.</span><span class="sxs-lookup"><span data-stu-id="63772-110">Familiarity with metadata specifications such as WSDL and Policy will aid in understanding this section.</span></span>

## <a name="endpoint-address"></a><span data-ttu-id="63772-111">Endereço do ponto de extremidade</span><span class="sxs-lookup"><span data-stu-id="63772-111">Endpoint address</span></span>

<span data-ttu-id="63772-112">O endereço de um ponto de extremidade (consulte o [**\_ \_ endereço do ponto de extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) é obtido de um elemento de extensibilidade dentro do elemento wsdl: Port do documento WSDL.</span><span class="sxs-lookup"><span data-stu-id="63772-112">The address of an endpoint (see [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address)) is obtained from an extensibility element within the wsdl:port element of the WSDL document.</span></span> <span data-ttu-id="63772-113">Os seguintes elementos de extensibilidade têm suporte para especificar o endereço:</span><span class="sxs-lookup"><span data-stu-id="63772-113">The following extensibility elements are supported for specifying the address:</span></span>

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

## <a name="ws_channel_binding"></a><span data-ttu-id="63772-114">Associação de WS \_ Channel \_</span><span class="sxs-lookup"><span data-stu-id="63772-114">WS\_CHANNEL\_BINDING</span></span>

<span data-ttu-id="63772-115">A associação de canal ( [**consulte \_ \_ Associação de WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) é determinada pelo transporte da Associação SOAP usada, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="63772-115">The channel binding (see [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)) is determined by the transport the soap binding used, as follows:</span></span>

``` syntax
<soap:binding transport=&quot;http://schemas.microsoft.com/soap/tcp&quot;/> => WS_TCP_CHANNEL_BINDING
```

``` syntax
<soap:binding transport=&quot;http://schemas.xmlsoap.org/soap/http&quot;/> => WS_HTTP_CHANNEL_BINDING
```

## <a name="ws_channel_property_envelope_version"></a><span data-ttu-id="63772-116">\_versão do \_ envelope da propriedade \_ \_ do WS Channel</span><span class="sxs-lookup"><span data-stu-id="63772-116">WS\_CHANNEL\_PROPERTY\_ENVELOPE\_VERSION</span></span>

<span data-ttu-id="63772-117">A versão do envelope (consulte a [**versão do envelope da Propriedade do WS \_ Channel \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) é determinada pela qual a associação SOAP é usada, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="63772-117">The envelope version (see [**WS\_CHANNEL\_PROPERTY\_ENVELOPE\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by which soap binding is used, as follows:</span></span>

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

## <a name="addressing-version"></a><span data-ttu-id="63772-118">Versão de endereçamento</span><span class="sxs-lookup"><span data-stu-id="63772-118">Addressing Version</span></span>

<span data-ttu-id="63772-119">A versão de endereçamento (consulte [**\_ \_ \_ \_ versão de endereçamento de Propriedade do WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) é determinada pelas seguintes asserções na política de ponto de extremidade:</span><span class="sxs-lookup"><span data-stu-id="63772-119">The addressing version (see [**WS\_CHANNEL\_PROPERTY\_ADDRESSING\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by the following assertions in the endpoint policy:</span></span>

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

<span data-ttu-id="63772-120">Se uma declaração de endereçamento não estiver presente, o [**\_ transporte da \_ versão \_ de endereçamento do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) será assumido.</span><span class="sxs-lookup"><span data-stu-id="63772-120">If an addressing assertion is not present, then [**WS\_ADDRESSING\_VERSION\_TRANSPORT**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) is assumed.</span></span>

## <a name="message-encoding"></a><span data-ttu-id="63772-121">Decodificador de mensagens</span><span class="sxs-lookup"><span data-stu-id="63772-121">Message Encoding</span></span>

<span data-ttu-id="63772-122">A codificação da mensagem (consulte [**codificação de \_ \_ propriedade \_ de WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) é determinada pelas seguintes asserções na política de ponto de extremidade:</span><span class="sxs-lookup"><span data-stu-id="63772-122">The encoding of the message (see [**WS\_CHANNEL\_PROPERTY\_ENCODING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)) is determined by the following assertions in the endpoint policy:</span></span>

``` syntax
<wsp:Policy...>
    <binp:BinaryEncoding.../> => WS_ENCODING_XML_BINARY_SESSION_1, WS_ENCODING_XML_BINARY_1
</wsp:Policy>
```

<span data-ttu-id="63772-123">Observe que a declaração de diretiva de codificação binária não inclui informações sobre se a codificação binária é sessão ou sem sessão.</span><span class="sxs-lookup"><span data-stu-id="63772-123">Note that the binary encoding policy assertion does not include information about whether the binary encoding is sessionful or sessionless.</span></span> <span data-ttu-id="63772-124">Isso é determinado pela restrição de propriedade de codificação (que deve ser apropriada de acordo com o [**tipo de \_ canal \_ do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) ou não que está sendo usado é sessão ou não).</span><span class="sxs-lookup"><span data-stu-id="63772-124">This is determined by the encoding property constraint (which should be appropriate according to whether or not the [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) being used is sessionful or not).</span></span>

``` syntax
<wsp:Policy...>
    <mtomp:OptimizedMimeSerialization.../> => WS_ENCODING_XML_MTOM_UTF8, WS_ENCODING_XML_MTOM_UTF16LE, WS_ENCODING_XML_MTOM_UTF16BE
</wsp:Policy>
```

<span data-ttu-id="63772-125">Se nenhuma das declarações acima estiver presente, uma codificação de texto será usada: [**WS \_ Encoding \_ XML \_ UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS \_ Encoding \_ XML \_ UTF16LE**, **WS \_ Encoding \_ XML \_ UTF16BE**.</span><span class="sxs-lookup"><span data-stu-id="63772-125">If neither of the above assertions are present, then a text encoding is used: [**WS\_ENCODING\_XML\_UTF8**](/windows/desktop/api/WebServices/ne-webservices-ws_encoding), **WS\_ENCODING\_XML\_UTF16LE**, **WS\_ENCODING\_XML\_UTF16BE**.</span></span>

<span data-ttu-id="63772-126">Observe que a política não inclui informações sobre o conjunto de caracteres para MTOM ou codificações de texto (seja UTF8, UTF16LE ou UTF16BE).</span><span class="sxs-lookup"><span data-stu-id="63772-126">Note that policy does not include information about the character set for MTOM or text encodings (whether it is UTF8, UTF16LE or UTF16BE).</span></span> <span data-ttu-id="63772-127">O valor do conjunto de caracteres real usado é determinado pela restrição de propriedade de codificação.</span><span class="sxs-lookup"><span data-stu-id="63772-127">The actual character set value used is determined by the encoding property constraint.</span></span>

## <a name="constraints-with-http-header-authentication"></a><span data-ttu-id="63772-128">Restrições com autenticação de cabeçalho HTTP</span><span class="sxs-lookup"><span data-stu-id="63772-128">Constraints with HTTP Header Authentication</span></span>

<span data-ttu-id="63772-129">Esta seção se aplica quando a restrição de associação de segurança de [**\_ restrição de \_ \_ \_ \_ Associação \_ de segurança do cabeçalho HTTP do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) é especificada.</span><span class="sxs-lookup"><span data-stu-id="63772-129">This section applies when the [**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint) security binding constraint is specified.</span></span>

<span data-ttu-id="63772-130">Essa associação de segurança é indicada na política por asserções diferentes que afirma que a autenticação do cabeçalho HTTP deve ser usada e que um esquema de autenticação específico deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="63772-130">This security binding is indicated in the policy by different assertions that states both that HTTP header authentication should be used, and that a particular authentication scheme should be used.</span></span> <span data-ttu-id="63772-131">As declarações de política correspondem aos valores do esquema de [**\_ autenticação do \_ \_ \_ \_ cabeçalho \_ \_ http da propriedade de associação de segurança do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="63772-131">The policy assertions correspond to the values of the [**WS\_SECURITY\_BINDING\_PROPERTY\_HTTP\_HEADER\_AUTH\_SCHEME**](/windows/desktop/api/WebServices/ne-webservices-ws_security_binding_property_id) as follows:</span></span>

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

## <a name="constraints-with-sll-transport-security"></a><span data-ttu-id="63772-132">Restrições com segurança de transporte SLL</span><span class="sxs-lookup"><span data-stu-id="63772-132">Constraints with SLL Transport Security</span></span>

<span data-ttu-id="63772-133">Esta seção se aplica quando a restrição de associação de segurança de [**restrição de associação de \_ segurança de \_ transporte \_ \_ \_ WS SSL**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) é especificada.</span><span class="sxs-lookup"><span data-stu-id="63772-133">This section applies when the [**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="63772-134">As seguintes declarações de política são usadas neste caso:</span><span class="sxs-lookup"><span data-stu-id="63772-134">The following policy assertions are used in this case:</span></span>

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

## <a name="constraints-with-sspi-transport-security"></a><span data-ttu-id="63772-135">Restrições com segurança de transporte SSPI</span><span class="sxs-lookup"><span data-stu-id="63772-135">Constraints with SSPI Transport Security</span></span>

<span data-ttu-id="63772-136">Esta seção se aplica quando a restrição de associação de segurança de [**restrição de associação de segurança de transporte do WS \_ TCP \_ SSPI \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) é especificada.</span><span class="sxs-lookup"><span data-stu-id="63772-136">This section applies when the [**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="63772-137">As seguintes declarações de política são usadas neste caso:</span><span class="sxs-lookup"><span data-stu-id="63772-137">The following policy assertions are used in this case:</span></span>

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

## <a name="constrains-with-transport-security"></a><span data-ttu-id="63772-138">Restrições com segurança de transporte</span><span class="sxs-lookup"><span data-stu-id="63772-138">Constrains with Transport Security</span></span>

<span data-ttu-id="63772-139">A restrição de Propriedade do [**\_ \_ \_ \_ \_ nível de proteção da propriedade de segurança WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) pode ser especificada se qualquer uma das restrições de associação de segurança for especificada:</span><span class="sxs-lookup"><span data-stu-id="63772-139">The [**WS\_SECURITY\_PROPERTY\_TRANSPORT\_PROTECTION\_LEVEL**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id) property constraint can be specified if any of the security binding constraints are specified:</span></span>

-   [<span data-ttu-id="63772-140">**\_restrição de \_ Associação de segurança de transporte WS SSL \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63772-140">**WS\_SSL\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_ssl_transport_security_binding_constraint)

    <span data-ttu-id="63772-141">O valor da política sempre é [**o \_ nível de proteção WS \_ \_ -Sign \_ e \_ Encrypt**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span><span class="sxs-lookup"><span data-stu-id="63772-141">The value from policy is always [**WS\_PROTECTION\_LEVEL\_SIGN\_AND\_ENCRYPT**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span></span>

-   [<span data-ttu-id="63772-142">**restrição de associação de segurança de transporte do WS \_ TCP \_ SSPI \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63772-142">**WS\_TCP\_SSPI\_TRANSPORT\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_tcp_sspi_transport_security_binding_constraint)

    <span data-ttu-id="63772-143">O valor da política é especificado como parte da asserção WindowsTransportSecurity, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="63772-143">The value from policy is specified as part of the WindowsTransportSecurity assertion, as follows:</span></span>

    ``` syntax
    <netf:WindowsTransportSecurity...>None</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_NONE
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>Sign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN
    ```

    ``` syntax
    <netf:WindowsTransportSecurity...>EncryptAndSign</netf:WindowsTransportSecurity> => WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT
    ```

-   [<span data-ttu-id="63772-144">**\_restrição de \_ \_ Associação de segurança de autenticação de cabeçalho \_ http \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="63772-144">**WS\_HTTP\_HEADER\_AUTH\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_http_header_auth_security_binding_constraint)

    <span data-ttu-id="63772-145">O valor da política sempre é [**o \_ \_ nível de \_ proteção WS**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span><span class="sxs-lookup"><span data-stu-id="63772-145">The value from policy is always [**WS\_PROTECTION\_LEVEL\_NONE**](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level).</span></span>

## <a name="constraints-with-kerberos-apreq-security-binding"></a><span data-ttu-id="63772-146">Restrições com a associação de segurança APREQ Kerberos</span><span class="sxs-lookup"><span data-stu-id="63772-146">Constraints with Kerberos APREQ Security Binding</span></span>

<span data-ttu-id="63772-147">Esta seção se aplica quando a restrição de associação de segurança de restrição de associação de segurança de [**mensagem de APREQ do WS \_ \_ \_ \_ \_ \_ Kerberos**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) é especificada.</span><span class="sxs-lookup"><span data-stu-id="63772-147">This section applies when the [**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="63772-148">As seguintes declarações de política são usadas neste caso:</span><span class="sxs-lookup"><span data-stu-id="63772-148">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens...>
    <wsp:Policy>
        <sp:KerberosToken>
            <WssGssKerberosV5ApReqToken11.../>
        </sp:KerberosToken>
    </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="constraints-with-message-security-binding"></a><span data-ttu-id="63772-149">Restrições com associação de segurança de mensagem</span><span class="sxs-lookup"><span data-stu-id="63772-149">Constraints with Message Security Binding</span></span>

<span data-ttu-id="63772-150">Esta seção se aplica quando a restrição de associação de segurança de [**\_ \_ \_ \_ \_ restrição**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) de segurança de mensagem do WS-nomedeusuário é especificada.</span><span class="sxs-lookup"><span data-stu-id="63772-150">This section applies when the [**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="63772-151">As seguintes declarações de política são usadas neste caso:</span><span class="sxs-lookup"><span data-stu-id="63772-151">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:SignedSupportingTokens>
    <wsp:Policy>
        <sp:UsernameToken.../>
    </wsp:Policy>
</sp:SignedSupportingTokens>
```

## <a name="ws_cert_message_security_binding_constraint"></a><span data-ttu-id="63772-152">\_restrição de \_ Associação de segurança de mensagem de certificado WS \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="63772-152">WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="63772-153">Esta seção se aplica quando a restrição de associação de segurança de [**restrição de associação de segurança de \_ mensagem de certificado \_ \_ \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) é especificada.</span><span class="sxs-lookup"><span data-stu-id="63772-153">This section applies when the [**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="63772-154">As seguintes declarações de política são usadas neste caso:</span><span class="sxs-lookup"><span data-stu-id="63772-154">The following policy assertions are used in this case:</span></span>

``` syntax
<sp:EndorsingSupportingTokens>
    <wsp:Policy>
        <sp:X509Token.../>
   </wsp:Policy>
</sp:EndorsingSupportingTokens>
```

## <a name="ws_issued_token_message_security_binding_constraint"></a><span data-ttu-id="63772-155">\_restrição de \_ \_ Associação de segurança de mensagem de token emitida \_ WS \_ \_</span><span class="sxs-lookup"><span data-stu-id="63772-155">WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="63772-156">Esta seção se aplica quando a restrição de associação de segurança de [**\_ mensagem de token de \_ segurança de mensagens de símbolo \_ \_ \_ \_ emitida WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) é especificada.</span><span class="sxs-lookup"><span data-stu-id="63772-156">This section applies when the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="63772-157">As seguintes declarações de política são usadas neste caso:</span><span class="sxs-lookup"><span data-stu-id="63772-157">The following policy assertions are used in this case:</span></span>

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

<span data-ttu-id="63772-158">O seguinte descreve o mapeamento de campos da [**restrição de \_ \_ Associação de \_ \_ segurança de \_ \_ mensagem de token emitida pelo WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) para a política acima:</span><span class="sxs-lookup"><span data-stu-id="63772-158">The following describes the mapping of fields of the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) to the above policy:</span></span>

-   <span data-ttu-id="63772-159">O campo claimConstraints é usado para verificar o conjunto de URIs de tipo de declaração que aparecem dentro do elemento WSI: ClaimType acima.</span><span class="sxs-lookup"><span data-stu-id="63772-159">The claimConstraints field is used to verify the set of claim type URIs that appear within the wsi:ClaimType element above.</span></span>

-   <span data-ttu-id="63772-160">O campo issuerAddress corresponde ao elemento WSP: emissor acima, que é o endereço do [**\_ ponto de \_ extremidade WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) do serviço que pode emitir o token.</span><span class="sxs-lookup"><span data-stu-id="63772-160">The issuerAddress field corresponds to the wsp:Issuer element above, which is the [**WS\_ENDPOINT\_ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) of the service that can issue the token.</span></span>

-   <span data-ttu-id="63772-161">O campo requestSecurityTokenTemplate corresponde aos elementos filho do elemento WSP: RequestSecurityTokenTemplate.</span><span class="sxs-lookup"><span data-stu-id="63772-161">The requestSecurityTokenTemplate field corresponds to the child elements of the wsp:RequestSecurityTokenTemplate element.</span></span>

## <a name="ws_security_context_message_security_binding_constraint"></a><span data-ttu-id="63772-162">\_restrição de \_ \_ Associação de segurança de mensagem de contexto \_ de \_ segurança WS \_</span><span class="sxs-lookup"><span data-stu-id="63772-162">WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT</span></span>

<span data-ttu-id="63772-163">Esta seção se aplica quando a restrição de associação de segurança da [**\_ \_ mensagem de contexto \_ \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) de segurança do WS Security é especificada.</span><span class="sxs-lookup"><span data-stu-id="63772-163">This section applies when the [**WS\_SECURITY\_CONTEXT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_security_context_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="63772-164">As seguintes declarações de política são usadas neste caso:</span><span class="sxs-lookup"><span data-stu-id="63772-164">The following policy assertions are used in this case:</span></span>

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

<span data-ttu-id="63772-165">O modo de entropia é determinado pela asserção <SP: Trust10>.</span><span class="sxs-lookup"><span data-stu-id="63772-165">The entropy mode is determined by the <sp:Trust10> assertion.</span></span> <span data-ttu-id="63772-166"><SP: RequireClientEntropy/> e <SP: RequireServerEntropy/> => [**\_ modo de entropia de chave de segurança ws \_ \_ \_ \_ combinado**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <SP: RequireClientEntropy/> => modo de entropia de chave de **segurança WS \_ \_ \_ \_ \_ \_ somente** <SP: RequireServerEntropy/> => **\_ \_ \_ \_ \_ \_ somente servidor do modo de entropia de chave de segurança WS**</span><span class="sxs-lookup"><span data-stu-id="63772-166"><sp:RequireClientEntropy/> and <sp:RequireServerEntropy/> => [**WS\_SECURITY\_KEY\_ENTROPY\_MODE\_COMBINED**](/windows/desktop/api/WebServices/ne-webservices-ws_security_key_entropy_mode) <sp:RequireClientEntropy/> => **WS\_SECURITY\_KEY\_ENTROPY\_MODE\_CLIENT\_ONLY** <sp:RequireServerEntropy/> => **WS\_SECURITY\_KEY\_ENTROPY\_MODE\_SERVER\_ONLY**</span></span>

## <a name="ws_request_security_token_property_trust_version"></a><span data-ttu-id="63772-167">\_versão de \_ \_ confiança da Propriedade do token de segurança \_ da \_ solicitação WS \_</span><span class="sxs-lookup"><span data-stu-id="63772-167">WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_TRUST\_VERSION</span></span>

<span data-ttu-id="63772-168">Esta seção se aplica quando a restrição de associação de segurança de [**\_ mensagem de token de \_ segurança de mensagens de símbolo \_ \_ \_ \_ emitida WS**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) é especificada.</span><span class="sxs-lookup"><span data-stu-id="63772-168">This section applies when the [**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint) security binding constraint is specified.</span></span> <span data-ttu-id="63772-169">As seguintes declarações de política são usadas para identificar a [**\_ \_ versão de confiança do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) e as opções associadas.</span><span class="sxs-lookup"><span data-stu-id="63772-169">The following policy assertions are used to identify the [**WS\_TRUST\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_trust_version) and associated options.</span></span>

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

<span data-ttu-id="63772-170">A versão de confiança pode ser especificada usando [**a \_ \_ restrição de \_ \_ Propriedade do \_ token de segurança de solicitação WS**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) com uma ID de propriedade da [**\_ \_ \_ \_ \_ \_ versão de confiança da propriedade de token de segurança de solicitação do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).</span><span class="sxs-lookup"><span data-stu-id="63772-170">The trust version can be specified using the [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_CONSTRAINT**](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property_constraint) with a property id of [**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_TRUST\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id).</span></span>

## <a name="ws_security_property_security_header_version"></a><span data-ttu-id="63772-171">\_versão do \_ cabeçalho de segurança da propriedade de segurança WS \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="63772-171">WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_VERSION</span></span>

<span data-ttu-id="63772-172">Esta seção se aplica quando qualquer uma das seguintes restrições de associação é usada:</span><span class="sxs-lookup"><span data-stu-id="63772-172">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="63772-173">**\_restrição de \_ \_ Associação de segurança de mensagem APREQ \_ \_ do WS Kerberos \_**</span><span class="sxs-lookup"><span data-stu-id="63772-173">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="63772-174">**\_restrição de \_ Associação de segurança de mensagem WS username \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63772-174">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="63772-175">**\_restrição de \_ Associação de segurança de mensagem de certificado WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63772-175">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="63772-176">**\_restrição de \_ \_ Associação de segurança de mensagem de token emitida \_ WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63772-176">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="63772-177">A versão de segurança do cabeçalho (conforme especificado pela versão do cabeçalho de segurança da propriedade de segurança do WS) é determinada por uma das seguintes declarações de política: [**\_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)</span><span class="sxs-lookup"><span data-stu-id="63772-177">The header security version (as specified by [**WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_VERSION**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by one of the following policy assertions:</span></span>

``` syntax
<wsp:Wss10> ... </wsp:Wss10> => WS_SECURITY_HEADER_VERSION_1_0
```

``` syntax
<wsp:Wss11> ... </wsp:Wss11> => WS_SECURITY_HEADER_VERSION_1_1
```

## <a name="constraints-with-header-security-layout"></a><span data-ttu-id="63772-178">Restrições com layout de segurança de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="63772-178">Constraints with Header Security Layout</span></span>

<span data-ttu-id="63772-179">Esta seção se aplica quando qualquer uma das seguintes restrições de associação é usada:</span><span class="sxs-lookup"><span data-stu-id="63772-179">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="63772-180">**\_restrição de \_ \_ Associação de segurança de mensagem APREQ \_ \_ do WS Kerberos \_**</span><span class="sxs-lookup"><span data-stu-id="63772-180">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="63772-181">**\_restrição de \_ Associação de segurança de mensagem WS username \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63772-181">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="63772-182">**\_restrição de \_ Associação de segurança de mensagem de certificado WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63772-182">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="63772-183">**\_restrição de \_ \_ Associação de segurança de mensagem de token emitida \_ WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63772-183">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="63772-184">O layout do cabeçalho de segurança (conforme especificado pelo layout do cabeçalho de segurança da propriedade de segurança do WS) é determinado por uma das seguintes declarações de política: [**\_ \_ \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)</span><span class="sxs-lookup"><span data-stu-id="63772-184">The security header layout (as specified by [**WS\_SECURITY\_PROPERTY\_SECURITY\_HEADER\_LAYOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by one of the following policy assertions:</span></span>

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

## <a name="constraints-with-timestamp-security"></a><span data-ttu-id="63772-185">Restrições com segurança de carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="63772-185">Constraints with Timestamp Security</span></span>

<span data-ttu-id="63772-186">Esta seção se aplica quando qualquer uma das seguintes restrições de associação é usada:</span><span class="sxs-lookup"><span data-stu-id="63772-186">This section applies when any of the following binding constraints are used:</span></span>

-   [<span data-ttu-id="63772-187">**\_restrição de \_ \_ Associação de segurança de mensagem APREQ \_ \_ do WS Kerberos \_**</span><span class="sxs-lookup"><span data-stu-id="63772-187">**WS\_KERBEROS\_APREQ\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_kerberos_apreq_message_security_binding_constraint)
-   [<span data-ttu-id="63772-188">**\_restrição de \_ Associação de segurança de mensagem WS username \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63772-188">**WS\_USERNAME\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_username_message_security_binding_constraint)
-   [<span data-ttu-id="63772-189">**\_restrição de \_ Associação de segurança de mensagem de certificado WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63772-189">**WS\_CERT\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_cert_message_security_binding_constraint)
-   [<span data-ttu-id="63772-190">**\_restrição de \_ \_ Associação de segurança de mensagem de token emitida \_ WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="63772-190">**WS\_ISSUED\_TOKEN\_MESSAGE\_SECURITY\_BINDING\_CONSTRAINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_issued_token_message_security_binding_constraint)

<span data-ttu-id="63772-191">Se um carimbo de data/hora está ou não incluído no cabeçalho de segurança (conforme especificado pelo [**\_ uso de carimbo de \_ \_ data/hora \_ da propriedade de segurança do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)), é determinado pela presença do SP: IncludeTimestamp no seguinte local:</span><span class="sxs-lookup"><span data-stu-id="63772-191">Whether or not a timestamp is included in the security header (as specified by [**WS\_SECURITY\_PROPERTY\_TIMESTAMP\_USAGE**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)) is determined by the presence of the sp:IncludeTimestamp in the following location:</span></span>

``` syntax
<sp:TransportBinding>
    <wsp:Policy>
        <sp:IncludeTimestamp.../>
    </wsp:Policy>
</sp:TransportBinding>
```

<span data-ttu-id="63772-192">Se a declaração SP: IncludeTimestamp estiver presente, o valor da política será [**o \_ uso do carimbo de \_ data/hora do WS Security \_ \_ sempre**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span><span class="sxs-lookup"><span data-stu-id="63772-192">If the sp:IncludeTimestamp assertion is present, the value from policy is [**WS\_SECURITY\_TIMESTAMP\_USAGE\_ALWAYS**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span></span>

<span data-ttu-id="63772-193">Se a declaração SP: IncludeTimestamp não estiver presente, o valor da política será [**o \_ uso do carimbo de \_ data/hora do WS Security \_ \_ nunca**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span><span class="sxs-lookup"><span data-stu-id="63772-193">If the sp:IncludeTimestamp assertion is not present, the value from policy is [**WS\_SECURITY\_TIMESTAMP\_USAGE\_NEVER**](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage).</span></span>

 

 




