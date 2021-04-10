---
description: O Microsoft Windows HTTP Services (WinHTTP) expõe um conjunto de funções C/C++ que permitem que seu aplicativo acesse recursos HTTP na Web. Este tópico fornece uma visão geral de como essas funções são usadas para interagir com um servidor HTTP.
ms.assetid: 66a1616b-0cf3-45c7-880b-e36728b5a9c4
title: Visão geral das sessões do WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98dc8116dff75f279b87cb5f5ee6af607034176f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090425"
---
# <a name="winhttp-sessions-overview"></a><span data-ttu-id="2797a-104">Visão geral das sessões do WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2797a-104">WinHTTP Sessions Overview</span></span>

<span data-ttu-id="2797a-105">O Microsoft Windows HTTP Services (WinHTTP) expõe um conjunto de funções C/C++ que permitem que seu aplicativo acesse recursos HTTP na Web.</span><span class="sxs-lookup"><span data-stu-id="2797a-105">The Microsoft Windows HTTP Services (WinHTTP) exposes a set of C/C++ functions that enable your application to access HTTP resources on the Web.</span></span> <span data-ttu-id="2797a-106">Este tópico fornece uma visão geral de como essas funções são usadas para interagir com um servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="2797a-106">This topic provides an overview of how these functions are used to interact with an HTTP server.</span></span>

-   [<span data-ttu-id="2797a-107">Usando a API do WinHTTP para acessar a Web</span><span class="sxs-lookup"><span data-stu-id="2797a-107">Using the WinHTTP API to Access the Web</span></span>](#using-the-winhttp-api-to-access-the-web)
-   [<span data-ttu-id="2797a-108">Inicializando WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2797a-108">Initializing WinHTTP</span></span>](#initializing-winhttp)
-   [<span data-ttu-id="2797a-109">Abrindo uma solicitação</span><span class="sxs-lookup"><span data-stu-id="2797a-109">Opening a Request</span></span>](#opening-a-request)
-   [<span data-ttu-id="2797a-110">Adicionando cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="2797a-110">Adding Request Headers</span></span>](#adding-request-headers)
-   [<span data-ttu-id="2797a-111">Enviando uma solicitação</span><span class="sxs-lookup"><span data-stu-id="2797a-111">Sending a Request</span></span>](#sending-a-request)
-   [<span data-ttu-id="2797a-112">Postando dados no servidor</span><span class="sxs-lookup"><span data-stu-id="2797a-112">Posting Data to the Server</span></span>](#posting-data-to-the-server)
-   [<span data-ttu-id="2797a-113">Obtendo informações sobre uma solicitação</span><span class="sxs-lookup"><span data-stu-id="2797a-113">Getting Information About a Request</span></span>](#getting-information-about-a-request)
-   [<span data-ttu-id="2797a-114">Baixando recursos da Web</span><span class="sxs-lookup"><span data-stu-id="2797a-114">Downloading Resources from the Web</span></span>](#downloading-resources-from-the-web)

## <a name="using-the-winhttp-api-to-access-the-web"></a><span data-ttu-id="2797a-115">Usando a API do WinHTTP para acessar a Web</span><span class="sxs-lookup"><span data-stu-id="2797a-115">Using the WinHTTP API to Access the Web</span></span>

<span data-ttu-id="2797a-116">O diagrama a seguir mostra a ordem na qual as funções WinHTTP são normalmente chamadas ao interagir com um servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="2797a-116">The following diagram shows the order in which WinHTTP functions are typically called when interacting with an HTTP server.</span></span> <span data-ttu-id="2797a-117">As caixas sombreadas representam funções que geram um identificador [HINTERNET](hinternet-handles-in-winhttp.md) , enquanto as caixas simples representam funções que usam esses identificadores.</span><span class="sxs-lookup"><span data-stu-id="2797a-117">The shaded boxes represent functions that generate an [HINTERNET](hinternet-handles-in-winhttp.md) handle, while the plain boxes represent functions that use those handles.</span></span>

![funções que criam identificadores](images/art-winhttp3.png)

## <a name="initializing-winhttp"></a><span data-ttu-id="2797a-119">Inicializando WinHTTP</span><span class="sxs-lookup"><span data-stu-id="2797a-119">Initializing WinHTTP</span></span>

<span data-ttu-id="2797a-120">Antes de interagir com um servidor, o WinHTTP deve ser inicializado chamando [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen).</span><span class="sxs-lookup"><span data-stu-id="2797a-120">Before interacting with a server, WinHTTP must be initialized by calling [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen).</span></span> <span data-ttu-id="2797a-121">[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) cria um contexto de sessão para manter detalhes sobre a sessão http e retorna um identificador de sessão.</span><span class="sxs-lookup"><span data-stu-id="2797a-121">[**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) creates a session context to maintain details about the HTTP session, and returns a session handle.</span></span> <span data-ttu-id="2797a-122">Usando esse identificador, a função [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) é capaz de especificar um servidor de destino http ou HTTPS (protocolo de transferência de hipertexto) seguro.</span><span class="sxs-lookup"><span data-stu-id="2797a-122">Using this handle, the [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) function is then able to specify a target HTTP or Secure Hypertext Transfer Protocol (HTTPS) server.</span></span>

> [!Note]  
> <span data-ttu-id="2797a-123">Uma chamada para [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) não resulta em uma conexão real com o servidor http até que uma solicitação seja feita para um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="2797a-123">A call to [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) does not result in an actual connection to the HTTP server until a request is made for a specific resource.</span></span>

 

## <a name="opening-a-request"></a><span data-ttu-id="2797a-124">Abrindo uma solicitação</span><span class="sxs-lookup"><span data-stu-id="2797a-124">Opening a Request</span></span>

<span data-ttu-id="2797a-125">A função [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) abre uma solicitação HTTP para um recurso específico e retorna um identificador [HINTERNET](hinternet-handles-in-winhttp.md) que pode ser usado pelas outras funções http.</span><span class="sxs-lookup"><span data-stu-id="2797a-125">The [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function opens an HTTP request for a particular resource and returns an [HINTERNET](hinternet-handles-in-winhttp.md) handle that can be used by the other HTTP functions.</span></span> <span data-ttu-id="2797a-126">O [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) não envia a solicitação ao servidor quando chamado.</span><span class="sxs-lookup"><span data-stu-id="2797a-126">[**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) does not send the request to the server when called.</span></span> <span data-ttu-id="2797a-127">A função [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) realmente estabelece uma conexão pela rede e envia a solicitação.</span><span class="sxs-lookup"><span data-stu-id="2797a-127">The [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function actually establishes a connection over the network and sends the request.</span></span>

<span data-ttu-id="2797a-128">O exemplo a seguir mostra uma chamada de exemplo para [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) que usa as opções padrão.</span><span class="sxs-lookup"><span data-stu-id="2797a-128">The following example shows a sample call to [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) that uses the default options.</span></span>

`HINTERNET hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL, NULL, NULL, NULL, 0);`

## <a name="adding-request-headers"></a><span data-ttu-id="2797a-129">Adicionando cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="2797a-129">Adding Request Headers</span></span>

<span data-ttu-id="2797a-130">A função [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) permite que um aplicativo acrescente cabeçalhos de solicitação de formato livre adicionais ao identificador de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="2797a-130">The [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) function allows an application to append additional free-format request headers to the HTTP request handle.</span></span> <span data-ttu-id="2797a-131">Ele é destinado ao uso por aplicativos sofisticados que exigem controle preciso sobre as solicitações enviadas ao servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="2797a-131">It is intended for use by sophisticated applications that require precise control over the requests sent to the HTTP server.</span></span>

<span data-ttu-id="2797a-132">A função [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) requer um identificador de solicitação HTTP criado pelo [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), uma cadeia de caracteres que contém os cabeçalhos, o comprimento dos cabeçalhos e quaisquer modificadores.</span><span class="sxs-lookup"><span data-stu-id="2797a-132">The [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) function requires an HTTP request handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), a string that contains the headers, the length of the headers, and any modifiers.</span></span>

<span data-ttu-id="2797a-133">Os modificadores a seguir podem ser usados com [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span><span class="sxs-lookup"><span data-stu-id="2797a-133">The following modifiers can be used with [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span></span>



| <span data-ttu-id="2797a-134">Modificador</span><span class="sxs-lookup"><span data-stu-id="2797a-134">Modifier</span></span>                                                                                         | <span data-ttu-id="2797a-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="2797a-135">Description</span></span>                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2797a-136">**\_ \_ Adicionar sinalizador de ADDREQ de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="2797a-136">**WINHTTP\_ADDREQ\_FLAG\_ADD**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                       | <span data-ttu-id="2797a-137">Adiciona o cabeçalho se ele não existir.</span><span class="sxs-lookup"><span data-stu-id="2797a-137">Adds the header if it does not exist.</span></span> <span data-ttu-id="2797a-138">Usado com [**a \_ \_ \_ substituição do sinalizador ADDREQ do WinHTTP**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span><span class="sxs-lookup"><span data-stu-id="2797a-138">Used with [**WINHTTP\_ADDREQ\_FLAG\_REPLACE**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders).</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="2797a-139">**sinalizador de ADDREQ de WINHTTP \_ \_ \_ Adicionar \_ se \_ novo**</span><span class="sxs-lookup"><span data-stu-id="2797a-139">**WINHTTP\_ADDREQ\_FLAG\_ADD\_IF\_NEW**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)              | <span data-ttu-id="2797a-140">Adiciona o cabeçalho somente se ele ainda não existir; caso contrário, um erro será retornado.</span><span class="sxs-lookup"><span data-stu-id="2797a-140">Adds the header only if it does not already exist; otherwise, an error is returned.</span></span>                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="2797a-141">**\_União de \_ sinalizador de ADDREQ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="2797a-141">**WINHTTP\_ADDREQ\_FLAG\_COALESCE**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                  | <span data-ttu-id="2797a-142">Mescla os cabeçalhos de mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="2797a-142">Merges headers of the same name.</span></span>                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="2797a-143">**\_ \_ \_ União de sinalizador de ADDREQ \_ de WinHTTP com \_ vírgula**</span><span class="sxs-lookup"><span data-stu-id="2797a-143">**WINHTTP\_ADDREQ\_FLAG\_COALESCE\_WITH\_COMMA**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)     | <span data-ttu-id="2797a-144">Mescla os cabeçalhos de mesmo nome usando uma vírgula.</span><span class="sxs-lookup"><span data-stu-id="2797a-144">Merges headers of the same name using a comma.</span></span> <span data-ttu-id="2797a-145">Por exemplo, adicionar "Accept: Text/ \* " seguido de "Accept: Audio/ \* " com esse sinalizador forma o cabeçalho único "Accept: Text/ \* , Audio/ \* ", fazendo com que o primeiro cabeçalho seja mesclado.</span><span class="sxs-lookup"><span data-stu-id="2797a-145">For example, adding "Accept: text/\*" followed by "Accept: audio/\*" with this flag forms the single header "Accept: text/\*, audio/\*", causing the first header found to be merged.</span></span> <span data-ttu-id="2797a-146">Cabe ao aplicativo de chamada garantir um esquema coeso em relação aos cabeçalhos mesclados/separados.</span><span class="sxs-lookup"><span data-stu-id="2797a-146">It is up to the calling application to ensure a cohesive scheme with respect to merged/separate headers.</span></span> |
| [<span data-ttu-id="2797a-147">**\_ \_ \_ União de sinalizador ADDREQ de WinHTTP \_ com \_ ponto e vírgula**</span><span class="sxs-lookup"><span data-stu-id="2797a-147">**WINHTTP\_ADDREQ\_FLAG\_COALESCE\_WITH\_SEMICOLON**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) | <span data-ttu-id="2797a-148">Mescla os cabeçalhos de mesmo nome usando um ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="2797a-148">Merges headers of the same name using a semicolon.</span></span>                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="2797a-149">**\_ \_ substituir sinalizador de ADDREQ de WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="2797a-149">**WINHTTP\_ADDREQ\_FLAG\_REPLACE**</span></span>](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders)                   | <span data-ttu-id="2797a-150">Substitui ou remove um cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="2797a-150">Replaces or removes a header.</span></span> <span data-ttu-id="2797a-151">Se o valor do cabeçalho estiver vazio e o cabeçalho for encontrado, ele será removido.</span><span class="sxs-lookup"><span data-stu-id="2797a-151">If the header value is empty and the header is found, it is removed.</span></span> <span data-ttu-id="2797a-152">Se o valor do cabeçalho não estiver vazio, o valor do cabeçalho será substituído.</span><span class="sxs-lookup"><span data-stu-id="2797a-152">If the header value is not empty, the header value is replaced.</span></span>                                                                                                                                                                            |



 

## <a name="sending-a-request"></a><span data-ttu-id="2797a-153">Enviando uma solicitação</span><span class="sxs-lookup"><span data-stu-id="2797a-153">Sending a Request</span></span>

<span data-ttu-id="2797a-154">A função [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) estabelece uma conexão com o servidor e envia a solicitação para o site especificado.</span><span class="sxs-lookup"><span data-stu-id="2797a-154">The [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function establishes a connection to the server and sends the request to the specified site.</span></span> <span data-ttu-id="2797a-155">Essa função requer um identificador [HINTERNET](hinternet-handles-in-winhttp.md) criado pelo [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span><span class="sxs-lookup"><span data-stu-id="2797a-155">This function requires an [HINTERNET](hinternet-handles-in-winhttp.md) handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest).</span></span> <span data-ttu-id="2797a-156">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) também pode enviar cabeçalhos adicionais ou informações opcionais.</span><span class="sxs-lookup"><span data-stu-id="2797a-156">[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) can also send additional headers or optional information.</span></span> <span data-ttu-id="2797a-157">As informações opcionais geralmente são usadas para operações que gravam informações no servidor, como PUT e POST.</span><span class="sxs-lookup"><span data-stu-id="2797a-157">The optional information is generally used for operations that write information to the server, such as PUT and POST.</span></span>

<span data-ttu-id="2797a-158">Depois que a função [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) enviar a solicitação, o aplicativo poderá usar as funções [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) e [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) no identificador [HINTERNET](hinternet-handles-in-winhttp.md) para baixar os recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="2797a-158">After the [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) function sends the request, the application can use the [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) and [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) functions on the [HINTERNET](hinternet-handles-in-winhttp.md) handle to download the server's resources.</span></span>

## <a name="posting-data-to-the-server"></a><span data-ttu-id="2797a-159">Postando dados no servidor</span><span class="sxs-lookup"><span data-stu-id="2797a-159">Posting Data to the Server</span></span>

<span data-ttu-id="2797a-160">Para postar dados em um servidor, o [*verbo http*](glossary.md) na chamada para [**WINHTTPOPENREQUEST**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) deve ser post ou PUT.</span><span class="sxs-lookup"><span data-stu-id="2797a-160">To post data to a server, the [*HTTP verb*](glossary.md) in the call to [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) must be either POST or PUT.</span></span> <span data-ttu-id="2797a-161">Quando [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) é chamado, o parâmetro *dwTotalLength* deve ser definido como o tamanho dos dados em bytes.</span><span class="sxs-lookup"><span data-stu-id="2797a-161">When [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) is called, the *dwTotalLength* parameter should be set to the size of the data in bytes.</span></span> <span data-ttu-id="2797a-162">Em seguida, use [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) para postar os dados no servidor.</span><span class="sxs-lookup"><span data-stu-id="2797a-162">Then use [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) to post the data to the server.</span></span>

<span data-ttu-id="2797a-163">Como alternativa, defina o parâmetro *lpOptional* de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) como o endereço de um buffer que contém os dados a serem postados no servidor.</span><span class="sxs-lookup"><span data-stu-id="2797a-163">Alternatively, set the *lpOptional* parameter of [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) to the address of a buffer that contains data to post to the server.</span></span> <span data-ttu-id="2797a-164">Ao usar essa técnica, você deve definir os parâmetros *dwOptionalLength* e *dwTotalLength* de [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) como o tamanho dos dados que estão sendo postados.</span><span class="sxs-lookup"><span data-stu-id="2797a-164">When using this technique, you must set both the *dwOptionalLength* and *dwTotalLength* parameters of [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) to be the size of the data being posted.</span></span> <span data-ttu-id="2797a-165">Chamar [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) dessa maneira elimina a necessidade de chamar [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).</span><span class="sxs-lookup"><span data-stu-id="2797a-165">Calling [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) in this manner eliminates the need to call [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata).</span></span>

## <a name="getting-information-about-a-request"></a><span data-ttu-id="2797a-166">Obtendo informações sobre uma solicitação</span><span class="sxs-lookup"><span data-stu-id="2797a-166">Getting Information About a Request</span></span>

<span data-ttu-id="2797a-167">A função [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) permite que um aplicativo recupere informações sobre uma solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="2797a-167">The [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) function allows an application to retrieve information about an HTTP request.</span></span> <span data-ttu-id="2797a-168">A função requer um identificador [HINTERNET](hinternet-handles-in-winhttp.md) criado pelo [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), um valor de nível de informação e um comprimento de buffer.</span><span class="sxs-lookup"><span data-stu-id="2797a-168">The function requires an [HINTERNET](hinternet-handles-in-winhttp.md) handle created by [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), an information level value, and a buffer length.</span></span> <span data-ttu-id="2797a-169">O [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) também aceita um buffer que armazena as informações e um índice de cabeçalho baseado em zero que enumera vários cabeçalhos com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="2797a-169">[**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders) also accepts a buffer that stores the information and a zero-based header index that enumerates multiple headers with the same name.</span></span>

<span data-ttu-id="2797a-170">Use qualquer um dos valores de nível de informação encontrados na página [**sinalizadores de informações de consulta**](query-info-flags.md) com um modificador para controlar o formato no qual as informações são armazenadas no parâmetro *lpvBuffer* de [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span><span class="sxs-lookup"><span data-stu-id="2797a-170">Use any of the information level values found on the [**Query Info Flags**](query-info-flags.md) page with a modifier to control the format in which the information is stored in the *lpvBuffer* parameter of [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders).</span></span>

## <a name="downloading-resources-from-the-web"></a><span data-ttu-id="2797a-171">Baixando recursos da Web</span><span class="sxs-lookup"><span data-stu-id="2797a-171">Downloading Resources from the Web</span></span>

<span data-ttu-id="2797a-172">Depois de abrir uma solicitação com a função [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) , enviá-la ao servidor com [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)e preparar o identificador de solicitação para receber uma resposta com [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), o aplicativo poderá usar as funções [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) e [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) para baixar o recurso do servidor http.</span><span class="sxs-lookup"><span data-stu-id="2797a-172">After opening a request with the [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) function, sending it to the server with [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), and preparing the request handle to receive a response with [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse), the application can use the [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) and [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) functions to download the resource from the HTTP server.</span></span>

<span data-ttu-id="2797a-173">O código de exemplo a seguir mostra como baixar um recurso com semântica de transação segura.</span><span class="sxs-lookup"><span data-stu-id="2797a-173">The following sample code shows how to download a resource with secure transaction semantics.</span></span> <span data-ttu-id="2797a-174">O código de exemplo inicializa a API (interface de programação de aplicativo) do WinHTTP, seleciona um servidor HTTPS de destino e, em seguida, abre e envia uma solicitação para esse recurso seguro.</span><span class="sxs-lookup"><span data-stu-id="2797a-174">The sample code initializes the WinHTTP application programming interface (API), selects a target HTTPS server, and then opens and sends a request for this secure resource.</span></span> <span data-ttu-id="2797a-175">[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) é usado com o identificador de solicitação para determinar a quantidade de dados disponível para download e, em seguida, [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) é usado para ler esses dados.</span><span class="sxs-lookup"><span data-stu-id="2797a-175">[**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) is used with the request handle to determine how much data is available for download, and then [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata) is used to read that data.</span></span> <span data-ttu-id="2797a-176">Esse processo é repetido até que todo o documento seja recuperado e exibido.</span><span class="sxs-lookup"><span data-stu-id="2797a-176">This process is repeated until the entire document has been retrieved and displayed.</span></span>


```C++
  DWORD dwSize = 0;
  DWORD dwDownloaded = 0;
  LPSTR pszOutBuffer;
  BOOL  bResults = FALSE;
  HINTERNET  hSession = NULL, 
             hConnect = NULL,
             hRequest = NULL;

  // Use WinHttpOpen to obtain a session handle.
  hSession = WinHttpOpen( L"WinHTTP Example/1.0",  
                          WINHTTP_ACCESS_TYPE_DEFAULT_PROXY,
                          WINHTTP_NO_PROXY_NAME, 
                          WINHTTP_NO_PROXY_BYPASS, 0 );

  // Specify an HTTP server.
  if( hSession )
    hConnect = WinHttpConnect( hSession, L"www.microsoft.com",
                               INTERNET_DEFAULT_HTTPS_PORT, 0 );

  // Create an HTTP request handle.
  if( hConnect )
    hRequest = WinHttpOpenRequest( hConnect, L"GET", NULL,
                                   NULL, WINHTTP_NO_REFERER, 
                                   WINHTTP_DEFAULT_ACCEPT_TYPES, 
                                   WINHTTP_FLAG_SECURE );

  // Send a request.
  if( hRequest )
    bResults = WinHttpSendRequest( hRequest,
                                   WINHTTP_NO_ADDITIONAL_HEADERS, 0,
                                   WINHTTP_NO_REQUEST_DATA, 0, 
                                   0, 0 );


  // End the request.
  if( bResults )
    bResults = WinHttpReceiveResponse( hRequest, NULL );

  // Keep checking for data until there is nothing left.
  if( bResults )
  {
    do 
    {
      // Check for available data.
      dwSize = 0;
      if( !WinHttpQueryDataAvailable( hRequest, &dwSize ) )
        printf( "Error %u in WinHttpQueryDataAvailable.\n",
                GetLastError( ) );

      // Allocate space for the buffer.
      pszOutBuffer = new char[dwSize+1];
      if( !pszOutBuffer )
      {
        printf( "Out of memory\n" );
        dwSize=0;
      }
      else
      {
        // Read the data.
        ZeroMemory( pszOutBuffer, dwSize+1 );

        if( !WinHttpReadData( hRequest, (LPVOID)pszOutBuffer, 
                              dwSize, &dwDownloaded ) )
          printf( "Error %u in WinHttpReadData.\n", GetLastError( ) );
        else
          printf( "%s", pszOutBuffer );

        // Free the memory allocated to the buffer.
        delete [] pszOutBuffer;
      }
    } while( dwSize > 0 );
  }


  // Report any errors.
  if( !bResults )
    printf( "Error %d has occurred.\n", GetLastError( ) );

  // Close any open handles.
  if( hRequest ) WinHttpCloseHandle( hRequest );
  if( hConnect ) WinHttpCloseHandle( hConnect );
  if( hSession ) WinHttpCloseHandle( hSession );
```



 

 



