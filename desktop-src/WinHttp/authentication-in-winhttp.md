---
description: Alguns servidores HTTP e proxies exigem autenticação antes de permitir o acesso a recursos na Internet. As funções do Microsoft Windows HTTP Services (WinHTTP) dão suporte à autenticação de servidor e proxy para sessões HTTP.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Autenticação no WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75c6703e9d28902c5705f0b8ab8433193c4d085
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380821"
---
# <a name="authentication-in-winhttp"></a><span data-ttu-id="c5de8-104">Autenticação no WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c5de8-104">Authentication in WinHTTP</span></span>

<span data-ttu-id="c5de8-105">Alguns servidores HTTP e proxies exigem autenticação antes de permitir o acesso a recursos na Internet.</span><span class="sxs-lookup"><span data-stu-id="c5de8-105">Some HTTP servers and proxies require authentication before allowing access to resources on the Internet.</span></span> <span data-ttu-id="c5de8-106">As funções do Microsoft Windows HTTP Services (WinHTTP) dão suporte à autenticação de servidor e proxy para sessões HTTP.</span><span class="sxs-lookup"><span data-stu-id="c5de8-106">The Microsoft Windows HTTP Services (WinHTTP) functions support server and proxy authentication for HTTP sessions.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="c5de8-107">Sobre a autenticação HTTP</span><span class="sxs-lookup"><span data-stu-id="c5de8-107">About HTTP Authentication</span></span>

<span data-ttu-id="c5de8-108">Se a autenticação for necessária, o aplicativo HTTP receberá um código de status 401 (o servidor requer autenticação) ou 407 (o proxy requer autenticação).</span><span class="sxs-lookup"><span data-stu-id="c5de8-108">If authentication is required, the HTTP application receives a status code of 401 (server requires authentication) or 407 (proxy requires authentication).</span></span> <span data-ttu-id="c5de8-109">Junto com o código de status, o proxy ou o servidor envia um ou mais cabeçalhos de autenticação: WWW-Authenticate (para autenticação de servidor) ou Proxy-Authenticate (para autenticação de proxy).</span><span class="sxs-lookup"><span data-stu-id="c5de8-109">Along with the status code, the proxy or server sends one or more authenticate headers: WWW-Authenticate (for server authentication) or Proxy-Authenticate (for proxy authentication).</span></span>

<span data-ttu-id="c5de8-110">Cada cabeçalho Authenticate contém um esquema de autenticação com suporte e, para os esquemas básico e Digest, um realm.</span><span class="sxs-lookup"><span data-stu-id="c5de8-110">Each authenticate header contains a supported authentication scheme and, for the Basic and Digest schemes, a realm.</span></span> <span data-ttu-id="c5de8-111">Se houver suporte para vários esquemas de autenticação, o servidor retornará vários cabeçalhos autenticar.</span><span class="sxs-lookup"><span data-stu-id="c5de8-111">If multiple authentication schemes are supported, the server returns multiple authenticate headers.</span></span> <span data-ttu-id="c5de8-112">O valor do Realm diferenciam maiúsculas de minúsculas e definem um conjunto de servidores ou proxies para os quais as mesmas credenciais são aceitas.</span><span class="sxs-lookup"><span data-stu-id="c5de8-112">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials are accepted.</span></span> <span data-ttu-id="c5de8-113">Por exemplo, o cabeçalho "WWW-Authenticate: Basic real =" example "" pode ser retornado quando a autenticação do servidor é necessária.</span><span class="sxs-lookup"><span data-stu-id="c5de8-113">For example, the header "WWW-Authenticate: Basic Realm="example"" might be returned when server authentication is required.</span></span> <span data-ttu-id="c5de8-114">Esse cabeçalho especifica que as credenciais do usuário devem ser fornecidas para o domínio "exemplo".</span><span class="sxs-lookup"><span data-stu-id="c5de8-114">This header specifies that user credentials must be supplied for the "example" domain.</span></span>

<span data-ttu-id="c5de8-115">Um aplicativo HTTP pode incluir um campo de cabeçalho de autorização com uma solicitação que ele envia para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c5de8-115">An HTTP application can include an authorization header field with a request it sends to the server.</span></span> <span data-ttu-id="c5de8-116">O cabeçalho Authorization contém o esquema de autenticação e a resposta apropriada exigida por esse esquema.</span><span class="sxs-lookup"><span data-stu-id="c5de8-116">The authorization header contains the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="c5de8-117">Por exemplo, o cabeçalho "Authorization: Basic \<username:password> " seria adicionado à solicitação e enviado ao servidor se o cliente recebeu o cabeçalho de resposta "www-Authenticate: Basic realment =" example "".</span><span class="sxs-lookup"><span data-stu-id="c5de8-117">For example, the header "Authorization: Basic \<username:password>" would be added to the request and sent to the server if the client received the response header "WWW-Authenticate: Basic Realm="example"".</span></span>

> [!Note]  
> <span data-ttu-id="c5de8-118">Embora eles sejam mostrados aqui como texto sem formatação, o nome de usuário e a senha são, na verdade, [*codificados na base64*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c5de8-118">Although they are shown here as plain text, the username and password are actually [*base64 encoded*](glossary.md).</span></span>

 

<span data-ttu-id="c5de8-119">Há dois tipos gerais de esquemas de autenticação:</span><span class="sxs-lookup"><span data-stu-id="c5de8-119">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="c5de8-120">Esquema de autenticação básica, no qual o nome de usuário e a senha são enviados em texto não criptografado para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c5de8-120">Basic authentication scheme, in which the user name and password are sent in clear text to the server.</span></span>

    <span data-ttu-id="c5de8-121">O esquema de autenticação básica baseia-se no modelo que um cliente deve identificar a si mesmo com um nome de usuário e senha para cada realm.</span><span class="sxs-lookup"><span data-stu-id="c5de8-121">The Basic authentication scheme is based on the model that a client must identify itself with a user name and password for each realm.</span></span> <span data-ttu-id="c5de8-122">O servidor serviçosá a solicitação somente se a solicitação for enviada com um cabeçalho de autorização que inclua um nome de usuário e senha válidos.</span><span class="sxs-lookup"><span data-stu-id="c5de8-122">The server services the request only if the request is sent with an authorization header that includes a valid user name and password.</span></span>

-   <span data-ttu-id="c5de8-123">Esquemas de desafio/resposta, como o Kerberos, em que o servidor desafia o cliente com os [*dados de autenticação*](glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c5de8-123">Challenge-response schemes, such as Kerberos, in which the server challenges the client with [*authentication data*](glossary.md).</span></span> <span data-ttu-id="c5de8-124">O cliente transforma os dados com as credenciais do usuário e envia os dados transformados de volta para o servidor para autenticação.</span><span class="sxs-lookup"><span data-stu-id="c5de8-124">The client transforms the data with the user credentials and sends the transformed data back to the server for authentication.</span></span>

    <span data-ttu-id="c5de8-125">Os esquemas de desafio/resposta permitem uma autenticação mais segura.</span><span class="sxs-lookup"><span data-stu-id="c5de8-125">Challenge-response schemes enable a more secure authentication.</span></span> <span data-ttu-id="c5de8-126">Em um esquema de desafio/resposta, o nome de usuário e a senha nunca são transmitidos pela rede.</span><span class="sxs-lookup"><span data-stu-id="c5de8-126">In a challenge-response scheme, the username and password are never transmitted over the network.</span></span> <span data-ttu-id="c5de8-127">Depois que o cliente seleciona um esquema de desafio/resposta, o servidor retorna um código de status apropriado com um desafio que contém os [*dados de autenticação*](glossary.md) para esse esquema.</span><span class="sxs-lookup"><span data-stu-id="c5de8-127">After the client selects a challenge-response scheme, the server returns an appropriate status code with a challenge that contains the [*authentication data*](glossary.md) for that scheme.</span></span> <span data-ttu-id="c5de8-128">O cliente reenvia a solicitação com a resposta apropriada para obter o serviço solicitado.</span><span class="sxs-lookup"><span data-stu-id="c5de8-128">The client then resends the request with the proper response to obtain the requested service.</span></span> <span data-ttu-id="c5de8-129">Os esquemas de desafio/resposta podem realizar várias trocas para serem concluídos.</span><span class="sxs-lookup"><span data-stu-id="c5de8-129">Challenge-response schemes can take multiple exchanges to complete.</span></span>

<span data-ttu-id="c5de8-130">A tabela a seguir contém os esquemas de autenticação que têm suporte do WinHTTP, o tipo de autenticação e uma descrição do esquema.</span><span class="sxs-lookup"><span data-stu-id="c5de8-130">The following table contains the authentication schemes that are supported by WinHTTP, the authentication type, and a description of the scheme.</span></span>



| <span data-ttu-id="c5de8-131">Esquema</span><span class="sxs-lookup"><span data-stu-id="c5de8-131">Scheme</span></span>            | <span data-ttu-id="c5de8-132">Type</span><span class="sxs-lookup"><span data-stu-id="c5de8-132">Type</span></span>               | <span data-ttu-id="c5de8-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5de8-133">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5de8-134">Básico (texto sem formatação)</span><span class="sxs-lookup"><span data-stu-id="c5de8-134">Basic (plaintext)</span></span> | <span data-ttu-id="c5de8-135">Basic</span><span class="sxs-lookup"><span data-stu-id="c5de8-135">Basic</span></span>              | <span data-ttu-id="c5de8-136">Usa uma cadeia de caracteres [*codificada em base64*](glossary.md) que contém o nome de usuário e a senha.</span><span class="sxs-lookup"><span data-stu-id="c5de8-136">Uses a [*base64 encoded*](glossary.md) string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c5de8-137">Digest</span><span class="sxs-lookup"><span data-stu-id="c5de8-137">Digest</span></span>            | <span data-ttu-id="c5de8-138">Desafio-resposta</span><span class="sxs-lookup"><span data-stu-id="c5de8-138">Challenge-response</span></span> | <span data-ttu-id="c5de8-139">Desafios que usam um valor nonce (uma cadeia de caracteres de dados especificada pelo servidor).</span><span class="sxs-lookup"><span data-stu-id="c5de8-139">Challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="c5de8-140">Uma resposta válida contém uma soma de verificação do nome de usuário, a senha, o valor de nonce fornecido, o [*verbo http*](glossary.md)e o Uniform Resource Identifier (URI) solicitado.</span><span class="sxs-lookup"><span data-stu-id="c5de8-140">A valid response contains a checksum of the user name, the password, the given nonce value, the [*HTTP verb*](glossary.md), and the requested Uniform Resource Identifier (URI).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="c5de8-141">NTLM</span><span class="sxs-lookup"><span data-stu-id="c5de8-141">NTLM</span></span>              | <span data-ttu-id="c5de8-142">Desafio-resposta</span><span class="sxs-lookup"><span data-stu-id="c5de8-142">Challenge-response</span></span> | <span data-ttu-id="c5de8-143">Requer que os [*dados de autenticação*](glossary.md) sejam transformados com as credenciais do usuário para provar a identidade.</span><span class="sxs-lookup"><span data-stu-id="c5de8-143">Requires the [*authentication data*](glossary.md) to be transformed with the user credentials to prove identity.</span></span> <span data-ttu-id="c5de8-144">Para que a autenticação NTLM funcione corretamente, várias trocas devem ocorrer na mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="c5de8-144">For NTLM authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="c5de8-145">Portanto, a autenticação NTLM não poderá ser usada se um proxy intermediário não oferecer suporte a conexões Keep Alive.</span><span class="sxs-lookup"><span data-stu-id="c5de8-145">Therefore, NTLM authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="c5de8-146">A autenticação NTLM também falhará se [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) for usado com o sinalizador de [**\_ \_ Keep \_ Alive do WinHTTP Disable**](option-flags.md) que desabilita a semântica Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="c5de8-146">NTLM authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span>                                                                                                                                                                                                                                       |
| <span data-ttu-id="c5de8-147">Passport</span><span class="sxs-lookup"><span data-stu-id="c5de8-147">Passport</span></span>          | <span data-ttu-id="c5de8-148">Desafio-resposta</span><span class="sxs-lookup"><span data-stu-id="c5de8-148">Challenge-response</span></span> | <span data-ttu-id="c5de8-149">Usa [Microsoft Passport 1,4](passport-authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="c5de8-149">Uses [Microsoft Passport 1.4](passport-authentication-in-winhttp.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="c5de8-150">Negotiate</span><span class="sxs-lookup"><span data-stu-id="c5de8-150">Negotiate</span></span>         | <span data-ttu-id="c5de8-151">Desafio-resposta</span><span class="sxs-lookup"><span data-stu-id="c5de8-151">Challenge-response</span></span> | <span data-ttu-id="c5de8-152">Se o servidor e o cliente estiverem usando o Windows 2000 ou posterior, a autenticação Kerberos será usada.</span><span class="sxs-lookup"><span data-stu-id="c5de8-152">If both the server and client are using Windows 2000 or later, Kerberos authentication is used.</span></span> <span data-ttu-id="c5de8-153">Caso contrário, a autenticação NTLM será usada.</span><span class="sxs-lookup"><span data-stu-id="c5de8-153">Otherwise NTLM authentication is used.</span></span> <span data-ttu-id="c5de8-154">O Kerberos está disponível em sistemas operacionais Windows 2000 e posteriores e é considerado mais seguro do que a autenticação NTLM.</span><span class="sxs-lookup"><span data-stu-id="c5de8-154">Kerberos is available in Windows 2000 and later operating systems and is considered to be more secure than NTLM authentication.</span></span> <span data-ttu-id="c5de8-155">Para que a autenticação Negotiate funcione corretamente, várias trocas devem ocorrer na mesma conexão.</span><span class="sxs-lookup"><span data-stu-id="c5de8-155">For Negotiate authentication to function correctly, several exchanges must take place on the same connection.</span></span> <span data-ttu-id="c5de8-156">Portanto, a autenticação de negociação não poderá ser usada se um proxy intermediário não oferecer suporte a conexões Keep Alive.</span><span class="sxs-lookup"><span data-stu-id="c5de8-156">Therefore, Negotiate authentication cannot be used if an intervening proxy does not support keep-alive connections.</span></span> <span data-ttu-id="c5de8-157">A autenticação de negociação também falhará se [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) for usado com o sinalizador de [**\_ \_ Keep \_ Alive do WinHTTP Disable**](option-flags.md) que desabilita a semântica Keep-Alive.</span><span class="sxs-lookup"><span data-stu-id="c5de8-157">Negotiate authentication also fails if [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) is used with the [**WINHTTP\_DISABLE\_KEEP\_ALIVE**](option-flags.md) flag that disables keep-alive semantics.</span></span> <span data-ttu-id="c5de8-158">O esquema de autenticação Negotiate às vezes é chamado de autenticação integrada do Windows.</span><span class="sxs-lookup"><span data-stu-id="c5de8-158">The Negotiate authentication scheme is sometimes called Integrated Windows authentication.</span></span> |



 

## <a name="authentication-in-winhttp-applications"></a><span data-ttu-id="c5de8-159">Autenticação em aplicativos WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c5de8-159">Authentication in WinHTTP Applications</span></span>

<span data-ttu-id="c5de8-160">A API (interface de programação de aplicativo) do WinHTTP fornece duas funções usadas para acessar recursos da Internet em situações em que a autenticação é necessária: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) e [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).</span><span class="sxs-lookup"><span data-stu-id="c5de8-160">The WinHTTP application programming interface (API) provides two functions used to access Internet resources in situations where authentication is required: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) and [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).</span></span>

<span data-ttu-id="c5de8-161">Quando uma resposta é recebida com um código de status 401 ou 407, [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) pode ser usado para analisar os cabeçalhos de autenticação para determinar os esquemas de autenticação com suporte e o destino de autenticação.</span><span class="sxs-lookup"><span data-stu-id="c5de8-161">When a response is received with a 401 or 407 status code, [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) can be used to parse the authentication headers to determine the supported authentication schemes and the authentication target.</span></span> <span data-ttu-id="c5de8-162">O destino de autenticação é o servidor ou proxy que solicita autenticação.</span><span class="sxs-lookup"><span data-stu-id="c5de8-162">The authentication target is the server or proxy that requests authentication.</span></span> <span data-ttu-id="c5de8-163">**WinHttpQueryAuthSchemes** também determina o primeiro esquema de autenticação, dos esquemas disponíveis, com base nas preferências de esquema de autenticação sugeridas pelo servidor.</span><span class="sxs-lookup"><span data-stu-id="c5de8-163">**WinHttpQueryAuthSchemes** also determines the first authentication scheme, from the available schemes, based on the authentication scheme preferences suggested by the server.</span></span> <span data-ttu-id="c5de8-164">Esse método para escolher um esquema de autenticação é o comportamento sugerido pela [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="c5de8-164">This method for choosing an authentication scheme is the behavior suggested by [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span>

<span data-ttu-id="c5de8-165">O [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) permite que um aplicativo especifique o esquema de autenticação que é usado junto com um nome de usuário e senha válidos para uso no servidor de destino ou proxy.</span><span class="sxs-lookup"><span data-stu-id="c5de8-165">[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) enables an application to specify the authentication scheme that is used along with a valid username and password for use on the target server or proxy.</span></span> <span data-ttu-id="c5de8-166">Depois de definir as credenciais e reenviar a solicitação, os cabeçalhos necessários são gerados e adicionados à solicitação automaticamente.</span><span class="sxs-lookup"><span data-stu-id="c5de8-166">After setting the credentials and resending the request, the necessary headers are generated and added to the request automatically.</span></span> <span data-ttu-id="c5de8-167">Como alguns esquemas de autenticação exigem várias transações [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) pode retornar o erro, erro \_ WinHTTP \_ reenviar \_ solicitação.</span><span class="sxs-lookup"><span data-stu-id="c5de8-167">Because some authentication schemes require multiple transactions [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) could return the error, ERROR\_WINHTTP\_RESEND\_REQUEST.</span></span> <span data-ttu-id="c5de8-168">Quando esse erro for encontrado, o aplicativo deverá continuar a reenviar a solicitação até que uma resposta seja recebida e não contenha um código de status 401 ou 407.</span><span class="sxs-lookup"><span data-stu-id="c5de8-168">When this error is encountered, the application should continue to resend the request until a response is received that does not contain a 401 or 407 status code.</span></span> <span data-ttu-id="c5de8-169">Um código de status 200 indica que o recurso está disponível e a solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c5de8-169">A 200 status code indicates that the resource is available and the request is successful.</span></span> <span data-ttu-id="c5de8-170">Consulte [**códigos de status http**](http-status-codes.md) para obter códigos de status adicionais que podem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="c5de8-170">See [**HTTP Status Codes**](http-status-codes.md) for additional status codes that can be returned.</span></span>

<span data-ttu-id="c5de8-171">Se um esquema de autenticação aceitável e as credenciais forem conhecidas antes que uma solicitação seja enviada ao servidor, um aplicativo poderá chamar [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) antes de chamar [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="c5de8-171">If an acceptable authentication scheme and credentials are known before a request is sent to the server, an application can call [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) before calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span> <span data-ttu-id="c5de8-172">Nesse caso, o WinHTTP tenta pré-autenticação com o servidor fornecendo credenciais ou [*dados de autenticação*](glossary.md) na solicitação inicial para o servidor.</span><span class="sxs-lookup"><span data-stu-id="c5de8-172">In this case, WinHTTP attempts pre-authentication with the server by providing credentials or [*authentication data*](glossary.md) in the initial request to the server.</span></span> <span data-ttu-id="c5de8-173">A pré-autenticação pode diminuir o número de trocas no processo de autenticação e, portanto, melhorar o desempenho do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c5de8-173">Pre-authentication can decrease the number of exchanges in the authentication process and therefore improve application performance.</span></span>

<span data-ttu-id="c5de8-174">A pré-autenticação pode ser usada com os seguintes esquemas de autenticação:</span><span class="sxs-lookup"><span data-stu-id="c5de8-174">Preauthentication can be used with the following authentication schemes:</span></span>

-   <span data-ttu-id="c5de8-175">Básico – sempre possível.</span><span class="sxs-lookup"><span data-stu-id="c5de8-175">Basic - always possible.</span></span>
-   <span data-ttu-id="c5de8-176">Negociar a resolução para o Kerberos – provavelmente possível; a única exceção é quando as distorções de tempo estão desativadas entre o cliente e o controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="c5de8-176">Negotiate resolving into Kerberos - very likely possible; the only exception is when the time-skews are off between the client and the domain controller.</span></span>
-   <span data-ttu-id="c5de8-177">(Negociar resolvendo em NTLM)-nunca é possível.</span><span class="sxs-lookup"><span data-stu-id="c5de8-177">(Negotiate resolving into NTLM) - never possible.</span></span>
-   <span data-ttu-id="c5de8-178">NTLM – possível somente no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c5de8-178">NTLM - possible in Windows Server 2008 R2 only.</span></span>
-   <span data-ttu-id="c5de8-179">Digest-nunca é possível.</span><span class="sxs-lookup"><span data-stu-id="c5de8-179">Digest - never possible.</span></span>
-   <span data-ttu-id="c5de8-180">Passport-nunca é possível; após o desafio inicial-resposta, o WinHTTP usa cookies para se autenticar previamente no Passport.</span><span class="sxs-lookup"><span data-stu-id="c5de8-180">Passport - never possible; after the initial challenge-response, WinHTTP uses cookies to pre-authenticate to Passport.</span></span>

<span data-ttu-id="c5de8-181">Um aplicativo WinHTTP típico conclui as etapas a seguir para lidar com a autenticação.</span><span class="sxs-lookup"><span data-stu-id="c5de8-181">A typical WinHTTP application completes the following steps in order to handle authentication.</span></span>

-   <span data-ttu-id="c5de8-182">Solicite um recurso com [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) e [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="c5de8-182">Request a resource with [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) and [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>
-   <span data-ttu-id="c5de8-183">Verifique os cabeçalhos de resposta com [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="c5de8-183">Check the response headers with [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>
-   <span data-ttu-id="c5de8-184">Se um código de status 401 ou 407 for retornado indicando que a autenticação é necessária, chame [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) para localizar um esquema aceitável.</span><span class="sxs-lookup"><span data-stu-id="c5de8-184">If a 401 or 407 status code is returned indicating that authentication is required, call [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) to find an acceptable scheme.</span></span>
-   <span data-ttu-id="c5de8-185">Defina o esquema de autenticação, o nome de usuário e a senha com [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).</span><span class="sxs-lookup"><span data-stu-id="c5de8-185">Set the authentication scheme, username, and password with [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).</span></span>
-   <span data-ttu-id="c5de8-186">Reenvie a solicitação com o mesmo identificador de solicitação chamando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="c5de8-186">Resend the request with the same request handle by calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

<span data-ttu-id="c5de8-187">As credenciais definidas por [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) são usadas somente para uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="c5de8-187">The credentials set by [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) are only used for one request.</span></span> <span data-ttu-id="c5de8-188">O WinHTTP não armazena em cache as credenciais para usar em outras solicitações, o que significa que os aplicativos devem ser escritos que podem responder a várias solicitações.</span><span class="sxs-lookup"><span data-stu-id="c5de8-188">WinHTTP does not cache the credentials to use in other requests, which means that applications must be written that can respond to multiple requests.</span></span> <span data-ttu-id="c5de8-189">Se uma conexão autenticada for reutilizada, outras solicitações poderão não ser desafiadas, mas seu código deverá ser capaz de responder a uma solicitação a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="c5de8-189">If an authenticated connection is re-used, other requests may not be challenged, but your code should be able to respond to a request at any time.</span></span>

### <a name="example-retrieving-a-document"></a><span data-ttu-id="c5de8-190">Exemplo: Recuperando um documento</span><span class="sxs-lookup"><span data-stu-id="c5de8-190">Example: Retrieving a Document</span></span>

<span data-ttu-id="c5de8-191">O código de exemplo a seguir tenta recuperar um documento especificado de um servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="c5de8-191">The following sample code attempts to retrieve a specified document from an HTTP server.</span></span> <span data-ttu-id="c5de8-192">O código de status é recuperado da resposta para determinar se a autenticação é necessária.</span><span class="sxs-lookup"><span data-stu-id="c5de8-192">The status code is retrieved from the response to determine if authentication is required.</span></span> <span data-ttu-id="c5de8-193">Se um código de status 200 for encontrado, o documento estará disponível.</span><span class="sxs-lookup"><span data-stu-id="c5de8-193">If a 200 status code is found, the document is available.</span></span> <span data-ttu-id="c5de8-194">Se um código de status de 401 ou 407 for encontrado, a autenticação será necessária antes que o documento possa ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="c5de8-194">If a status code of 401 or 407 is found, authentication is required before the document can be retrieved.</span></span> <span data-ttu-id="c5de8-195">Para qualquer outro código de status, é exibida uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="c5de8-195">For any other status code, an error message is displayed.</span></span> <span data-ttu-id="c5de8-196">Consulte [**códigos de status http**](http-status-codes.md) para obter uma lista de códigos de status possíveis.</span><span class="sxs-lookup"><span data-stu-id="c5de8-196">See [**HTTP Status Codes**](http-status-codes.md) for a list of possible status codes.</span></span>


```C++
#include <windows.h>
#include <winhttp.h>
#include <stdio.h>

#pragma comment(lib, "winhttp.lib")

DWORD ChooseAuthScheme( DWORD dwSupportedSchemes )
{
  //  It is the server's responsibility only to accept 
  //  authentication schemes that provide a sufficient
  //  level of security to protect the servers resources.
  //
  //  The client is also obligated only to use an authentication
  //  scheme that adequately protects its username and password.
  //
  //  Thus, this sample code does not use Basic authentication  
  //  becaus Basic authentication exposes the client's username
  //  and password to anyone monitoring the connection.
  
  if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NEGOTIATE )
    return WINHTTP_AUTH_SCHEME_NEGOTIATE;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_NTLM )
    return WINHTTP_AUTH_SCHEME_NTLM;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_PASSPORT )
    return WINHTTP_AUTH_SCHEME_PASSPORT;
  else if( dwSupportedSchemes & WINHTTP_AUTH_SCHEME_DIGEST )
    return WINHTTP_AUTH_SCHEME_DIGEST;
  else
    return 0;
}

struct SWinHttpSampleGet
{
  LPCWSTR szServer;
  LPCWSTR szPath;
  BOOL fUseSSL;
  LPCWSTR szServerUsername;
  LPCWSTR szServerPassword;
  LPCWSTR szProxyUsername;
  LPCWSTR szProxyPassword;
};

void WinHttpAuthSample( IN SWinHttpSampleGet *pGetRequest )
{
  DWORD dwStatusCode = 0;
  DWORD dwSupportedSchemes;
  DWORD dwFirstScheme;
  DWORD dwSelectedScheme;
  DWORD dwTarget;
  DWORD dwLastStatus = 0;
  DWORD dwSize = sizeof(DWORD);
  BOOL  bResults = FALSE;
  BOOL  bDone = FALSE;

  DWORD dwProxyAuthScheme = 0;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  INTERNET_PORT nPort = ( pGetRequest->fUseSSL ) ? 
                        INTERNET_DEFAULT_HTTPS_PORT  :
                        INTERNET_DEFAULT_HTTP_PORT;

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, 
                               pGetRequest->szServer, 
                               nPort, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, 
                                   L"GET", 
                                   pGetRequest->szPath,
                                   NULL, 
                                   WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES,
                                   ( pGetRequest->fUseSSL ) ? 
                                       WINHTTP_FLAG_SECURE : 0 );

  // Continue to send a request until status code 
  // is not 401 or 407.
  if( hRequest == NULL )
    bDone = TRUE;

  while( !bDone )
  {
    //  If a proxy authentication challenge was responded to, reset
    //  those credentials before each SendRequest, because the proxy  
    //  may require re-authentication after responding to a 401 or  
    //  to a redirect. If you don't, you can get into a 
    //  407-401-407-401- loop.
    if( dwProxyAuthScheme != 0 )
      bResults = WinHttpSetCredentials( hRequest, 
                                        WINHTTP_AUTH_TARGET_PROXY, 
                                        dwProxyAuthScheme, 
                                        pGetRequest->szProxyUsername,
                                        pGetRequest->szProxyPassword,
                                        NULL );
    // Send a request.
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS,
                                   0,
                                   WINHTTP_NO_REQUEST_DATA,
                                   0, 
                                   0, 
                                   0 );

    // End the request.
    if( bResults )
      bResults = WinHttpReceiveResponse( hRequest, NULL );

    // Resend the request in case of 
    // ERROR_WINHTTP_RESEND_REQUEST error.
    if( !bResults && GetLastError( ) == ERROR_WINHTTP_RESEND_REQUEST)
        continue;

    // Check the status code.
    if( bResults ) 
      bResults = WinHttpQueryHeaders( hRequest, 
                                      WINHTTP_QUERY_STATUS_CODE |
                                      WINHTTP_QUERY_FLAG_NUMBER,
                                      NULL, 
                                      &dwStatusCode, 
                                      &dwSize, 
                                      NULL );

    if( bResults )
    {
      switch( dwStatusCode )
      {
        case 200: 
          // The resource was successfully retrieved.
          // You can use WinHttpReadData to read the 
          // contents of the server's response.
          printf( "The resource was successfully retrieved.\n" );
          bDone = TRUE;
          break;

        case 401:
          // The server requires authentication.
          printf(" The server requires authentication. Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
          {
            dwSelectedScheme = ChooseAuthScheme( dwSupportedSchemes);

            if( dwSelectedScheme == 0 )
              bDone = TRUE;
            else
              bResults = WinHttpSetCredentials( hRequest, 
                                        dwTarget, 
                                        dwSelectedScheme,
                                        pGetRequest->szServerUsername,
                                        pGetRequest->szServerPassword,
                                        NULL );
          }

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check
          // for a repeated sequence of status codes.
          if( dwLastStatus == 401 )
            bDone = TRUE;

          break;

        case 407:
          // The proxy requires authentication.
          printf( "The proxy requires authentication.  Sending credentials...\n" );

          // Obtain the supported and preferred schemes.
          bResults = WinHttpQueryAuthSchemes( hRequest, 
                                              &dwSupportedSchemes, 
                                              &dwFirstScheme, 
                                              &dwTarget );

          // Set the credentials before resending the request.
          if( bResults )
            dwProxyAuthScheme = ChooseAuthScheme(dwSupportedSchemes);

          // If the same credentials are requested twice, abort the
          // request.  For simplicity, this sample does not check 
          // for a repeated sequence of status codes.
          if( dwLastStatus == 407 )
            bDone = TRUE;
          break;

        default:
          // The status code does not indicate success.
          printf("Error. Status code %d returned.\n", dwStatusCode);
          bDone = TRUE;
      }
    }

    // Keep track of the last status code.
    dwLastStatus = dwStatusCode;

    // If there are any errors, break out of the loop.
    if( !bResults ) 
        bDone = TRUE;
  }

  // Report any errors.
  if( !bResults )
  {
    DWORD dwLastError = GetLastError( );
    printf( "Error %d has occurred.\n", dwLastError );
  }

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
}

```



## <a name="automatic-logon-policy"></a><span data-ttu-id="c5de8-197">Política de logon automático</span><span class="sxs-lookup"><span data-stu-id="c5de8-197">Automatic Logon Policy</span></span>

<span data-ttu-id="c5de8-198">A política de logon automático (logon automático) determina quando é aceitável que o WinHTTP inclua as credenciais padrão em uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="c5de8-198">The automatic logon (auto-logon) policy determines when it is acceptable for WinHTTP to include the default credentials in a request.</span></span> <span data-ttu-id="c5de8-199">As credenciais padrão são o token de thread atual ou o token de sessão, dependendo se o WinHTTP é usado no modo síncrono ou assíncrono.</span><span class="sxs-lookup"><span data-stu-id="c5de8-199">The default credentials are either the current thread token or the session token depending on whether WinHTTP is used in synchronous or asynchronous mode.</span></span> <span data-ttu-id="c5de8-200">O token de thread é usado no modo síncrono e o token de sessão é usado no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="c5de8-200">The thread token is used in synchronous mode, and the session token is used in asynchronous mode.</span></span> <span data-ttu-id="c5de8-201">Essas credenciais padrão geralmente são o nome de usuário e a senha usados para fazer logon no Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c5de8-201">These default credentials are often the username and password used to log on to Microsoft Windows.</span></span>

<span data-ttu-id="c5de8-202">A política de logon automático foi implementada para impedir que essas credenciais sejam usadas casualmente para autenticar em um servidor não confiável.</span><span class="sxs-lookup"><span data-stu-id="c5de8-202">The auto-logon policy was implemented to prevent these credentials from being casually used to authenticate against an untrusted server.</span></span> <span data-ttu-id="c5de8-203">Por padrão, o nível de segurança é definido para o nível de segurança do WINHTTP com \_ logon automático \_ \_ \_ médio, que permite que as credenciais padrão sejam usadas somente para solicitações de intranet.</span><span class="sxs-lookup"><span data-stu-id="c5de8-203">By default, the security level is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_MEDIUM, which allows the default credentials to be used only for Intranet requests.</span></span> <span data-ttu-id="c5de8-204">A política de logon automático só se aplica aos esquemas de autenticação NTLM e negociar.</span><span class="sxs-lookup"><span data-stu-id="c5de8-204">The auto-logon policy only applies to the NTLM and Negotiate authentication schemes.</span></span> <span data-ttu-id="c5de8-205">As credenciais nunca são transmitidas automaticamente com outros esquemas.</span><span class="sxs-lookup"><span data-stu-id="c5de8-205">Credentials are never automatically transmitted with other schemes.</span></span>

<span data-ttu-id="c5de8-206">A política de logon automático pode ser definida usando a função [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) com a [**opção WinHTTP sinalizador de \_ \_ \_ política de autologoização**](option-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="c5de8-206">The auto-logon policy can be set using the [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) function with the [**WINHTTP\_OPTION\_AUTOLOGON\_POLICY**](option-flags.md) flag.</span></span> <span data-ttu-id="c5de8-207">Esse sinalizador se aplica somente ao identificador de solicitação.</span><span class="sxs-lookup"><span data-stu-id="c5de8-207">This flag applies only to the request handle.</span></span> <span data-ttu-id="c5de8-208">Quando a política é definida como WINHTTP \_ , o nível de segurança de logon automático é \_ \_ \_ baixo, as credenciais padrão podem ser enviadas para todos os servidores.</span><span class="sxs-lookup"><span data-stu-id="c5de8-208">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_LOW, default credentials can be sent to all servers.</span></span> <span data-ttu-id="c5de8-209">Quando a política é definida para o \_ nível de segurança do WinHTTP AUTOlogon \_ \_ \_ alto, as credenciais padrão não podem ser usadas para autenticação.</span><span class="sxs-lookup"><span data-stu-id="c5de8-209">When the policy is set to WINHTTP\_AUTOLOGON\_SECURITY\_LEVEL\_HIGH, default credentials cannot be used for authentication.</span></span> <span data-ttu-id="c5de8-210">É altamente recomendável que você use o logon automático no nível médio.</span><span class="sxs-lookup"><span data-stu-id="c5de8-210">It is strongly recommended that you use the auto-logon at the MEDIUM level.</span></span>

## <a name="stored-user-names-and-passwords"></a><span data-ttu-id="c5de8-211">Nomes de usuário e senhas armazenados</span><span class="sxs-lookup"><span data-stu-id="c5de8-211">Stored User Names and Passwords</span></span>

<span data-ttu-id="c5de8-212">O Windows XP introduziu o conceito de nomes de usuário e senhas armazenados.</span><span class="sxs-lookup"><span data-stu-id="c5de8-212">Windows XP introduced the concept of Stored User Names and Passwords.</span></span> <span data-ttu-id="c5de8-213">Se as credenciais do Passport de um usuário forem salvas por meio do **Assistente de registro do Passport** ou da caixa de **diálogo credencial** padrão, ela será salva nos nomes de usuário e senhas armazenados.</span><span class="sxs-lookup"><span data-stu-id="c5de8-213">If a user's Passport credentials are saved through the **Passport Registration Wizard** or the standard **Credential Dialog**, it is saved in the Stored User Names and Passwords.</span></span> <span data-ttu-id="c5de8-214">Ao usar o WinHTTP no Windows XP ou posterior, o WinHTTP usará automaticamente as credenciais nos nomes de usuário e senhas armazenados se as credenciais não estiverem definidas explicitamente.</span><span class="sxs-lookup"><span data-stu-id="c5de8-214">When using WinHTTP on Windows XP or later, WinHTTP automatically uses the credentials in the Stored User Names and Passwords if credentials are not explicitly set.</span></span> <span data-ttu-id="c5de8-215">Isso é semelhante ao suporte de credenciais de logon padrão para NTLM/Kerberos.</span><span class="sxs-lookup"><span data-stu-id="c5de8-215">This is similar to the support of default logon credentials for NTLM/Kerberos.</span></span> <span data-ttu-id="c5de8-216">No entanto, o uso de credenciais padrão do Passport não está sujeito às configurações de política de logon automático.</span><span class="sxs-lookup"><span data-stu-id="c5de8-216">However, use of default Passport credentials is not subject to the automatic logon policy settings.</span></span>

 

 



