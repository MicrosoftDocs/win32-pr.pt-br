---
description: O Microsoft Windows Http Services (WinHTTP) expõe um conjunto de funções C/C++ que permitem que seu aplicativo acesse recursos HTTP na Web. Este tópico fornece uma visão geral de como essas funções são usadas para interagir com um servidor HTTP.
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: Visão geral das sessões do WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753f7c2a3845b34ac306c1fb8d87441955ab9f4cfe0e1ea250737f62f993cd43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743896"
---
# <a name="winhttp-sessions-overview"></a>Visão geral das sessões do WinHTTP

O Microsoft Windows Http Services (WinHTTP) expõe um conjunto de funções C/C++ que permitem que seu aplicativo acesse recursos HTTP na Web. Este tópico fornece uma visão geral de como essas funções são usadas para interagir com um servidor HTTP.

-   [Usando a API WinHTTP para acessar a Web](#using-the-winhttp-api-to-access-the-web)
-   [Inicializando WinHTTP](#initializing-winhttp)
-   [Abrindo uma solicitação](#opening-a-request)
-   [Adicionando os headers de solicitação](#adding-request-headers)
-   [Enviando uma solicitação](#sending-a-request)
-   [Postando dados no servidor](#posting-data-to-the-server)
-   [Obter informações sobre uma solicitação](#getting-information-about-a-request)
-   [Baixando recursos da Web](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a>Usando a API WinHTTP para acessar a Web

O diagrama a seguir mostra a ordem na qual as funções WinHTTP normalmente são chamadas ao interagir com um servidor HTTP. As caixas sombreadas representam funções que geram um alça [HINTERNET,](hinternet-handles-in-winhttp.md) enquanto as caixas simples representam funções que usam esses alças.

![funções que criam alças](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a>Inicializando WinHTTP

Antes de interagir com um servidor, o WinHTTP deve ser inicializado chamando [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen). [**WinHttpOpen cria**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) um contexto de sessão para manter detalhes sobre a sessão HTTP e retorna um handle de sessão. Usando esse handle, a [**função WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) é capaz de especificar um servidor HTTP de destino ou HTTPS (Secure Hypertext Transfer Protocol).

> [!Note]  
> Uma chamada para [**WinHttpConnect não**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) resulta em uma conexão real com o servidor HTTP até que uma solicitação seja feita para um recurso específico.

 

## <a name="opening-a-request"></a>Abrindo uma solicitação

A [**função WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) abre uma solicitação HTTP para um recurso específico e retorna um handle [HINTERNET](hinternet-handles-in-winhttp.md) que pode ser usado pelas outras funções HTTP. [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) não envia a solicitação ao servidor quando chamado. A [**função WinHttpSendRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) na verdade, estabelece uma conexão pela rede e envia a solicitação.

O exemplo a seguir mostra uma chamada de exemplo [**para WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) que usa as opções padrão.

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a>Adicionando os headers de solicitação

A [**função WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) permite que um aplicativo adeque cabeçalhos de solicitação de formato livre adicionais ao alça de solicitação HTTP. Ele destina-se ao uso por aplicativos sofisticados que exigem controle preciso sobre as solicitações enviadas ao servidor HTTP.

A [**função WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) requer um handle de solicitação HTTP criado por [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), uma cadeia de caracteres que contém os cabeçalhos, o comprimento dos cabeçalhos e quaisquer modificadores.

Os modificadores a seguir podem ser usados [**com WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).



| Modificador                                                                                         | Descrição                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ADICIONAR SINALIZADOR \_ WINHTTPREQ \_ \_**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | Adiciona o header se ele não existir. Usado com [**WINHTTP \_ ADDREQ \_ FLAG \_ REPLACE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).                                                                                                                                                                                                               |
| [**WINHTTP \_ ADDREQ \_ FLAG \_ ADD \_ IF \_ NEW**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | Adiciona o header somente se ele ainda não existir; caso contrário, um erro será retornado.                                                                                                                                                                                                                                                           |
| [**COALESCE DO SINALIZADOR WINHTTP \_ ADDREQ \_ \_**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | Mescla os headers de mesmo nome.                                                                                                                                                                                                                                                                                                              |
| [**WINHTTP \_ ADDREQ \_ FLAG \_ COALESCE \_ WITH \_ VÍRGULA**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | Mescla os headers do mesmo nome usando uma vírgula. Por exemplo, adicionar "Accept: text/ " seguido por "Accept: audio/ " com esse sinalizador forma o único \* \* header "Accept: text/ , audio/ ", fazendo com que o primeiro header seja \* \* mesclado. Cabe ao aplicativo de chamada garantir um esquema coeso em relação aos títulos mesclados/separados. |
| [**SINALIZADOR WINHTTP \_ ADDREQ \_ \_ COALESCE \_ COM PONTO E \_ VÍRGULA**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | Mescla os headers do mesmo nome usando um ponto e vírgula.                                                                                                                                                                                                                                                                                            |
| [**WINHTTP \_ ADDREQ \_ FLAG \_ REPLACE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | Substitui ou remove um header. Se o valor do header estiver vazio e o header for encontrado, ele será removido. Se o valor do header não estiver vazio, o valor do header será substituído.                                                                                                                                                                            |



 

## <a name="sending-a-request"></a>Enviando uma solicitação

A [**função WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) estabelece uma conexão com o servidor e envia a solicitação para o site especificado. Essa função requer um [alça HINTERNET](hinternet-handles-in-winhttp.md) criado [**por WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) também pode enviar outros títulos ou informações opcionais. As informações opcionais geralmente são usadas para operações que escrevem informações no servidor, como PUT e POST.

Depois que a [**função WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) envia a solicitação, o aplicativo pode usar as funções [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) e [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) no handle [HINTERNET](hinternet-handles-in-winhttp.md) para baixar os recursos do servidor.

## <a name="posting-data-to-the-server"></a>Postando dados no servidor

Para postar dados em um servidor, o [*verbo HTTP*](glossary.md) na chamada para [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) deve ser POST ou PUT. Quando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) é chamado, o parâmetro *dwTotalLength* deve ser definido como o tamanho dos dados em bytes. Em seguida, [**use WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) para postar os dados no servidor.

Como alternativa, defina *o parâmetro lpOptional* [**de WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) como o endereço de um buffer que contém dados para postar no servidor. Ao usar essa técnica, você deve definir os parâmetros *dwOptionalLength* e *dwTotalLength* de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) como sendo o tamanho dos dados que estão sendo postados. Chamar [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) dessa maneira elimina a necessidade de [**chamar WinHttpWriteData.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)

## <a name="getting-information-about-a-request"></a>Obter informações sobre uma solicitação

A [**função WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) permite que um aplicativo recupere informações sobre uma solicitação HTTP. A função requer um alça [HINTERNET](hinternet-handles-in-winhttp.md) criado por [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), um valor de nível de informação e um comprimento de buffer. [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) também aceita um buffer que armazena as informações e um índice de título baseado em zero que enumera vários headers com o mesmo nome.

Use qualquer um dos valores de nível de informações encontrados na página Sinalizadores de Informações de Consulta com um modificador para controlar o formato no qual as informações são [**armazenadas**](query-info-flags.md) no parâmetro *lpvBuffer* [**de WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).

## <a name="downloading-resources-from-the-web"></a>Baixando recursos da Web

Depois de abrir uma solicitação com a função [**WinHttpOpenRequest,**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) enviá-la ao servidor com [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)e preparar o handle de solicitação para receber uma resposta com [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), o aplicativo pode usar as funções [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) e [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) para baixar o recurso do servidor HTTP.

O código de exemplo a seguir mostra como baixar um recurso com semântica de transação segura. O código de exemplo inicializa a API (interface de programação de aplicativo) WinHTTP, seleciona um servidor HTTPS de destino e, em seguida, abre e envia uma solicitação para esse recurso seguro. [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) é usado com o handle de solicitação para determinar quantos dados estão disponíveis para download e, em seguida, [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) é usado para ler esses dados. Esse processo é repetido até que todo o documento seja recuperado e exibido.


```C++
  DWORD dwSize = 0;
  DWORD dwDownloaded = 0;
  LPSTR pszOutBuffer;
  BOOL  bResults = FALSE;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTPS_PORT, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                   NULL, WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                   WINHTTP_FLAG_SECURE );

  // Send a request.
  if( hRequest )
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS, 0,
                                   WINHTTP_NO_REQUEST_DATA, 0, 
                                   0, 0 );


  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL );

  // Keep checking for data until there is nothing left.
  if( bResults )
  {
    do 
    {
      // Check for available data.
      dwSize = 0;
      if( !WinHttpQueryDataAvailable( hRequest, &dwSize ) )
        printf( "Error %u in WinHttpQueryDataAvailable.\n",
                GetLastError( ) );

      // Allocate space for the buffer.
      pszOutBuffer = new char[dwSize+1];
      if( !pszOutBuffer )
      {
        printf( "Out of memory\n" );
        dwSize=0;
      }
      else
      {
        // Read the data.
        ZeroMemory( pszOutBuffer, dwSize+1 );

        if( !WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                              dwSize, &dwDownloaded ) )
          printf( "Error %u in WinHttpReadData.\n", GetLastError( ) );
        else
          printf( "%s", pszOutBuffer );

        // Free the memory allocated to the buffer.
        delete [] pszOutBuffer;
      }
    } while( dwSize > 0 );
  }


  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
```



 

 



