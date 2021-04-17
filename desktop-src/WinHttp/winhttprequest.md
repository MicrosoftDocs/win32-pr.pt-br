---
Description: Este tópico fornece informações sobre como usar o objeto COM do WinHTTP WinHttpRequest com linguagens de script.
ms.assetid: 0bbbf3dc-84b8-41d8-8627-e3d80ddcb783
title: Objeto WinHttpRequest
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 907e94a731b2ec150a331347480c461d0d0fa319
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812152"
---
# <a name="winhttprequest-object"></a><span data-ttu-id="d7b44-103">Objeto WinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="d7b44-103">WinHttpRequest object</span></span>

<span data-ttu-id="d7b44-104">Este tópico fornece informações sobre como usar o objeto com do WinHTTP **WinHttpRequest** com linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="d7b44-104">This topic provides information about using the WinHTTP **WinHttpRequest** COM object with scripting languages.</span></span> <span data-ttu-id="d7b44-105">Para obter mais informações, incluindo a API do C++ (WinHTTP), consulte [sobre WinHTTP](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="d7b44-105">For more information, including the C++ API (WinHTTP) please see [About WinHTTP](about-winhttp.md).</span></span> <span data-ttu-id="d7b44-106">Consulte [escolhendo uma interface WinHTTP](choosing-a-winhttp-interface.md) para uma comparação dessas interfaces.</span><span class="sxs-lookup"><span data-stu-id="d7b44-106">See [Choosing a WinHTTP Interface](choosing-a-winhttp-interface.md) for a comparison of these interfaces.</span></span>

## <a name="example"></a><span data-ttu-id="d7b44-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d7b44-107">Example</span></span>

```javascript
// Instantiate a WinHttpRequest object.
var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```

```cpp
 IWinHttpRequest *  pIWinHttpRequest = NULL;
 \\..
    hr = CLSIDFromProgID(L"WinHttp.WinHttpRequest.5.1", &clsid);

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(clsid, NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IWinHttpRequest,
                              (void **)&pIWinHttpRequest);
    }
```

<span data-ttu-id="d7b44-108">Exemplos de código obtidos da [Propriedade IWinHttpRequest:: status](iwinhttprequest-status.md).</span><span class="sxs-lookup"><span data-stu-id="d7b44-108">Code examples taken from [IWinHttpRequest::Status property](iwinhttprequest-status.md).</span></span>



## <a name="members"></a><span data-ttu-id="d7b44-109">Membros</span><span class="sxs-lookup"><span data-stu-id="d7b44-109">Members</span></span>

<span data-ttu-id="d7b44-110">O objeto **WinHttpRequest** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d7b44-110">The **WinHttpRequest** object has these types of members:</span></span>

-   [<span data-ttu-id="d7b44-111">Eventos</span><span class="sxs-lookup"><span data-stu-id="d7b44-111">Events</span></span>](#events)
-   [<span data-ttu-id="d7b44-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7b44-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d7b44-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d7b44-113">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="d7b44-114">Eventos</span><span class="sxs-lookup"><span data-stu-id="d7b44-114">Events</span></span>

<span data-ttu-id="d7b44-115">O objeto **WinHttpRequest** tem esses eventos.</span><span class="sxs-lookup"><span data-stu-id="d7b44-115">The **WinHttpRequest** object has these events.</span></span>



| <span data-ttu-id="d7b44-116">Evento</span><span class="sxs-lookup"><span data-stu-id="d7b44-116">Event</span></span>                                                                            | <span data-ttu-id="d7b44-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7b44-117">Description</span></span>                                                          |
|:---------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [<span data-ttu-id="d7b44-118">**OnError**</span><span class="sxs-lookup"><span data-stu-id="d7b44-118">**OnError**</span></span>](iwinhttprequestevents-onerror.md)                                 | <span data-ttu-id="d7b44-119">Ocorre quando há um erro em tempo de execução no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d7b44-119">Occurs when there is a run-time error in the application.</span></span><br/> |
| [<span data-ttu-id="d7b44-120">**OnResponseDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="d7b44-120">**OnResponseDataAvailable**</span></span>](iwinhttprequestevents-onresponsedataavailable.md) | <span data-ttu-id="d7b44-121">Ocorre quando os dados estão disponíveis da resposta.</span><span class="sxs-lookup"><span data-stu-id="d7b44-121">Occurs when data is available from the response.</span></span><br/>          |
| [<span data-ttu-id="d7b44-122">**OnResponseFinished**</span><span class="sxs-lookup"><span data-stu-id="d7b44-122">**OnResponseFinished**</span></span>](iwinhttprequestevents-onresponsefinished.md)           | <span data-ttu-id="d7b44-123">Ocorre quando os dados da resposta são concluídos.</span><span class="sxs-lookup"><span data-stu-id="d7b44-123">Occurs when the response data is complete.</span></span><br/>                |
| [<span data-ttu-id="d7b44-124">**OnResponseStart**</span><span class="sxs-lookup"><span data-stu-id="d7b44-124">**OnResponseStart**</span></span>](iwinhttprequestevents-onresponsestart.md)                 | <span data-ttu-id="d7b44-125">Ocorre quando os dados de resposta começam a ser recebidos.</span><span class="sxs-lookup"><span data-stu-id="d7b44-125">Occurs when the response data starts to be received.</span></span><br/>      |



 

### <a name="methods"></a><span data-ttu-id="d7b44-126">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7b44-126">Methods</span></span>

<span data-ttu-id="d7b44-127">O objeto **WinHttpRequest** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d7b44-127">The **WinHttpRequest** object has these methods.</span></span>



| <span data-ttu-id="d7b44-128">Método</span><span class="sxs-lookup"><span data-stu-id="d7b44-128">Method</span></span>                                                                 | <span data-ttu-id="d7b44-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7b44-129">Description</span></span>                                                                                                                                                |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7b44-130">**Anular**</span><span class="sxs-lookup"><span data-stu-id="d7b44-130">**Abort**</span></span>](iwinhttprequest-abort.md)                                 | <span data-ttu-id="d7b44-131">Anula um método de [**envio**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="d7b44-131">Aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span><br/>                                                              |
| [<span data-ttu-id="d7b44-132">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="d7b44-132">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md) | <span data-ttu-id="d7b44-133">Recupera todos os cabeçalhos de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="d7b44-133">Retrieves all HTTP response headers.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="d7b44-134">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="d7b44-134">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)         | <span data-ttu-id="d7b44-135">Recupera os cabeçalhos de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="d7b44-135">Retrieves the HTTP response headers.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="d7b44-136">**Aberto**</span><span class="sxs-lookup"><span data-stu-id="d7b44-136">**Open**</span></span>](iwinhttprequest-open.md)                                   | <span data-ttu-id="d7b44-137">Abre uma conexão HTTP para um recurso HTTP.</span><span class="sxs-lookup"><span data-stu-id="d7b44-137">Opens an HTTP connection to an HTTP resource.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="d7b44-138">**Enviar**</span><span class="sxs-lookup"><span data-stu-id="d7b44-138">**Send**</span></span>](iwinhttprequest-send.md)                                   | <span data-ttu-id="d7b44-139">Envia uma solicitação HTTP para um servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="d7b44-139">Sends an HTTP request to an HTTP server.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="d7b44-140">**SetAutoLogonPolicy**</span><span class="sxs-lookup"><span data-stu-id="d7b44-140">**SetAutoLogonPolicy**</span></span>](iwinhttprequest-setautologonpolicy.md)       | <span data-ttu-id="d7b44-141">Define a [política de logon automático](authentication-in-winhttp.md)atual.</span><span class="sxs-lookup"><span data-stu-id="d7b44-141">Sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span><br/>                                                |
| [<span data-ttu-id="d7b44-142">**SetClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="d7b44-142">**SetClientCertificate**</span></span>](iwinhttprequest-setclientcertificate.md)   | <span data-ttu-id="d7b44-143">Seleciona um certificado de cliente para enviar a um servidor HTTPS (protocolo de transferência de hipertexto) seguro.</span><span class="sxs-lookup"><span data-stu-id="d7b44-143">Selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span><br/>                                                    |
| [<span data-ttu-id="d7b44-144">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="d7b44-144">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)               | <span data-ttu-id="d7b44-145">Define as credenciais a serem usadas com um servidor HTTP como uma origem ou um servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="d7b44-145">Sets credentials to be used with an HTTP server either an origin or a proxy server.</span></span><br/>                                                             |
| [<span data-ttu-id="d7b44-146">**SetProxy**</span><span class="sxs-lookup"><span data-stu-id="d7b44-146">**SetProxy**</span></span>](iwinhttprequest-setproxy.md)                           | <span data-ttu-id="d7b44-147">Define informações do servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="d7b44-147">Sets proxy server information.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="d7b44-148">**SetRequestHeader**</span><span class="sxs-lookup"><span data-stu-id="d7b44-148">**SetRequestHeader**</span></span>](iwinhttprequest-setrequestheader.md)           | <span data-ttu-id="d7b44-149">Adiciona, altera ou exclui um cabeçalho de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="d7b44-149">Adds, changes, or deletes an HTTP request header.</span></span><br/>                                                                                               |
| [<span data-ttu-id="d7b44-150">**Settempo_limites**</span><span class="sxs-lookup"><span data-stu-id="d7b44-150">**SetTimeouts**</span></span>](iwinhttprequest-settimeouts.md)                     | <span data-ttu-id="d7b44-151">Especifica, em milissegundos, os componentes de tempo limite individuais de uma operação de envio/recebimento.</span><span class="sxs-lookup"><span data-stu-id="d7b44-151">Specifies, in milliseconds, the individual time-out components of a send/receive operation.</span></span><br/>                                                     |
| [<span data-ttu-id="d7b44-152">**WaitForResponse**</span><span class="sxs-lookup"><span data-stu-id="d7b44-152">**WaitForResponse**</span></span>](iwinhttprequest-waitforresponse.md)             | <span data-ttu-id="d7b44-153">Especifica o tempo de espera, em segundos, para que um método de [**envio**](iwinhttprequest-send.md) assíncrono seja concluído, com valor de tempo limite opcional.</span><span class="sxs-lookup"><span data-stu-id="d7b44-153">Specifies the wait time, in seconds, for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="d7b44-154">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d7b44-154">Properties</span></span>

<span data-ttu-id="d7b44-155">O objeto **WinHttpRequest** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d7b44-155">The **WinHttpRequest** object has these properties.</span></span>



| <span data-ttu-id="d7b44-156">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d7b44-156">Property</span></span>                                                            | <span data-ttu-id="d7b44-157">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="d7b44-157">Access type</span></span>           | <span data-ttu-id="d7b44-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7b44-158">Description</span></span>                                                                     |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="d7b44-159">**Opção**</span><span class="sxs-lookup"><span data-stu-id="d7b44-159">**Option**</span></span>](iwinhttprequest-option.md)<br/>                 | <span data-ttu-id="d7b44-160">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d7b44-160">Read/write</span></span><br/> | <span data-ttu-id="d7b44-161">Define ou recupera um valor de opção de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="d7b44-161">Sets or retrieves a WinHTTP option value.</span></span><br/>                            |
| [<span data-ttu-id="d7b44-162">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="d7b44-162">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)<br/>     | <span data-ttu-id="d7b44-163">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7b44-163">Read-only</span></span><br/>  | <span data-ttu-id="d7b44-164">Recupera o corpo da entidade de resposta como uma matriz de bytes não assinados.</span><span class="sxs-lookup"><span data-stu-id="d7b44-164">Retrieves the response entity body as an array of unsigned bytes.</span></span><br/>    |
| [<span data-ttu-id="d7b44-165">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="d7b44-165">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)<br/> | <span data-ttu-id="d7b44-166">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7b44-166">Read-only</span></span><br/>  | <span data-ttu-id="d7b44-167">Recupera o corpo da entidade de resposta como um [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="d7b44-167">Retrieves the response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span><br/> |
| [<span data-ttu-id="d7b44-168">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="d7b44-168">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)<br/>     | <span data-ttu-id="d7b44-169">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7b44-169">Read-only</span></span><br/>  | <span data-ttu-id="d7b44-170">Recupera o corpo da entidade de resposta como texto.</span><span class="sxs-lookup"><span data-stu-id="d7b44-170">Retrieves the response entity body as text.</span></span><br/>                          |
| [<span data-ttu-id="d7b44-171">**Status**</span><span class="sxs-lookup"><span data-stu-id="d7b44-171">**Status**</span></span>](iwinhttprequest-status.md)<br/>                 | <span data-ttu-id="d7b44-172">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7b44-172">Read-only</span></span><br/>  | <span data-ttu-id="d7b44-173">Recupera o código de status HTTP da última resposta.</span><span class="sxs-lookup"><span data-stu-id="d7b44-173">Retrieves the HTTP status code from the last response.</span></span><br/>               |
| [<span data-ttu-id="d7b44-174">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="d7b44-174">**StatusText**</span></span>](iwinhttprequest-statustext.md)<br/>         | <span data-ttu-id="d7b44-175">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d7b44-175">Read-only</span></span><br/>  | <span data-ttu-id="d7b44-176">Recupera o texto de status HTTP.</span><span class="sxs-lookup"><span data-stu-id="d7b44-176">Retrieves HTTP status text.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="d7b44-177">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7b44-177">Remarks</span></span>

<span data-ttu-id="d7b44-178">O objeto **WinHttpRequest** usa a interface [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) para fornecer dados de erro.</span><span class="sxs-lookup"><span data-stu-id="d7b44-178">The **WinHttpRequest** object uses the [**IErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo) interface to provide error data.</span></span> <span data-ttu-id="d7b44-179">Uma descrição e um valor numérico de erro podem ser obtidos com o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) no Microsoft Visual Basic Scripting Edition (VBScript) e o objeto [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) no Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="d7b44-179">A description and numerical error value can be obtained with the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object in Microsoft Visual Basic Scripting Edition (VBScript), and the [Error](https://msdn.microsoft.com/library/dww52sbt.aspx) object in Microsoft JScript.</span></span> <span data-ttu-id="d7b44-180">Os 16 bits inferiores de um número de erro correspondem aos valores encontrados em [**mensagens de erro**](error-messages.md).</span><span class="sxs-lookup"><span data-stu-id="d7b44-180">The lower 16 bits of an error number correspond to the values found in [**Error Messages**](error-messages.md).</span></span>

> [!Note]  
> <span data-ttu-id="d7b44-181">Para o Windows XP e o Windows 2000, consulte [requisitos de tempo de execução](winhttp-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="d7b44-181">For Windows XP and Windows 2000, see [Run-Time Requirements](winhttp-start-page.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d7b44-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7b44-182">Requirements</span></span>



| <span data-ttu-id="d7b44-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7b44-183">Requirement</span></span> | <span data-ttu-id="d7b44-184">Valor</span><span class="sxs-lookup"><span data-stu-id="d7b44-184">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b44-185">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7b44-185">Minimum supported client</span></span><br/> | <span data-ttu-id="d7b44-186">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="d7b44-186">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="d7b44-187">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7b44-187">Minimum supported server</span></span><br/> | <span data-ttu-id="d7b44-188">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="d7b44-188">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="d7b44-189">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="d7b44-189">Redistributable</span></span><br/>          | <span data-ttu-id="d7b44-190">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d7b44-190">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="d7b44-191">INSERI</span><span class="sxs-lookup"><span data-stu-id="d7b44-191">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7b44-192"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7b44-192"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="d7b44-193">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7b44-193">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7b44-194"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7b44-194"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="d7b44-195">DLL</span><span class="sxs-lookup"><span data-stu-id="d7b44-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7b44-196"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7b44-196"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d7b44-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7b44-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7b44-198">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="d7b44-198">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

