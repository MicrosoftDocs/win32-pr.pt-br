---
description: Define as credenciais a serem usadas com um servidor HTTP, seja um servidor proxy ou um servidor de origem.
ms.assetid: d96c6e76-92b8-4ad7-8ca7-a9acbed523ff
title: 'Método IWinHttpRequest:: SetCredentials'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest.SetCredentials
- WinHttpRequest.SetCredentials
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 46b0dfb321763a3b3bfe622e116f2e76c5e59423
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765322"
---
# <a name="iwinhttprequestsetcredentials-method"></a><span data-ttu-id="45547-103">Método IWinHttpRequest:: SetCredentials</span><span class="sxs-lookup"><span data-stu-id="45547-103">IWinHttpRequest::SetCredentials method</span></span>

<span data-ttu-id="45547-104">O método **SetCredentials** define as credenciais a serem usadas com um servidor http, seja um servidor proxy ou um servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="45547-104">The **SetCredentials** method sets credentials to be used with an HTTP server, whether it is a proxy server or an originating server.</span></span>

## <a name="syntax"></a><span data-ttu-id="45547-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45547-105">Syntax</span></span>


```C++
HRESULT SetCredentials(
  [in] BSTR                             UserName,
  [in] BSTR                             Password,
  [in] HTTPREQUEST_SETCREDENTIALS_FLAGS Flags
);
```



## <a name="parameters"></a><span data-ttu-id="45547-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45547-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45547-107">*Nome de usuário* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45547-107">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45547-108">Especifica o nome de usuário para autenticação.</span><span class="sxs-lookup"><span data-stu-id="45547-108">Specifies the user name for authentication.</span></span>

</dd> <dt>

<span data-ttu-id="45547-109">*Senha* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="45547-109">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45547-110">Especifica a senha para autenticação.</span><span class="sxs-lookup"><span data-stu-id="45547-110">Specifies the password for authentication.</span></span> <span data-ttu-id="45547-111">Esse parâmetro será ignorado se *bstrUserName* for **nulo** ou estiver ausente.</span><span class="sxs-lookup"><span data-stu-id="45547-111">This parameter is ignored if *bstrUserName* is **NULL** or missing.</span></span>

</dd> <dt>

<span data-ttu-id="45547-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="45547-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45547-113">Especifica quando [**IWinHttpRequest**](iwinhttprequest-interface.md) usa credenciais.</span><span class="sxs-lookup"><span data-stu-id="45547-113">Specifies when [**IWinHttpRequest**](iwinhttprequest-interface.md) uses credentials.</span></span> <span data-ttu-id="45547-114">Pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="45547-114">Can be one of the following values.</span></span>



| <span data-ttu-id="45547-115">Valor</span><span class="sxs-lookup"><span data-stu-id="45547-115">Value</span></span>                                                                                                               | <span data-ttu-id="45547-116">Significado</span><span class="sxs-lookup"><span data-stu-id="45547-116">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="45547-117"><dt>HTTPREQUEST \_ SETcredentials \_ para o \_ servidor</dt></span><span class="sxs-lookup"><span data-stu-id="45547-117"><dt>HTTPREQUEST\_SETCREDENTIALS\_FOR\_SERVER</dt></span></span> </dl> | <span data-ttu-id="45547-118">As credenciais são passadas para um servidor.</span><span class="sxs-lookup"><span data-stu-id="45547-118">Credentials are passed to a server.</span></span><br/> |
| <dl> <span data-ttu-id="45547-119"><dt>HTTPREQUEST \_ SETcredentials \_ para o \_ proxy</dt></span><span class="sxs-lookup"><span data-stu-id="45547-119"><dt>HTTPREQUEST\_SETCREDENTIALS\_FOR\_PROXY</dt></span></span> </dl>  | <span data-ttu-id="45547-120">As credenciais são passadas para um proxy.</span><span class="sxs-lookup"><span data-stu-id="45547-120">Credentials are passed to a proxy.</span></span><br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45547-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45547-121">Return value</span></span>

<span data-ttu-id="45547-122">O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="45547-122">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="45547-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="45547-123">Remarks</span></span>

<span data-ttu-id="45547-124">Esse método retornará um valor de erro se uma chamada para [**abrir**](iwinhttprequest-open.md) não tiver sido concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="45547-124">This method returns an error value if a call to [**Open**](iwinhttprequest-open.md) has not completed successfully.</span></span> <span data-ttu-id="45547-125">Supõe-se que alguma medida de interação com um servidor proxy ou servidor de origem deve ocorrer antes que os usuários possam definir credenciais para a sessão.</span><span class="sxs-lookup"><span data-stu-id="45547-125">It is assumed that some measure of interaction with a proxy server or origin server must occur before users can set credentials for the session.</span></span> <span data-ttu-id="45547-126">Além disso, até que os usuários saibam quais esquemas de autenticação têm suporte, eles não podem formatar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="45547-126">Moreover, until users know which authentication scheme(s) are supported, they cannot format the credentials.</span></span>

> [!Note]  
> <span data-ttu-id="45547-127">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="45547-127">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

<span data-ttu-id="45547-128">Para autenticar com o servidor e o proxy, o aplicativo deve chamar **SetCredentials** duas vezes; Primeiro, com o parâmetro *flags* definido como **HttpRequest \_ SetCredentials \_ para \_ Server** e Second, com o parâmetro *flags* definido como **HttpRequest \_ SetCredentials \_ para \_ proxy**.</span><span class="sxs-lookup"><span data-stu-id="45547-128">To authenticate with both the server and the proxy, the application must call **SetCredentials** twice; first with the *Flags* parameter set to **HTTPREQUEST\_SETCREDENTIALS\_FOR\_SERVER**, and second, with the *Flags* parameter set to **HTTPREQUEST\_SETCREDENTIALS\_FOR\_PROXY**.</span></span>

## <a name="examples"></a><span data-ttu-id="45547-129">Exemplos</span><span class="sxs-lookup"><span data-stu-id="45547-129">Examples</span></span>

<span data-ttu-id="45547-130">O exemplo a seguir mostra como abrir uma conexão HTTP, definir credenciais para o servidor, enviar uma solicitação HTTP e ler o texto da resposta.</span><span class="sxs-lookup"><span data-stu-id="45547-130">The following example shows how to open an HTTP connection, set credentials for the server, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="45547-131">Este exemplo deve ser executado em um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="45547-131">This example must be run from a command prompt.</span></span>


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
        BSTR bstrMethod = SysAllocString(L"GET");
        BSTR bstrUrl = SysAllocString(L"https://microsoft.com");
        hr = pIWinHttpRequest->Open(bstrMethod, bstrUrl, varFalse);
        SysFreeString(bstrMethod);
        SysFreeString(bstrUrl);
    }
    if (SUCCEEDED(hr))
    {    // Set Credentials.
        BSTR bstrUserName = SysAllocString(L"User Name");
        BSTR bstrPassword = SysAllocString(L"Password");
        hr = pIWinHttpRequest->SetCredentials(
                               bstrUserName,
                               bstrPassword,
                               HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);
        SysFreeString(bstrUserName);
        SysFreeString(bstrPassword);
    }
    if (SUCCEEDED(hr))
    {    // Send Request.
        hr = pIWinHttpRequest->Send(varEmpty);
    }
    if (SUCCEEDED(hr))
    {    // Get Response text.
        hr = pIWinHttpRequest->get_ResponseText(&bstrResponse);
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



<span data-ttu-id="45547-132">O exemplo de script a seguir mostra como abrir uma conexão HTTP, definir credenciais para o servidor, definir credenciais para um proxy, se um for usado, enviar uma solicitação HTTP e ler o texto da resposta.</span><span class="sxs-lookup"><span data-stu-id="45547-132">The following scripting example shows how to open an HTTP connection, set credentials for the server, set credentials for a proxy if one is used, send an HTTP request, and read the response text.</span></span>


```JScript
// HttpRequest SetCredentials flags
HTTPREQUEST_SETCREDENTIALS_FOR_SERVER = 0;
HTTPREQUEST_SETCREDENTIALS_FOR_PROXY = 1;

// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");

// Specify the target resource.
var targURL = "https://msdn.microsoft.com/downloads/samples/"+
              "internet/winhttp/auth/authenticate.asp";    
WinHttpReq.open("GET", targURL, false);

var Done = false;
var LastStatus=0;
do {
    // Send a request to the server and wait for a response.                               
    WinHttpReq.send(); 
    
    // Obtain the status code from the response.
    var Status = WinHttpReq.Status;

    switch (Status){
        // A 200 status indicates that the resource was retrieved.
        case 200:
            Done = true;
            break;
                
        // A 401 status indicates that the server 
        // requires authentication.    
        case 401:
            WScript.Echo("Requires Server UserName and Password.");

            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
                            
            // Set credentials for the server.
            WinHttpReq.SetCredentials("User Name", "Password", 
                        HTTPREQUEST_SETCREDENTIALS_FOR_SERVER);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==401)
                Done = true;
            break;

        // A 407 status indicates that the proxy 
        // requires authentication.    
        case 407:
            WScript.Echo("Requires Proxy UserName and Password.");
                
            // Specify the target resource.
            WinHttpReq.open("GET", targURL, false);
    
            // Set credentials for the proxy.
            WinHttpReq.SetCredentials("User Name", "Password", 
                HTTPREQUEST_SETCREDENTIALS_FOR_PROXY);

            // If the same credentials are requested twice, abort 
            // the request.  For simplicity, this sample does not 
            // check for a repeated sequence of status codes.
            if (LastStatus==407)
                Done = true;
            break;
        
        // Any other status is unexpected.
        default:
            WScript.Echo("Unexpected Status: "+Status);
            Done = true;
            break;
    }
    
    // Keep track of the last status code.
    LastStatus = Status;
    
} while (!Done);

// Display the results of the request.
WScript.Echo(WinHttpReq.Status + "   " + WinHttpReq.StatusText);
WScript.Echo(WinHttpReq.GetAllResponseHeaders());
```



## <a name="requirements"></a><span data-ttu-id="45547-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45547-133">Requirements</span></span>



| <span data-ttu-id="45547-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="45547-134">Requirement</span></span> | <span data-ttu-id="45547-135">Valor</span><span class="sxs-lookup"><span data-stu-id="45547-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="45547-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45547-136">Minimum supported client</span></span><br/> | <span data-ttu-id="45547-137">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="45547-137">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="45547-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45547-138">Minimum supported server</span></span><br/> | <span data-ttu-id="45547-139">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="45547-139">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="45547-140">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="45547-140">Redistributable</span></span><br/>          | <span data-ttu-id="45547-141">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="45547-141">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="45547-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="45547-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="45547-143"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="45547-143"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="45547-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45547-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="45547-145"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45547-145"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="45547-146">DLL</span><span class="sxs-lookup"><span data-stu-id="45547-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45547-147"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45547-147"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="45547-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="45547-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45547-149">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="45547-149">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="45547-150">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="45547-150">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="45547-151">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="45547-151">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




