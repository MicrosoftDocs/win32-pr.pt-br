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
ms.openlocfilehash: 81e2dec50ccf765239bbbd1d6a71c8f8fb2be0e4f70f2db5717b0072f0b62d6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052094"
---
# <a name="authentication-using-script"></a>Autenticação usando script

Esta seção demonstra como escrever um script que usa o objeto [**WinHttpRequest**](winhttprequest.md) para acessar dados de um servidor que requer autenticação http.

-   [Pré-requisitos e requisitos](#prerequisites-and-requirements)
-   [Acessando um site com autenticação](#accessing-a-web-site-with-authentication)
-   [Verificando os códigos de status](#checking-the-status-codes)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites-and-requirements"></a>Pré-requisitos e requisitos

além de um conhecimento prático do Microsoft JScript, este exemplo requer o seguinte:

-   a versão atual do Microsoft Windows Software Development Kit (SDK).
-   a ferramenta de configuração de proxy para estabelecer as configurações de proxy para o Microsoft Windows HTTP Services (WinHTTP), se a conexão com a Internet for por meio de um servidor proxy. Consulte [Proxycfg.exe, uma ferramenta de configuração de proxy](proxycfg-exe--a-proxy-configuration-tool.md) para obter mais informações.
-   Familiaridade com a [terminologia](network-terminology.md) e os conceitos de rede.

## <a name="accessing-a-web-site-with-authentication"></a>Acessando um site com autenticação

**Para criar um script que demonstre a autenticação, faça o seguinte:**

1.  abra um editor de texto como o Microsoft Bloco de notas.
2.  Copie o código a seguir no editor de texto depois de substituir " \[ authenticationSite \] " pelo texto apropriado para especificar a URL de um site que requer autenticação http.

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

    

3.  Salve o arquivo como "Auth.js".
4.  Em um prompt de comando, digite "cscript Auth.js" e pressione ENTER.

Agora você tem um programa que solicita um recurso de duas maneiras diferentes. O primeiro método solicita o recurso sem fornecer credenciais. Um código de status 401 é retornado para indicar que o servidor requer autenticação. Os cabeçalhos de resposta também são exibidos e devem ser semelhantes ao seguinte:

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

Embora a resposta indique que o acesso ao recurso foi negado, ele ainda retorna vários cabeçalhos que fornecem algumas informações sobre o recurso. O cabeçalho chamado "WWW-Authenticate" indica que o servidor requer autenticação para esse recurso. Se houvesse um cabeçalho chamado "proxy-Authenticate", ele indicaria que o servidor proxy requer autenticação. Cada cabeçalho Authenticate contém um esquema de autenticação disponível e, às vezes, um realm. O valor do Realm diferenciam maiúsculas de minúsculas e definem um conjunto de servidores ou proxies para os quais as mesmas credenciais devem ser aceitas.

Há dois cabeçalhos chamados "WWW-Authenticate", que indicam que há suporte para vários esquemas de autenticação. Se você chamar o método [**getResponseHeader**](iwinhttprequest-getresponseheader.md) para localizar cabeçalhos "www-Authenticate", o método retornará apenas o conteúdo do primeiro cabeçalho desse nome. Nesse caso, ele retorna um valor de "NTLM". Para garantir que todas as ocorrências de um cabeçalho sejam processadas, use o método [**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md) em vez disso.

A segunda chamada de método solicita o mesmo recurso, mas primeiro fornece as credenciais de autenticação chamando o método [**SetCredentials**](iwinhttprequest-setcredentials.md) . A seção de código a seguir mostra como esse método é usado.


```VB
WinHttpReq.SetCredentials( "User Name", "Password",
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
```



Esse método define o nome de usuário como "UserName", a senha como "password" e indica que as credenciais de autorização se aplicam ao servidor de recursos. As credenciais de autenticação também podem ser enviadas a um proxy.

Quando as credenciais são fornecidas, o servidor retorna um código de status 200 que indica que o documento pode ser recuperado.

## <a name="checking-the-status-codes"></a>Verificando os códigos de status

O exemplo anterior é instrutivo, mas requer que o usuário forneça explicitamente as credenciais. Um aplicativo que fornece credenciais quando necessário e não fornece credenciais quando não é necessário é mais útil. Para implementar um recurso que faz isso, você deve modificar seu exemplo para examinar o código de status retornado com a resposta.

Para obter uma lista completa de códigos de status possíveis, juntamente com descrições, consulte [**códigos de status http**](http-status-codes.md). Neste exemplo, no entanto, você deve encontrar apenas um dos três códigos. Um código de status 200 indica que um recurso está disponível e está sendo enviado com a resposta. Um código de status 401 indica que o servidor requer autenticação. Um código de status 407 indica que o proxy requer autenticação.

Modifique o exemplo criado na última seção, substituindo a função "getText2" pelo código a seguir (substitua " \[ authenticationSite \] " pelo seu próprio texto para especificar a URL de um site que requer autenticação http):


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



Novamente, salve e execute o arquivo. O segundo método ainda recupera o documento, mas só fornece credenciais quando necessário. A função "getText2" executa os métodos [**Open**](iwinhttprequest-open.md) e [**Send**](iwinhttprequest-send.md) como se a autenticação não fosse necessária. O status é recuperado com a propriedade [**status**](iwinhttprequest-status.md) e uma instrução switch responde ao código de status resultante. Se o status for 401 (servidor requer autenticação) ou 407 (o proxy requer autenticação), o método [**Open**](iwinhttprequest-open.md) será executado novamente. Isso é seguido pelo método [**SetCredentials**](iwinhttprequest-setcredentials.md) , que define o nome de usuário e a senha. Em seguida, o código executa um loop de volta para o método [**Send**](iwinhttprequest-send.md) . Se, após três tentativas, o recurso não puder ser recuperado com êxito, a função interromperá a execução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Autenticação no WinHTTP](authentication-in-winhttp.md)
</dt> <dt>

[WinHttpRequest](winhttprequest.md)
</dt> <dt>

[**SetCredentials**](iwinhttprequest-setcredentials.md)
</dt> <dt>

[Solicitação de comentários de HTTP/1.1 (RFC 2616)](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



