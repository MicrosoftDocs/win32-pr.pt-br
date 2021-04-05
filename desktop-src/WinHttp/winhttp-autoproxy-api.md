---
description: O WinHTTP implementa o protocolo WPAD usando a função WinHttpGetProxyForUrl juntamente com duas funções de utilitário de suporte, WinHttpDetectAutoProxyConfigUrl e WinHttpGetIEProxyConfigForCurrentUser.
ms.assetid: d941e3c6-c1db-4de1-b640-4f582f86fc54
title: Funções de AutoProxy do WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd4cf8289add4c72c2266df4bb9025e0b4c1aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920920"
---
# <a name="winhttp-autoproxy-functions"></a><span data-ttu-id="96c10-103">Funções de AutoProxy do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="96c10-103">WinHTTP AutoProxy Functions</span></span>

<span data-ttu-id="96c10-104">O WinHTTP implementa o protocolo WPAD usando a função [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) juntamente com duas funções de utilitário de suporte, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) e [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).</span><span class="sxs-lookup"><span data-stu-id="96c10-104">WinHTTP implements the WPAD protocol using the [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function along with two supporting utility functions, [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) and [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser).</span></span>

<span data-ttu-id="96c10-105">O suporte a AutoProxy não está totalmente integrado à pilha HTTP no WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="96c10-105">AutoProxy support is not fully integrated into the HTTP stack in WinHTTP.</span></span> <span data-ttu-id="96c10-106">Antes de enviar uma solicitação, o aplicativo deve chamar [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) para obter o nome de um servidor proxy e, em seguida, chamar [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) usando o **\_ \_ proxy de opção WinHTTP** para definir a configuração de proxy no identificador de solicitação WinHTTP criado pelo [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span><span class="sxs-lookup"><span data-stu-id="96c10-106">Before sending a request, the application must call [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) to obtain the name of a proxy server and then call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) using **WINHTTP\_OPTION\_PROXY** to set the proxy configuration on the WinHTTP request handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span></span>

<span data-ttu-id="96c10-107">A função [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) pode executar todas as três etapas do protocolo WPAD descritas na visão geral anterior: (1) descobrir a URL de PAC, (2) baixar o arquivo de script de PAC, (3) executar o código de script e retornar a configuração de proxy em uma estrutura de **\_ \_ informações de proxy WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="96c10-107">The [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) function can execute all three steps of the WPAD protocol described in the previous overview: (1) discover the PAC URL, (2) download the PAC script file, (3) execute the script code and return the proxy configuration in a **WINHTTP\_PROXY\_INFO** structure.</span></span> <span data-ttu-id="96c10-108">Opcionalmente, se o aplicativo sabe antecipadamente a URL de PAC, ele pode especificar isso para **WinHttpGetProxyForUrl**.</span><span class="sxs-lookup"><span data-stu-id="96c10-108">Optionally, if the application knows in advance the PAC URL it can specify this to **WinHttpGetProxyForUrl**.</span></span>

<span data-ttu-id="96c10-109">O código de exemplo a seguir usa o AutoProxy.</span><span class="sxs-lookup"><span data-stu-id="96c10-109">The following example code uses autoproxy.</span></span> <span data-ttu-id="96c10-110">Ele configura uma solicitação HTTP GET primeiro criando os identificadores de solicitação e conexão da sessão WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="96c10-110">It sets up an HTTP GET request by first creating the WinHTTP session connect and request handles.</span></span> <span data-ttu-id="96c10-111">A chamada [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) especifica o **tipo de acesso WinHTTP \_ \_ \_ sem \_ proxy** para a configuração de proxy inicial, para indicar que as solicitações são enviadas diretamente para o servidor de destino por padrão.</span><span class="sxs-lookup"><span data-stu-id="96c10-111">The [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) call specifies **WINHTTP\_ACCESS\_TYPE\_NO\_PROXY** for the initial proxy configuration, to indicate that requests are sent directly to the target server by default.</span></span> <span data-ttu-id="96c10-112">Usando o AutoProxy, ele define a configuração de proxy diretamente no identificador de solicitação.</span><span class="sxs-lookup"><span data-stu-id="96c10-112">Using autoproxy, it then sets the proxy configuration directly on the request handle.</span></span>


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



<span data-ttu-id="96c10-113">No código de exemplo fornecido, a chamada para [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) instrui a função para descobrir automaticamente o arquivo de configuração automática do proxy especificando o sinalizador **de \_ \_ \_ detecção automática de proxy do WinHTTP** na estrutura de [**\_ \_ Opções de AutoProxy do WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) .</span><span class="sxs-lookup"><span data-stu-id="96c10-113">In the provided example code, the call to [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) instructs the function to discover the proxy auto-config file automatically by specifying the **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** flag in the [**WINHTTP\_AUTOPROXY\_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) structure.</span></span> <span data-ttu-id="96c10-114">O uso do sinalizador de detecção **\_ \_ automática \_ de proxy do WinHTTP** requer que o código especifique um ou ambos os sinalizadores de detecção automática (tipo de **\_ detectada automática do WinHTTP \_ \_ \_ DHCP**, **\_ \_ tipo de detecção automática do WinHTTP \_ \_ DNS \_ A**).</span><span class="sxs-lookup"><span data-stu-id="96c10-114">Use of the **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** flag requires the code to specify one or both of the auto-detection flags (**WINHTTP\_AUTO\_DETECT\_TYPE\_DHCP**, **WINHTTP\_AUTO\_DETECT\_TYPE\_DNS\_A**).</span></span> <span data-ttu-id="96c10-115">O código de exemplo usa o recurso de detecção automática de **WinHttpGetProxyForUrl** porque a URL de PAC não é conhecida com antecedência.</span><span class="sxs-lookup"><span data-stu-id="96c10-115">The example code uses the auto-detection feature of **WinHttpGetProxyForUrl** because the PAC URL is not known in advance.</span></span> <span data-ttu-id="96c10-116">Se uma URL de PAC não puder ser localizada na rede nesse cenário, **WinHttpGetProxyForUrl** falhará ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna **erro \_ WinHTTP \_ \_ falha de detecção** automática).</span><span class="sxs-lookup"><span data-stu-id="96c10-116">If a PAC URL cannot be located on the network in this scenario, **WinHttpGetProxyForUrl** fails ([**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR\_WINHTTP\_AUTODETECTION\_FAILED**).</span></span>

## <a name="if-the-pac-url-is-known-in-advance"></a><span data-ttu-id="96c10-117">Se a URL de PAC for conhecida com antecedência</span><span class="sxs-lookup"><span data-stu-id="96c10-117">If the PAC URL is Known in Advance</span></span>

<span data-ttu-id="96c10-118">Se o aplicativo souber a URL de PAC, ele poderá especificá-la na \_ estrutura de opções de AutoProxy do WinHTTP \_ e configurar o [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) para ignorar a fase de detecção automática.</span><span class="sxs-lookup"><span data-stu-id="96c10-118">If the application does know the PAC URL, it can specify it in the WINHTTP\_AUTOPROXY\_OPTIONS structure and configure [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) to skip the auto-detection phase.</span></span>

<span data-ttu-id="96c10-119">Por exemplo, se um arquivo PAC estiver disponível na rede local na URL, " https://InternalSite/proxy-config.pac ", a chamada para [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) deverá ter a seguinte aparência.</span><span class="sxs-lookup"><span data-stu-id="96c10-119">For example, if a PAC file is available on the local network at the URL, "https://InternalSite/proxy-config.pac", the call to [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) would look the following.</span></span>


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



<span data-ttu-id="96c10-120">Se a estrutura de [**\_ \_ Opções de AutoProxy do WinHTTP**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) especificar a detecção **automática de WinHTTP \_ AutoProxy \_ \_** e os sinalizadores de **URL de configuração do WinHTTP \_ AutoProxy \_ \_** (e especificar sinalizadores detction e uma URL de configuração automática), o [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) primeiro tentará a detecção automática e, em seguida, se a detecção automática falhar ao localizar uma URL de PAC, "retornará" à URL de configuração automática fornecida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96c10-120">If the [**WINHTTP\_AUTOPROXY\_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options) structure specifies both **WINHTTP\_AUTOPROXY\_AUTO\_DETECT** and **WINHTTP\_AUTOPROXY\_CONFIG\_URL** flags (and specifies auto-detction flags and an auto-config URL), [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) first attempts auto-detection, and then, if auto-detection fails to locate a PAC URL, "falls back" to the auto-config URL supplied by the application.</span></span>

## <a name="the-winhttpdetectautoproxyconfigurl-function"></a><span data-ttu-id="96c10-121">A função WinHttpDetectAutoProxyConfigUrl</span><span class="sxs-lookup"><span data-stu-id="96c10-121">The WinHttpDetectAutoProxyConfigUrl Function</span></span>

<span data-ttu-id="96c10-122">A função [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) implementa um subconjunto do protocolo WPAD: ele tenta detectar automaticamente a URL para o arquivo de configuração automática de proxy, sem baixar ou executar o arquivo PAC.</span><span class="sxs-lookup"><span data-stu-id="96c10-122">The [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) function implements a subset of the WPAD protocol: it attempts to auto-detect the URL for the proxy auto-config file, without downloading or executing the PAC file.</span></span> <span data-ttu-id="96c10-123">Essa função é útil em situações especiais em que um aplicativo cliente da Web deve lidar com o download e a execução do próprio arquivo PAC.</span><span class="sxs-lookup"><span data-stu-id="96c10-123">This function is useful in special situations where a Web client application must handle the download and execution of the PAC file itself.</span></span>

## <a name="the-winhttpgetieproxyconfigforcurrentuser-function"></a><span data-ttu-id="96c10-124">A função WinHttpGetIEProxyConfigForCurrentUser</span><span class="sxs-lookup"><span data-stu-id="96c10-124">The WinHttpGetIEProxyConfigForCurrentUser Function</span></span>

<span data-ttu-id="96c10-125">A função [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) retorna as configurações de proxy do Internet Explorer do usuário atual para a conexão de rede ativa atual, sem chamar "WinInet.dll".</span><span class="sxs-lookup"><span data-stu-id="96c10-125">The [**WinHttpGetIEProxyConfigForCurrentUser**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser) function returns the current user Internet Explorer proxy settings for the current active network connection, without calling into "WinInet.dll".</span></span> <span data-ttu-id="96c10-126">Essa função só é útil quando chamada dentro de um processo que está sendo executado sob uma identidade de conta de usuário interativa, pois nenhuma configuração de proxy do Internet Explorer provavelmente estará disponível.</span><span class="sxs-lookup"><span data-stu-id="96c10-126">This function is only useful when called within a process that is running under an interactive user account identity, because no Internet Explorer proxy configuration is likely to be available otherwise.</span></span> <span data-ttu-id="96c10-127">Por exemplo, não seria útil chamar essa função de uma DLL ISAPI em execução no processo do serviço IIS.</span><span class="sxs-lookup"><span data-stu-id="96c10-127">For example, it would not be useful to call this function from an ISAPI DLL running in the IIS service process.</span></span> <span data-ttu-id="96c10-128">Para obter mais informações e um cenário no qual um aplicativo baseado em WinHTTP usaria o **WinHttpGetIEProxyConfigForCurrentUser**, consulte [descoberta sem um arquivo de configuração automática](discovery-without-an-auto-config-file.md).</span><span class="sxs-lookup"><span data-stu-id="96c10-128">For more information and a scenario in which a WinHTTP-based application would use **WinHttpGetIEProxyConfigForCurrentUser**, see [Discovery Without an Auto-Config File](discovery-without-an-auto-config-file.md).</span></span>

 

 
