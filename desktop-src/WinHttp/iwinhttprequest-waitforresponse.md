---
description: O método WaitForResponse aguarda a conclusão de um método Send assíncrono, com valor de tempo limite opcional, em segundos.
ms.assetid: 33265710-ecdc-4eae-8822-161dffbd03fc
title: 'Método IWinHttpRequest:: WaitForResponse'
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
ms.openlocfilehash: fe9e3508273a3ee52d72ede65fd6575d72decb8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782286"
---
# <a name="iwinhttprequestwaitforresponse-method"></a><span data-ttu-id="f6052-103">Método IWinHttpRequest:: WaitForResponse</span><span class="sxs-lookup"><span data-stu-id="f6052-103">IWinHttpRequest::WaitForResponse method</span></span>

<span data-ttu-id="f6052-104">O método **WaitForResponse** aguarda a conclusão de um método [**Send**](iwinhttprequest-send.md) assíncrono, com valor de tempo limite opcional, em segundos.</span><span class="sxs-lookup"><span data-stu-id="f6052-104">The **WaitForResponse** method waits for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value, in seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6052-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6052-105">Syntax</span></span>


```C++
HRESULT WaitForResponse(
  [in, optional] VARIANT      Timeout,
  [out, retval]  VARIANT_BOOL *Succeeded
);
```



## <a name="parameters"></a><span data-ttu-id="f6052-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6052-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6052-107">*Tempo limite* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="f6052-107">*Timeout* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f6052-108">Valor de tempo limite, em segundos.</span><span class="sxs-lookup"><span data-stu-id="f6052-108">Time-out value, in seconds.</span></span> <span data-ttu-id="f6052-109">O tempo limite padrão é infinito.</span><span class="sxs-lookup"><span data-stu-id="f6052-109">Default time-out is infinite.</span></span> <span data-ttu-id="f6052-110">Para definir explicitamente o tempo limite para infinito, use o valor-1.</span><span class="sxs-lookup"><span data-stu-id="f6052-110">To explicitly set time-out to infinite, use the value -1.</span></span>

</dd> <dt>

<span data-ttu-id="f6052-111">Com *êxito* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="f6052-111">*Succeeded* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f6052-112">Recebe um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6052-112">Receives one of the following values.</span></span>



| <span data-ttu-id="f6052-113">Valor</span><span class="sxs-lookup"><span data-stu-id="f6052-113">Value</span></span>                                                                                                                                                         | <span data-ttu-id="f6052-114">Significado</span><span class="sxs-lookup"><span data-stu-id="f6052-114">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="VARIANT_TRUE"></span><span id="variant_true"></span><dl> <span data-ttu-id="f6052-115"><dt>**VARIANTE \_ true**</dt></span><span class="sxs-lookup"><span data-stu-id="f6052-115"><dt>**VARIANT\_TRUE**</dt></span></span> </dl>    | <span data-ttu-id="f6052-116">Uma resposta foi recebida.</span><span class="sxs-lookup"><span data-stu-id="f6052-116">A response has been received.</span></span><br/>               |
| <span id="VARIANT_FALSE"></span><span id="variant_false"></span><dl> <span data-ttu-id="f6052-117"><dt>**VARIANTE \_ falso**</dt></span><span class="sxs-lookup"><span data-stu-id="f6052-117"><dt>**VARIANT\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="f6052-118">O período de tempo limite especificado foi excedido.</span><span class="sxs-lookup"><span data-stu-id="f6052-118">The specified time-out period was exceeded.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6052-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f6052-119">Return value</span></span>

<span data-ttu-id="f6052-120">O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="f6052-120">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6052-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6052-121">Remarks</span></span>

<span data-ttu-id="f6052-122">Esse método suspende a execução enquanto aguarda uma resposta a uma solicitação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f6052-122">This method suspends execution while waiting for a response to an asynchronous request.</span></span> <span data-ttu-id="f6052-123">Esse método deve ser chamado após um [**envio**](iwinhttprequest-send.md).</span><span class="sxs-lookup"><span data-stu-id="f6052-123">This method should be called after a [**Send**](iwinhttprequest-send.md).</span></span> <span data-ttu-id="f6052-124">A chamada de aplicativos pode especificar um valor de *tempo limite* opcional, em segundos.</span><span class="sxs-lookup"><span data-stu-id="f6052-124">Calling applications can specify an optional *Timeout* value, in seconds.</span></span> <span data-ttu-id="f6052-125">Se esse método atingir o tempo limite, a solicitação não será anulada.</span><span class="sxs-lookup"><span data-stu-id="f6052-125">If this method times out, the request is not aborted.</span></span> <span data-ttu-id="f6052-126">Dessa forma, o aplicativo de chamada pode continuar aguardando a solicitação, se desejado, em uma chamada subsequente para esse método.</span><span class="sxs-lookup"><span data-stu-id="f6052-126">This way, the calling application can continue to wait for the request, if desired, in a subsequent call to this method.</span></span>

<span data-ttu-id="f6052-127">Chamar essa propriedade após um método [**Send**](iwinhttprequest-send.md) síncrono retorna imediatamente e não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="f6052-127">Calling this property after a synchronous [**Send**](iwinhttprequest-send.md) method returns immediately and has no effect.</span></span>

> [!Note]  
> <span data-ttu-id="f6052-128">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="f6052-128">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="f6052-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f6052-129">Examples</span></span>

<span data-ttu-id="f6052-130">O exemplo a seguir mostra como abrir uma conexão HTTP assíncrona, enviar uma solicitação HTTP, aguardar a resposta e ler o texto da resposta.</span><span class="sxs-lookup"><span data-stu-id="f6052-130">The following example shows how to open an asynchronous HTTP connection, send an HTTP request, wait for the response and read the response text.</span></span>


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



<span data-ttu-id="f6052-131">O exemplo de script a seguir mostra como abrir uma conexão HTTP assíncrona, enviar uma solicitação HTTP, aguardar uma resposta e ler o texto da resposta.</span><span class="sxs-lookup"><span data-stu-id="f6052-131">The following scripting example shows how to open an asynchronous HTTP connection, send an HTTP request, wait for a response, and read the response text.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="f6052-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6052-132">Requirements</span></span>



| <span data-ttu-id="f6052-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6052-133">Requirement</span></span> | <span data-ttu-id="f6052-134">Valor</span><span class="sxs-lookup"><span data-stu-id="f6052-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6052-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6052-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f6052-136">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="f6052-136">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="f6052-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f6052-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f6052-138">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="f6052-138">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="f6052-139">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f6052-139">Redistributable</span></span><br/>          | <span data-ttu-id="f6052-140">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f6052-140">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="f6052-141">INSERI</span><span class="sxs-lookup"><span data-stu-id="f6052-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f6052-142"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f6052-142"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="f6052-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6052-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="f6052-144"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6052-144"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="f6052-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f6052-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6052-146"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6052-146"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f6052-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6052-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6052-148">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="f6052-148">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="f6052-149">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="f6052-149">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="f6052-150">**Abrir**</span><span class="sxs-lookup"><span data-stu-id="f6052-150">**Open**</span></span>](iwinhttprequest-open.md)
</dt> <dt>

[<span data-ttu-id="f6052-151">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="f6052-151">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




