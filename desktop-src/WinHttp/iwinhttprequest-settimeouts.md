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
# <a name="iwinhttprequestsettimeouts-method"></a><span data-ttu-id="3be93-103">Método IWinHttpRequest:: settempo_limites</span><span class="sxs-lookup"><span data-stu-id="3be93-103">IWinHttpRequest::SetTimeouts method</span></span>

<span data-ttu-id="3be93-104">O método **Settempo_limites** especifica os componentes de tempo limite individuais de uma operação de envio/recebimento, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="3be93-104">The **SetTimeouts** method specifies the individual time-out components of a send/receive operation, in milliseconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="3be93-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3be93-105">Syntax</span></span>


```C++
HRESULT SetTimeouts(
  [in] long ResolveTimeout,
  [in] long ConnectTimeout,
  [in] long SendTimeout,
  [in] long ReceiveTimeout
);
```



## <a name="parameters"></a><span data-ttu-id="3be93-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3be93-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3be93-107">*ResolveTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3be93-107">*ResolveTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3be93-108">Valor de tempo limite aplicado ao resolver um nome de host (como `www.microsoft.com` ) para um endereço IP (como 192.168.131.199), em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="3be93-108">Time-out value applied when resolving a host name (such as `www.microsoft.com`) to an IP address (such as 192.168.131.199), in milliseconds.</span></span> <span data-ttu-id="3be93-109">O valor padrão é zero, o que significa que não há tempo limite (infinito).</span><span class="sxs-lookup"><span data-stu-id="3be93-109">The default value is zero, meaning no time-out (infinite).</span></span> <span data-ttu-id="3be93-110">Se o tempo limite do DNS for especificado usando \_ \_ o tempo limite de resolução de nome, haverá uma sobrecarga de um thread por solicitação.</span><span class="sxs-lookup"><span data-stu-id="3be93-110">If DNS timeout is specified using NAME\_RESOLUTION\_TIMEOUT, there is an overhead of one thread per request.</span></span>

</dd> <dt>

<span data-ttu-id="3be93-111">*ConnectTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3be93-111">*ConnectTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3be93-112">Valor de tempo limite aplicado ao estabelecer um soquete de comunicação com o servidor de destino, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="3be93-112">Time-out value applied when establishing a communication socket with the target server, in milliseconds.</span></span> <span data-ttu-id="3be93-113">O valor padrão é 60.000 (60 segundos).</span><span class="sxs-lookup"><span data-stu-id="3be93-113">The default value is 60,000 (60 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="3be93-114">*SendTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3be93-114">*SendTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3be93-115">Valor de tempo limite aplicado ao enviar um pacote individual de dados de solicitação no soquete de comunicação para o servidor de destino, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="3be93-115">Time-out value applied when sending an individual packet of request data on the communication socket to the target server, in milliseconds.</span></span> <span data-ttu-id="3be93-116">Uma solicitação grande enviada a um servidor HTTP normalmente é dividida em vários pacotes; o tempo limite de envio se aplica ao envio individual de cada pacote.</span><span class="sxs-lookup"><span data-stu-id="3be93-116">A large request sent to an HTTP server are normally be broken up into multiple packets; the send time-out applies to sending each packet individually.</span></span> <span data-ttu-id="3be93-117">O valor padrão é 30.000 (30 segundos).</span><span class="sxs-lookup"><span data-stu-id="3be93-117">The default value is 30,000 (30 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="3be93-118">*ReceiveTimeout* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3be93-118">*ReceiveTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3be93-119">Valor de tempo limite aplicado ao receber um pacote de dados de resposta do servidor de destino, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="3be93-119">Time-out value applied when receiving a packet of response data from the target server, in milliseconds.</span></span> <span data-ttu-id="3be93-120">As respostas grandes são divididas em vários pacotes; o tempo limite de recebimento se aplica à busca de cada pacote de dados fora do soquete.</span><span class="sxs-lookup"><span data-stu-id="3be93-120">Large responses are be broken up into multiple packets; the receive time-out applies to fetching each packet of data off the socket.</span></span> <span data-ttu-id="3be93-121">O valor padrão é 30.000 (30 segundos).</span><span class="sxs-lookup"><span data-stu-id="3be93-121">The default value is 30,000 (30 seconds).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3be93-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3be93-122">Return value</span></span>

<span data-ttu-id="3be93-123">O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3be93-123">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3be93-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="3be93-124">Remarks</span></span>

<span data-ttu-id="3be93-125">Todos os parâmetros são obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3be93-125">All parameters are required.</span></span> <span data-ttu-id="3be93-126">Um valor de 0 ou-1 define um tempo limite para aguardar infinitamente.</span><span class="sxs-lookup"><span data-stu-id="3be93-126">A value of 0 or -1 sets a time-out to wait infinitely.</span></span> <span data-ttu-id="3be93-127">Um valor maior que 0 define o valor de tempo limite em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="3be93-127">A value greater than 0 sets the time-out value in milliseconds.</span></span> <span data-ttu-id="3be93-128">Por exemplo, 30.000 definiria o tempo limite para 30 segundos.</span><span class="sxs-lookup"><span data-stu-id="3be93-128">For example, 30,000 would set the time-out to 30 seconds.</span></span> <span data-ttu-id="3be93-129">Todos os valores negativos diferentes de-1 causam a falha desse método.</span><span class="sxs-lookup"><span data-stu-id="3be93-129">All negative values other than -1 cause this method to fail.</span></span>

<span data-ttu-id="3be93-130">Os valores de tempo limite são aplicados na camada do Winsock.</span><span class="sxs-lookup"><span data-stu-id="3be93-130">Time-out values are applied at the Winsock layer.</span></span>

> [!Note]  
> <span data-ttu-id="3be93-131">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="3be93-131">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="3be93-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="3be93-132">Examples</span></span>

<span data-ttu-id="3be93-133">O exemplo a seguir mostra como definir todos os tempos limite de WinHTTP para 30 segundos, abrir uma conexão HTTP, enviar uma solicitação HTTP e ler o texto da resposta.</span><span class="sxs-lookup"><span data-stu-id="3be93-133">The following example shows how to set all WinHTTP time-outs to 30 seconds, open an HTTP connection, send an HTTP request, and read the response text.</span></span>


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



<span data-ttu-id="3be93-134">O exemplo de script a seguir mostra como definir todos os tempos limite de WinHTTP para 30 segundos, abrir uma conexão HTTP e enviar uma solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="3be93-134">The following scripting example shows how to set all WinHTTP time-outs to 30 seconds, open an HTTP connection, and send an HTTP request.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3be93-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3be93-135">Requirements</span></span>



| <span data-ttu-id="3be93-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3be93-136">Requirement</span></span> | <span data-ttu-id="3be93-137">Valor</span><span class="sxs-lookup"><span data-stu-id="3be93-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3be93-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3be93-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3be93-139">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="3be93-139">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="3be93-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3be93-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3be93-141">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="3be93-141">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="3be93-142">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="3be93-142">Redistributable</span></span><br/>          | <span data-ttu-id="3be93-143">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3be93-143">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="3be93-144">INSERI</span><span class="sxs-lookup"><span data-stu-id="3be93-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3be93-145"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3be93-145"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="3be93-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3be93-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="3be93-147"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3be93-147"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="3be93-148">DLL</span><span class="sxs-lookup"><span data-stu-id="3be93-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3be93-149"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3be93-149"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3be93-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="3be93-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3be93-151">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="3be93-151">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="3be93-152">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="3be93-152">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="3be93-153">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3be93-153">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




