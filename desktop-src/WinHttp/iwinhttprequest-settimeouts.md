---
description: O método settempo_limites especifica os componentes de tempo limite individuais de uma operação de envio/recebimento, em milissegundos.
ms.assetid: c2b6c432-5f3b-4361-8026-1b843c6697ae
title: 'Método IWinHttpRequest:: settempo_limites'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetTimeouts
- WinHttpRequest.SetTimeouts
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 3f2f81585fdf444b6b5ab1795f183897687732ed
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104172903"
---
# <a name="iwinhttprequestsettimeouts-method"></a>Método IWinHttpRequest:: settempo_limites

O método **Settempo_limites** especifica os componentes de tempo limite individuais de uma operação de envio/recebimento, em milissegundos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetTimeouts(
  [in] long ResolveTimeout,
  [in] long ConnectTimeout,
  [in] long SendTimeout,
  [in] long ReceiveTimeout
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ResolveTimeout* \[ no\]
</dt> <dd>

Valor de tempo limite aplicado ao resolver um nome de host (como `www.microsoft.com` ) para um endereço IP (como 192.168.131.199), em milissegundos. O valor padrão é zero, o que significa que não há tempo limite (infinito). Se o tempo limite do DNS for especificado usando \_ \_ o tempo limite de resolução de nome, haverá uma sobrecarga de um thread por solicitação.

</dd> <dt>

*ConnectTimeout* \[ no\]
</dt> <dd>

Valor de tempo limite aplicado ao estabelecer um soquete de comunicação com o servidor de destino, em milissegundos. O valor padrão é 60.000 (60 segundos).

</dd> <dt>

*SendTimeout* \[ no\]
</dt> <dd>

Valor de tempo limite aplicado ao enviar um pacote individual de dados de solicitação no soquete de comunicação para o servidor de destino, em milissegundos. Uma solicitação grande enviada a um servidor HTTP normalmente é dividida em vários pacotes; o tempo limite de envio se aplica ao envio individual de cada pacote. O valor padrão é 30.000 (30 segundos).

</dd> <dt>

*ReceiveTimeout* \[ no\]
</dt> <dd>

Valor de tempo limite aplicado ao receber um pacote de dados de resposta do servidor de destino, em milissegundos. As respostas grandes são divididas em vários pacotes; o tempo limite de recebimento se aplica à busca de cada pacote de dados fora do soquete. O valor padrão é 30.000 (30 segundos).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.

## <a name="remarks"></a>Comentários

Todos os parâmetros são obrigatórios. Um valor de 0 ou-1 define um tempo limite para aguardar infinitamente. Um valor maior que 0 define o valor de tempo limite em milissegundos. Por exemplo, 30.000 definiria o tempo limite para 30 segundos. Todos os valores negativos diferentes de-1 causam a falha desse método.

Os valores de tempo limite são aplicados na camada do Winsock.

> [!Note]  
> Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como definir todos os tempos limite de WinHTTP para 30 segundos, abrir uma conexão HTTP, enviar uma solicitação HTTP e ler o texto da resposta.


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
    // variable for return value
    HRESULT    hr;

    // initialize COM
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
    {    // Set Time-outs.
        hr = pIWinHttpRequest->SetTimeouts(30000, 30000,
                                           30000, 30000);
    }
    if (SUCCEEDED(hr))
    {    // Open WinHttpRequest.
        BSTR bstrMethod  = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod,
                                    bstrUrl,
                                    varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->GetAllResponseHeaders(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {    // Print response to console.
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



O exemplo de script a seguir mostra como definir todos os tempos limite de WinHTTP para 30 segundos, abrir uma conexão HTTP e enviar uma solicitação HTTP.


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Set time-outs. If time-outs are set, they must 
// be set before open.
WinHttpReq.SetTimeouts(30000, 30000, 30000, 30000);

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

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

 

 




