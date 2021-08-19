---
description: O método WaitForResponse aguarda a conclusão de um método Send assíncrono, com o valor opcional de tempo-out, em segundos.
ms.assetid: 33265710-ecdc-4eae-8822-161dffbd03fc
title: Método IWinHttpRequest::WaitForResponse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.WaitForResponse
- WinHttpRequest.WaitForResponse
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: e4f72edf2a3532c6d0f2641d979885e6d294c2ad923a28f19b71b348ea3a6377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051994"
---
# <a name="iwinhttprequestwaitforresponse-method"></a>Método IWinHttpRequest::WaitForResponse

O **método WaitForResponse** aguarda a conclusão de um método [**Send**](iwinhttprequest-send.md) assíncrono, com o valor opcional de tempo-out, em segundos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WaitForResponse(
  [in, optional] VARIANT      Timeout,
  [out, retval]  VARIANT_BOOL *Succeeded
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Tempo de vida* \[ in, opcional\]
</dt> <dd>

Valor de tempo-out, em segundos. O tempo-out padrão é infinito. Para definir explicitamente o tempo-fora como infinito, use o valor -1.

</dd> <dt>

*Êxito* \[ out, retval\]
</dt> <dd>

Recebe um dos valores a seguir.



| Valor                                                                                                                                                         | Significado                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <dt>**VARIANT \_ TRUE**</dt> </dl>    | Uma resposta foi recebida.<br/>               |
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <dt>**VARIANT \_ FALSE**</dt> </dl> | O período de tempo limite especificado foi excedido.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é **S \_ OK em** caso de êxito ou um valor de erro, caso contrário.

## <a name="remarks"></a>Comentários

Esse método suspende a execução enquanto aguarda uma resposta a uma solicitação assíncrona. Esse método deve ser chamado após um [**Enviar**](iwinhttprequest-send.md). Chamar aplicativos pode especificar um *valor de Tempoout* opcional, em segundos. Se esse método tiver o tempo de vida, a solicitação não será anulada. Dessa forma, o aplicativo de chamada pode continuar a aguardar a solicitação, se desejado, em uma chamada subsequente para esse método.

Chamar essa propriedade após um método [**Send**](iwinhttprequest-send.md) síncrono retorna imediatamente e não tem nenhum efeito.

> [!Note]  
> Para Windows XP e Windows 2000, consulte [](winhttp-start-page.md) a seção Requisitos de tempo de executar da página inicial do WinHTTP.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como abrir uma conexão HTTP assíncrona, enviar uma solicitação HTTP, aguardar a resposta e ler o texto da resposta.


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
    VARIANT         varTrue;
    VARIANT         varEmpty;

    CLSID           clsid;

    VariantInit(&varTrue);
    V_VT(&varTrue)   = VT_BOOL;
    V_BOOL(&varTrue) = VARIANT_TRUE;

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
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varTrue);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Wait for response.
        VARIANT_BOOL varResult;
        hr = pIWinHttpRequest->WaitForResponse(varEmpty, &varResult);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print the response to a console.
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



O exemplo de script a seguir mostra como abrir uma conexão HTTP assíncrona, enviar uma solicitação HTTP, aguardar uma resposta e ler o texto da resposta.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", true);

// Send the HTTP request.
WinHttpReq.Send(); 

// Wait for the response.
WinHttpReq.WaitForResponse();

// Display the response text.
WScript.Echo( WinHttpReq.ResponseText);
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP, Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]<br/>            |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server somente com aplicativos da área de trabalho SP3 \[\]<br/>         |
| Redistribuível<br/>          | WinHTTP 5.0 e Internet Explorer 5.01 ou posterior no Windows XP e Windows 2000.<br/> |
| Idl<br/>                      | <dl> <dt>HttpRequest.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winhttp.lib</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>Winhttp.dll</dt> </dl>     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWinHttpRequest**](iwinhttprequest-interface.md)
</dt> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[**Aberto**](iwinhttprequest-open.md)
</dt> <dt>

[Versões do WinHTTP](winhttp-versions.md)
</dt> </dl>

 

 




