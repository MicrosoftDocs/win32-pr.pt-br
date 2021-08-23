---
description: Alguns servidores HTTP e proxies exigem autenticação antes de permitir o acesso aos recursos na Internet. As funções do Microsoft Windows HTTP Services (WinHTTP) são suporte à autenticação de servidor e proxy para sessões HTTP.
ms.assetid: 077d6275-8600-4091-b78e-419a41a2101a
title: Autenticação no WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 810fadf470861b23ed2291bfa5665e1e429e86b7be77675f332267ee1d1c4de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052114"
---
# <a name="authentication-in-winhttp"></a>Autenticação no WinHTTP

Alguns servidores HTTP e proxies exigem autenticação antes de permitir o acesso aos recursos na Internet. As funções do Microsoft Windows HTTP Services (WinHTTP) são suporte à autenticação de servidor e proxy para sessões HTTP.

## <a name="about-http-authentication"></a>Sobre a autenticação HTTP

Se a autenticação for necessária, o aplicativo HTTP receberá um código de status 401 (o servidor requer autenticação) ou 407 (o proxy requer autenticação). Juntamente com o código de status, o proxy ou servidor envia um ou mais headers de autenticação: WWW-Authenticate (para autenticação de servidor) ou Proxy-Authenticate (para autenticação de proxy).

Cada header de autenticação contém um esquema de autenticação com suporte e, para os esquemas Básico e Digest, um realm. Se vários esquemas de autenticação são suportados, o servidor retorna vários headers de autenticação. O valor de realm é sensível a minúsculas e define um conjunto de servidores ou proxies para os quais as mesmas credenciais são aceitas. Por exemplo, o header "WWW-Authenticate: Basic Realm="example"" pode ser retornado quando a autenticação do servidor é necessária. Esse header especifica que as credenciais do usuário devem ser fornecidas para o domínio de "exemplo".

Um aplicativo HTTP pode incluir um campo de cabeçalho de autorização com uma solicitação que ele envia ao servidor. O header de autorização contém o esquema de autenticação e a resposta apropriada exigida por esse esquema. Por exemplo, o header "Authorization: Basic" seria adicionado à solicitação e enviado ao servidor se o cliente recebesse o header de resposta \<username:password> "WWW-Authenticate: Basic Realm="example"".

> [!Note]  
> Embora eles sejam mostrados aqui como texto sem-texto, o nome de usuário e a senha são, na verdade, [*codificados em base64.*](glossary.md)

 

Há dois tipos gerais de esquemas de autenticação:

-   Esquema de autenticação básico, no qual o nome de usuário e a senha são enviados em texto não claro para o servidor.

    O esquema de autenticação Básico baseia-se no modelo em que um cliente deve se identificar com um nome de usuário e senha para cada realm. O servidor só será responsável pela solicitação se a solicitação for enviada com um header de autorização que inclua um nome de usuário e uma senha válidos.

-   Esquemas de desafio-resposta, como Kerberos, em que o servidor desafiou o cliente com dados [*de autenticação*](glossary.md). O cliente transforma os dados com as credenciais do usuário e envia os dados transformados de volta para o servidor para autenticação.

    Os esquemas de desafio-resposta permitem uma autenticação mais segura. Em um esquema de desafio-resposta, o nome de usuário e a senha nunca são transmitidos pela rede. Depois que o cliente seleciona um esquema de desafio-resposta, o servidor retorna um código de status apropriado com um desafio que contém os dados de [*autenticação*](glossary.md) para esse esquema. Em seguida, o cliente reende a solicitação com a resposta adequada para obter o serviço solicitado. Esquemas de desafio-resposta podem levar várias trocas para ser concluídas.

A tabela a seguir contém os esquemas de autenticação com suporte pelo WinHTTP, o tipo de autenticação e uma descrição do esquema.



| Esquema            | Tipo               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Básico (texto não criptografado) | Basic              | Usa uma cadeia [*de caracteres codificada em base64*](glossary.md) que contém o nome de usuário e a senha.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Digest            | Desafio-resposta | Desafios ao usar um valor nonce (uma cadeia de caracteres de dados especificada pelo servidor). Uma resposta válida contém uma verificação do nome de usuário, a senha, o valor nonce fornecido, o [*verbo HTTP*](glossary.md)e o URI (Uniform Resource Identifier) solicitados.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| NTLM              | Desafio-resposta | Exige que [*os dados de autenticação*](glossary.md) sejam transformados com as credenciais do usuário para provar a identidade. Para que a autenticação NTLM funcione corretamente, várias trocas devem ocorrer na mesma conexão. Portanto, a autenticação NTLM não pode ser usada se um proxy intermediário não dá suporte a conexões keep alive. A autenticação NTLM também falhará se [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) for usado com o sinalizador [**WINHTTP \_ DISABLE KEEP \_ \_ ALIVE**](option-flags.md) que desabilita a semântica keep alive.                                                                                                                                                                                                                                       |
| Passport          | Desafio-resposta | Usa [Microsoft Passport 1.4](passport-authentication-in-winhttp.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Negotiate         | Desafio-resposta | Se o servidor e o cliente estão usando Windows 2000 ou posterior, a autenticação Kerberos será usada. Caso contrário, a autenticação NTLM será usada. O Kerberos está disponível no Windows 2000 e sistemas operacionais posteriores e é considerado mais seguro do que a autenticação NTLM. Para que a autenticação Negotiate funcione corretamente, várias trocas devem ocorrer na mesma conexão. Portanto, a autenticação Negotiate não pode ser usada se um proxy intermediário não dá suporte a conexões keep alive. A autenticação negotiate também [**falhará se WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) for usado com o sinalizador [**WINHTTP \_ DISABLE KEEP \_ \_ ALIVE**](option-flags.md) que desabilita a semântica keep alive. Às vezes, o esquema de autenticação Negotiate é chamado Windows autenticação integrada. |



 

## <a name="authentication-in-winhttp-applications"></a>Autenticação em aplicativos WinHTTP

A API (interface de programação de aplicativo) WinHTTP fornece duas funções usadas para acessar recursos da Internet em situações em que a autenticação é necessária: [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) e [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes).

Quando uma resposta é recebida com um código de status 401 ou 407, [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) pode ser usado para analisar os headers de autenticação para determinar os esquemas de autenticação com suporte e o destino de autenticação. O destino de autenticação é o servidor ou proxy que solicita autenticação. **WinHttpQueryAuthSchemes** também determina o primeiro esquema de autenticação, dos esquemas disponíveis, com base nas preferências de esquema de autenticação sugeridas pelo servidor. Esse método para escolher um esquema de autenticação é o comportamento sugerido [pelo RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).

[**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) permite que um aplicativo especifique o esquema de autenticação usado juntamente com um nome de usuário e senha válidos para uso no servidor ou proxy de destino. Depois de definir as credenciais e reenderar a solicitação, os headers necessários são gerados e adicionados à solicitação automaticamente. Como alguns esquemas de autenticação exigem várias [**transações, WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) pode retornar o erro, ERROR \_ WINHTTP \_ RESEND \_ REQUEST. Quando esse erro for encontrado, o aplicativo deverá continuar a reenviar a solicitação até que uma resposta seja recebida que não contenha um código de status 401 ou 407. Um código de status 200 indica que o recurso está disponível e a solicitação foi bem-sucedida. Consulte [**Códigos de status HTTP**](http-status-codes.md) para obter códigos de status adicionais que podem ser retornados.

Se um esquema de autenticação aceitável e credenciais são conhecidas antes de uma solicitação ser enviada ao servidor, um aplicativo pode chamar [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) antes de chamar [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Nesse caso, o WinHTTP tenta a pré-autenticação [](glossary.md) com o servidor fornecendo credenciais ou dados de autenticação na solicitação inicial para o servidor. A pré-autenticação pode diminuir o número de trocas no processo de autenticação e, portanto, melhorar o desempenho do aplicativo.

A pré-autenticação pode ser usada com os seguintes esquemas de autenticação:

-   Básico – sempre possível.
-   Negociar a resolução no Kerberos – muito provavelmente possível; a única exceção é quando as distorções de tempo estão desligadas entre o cliente e o controlador de domínio.
-   (Negociar a resolução no NTLM) – nunca é possível.
-   NTLM – possível somente Windows Server 2008 R2.
-   Resumo – nunca é possível.
-   Passport – nunca é possível; após a resposta-desafio inicial, o WinHTTP usa cookies para pré-autenticar no Passport.

Um aplicativo WinHTTP típico conclui as etapas a seguir para lidar com a autenticação.

-   Solicite um recurso [**com WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) [**e WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
-   Verifique os títulos de resposta [**com WinHttpQueryHeaders.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
-   Se um código de status 401 ou 407 for retornado indicando que a autenticação é necessária, chame [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes) para encontrar um esquema aceitável.
-   De definir o esquema de autenticação, o nome de usuário e a senha [**com WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials).
-   Reenda a solicitação com o mesmo handle de solicitação chamando [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)

As credenciais definidas por [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) são usadas apenas para uma solicitação. O WinHTTP não armazena em cache as credenciais a serem usadas em outras solicitações, o que significa que os aplicativos devem ser gravados que podem responder a várias solicitações. Se uma conexão autenticada for rea usada, outras solicitações poderão não ser desafiadas, mas seu código deverá ser capaz de responder a uma solicitação a qualquer momento.

### <a name="example-retrieving-a-document"></a>Exemplo: Recuperando um documento

O código de exemplo a seguir tenta recuperar um documento especificado de um servidor HTTP. O código de status é recuperado da resposta para determinar se a autenticação é necessária. Se um código de status 200 for encontrado, o documento estará disponível. Se um código de status 401 ou 407 for encontrado, a autenticação será necessária antes que o documento possa ser recuperado. Para qualquer outro código de status, uma mensagem de erro é exibida. Consulte [**Códigos de status HTTP**](http-status-codes.md) para ver uma lista de códigos de status possíveis.


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



## <a name="automatic-logon-policy"></a>Política de logon automático

A política de logon automático (logon automático) determina quando é aceitável que o WinHTTP inclua as credenciais padrão em uma solicitação. As credenciais padrão são o token de thread atual ou o token de sessão, dependendo se o WinHTTP é usado no modo síncrono ou assíncrono. O token de thread é usado no modo síncrono e o token de sessão é usado no modo assíncrono. Essas credenciais padrão geralmente são o nome de usuário e a senha usados para fazer logon no Microsoft Windows.

A política de logon automático foi implementada para impedir que essas credenciais sejam usadas casualmente para autenticar em um servidor não confiável. Por padrão, o nível de segurança é definido para o nível de segurança do WINHTTP com \_ logon automático \_ \_ \_ médio, que permite que as credenciais padrão sejam usadas somente para solicitações de intranet. A política de logon automático só se aplica aos esquemas de autenticação NTLM e negociar. As credenciais nunca são transmitidas automaticamente com outros esquemas.

A política de logon automático pode ser definida usando a função [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) com a [**opção WinHTTP sinalizador de \_ \_ \_ política de autologoização**](option-flags.md) . Esse sinalizador se aplica somente ao identificador de solicitação. Quando a política é definida como WINHTTP \_ , o nível de segurança de logon automático é \_ \_ \_ baixo, as credenciais padrão podem ser enviadas para todos os servidores. Quando a política é definida para o \_ nível de segurança do WinHTTP AUTOlogon \_ \_ \_ alto, as credenciais padrão não podem ser usadas para autenticação. É altamente recomendável que você use o logon automático no nível médio.

## <a name="stored-user-names-and-passwords"></a>Nomes de usuário e senhas armazenados

Windows O XP introduziu o conceito de nomes de usuário e senhas armazenados. Se as credenciais do Passport de um usuário forem salvas por meio do **Assistente de registro do Passport** ou da caixa de **diálogo credencial** padrão, ela será salva nos nomes de usuário e senhas armazenados. ao usar o WinHTTP no Windows XP ou posterior, o WinHTTP usará automaticamente as credenciais nos nomes de usuário e senhas armazenados se as credenciais não estiverem definidas explicitamente. Isso é semelhante ao suporte de credenciais de logon padrão para NTLM/Kerberos. No entanto, o uso de credenciais padrão do Passport não está sujeito às configurações de política de logon automático.

 

 



