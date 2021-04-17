---
description: Recupera todos os cabeçalhos de resposta HTTP.
ms.assetid: 68b13d4c-5afd-486d-8b78-a7eef0f59a24
title: 'Método IWinHttpRequest:: GetAllResponseHeaders'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.GetAllResponseHeaders
- WinHttpRequest.GetAllResponseHeaders
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 74c113216cf41e2f9816176dd28ba5e84208c635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749545"
---
# <a name="iwinhttprequestgetallresponseheaders-method"></a><span data-ttu-id="7ef6c-103">Método IWinHttpRequest:: GetAllResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="7ef6c-103">IWinHttpRequest::GetAllResponseHeaders method</span></span>

<span data-ttu-id="7ef6c-104">O método **GetAllResponseHeaders** recupera todos os cabeçalhos de resposta http.</span><span class="sxs-lookup"><span data-stu-id="7ef6c-104">The **GetAllResponseHeaders** method retrieves all HTTP response headers.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ef6c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ef6c-105">Syntax</span></span>


```C++
HRESULT GetAllResponseHeaders(
  [out, retval] BSTR *Headers
);
```



## <a name="parameters"></a><span data-ttu-id="7ef6c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ef6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ef6c-107">*Cabeçalhos* \[ de out, retval\]</span><span class="sxs-lookup"><span data-stu-id="7ef6c-107">*Headers* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7ef6c-108">Recebe as informações de cabeçalho resultantes.</span><span class="sxs-lookup"><span data-stu-id="7ef6c-108">Receives the resulting header information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ef6c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ef6c-109">Return value</span></span>

<span data-ttu-id="7ef6c-110">O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7ef6c-110">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ef6c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ef6c-111">Remarks</span></span>

<span data-ttu-id="7ef6c-112">Esse método retorna todos os cabeçalhos contidos na resposta mais recente do servidor.</span><span class="sxs-lookup"><span data-stu-id="7ef6c-112">This method returns all of the headers contained in the most recent server response.</span></span> <span data-ttu-id="7ef6c-113">Os cabeçalhos individuais são delimitados por uma combinação de retorno de carro e alimentação de linha (ASCII 13 e 10).</span><span class="sxs-lookup"><span data-stu-id="7ef6c-113">The individual headers are delimited by a carriage return and line feed combination (ASCII 13 and 10).</span></span> <span data-ttu-id="7ef6c-114">A última entrada é seguida por dois delimitadores (13, 10, 13, 10).</span><span class="sxs-lookup"><span data-stu-id="7ef6c-114">The last entry is followed by two delimiters (13, 10, 13, 10).</span></span> <span data-ttu-id="7ef6c-115">Invoque esse método somente depois que o método [**Send**](iwinhttprequest-send.md) tiver sido chamado.</span><span class="sxs-lookup"><span data-stu-id="7ef6c-115">Invoke this method only after the [**Send**](iwinhttprequest-send.md) method has been called.</span></span>

> [!Note]  
> <span data-ttu-id="7ef6c-116">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7ef6c-116">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="7ef6c-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7ef6c-117">Examples</span></span>

<span data-ttu-id="7ef6c-118">O exemplo a seguir mostra como abrir uma conexão HTTP, enviar uma solicitação HTTP e obter todos os cabeçalhos da resposta.</span><span class="sxs-lookup"><span data-stu-id="7ef6c-118">The following example shows how to open an HTTP connection, send an HTTP request, and get all of the headers from the response.</span></span> <span data-ttu-id="7ef6c-119">Este exemplo deve ser executado em um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="7ef6c-119">This example should be run from a command prompt.</span></span>


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

int main(int argc, char* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);

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
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
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



<span data-ttu-id="7ef6c-120">O exemplo de script a seguir mostra como abrir uma conexão HTTP, enviar uma solicitação HTTP e obter todos os cabeçalhos da resposta.</span><span class="sxs-lookup"><span data-stu-id="7ef6c-120">The following scripting example shows how to open an HTTP connection, send an HTTP request, and get all of the headers from the response.</span></span>


```JScript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Initialize an HTTP request.  
WinHttpReq.Open("GET", "https://www.microsoft.com", false);

// Send the HTTP request.
WinHttpReq.Send(); 

// Get all response headers.
WScript.Echo( WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="7ef6c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ef6c-121">Requirements</span></span>



| <span data-ttu-id="7ef6c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ef6c-122">Requirement</span></span> | <span data-ttu-id="7ef6c-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7ef6c-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ef6c-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ef6c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7ef6c-125">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="7ef6c-125">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="7ef6c-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ef6c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7ef6c-127">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="7ef6c-127">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="7ef6c-128">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7ef6c-128">Redistributable</span></span><br/>          | <span data-ttu-id="7ef6c-129">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7ef6c-129">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="7ef6c-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="7ef6c-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ef6c-131"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ef6c-131"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="7ef6c-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ef6c-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ef6c-133"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ef6c-133"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="7ef6c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7ef6c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ef6c-135"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ef6c-135"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7ef6c-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ef6c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ef6c-137">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="7ef6c-137">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="7ef6c-138">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="7ef6c-138">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="7ef6c-139">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="7ef6c-139">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)
</dt> <dt>

[<span data-ttu-id="7ef6c-140">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7ef6c-140">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




