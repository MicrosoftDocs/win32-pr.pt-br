---
description: O WinHTTP implementa o protocolo WPAD usando a função WinHttpGetProxyForUrl juntamente com duas funções de utilitário de suporte, WinHttpDetectAutoProxyConfigUrl e WinHttpGetIEProxyConfigForCurrentUser.
ms.assetid: d941e3c6-c1db-4de1-b640-4f582f86fc54
title: Funções de AutoProxy do WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8443567e12d7a0f3b75d09fc284dc634315ec635ff8b630821bb84031e39781b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955706"
---
# <a name="winhttp-autoproxy-functions"></a>Funções de AutoProxy do WinHTTP

O WinHTTP implementa o protocolo WPAD usando a função [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) juntamente com duas funções de utilitário de suporte, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) e [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).

O suporte a AutoProxy não está totalmente integrado à pilha HTTP no WinHTTP. Antes de enviar uma solicitação, o aplicativo deve chamar [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) para obter o nome de um servidor proxy e, em seguida, chamar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) usando o **\_ \_ proxy de opção WinHTTP** para definir a configuração de proxy no identificador de solicitação WinHTTP criado pelo [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).

A função [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) pode executar todas as três etapas do protocolo WPAD descritas na visão geral anterior: (1) descobrir a URL de PAC, (2) baixar o arquivo de script de PAC, (3) executar o código de script e retornar a configuração de proxy em uma estrutura de **\_ \_ informações de proxy WinHTTP** . Opcionalmente, se o aplicativo sabe antecipadamente a URL de PAC, ele pode especificar isso para **WinHttpGetProxyForUrl**.

O código de exemplo a seguir usa o AutoProxy. Ele configura uma solicitação HTTP GET primeiro criando os identificadores de solicitação e conexão da sessão WinHTTP. A chamada [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) especifica o **tipo de acesso WinHTTP \_ \_ \_ sem \_ proxy** para a configuração de proxy inicial, para indicar que as solicitações são enviadas diretamente para o servidor de destino por padrão. Usando o AutoProxy, ele define a configuração de proxy diretamente no identificador de solicitação.


```C++
  HINTERNET hHttpSession = NULL;
  HINTERNET hConnect     = NULL;
  HINTERNET hRequest     = NULL;
  
  WINHTTP_AUTOPROXY_OPTIONS  AutoProxyOptions;
  WINHTTP_PROXY_INFO         ProxyInfo;
  DWORD                      cbProxyInfoSize = sizeof(ProxyInfo);
  
  ZeroMemory( &AutoProxyOptions, sizeof(AutoProxyOptions) );
  ZeroMemory( &ProxyInfo, sizeof(ProxyInfo) );
  
//
// Create the WinHTTP session.
//
  hHttpSession = WinHttpOpen( L"WinHTTP AutoProxy Sample/1.0",
                              WINHTTP_ACCESS_TYPE_NO_PROXY,
                              WINHTTP_NO_PROXY_NAME,
                              WINHTTP_NO_PROXY_BYPASS,
                              0 );
  
// Exit if WinHttpOpen failed.
  if( !hHttpSession )
    goto Exit;
  
//
// Create the WinHTTP connect handle.
//
  hConnect = WinHttpConnect( hHttpSession,
                             L"www.microsoft.com",
                             INTERNET_DEFAULT_HTTP_PORT,
                             0 );
  
// Exit if WinHttpConnect failed.
  if( !hConnect )
    goto Exit;
  
//
// Create the HTTP request handle.
//
  hRequest = WinHttpOpenRequest( hConnect,
                                 L"GET",
                                 L"ms.htm",
                                 L"HTTP/1.1",
                                 WINHTTP_NO_REFERER,
                                 WINHTTP_DEFAULT_ACCEPT_TYPES,
                                 0 );
  
// Exit if WinHttpOpenRequest failed.
  if( !hRequest )
    goto Exit;
  
//
// Set up the autoproxy call.
//

// Use auto-detection because the Proxy 
// Auto-Config URL is not known.
  AutoProxyOptions.dwFlags = WINHTTP_AUTOPROXY_AUTO_DETECT;

// Use DHCP and DNS-based auto-detection.
  AutoProxyOptions.dwAutoDetectFlags = 
                             WINHTTP_AUTO_DETECT_TYPE_DHCP |
                             WINHTTP_AUTO_DETECT_TYPE_DNS_A;

// If obtaining the PAC script requires NTLM/Negotiate
// authentication, then automatically supply the client
// domain credentials.
  AutoProxyOptions.fAutoLogonIfChallenged = TRUE;

//
// Call WinHttpGetProxyForUrl with our target URL. If 
// auto-proxy succeeds, then set the proxy info on the 
// request handle. If auto-proxy fails, ignore the error 
// and attempt to send the HTTP request directly to the 
// target server (using the default WINHTTP_ACCESS_TYPE_NO_PROXY 
// configuration, which the requesthandle will inherit 
// from the session).
//
  if( WinHttpGetProxyForUrl( hHttpSession,
                             L"https://www.microsoft.com/ms.htm",
                             &AutoProxyOptions,
                             &ProxyInfo))
  {
  // A proxy configuration was found, set it on the
  // request handle.
    
    if( !WinHttpSetOption( hRequest, 
                           WINHTTP_OPTION_PROXY,
                           &ProxyInfo,
                           cbProxyInfoSize ) )
    {
      // Exit if setting the proxy info failed.
      goto Exit;
    }
  }

//
// Send the request.
//
  if( !WinHttpSendRequest( hRequest,
                           WINHTTP_NO_ADDITIONAL_HEADERS,
                           0,
                           WINHTTP_NO_REQUEST_DATA,
                           0,
                           0,
                           NULL ) )
  {
    // Exit if WinHttpSendRequest failed.
    goto Exit;
  }

//
// Wait for the response.
//

  if( !WinHttpReceiveResponse( hRequest, NULL ) )
    goto Exit;

//
// A response has been received, then process it.
// (omitted)
//


  Exit:
  //
  // Clean up the WINHTTP_PROXY_INFO structure.
  //
    if( ProxyInfo.lpszProxy != NULL )
      GlobalFree(ProxyInfo.lpszProxy);

    if( ProxyInfo.lpszProxyBypass != NULL )
      GlobalFree( ProxyInfo.lpszProxyBypass );

  //
  // Close the WinHTTP handles.
  //
    if( hRequest != NULL )
      WinHttpCloseHandle( hRequest );
  
    if( hConnect != NULL )
      WinHttpCloseHandle( hConnect );
  
    if( hHttpSession != NULL )
      WinHttpCloseHandle( hHttpSession );

```



No código de exemplo fornecido, a chamada para [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) instrui a função para descobrir automaticamente o arquivo de configuração automática do proxy especificando o sinalizador **de \_ \_ \_ detecção automática de proxy do WinHTTP** na estrutura de [**\_ \_ Opções de AutoProxy do WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) . O uso do sinalizador de detecção **\_ \_ automática \_ de proxy do WinHTTP** requer que o código especifique um ou ambos os sinalizadores de detecção automática (tipo de **\_ detectada automática do WinHTTP \_ \_ \_ DHCP**, **\_ \_ tipo de detecção automática do WinHTTP \_ \_ DNS \_ A**). O código de exemplo usa o recurso de detecção automática de **WinHttpGetProxyForUrl** porque a URL de PAC não é conhecida com antecedência. Se uma URL de PAC não puder ser localizada na rede nesse cenário, **WinHttpGetProxyForUrl** falhará ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna **erro \_ WinHTTP \_ \_ falha de detecção** automática).

## <a name="if-the-pac-url-is-known-in-advance"></a>Se a URL de PAC for conhecida com antecedência

Se o aplicativo souber a URL de PAC, ele poderá especificá-la na \_ estrutura de opções de AutoProxy do WinHTTP \_ e configurar o [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) para ignorar a fase de detecção automática.

Por exemplo, se um arquivo PAC estiver disponível na rede local na URL, " https://InternalSite/proxy-config.pac ", a chamada para [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) deverá ter a seguinte aparência.


```C++
//
// Set up the autoproxy call.
//

// The proxy auto-config URL is known. Auto-detection
// is not required.
  AutoProxyOptions.dwFlags = WINHTTP_AUTOPROXY_CONFIG_URL;

// Set the proxy auto-config URL.
  AutoProxyOptions. lpszAutoConfigUrl =  L"https://InternalSite/proxy-config.pac";

// If obtaining the PAC script requires NTLM/Negotiate
// authentication, then automatically supply the client
// domain credentials.
  AutoProxyOptions.fAutoLogonIfChallenged = TRUE;

//
// Call WinHttpGetProxyForUrl with our target URL. If auto-proxy
// succeeds, then set the proxy info on the request handle.
// If auto-proxy fails, ignore the error and attempt to send the
// HTTP request directly to the target server (using the default
// WINHTTP_ACCESS_TYPE_NO_PROXY configuration, which the request
// handle will inherit from the session).
//
  if( WinHttpGetProxyForUrl( hHttpSession,
                             L"https://www.microsoft.com/ms.htm",
                             &AutoProxyOptions,
                             &ProxyInfo ) )
{
  //...

```



Se a estrutura de [**\_ \_ Opções de AutoProxy do WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) especificar a detecção **automática de WinHTTP \_ AutoProxy \_ \_** e os sinalizadores de **URL de configuração do WinHTTP \_ AutoProxy \_ \_** (e especificar sinalizadores detction e uma URL de configuração automática), o [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) primeiro tentará a detecção automática e, em seguida, se a detecção automática falhar ao localizar uma URL de PAC, "retornará" à URL de configuração automática fornecida pelo aplicativo.

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a>A função WinHttpDetectAutoProxyConfigUrl

A função [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) implementa um subconjunto do protocolo WPAD: ele tenta detectar automaticamente a URL para o arquivo de configuração automática de proxy, sem baixar ou executar o arquivo PAC. Essa função é útil em situações especiais em que um aplicativo cliente da Web deve lidar com o download e a execução do próprio arquivo PAC.

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a>A função WinHttpGetIEProxyConfigForCurrentUser

A função [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) retorna as configurações de proxy do Internet Explorer do usuário atual para a conexão de rede ativa atual, sem chamar "WinInet.dll". Essa função só é útil quando chamada dentro de um processo que está sendo executado sob uma identidade de conta de usuário interativa, pois nenhuma configuração de proxy do Internet Explorer provavelmente estará disponível. Por exemplo, não seria útil chamar essa função de uma DLL ISAPI em execução no processo do serviço IIS. Para obter mais informações e um cenário no qual um aplicativo baseado em WinHTTP usaria o **WinHttpGetIEProxyConfigForCurrentUser**, consulte [descoberta sem um arquivo de configuração automática](discovery-without-an-auto-config-file.md).

 

 
