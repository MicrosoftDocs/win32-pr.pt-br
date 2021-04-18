---
description: Adiciona, altera ou exclui um cabeçalho de solicitação HTTP.
ms.assetid: 8cb4891d-0bdb-4dea-8ebe-d6ed26a50e41
title: 'Método IWinHttpRequest:: SetRequestHeader'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetRequestHeader
- WinHttpRequest.SetRequestHeader
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 9bc2ae6df420f38d11fb2f0f19d5fcbd0bcc0909
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812871"
---
# <a name="iwinhttprequestsetrequestheader-method"></a>Método IWinHttpRequest:: SetRequestHeader

O método **SetRequestHeader** adiciona, altera ou exclui um cabeçalho de solicitação HTTP.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetRequestHeader(
  [in] BSTR Header,
  [in] BSTR Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cabeçalho* \[ do no\]
</dt> <dd>

Especifica o nome do cabeçalho a ser definido, por exemplo, "Depth". Esse parâmetro não deve conter dois-pontos e deve ser o texto real do cabeçalho HTTP.

</dd> <dt>

*Valor* \[ do no\]
</dt> <dd>

Especifica o valor do cabeçalho, por exemplo, "Infinity".

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.

## <a name="remarks"></a>Comentários

Os cabeçalhos são transferidos entre redirecionamentos. Isso pode criar uma vulnerabilidade de segurança. Para evitar que os cabeçalhos sejam transferidos se um redirecionamento ocorrer, use o retorno de chamada de [*\_ \_ status do WinHTTP*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) para corrigir os cabeçalhos específicos quando ocorrer um redirecionamento.

O método **SetRequestHeader** permite que o aplicativo de chamada adicione ou exclua um cabeçalho de solicitação HTTP antes de enviar a solicitação. O nome do cabeçalho é fornecido no *cabeçalho* e o token ou valor do cabeçalho é fornecido em *valor*. Para adicionar um cabeçalho, forneça um nome e um valor de cabeçalho. Se outro cabeçalho já existir com esse nome, ele será substituído. Para excluir um cabeçalho, defina o *cabeçalho* como o nome do cabeçalho a ser excluído e defina o *valor* como **nulo**.

O nome e o valor dos cabeçalhos de solicitação adicionados com esse método são validados. Os cabeçalhos devem estar bem formados. Para obter mais informações sobre cabeçalhos HTTP válidos, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt). Se um cabeçalho inválido for usado, ocorrerá um erro e o cabeçalho não será adicionado.

> [!Note]  
> Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como abrir uma conexão HTTP, definir um cabeçalho de solicitação, enviar uma solicitação HTTP e ler o texto da resposta. Este exemplo deve ser executado em um prompt de comando.


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
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set request header.
        BSTR bstrName  = SysAllocString(L"Date");
        BSTR bstrValue = SysAllocString(L"Fri, 16 Mar 2001 00:25:54 GMT");
        hr = pIWinHttpRequest->SetRequestHeader(bstrName, bstrValue);
        SysFreeString(bstrName);
        SysFreeString(bstrValue);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response headers.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
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



O exemplo de script a seguir mostra como abrir uma conexão HTTP, definir um cabeçalho de solicitação e enviar uma solicitação HTTP.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Add/replace a request header.
WinHttpReq.SetRequestHeader("Date", Date());

// Send the HTTP request.
WinHttpReq.Send();
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

 

