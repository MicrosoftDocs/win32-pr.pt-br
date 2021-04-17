---
description: Esta seção demonstra como escrever um script que usa o objeto WinHttpRequest para acessar dados de um servidor que requer autenticação HTTP.
ms.assetid: 9e46777c-4d79-4f9b-9b31-1280ed1e3289
title: Autenticação usando script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1d33b8042cd1fd15d46e15dfb3624e0d3b4a885b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798559"
---
# <a name="authentication-using-script"></a><span data-ttu-id="be190-103">Autenticação usando script</span><span class="sxs-lookup"><span data-stu-id="be190-103">Authentication Using Script</span></span>

<span data-ttu-id="be190-104">Esta seção demonstra como escrever um script que usa o objeto [**WinHttpRequest**](winhttprequest.md) para acessar dados de um servidor que requer autenticação http.</span><span class="sxs-lookup"><span data-stu-id="be190-104">This section demonstrates how to write script that uses the [**WinHttpRequest**](winhttprequest.md) object to access data from a server that requires HTTP authentication.</span></span>

-   [<span data-ttu-id="be190-105">Pré-requisitos e requisitos</span><span class="sxs-lookup"><span data-stu-id="be190-105">Prerequisites and Requirements</span></span>](#prerequisites-and-requirements)
-   [<span data-ttu-id="be190-106">Acessando um site com autenticação</span><span class="sxs-lookup"><span data-stu-id="be190-106">Accessing a Web Site With Authentication</span></span>](#accessing-a-web-site-with-authentication)
-   [<span data-ttu-id="be190-107">Verificando os códigos de status</span><span class="sxs-lookup"><span data-stu-id="be190-107">Checking the Status Codes</span></span>](#checking-the-status-codes)
-   [<span data-ttu-id="be190-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="be190-108">Related topics</span></span>](#related-topics)

## <a name="prerequisites-and-requirements"></a><span data-ttu-id="be190-109">Pré-requisitos e requisitos</span><span class="sxs-lookup"><span data-stu-id="be190-109">Prerequisites and Requirements</span></span>

<span data-ttu-id="be190-110">Além de um conhecimento prático do Microsoft JScript, este exemplo requer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="be190-110">In addition to a working knowledge of Microsoft JScript, this example requires the following:</span></span>

-   <span data-ttu-id="be190-111">A versão atual do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="be190-111">The current version of the Microsoft Windows Software Development Kit (SDK).</span></span>
-   <span data-ttu-id="be190-112">A ferramenta de configuração de proxy para estabelecer as configurações de proxy para o Microsoft Windows HTTP Services (WinHTTP), se a conexão com a Internet for por meio de um servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="be190-112">The proxy configuration tool to establish the proxy settings for Microsoft Windows HTTP Services (WinHTTP), if your connection to the Internet is through a proxy server.</span></span> <span data-ttu-id="be190-113">Consulte [Proxycfg.exe, uma ferramenta de configuração de proxy](proxycfg-exe--a-proxy-configuration-tool.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="be190-113">See [Proxycfg.exe, a Proxy Configuration Tool](proxycfg-exe--a-proxy-configuration-tool.md) for more information.</span></span>
-   <span data-ttu-id="be190-114">Familiaridade com a [terminologia](network-terminology.md) e os conceitos de rede.</span><span class="sxs-lookup"><span data-stu-id="be190-114">A familiarity with [network terminology](network-terminology.md) and concepts.</span></span>

## <a name="accessing-a-web-site-with-authentication"></a><span data-ttu-id="be190-115">Acessando um site com autenticação</span><span class="sxs-lookup"><span data-stu-id="be190-115">Accessing a Web Site With Authentication</span></span>

<span data-ttu-id="be190-116">**Para criar um script que demonstre a autenticação, faça o seguinte:**</span><span class="sxs-lookup"><span data-stu-id="be190-116">**To create a script that demonstrates authentication, do the following:**</span></span>

1.  <span data-ttu-id="be190-117">Abra um editor de texto como o bloco de notas da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="be190-117">Open a text editor such as Microsoft Notepad.</span></span>
2.  <span data-ttu-id="be190-118">Copie o código a seguir no editor de texto depois de substituir " \[ authenticationSite \] " pelo texto apropriado para especificar a URL de um site que requer autenticação http.</span><span class="sxs-lookup"><span data-stu-id="be190-118">Copy the following code into the text editor after replacing "\[authenticationSite\]" with the appropriate text to specify the URL of a site that requires HTTP authentication.</span></span>

    ```VB
    // Load the WinHttpRequest object.
    var WinHttpReq = 
              new ActiveXObject("WinHttp.WinHttpRequest.5.1");

    function getText1( )
    {
      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false;

      // Send a request to the server and wait for a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "No Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText);
      WScript.Echo( WinHttpReq.GetAllResponseHeaders);
      WScript.Echo( );
    };

    function getText2( )
    {
      // HttpRequest SetCredentials flags
      HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;

      // Specify the target resource.
      WinHttpReq.open( "GET", 
                       "https://[authenticationSite]", 
                       false );

      // Set credentials for server.
      WinHttpReq.SetCredentials( "User Name", 
                                 "Password",
                                 HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

      // It might also be necessary to supply credentials 
      // to the proxy if you connect to the Internet 
      // through a proxy that requires authentication.

      // Send a request to the server and wait for 
      // a response.
      WinHttpReq.send( );

      // Display the results of the request.
      WScript.Echo( "Credentials: " );
      WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
      WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
      WScript.Echo( );
    };

    getText1( );
    getText2( );
    ```

    

3.  <span data-ttu-id="be190-119">Salve o arquivo como "Auth.js".</span><span class="sxs-lookup"><span data-stu-id="be190-119">Save the file as "Auth.js".</span></span>
4.  <span data-ttu-id="be190-120">Em um prompt de comando, digite "cscript Auth.js" e pressione ENTER.</span><span class="sxs-lookup"><span data-stu-id="be190-120">From a command prompt, type "cscript Auth.js" and press ENTER.</span></span>

<span data-ttu-id="be190-121">Agora você tem um programa que solicita um recurso de duas maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="be190-121">You now have a program that requests a resource two different ways.</span></span> <span data-ttu-id="be190-122">O primeiro método solicita o recurso sem fornecer credenciais.</span><span class="sxs-lookup"><span data-stu-id="be190-122">The first method requests the resource without supplying credentials.</span></span> <span data-ttu-id="be190-123">Um código de status 401 é retornado para indicar que o servidor requer autenticação.</span><span class="sxs-lookup"><span data-stu-id="be190-123">A 401 status code is returned to indicate that the server requires authentication.</span></span> <span data-ttu-id="be190-124">Os cabeçalhos de resposta também são exibidos e devem ser semelhantes ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="be190-124">The response headers are also displayed and should look similar to the following:</span></span>

``` syntax
Connection: Keep-Alive
Content-Length: 0
Date: Fri, 27 Apr 2001 01:47:18 GMT
Content-Type: text/html
Server: Microsoft-IIS/5.0
WWW-Authenticate: NTLM
WWW-Authenticate: Negotiate
Cache-control: private
```

<span data-ttu-id="be190-125">Embora a resposta indique que o acesso ao recurso foi negado, ele ainda retorna vários cabeçalhos que fornecem algumas informações sobre o recurso.</span><span class="sxs-lookup"><span data-stu-id="be190-125">Although the response indicates that access to the resource was denied, it still returns several headers that provide some information about the resource.</span></span> <span data-ttu-id="be190-126">O cabeçalho chamado "WWW-Authenticate" indica que o servidor requer autenticação para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="be190-126">The header named "WWW-Authenticate" indicates that the server requires authentication for this resource.</span></span> <span data-ttu-id="be190-127">Se houvesse um cabeçalho chamado "proxy-Authenticate", ele indicaria que o servidor proxy requer autenticação.</span><span class="sxs-lookup"><span data-stu-id="be190-127">If there was a header named "Proxy-Authenticate", it would indicate that the proxy server requires authentication.</span></span> <span data-ttu-id="be190-128">Cada cabeçalho Authenticate contém um esquema de autenticação disponível e, às vezes, um realm.</span><span class="sxs-lookup"><span data-stu-id="be190-128">Each authenticate header contains an available authentication scheme and sometimes a realm.</span></span> <span data-ttu-id="be190-129">O valor do Realm diferenciam maiúsculas de minúsculas e definem um conjunto de servidores ou proxies para os quais as mesmas credenciais devem ser aceitas.</span><span class="sxs-lookup"><span data-stu-id="be190-129">The realm value is case-sensitive and defines a set of servers or proxies for which the same credentials should be accepted.</span></span>

<span data-ttu-id="be190-130">Há dois cabeçalhos chamados "WWW-Authenticate", que indicam que há suporte para vários esquemas de autenticação.</span><span class="sxs-lookup"><span data-stu-id="be190-130">There are two headers named "WWW-Authenticate", which indicate that multiple authentication schemes are supported.</span></span> <span data-ttu-id="be190-131">Se você chamar o método [**getResponseHeader**](iwinhttprequest-getresponseheader.md) para localizar cabeçalhos "www-Authenticate", o método retornará apenas o conteúdo do primeiro cabeçalho desse nome.</span><span class="sxs-lookup"><span data-stu-id="be190-131">If you call the [**GetResponseHeader**](iwinhttprequest-getresponseheader.md) method to find "WWW-Authenticate" headers, the method only returns the contents of the first header of that name.</span></span> <span data-ttu-id="be190-132">Nesse caso, ele retorna um valor de "NTLM".</span><span class="sxs-lookup"><span data-stu-id="be190-132">In this case, it returns a value of "NTLM".</span></span> <span data-ttu-id="be190-133">Para garantir que todas as ocorrências de um cabeçalho sejam processadas, use o método [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="be190-133">To ensure that all occurrences of a header are processed, use the [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) method instead.</span></span>

<span data-ttu-id="be190-134">A segunda chamada de método solicita o mesmo recurso, mas primeiro fornece as credenciais de autenticação chamando o método [**SetCredentials**](iwinhttprequest-setcredentials.md) .</span><span class="sxs-lookup"><span data-stu-id="be190-134">The second method call requests the same resource, but first supplies authentication credentials by calling the [**SetCredentials**](iwinhttprequest-setcredentials.md) method.</span></span> <span data-ttu-id="be190-135">A seção de código a seguir mostra como esse método é usado.</span><span class="sxs-lookup"><span data-stu-id="be190-135">The following section of code shows how this method is used.</span></span>


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



<span data-ttu-id="be190-136">Esse método define o nome de usuário como "UserName", a senha como "password" e indica que as credenciais de autorização se aplicam ao servidor de recursos.</span><span class="sxs-lookup"><span data-stu-id="be190-136">This method sets the user name to "UserName", the password to "Password", and indicates that the authorization credentials apply to the resource server.</span></span> <span data-ttu-id="be190-137">As credenciais de autenticação também podem ser enviadas a um proxy.</span><span class="sxs-lookup"><span data-stu-id="be190-137">Authentication credentials can also be sent to a proxy.</span></span>

<span data-ttu-id="be190-138">Quando as credenciais são fornecidas, o servidor retorna um código de status 200 que indica que o documento pode ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="be190-138">When credentials are supplied, the server returns a 200 status code that indicates that the document can be retrieved.</span></span>

## <a name="checking-the-status-codes"></a><span data-ttu-id="be190-139">Verificando os códigos de status</span><span class="sxs-lookup"><span data-stu-id="be190-139">Checking the Status Codes</span></span>

<span data-ttu-id="be190-140">O exemplo anterior é instrutivo, mas requer que o usuário forneça explicitamente as credenciais.</span><span class="sxs-lookup"><span data-stu-id="be190-140">The previous example is instructional, but it requires that the user explicitly supply credentials.</span></span> <span data-ttu-id="be190-141">Um aplicativo que fornece credenciais quando necessário e não fornece credenciais quando não é necessário é mais útil.</span><span class="sxs-lookup"><span data-stu-id="be190-141">An application that supplies credentials when it is necessary and does not supply credentials when it is not necessary is more useful.</span></span> <span data-ttu-id="be190-142">Para implementar um recurso que faz isso, você deve modificar seu exemplo para examinar o código de status retornado com a resposta.</span><span class="sxs-lookup"><span data-stu-id="be190-142">To implement a feature that does this, you must modify your example to examine the status code returned with the response.</span></span>

<span data-ttu-id="be190-143">Para obter uma lista completa de códigos de status possíveis, juntamente com descrições, consulte [**códigos de status http**](http-status-codes.md).</span><span class="sxs-lookup"><span data-stu-id="be190-143">For a complete list of possible status codes, along with descriptions, see [**HTTP Status Codes**](http-status-codes.md).</span></span> <span data-ttu-id="be190-144">Neste exemplo, no entanto, você deve encontrar apenas um dos três códigos.</span><span class="sxs-lookup"><span data-stu-id="be190-144">For this example, however, you should encounter only one of three codes.</span></span> <span data-ttu-id="be190-145">Um código de status 200 indica que um recurso está disponível e está sendo enviado com a resposta.</span><span class="sxs-lookup"><span data-stu-id="be190-145">A status code of 200 indicates that a resource is available and is being sent with the response.</span></span> <span data-ttu-id="be190-146">Um código de status 401 indica que o servidor requer autenticação.</span><span class="sxs-lookup"><span data-stu-id="be190-146">A status code of 401 indicates that the server requires authentication.</span></span> <span data-ttu-id="be190-147">Um código de status 407 indica que o proxy requer autenticação.</span><span class="sxs-lookup"><span data-stu-id="be190-147">A status code of 407 indicates that the proxy requires authentication.</span></span>

<span data-ttu-id="be190-148">Modifique o exemplo criado na última seção, substituindo a função "getText2" pelo código a seguir (substitua " \[ authenticationSite \] " pelo seu próprio texto para especificar a URL de um site que requer autenticação http):</span><span class="sxs-lookup"><span data-stu-id="be190-148">Modify the example you created in the last section by replacing the "getText2" function with the following code (replace "\[authenticationSite\]" with your own text to specifies the URL of a site that requires HTTP authentication):</span></span>


```VB
function getText2() {
  WScript.Echo( "Credentials: " );

  // HttpRequest SetCredentials flags.
  HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
  HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

  // Specify the target resource.
  var targURL = "https://[authenticationSite]";
  WinHttpReq.open( "GET", targURL, false );

  var Done = false;
  var Attempts = 0;
  do
  {
    // Keep track of the number of request attempts.
    Attempts++;

    // Send a request to the server and wait for a response.
    WinHttpReq.send( );

    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status)
    {
      // A 200 status indicates that the resource was retrieved.
      case 200:
        Done = true;
        break;

      // A 401 status indicates that the server 
      // requires authentication.
      case 401:
        WScript.Echo( "Requires Server UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the server.
        WinHttpReq.SetCredentials( "User Name", 
                             "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        break;

      // A 407 status indicates that the proxy 
      // requires authentication.
      case 407:
        WScript.Echo( "Requires Proxy UserName and Password." );

        // Specify the target resource.
        WinHttpReq.open( "GET", targURL, false );

        // Set credentials for the proxy.
        WinHttpReq.SetCredentials( "User Name", 
                              "Password",
                              HTTPREQUEST_SETCREDENTIALS_FOR_PROXY );
        break;
    }
  } while( ( !Done ) && ( Attempts < 3 ) );

  // Display the results of the request.
  WScript.Echo( WinHttpReq.Status + "   " + WinHttpReq.StatusText );
  WScript.Echo( WinHttpReq.GetAllResponseHeaders( ) );
  WScript.Echo( );
};
```



<span data-ttu-id="be190-149">Novamente, salve e execute o arquivo.</span><span class="sxs-lookup"><span data-stu-id="be190-149">Again, save and run the file.</span></span> <span data-ttu-id="be190-150">O segundo método ainda recupera o documento, mas só fornece credenciais quando necessário.</span><span class="sxs-lookup"><span data-stu-id="be190-150">The second method still retrieves the document, but it only provides credentials when required.</span></span> <span data-ttu-id="be190-151">A função "getText2" executa os métodos [**Open**](iwinhttprequest-open.md) e [**Send**](iwinhttprequest-send.md) como se a autenticação não fosse necessária.</span><span class="sxs-lookup"><span data-stu-id="be190-151">The "getText2" function executes the [**Open**](iwinhttprequest-open.md) and [**Send**](iwinhttprequest-send.md) methods as if authentication was not required.</span></span> <span data-ttu-id="be190-152">O status é recuperado com a propriedade [**status**](iwinhttprequest-status.md) e uma instrução switch responde ao código de status resultante.</span><span class="sxs-lookup"><span data-stu-id="be190-152">The status is retrieved with the [**Status**](iwinhttprequest-status.md) property and a switch statement responds to the resulting status code.</span></span> <span data-ttu-id="be190-153">Se o status for 401 (servidor requer autenticação) ou 407 (o proxy requer autenticação), o método [**Open**](iwinhttprequest-open.md) será executado novamente.</span><span class="sxs-lookup"><span data-stu-id="be190-153">If the status is 401 (server requires authentication) or 407 (proxy requires authentication), the [**Open**](iwinhttprequest-open.md) method is executed again.</span></span> <span data-ttu-id="be190-154">Isso é seguido pelo método [**SetCredentials**](iwinhttprequest-setcredentials.md) , que define o nome de usuário e a senha.</span><span class="sxs-lookup"><span data-stu-id="be190-154">This is followed by the [**SetCredentials**](iwinhttprequest-setcredentials.md) method, which sets the user name and password.</span></span> <span data-ttu-id="be190-155">Em seguida, o código executa um loop de volta para o método [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="be190-155">The code then loops back to the [**Send**](iwinhttprequest-send.md) method.</span></span> <span data-ttu-id="be190-156">Se, após três tentativas, o recurso não puder ser recuperado com êxito, a função interromperá a execução.</span><span class="sxs-lookup"><span data-stu-id="be190-156">If, after three attempts, the resource cannot be successfully retrieved, then the function stops execution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be190-157">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="be190-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be190-158">Autenticação no WinHTTP</span><span class="sxs-lookup"><span data-stu-id="be190-158">Authentication in WinHTTP</span></span>](authentication-in-winhttp.md)
</dt> <dt>

[<span data-ttu-id="be190-159">WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="be190-159">WinHttpRequest</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="be190-160">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="be190-160">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)
</dt> <dt>

[<span data-ttu-id="be190-161">Solicitação de comentários de HTTP/1.1 (RFC 2616)</span><span class="sxs-lookup"><span data-stu-id="be190-161">HTTP/1.1 Request for Comments (RFC 2616)</span></span>](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



