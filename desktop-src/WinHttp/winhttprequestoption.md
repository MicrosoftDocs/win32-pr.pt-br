---
description: Inclui opções que podem ser definidas ou recuperadas para a sessão atual do WinHTTP (Microsoft Windows HTTP Services).
ms.assetid: 8464d794-b4a8-4c83-9e26-69257000102a
title: Enumeração WinHttpRequestOption
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestOption
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: 32ae65f43cd04027027e43d29c49ed0f68f29c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501717"
---
# <a name="winhttprequestoption-enumeration"></a><span data-ttu-id="c4a72-103">Enumeração WinHttpRequestOption</span><span class="sxs-lookup"><span data-stu-id="c4a72-103">WinHttpRequestOption enumeration</span></span>

<span data-ttu-id="c4a72-104">A enumeração **WinHttpRequestOption** inclui opções que podem ser definidas ou recuperadas para a sessão atual do WinHTTP (Microsoft Windows http Services).</span><span class="sxs-lookup"><span data-stu-id="c4a72-104">The **WinHttpRequestOption** enumeration includes options that can be set or retrieved for the current Microsoft Windows HTTP Services (WinHTTP) session.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4a72-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4a72-105">Syntax</span></span>


```C++
typedef enum WinHttpRequestOption { 
  WinHttpRequestOption_UserAgentString,
  WinHttpRequestOption_URL,
  WinHttpRequestOption_URLCodePage,
  WinHttpRequestOption_EscapePercentInURL,
  WinHttpRequestOption_SslErrorIgnoreFlags,
  WinHttpRequestOption_SelectCertificate,
  WinHttpRequestOption_EnableRedirects,
  WinHttpRequestOption_UrlEscapeDisable,
  WinHttpRequestOption_UrlEscapeDisableQuery,
  WinHttpRequestOption_SecureProtocols,
  WinHttpRequestOption_EnableTracing,
  WinHttpRequestOption_RevertImpersonationOverSsl,
  WinHttpRequestOption_EnableHttpsToHttpRedirects,
  WinHttpRequestOption_EnablePassportAuthentication,
  WinHttpRequestOption_MaxAutomaticRedirects,
  WinHttpRequestOption_MaxResponseHeaderSize,
  WinHttpRequestOption_MaxResponseDrainSize,
  WinHttpRequestOption_EnableHttp1_1,
  WinHttpRequestOption_EnableCertificateRevocationCheck
} WinHttpRequestOption;
```



## <a name="constants"></a><span data-ttu-id="c4a72-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c4a72-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c4a72-107"><span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**Useragentstring do WinHttpRequestOption \_**</span><span class="sxs-lookup"><span data-stu-id="c4a72-107"><span id="WinHttpRequestOption_UserAgentString"></span><span id="winhttprequestoption_useragentstring"></span><span id="WINHTTPREQUESTOPTION_USERAGENTSTRING"></span>**WinHttpRequestOption\_UserAgentString**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-108">Define ou recupera uma **variante** que contém a cadeia de caracteres do [*agente do usuário*](glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="c4a72-108">Sets or retrieves a **VARIANT** that contains the [*user agent*](glossary.md) string.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-109"><span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**URL do WinHttpRequestOption \_**</span><span class="sxs-lookup"><span data-stu-id="c4a72-109"><span id="WinHttpRequestOption_URL"></span><span id="winhttprequestoption_url"></span><span id="WINHTTPREQUESTOPTION_URL"></span>**WinHttpRequestOption\_URL**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-110">Recupera uma **variante** que contém a URL do recurso.</span><span class="sxs-lookup"><span data-stu-id="c4a72-110">Retrieves a **VARIANT** that contains the URL of the resource.</span></span> <span data-ttu-id="c4a72-111">Esse valor é somente leitura; Você não pode definir a URL usando essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="c4a72-111">This value is read-only; you cannot set the URL using this property.</span></span> <span data-ttu-id="c4a72-112">A URL não pode ser lida até que o método [**Open**](iwinhttprequest-open.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="c4a72-112">The URL cannot be read until the [**Open**](iwinhttprequest-open.md) method is called.</span></span> <span data-ttu-id="c4a72-113">Essa opção é útil para verificar a URL depois que o método [**Send**](iwinhttprequest-send.md) for concluído para verificar se ocorreu algum redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="c4a72-113">This option is useful for checking the URL after the [**Send**](iwinhttprequest-send.md) method is finished to verify that any redirection occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-114"><span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption \_ URLCodePage**</span><span class="sxs-lookup"><span data-stu-id="c4a72-114"><span id="WinHttpRequestOption_URLCodePage"></span><span id="winhttprequestoption_urlcodepage"></span><span id="WINHTTPREQUESTOPTION_URLCODEPAGE"></span>**WinHttpRequestOption\_URLCodePage**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-115">Define ou recupera uma **variante** que identifica a [*página de código*](glossary.md) da cadeia de caracteres da URL.</span><span class="sxs-lookup"><span data-stu-id="c4a72-115">Sets or retrieves a **VARIANT** that identifies the [*code page*](glossary.md) for the URL string.</span></span> <span data-ttu-id="c4a72-116">O valor padrão é a página de código UTF-8.</span><span class="sxs-lookup"><span data-stu-id="c4a72-116">The default value is the UTF-8 code page.</span></span> <span data-ttu-id="c4a72-117">A página de código é usada para converter a cadeia de caracteres da URL Unicode, passada no método [**Open**](iwinhttprequest-open.md) , para uma representação de cadeia de caracteres de byte único.</span><span class="sxs-lookup"><span data-stu-id="c4a72-117">The code page is used to convert the Unicode URL string, passed in the [**Open**](iwinhttprequest-open.md) method, to a single-byte string representation.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-118"><span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption \_ EscapePercentInURL**</span><span class="sxs-lookup"><span data-stu-id="c4a72-118"><span id="WinHttpRequestOption_EscapePercentInURL"></span><span id="winhttprequestoption_escapepercentinurl"></span><span id="WINHTTPREQUESTOPTION_ESCAPEPERCENTINURL"></span>**WinHttpRequestOption\_EscapePercentInURL**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-119">Define ou recupera uma **variante** que indica se os caracteres percentuais na cadeia de caracteres da URL são convertidos em uma sequência de escape.</span><span class="sxs-lookup"><span data-stu-id="c4a72-119">Sets or retrieves a **VARIANT** that indicates whether percent characters in the URL string are converted to an escape sequence.</span></span> <span data-ttu-id="c4a72-120">O valor padrão dessa opção é **Variant \_ true** , que especifica todos os caracteres de American National Standards Institute não seguros (ANSI), exceto que o símbolo de porcentagem é convertido em uma sequência de escape.</span><span class="sxs-lookup"><span data-stu-id="c4a72-120">The default value of this option is **VARIANT\_TRUE** which specifies all unsafe American National Standards Institute (ANSI) characters except the percent symbol are converted to an escape sequence.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-121"><span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption \_ SslErrorIgnoreFlags**</span><span class="sxs-lookup"><span data-stu-id="c4a72-121"><span id="WinHttpRequestOption_SslErrorIgnoreFlags"></span><span id="winhttprequestoption_sslerrorignoreflags"></span><span id="WINHTTPREQUESTOPTION_SSLERRORIGNOREFLAGS"></span>**WinHttpRequestOption\_SslErrorIgnoreFlags**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-122">Define ou recupera uma **variante** que indica quais erros de certificado de servidor devem ser ignorados.</span><span class="sxs-lookup"><span data-stu-id="c4a72-122">Sets or retrieves a **VARIANT** that indicates which server certificate errors should be ignored.</span></span> <span data-ttu-id="c4a72-123">Isso pode ser uma combinação de um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4a72-123">This can be a combination of one or more of the following flags.</span></span>



| <span data-ttu-id="c4a72-124">Erro</span><span class="sxs-lookup"><span data-stu-id="c4a72-124">Error</span></span>                                                  | <span data-ttu-id="c4a72-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c4a72-125">Value</span></span>  |
|--------------------------------------------------------|--------|
| <span data-ttu-id="c4a72-126">Autoridade de certificação (CA) desconhecida ou raiz não confiável</span><span class="sxs-lookup"><span data-stu-id="c4a72-126">Unknown certification authority (CA) or untrusted root</span></span> | <span data-ttu-id="c4a72-127">0x0100</span><span class="sxs-lookup"><span data-stu-id="c4a72-127">0x0100</span></span> |
| <span data-ttu-id="c4a72-128">Uso incorreto</span><span class="sxs-lookup"><span data-stu-id="c4a72-128">Wrong usage</span></span>                                            | <span data-ttu-id="c4a72-129">0x0200</span><span class="sxs-lookup"><span data-stu-id="c4a72-129">0x0200</span></span> |
| <span data-ttu-id="c4a72-130">Nome comum inválido (CN)</span><span class="sxs-lookup"><span data-stu-id="c4a72-130">Invalid common name (CN)</span></span>                               | <span data-ttu-id="c4a72-131">0x1000</span><span class="sxs-lookup"><span data-stu-id="c4a72-131">0x1000</span></span> |
| <span data-ttu-id="c4a72-132">Data inválida ou certificado expirado</span><span class="sxs-lookup"><span data-stu-id="c4a72-132">Invalid date or certificate expired</span></span>                    | <span data-ttu-id="c4a72-133">0x2000</span><span class="sxs-lookup"><span data-stu-id="c4a72-133">0x2000</span></span> |



 

<span data-ttu-id="c4a72-134">O valor padrão dessa opção na versão 5,1 do WinHTTP é zero, o que resulta em nenhum erro ignorado.</span><span class="sxs-lookup"><span data-stu-id="c4a72-134">The default value of this option in Version 5.1 of WinHTTP is zero, which results in no errors being ignored.</span></span> <span data-ttu-id="c4a72-135">Em versões anteriores do WinHTTP, a configuração padrão era 0x3300, o que resultou em todos os erros de certificado do servidor sendo ignorados por padrão.</span><span class="sxs-lookup"><span data-stu-id="c4a72-135">In earlier versions of WinHTTP, the default setting was 0x3300, which resulted in all server certificate errors being ignored by default.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-136"><span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption \_ SelectCertificate**</span><span class="sxs-lookup"><span data-stu-id="c4a72-136"><span id="WinHttpRequestOption_SelectCertificate"></span><span id="winhttprequestoption_selectcertificate"></span><span id="WINHTTPREQUESTOPTION_SELECTCERTIFICATE"></span>**WinHttpRequestOption\_SelectCertificate**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-137">Define uma **variante** que especifica o certificado do cliente que é enviado a um servidor para autenticação.</span><span class="sxs-lookup"><span data-stu-id="c4a72-137">Sets a **VARIANT** that specifies the client certificate that is sent to a server for authentication.</span></span> <span data-ttu-id="c4a72-138">Essa opção indica o local, o [*repositório de certificados*](glossary.md)e o assunto de um certificado de cliente delimitado por barras invertidas.</span><span class="sxs-lookup"><span data-stu-id="c4a72-138">This option indicates the location, [*certificate store*](glossary.md), and subject of a client certificate delimited with backslashes.</span></span> <span data-ttu-id="c4a72-139">Para obter mais informações sobre como selecionar um certificado de cliente, consulte [SSL no WinHTTP](ssl-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="c4a72-139">For more information about selecting a client certificate, see [SSL in WinHTTP](ssl-in-winhttp.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-140"><span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption \_ EnableRedirects**</span><span class="sxs-lookup"><span data-stu-id="c4a72-140"><span id="WinHttpRequestOption_EnableRedirects"></span><span id="winhttprequestoption_enableredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEREDIRECTS"></span>**WinHttpRequestOption\_EnableRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-141">Define ou recupera uma **variante** que indica se as solicitações são redirecionadas automaticamente quando o servidor especifica um novo local para o recurso.</span><span class="sxs-lookup"><span data-stu-id="c4a72-141">Sets or retrieves a **VARIANT** that indicates whether requests are automatically redirected when the server specifies a new location for the resource.</span></span> <span data-ttu-id="c4a72-142">O valor padrão dessa opção é **Variant \_ true** para indicar que as solicitações são redirecionadas automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c4a72-142">The default value of this option is **VARIANT\_TRUE** to indicate that requests are automatically redirected.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-143"><span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption \_ UrlEscapeDisable**</span><span class="sxs-lookup"><span data-stu-id="c4a72-143"><span id="WinHttpRequestOption_UrlEscapeDisable"></span><span id="winhttprequestoption_urlescapedisable"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLE"></span>**WinHttpRequestOption\_UrlEscapeDisable**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-144">Define ou recupera uma **variante** que indica se caracteres não seguros no caminho e os componentes de consulta de uma URL são convertidos em sequências de escape.</span><span class="sxs-lookup"><span data-stu-id="c4a72-144">Sets or retrieves a **VARIANT** that indicates whether unsafe characters in the path and query components of a URL are converted to escape sequences.</span></span> <span data-ttu-id="c4a72-145">O valor padrão dessa opção é **Variant \_ true**, que especifica que os caracteres no caminho e na consulta são convertidos.</span><span class="sxs-lookup"><span data-stu-id="c4a72-145">The default value of this option is **VARIANT\_TRUE**, which specifies that characters in the path and query are converted.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-146"><span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption \_ UrlEscapeDisableQuery**</span><span class="sxs-lookup"><span data-stu-id="c4a72-146"><span id="WinHttpRequestOption_UrlEscapeDisableQuery"></span><span id="winhttprequestoption_urlescapedisablequery"></span><span id="WINHTTPREQUESTOPTION_URLESCAPEDISABLEQUERY"></span>**WinHttpRequestOption\_UrlEscapeDisableQuery**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-147">Define ou recupera uma **variante** que indica se caracteres não seguros no componente de consulta da URL são convertidos em sequências de escape.</span><span class="sxs-lookup"><span data-stu-id="c4a72-147">Sets or retrieves a **VARIANT** that indicates whether unsafe characters in the query component of the URL are converted to escape sequences.</span></span> <span data-ttu-id="c4a72-148">O valor padrão dessa opção é **Variant \_ true**, que especifica que os caracteres na consulta são convertidos.</span><span class="sxs-lookup"><span data-stu-id="c4a72-148">The default value of this option is **VARIANT\_TRUE**, which specifies that characters in the query are converted.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-149"><span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption \_ SecureProtocols**</span><span class="sxs-lookup"><span data-stu-id="c4a72-149"><span id="WinHttpRequestOption_SecureProtocols"></span><span id="winhttprequestoption_secureprotocols"></span><span id="WINHTTPREQUESTOPTION_SECUREPROTOCOLS"></span>**WinHttpRequestOption\_SecureProtocols**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-150">Define ou recupera uma **variante** que indica quais protocolos seguros podem ser usados.</span><span class="sxs-lookup"><span data-stu-id="c4a72-150">Sets or retrieves a **VARIANT** that indicates which secure protocols can be used.</span></span> <span data-ttu-id="c4a72-151">Essa opção seleciona os protocolos aceitáveis para o cliente.</span><span class="sxs-lookup"><span data-stu-id="c4a72-151">This option selects the protocols acceptable to the client.</span></span> <span data-ttu-id="c4a72-152">O protocolo é negociado durante o handshake de protocolo SSL (SSL).</span><span class="sxs-lookup"><span data-stu-id="c4a72-152">The protocol is negotiated during the Secure Sockets Layer (SSL) handshake.</span></span> <span data-ttu-id="c4a72-153">Isso pode ser uma combinação de um ou mais dos sinalizadores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4a72-153">This can be a combination of one or more of the following flags.</span></span>



| <span data-ttu-id="c4a72-154">Protocolo</span><span class="sxs-lookup"><span data-stu-id="c4a72-154">Protocol</span></span>                           | <span data-ttu-id="c4a72-155">Valor</span><span class="sxs-lookup"><span data-stu-id="c4a72-155">Value</span></span>  |
|------------------------------------|--------|
| <span data-ttu-id="c4a72-156">SSL 2.0</span><span class="sxs-lookup"><span data-stu-id="c4a72-156">SSL 2.0</span></span>                            | <span data-ttu-id="c4a72-157">0x0008</span><span class="sxs-lookup"><span data-stu-id="c4a72-157">0x0008</span></span> |
| <span data-ttu-id="c4a72-158">SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="c4a72-158">SSL 3.0</span></span>                            | <span data-ttu-id="c4a72-159">0x0020</span><span class="sxs-lookup"><span data-stu-id="c4a72-159">0x0020</span></span> |
| <span data-ttu-id="c4a72-160">Segurança de camada de transporte (TLS) 1,0</span><span class="sxs-lookup"><span data-stu-id="c4a72-160">Transport Layer Security (TLS) 1.0</span></span> | <span data-ttu-id="c4a72-161">0x0080</span><span class="sxs-lookup"><span data-stu-id="c4a72-161">0x0080</span></span> |



 

<span data-ttu-id="c4a72-162">O valor padrão dessa opção é 0x0028, que indica que o SSL 2,0 ou SSL 3,0 pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="c4a72-162">The default value of this option is 0x0028, which indicates that SSL 2.0 or SSL 3.0 can be used.</span></span> <span data-ttu-id="c4a72-163">Se essa opção for definida como zero, o cliente e o servidor não poderão determinar um protocolo de segurança aceitável e o próximo [**envio**](iwinhttprequest-send.md) resultará em um erro.</span><span class="sxs-lookup"><span data-stu-id="c4a72-163">If this option is set to zero, the client and server are not able to determine an acceptable security protocol and the next [**Send**](iwinhttprequest-send.md) results in an error.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-164"><span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption \_ EnableTracing**</span><span class="sxs-lookup"><span data-stu-id="c4a72-164"><span id="WinHttpRequestOption_EnableTracing"></span><span id="winhttprequestoption_enabletracing"></span><span id="WINHTTPREQUESTOPTION_ENABLETRACING"></span>**WinHttpRequestOption\_EnableTracing**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-165">Define ou recupera uma **variante** que indica se o rastreamento está habilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="c4a72-165">Sets or retrieves a **VARIANT** that indicates whether tracing is currently enabled.</span></span> <span data-ttu-id="c4a72-166">Para obter mais informações sobre o recurso de rastreamento no Microsoft Windows HTTP Services (WinHTTP), consulte [recursos de rastreamento do WinHTTP](winhttptracecfg-exe--a-trace-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="c4a72-166">For more information about the trace facility in Microsoft Windows HTTP Services (WinHTTP), see [WinHTTP Trace Facility](winhttptracecfg-exe--a-trace-configuration-tool.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-167"><span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption \_ RevertImpersonationOverSsl**</span><span class="sxs-lookup"><span data-stu-id="c4a72-167"><span id="WinHttpRequestOption_RevertImpersonationOverSsl"></span><span id="winhttprequestoption_revertimpersonationoverssl"></span><span id="WINHTTPREQUESTOPTION_REVERTIMPERSONATIONOVERSSL"></span>**WinHttpRequestOption\_RevertImpersonationOverSsl**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-168">Controla se o objeto [**WinHttpRequest**](winhttprequest.md) reverte temporariamente a representação do cliente pela duração das operações de autenticação do certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="c4a72-168">Controls whether the [**WinHttpRequest**](winhttprequest.md) object temporarily reverts client impersonation for the duration of the SSL certificate authentication operations.</span></span> <span data-ttu-id="c4a72-169">A configuração padrão para o objeto **WinHttpRequest** é **true**.</span><span class="sxs-lookup"><span data-stu-id="c4a72-169">The default setting for the **WinHttpRequest** object is **TRUE**.</span></span> <span data-ttu-id="c4a72-170">Defina essa opção como **false** para manter a representação ao executar operações de autenticação de certificado.</span><span class="sxs-lookup"><span data-stu-id="c4a72-170">Set this option to **FALSE** to keep impersonation while performing certificate authentication operations.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-171"><span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption \_ EnableHttpsToHttpRedirects**</span><span class="sxs-lookup"><span data-stu-id="c4a72-171"><span id="WinHttpRequestOption_EnableHttpsToHttpRedirects"></span><span id="winhttprequestoption_enablehttpstohttpredirects"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTPSTOHTTPREDIRECTS"></span>**WinHttpRequestOption\_EnableHttpsToHttpRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-172">Controla se o WinHTTP permite ou não redirecionamentos.</span><span class="sxs-lookup"><span data-stu-id="c4a72-172">Controls whether or not WinHTTP allows redirects.</span></span> <span data-ttu-id="c4a72-173">Por padrão, todos os redirecionamentos são automaticamente seguidos, exceto aqueles que são transferidos de uma URL segura (https) para uma URL não segura (http).</span><span class="sxs-lookup"><span data-stu-id="c4a72-173">By default, all redirects are automatically followed, except those that transfer from a secure (https) URL to an non-secure (http) URL.</span></span> <span data-ttu-id="c4a72-174">Defina essa opção como **true** para habilitar HTTPS para redirecionamentos http.</span><span class="sxs-lookup"><span data-stu-id="c4a72-174">Set this option to **TRUE** to enable HTTPS to HTTP redirects.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-175"><span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption \_ EnablePassportAuthentication**</span><span class="sxs-lookup"><span data-stu-id="c4a72-175"><span id="WinHttpRequestOption_EnablePassportAuthentication"></span><span id="winhttprequestoption_enablepassportauthentication"></span><span id="WINHTTPREQUESTOPTION_ENABLEPASSPORTAUTHENTICATION"></span>**WinHttpRequestOption\_EnablePassportAuthentication**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-176">Habilita ou desabilita o suporte para autenticação do Passport.</span><span class="sxs-lookup"><span data-stu-id="c4a72-176">Enables or disables support for Passport authentication.</span></span> <span data-ttu-id="c4a72-177">Por padrão, o suporte automático para autenticação do Passport está desabilitado; Defina essa opção como **true** para habilitar o suporte à autenticação do Passport.</span><span class="sxs-lookup"><span data-stu-id="c4a72-177">By default, automatic support for Passport authentication is disabled; set this option to **TRUE** to enable Passport authentication support.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-178"><span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption \_ MaxAutomaticRedirects**</span><span class="sxs-lookup"><span data-stu-id="c4a72-178"><span id="WinHttpRequestOption_MaxAutomaticRedirects"></span><span id="winhttprequestoption_maxautomaticredirects"></span><span id="WINHTTPREQUESTOPTION_MAXAUTOMATICREDIRECTS"></span>**WinHttpRequestOption\_MaxAutomaticRedirects**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-179">Define ou recupera o número máximo de redirecionamentos que o WinHTTP segue; o padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="c4a72-179">Sets or retrieves the maximum number of redirects that WinHTTP follows; the default is 10.</span></span> <span data-ttu-id="c4a72-180">Esse limite impede que sites não autorizados tornem a parada do cliente WinHTTP após um grande número de redirecionamentos.</span><span class="sxs-lookup"><span data-stu-id="c4a72-180">This limit prevents unauthorized sites from making the WinHTTP client stall following a large number of redirects.</span></span>

<span data-ttu-id="c4a72-181">**Windows XP com SP1 e windows 2000 com SP3:** Não há suporte para esse valor de enumeração.</span><span class="sxs-lookup"><span data-stu-id="c4a72-181">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-182"><span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption \_ MaxResponseHeaderSize**</span><span class="sxs-lookup"><span data-stu-id="c4a72-182"><span id="WinHttpRequestOption_MaxResponseHeaderSize"></span><span id="winhttprequestoption_maxresponseheadersize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEHEADERSIZE"></span>**WinHttpRequestOption\_MaxResponseHeaderSize**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-183">Define ou recupera um conjunto associado no tamanho máximo da parte do cabeçalho da resposta do servidor.</span><span class="sxs-lookup"><span data-stu-id="c4a72-183">Sets or retrieves a bound set on the maximum size of the header portion of the server's response.</span></span> <span data-ttu-id="c4a72-184">Essa ligação protege o cliente de um servidor mal-intencionado tentando paralisar o cliente enviando uma resposta com uma quantidade infinita de dados de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="c4a72-184">This bound protects the client from a malicious server attempting to stall the client by sending a response with an infinite amount of header data.</span></span> <span data-ttu-id="c4a72-185">O valor padrão é 64 KB.</span><span class="sxs-lookup"><span data-stu-id="c4a72-185">The default value is 64 KB.</span></span>

<span data-ttu-id="c4a72-186">**Windows XP com SP1 e windows 2000 com SP3:** Não há suporte para esse valor de enumeração.</span><span class="sxs-lookup"><span data-stu-id="c4a72-186">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-187"><span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption \_ MaxResponseDrainSize**</span><span class="sxs-lookup"><span data-stu-id="c4a72-187"><span id="WinHttpRequestOption_MaxResponseDrainSize"></span><span id="winhttprequestoption_maxresponsedrainsize"></span><span id="WINHTTPREQUESTOPTION_MAXRESPONSEDRAINSIZE"></span>**WinHttpRequestOption\_MaxResponseDrainSize**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-188">Define ou recupera um limite na quantidade de dados que será descarregada de respostas para reutilizar uma conexão.</span><span class="sxs-lookup"><span data-stu-id="c4a72-188">Sets or retrieves a bound on the amount of data that will be drained from responses in order to reuse a connection.</span></span> <span data-ttu-id="c4a72-189">O padrão é 1 MB.</span><span class="sxs-lookup"><span data-stu-id="c4a72-189">The default is 1 MB.</span></span>

<span data-ttu-id="c4a72-190">**Windows XP com SP1 e windows 2000 com SP3:** Não há suporte para esse valor de enumeração.</span><span class="sxs-lookup"><span data-stu-id="c4a72-190">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-191"><span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption \_ EnableHttp1 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c4a72-191"><span id="WinHttpRequestOption_EnableHttp1_1"></span><span id="winhttprequestoption_enablehttp1_1"></span><span id="WINHTTPREQUESTOPTION_ENABLEHTTP1_1"></span>**WinHttpRequestOption\_EnableHttp1\_1**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-192">Define ou recupera um valor booliano que indica se HTTP/1.1 ou HTTP/1.0 devem ser usados.</span><span class="sxs-lookup"><span data-stu-id="c4a72-192">Sets or retrieves a boolean value that indicates whether HTTP/1.1 or HTTP/1.0 should be used.</span></span> <span data-ttu-id="c4a72-193">O padrão é **true**, para que http/1.1 seja usado por padrão.</span><span class="sxs-lookup"><span data-stu-id="c4a72-193">The default is **TRUE**, so that HTTP/1.1 is used by default.</span></span>

<span data-ttu-id="c4a72-194">**Windows XP com SP1 e windows 2000 com SP3:** Não há suporte para esse valor de enumeração.</span><span class="sxs-lookup"><span data-stu-id="c4a72-194">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="c4a72-195"><span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption \_ EnableCertificateRevocationCheck**</span><span class="sxs-lookup"><span data-stu-id="c4a72-195"><span id="WinHttpRequestOption_EnableCertificateRevocationCheck"></span><span id="winhttprequestoption_enablecertificaterevocationcheck"></span><span id="WINHTTPREQUESTOPTION_ENABLECERTIFICATEREVOCATIONCHECK"></span>**WinHttpRequestOption\_EnableCertificateRevocationCheck**</span></span>
</dt> <dd>

<span data-ttu-id="c4a72-196">Habilita a verificação de revogação de certificado do servidor durante a negociação SSL.</span><span class="sxs-lookup"><span data-stu-id="c4a72-196">Enables server certificate revocation checking during SSL negotiation.</span></span> <span data-ttu-id="c4a72-197">Quando o servidor apresenta um certificado, uma verificação é executada para determinar se o certificado foi revogado pelo emissor.</span><span class="sxs-lookup"><span data-stu-id="c4a72-197">When the server presents a certificate, a check is performed to determine whether the certificate has been revoked by its issuer.</span></span> <span data-ttu-id="c4a72-198">Se o certificado for realmente revogado ou a verificação de revogação falhar porque a CRL (lista de certificados revogados) não pode ser baixada, a solicitação falhará; esses erros de revogação não podem ser suprimidos.</span><span class="sxs-lookup"><span data-stu-id="c4a72-198">If the certificate is indeed revoked, or the revocation check fails because the Certificate Revocation List (CRL) cannot be downloaded, the request fails; such revocation errors cannot be suppressed.</span></span>

<span data-ttu-id="c4a72-199">**Windows XP com SP1 e windows 2000 com SP3:** Não há suporte para esse valor de enumeração.</span><span class="sxs-lookup"><span data-stu-id="c4a72-199">**Windows XP with SP1 and Windows 2000 with SP3:** This enumeration value is not supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4a72-200">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4a72-200">Remarks</span></span>

<span data-ttu-id="c4a72-201">Defina uma opção especificando uma das constantes anteriores como o parâmetro da propriedade [**Option**](iwinhttprequest-option.md) .</span><span class="sxs-lookup"><span data-stu-id="c4a72-201">Set an option by specifying one of the preceding constants as the parameter of the [**Option**](iwinhttprequest-option.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="c4a72-202">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c4a72-202">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c4a72-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4a72-203">Requirements</span></span>



| <span data-ttu-id="c4a72-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4a72-204">Requirement</span></span> | <span data-ttu-id="c4a72-205">Valor</span><span class="sxs-lookup"><span data-stu-id="c4a72-205">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a72-206">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4a72-206">Minimum supported client</span></span><br/> | <span data-ttu-id="c4a72-207">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="c4a72-207">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="c4a72-208">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4a72-208">Minimum supported server</span></span><br/> | <span data-ttu-id="c4a72-209">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="c4a72-209">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="c4a72-210">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c4a72-210">Redistributable</span></span><br/>          | <span data-ttu-id="c4a72-211">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c4a72-211">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="c4a72-212">INSERI</span><span class="sxs-lookup"><span data-stu-id="c4a72-212">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4a72-213"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4a72-213"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4a72-214">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4a72-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4a72-215">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c4a72-215">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




