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
# <a name="iwinhttprequestgetresponseheader-method"></a><span data-ttu-id="c32d2-103">Método IWinHttpRequest:: GetResponseHeader</span><span class="sxs-lookup"><span data-stu-id="c32d2-103">IWinHttpRequest::GetResponseHeader method</span></span>

<span data-ttu-id="c32d2-104">O método **getResponseHeader** recupera os cabeçalhos de resposta http.</span><span class="sxs-lookup"><span data-stu-id="c32d2-104">The **GetResponseHeader** method retrieves the HTTP response headers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c32d2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c32d2-105">Syntax</span></span>


```C++
HRESULT GetResponseHeader(
  [in]          BSTR Header,
  [out, retval] BSTR *Value
);
```



## <a name="parameters"></a><span data-ttu-id="c32d2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c32d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c32d2-107">*Cabeçalho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="c32d2-107">*Header* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c32d2-108">Especifica o nome do cabeçalho que não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="c32d2-108">Specifies the case-insensitive header name.</span></span>

</dd> <dt>

<span data-ttu-id="c32d2-109">*Valor* \[ do out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c32d2-109">*Value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c32d2-110">Recebe as informações de cabeçalho resultantes.</span><span class="sxs-lookup"><span data-stu-id="c32d2-110">Receives the resulting header information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c32d2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c32d2-111">Return value</span></span>

<span data-ttu-id="c32d2-112">O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c32d2-112">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c32d2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c32d2-113">Remarks</span></span>

<span data-ttu-id="c32d2-114">Esse método retorna o valor do cabeçalho de resposta chamado em *header*.</span><span class="sxs-lookup"><span data-stu-id="c32d2-114">This method returns the value of the response header named in *Header*.</span></span> <span data-ttu-id="c32d2-115">Lembre-se de que os clientes de automação, como o script, obtêm os dados de cabeçalho como o valor de retorno da chamada de função, não através de um parâmetro de função.</span><span class="sxs-lookup"><span data-stu-id="c32d2-115">Be aware that automation clients, such as script, get the header data as the return value of the function call, not through a function parameter.</span></span> <span data-ttu-id="c32d2-116">Invoque esse método somente depois que o método [**Send**](iwinhttprequest-send.md) tiver sido chamado.</span><span class="sxs-lookup"><span data-stu-id="c32d2-116">Invoke this method only after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="c32d2-117">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="c32d2-117">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c32d2-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c32d2-118">Examples</span></span>

<span data-ttu-id="c32d2-119">O exemplo a seguir mostra como abrir uma conexão HTTP, enviar uma solicitação HTTP e obter o cabeçalho de data da resposta.</span><span class="sxs-lookup"><span data-stu-id="c32d2-119">The following example shows how to open an HTTP connection, send an HTTP request, and get the date header from the response.</span></span> <span data-ttu-id="c32d2-120">Este exemplo deve ser executado em um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="c32d2-120">This example must be run from a command prompt.</span></span>


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



<span data-ttu-id="c32d2-121">O exemplo de script a seguir mostra como abrir uma conexão HTTP, enviar uma solicitação HTTP e obter o cabeçalho de data da resposta.</span><span class="sxs-lookup"><span data-stu-id="c32d2-121">The following scripting example shows how to open an HTTP connection, send an HTTP request, and get the date header from the response.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="c32d2-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c32d2-122">Requirements</span></span>



| <span data-ttu-id="c32d2-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c32d2-123">Requirement</span></span> | <span data-ttu-id="c32d2-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c32d2-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c32d2-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c32d2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c32d2-126">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="c32d2-126">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="c32d2-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c32d2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c32d2-128">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="c32d2-128">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="c32d2-129">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c32d2-129">Redistributable</span></span><br/>          | <span data-ttu-id="c32d2-130">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c32d2-130">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="c32d2-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="c32d2-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c32d2-132"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c32d2-132"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="c32d2-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c32d2-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="c32d2-134"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c32d2-134"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="c32d2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c32d2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c32d2-136"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c32d2-136"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c32d2-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="c32d2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c32d2-138">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="c32d2-138">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="c32d2-139">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="c32d2-139">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="c32d2-140">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="c32d2-140">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md)
</dt> <dt>

[<span data-ttu-id="c32d2-141">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="c32d2-141">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




