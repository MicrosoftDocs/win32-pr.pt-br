---
description: Recupera o corpo da entidade de resposta como texto.
ms.assetid: 87caf64f-be11-45c9-af1e-997a55c5e76e
title: 'Propriedade IWinHttpRequest:: ResponseText'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.ResponseText
- IWinHttpRequest.get_ResponseText
- WinHttpRequest.ResponseText
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: e43169ee789a067b75444e5f19e5bb7985ce402efd4b89c08f049dbcad9a7049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563184"
---
# <a name="iwinhttprequestresponsetext-property"></a>Propriedade IWinHttpRequest:: ResponseText

A propriedade **ResponseText** recupera o corpo da entidade de resposta como texto.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_ResponseText(
  [out, retval] BSTR *Body
);
```


```JScript

strResponseText = WinHttpRequest.ResponseText
```





## <a name="property-value"></a>Valor da propriedade

**BSTR** que recebe o corpo da entidade da resposta como texto.

## <a name="error-codes"></a>Códigos do Erro

O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.

## <a name="remarks"></a>Comentários

Essa propriedade só pode ser chamada depois que o método [**Send**](iwinhttprequest-send.md) for chamado.

Ao usar essa propriedade no modo síncrono, o limite para o número de caracteres que ele retorna é de aproximadamente 2.169.895.

> [!Note]  
> para Windows XP e Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como abrir uma conexão HTTP, enviar uma solicitação HTTP e ler o texto da resposta. Este exemplo deve ser executado em um prompt de comando.


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

    // Initialize COM.
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

    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
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

    // Print the response to a console.
    wprintf(L"%.256s",bstrResponse);

    // Release memory.
    if (pIWinHttpRequest)
        pIWinHttpRequest->Release();
    if (bstrResponse)
        SysFreeString(bstrResponse);

    CoUninitialize();
    return 0;
}

```



O exemplo de script a seguir mostra como abrir uma conexão HTTP, enviar uma solicitação HTTP e ler o texto da resposta.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

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
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com \[ aplicativos da área de trabalho do SP3\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows servidor 2003, Windows 2000 servidor somente com \[ aplicativos de área de trabalho do SP3\]<br/>         |
| Redistribuível<br/>          | WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior em Windows XP e Windows 2000.<br/> |
| INSERI<br/>                      | <dl> <dt>HttpRequest. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WinHTTP. lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[**ResponseBody**](iwinhttprequest-responsebody.md)
</dt> <dt>

[**ResponseStream**](iwinhttprequest-responsestream.md)
</dt> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




