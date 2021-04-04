---
title: Manipulando a autenticação
description: Alguns proxies e servidores exigem autenticação antes de conceder acesso aos recursos na Internet.
ms.assetid: f3752031-30d3-4e35-8eae-1d4971b66bc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36a8eaa38f61f0d97f1f543e0623313aa196aab7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104008530"
---
# <a name="handling-authentication"></a><span data-ttu-id="b08c1-103">Manipulando a autenticação</span><span class="sxs-lookup"><span data-stu-id="b08c1-103">Handling Authentication</span></span>

<span data-ttu-id="b08c1-104">Alguns proxies e servidores exigem autenticação antes de conceder acesso aos recursos na Internet.</span><span class="sxs-lookup"><span data-stu-id="b08c1-104">Some proxies and servers require authentication before granting access to resources on the Internet.</span></span> <span data-ttu-id="b08c1-105">As funções do WinINet dão suporte à autenticação de servidor e proxy para sessões http.</span><span class="sxs-lookup"><span data-stu-id="b08c1-105">The WinINet functions support server and proxy authentication for http sessions.</span></span> <span data-ttu-id="b08c1-106">A autenticação de servidores FTP deve ser tratada pela função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) .</span><span class="sxs-lookup"><span data-stu-id="b08c1-106">Authentication of ftp servers must be handled by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function.</span></span> <span data-ttu-id="b08c1-107">Atualmente, não há suporte para a autenticação de gateway de FTP.</span><span class="sxs-lookup"><span data-stu-id="b08c1-107">Currently, FTP gateway authentication is not supported.</span></span>

## <a name="about-http-authentication"></a><span data-ttu-id="b08c1-108">Sobre a autenticação HTTP</span><span class="sxs-lookup"><span data-stu-id="b08c1-108">About HTTP Authentication</span></span>

<span data-ttu-id="b08c1-109">Se a autenticação for necessária, o aplicativo cliente receberá um código de status 401, se o servidor exigir autenticação, ou 407, se o proxy exigir autenticação.</span><span class="sxs-lookup"><span data-stu-id="b08c1-109">If authentication is required, the client application receives a status code 401, if the server requires authentication, or 407, if the proxy requires authentication.</span></span> <span data-ttu-id="b08c1-110">Com o código de status, o proxy ou o servidor envia um ou mais cabeçalhos de resposta de autenticação — autenticar proxy (para autenticação de proxy) ou WWW-Authenticate (para autenticação de servidor).</span><span class="sxs-lookup"><span data-stu-id="b08c1-110">With the status code, the proxy or server sends one, or more, authenticate response headers—Proxy-Authenticate (for proxy authentication) or WWW-Authenticate (for server authentication).</span></span>

<span data-ttu-id="b08c1-111">Cada cabeçalho de resposta de autenticação contém um esquema de autenticação disponível e um realm.</span><span class="sxs-lookup"><span data-stu-id="b08c1-111">Each authenticate response header contains an available authentication scheme and a realm.</span></span> <span data-ttu-id="b08c1-112">Se houver suporte para vários esquemas de autenticação, o servidor retornará vários cabeçalhos de resposta de autenticações.</span><span class="sxs-lookup"><span data-stu-id="b08c1-112">If multiple authentication schemes are supported, the server returns multiple authenticate response headers.</span></span> <span data-ttu-id="b08c1-113">O valor do Realm diferenciam maiúsculas de minúsculas e definem um espaço de proteção no proxy ou servidor.</span><span class="sxs-lookup"><span data-stu-id="b08c1-113">The realm value is case-sensitive and defines a protection space on the proxy or server.</span></span> <span data-ttu-id="b08c1-114">Por exemplo, o cabeçalho "WWW-Authenticate: Basic real =" example "" seria um exemplo de um cabeçalho retornado quando a autenticação do servidor for necessária.</span><span class="sxs-lookup"><span data-stu-id="b08c1-114">For example, the header "WWW-Authenticate: Basic Realm="example"" would be an example of a header returned when server authentication is required.</span></span>

<span data-ttu-id="b08c1-115">O aplicativo cliente que enviou a solicitação pode se autenticar, incluindo um campo de cabeçalho de autorização com a solicitação.</span><span class="sxs-lookup"><span data-stu-id="b08c1-115">The client application that sent the request can authenticate itself by including an Authorization header field with the request.</span></span> <span data-ttu-id="b08c1-116">O cabeçalho Authorization conterá o esquema de autenticação e a resposta apropriada exigida por esse esquema.</span><span class="sxs-lookup"><span data-stu-id="b08c1-116">The Authorization header would contain the authentication scheme and the appropriate response required by that scheme.</span></span> <span data-ttu-id="b08c1-117">Por exemplo, o cabeçalho "Authorization: Basic <nome de usuário: Password>" seria adicionado à solicitação e reenviado para o servidor se o cliente recebeu o cabeçalho de resposta de autenticação "WWW-Authenticate: Basic real =" example "".</span><span class="sxs-lookup"><span data-stu-id="b08c1-117">For example, the header "Authorization: Basic <username:password>" would be added to the request and re-sent to the server if the client received the authenticate response header "WWW-Authenticate: Basic Realm="example"".</span></span>

<span data-ttu-id="b08c1-118">Há dois tipos gerais de esquemas de autenticação:</span><span class="sxs-lookup"><span data-stu-id="b08c1-118">There are two general types of authentication schemes:</span></span>

-   <span data-ttu-id="b08c1-119">Esquema de autenticação básica, em que o nome de usuário e a senha são enviados em texto não criptografado para o servidor.</span><span class="sxs-lookup"><span data-stu-id="b08c1-119">Basic authentication scheme, where the user name and password are sent in cleartext to the server.</span></span>
-   <span data-ttu-id="b08c1-120">Esquemas de desafio/resposta, que permitem um formato de desafio/resposta.</span><span class="sxs-lookup"><span data-stu-id="b08c1-120">Challenge-response schemes, which allow for a challenge-response format.</span></span>

<span data-ttu-id="b08c1-121">O esquema de autenticação básica é baseado no modelo que um cliente deve autenticar a si mesmo com um nome de usuário e senha para cada realm.</span><span class="sxs-lookup"><span data-stu-id="b08c1-121">The Basic authentication scheme is based on the model that a client must authenticate itself with a user name and password for each realm.</span></span> <span data-ttu-id="b08c1-122">O servidor serviçosá a solicitação se ele for reenviado com um cabeçalho de autorização que inclua um nome de usuário e senha válidos.</span><span class="sxs-lookup"><span data-stu-id="b08c1-122">The server services the request if it is resent with an Authorization header that includes a valid user name and password.</span></span>

<span data-ttu-id="b08c1-123">Os esquemas de desafio/resposta permitem uma autenticação mais segura.</span><span class="sxs-lookup"><span data-stu-id="b08c1-123">Challenge-response schemes enable more secure authentication.</span></span> <span data-ttu-id="b08c1-124">Se uma solicitação exigir autenticação usando um esquema de desafio/resposta, o código de status apropriado e os cabeçalhos de autenticação serão retornados ao cliente.</span><span class="sxs-lookup"><span data-stu-id="b08c1-124">If a request requires authentication using a challenge-response scheme, the appropriate status code and Authenticate headers are returned to the client.</span></span> <span data-ttu-id="b08c1-125">O cliente deve, então, reenviar a solicitação com um Negotiate.</span><span class="sxs-lookup"><span data-stu-id="b08c1-125">The client must then to resend the request with a negotiate.</span></span> <span data-ttu-id="b08c1-126">O servidor retornaria um código de status apropriado com um desafio e, em seguida, o cliente exigiria reenviar a solicitação com a resposta correta para obter o serviço solicitado.</span><span class="sxs-lookup"><span data-stu-id="b08c1-126">The server would return an appropriate status code with a challenge, and the client would then require to resend the request with the proper response to get the requested service.</span></span>

<span data-ttu-id="b08c1-127">A tabela a seguir lista os esquemas de autenticação, o tipo de autenticação, a DLL que oferece suporte a eles e uma descrição do esquema.</span><span class="sxs-lookup"><span data-stu-id="b08c1-127">The following table lists authentication schemes, the authentication type, the DLL that supports them, and a description of the scheme.</span></span>



| <span data-ttu-id="b08c1-128">Esquema</span><span class="sxs-lookup"><span data-stu-id="b08c1-128">Scheme</span></span>                                    | <span data-ttu-id="b08c1-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b08c1-129">Type</span></span>               | <span data-ttu-id="b08c1-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b08c1-130">DLL</span></span>                  | <span data-ttu-id="b08c1-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="b08c1-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|-------------------------------------------|--------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b08c1-132">Básico (texto não criptografado)</span><span class="sxs-lookup"><span data-stu-id="b08c1-132">Basic (cleartext)</span></span>                         | <span data-ttu-id="b08c1-133">básico</span><span class="sxs-lookup"><span data-stu-id="b08c1-133">basic</span></span>              | <span data-ttu-id="b08c1-134">Wininet.dll</span><span class="sxs-lookup"><span data-stu-id="b08c1-134">Wininet.dll</span></span>          | <span data-ttu-id="b08c1-135">Usa uma cadeia de caracteres codificada em base64 que contém o nome de usuário e a senha.</span><span class="sxs-lookup"><span data-stu-id="b08c1-135">Uses a base64 encoded string that contains the user name and password.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b08c1-136">Digest</span><span class="sxs-lookup"><span data-stu-id="b08c1-136">Digest</span></span>                                    | <span data-ttu-id="b08c1-137">desafio-resposta</span><span class="sxs-lookup"><span data-stu-id="b08c1-137">challenge-response</span></span> | <span data-ttu-id="b08c1-138">Digest.dll</span><span class="sxs-lookup"><span data-stu-id="b08c1-138">Digest.dll</span></span>           | <span data-ttu-id="b08c1-139">Um esquema de desafio/resposta que desafia o uso de um valor nonce (uma cadeia de caracteres de dados especificada pelo servidor).</span><span class="sxs-lookup"><span data-stu-id="b08c1-139">A challenge-response scheme that challenges using a nonce (a server-specified data string) value.</span></span> <span data-ttu-id="b08c1-140">Uma resposta válida contém uma soma de verificação do nome de usuário, a senha, o valor de nonce fornecido, o método HTTP e o Uniform Resource Identifier (URI) solicitado.</span><span class="sxs-lookup"><span data-stu-id="b08c1-140">A valid response contains a checksum of the user name, the password, the given nonce value, the HTTP method, and the requested Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="b08c1-141">O suporte à autenticação Digest foi introduzido no Microsoft Internet Explorer 5.</span><span class="sxs-lookup"><span data-stu-id="b08c1-141">Digest authentication support was introduced in Microsoft Internet Explorer 5.</span></span> |
| <span data-ttu-id="b08c1-142">NTLM (NT LAN Manager)</span><span class="sxs-lookup"><span data-stu-id="b08c1-142">NT LAN Manager (NTLM)</span></span>                     | <span data-ttu-id="b08c1-143">desafio-resposta</span><span class="sxs-lookup"><span data-stu-id="b08c1-143">challenge-response</span></span> | <span data-ttu-id="b08c1-144">Winsspi.dll</span><span class="sxs-lookup"><span data-stu-id="b08c1-144">Winsspi.dll</span></span>          | <span data-ttu-id="b08c1-145">Um esquema de desafio/resposta que baseia o desafio no nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="b08c1-145">A challenge-response scheme that bases the challenge on the user name.</span></span>                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="b08c1-146">Rede da Microsoft (MSN)</span><span class="sxs-lookup"><span data-stu-id="b08c1-146">Microsoft Network (MSN)</span></span>                   | <span data-ttu-id="b08c1-147">desafio-resposta</span><span class="sxs-lookup"><span data-stu-id="b08c1-147">challenge-response</span></span> | <span data-ttu-id="b08c1-148">Msnsspc.dll</span><span class="sxs-lookup"><span data-stu-id="b08c1-148">Msnsspc.dll</span></span>          | <span data-ttu-id="b08c1-149">O esquema de autenticação da rede da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b08c1-149">The Microsoft Network's authentication scheme.</span></span>                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="b08c1-150">DPA (autenticação de senha distribuída)</span><span class="sxs-lookup"><span data-stu-id="b08c1-150">Distributed Password Authentication (DPA)</span></span> | <span data-ttu-id="b08c1-151">desafio-resposta</span><span class="sxs-lookup"><span data-stu-id="b08c1-151">challenge-response</span></span> | <span data-ttu-id="b08c1-152">Msapsspc.dll</span><span class="sxs-lookup"><span data-stu-id="b08c1-152">Msapsspc.dll</span></span>         | <span data-ttu-id="b08c1-153">Semelhante à autenticação do MSN e também é usado pela rede da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b08c1-153">Similar to MSN authentication and is also used by the Microsoft Network.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="b08c1-154">Autenticação de senha remota (RPA)</span><span class="sxs-lookup"><span data-stu-id="b08c1-154">Remote Passphrase Authentication (RPA)</span></span>    | <span data-ttu-id="b08c1-155">CompuServe</span><span class="sxs-lookup"><span data-stu-id="b08c1-155">CompuServe</span></span>         | <span data-ttu-id="b08c1-156">Rpawinet.dll, da.dll</span><span class="sxs-lookup"><span data-stu-id="b08c1-156">Rpawinet.dll, da.dll</span></span> | <span data-ttu-id="b08c1-157">Esquema de autenticação do CompuServe.</span><span class="sxs-lookup"><span data-stu-id="b08c1-157">CompuServe authentication scheme.</span></span> <span data-ttu-id="b08c1-158">Para obter mais informações, consulte as [especificações do mecanismo do RPA](https://www.compuserve.com/).</span><span class="sxs-lookup"><span data-stu-id="b08c1-158">For more information, see the [RPA Mechanism Specifications](https://www.compuserve.com/).</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="b08c1-159">Para qualquer coisa que não seja a autenticação básica, as chaves do registro devem ser configuradas, além da instalação da DLL apropriada.</span><span class="sxs-lookup"><span data-stu-id="b08c1-159">For anything other than Basic authentication, the registry keys must be set up in addition to installing the appropriate DLL.</span></span>

<span data-ttu-id="b08c1-160">Se a autenticação for necessária, o sinalizador [ \_ \_ manter \_ conexão da Internet](api-flags.md) deve ser usado na chamada para [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="b08c1-160">If authentication is required, the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag should be used in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="b08c1-161">O sinalizador \_ \_ para manter \_ a conexão com a Internet é necessário para NTLM e outros tipos de autenticação para manter a conexão ao concluir o processo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="b08c1-161">The INTERNET\_FLAG\_KEEP\_CONNECTION flag is required for NTLM and other types of authentication in order to maintain the connection while completing the authentication process.</span></span> <span data-ttu-id="b08c1-162">Se a conexão não for mantida, o processo de autenticação deverá ser reiniciado com o proxy ou o servidor.</span><span class="sxs-lookup"><span data-stu-id="b08c1-162">If the connection is not maintained, the authentication process must be restarted with the proxy or server.</span></span>

<span data-ttu-id="b08c1-163">As funções [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) são concluídas com êxito mesmo quando a autenticação é necessária.</span><span class="sxs-lookup"><span data-stu-id="b08c1-163">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions complete successfully even when authentication is required.</span></span> <span data-ttu-id="b08c1-164">A diferença é que os dados retornados nos arquivos de cabeçalho e [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) receberão uma página HTML informando ao usuário do código de status.</span><span class="sxs-lookup"><span data-stu-id="b08c1-164">The difference is, the data returned in the header files and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) would receive an HTML page informing the user of the status code.</span></span>

### <a name="registering-authentication-keys"></a><span data-ttu-id="b08c1-165">Registrando chaves de autenticação</span><span class="sxs-lookup"><span data-stu-id="b08c1-165">Registering Authentication Keys</span></span>

<span data-ttu-id="b08c1-166">INTERNET \_ Open \_ Type a \_ preconfig examina os valores de registro **ProxyEnable**, **ProxyServer** e **ProxyOverride**.</span><span class="sxs-lookup"><span data-stu-id="b08c1-166">INTERNET\_OPEN\_TYPE\_PRECONFIG looks at the registry values **ProxyEnable**, **ProxyServer**, and **ProxyOverride**.</span></span> <span data-ttu-id="b08c1-167">Esses valores estão localizados em **HKEY \_ Current \_ User** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Internet Settings**.</span><span class="sxs-lookup"><span data-stu-id="b08c1-167">These values are located under **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Internet Settings**.</span></span>

<span data-ttu-id="b08c1-168">Para esquemas de autenticação diferentes do básico, uma chave deve ser adicionada ao registro em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**.</span><span class="sxs-lookup"><span data-stu-id="b08c1-168">For authentication schemes other than Basic, a key must be added to the registry under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="b08c1-169">Um valor **DWORD** , **flags**, deve ser definido com o valor apropriado.</span><span class="sxs-lookup"><span data-stu-id="b08c1-169">A **DWORD** value, **Flags**, should be set with the appropriate value.</span></span> <span data-ttu-id="b08c1-170">A lista a seguir mostra os valores possíveis para o valor de **flags** .</span><span class="sxs-lookup"><span data-stu-id="b08c1-170">The following list shows the possible values for the **Flags** value.</span></span>

-   <span data-ttu-id="b08c1-171">\_ \_ \_ Contexto exclusivo dos sinalizadores \_ de autenticação do plugin \_ por \_ tcpip (valor = 0x01)</span><span class="sxs-lookup"><span data-stu-id="b08c1-171">PLUGIN\_AUTH\_FLAGS\_UNIQUE\_CONTEXT\_PER\_TCPIP (value=0x01)</span></span>

    <span data-ttu-id="b08c1-172">Cada soquete do protocolo TCP/IP (Transmission Control Protocol/Internet Protocol) contém um contexto diferente.</span><span class="sxs-lookup"><span data-stu-id="b08c1-172">Each Transmission Control Protocol/Internet Protocol (TCP/IP) socket contains a different context.</span></span> <span data-ttu-id="b08c1-173">Caso contrário, um novo contexto é passado para cada modelo de URL de bloco ou realm.</span><span class="sxs-lookup"><span data-stu-id="b08c1-173">Otherwise, a new context is passed for each realm or block URL template.</span></span>

-   <span data-ttu-id="b08c1-174">Os \_ sinalizadores de autenticação do plug-in \_ \_ podem \_ manipular a \_ interface do usuário (valor = 0x02)</span><span class="sxs-lookup"><span data-stu-id="b08c1-174">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_UI (value=0x02)</span></span>

    <span data-ttu-id="b08c1-175">Essa DLL pode tratar sua própria entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="b08c1-175">This DLL can handle its own user input.</span></span>

-   <span data-ttu-id="b08c1-176">Os \_ sinalizadores de autenticação do plug-in \_ \_ \_ não podem lidar com \_ \_ passwd (Value = 0x04)</span><span class="sxs-lookup"><span data-stu-id="b08c1-176">PLUGIN\_AUTH\_FLAGS\_CAN\_HANDLE\_NO\_PASSWD (value=0x04)</span></span>

    <span data-ttu-id="b08c1-177">Essa DLL pode ser capaz de fazer uma autenticação sem solicitar uma senha ao usuário.</span><span class="sxs-lookup"><span data-stu-id="b08c1-177">This DLL might be capable of doing an authentication without prompting the user for a password.</span></span>

-   <span data-ttu-id="b08c1-178">\_Sinalizadores de autenticação do plug-in \_ \_ sem \_ Realm (valor = 0x08)</span><span class="sxs-lookup"><span data-stu-id="b08c1-178">PLUGIN\_AUTH\_FLAGS\_NO\_REALM (value=0x08)</span></span>

    <span data-ttu-id="b08c1-179">Essa DLL não usa uma cadeia de caracteres de realm http padrão.</span><span class="sxs-lookup"><span data-stu-id="b08c1-179">This DLL does not use a standard http realm string.</span></span> <span data-ttu-id="b08c1-180">Todos os dados que parecem ser um realm são dados específicos do esquema.</span><span class="sxs-lookup"><span data-stu-id="b08c1-180">Any data that appears to be a realm is scheme-specific data.</span></span>

-   <span data-ttu-id="b08c1-181">\_Não são \_ necessários sinalizadores de autenticação do plug-in \_ Keep \_ Alive \_ \_ (valor = 0x10)</span><span class="sxs-lookup"><span data-stu-id="b08c1-181">PLUGIN\_AUTH\_FLAGS\_KEEP\_ALIVE\_NOT\_REQUIRED (value=0x10)</span></span>

    <span data-ttu-id="b08c1-182">Essa DLL não requer uma conexão persistente para sua sequência de desafio/resposta.</span><span class="sxs-lookup"><span data-stu-id="b08c1-182">This DLL does not require a persistent connection for its challenge-response sequence.</span></span>

<span data-ttu-id="b08c1-183">Por exemplo, para adicionar a autenticação NTLM, a chave NTLM deve ser adicionada ao **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security**.</span><span class="sxs-lookup"><span data-stu-id="b08c1-183">For example, to add NTLM authentication, the key NTLM must be added to **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**.</span></span> <span data-ttu-id="b08c1-184">Em **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\ **Security** \\ **NTLM**, o valor da cadeia de caracteres, **DLLFile** e um valor **DWORD** , **flags**, devem ser adicionados.</span><span class="sxs-lookup"><span data-stu-id="b08c1-184">Under **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Internet Explorer**\\**Security**\\**NTLM**, the string value, **DLLFile**, and a **DWORD** value, **Flags**, must be added.</span></span> <span data-ttu-id="b08c1-185">**DLLFile** deve ser definido como Winsspi.dll e os **sinalizadores** devem ser definidos como 0x08.</span><span class="sxs-lookup"><span data-stu-id="b08c1-185">**DLLFile** must be set to Winsspi.dll, and **Flags** must be set to 0x08.</span></span>

### <a name="server-authentication"></a><span data-ttu-id="b08c1-186">Autenticação do servidor</span><span class="sxs-lookup"><span data-stu-id="b08c1-186">Server Authentication</span></span>

<span data-ttu-id="b08c1-187">Quando um servidor recebe uma solicitação que requer autenticação, o servidor retorna uma mensagem de código de status 401.</span><span class="sxs-lookup"><span data-stu-id="b08c1-187">When a server receives a request that requires authentication, the server returns a 401 status code message.</span></span> <span data-ttu-id="b08c1-188">Nessa mensagem, o servidor deve incluir um ou mais cabeçalhos de resposta WWW-Authenticate.</span><span class="sxs-lookup"><span data-stu-id="b08c1-188">In that message, the server should include one or more WWW-Authenticate response headers.</span></span> <span data-ttu-id="b08c1-189">Esses cabeçalhos incluem os métodos de autenticação disponíveis para o servidor.</span><span class="sxs-lookup"><span data-stu-id="b08c1-189">These headers include the authentication methods the server has available.</span></span> <span data-ttu-id="b08c1-190">O WinINet escolhe o primeiro método que reconhece.</span><span class="sxs-lookup"><span data-stu-id="b08c1-190">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="b08c1-191">A autenticação básica fornece segurança fraca, a menos que o canal seja primeiro criptografado por link com SSL ou PCT.</span><span class="sxs-lookup"><span data-stu-id="b08c1-191">Basic authentication provides weak security unless the channel is first link-encrypted with SSL or PCT.</span></span>

<span data-ttu-id="b08c1-192">A função [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) pode ser usada para obter os dados de nome de usuário e senha do usuário, ou uma interface do usuário personalizada pode ser projetada para obter os dados.</span><span class="sxs-lookup"><span data-stu-id="b08c1-192">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed to obtain the data.</span></span>

<span data-ttu-id="b08c1-193">Uma interface personalizada pode usar a função [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) para definir a [ \_ \_ senha da opção de Internet](option-flags.md) e os valores de nome de [ \_ \_ usuário da opção de Internet](option-flags.md) e, em seguida, reenviar a solicitação para o servidor.</span><span class="sxs-lookup"><span data-stu-id="b08c1-193">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_USERNAME](option-flags.md) values and then resend the request to the server.</span></span>

### <a name="proxy-authentication"></a><span data-ttu-id="b08c1-194">Autenticação de proxy</span><span class="sxs-lookup"><span data-stu-id="b08c1-194">Proxy Authentication</span></span>

<span data-ttu-id="b08c1-195">Quando um cliente tenta usar um proxy que requer autenticação, o proxy Retorna uma mensagem de código de status 407 para o cliente.</span><span class="sxs-lookup"><span data-stu-id="b08c1-195">When a client attempts to use a proxy that requires authentication, the proxy returns a 407 status code message to the client.</span></span> <span data-ttu-id="b08c1-196">Nessa mensagem, o proxy deve incluir um ou mais cabeçalhos de resposta Proxy-Authenticate.</span><span class="sxs-lookup"><span data-stu-id="b08c1-196">In that message, the proxy should include one or more Proxy-Authenticate response headers.</span></span> <span data-ttu-id="b08c1-197">Esses cabeçalhos incluem os métodos de autenticação disponíveis do proxy.</span><span class="sxs-lookup"><span data-stu-id="b08c1-197">These headers include the authentication methods available from the proxy.</span></span> <span data-ttu-id="b08c1-198">O WinINet escolhe o primeiro método que reconhece.</span><span class="sxs-lookup"><span data-stu-id="b08c1-198">WinINet chooses the first method it recognizes.</span></span>

<span data-ttu-id="b08c1-199">A função [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) pode ser usada para obter os dados de nome de usuário e senha do usuário, ou uma interface do usuário personalizada pode ser projetada.</span><span class="sxs-lookup"><span data-stu-id="b08c1-199">The [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) function can be used to obtain the user name and password data from the user, or a customized user interface can be designed.</span></span>

<span data-ttu-id="b08c1-200">Uma interface personalizada pode usar a função [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) para definir a [ \_ \_ \_ senha do proxy de opção da Internet](option-flags.md) e os valores de nome de [ \_ \_ \_ usuário do proxy de opção de Internet](option-flags.md) e, em seguida, reenviar a solicitação para o proxy.</span><span class="sxs-lookup"><span data-stu-id="b08c1-200">A custom interface can use the [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) function to set the [INTERNET\_OPTION\_PROXY\_PASSWORD](option-flags.md) and [INTERNET\_OPTION\_PROXY\_USERNAME](option-flags.md) values and then resend the request to the proxy.</span></span>

<span data-ttu-id="b08c1-201">Se nenhum nome de usuário e senha de proxy forem definidos, o WinINet tentará usar o nome de usuário e a senha para o servidor.</span><span class="sxs-lookup"><span data-stu-id="b08c1-201">If no proxy user name and password are set, WinINet attempts to use the user name and password for the server.</span></span> <span data-ttu-id="b08c1-202">Esse comportamento permite que os clientes implementem a mesma interface de usuário personalizada usada para lidar com a autenticação do servidor.</span><span class="sxs-lookup"><span data-stu-id="b08c1-202">This behavior enables clients to implement the same customized user interface used to handle server authentication.</span></span>

## <a name="handling-http-authentication"></a><span data-ttu-id="b08c1-203">Manipulando a autenticação HTTP</span><span class="sxs-lookup"><span data-stu-id="b08c1-203">Handling HTTP Authentication</span></span>

<span data-ttu-id="b08c1-204">A autenticação HTTP pode ser tratada com o [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) ou com uma função personalizada que usa [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) ou adiciona seus próprios cabeçalhos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="b08c1-204">HTTP authentication can be handled with either [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or a customized function that uses [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) or adds its own authentication headers.</span></span> <span data-ttu-id="b08c1-205">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) pode examinar os cabeçalhos associados a um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) para localizar erros ocultos, como códigos de status de um proxy ou servidor.</span><span class="sxs-lookup"><span data-stu-id="b08c1-205">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can examine the headers associated with an [**HINTERNET**](appendix-a-hinternet-handles.md) handle to find hidden errors, such as status codes from a proxy or server.</span></span> <span data-ttu-id="b08c1-206">O [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) pode ser usado para definir o nome de usuário e a senha para o proxy e o servidor.</span><span class="sxs-lookup"><span data-stu-id="b08c1-206">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) can be used to set the user name and password for the proxy and server.</span></span> <span data-ttu-id="b08c1-207">Para a autenticação do MSN e DPA, [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) deve ser usado para definir o nome de usuário e a senha.</span><span class="sxs-lookup"><span data-stu-id="b08c1-207">For MSN and DPA authentication, [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) must be used to set the user name and password.</span></span>

<span data-ttu-id="b08c1-208">Para qualquer função personalizada que adicione seus próprios cabeçalhos WWW-Authenticate ou Proxy-Authenticate, o [sinalizador \_ Internet \_ não \_ ](api-flags.md) deve ser definido para desabilitar a autenticação.</span><span class="sxs-lookup"><span data-stu-id="b08c1-208">For any customized function that adds its own WWW-Authenticate or Proxy-Authenticate headers, the [INTERNET\_FLAG\_NO\_AUTH](api-flags.md) flag should be set to disable authentication.</span></span>

<span data-ttu-id="b08c1-209">O exemplo a seguir mostra como [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) pode ser usado para manipular a autenticação http.</span><span class="sxs-lookup"><span data-stu-id="b08c1-209">The following example shows how [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) can be used to handle HTTP authentication.</span></span>


```C++
HINTERNET hOpenHandle,  hConnectHandle, hResourceHandle;
DWORD dwError, dwErrorCode;
HWND hwnd = GetConsoleWindow();

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG, 
                           NULL, NULL, 0);

hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"), 
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL, 
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL, 
                                  INTERNET_FLAG_KEEP_CONNECTION, 0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

// dwErrorCode stores the error code associated with the call to
// HttpSendRequest.  

dwErrorCode = hResourceHandle ? ERROR_SUCCESS : GetLastError();

dwError = InternetErrorDlg(hwnd, hResourceHandle, dwErrorCode, 
                           FLAGS_ERROR_UI_FILTER_FOR_ERRORS | 
                           FLAGS_ERROR_UI_FLAGS_CHANGE_OPTIONS |
                           FLAGS_ERROR_UI_FLAGS_GENERATE_DATA,
                           NULL);

if (dwError == ERROR_INTERNET_FORCE_RETRY)
    goto resend;

// Insert code to read the data from the hResourceHandle
// at this point.

```



<span data-ttu-id="b08c1-210">No exemplo, dwErrorCode é usado para armazenar quaisquer erros associados à chamada para [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="b08c1-210">In the example, dwErrorCode is used to store any errors associated with the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="b08c1-211">O [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) é concluído com êxito, mesmo que o proxy ou o servidor exija autenticação.</span><span class="sxs-lookup"><span data-stu-id="b08c1-211">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) completes successfully, even if the proxy or server requires authentication.</span></span> <span data-ttu-id="b08c1-212">Quando o \_ \_ \_ sinalizador filtro de IU \_ de erro de sinalizadores para \_ erros é passado para [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), a função verifica os cabeçalhos em busca de erros ocultos.</span><span class="sxs-lookup"><span data-stu-id="b08c1-212">When the FLAGS\_ERROR\_UI\_FILTER\_FOR\_ERRORS flag is passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), the function checks the headers for any hidden errors.</span></span> <span data-ttu-id="b08c1-213">Esses erros ocultos incluem qualquer solicitação de autenticação.</span><span class="sxs-lookup"><span data-stu-id="b08c1-213">These hidden errors would include any requests for authentication.</span></span> <span data-ttu-id="b08c1-214">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) exibe a caixa de diálogo apropriada para solicitar os dados necessários ao usuário.</span><span class="sxs-lookup"><span data-stu-id="b08c1-214">[**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) displays the appropriate dialog box to prompt the user for the necessary data.</span></span> <span data-ttu-id="b08c1-215">Os sinalizadores da interface do usuário de erros de sinalizadores \_ \_ \_ \_ GERAm \_ dados e sinalizadores sinalizadores de \_ \_ interface do usuário de erro de \_ \_ alteração \_ sinalizadores de opções também devem ser passados para [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), para que a função Construa a estrutura de dados apropriada para o erro e armazene os resultados da caixa de diálogo no identificador [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="b08c1-215">The FLAGS\_ERROR\_UI\_FLAGS\_GENERATE\_DATA and FLAGS\_ERROR\_UI\_FLAGS\_CHANGE\_OPTIONS flags should also be passed to [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg), so that the function constructs the appropriate data structure for the error and stores the results of the dialog box in the [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span>

<span data-ttu-id="b08c1-216">O código de exemplo a seguir mostra como a autenticação pode ser tratada usando [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="b08c1-216">The following example code shows how authentication could be handled using [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


```C++
HINTERNET hOpenHandle,  hResourceHandle, hConnectHandle;
DWORD dwStatus;
DWORD dwStatusSize = sizeof(dwStatus);
char strUsername[64], strPassword[64];

// Normally, hOpenHandle, hResourceHandle,
// and hConnectHandle need to be properly assigned.

hOpenHandle = InternetOpen(TEXT("Example"),
                           INTERNET_OPEN_TYPE_PRECONFIG,
                           NULL, NULL, 0);
hConnectHandle = InternetConnect(hOpenHandle,
                                 TEXT("www.server.com"),
                                 INTERNET_INVALID_PORT_NUMBER,
                                 NULL,
                                 NULL,
                                 INTERNET_SERVICE_HTTP,
                                 0,0);

hResourceHandle = HttpOpenRequest(hConnectHandle, TEXT("GET"),
                                  TEXT("/premium/default.htm"),
                                  NULL, NULL, NULL,
                                  INTERNET_FLAG_KEEP_CONNECTION,
                                  0);

resend:

HttpSendRequest(hResourceHandle, NULL, 0, NULL, 0);

HttpQueryInfo(hResourceHandle, HTTP_QUERY_FLAG_NUMBER |
              HTTP_QUERY_STATUS_CODE, &dwStatus, &dwStatusSize, NULL);

switch (dwStatus)
{
    // cchUserLength is the length of strUsername and
    // cchPasswordLength is the length of strPassword.
    DWORD cchUserLength, cchPasswordLength;

    case HTTP_STATUS_PROXY_AUTH_REQ: // Proxy Authentication Required
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert appropriate error handling code.
        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_USERNAME,
                          strUsername,
                          cchUserLength+1);

        InternetSetOption(hResourceHandle,
                          INTERNET_OPTION_PROXY_PASSWORD,
                          strPassword,
                          cchPasswordLength+1);
        goto resend;
        break;

    case HTTP_STATUS_DENIED:     // Server Authentication Required.
        // Insert code to set strUsername and strPassword.

        // Insert code to safely determine cchUserLength and
        // cchPasswordLength. Insert error handling code as
        // appropriate.
        InternetSetOption(hResourceHandle, INTERNET_OPTION_USERNAME,
                          strUsername, cchUserLength+1);
        InternetSetOption(hResourceHandle, INTERNET_OPTION_PASSWORD,
                          strPassword, cchPasswordLength+1);
        goto resend;
        break;
}

// Insert code to read the data from the hResourceHandle
// at this point.

```



> [!Note]  
> <span data-ttu-id="b08c1-217">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="b08c1-217">WinINet does not support server implementations.</span></span> <span data-ttu-id="b08c1-218">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="b08c1-218">In addition, it should not be used from a service.</span></span> <span data-ttu-id="b08c1-219">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="b08c1-219">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 