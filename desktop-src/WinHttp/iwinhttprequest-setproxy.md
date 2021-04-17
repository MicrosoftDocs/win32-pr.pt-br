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
# <a name="iwinhttprequestsetproxy-method"></a>Método IWinHttpRequest:: SetProxy

O método **SetProxy** define as informações do servidor proxy.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetProxy(
  [in]           HTTPREQUEST_PROXY_SETTING ProxySetting,
  [in, optional] VARIANT                   ProxyServer,
  [in, optional] VARIANT                   BypassList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProxySetting* \[ no\]
</dt> <dd>

Os sinalizadores que controlam esse método. Pode ser um dos valores a seguir.



| Valor                                                                                                           | Significado                                                                                                                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>\_padrão HTTPREQUEST PROXYSETTING \_</dt> </dl>   | Configuração de proxy padrão. Equivalente a **HTTPREQUEST \_ PROXYSETTING \_ preconfig**.<br/>                                                                                                                                                                                                                                                             |
| <dl> <dt>\_configuração de PROXYSETTING HTTPREQUEST \_</dt> </dl> | Indica que as configurações de proxy devem ser obtidas no registro. Isso pressupõe que [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md) foi executado. Se Proxycfg.exe não tiver sido executado e **HttpRequest \_ PROXYSETTING \_ preconfig** for especificado, o comportamento será equivalente a **HTTPREQUEST \_ PROXYSETTING \_ Direct**.<br/> |
| <dl> <dt>HTTPREQUEST \_ PROXYSETTING \_ direto</dt> </dl>    | Indica que todos os servidores HTTP e HTTPS devem ser acessados diretamente. Use este comando se não houver nenhum servidor proxy.<br/>                                                                                                                                                                                                                       |
| <dl> <dt>\_proxy HTTPREQUEST PROXYSETTING \_</dt> </dl>     | Quando **o \_ \_ proxy HTTPREQUEST PROXYSETTING** é especificado, *varProxyServer* deve ser definido como uma cadeia de caracteres do servidor proxy e *varBypassList* deve ser definido como uma cadeia de caracteres da lista de ignorados de domínio. Essa configuração de proxy aplica-se somente à instância atual do objeto [**WinHttpRequest**](winhttprequest.md) .<br/>                                    |



 

</dd> <dt>

*ProxyServer* \[ em, opcional\]
</dt> <dd>

Defina como uma cadeia de caracteres de servidor proxy quando *ProxySetting* for igual a **HTTPREQUEST \_ ProxySetting \_ proxy**.

</dd> <dt>

*BypassList* \[ em, opcional\]
</dt> <dd>

Defina como uma cadeia de caracteres de lista de ignorados de domínio quando *ProxySetting* for igual a **HTTPREQUEST \_ ProxySetting \_ proxy**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.

## <a name="remarks"></a>Comentários

Permite que o aplicativo de chamada especifique o uso de informações de proxy padrão (configuradas pela ferramenta de configuração de proxy) ou substitua [Proxycfg.exe](proxycfg-exe--a-proxy-configuration-tool.md). Esse método deve ser chamado antes de chamar o método [**Send**](iwinhttprequest-send.md) . Se esse método for chamado após o método [**Send**](iwinhttprequest-send.md) , ele não terá nenhum efeito.

[**IWinHttpRequest**](iwinhttprequest-interface.md) passa esses parâmetros para o Microsoft Windows http Services (WinHTTP).

> [!Note]  
> Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como definir as configurações de proxy para um servidor proxy específico, abrir uma conexão HTTP, enviar uma solicitação HTTP e ler o texto da resposta. Este exemplo deve ser executado em um prompt de comando. Essas configurações de proxy só funcionarão se você tiver um servidor proxy chamado " \_ servidor proxy" que usa a porta 80 e o computador puder ignorar o servidor proxy quando o nome do host terminar com ". Microsoft.com".


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



O exemplo de script a seguir mostra como definir as configurações de proxy para um servidor proxy específico, abrir uma conexão HTTP, enviar uma solicitação HTTP e ler o texto da resposta. Essas configurações de proxy só funcionarão se você tiver um servidor proxy chamado " \_ servidor proxy" que usa a porta 80 e o computador puder ignorar o servidor proxy quando o nome do host terminar com ". Microsoft.com".


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]<br/>         |
| Redistribuível<br/>          | WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.<br/> |
| INSERI<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




