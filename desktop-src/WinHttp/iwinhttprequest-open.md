---
description: Abre uma conexão HTTP para um recurso HTTP.
ms.assetid: 5207e873-44c0-4eeb-9db8-d8b69432070c
title: 'Método IWinHttpRequest:: Open'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.Open
- WinHttpRequest.Open
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 5543832eb1ebc3df210237eff71d415de14b2f62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763236"
---
# <a name="iwinhttprequestopen-method"></a><span data-ttu-id="29fdc-103">Método IWinHttpRequest:: Open</span><span class="sxs-lookup"><span data-stu-id="29fdc-103">IWinHttpRequest::Open method</span></span>

<span data-ttu-id="29fdc-104">O método **Open** abre uma conexão HTTP para um recurso http.</span><span class="sxs-lookup"><span data-stu-id="29fdc-104">The **Open** method opens an HTTP connection to an HTTP resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="29fdc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29fdc-105">Syntax</span></span>


```C++
HRESULT Open(
  [in]           BSTR    Method,
  [in]           BSTR    Url,
  [in, optional] VARIANT Async
);
```



## <a name="parameters"></a><span data-ttu-id="29fdc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29fdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29fdc-107">*Método* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="29fdc-107">*Method* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29fdc-108">Especifica o [*verbo http*](glossary.md) usado para o método **Open** , como "Get" ou "Put".</span><span class="sxs-lookup"><span data-stu-id="29fdc-108">Specifies the [*HTTP verb*](glossary.md) used for the **Open** method, such as "GET" or "PUT".</span></span> <span data-ttu-id="29fdc-109">Sempre use maiúsculas, pois alguns servidores ignoram o *verbo http* s minúsculos.</span><span class="sxs-lookup"><span data-stu-id="29fdc-109">Always use uppercase as some servers ignore lowercase *HTTP verb* s.</span></span>

</dd> <dt>

<span data-ttu-id="29fdc-110">*URL* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="29fdc-110">*Url* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29fdc-111">Especifica o nome do recurso.</span><span class="sxs-lookup"><span data-stu-id="29fdc-111">Specifies the name of the resource.</span></span> <span data-ttu-id="29fdc-112">Deve ser uma URL absoluta.</span><span class="sxs-lookup"><span data-stu-id="29fdc-112">This must be an absolute URL.</span></span>

</dd> <dt>

<span data-ttu-id="29fdc-113">*Async* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="29fdc-113">*Async* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29fdc-114">Indica se o modo assíncrono deve ser aberto.</span><span class="sxs-lookup"><span data-stu-id="29fdc-114">Indicates whether to open in asynchronous mode.</span></span>



| <span data-ttu-id="29fdc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="29fdc-115">Value</span></span>                                                                                                                                                         | <span data-ttu-id="29fdc-116">Significado</span><span class="sxs-lookup"><span data-stu-id="29fdc-116">Meaning</span></span>                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <span data-ttu-id="29fdc-117"><dt>**VARIANTE \_ falso**</dt></span><span class="sxs-lookup"><span data-stu-id="29fdc-117"><dt>**VARIANT\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="29fdc-118">Abre a conexão HTTP no modo síncrono.</span><span class="sxs-lookup"><span data-stu-id="29fdc-118">Opens the HTTP connection in synchronous mode.</span></span> <span data-ttu-id="29fdc-119">Uma chamada para [**Send**](iwinhttprequest-send.md) não retorna até que o [WinHTTP](about-winhttp.md) tenha recebido completamente a resposta.</span><span class="sxs-lookup"><span data-stu-id="29fdc-119">A call to [**Send**](iwinhttprequest-send.md) does not return until [WinHTTP](about-winhttp.md) has completely received the response.</span></span><br/> |
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <span data-ttu-id="29fdc-120"><dt>**VARIANTE \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="29fdc-120"><dt>**VARIANT\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="29fdc-121">Abre a conexão HTTP no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="29fdc-121">Opens the HTTP connection in asynchronous mode.</span></span><br/>                                                                                                                                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29fdc-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="29fdc-122">Return value</span></span>

<span data-ttu-id="29fdc-123">O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="29fdc-123">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="29fdc-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="29fdc-124">Remarks</span></span>

<span data-ttu-id="29fdc-125">Esse método abre uma conexão com o recurso identificado na *URL* usando o [*verbo http*](glossary.md) fornecido no *método*.</span><span class="sxs-lookup"><span data-stu-id="29fdc-125">This method opens a connection to the resource identified in *Url* using the [*HTTP verb*](glossary.md) given in *Method*.</span></span>

> [!Note]  
> <span data-ttu-id="29fdc-126">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="29fdc-126">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="29fdc-127">Exemplos</span><span class="sxs-lookup"><span data-stu-id="29fdc-127">Examples</span></span>

<span data-ttu-id="29fdc-128">O exemplo a seguir mostra como abrir uma conexão HTTP, enviar uma solicitação HTTP e ler o texto da resposta.</span><span class="sxs-lookup"><span data-stu-id="29fdc-128">The following example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
    }
    if (SUCCEEDED(hr))
    {
        // Print the response to a console.
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



<span data-ttu-id="29fdc-129">O exemplo de script a seguir mostra como abrir uma conexão HTTP, enviar uma solicitação HTTP e ler o texto da resposta.</span><span class="sxs-lookup"><span data-stu-id="29fdc-129">The following scripting example shows how to open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="29fdc-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29fdc-130">Requirements</span></span>



| <span data-ttu-id="29fdc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="29fdc-131">Requirement</span></span> | <span data-ttu-id="29fdc-132">Valor</span><span class="sxs-lookup"><span data-stu-id="29fdc-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="29fdc-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29fdc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="29fdc-134">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="29fdc-134">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="29fdc-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29fdc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="29fdc-136">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="29fdc-136">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="29fdc-137">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="29fdc-137">Redistributable</span></span><br/>          | <span data-ttu-id="29fdc-138">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="29fdc-138">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="29fdc-139">INSERI</span><span class="sxs-lookup"><span data-stu-id="29fdc-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="29fdc-140"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="29fdc-140"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="29fdc-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="29fdc-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="29fdc-142"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="29fdc-142"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="29fdc-143">DLL</span><span class="sxs-lookup"><span data-stu-id="29fdc-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29fdc-144"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29fdc-144"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="29fdc-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="29fdc-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29fdc-146">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="29fdc-146">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="29fdc-147">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="29fdc-147">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="29fdc-148">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="29fdc-148">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




