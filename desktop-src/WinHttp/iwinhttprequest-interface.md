---
description: A interface IWinHttpRequest fornece todos os métodos não uniformes para o Microsoft Windows HTTP Services (WinHTTP).
ms.assetid: 6417b3b5-b74a-4c7b-acf9-87e2e814a4df
title: Interface IWinHttpRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWinHttpRequest
api_type:
- COM
api_location:
- Winhttp.dll
ms.openlocfilehash: 77ebc8947ad36d2dc9efba121cdd6da2d6de359b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169816"
---
# <a name="iwinhttprequest-interface"></a><span data-ttu-id="7850b-103">Interface IWinHttpRequest</span><span class="sxs-lookup"><span data-stu-id="7850b-103">IWinHttpRequest interface</span></span>

<span data-ttu-id="7850b-104">A interface **IWinHttpRequest** fornece todos os métodos não uniformes para [o Microsoft Windows http Services (WinHTTP)](about-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="7850b-104">The **IWinHttpRequest** interface provides all of the nonevent methods for [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md).</span></span>

## <a name="members"></a><span data-ttu-id="7850b-105">Membros</span><span class="sxs-lookup"><span data-stu-id="7850b-105">Members</span></span>

<span data-ttu-id="7850b-106">A interface **IWinHttpRequest** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7850b-106">The **IWinHttpRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7850b-107">**IWinHttpRequest** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7850b-107">**IWinHttpRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="7850b-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="7850b-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="7850b-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7850b-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7850b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="7850b-110">Methods</span></span>

<span data-ttu-id="7850b-111">A interface **IWinHttpRequest** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="7850b-111">The **IWinHttpRequest** interface has these methods.</span></span>



| <span data-ttu-id="7850b-112">Método</span><span class="sxs-lookup"><span data-stu-id="7850b-112">Method</span></span>                                                                 | <span data-ttu-id="7850b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="7850b-113">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7850b-114">**Anular**</span><span class="sxs-lookup"><span data-stu-id="7850b-114">**Abort**</span></span>](iwinhttprequest-abort.md)                                 | <span data-ttu-id="7850b-115">Anula um método de [**envio**](iwinhttprequest-send.md) [WinHTTP](about-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="7850b-115">Aborts a [WinHTTP](about-winhttp.md) [**Send**](iwinhttprequest-send.md) method.</span></span><br/>                                           |
| [<span data-ttu-id="7850b-116">**GetAllResponseHeaders**</span><span class="sxs-lookup"><span data-stu-id="7850b-116">**GetAllResponseHeaders**</span></span>](iwinhttprequest-getallresponseheaders.md) | <span data-ttu-id="7850b-117">Recupera todos os cabeçalhos de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="7850b-117">Retrieves all HTTP response headers.</span></span><br/>                                                                                         |
| [<span data-ttu-id="7850b-118">**GetResponseHeader**</span><span class="sxs-lookup"><span data-stu-id="7850b-118">**GetResponseHeader**</span></span>](iwinhttprequest-getresponseheader.md)         | <span data-ttu-id="7850b-119">Recupera os cabeçalhos de resposta HTTP.</span><span class="sxs-lookup"><span data-stu-id="7850b-119">Retrieves the HTTP response headers.</span></span><br/>                                                                                         |
| [<span data-ttu-id="7850b-120">**Aberto**</span><span class="sxs-lookup"><span data-stu-id="7850b-120">**Open**</span></span>](iwinhttprequest-open.md)                                   | <span data-ttu-id="7850b-121">Abre uma conexão HTTP para um recurso HTTP.</span><span class="sxs-lookup"><span data-stu-id="7850b-121">Opens an HTTP connection to an HTTP resource.</span></span><br/>                                                                                |
| [<span data-ttu-id="7850b-122">**Enviar**</span><span class="sxs-lookup"><span data-stu-id="7850b-122">**Send**</span></span>](iwinhttprequest-send.md)                                   | <span data-ttu-id="7850b-123">Envia uma solicitação HTTP para um servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="7850b-123">Sends an HTTP request to an HTTP server.</span></span><br/>                                                                                     |
| [<span data-ttu-id="7850b-124">**SetAutoLogonPolicy**</span><span class="sxs-lookup"><span data-stu-id="7850b-124">**SetAutoLogonPolicy**</span></span>](iwinhttprequest-setautologonpolicy.md)       | <span data-ttu-id="7850b-125">Define a [política de logon automático](authentication-in-winhttp.md)atual.</span><span class="sxs-lookup"><span data-stu-id="7850b-125">Sets the current [Automatic Logon Policy](authentication-in-winhttp.md).</span></span><br/>                             |
| [<span data-ttu-id="7850b-126">**SetClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="7850b-126">**SetClientCertificate**</span></span>](iwinhttprequest-setclientcertificate.md)   | <span data-ttu-id="7850b-127">Seleciona um certificado de cliente para enviar a um servidor HTTPS (protocolo de transferência de hipertexto) seguro.</span><span class="sxs-lookup"><span data-stu-id="7850b-127">Selects a client certificate to send to a Secure Hypertext Transfer Protocol (HTTPS) server.</span></span><br/>                                 |
| [<span data-ttu-id="7850b-128">**SetCredentials**</span><span class="sxs-lookup"><span data-stu-id="7850b-128">**SetCredentials**</span></span>](iwinhttprequest-setcredentials.md)               | <span data-ttu-id="7850b-129">Define as credenciais a serem usadas com um servidor HTTP, um servidor proxy ou um servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="7850b-129">Sets credentials to be used with an HTTP server, either a proxy server or an originating server.</span></span><br/>                             |
| [<span data-ttu-id="7850b-130">**SetProxy**</span><span class="sxs-lookup"><span data-stu-id="7850b-130">**SetProxy**</span></span>](iwinhttprequest-setproxy.md)                           | <span data-ttu-id="7850b-131">Define informações do servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="7850b-131">Sets proxy server information.</span></span><br/>                                                                                               |
| [<span data-ttu-id="7850b-132">**SetRequestHeader**</span><span class="sxs-lookup"><span data-stu-id="7850b-132">**SetRequestHeader**</span></span>](iwinhttprequest-setrequestheader.md)           | <span data-ttu-id="7850b-133">Adiciona, altera ou exclui um cabeçalho de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="7850b-133">Adds, changes, or deletes an HTTP request header.</span></span><br/>                                                                            |
| [<span data-ttu-id="7850b-134">**Settempo_limites**</span><span class="sxs-lookup"><span data-stu-id="7850b-134">**SetTimeouts**</span></span>](iwinhttprequest-settimeouts.md)                     | <span data-ttu-id="7850b-135">Especifica os componentes de tempo limite individuais de uma operação de envio/recebimento, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="7850b-135">Specifies the individual time-out components of a send/receive operation, in milliseconds.</span></span><br/>                                   |
| [<span data-ttu-id="7850b-136">**WaitForResponse**</span><span class="sxs-lookup"><span data-stu-id="7850b-136">**WaitForResponse**</span></span>](iwinhttprequest-waitforresponse.md)             | <span data-ttu-id="7850b-137">Aguarda a conclusão de um método [**Send**](iwinhttprequest-send.md) assíncrono, com valor de tempo limite opcional, em segundos.</span><span class="sxs-lookup"><span data-stu-id="7850b-137">Waits for an asynchronous [**Send**](iwinhttprequest-send.md) method to complete, with optional time-out value, in seconds.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7850b-138">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7850b-138">Properties</span></span>

<span data-ttu-id="7850b-139">A interface **IWinHttpRequest** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7850b-139">The **IWinHttpRequest** interface has these properties.</span></span>



| <span data-ttu-id="7850b-140">Propriedade</span><span class="sxs-lookup"><span data-stu-id="7850b-140">Property</span></span>                                                            | <span data-ttu-id="7850b-141">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="7850b-141">Access type</span></span>           | <span data-ttu-id="7850b-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="7850b-142">Description</span></span>                                                           |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [<span data-ttu-id="7850b-143">**Opção**</span><span class="sxs-lookup"><span data-stu-id="7850b-143">**Option**</span></span>](iwinhttprequest-option.md)<br/>                 | <span data-ttu-id="7850b-144">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7850b-144">Read/write</span></span><br/> | <span data-ttu-id="7850b-145">Um valor de opção de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7850b-145">A WinHTTP option value.</span></span><br/>                                    |
| [<span data-ttu-id="7850b-146">**ResponseBody**</span><span class="sxs-lookup"><span data-stu-id="7850b-146">**ResponseBody**</span></span>](iwinhttprequest-responsebody.md)<br/>     | <span data-ttu-id="7850b-147">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7850b-147">Read-only</span></span><br/>  | <span data-ttu-id="7850b-148">O corpo da entidade de resposta como uma matriz de bytes não assinados.</span><span class="sxs-lookup"><span data-stu-id="7850b-148">The response entity body as an array of unsigned bytes.</span></span><br/>    |
| [<span data-ttu-id="7850b-149">**ResponseStream**</span><span class="sxs-lookup"><span data-stu-id="7850b-149">**ResponseStream**</span></span>](iwinhttprequest-responsestream.md)<br/> | <span data-ttu-id="7850b-150">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7850b-150">Read-only</span></span><br/>  | <span data-ttu-id="7850b-151">O corpo da entidade de resposta como um [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="7850b-151">The response entity body as an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span><br/> |
| [<span data-ttu-id="7850b-152">**ResponseText**</span><span class="sxs-lookup"><span data-stu-id="7850b-152">**ResponseText**</span></span>](iwinhttprequest-responsetext.md)<br/>     | <span data-ttu-id="7850b-153">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7850b-153">Read-only</span></span><br/>  | <span data-ttu-id="7850b-154">O corpo da entidade de resposta.</span><span class="sxs-lookup"><span data-stu-id="7850b-154">The response entity body.</span></span><br/>                                  |
| [<span data-ttu-id="7850b-155">**Status**</span><span class="sxs-lookup"><span data-stu-id="7850b-155">**Status**</span></span>](iwinhttprequest-status.md)<br/>                 | <span data-ttu-id="7850b-156">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7850b-156">Read-only</span></span><br/>  | <span data-ttu-id="7850b-157">O código de status HTTP da última resposta.</span><span class="sxs-lookup"><span data-stu-id="7850b-157">The HTTP status code from the last response.</span></span><br/>               |
| [<span data-ttu-id="7850b-158">**StatusText**</span><span class="sxs-lookup"><span data-stu-id="7850b-158">**StatusText**</span></span>](iwinhttprequest-statustext.md)<br/>         | <span data-ttu-id="7850b-159">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7850b-159">Read-only</span></span><br/>  | <span data-ttu-id="7850b-160">O texto de status HTTP.</span><span class="sxs-lookup"><span data-stu-id="7850b-160">The HTTP status text.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="7850b-161">Comentários</span><span class="sxs-lookup"><span data-stu-id="7850b-161">Remarks</span></span>

<span data-ttu-id="7850b-162">A interface **IWinHttpRequest** definida em HttpRequest. idl é implementada por uma classe com ID de **CLSID \_ WinHttpRequest**.</span><span class="sxs-lookup"><span data-stu-id="7850b-162">The **IWinHttpRequest** interface defined in httprequest.idl is implemented by a class with id of **CLSID\_WinHttpRequest**.</span></span> <span data-ttu-id="7850b-163">Um aplicativo obtém essa interface chamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) com uma ID de classe de **CLSID \_ WinHttpRequest** e uma ID de interface **de \_ IWinHttpRequest de IID**.</span><span class="sxs-lookup"><span data-stu-id="7850b-163">An application obtain this interface by calling [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) with a class id of **CLSID\_WinHttpRequest** and an interface id of **IID\_IWinHttpRequest**.</span></span>

> [!Note]  
> <span data-ttu-id="7850b-164">Para o Windows XP e o Windows 2000, consulte a seção [requisitos de tempo de execução](winhttp-start-page.md) da página inicial do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="7850b-164">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7850b-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7850b-165">Requirements</span></span>



| <span data-ttu-id="7850b-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="7850b-166">Requirement</span></span> | <span data-ttu-id="7850b-167">Valor</span><span class="sxs-lookup"><span data-stu-id="7850b-167">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7850b-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7850b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="7850b-169">Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="7850b-169">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="7850b-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7850b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="7850b-171">Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]</span><span class="sxs-lookup"><span data-stu-id="7850b-171">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="7850b-172">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="7850b-172">Redistributable</span></span><br/>          | <span data-ttu-id="7850b-173">WinHTTP 5,0 e Internet Explorer 5, 1 ou posterior no Windows XP e no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="7850b-173">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="7850b-174">INSERI</span><span class="sxs-lookup"><span data-stu-id="7850b-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7850b-175"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7850b-175"><dt>HttpRequest.idl</dt></span></span> </dl> |
| <span data-ttu-id="7850b-176">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7850b-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="7850b-177"><dt>WinHTTP. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7850b-177"><dt>Winhttp.lib</dt></span></span> </dl>     |
| <span data-ttu-id="7850b-178">DLL</span><span class="sxs-lookup"><span data-stu-id="7850b-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7850b-179"><dt>Winhttp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7850b-179"><dt>Winhttp.dll</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="7850b-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="7850b-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7850b-181">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="7850b-181">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="7850b-182">Versões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="7850b-182">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

