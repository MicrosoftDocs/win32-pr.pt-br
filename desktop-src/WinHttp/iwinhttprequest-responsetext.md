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
ms.openlocfilehash: 93e0a9b17ba356f9ce6b038be114f5f2c9804eab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812211"
---
# <a name="iwinhttprequestresponsetext-property"></a><span data-ttu-id="5894a-103">Propriedade IWinHttpRequest:: ResponseText</span><span class="sxs-lookup"><span data-stu-id="5894a-103">IWinHttpRequest::ResponseText property</span></span>

<span data-ttu-id="5894a-104">A propriedade **ResponseText** recupera o corpo da entidade de resposta como texto.</span><span class="sxs-lookup"><span data-stu-id="5894a-104">The **ResponseText** property retrieves the response entity body as text.</span></span>

<span data-ttu-id="5894a-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="5894a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5894a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5894a-106">Syntax</span></span>


```C++
HRESULT get_ResponseText(
  [out, retval] BSTR *Body
);
```


```JScript

strResponseText = WinHttpRequest.ResponseText
```





## <a name="property-value"></a><span data-ttu-id="5894a-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="5894a-107">Property value</span></span>

<span data-ttu-id="5894a-108">**BSTR** que recebe o corpo da entidade da resposta como texto.</span><span class="sxs-lookup"><span data-stu-id="5894a-108">**BSTR** that receives the entity body of the response as text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5894a-109">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="5894a-109">Error codes</span></span>

<span data-ttu-id="5894a-110">O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="5894a-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5894a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5894a-111">Remarks</span></span>

<span data-ttu-id="5894a-112">Essa propriedade só pode ser chamada depois que o método [**Send**](iwinhttprequest-send.md) for chamado.</span><span class="sxs-lookup"><span data-stu-id="5894a-112">This property can only be invoked after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

<span data-ttu-id="5894a-113">Ao usar essa propriedade no modo síncrono, o limite para o número de caracteres que ele retorna é de aproximadamente 2.169.895.</span><span class="sxs-lookup"><span data-stu-id="5894a-113">When using this property in synchronous mode, the limit to the number of characters it returns is approximately 2,169,895.</span></span>

> [!Note]  
> <span data-ttu-id="5894a-114">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="5894a-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="5894a-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5894a-115">Examples</span></span>

<span data-ttu-id="5894a-116">O exemplo a seguir mostra como abrir uma conexão HTTP, enviar uma solicitação HTTP e ler o texto da resposta.</span><span class="sxs-lookup"><span data-stu-id="5894a-116">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="5894a-117">Este exemplo deve ser executado em um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="5894a-117">This example must be run from a command prompt.</span></span>


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



<span data-ttu-id="5894a-118">O exemplo de script a seguir mostra como abrir uma conexão HTTP, enviar uma solicitação HTTP e ler o texto da resposta.</span><span class="sxs-lookup"><span data-stu-id="5894a-118">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="5894a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5894a-119">Requirements</span></span>



| <span data-ttu-id="5894a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5894a-120">Requirement</span></span> | <span data-ttu-id="5894a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5894a-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5894a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5894a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5894a-123">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="5894a-123">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="5894a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5894a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5894a-125">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="5894a-125">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="5894a-126">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="5894a-126">Redistributable</span></span><br/>          | <span data-ttu-id="5894a-127">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="5894a-127">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="5894a-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="5894a-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5894a-129"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5894a-129"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="5894a-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5894a-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="5894a-131"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5894a-131"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="5894a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5894a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5894a-133"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5894a-133"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5894a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5894a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5894a-135">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="5894a-135">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="5894a-136">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="5894a-136">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="5894a-137">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="5894a-137">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)
</dt> <dt>

[<span data-ttu-id="5894a-138">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="5894a-138">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)
</dt> <dt>

[<span data-ttu-id="5894a-139">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="5894a-139">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




