---
description: Este tópico identifica as funções que o WinHTTP fornece.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Funções de WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6511d2e66acc923072cc7a961aae3cb572b8e466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773034"
---
# <a name="winhttp-functions"></a><span data-ttu-id="8dd95-103">Funções de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="8dd95-103">WinHTTP Functions</span></span>

<span data-ttu-id="8dd95-104">O WinHTTP fornece as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="8dd95-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="8dd95-105">**WinHttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="8dd95-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="8dd95-106">Adiciona um ou mais cabeçalhos de solicitação HTTP ao identificador de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="8dd95-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-107">**WinHttpCheckPlatform**</span><span class="sxs-lookup"><span data-stu-id="8dd95-107">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="8dd95-108">Determina se a plataforma atual tem suporte pelo WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="8dd95-108">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-109">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="8dd95-109">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="8dd95-110">Fecha um único identificador [HINTERNET](hinternet-handles-in-winhttp.md) .</span><span class="sxs-lookup"><span data-stu-id="8dd95-110">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-111">**WinHttpConnect**</span><span class="sxs-lookup"><span data-stu-id="8dd95-111">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="8dd95-112">Especifica o servidor de destino inicial de uma solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="8dd95-112">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-113">**WinHttpCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="8dd95-113">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="8dd95-114">Separa uma URL em suas partes de componente, por exemplo, o nome do host e o caminho.</span><span class="sxs-lookup"><span data-stu-id="8dd95-114">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-115">**WinHttpCreateProxyResolver**</span><span class="sxs-lookup"><span data-stu-id="8dd95-115">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="8dd95-116">Cria um identificador para uso pelo [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="8dd95-116">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-117">**WinHttpCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="8dd95-117">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="8dd95-118">Cria uma URL a partir de partes de componente, por exemplo, o nome do host e o caminho.</span><span class="sxs-lookup"><span data-stu-id="8dd95-118">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-119">**WinHttpDetectAutoProxyConfigUrl**</span><span class="sxs-lookup"><span data-stu-id="8dd95-119">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="8dd95-120">Localiza a URL do Arquivo PAC (configuração automática do proxy).</span><span class="sxs-lookup"><span data-stu-id="8dd95-120">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="8dd95-121">Essa função relata a URL do Arquivo PAC, mas não baixa o arquivo.</span><span class="sxs-lookup"><span data-stu-id="8dd95-121">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-122">**WinHttpFreeProxyResult**</span><span class="sxs-lookup"><span data-stu-id="8dd95-122">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="8dd95-123">Libera os dados recuperados de uma chamada anterior para [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span><span class="sxs-lookup"><span data-stu-id="8dd95-123">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-124">**WinHttpGetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8dd95-124">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="8dd95-125">Recupera a configuração padrão do proxy WinHTTP do registro.</span><span class="sxs-lookup"><span data-stu-id="8dd95-125">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-126">**WinHTTPGetIEProxyConfigForCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="8dd95-126">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="8dd95-127">Obtém a configuração de proxy do Internet Explorer (IE) para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="8dd95-127">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-128">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="8dd95-128">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="8dd95-129">Recupera as informações de proxy para a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="8dd95-129">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-130">**WinHttpGetProxyForUrlEx**</span><span class="sxs-lookup"><span data-stu-id="8dd95-130">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="8dd95-131">Recupera as informações de proxy para a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="8dd95-131">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-132">**WinHttpGetProxyResult**</span><span class="sxs-lookup"><span data-stu-id="8dd95-132">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="8dd95-133">Recupera os resultados de uma chamada para [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span><span class="sxs-lookup"><span data-stu-id="8dd95-133">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-134">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="8dd95-134">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="8dd95-135">Inicializa o uso de um aplicativo das funções do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="8dd95-135">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-136">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="8dd95-136">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="8dd95-137">Cria um identificador de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="8dd95-137">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-138">**WinHttpQueryAuthSchemes**</span><span class="sxs-lookup"><span data-stu-id="8dd95-138">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="8dd95-139">Retorna os esquemas de autorização aos quais o servidor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="8dd95-139">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-140">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="8dd95-140">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="8dd95-141">Retorna o número de bytes de dados que estão disponíveis imediatamente para serem lidos com [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span><span class="sxs-lookup"><span data-stu-id="8dd95-141">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-142">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="8dd95-142">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="8dd95-143">Recupera informações de cabeçalho associadas a uma solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="8dd95-143">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-144">**WinHttpQueryOption**</span><span class="sxs-lookup"><span data-stu-id="8dd95-144">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="8dd95-145">Consulta uma opção de Internet no identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="8dd95-145">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-146">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="8dd95-146">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="8dd95-147">Lê dados de um identificador aberto pela função [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) .</span><span class="sxs-lookup"><span data-stu-id="8dd95-147">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-148">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="8dd95-148">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="8dd95-149">Termina uma solicitação HTTP que é iniciada pelo [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="8dd95-149">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-150">**WinHttpResetAutoProxy**</span><span class="sxs-lookup"><span data-stu-id="8dd95-150">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="8dd95-151">Redefine o proxy automático.</span><span class="sxs-lookup"><span data-stu-id="8dd95-151">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-152">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="8dd95-152">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="8dd95-153">Envia a solicitação especificada para o servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="8dd95-153">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-154">**WinHttpSetCredentials**</span><span class="sxs-lookup"><span data-stu-id="8dd95-154">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="8dd95-155">Passa as credenciais de autorização necessárias para o servidor.</span><span class="sxs-lookup"><span data-stu-id="8dd95-155">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-156">**WinHttpSetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="8dd95-156">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="8dd95-157">Define a configuração padrão do proxy WinHTTP no registro.</span><span class="sxs-lookup"><span data-stu-id="8dd95-157">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-158">**WinHttpSetOption**</span><span class="sxs-lookup"><span data-stu-id="8dd95-158">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="8dd95-159">Define uma opção da Internet.</span><span class="sxs-lookup"><span data-stu-id="8dd95-159">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-160">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="8dd95-160">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="8dd95-161">Configura uma função de retorno de chamada que o WinHTTP pode chamar conforme o progresso é feito durante uma operação.</span><span class="sxs-lookup"><span data-stu-id="8dd95-161">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-162">**WinHttpSetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="8dd95-162">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="8dd95-163">Define os vários tempos limite envolvidos em transações HTTP.</span><span class="sxs-lookup"><span data-stu-id="8dd95-163">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-164">**WinHttpTimeFromSystemTime**</span><span class="sxs-lookup"><span data-stu-id="8dd95-164">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="8dd95-165">Formata uma data e hora de acordo com a especificação HTTP versão 1,0.</span><span class="sxs-lookup"><span data-stu-id="8dd95-165">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-166">**WinHttpTimeToSystemTime**</span><span class="sxs-lookup"><span data-stu-id="8dd95-166">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="8dd95-167">Usa uma cadeia de caracteres de data/hora HTTP e a converte em uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="8dd95-167">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-168">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="8dd95-168">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="8dd95-169">Grava dados de solicitação em um servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="8dd95-169">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-170">**WinHttpWebSocketClose**</span><span class="sxs-lookup"><span data-stu-id="8dd95-170">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="8dd95-171">Fecha uma conexão WebSocket.</span><span class="sxs-lookup"><span data-stu-id="8dd95-171">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-172">**WinHttpWebSocketCompleteUpgrade**</span><span class="sxs-lookup"><span data-stu-id="8dd95-172">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="8dd95-173">Conclui um handshake WebSocket iniciado pelo [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span><span class="sxs-lookup"><span data-stu-id="8dd95-173">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-174">**WinHttpWebSocketQueryCloseStatus**</span><span class="sxs-lookup"><span data-stu-id="8dd95-174">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="8dd95-175">Obtém o status de fechamento enviado por um servidor.</span><span class="sxs-lookup"><span data-stu-id="8dd95-175">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-176">**WinHttpWebSocketReceive**</span><span class="sxs-lookup"><span data-stu-id="8dd95-176">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="8dd95-177">Recebe dados de uma conexão WebSocket.</span><span class="sxs-lookup"><span data-stu-id="8dd95-177">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-178">**WinHttpWebSocketSend**</span><span class="sxs-lookup"><span data-stu-id="8dd95-178">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="8dd95-179">Envia dados por uma conexão WebSocket.</span><span class="sxs-lookup"><span data-stu-id="8dd95-179">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="8dd95-180">**WinHttpWebSocketShutdown**</span><span class="sxs-lookup"><span data-stu-id="8dd95-180">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="8dd95-181">Envia um quadro de fechamento para uma conexão WebSocket.</span><span class="sxs-lookup"><span data-stu-id="8dd95-181">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>

 

 
