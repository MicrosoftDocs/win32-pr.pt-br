---
description: Este tópico identifica as funções que o WinHTTP fornece.
ms.assetid: dcb56d5d-ed0d-49bb-95bf-940a49c033f1
title: Funções WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e45289230c1cc22a7f8799dfbbe1dafddccf38
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174970"
---
# <a name="winhttp-functions"></a><span data-ttu-id="5a424-103">Funções WinHTTP</span><span class="sxs-lookup"><span data-stu-id="5a424-103">WinHTTP Functions</span></span>

<span data-ttu-id="5a424-104">O WinHTTP fornece as seguintes funções:</span><span class="sxs-lookup"><span data-stu-id="5a424-104">WinHTTP provides the following functions:</span></span>

<dl> <dt>

[<span data-ttu-id="5a424-105">**WinHttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="5a424-105">**WinHttpAddRequestHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)
</dt> <dd>

<span data-ttu-id="5a424-106">Adiciona um ou mais cabeçalhos de solicitação HTTP ao alça de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="5a424-106">Adds one or more HTTP request headers to the HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-107">**WinHttpAddRequestHeadersEx**</span><span class="sxs-lookup"><span data-stu-id="5a424-107">**WinHttpAddRequestHeadersEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheadersex)
</dt> <dd>

<span data-ttu-id="5a424-108">Adiciona um ou mais cabeçalhos de solicitação HTTP a um handle de solicitação HTTP, permitindo que você use cadeias de caracteres de nome/valor separadas.</span><span class="sxs-lookup"><span data-stu-id="5a424-108">Adds one or more HTTP request headers to an HTTP request handle, allowing you to use separate name/value strings.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-109">**WinHttpCheckPlatform**</span><span class="sxs-lookup"><span data-stu-id="5a424-109">**WinHttpCheckPlatform**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcheckplatform)
</dt> <dd>

<span data-ttu-id="5a424-110">Determina se a plataforma atual é suportada pelo WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="5a424-110">Determines whether the current platform is supported by WinHTTP.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-111">**WinHttpCloseHandle**</span><span class="sxs-lookup"><span data-stu-id="5a424-111">**WinHttpCloseHandle**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle)
</dt> <dd>

<span data-ttu-id="5a424-112">Fecha um único alça [HINTERNET.](hinternet-handles-in-winhttp.md)</span><span class="sxs-lookup"><span data-stu-id="5a424-112">Closes a single [HINTERNET](hinternet-handles-in-winhttp.md) handle.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-113">**WinHttpConnect**</span><span class="sxs-lookup"><span data-stu-id="5a424-113">**WinHttpConnect**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)
</dt> <dd>

<span data-ttu-id="5a424-114">Especifica o servidor de destino inicial de uma solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="5a424-114">Specifies the initial target server of an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-115">**WinHttpCrackUrl**</span><span class="sxs-lookup"><span data-stu-id="5a424-115">**WinHttpCrackUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl)
</dt> <dd>

<span data-ttu-id="5a424-116">Separa uma URL em suas partes de componente, por exemplo, nome e caminho do host.</span><span class="sxs-lookup"><span data-stu-id="5a424-116">Separates a URL into its component parts, for example, host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-117">**WinHttpCreateProxyResolver**</span><span class="sxs-lookup"><span data-stu-id="5a424-117">**WinHttpCreateProxyResolver**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateproxyresolver)
</dt> <dd>

<span data-ttu-id="5a424-118">Cria um handle para uso [**por WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)</span><span class="sxs-lookup"><span data-stu-id="5a424-118">Creates a handle for use by [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-119">**WinHttpCreateUrl**</span><span class="sxs-lookup"><span data-stu-id="5a424-119">**WinHttpCreateUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl)
</dt> <dd>

<span data-ttu-id="5a424-120">Cria uma URL de partes do componente, por exemplo, o nome e o caminho do host.</span><span class="sxs-lookup"><span data-stu-id="5a424-120">Creates a URL from component parts, for example, the host name and path.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-121">**WinHttpDetectAutoProxyConfigUrl**</span><span class="sxs-lookup"><span data-stu-id="5a424-121">**WinHttpDetectAutoProxyConfigUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl)
</dt> <dd>

<span data-ttu-id="5a424-122">Localiza a URL para o arquivo PAC (Configuração Automática de Proxy).</span><span class="sxs-lookup"><span data-stu-id="5a424-122">Finds the URL for the Proxy Auto-Configuration (PAC) file.</span></span> <span data-ttu-id="5a424-123">Essa função relata a URL do arquivo PAC, mas não baixa o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5a424-123">This function reports the URL of the PAC file, but it does not download the file.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-124">**WinHttpFreeProxyResult**</span><span class="sxs-lookup"><span data-stu-id="5a424-124">**WinHttpFreeProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpfreeproxyresult)
</dt> <dd>

<span data-ttu-id="5a424-125">Libera os dados recuperados de uma chamada anterior para [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)</span><span class="sxs-lookup"><span data-stu-id="5a424-125">Frees the data retrieved from a previous call to [**WinHttpGetProxyResult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-126">**WinHttpFreeQueryConnectionGroupResult**</span><span class="sxs-lookup"><span data-stu-id="5a424-126">**WinHttpFreeQueryConnectionGroupResult**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpfreequeryconnectiongroupresult)
</dt> <dd>

<span data-ttu-id="5a424-127">Libera a memória alocada por uma chamada anterior para [WinHttpQueryConnectionGroup.](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)</span><span class="sxs-lookup"><span data-stu-id="5a424-127">Frees the memory allocated by a previous call to [WinHttpQueryConnectionGroup](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup).</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-128">**WinHttpGetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="5a424-128">**WinHttpGetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="5a424-129">Recupera a configuração de proxy WinHTTP padrão do Registro.</span><span class="sxs-lookup"><span data-stu-id="5a424-129">Retrieves the default WinHTTP proxy configuration from the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-130">**WinHTTPGetIEProxyConfigForCurrentUser**</span><span class="sxs-lookup"><span data-stu-id="5a424-130">**WinHTTPGetIEProxyConfigForCurrentUser**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetieproxyconfigforcurrentuser)
</dt> <dd>

<span data-ttu-id="5a424-131">Obtém a configuração de proxy Internet Explorer (IE) para o usuário atual.</span><span class="sxs-lookup"><span data-stu-id="5a424-131">Obtains the Internet Explorer (IE) proxy configuration for the current user.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-132">**WinHttpGetProxyForUrl**</span><span class="sxs-lookup"><span data-stu-id="5a424-132">**WinHttpGetProxyForUrl**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl)
</dt> <dd>

<span data-ttu-id="5a424-133">Recupera as informações de proxy para a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="5a424-133">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-134">**WinHttpGetProxyForUrlEx**</span><span class="sxs-lookup"><span data-stu-id="5a424-134">**WinHttpGetProxyForUrlEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)
</dt> <dd>

<span data-ttu-id="5a424-135">Recupera as informações de proxy para a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="5a424-135">Retrieves the proxy information for the specified URL.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-136">**WinHttpGetProxyResult**</span><span class="sxs-lookup"><span data-stu-id="5a424-136">**WinHttpGetProxyResult**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)
</dt> <dd>

<span data-ttu-id="5a424-137">Recupera os resultados de uma chamada para [**WinHttpGetProxyForUrlEx.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex)</span><span class="sxs-lookup"><span data-stu-id="5a424-137">Retrieves the results of a call to [**WinHttpGetProxyForUrlEx**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurlex).</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-138">**WinHttpOpen**</span><span class="sxs-lookup"><span data-stu-id="5a424-138">**WinHttpOpen**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)
</dt> <dd>

<span data-ttu-id="5a424-139">Inicializa o uso de um aplicativo das funções WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="5a424-139">Initializes an application's use of the WinHTTP functions.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-140">**WinHttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="5a424-140">**WinHttpOpenRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)
</dt> <dd>

<span data-ttu-id="5a424-141">Cria um alça de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="5a424-141">Creates an HTTP request handle.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-142">**WinHttpQueryAuthSchemes**</span><span class="sxs-lookup"><span data-stu-id="5a424-142">**WinHttpQueryAuthSchemes**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)
</dt> <dd>

<span data-ttu-id="5a424-143">Retorna os esquemas de autorização compatíveis com o servidor.</span><span class="sxs-lookup"><span data-stu-id="5a424-143">Returns the authorization schemes that the server supports.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-144">**WinHttpQueryConnectionGroup**</span><span class="sxs-lookup"><span data-stu-id="5a424-144">**WinHttpQueryConnectionGroup**</span></span>](/windows/win32/api/Winhttp/nf-winhttp-winhttpqueryconnectiongroup)
</dt> <dd>

<span data-ttu-id="5a424-145">Recupera uma descrição do estado atual das conexões do WinHttp.</span><span class="sxs-lookup"><span data-stu-id="5a424-145">Retrieves a description of the current state of WinHttp's connections.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-146">**WinHttpQueryDataAvailable**</span><span class="sxs-lookup"><span data-stu-id="5a424-146">**WinHttpQueryDataAvailable**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable)
</dt> <dd>

<span data-ttu-id="5a424-147">Retorna o número de bytes de dados que estão disponíveis imediatamente para serem lidos com [**WinHttpReadData.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)</span><span class="sxs-lookup"><span data-stu-id="5a424-147">Returns the number of bytes of data that are available immediately to be read with [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-148">**WinHttpQueryHeaders**</span><span class="sxs-lookup"><span data-stu-id="5a424-148">**WinHttpQueryHeaders**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders)
</dt> <dd>

<span data-ttu-id="5a424-149">Recupera informações de cabeçalho associadas a uma solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="5a424-149">Retrieves header information associated with an HTTP request.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-150">**WinHttpQueryHeadersEx**</span><span class="sxs-lookup"><span data-stu-id="5a424-150">**WinHttpQueryHeadersEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheadersex)
</dt> <dd>

<span data-ttu-id="5a424-151">Recupera informações de cabeçalho associadas a uma solicitação HTTP; oferece uma maneira de recuperar cadeias de caracteres de valor e nome de header analisados.</span><span class="sxs-lookup"><span data-stu-id="5a424-151">Retrieves header information associated with an HTTP request; offers a way to retrieve parsed header name and value strings.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-152">**WinHttpQueryOption**</span><span class="sxs-lookup"><span data-stu-id="5a424-152">**WinHttpQueryOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption)
</dt> <dd>

<span data-ttu-id="5a424-153">Consulta uma opção de Internet no alça especificado.</span><span class="sxs-lookup"><span data-stu-id="5a424-153">Queries an Internet option on the specified handle.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-154">**WinHttpReadData**</span><span class="sxs-lookup"><span data-stu-id="5a424-154">**WinHttpReadData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata)
</dt> <dd>

<span data-ttu-id="5a424-155">Lê dados de um handle aberto pela [**função WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)</span><span class="sxs-lookup"><span data-stu-id="5a424-155">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-156">**WinHttpReadDataEx**</span><span class="sxs-lookup"><span data-stu-id="5a424-156">**WinHttpReadDataEx**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddataex)
</dt> <dd>

<span data-ttu-id="5a424-157">Lê dados de um handle aberto pela [**função WinHttpOpenRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)</span><span class="sxs-lookup"><span data-stu-id="5a424-157">Reads data from a handle opened by the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-158">**WinHttpReceiveResponse**</span><span class="sxs-lookup"><span data-stu-id="5a424-158">**WinHttpReceiveResponse**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse)
</dt> <dd>

<span data-ttu-id="5a424-159">Encerra uma solicitação HTTP iniciada por [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="5a424-159">Ends an HTTP request that is initiated by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-160">**WinHttpResetAutoProxy**</span><span class="sxs-lookup"><span data-stu-id="5a424-160">**WinHttpResetAutoProxy**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpresetautoproxy)
</dt> <dd>

<span data-ttu-id="5a424-161">Redefine o proxy automático.</span><span class="sxs-lookup"><span data-stu-id="5a424-161">Resets the auto-proxy.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-162">**WinHttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="5a424-162">**WinHttpSendRequest**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)
</dt> <dd>

<span data-ttu-id="5a424-163">Envia a solicitação especificada para o servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="5a424-163">Sends the specified request to the HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-164">**WinHttpSetCredentials**</span><span class="sxs-lookup"><span data-stu-id="5a424-164">**WinHttpSetCredentials**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials)
</dt> <dd>

<span data-ttu-id="5a424-165">Passa as credenciais de autorização necessárias para o servidor.</span><span class="sxs-lookup"><span data-stu-id="5a424-165">Passes the required authorization credentials to the server.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-166">**WinHttpSetDefaultProxyConfiguration**</span><span class="sxs-lookup"><span data-stu-id="5a424-166">**WinHttpSetDefaultProxyConfiguration**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetdefaultproxyconfiguration)
</dt> <dd>

<span data-ttu-id="5a424-167">Define a configuração de proxy WinHTTP padrão no Registro.</span><span class="sxs-lookup"><span data-stu-id="5a424-167">Sets the default WinHTTP proxy configuration in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-168">**WinHttpSetOption**</span><span class="sxs-lookup"><span data-stu-id="5a424-168">**WinHttpSetOption**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption)
</dt> <dd>

<span data-ttu-id="5a424-169">Define uma opção de Internet.</span><span class="sxs-lookup"><span data-stu-id="5a424-169">Sets an Internet option.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-170">**WinHttpSetStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="5a424-170">**WinHttpSetStatusCallback**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback)
</dt> <dd>

<span data-ttu-id="5a424-171">Configura uma função de retorno de chamada que o WinHTTP pode chamar conforme o progresso é feito durante uma operação.</span><span class="sxs-lookup"><span data-stu-id="5a424-171">Sets up a callback function that WinHTTP can call as progress is made during an operation.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-172">**WinHttpSetTimeouts**</span><span class="sxs-lookup"><span data-stu-id="5a424-172">**WinHttpSetTimeouts**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsettimeouts)
</dt> <dd>

<span data-ttu-id="5a424-173">Define os vários tempos de tempo que estão envolvidos com transações HTTP.</span><span class="sxs-lookup"><span data-stu-id="5a424-173">Sets the various time-outs that are involved with HTTP transactions.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-174">**WinHttpTimeFromSystemTime**</span><span class="sxs-lookup"><span data-stu-id="5a424-174">**WinHttpTimeFromSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimefromsystemtime)
</dt> <dd>

<span data-ttu-id="5a424-175">Formatar uma data e hora de acordo com a especificação http versão 1.0.</span><span class="sxs-lookup"><span data-stu-id="5a424-175">Formats a date and time according to the HTTP version 1.0 specification.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-176">**WinHttpTimeToSystemTime**</span><span class="sxs-lookup"><span data-stu-id="5a424-176">**WinHttpTimeToSystemTime**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttptimetosystemtime)
</dt> <dd>

<span data-ttu-id="5a424-177">Pega uma cadeia de caracteres de data/hora HTTP e a converte em uma [**estrutura SYSTEMTIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)</span><span class="sxs-lookup"><span data-stu-id="5a424-177">Takes an HTTP time/date string and converts it to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-178">**WinHttpWriteData**</span><span class="sxs-lookup"><span data-stu-id="5a424-178">**WinHttpWriteData**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)
</dt> <dd>

<span data-ttu-id="5a424-179">Grava dados de solicitação em um servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="5a424-179">Writes request data to an HTTP server.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-180">**WinHttpWebSocketClose**</span><span class="sxs-lookup"><span data-stu-id="5a424-180">**WinHttpWebSocketClose**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketclose)
</dt> <dd>

<span data-ttu-id="5a424-181">Fecha uma conexão WebSocket.</span><span class="sxs-lookup"><span data-stu-id="5a424-181">Closes a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-182">**WinHttpWebSocketCompleteUpgrade**</span><span class="sxs-lookup"><span data-stu-id="5a424-182">**WinHttpWebSocketCompleteUpgrade**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketcompleteupgrade)
</dt> <dd>

<span data-ttu-id="5a424-183">Conclui um handshake do WebSocket iniciado por [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)</span><span class="sxs-lookup"><span data-stu-id="5a424-183">Completes a WebSocket handshake started by [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest).</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-184">**WinHttpWebSocketQueryCloseStatus**</span><span class="sxs-lookup"><span data-stu-id="5a424-184">**WinHttpWebSocketQueryCloseStatus**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketqueryclosestatus)
</dt> <dd>

<span data-ttu-id="5a424-185">Obtém o status de fechamento enviado por um servidor.</span><span class="sxs-lookup"><span data-stu-id="5a424-185">Gets the close status sent by a server.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-186">**WinHttpWebSocketReceive**</span><span class="sxs-lookup"><span data-stu-id="5a424-186">**WinHttpWebSocketReceive**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketreceive)
</dt> <dd>

<span data-ttu-id="5a424-187">Recebe dados de uma conexão WebSocket.</span><span class="sxs-lookup"><span data-stu-id="5a424-187">Receives data from a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-188">**WinHttpWebSocketSend**</span><span class="sxs-lookup"><span data-stu-id="5a424-188">**WinHttpWebSocketSend**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketsend)
</dt> <dd>

<span data-ttu-id="5a424-189">Envia dados por uma conexão WebSocket.</span><span class="sxs-lookup"><span data-stu-id="5a424-189">Sends data over a WebSocket connection.</span></span>

</dd> <dt>

[<span data-ttu-id="5a424-190">**WinHttpWebSocketShutdown**</span><span class="sxs-lookup"><span data-stu-id="5a424-190">**WinHttpWebSocketShutdown**</span></span>](/windows/desktop/api/winhttp/nf-winhttp-winhttpwebsocketshutdown)
</dt> <dd>

<span data-ttu-id="5a424-191">Envia um quadro próximo a uma conexão WebSocket.</span><span class="sxs-lookup"><span data-stu-id="5a424-191">Sends a close frame to a WebSocket connection.</span></span>

</dd> </dl>


