---
description: Este tópico identifica as funções que o WinHTTP fornece.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Funções WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5f9db8fcde5589a86556111bec6df3b2b18c76
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587750"
---
# <a name="winhttp-functions"></a><span data-ttu-id="b0459-103">Funções WinHTTP</span><span class="sxs-lookup"><span data-stu-id="b0459-103">WinHTTP Functions</span></span>

<span data-ttu-id="b0459-104">O WinHTTP fornece as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="b0459-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="b0459-105">**WinHttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="b0459-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="b0459-106">Adiciona um ou mais cabeçalhos de solicitação HTTP ao alça de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0459-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-107">**WinHttpCheckPlatform**</span><span class="sxs-lookup"><span data-stu-id="b0459-107">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="b0459-108">Determina se a plataforma atual é suportada pelo WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b0459-108">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-109">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="b0459-109">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="b0459-110">Fecha um único alça [HINTERNET.](hinternet-handles-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="b0459-110">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-111">**WinHttpConnect**</span><span class="sxs-lookup"><span data-stu-id="b0459-111">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="b0459-112">Especifica o servidor de destino inicial de uma solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0459-112">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-113">**WinHttpCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="b0459-113">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="b0459-114">Separa uma URL em suas partes de componente, por exemplo, nome e caminho do host.</span><span class="sxs-lookup"><span data-stu-id="b0459-114">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-115">**WinHttpCreateProxyResolver**</span><span class="sxs-lookup"><span data-stu-id="b0459-115">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="b0459-116">Cria um handle para uso [**por WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)</span><span class="sxs-lookup"><span data-stu-id="b0459-116">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-117">**WinHttpCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="b0459-117">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="b0459-118">Cria uma URL de partes do componente, por exemplo, o nome e o caminho do host.</span><span class="sxs-lookup"><span data-stu-id="b0459-118">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-119">**WinHttpDetectAutoProxyConfigUrl**</span><span class="sxs-lookup"><span data-stu-id="b0459-119">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="b0459-120">Localiza a URL para o arquivo PAC (Configuração Automática de Proxy).</span><span class="sxs-lookup"><span data-stu-id="b0459-120">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="b0459-121">Essa função relata a URL do arquivo PAC, mas não baixa o arquivo.</span><span class="sxs-lookup"><span data-stu-id="b0459-121">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-122">**WinHttpFreeProxyResult**</span><span class="sxs-lookup"><span data-stu-id="b0459-122">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="b0459-123">Libera os dados recuperados de uma chamada anterior para [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)</span><span class="sxs-lookup"><span data-stu-id="b0459-123">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-124">**WinHttpFreeQueryConnectionGroupResult**</span><span class="sxs-lookup"><span data-stu-id="b0459-124">**WinHttpFreeQueryConnectionGroupResult**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

<span data-ttu-id="b0459-125">Libera a memória alocada por uma chamada anterior para [WinHttpQueryConnectionGroup.](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)</span><span class="sxs-lookup"><span data-stu-id="b0459-125">Frees the memory allocated by a previous call to [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-126">**WinHttpGetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="b0459-126">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="b0459-127">Recupera a configuração de proxy WinHTTP padrão do Registro.</span><span class="sxs-lookup"><span data-stu-id="b0459-127">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-128">**WinHTTPGetIEProxyConfigForCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="b0459-128">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="b0459-129">Obtém a configuração de proxy Internet Explorer (IE) para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="b0459-129">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-130">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="b0459-130">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="b0459-131">Recupera as informações de proxy para a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="b0459-131">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-132">**WinHttpGetProxyForUrlEx**</span><span class="sxs-lookup"><span data-stu-id="b0459-132">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="b0459-133">Recupera as informações de proxy para a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="b0459-133">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-134">**WinHttpGetProxyResult**</span><span class="sxs-lookup"><span data-stu-id="b0459-134">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="b0459-135">Recupera os resultados de uma chamada para [**WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)</span><span class="sxs-lookup"><span data-stu-id="b0459-135">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-136">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="b0459-136">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="b0459-137">Inicializa o uso de um aplicativo das funções WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b0459-137">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-138">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="b0459-138">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="b0459-139">Cria um alça de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0459-139">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-140">**WinHttpQueryAuthSchemes**</span><span class="sxs-lookup"><span data-stu-id="b0459-140">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="b0459-141">Retorna os esquemas de autorização compatíveis com o servidor.</span><span class="sxs-lookup"><span data-stu-id="b0459-141">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-142">**WinHttpQueryConnectionGroup**</span><span class="sxs-lookup"><span data-stu-id="b0459-142">**WinHttpQueryConnectionGroup**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

<span data-ttu-id="b0459-143">Recupera uma descrição do estado atual das conexões do WinHttp.</span><span class="sxs-lookup"><span data-stu-id="b0459-143">Retrieves a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-144">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="b0459-144">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="b0459-145">Retorna o número de bytes de dados que estão disponíveis imediatamente para serem lidos com [**WinHttpReadData.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)</span><span class="sxs-lookup"><span data-stu-id="b0459-145">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-146">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="b0459-146">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="b0459-147">Recupera informações de cabeçalho associadas a uma solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0459-147">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-148">**WinHttpQueryOption**</span><span class="sxs-lookup"><span data-stu-id="b0459-148">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="b0459-149">Consulta uma opção de Internet no alça especificado.</span><span class="sxs-lookup"><span data-stu-id="b0459-149">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-150">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="b0459-150">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="b0459-151">Lê dados de um handle aberto pela [**função WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)</span><span class="sxs-lookup"><span data-stu-id="b0459-151">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-152">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="b0459-152">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="b0459-153">Encerra uma solicitação HTTP iniciada por [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="b0459-153">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-154">**WinHttpResetAutoProxy**</span><span class="sxs-lookup"><span data-stu-id="b0459-154">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="b0459-155">Redefine o proxy automático.</span><span class="sxs-lookup"><span data-stu-id="b0459-155">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-156">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="b0459-156">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="b0459-157">Envia a solicitação especificada para o servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0459-157">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-158">**WinHttpSetCredentials**</span><span class="sxs-lookup"><span data-stu-id="b0459-158">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="b0459-159">Passa as credenciais de autorização necessárias para o servidor.</span><span class="sxs-lookup"><span data-stu-id="b0459-159">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-160">**WinHttpSetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="b0459-160">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="b0459-161">Define a configuração de proxy WinHTTP padrão no Registro.</span><span class="sxs-lookup"><span data-stu-id="b0459-161">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-162">**WinHttpSetOption**</span><span class="sxs-lookup"><span data-stu-id="b0459-162">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="b0459-163">Define uma opção de Internet.</span><span class="sxs-lookup"><span data-stu-id="b0459-163">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-164">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="b0459-164">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="b0459-165">Configura uma função de retorno de chamada que o WinHTTP pode chamar conforme o progresso é feito durante uma operação.</span><span class="sxs-lookup"><span data-stu-id="b0459-165">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-166">**WinHttpSetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="b0459-166">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="b0459-167">Define os vários tempos de tempo que estão envolvidos com transações HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0459-167">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-168">**WinHttpTimeFromSystemTime**</span><span class="sxs-lookup"><span data-stu-id="b0459-168">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="b0459-169">Formatar uma data e hora de acordo com a especificação http versão 1.0.</span><span class="sxs-lookup"><span data-stu-id="b0459-169">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-170">**WinHttpTimeToSystemTime**</span><span class="sxs-lookup"><span data-stu-id="b0459-170">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="b0459-171">Pega uma cadeia de caracteres de data/hora HTTP e a converte em uma [**estrutura SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)</span><span class="sxs-lookup"><span data-stu-id="b0459-171">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-172">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="b0459-172">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="b0459-173">Grava dados de solicitação em um servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0459-173">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-174">**WinHttpWebSocketClose**</span><span class="sxs-lookup"><span data-stu-id="b0459-174">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="b0459-175">Fecha uma conexão WebSocket.</span><span class="sxs-lookup"><span data-stu-id="b0459-175">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-176">**WinHttpWebSocketCompleteUpgrade**</span><span class="sxs-lookup"><span data-stu-id="b0459-176">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="b0459-177">Conclui um handshake do WebSocket iniciado por [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="b0459-177">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-178">**WinHttpWebSocketQueryCloseStatus**</span><span class="sxs-lookup"><span data-stu-id="b0459-178">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="b0459-179">Obtém o status de fechamento enviado por um servidor.</span><span class="sxs-lookup"><span data-stu-id="b0459-179">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-180">**WinHttpWebSocketReceive**</span><span class="sxs-lookup"><span data-stu-id="b0459-180">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="b0459-181">Recebe dados de uma conexão WebSocket.</span><span class="sxs-lookup"><span data-stu-id="b0459-181">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-182">**WinHttpWebSocketSend**</span><span class="sxs-lookup"><span data-stu-id="b0459-182">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="b0459-183">Envia dados por uma conexão WebSocket.</span><span class="sxs-lookup"><span data-stu-id="b0459-183">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="b0459-184">**WinHttpWebSocketShutdown**</span><span class="sxs-lookup"><span data-stu-id="b0459-184">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="b0459-185">Envia um quadro próximo a uma conexão WebSocket.</span><span class="sxs-lookup"><span data-stu-id="b0459-185">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>

 

 
