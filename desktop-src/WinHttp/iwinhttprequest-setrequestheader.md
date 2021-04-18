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
# <a name="iwinhttprequestsetrequestheader-method"></a><span data-ttu-id="8ba5a-103">Método IWinHttpRequest:: SetRequestHeader</span><span class="sxs-lookup"><span data-stu-id="8ba5a-103">IWinHttpRequest::SetRequestHeader method</span></span>

<span data-ttu-id="8ba5a-104">O método **SetRequestHeader** adiciona, altera ou exclui um cabeçalho de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-104">The **SetRequestHeader** method adds, changes, or deletes an HTTP request header.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba5a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ba5a-105">Syntax</span></span>


```C++
HRESULT SetRequestHeader(
  [in] BSTR Header,
  [in] BSTR Value
);
```



## <a name="parameters"></a><span data-ttu-id="8ba5a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ba5a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ba5a-107">*Cabeçalho* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8ba5a-107">*Header* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba5a-108">Especifica o nome do cabeçalho a ser definido, por exemplo, "Depth".</span><span class="sxs-lookup"><span data-stu-id="8ba5a-108">Specifies the name of the header to be set, for example, "depth".</span></span> <span data-ttu-id="8ba5a-109">Esse parâmetro não deve conter dois-pontos e deve ser o texto real do cabeçalho HTTP.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-109">This parameter should not contain a colon and must be the actual text of the HTTP header.</span></span>

</dd> <dt>

<span data-ttu-id="8ba5a-110">*Valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8ba5a-110">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ba5a-111">Especifica o valor do cabeçalho, por exemplo, "Infinity".</span><span class="sxs-lookup"><span data-stu-id="8ba5a-111">Specifies the value of the header, for example, "infinity".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ba5a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ba5a-112">Return value</span></span>

<span data-ttu-id="8ba5a-113">O valor de retorno será **S \_ OK** em caso de êxito ou um valor de erro, caso contrário.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-113">The return value is **S\_OK** on success or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba5a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ba5a-114">Remarks</span></span>

<span data-ttu-id="8ba5a-115">Os cabeçalhos são transferidos entre redirecionamentos.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-115">Headers are transferred across redirects.</span></span> <span data-ttu-id="8ba5a-116">Isso pode criar uma vulnerabilidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-116">This can create a security vulnerability.</span></span> <span data-ttu-id="8ba5a-117">Para evitar que os cabeçalhos sejam transferidos se um redirecionamento ocorrer, use o retorno de chamada de [*\_ \_ status do WinHTTP*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) para corrigir os cabeçalhos específicos quando ocorrer um redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-117">To avoid having headers transferred if a redirect occurs, use the [*WINHTTP\_STATUS\_CALLBACK*](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) callback to correct the specific headers when a redirect occurs.</span></span>

<span data-ttu-id="8ba5a-118">O método **SetRequestHeader** permite que o aplicativo de chamada adicione ou exclua um cabeçalho de solicitação HTTP antes de enviar a solicitação.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-118">The **SetRequestHeader** method enables the calling application to add or delete an HTTP request header prior to sending the request.</span></span> <span data-ttu-id="8ba5a-119">O nome do cabeçalho é fornecido no *cabeçalho* e o token ou valor do cabeçalho é fornecido em *valor*.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-119">The header name is given in *Header*, and the header token or value is given in *Value*.</span></span> <span data-ttu-id="8ba5a-120">Para adicionar um cabeçalho, forneça um nome e um valor de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-120">To add a header, supply a header name and value.</span></span> <span data-ttu-id="8ba5a-121">Se outro cabeçalho já existir com esse nome, ele será substituído.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-121">If another header already exists with this name, it is replaced.</span></span> <span data-ttu-id="8ba5a-122">Para excluir um cabeçalho, defina o *cabeçalho* como o nome do cabeçalho a ser excluído e defina o *valor* como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-122">To delete a header, set *Header* to the name of the header to delete and set *Value* to **NULL**.</span></span>

<span data-ttu-id="8ba5a-123">O nome e o valor dos cabeçalhos de solicitação adicionados com esse método são validados.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-123">The name and value of request headers added with this method are validated.</span></span> <span data-ttu-id="8ba5a-124">Os cabeçalhos devem estar bem formados.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-124">Headers must be well formed.</span></span> <span data-ttu-id="8ba5a-125">Para obter mais informações sobre cabeçalhos HTTP válidos, consulte [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span><span class="sxs-lookup"><span data-stu-id="8ba5a-125">For more information about valid HTTP headers, see [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span> <span data-ttu-id="8ba5a-126">Se um cabeçalho inválido for usado, ocorrerá um erro e o cabeçalho não será adicionado.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-126">If an invalid header is used, an error occurs and the header is not added.</span></span>

> [!Note]  
> <span data-ttu-id="8ba5a-127">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-127">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8ba5a-128">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8ba5a-128">Examples</span></span>

<span data-ttu-id="8ba5a-129">O exemplo a seguir mostra como abrir uma conexão HTTP, definir um cabeçalho de solicitação, enviar uma solicitação HTTP e ler o texto da resposta.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-129">The following example shows how to open an HTTP connection, set a request header, send an HTTP request, and read the response text.</span></span> <span data-ttu-id="8ba5a-130">Este exemplo deve ser executado em um prompt de comando.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-130">This example must be run from a command prompt.</span></span>


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



<span data-ttu-id="8ba5a-131">O exemplo de script a seguir mostra como abrir uma conexão HTTP, definir um cabeçalho de solicitação e enviar uma solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-131">The following scripting example shows how to open an HTTP connection, set a request header, and send an HTTP request.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8ba5a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ba5a-132">Requirements</span></span>



| <span data-ttu-id="8ba5a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ba5a-133">Requirement</span></span> | <span data-ttu-id="8ba5a-134">Valor</span><span class="sxs-lookup"><span data-stu-id="8ba5a-134">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba5a-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ba5a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8ba5a-136">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="8ba5a-136">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="8ba5a-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ba5a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8ba5a-138">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="8ba5a-138">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="8ba5a-139">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="8ba5a-139">Redistributable</span></span><br/>          | <span data-ttu-id="8ba5a-140">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8ba5a-140">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="8ba5a-141">INSERI</span><span class="sxs-lookup"><span data-stu-id="8ba5a-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8ba5a-142"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ba5a-142"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="8ba5a-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ba5a-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="8ba5a-144"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ba5a-144"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="8ba5a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8ba5a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ba5a-146"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ba5a-146"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="8ba5a-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ba5a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba5a-148">**IWinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="8ba5a-148">**IWinHttpRequest**</span></span>](iwinhttprequest-interface.md)
</dt> <dt>

[<span data-ttu-id="8ba5a-149">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="8ba5a-149">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="8ba5a-150">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="8ba5a-150">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

