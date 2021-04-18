---
description: Recupera os cabeçalhos de resposta HTTP.
ms.assetid: 3d59ee83-280c-4074-82e1-ded203fa1049
title: 'Método IWinHttpRequest:: GetResponseHeader'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.GetResponseHeader
- WinHttpRequest.GetResponseHeader
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 6e51b0973c7b078c7de592565db19bf6e029c5a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813614"
---
# <a name="iwinhttprequestgetresponseheader-method"></a>Método IWinHttpRequest:: GetResponseHeader

O método **getResponseHeader** recupera os cabeçalhos de resposta http.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetResponseHeader(
  [in]          BSTR Header,
  [out, retval] BSTR *Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cabeçalho* \[ do no\]
</dt> <dd>

Especifica o nome do cabeçalho que não diferencia maiúsculas de minúsculas.

</dd> <dt>

*Valor* \[ do out, retval\]
</dt> <dd>

Recebe as informações de cabeçalho resultantes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.

## <a name="remarks"></a>Comentários

Esse método retorna o valor do cabeçalho de resposta chamado em *header*. Lembre-se de que os clientes de automação, como o script, obtêm os dados de cabeçalho como o valor de retorno da chamada de função, não através de um parâmetro de função. Invoque esse método somente depois que o método [**Send**](iwinhttprequest-send.md) tiver sido chamado.

> [!Note]  
> Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como abrir uma conexão HTTP, enviar uma solicitação HTTP e obter o cabeçalho de data da resposta. Este exemplo deve ser executado em um prompt de comando.


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

    CLSID           clsid;

    VariantInit(&varFalse);
    V_VT(&varFalse)   = VT_BOOL;
    V_BOOL(&varFalse) = VARIANT_FALSE;

    VariantInit(&varEmpty);
    V_VT(&varEmpty) = VT_ERROR;

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1",
                         &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
    if (SUCCEEDED(hr))
    {
        // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {
        // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {
        // Get Response text.
        BSTR bstrName = SysAllocString(L"Date");
        hr = pIWinHttpRequest->GetResponseHeader(bstrName,
                                             &bstrResponse);
    }
    if (SUCCEEDED(hr))
    {
        // Print response to console.
        wprintf(L"%.256s",bstrResponse);
    }

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



O exemplo de script a seguir mostra como abrir uma conexão HTTP, enviar uma solicitação HTTP e obter o cabeçalho de data da resposta.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", 
                "https://www.microsoft.com", 
                 false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Display the date header.
WScript.Echo( WinHttpReq.GetResponseHeader("Date"));
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

[**GetAllResponseHeaders**](iwinhttprequest-getallresponseheaders.md)
</dt> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




