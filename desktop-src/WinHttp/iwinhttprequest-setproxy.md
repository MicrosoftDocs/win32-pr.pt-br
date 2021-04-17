---
description: Define informações do servidor proxy.
ms.assetid: 279d0557-2718-4c50-b84c-cc7c8def57a6
title: 'Método IWinHttpRequest:: SetProxy'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetProxy
- WinHttpRequest.SetProxy
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 7af3c7c33b17e14c3adbdd70f3d2031e7438747a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780299"
---
# <a name="iwinhttprequestsetproxy-method"></a><span data-ttu-id="f7601-103">Método IWinHttpRequest:: SetProxy</span><span class="sxs-lookup"><span data-stu-id="f7601-103">IWinHttpRequest::SetProxy method</span></span>

<span data-ttu-id="f7601-104">O método **SetProxy** define as informações do servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="f7601-104">The **SetProxy** method sets proxy server information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7601-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7601-105">Syntax</span></span>


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a><span data-ttu-id="f7601-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7601-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7601-107">*ProxySetting* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7601-107">*ProxySetting* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7601-108">Os sinalizadores que controlam esse método.</span><span class="sxs-lookup"><span data-stu-id="f7601-108">The flags that control this method.</span></span> <span data-ttu-id="f7601-109">Pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f7601-109">Can be one of the following values.</span></span>



| <span data-ttu-id="f7601-110">Valor</span><span class="sxs-lookup"><span data-stu-id="f7601-110">Value</span></span>                                                                                                           | <span data-ttu-id="f7601-111">Significado</span><span class="sxs-lookup"><span data-stu-id="f7601-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f7601-112"><dt>\_padrão HTTPREQUEST PROXYSETTING \_</dt></span><span class="sxs-lookup"><span data-stu-id="f7601-112"><dt>HTTPREQUEST\_PROXYSETTING\_DEFAULT</dt></span></span> </dl>   | <span data-ttu-id="f7601-113">Configuração de proxy padrão.</span><span class="sxs-lookup"><span data-stu-id="f7601-113">Default proxy setting.</span></span> <span data-ttu-id="f7601-114">Equivalente a **HTTPREQUEST \_ PROXYSETTING \_ preconfig**.</span><span class="sxs-lookup"><span data-stu-id="f7601-114">Equivalent to **HTTPREQUEST\_PROXYSETTING\_PRECONFIG**.</span></span><br/>                                                                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="f7601-115"><dt>\_configuração de PROXYSETTING HTTPREQUEST \_</dt></span><span class="sxs-lookup"><span data-stu-id="f7601-115"><dt>HTTPREQUEST\_PROXYSETTING\_PRECONFIG</dt></span></span> </dl> | <span data-ttu-id="f7601-116">Indica que as configurações de proxy devem ser obtidas no registro.</span><span class="sxs-lookup"><span data-stu-id="f7601-116">Indicates that the proxy settings should be obtained from the registry.</span></span> <span data-ttu-id="f7601-117">Isso pressupõe que [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) foi executado.</span><span class="sxs-lookup"><span data-stu-id="f7601-117">This assumes that [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) has been run.</span></span> <span data-ttu-id="f7601-118">Se Proxycfg.exe não tiver sido executado e **HttpRequest \_ PROXYSETTING \_ preconfig** for especificado, o comportamento será equivalente a **HTTPREQUEST \_ PROXYSETTING \_ Direct**.</span><span class="sxs-lookup"><span data-stu-id="f7601-118">If Proxycfg.exe has not been run and **HTTPREQUEST\_PROXYSETTING\_PRECONFIG** is specified, then the behavior is equivalent to **HTTPREQUEST\_PROXYSETTING\_DIRECT**.</span></span><br/> |
| <dl> <span data-ttu-id="f7601-119"><dt>HTTPREQUEST \_ PROXYSETTING \_ direto</dt></span><span class="sxs-lookup"><span data-stu-id="f7601-119"><dt>HTTPREQUEST\_PROXYSETTING\_DIRECT</dt></span></span> </dl>    | <span data-ttu-id="f7601-120">Indica que todos os servidores HTTP e HTTPS devem ser acessados diretamente.</span><span class="sxs-lookup"><span data-stu-id="f7601-120">Indicates that all HTTP and HTTPS servers should be accessed directly.</span></span> <span data-ttu-id="f7601-121">Use este comando se não houver nenhum servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="f7601-121">Use this command if there is no proxy server.</span></span><br/>                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="f7601-122"><dt>\_proxy HTTPREQUEST PROXYSETTING \_</dt></span><span class="sxs-lookup"><span data-stu-id="f7601-122"><dt>HTTPREQUEST\_PROXYSETTING\_PROXY</dt></span></span> </dl>     | <span data-ttu-id="f7601-123">Quando **o \_ \_ proxy HTTPREQUEST PROXYSETTING** é especificado, *varProxyServer* deve ser definido como uma cadeia de caracteres do servidor proxy e *varBypassList* deve ser definido como uma cadeia de caracteres da lista de ignorados de domínio.</span><span class="sxs-lookup"><span data-stu-id="f7601-123">When **HTTPREQUEST\_PROXYSETTING\_PROXY** is specified, *varProxyServer* should be set to a proxy server string and *varBypassList* should be set to a domain bypass list string.</span></span> <span data-ttu-id="f7601-124">Essa configuração de proxy aplica-se somente à instância atual do objeto [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="f7601-124">This proxy configuration applies only to the current instance of the [**WinHttpRequest**](winhttprequest.md) object.</span></span><br/>                                    |



 

</dd> <dt>

<span data-ttu-id="f7601-125">*ProxyServer* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f7601-125">*ProxyServer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7601-126">Defina como uma cadeia de caracteres de servidor proxy quando *ProxySetting* for igual a **HTTPREQUEST \_ ProxySetting \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="f7601-126">Set to a proxy server string when *ProxySetting* equals **HTTPREQUEST\_PROXYSETTING\_PROXY**.</span></span>

</dd> <dt>

<span data-ttu-id="f7601-127">*BypassList* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f7601-127">*BypassList* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f7601-128">Defina como uma cadeia de caracteres de lista de ignorados de domínio quando *ProxySetting* for igual a **HTTPREQUEST \_ ProxySetting \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="f7601-128">Set to a domain bypass list string when *ProxySetting* equals **HTTPREQUEST\_PROXYSETTING\_PROXY**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7601-129">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7601-129">Return value</span></span>

<span data-ttu-id="f7601-130">O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f7601-130">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7601-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7601-131">Remarks</span></span>

<span data-ttu-id="f7601-132">Permite que o aplicativo de chamada especifique o uso de informações de proxy padrão (configuradas pela ferramenta de configuração de proxy) ou substitua [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md).</span><span class="sxs-lookup"><span data-stu-id="f7601-132">Enables the calling application to specify use of default proxy information (configured by the proxy configuration tool) or to override [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md).</span></span> <span data-ttu-id="f7601-133">Esse método deve ser chamado antes de chamar o método [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="f7601-133">This method must be called before calling the [**Send**](iwinhttprequest-send.md) method.</span></span> <span data-ttu-id="f7601-134">Se esse método for chamado após o método [**Send**](iwinhttprequest-send.md) , ele não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="f7601-134">If this method is called after the [**Send**](iwinhttprequest-send.md) method, it has no effect.</span></span>

<span data-ttu-id="f7601-135">[**IWinHttpRequest**](iwinhttprequest-interface.md) passa esses parâmetros para o Microsoft Windows http Services (WinHTTP).</span><span class="sxs-lookup"><span data-stu-id="f7601-135">[**IWinHttpRequest**](iwinhttprequest-interface.md) passes these parameters to Microsoft Windows HTTP Services (WinHTTP).</span></span>

> [!Note]  
> <span data-ttu-id="f7601-136">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="f7601-136">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="f7601-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f7601-137">Examples</span></span>

<span data-ttu-id="f7601-138">O exemplo a seguir mostra como definir as configurações de proxy para um servidor proxy específico, abrir uma conexão HTTP, enviar uma solicitação HTTP e ler o texto da resposta.</span><span class="sxs-lookup"><span data-stu-id="f7601-138">The following example shows how to set the proxy settings for a particular proxy server, open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="f7601-139">Este exemplo deve ser executado em um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="f7601-139">This example must be run from a command prompt.</span></span> <span data-ttu-id="f7601-140">Essas configurações de proxy só funcionarão se você tiver um servidor proxy chamado " \_ servidor proxy" que usa a porta 80 e o computador puder ignorar o servidor proxy quando o nome do host terminar com ". Microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="f7601-140">These proxy settings work only if you have a proxy server named "proxy\_server" that uses port 80 and your computer can bypass the proxy server when the host name ends with ".microsoft.com".</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <objbase.h>

#include "httprequest.h"

#pragma comment(lib, "ole32.lib")
#pragma comment(lib, "oleaut32.lib")

// IID for IWinHttpRequest.
const IID IID_IWinHttpRequest =
{
  0x06f29373,
  0x5c5a,
  0x4b54,
  {0xb0, 0x25, 0x6e, 0xf1, 0xbf, 0x8a, 0xbf, 0x0e}
};

int main()
{
    // Variable for return value
    HRESULT    hr;

    // Initialize COM
    hr = CoInitialize( NULL );

    IWinHttpRequest *  pIWinHttpRequest = NULL;

    BSTR            bstrResponse = NULL;
    VARIANT         varFalse;
    VARIANT         varEmpty;
    VARIANT         varProxy;
    VARIANT         varUrl;
    
    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    VariantInit(&varProxy);
    VariantInit(&varUrl);

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IWinHttpRequest, 
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {   // Specify proxy and URL.
                varProxy.vt = VT_BSTR;
                varProxy.bstrVal = SysAllocString(L"proxy_server:80");
                varUrl.vt = VT_BSTR;
                varUrl.bstrVal = SysAllocString(L"*.microsoft.com");
                hr = pIWinHttpRequest->SetProxy(HTTPREQUEST_PROXYSETTING_PROXY,
                                    varProxy, varUrl); 
        }
    if (SUCCEEDED(hr))
    {   // Open WinHttpRequest.
            BSTR bstrMethod  = SysAllocString(L"GET");
                BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
                SysFreeString(bstrMethod);
                SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {   // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {   // Get Response text.
                hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {   // Print the response to a console.
                wprintf(L"%.256s",bstrResponse);
    }
        
        // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
        if (varProxy.bstrVal)
                SysFreeString(varProxy.bstrVal);
        if (varUrl.bstrVal)
                SysFreeString(varUrl.bstrVal);
    if (bstrResponse)
        SysFreeString(bstrResponse);
        
        CoUninitialize();
        return 0;
}
```



<span data-ttu-id="f7601-141">O exemplo de script a seguir mostra como definir as configurações de proxy para um servidor proxy específico, abrir uma conexão HTTP, enviar uma solicitação HTTP e ler o texto da resposta.</span><span class="sxs-lookup"><span data-stu-id="f7601-141">The following scripting example shows how to set the proxy settings for a particular proxy server, open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="f7601-142">Essas configurações de proxy só funcionarão se você tiver um servidor proxy chamado " \_ servidor proxy" que usa a porta 80 e o computador puder ignorar o servidor proxy quando o nome do host terminar com ". Microsoft.com".</span><span class="sxs-lookup"><span data-stu-id="f7601-142">These proxy settings work only if you have a proxy server named "proxy\_server" that uses port 80 and your computer can bypass the proxy server when the host name ends with ".microsoft.com".</span></span>


```JScript
// HttpRequest SetCredentials flags.
HTTPREQUEST_PROXYSETTING_DEFAULT   = 0;
HTTPREQUEST_PROXYSETTING_PRECONFIG = 0;
HTTPREQUEST_PROXYSETTING_DIRECT    = 1;
HTTPREQUEST_PROXYSETTING_PROXY     = 2;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Use proxy_server for all requests outside of 
// the microsoft.com domain.
WinHttpReq.SetProxy( HTTPREQUEST_PROXYSETTING_PROXY, 
                     "proxy_server:80", 
                     "*.microsoft.com");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a><span data-ttu-id="f7601-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7601-143">Requirements</span></span>



| <span data-ttu-id="f7601-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7601-144">Requirement</span></span> | <span data-ttu-id="f7601-145">Valor</span><span class="sxs-lookup"><span data-stu-id="f7601-145">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7601-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7601-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f7601-147">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="f7601-147">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="f7601-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7601-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f7601-149">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="f7601-149">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="f7601-150">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f7601-150">Redistributable</span></span><br/>          | <span data-ttu-id="f7601-151">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f7601-151">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="f7601-152">INSERI</span><span class="sxs-lookup"><span data-stu-id="f7601-152">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f7601-153"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f7601-153"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="f7601-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f7601-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="f7601-155"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7601-155"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="f7601-156">DLL</span><span class="sxs-lookup"><span data-stu-id="f7601-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7601-157"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7601-157"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f7601-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7601-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7601-159">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="f7601-159">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="f7601-160">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="f7601-160">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="f7601-161">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="f7601-161">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




