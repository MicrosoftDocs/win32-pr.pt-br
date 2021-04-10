---
title: Sessões HTTP
description: Os recursos na WWW são acessados usando http.
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85b0b4d30bc86c588495a55ed4867a4084c43a09
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084656"
---
# <a name="http-sessions"></a><span data-ttu-id="e6592-103">Sessões HTTP</span><span class="sxs-lookup"><span data-stu-id="e6592-103">HTTP Sessions</span></span>

<span data-ttu-id="e6592-104">O WinINet permite que você acesse recursos no World Wide Web (WWW).</span><span class="sxs-lookup"><span data-stu-id="e6592-104">WinINet enables you to access resources on the World Wide Web (WWW).</span></span> <span data-ttu-id="e6592-105">Esses recursos podem ser acessados diretamente usando [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para obter mais informações, consulte [acessando URLs diretamente](handling-uniform-resource-locators.md)).</span><span class="sxs-lookup"><span data-stu-id="e6592-105">These resources can be accessed directly by using [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for more information, see [Accessing URLs Directly](handling-uniform-resource-locators.md)).</span></span>

<span data-ttu-id="e6592-106">Os recursos na WWW são acessados usando http.</span><span class="sxs-lookup"><span data-stu-id="e6592-106">Resources on the WWW are accessed by using http.</span></span> <span data-ttu-id="e6592-107">As funções HTTP lidam com os protocolos subjacentes, permitindo que seu aplicativo acesse as informações na WWW.</span><span class="sxs-lookup"><span data-stu-id="e6592-107">The HTTP functions handle the underlying protocols, while allowing your application to access information on the WWW.</span></span> <span data-ttu-id="e6592-108">À medida que o protocolo HTTP evolui, os protocolos subjacentes são atualizados para manter o comportamento da função.</span><span class="sxs-lookup"><span data-stu-id="e6592-108">As the HTTP protocol evolves, the underlying protocols are updated to maintain function behavior.</span></span>

<span data-ttu-id="e6592-109">O diagrama a seguir mostra as relações das funções que são usadas com o protocolo HTTP.</span><span class="sxs-lookup"><span data-stu-id="e6592-109">The following diagram shows the relationships of the functions that are used with the HTTP protocol.</span></span> <span data-ttu-id="e6592-110">As caixas sombreadas representam funções que retornam identificadores [**HINTERNET**](appendix-a-hinternet-handles.md) , enquanto as caixas simples representam funções que usam o identificador **HINTERNET** criado pela função na qual dependem.</span><span class="sxs-lookup"><span data-stu-id="e6592-110">The shaded boxes represent functions that return [**HINTERNET**](appendix-a-hinternet-handles.md) handles, while the plain boxes represent functions that use the **HINTERNET** handle created by the function on which they depend.</span></span>

![funções do Wininet usadas para http](images/ax-wnt05.png)

<span data-ttu-id="e6592-112">Para obter mais informações, consulte [HINTERNET Handles](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="e6592-112">For more information, see [HINTERNET Handles](appendix-a-hinternet-handles.md).</span></span>

## <a name="using-the-wininet-functions-to-access-the-www"></a><span data-ttu-id="e6592-113">Usando as funções WinINet para acessar a WWW</span><span class="sxs-lookup"><span data-stu-id="e6592-113">Using the WinINet Functions to Access the WWW</span></span>

-   [<span data-ttu-id="e6592-114">Iniciando uma conexão com a WWW</span><span class="sxs-lookup"><span data-stu-id="e6592-114">Initiating a Connection to the WWW</span></span>](#initiating-a-connection-to-the-www)
-   [<span data-ttu-id="e6592-115">Abrindo uma solicitação</span><span class="sxs-lookup"><span data-stu-id="e6592-115">Opening a Request</span></span>](#opening-a-request)
-   [<span data-ttu-id="e6592-116">Adicionando cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="e6592-116">Adding Request Headers</span></span>](#adding-request-headers)
-   [<span data-ttu-id="e6592-117">Enviando uma solicitação</span><span class="sxs-lookup"><span data-stu-id="e6592-117">Sending a Request</span></span>](#sending-a-request)
-   [<span data-ttu-id="e6592-118">Postando dados no servidor</span><span class="sxs-lookup"><span data-stu-id="e6592-118">Posting Data to the Server</span></span>](#posting-data-to-the-server)
-   [<span data-ttu-id="e6592-119">Obtendo informações sobre uma solicitação</span><span class="sxs-lookup"><span data-stu-id="e6592-119">Getting Information About a Request</span></span>](#getting-information-about-a-request)
-   [<span data-ttu-id="e6592-120">Baixando recursos da WWW</span><span class="sxs-lookup"><span data-stu-id="e6592-120">Downloading Resources from the WWW</span></span>](#downloading-resources-from-the-www)

<span data-ttu-id="e6592-121">As funções a seguir são usadas durante sessões HTTP para acessar a WWW.</span><span class="sxs-lookup"><span data-stu-id="e6592-121">The following functions are used during HTTP sessions to access the WWW.</span></span>



| <span data-ttu-id="e6592-122">Função</span><span class="sxs-lookup"><span data-stu-id="e6592-122">Function</span></span>                                               | <span data-ttu-id="e6592-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="e6592-123">Description</span></span>                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6592-124">**HttpAddRequestHeaders**</span><span class="sxs-lookup"><span data-stu-id="e6592-124">**HttpAddRequestHeaders**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | <span data-ttu-id="e6592-125">Adiciona cabeçalhos de solicitação HTTP ao identificador de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="e6592-125">Adds HTTP request headers to the HTTP request handle.</span></span> <span data-ttu-id="e6592-126">Essa função requer um identificador criado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="e6592-126">This function requires a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                 |
| [<span data-ttu-id="e6592-127">**HttpOpenRequest**</span><span class="sxs-lookup"><span data-stu-id="e6592-127">**HttpOpenRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | <span data-ttu-id="e6592-128">Abre um identificador de solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="e6592-128">Opens an HTTP request handle.</span></span> <span data-ttu-id="e6592-129">Essa função requer um identificador criado pelo [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="e6592-129">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                                                         |
| [<span data-ttu-id="e6592-130">**HttpQueryInfo**</span><span class="sxs-lookup"><span data-stu-id="e6592-130">**HttpQueryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | <span data-ttu-id="e6592-131">Consulta informações sobre uma solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="e6592-131">Queries information about an HTTP request.</span></span> <span data-ttu-id="e6592-132">Essa função requer um identificador criado pela função [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="e6592-132">This function requires a handle created by the [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> |
| [<span data-ttu-id="e6592-133">**HttpSendRequest**</span><span class="sxs-lookup"><span data-stu-id="e6592-133">**HttpSendRequest**</span></span>](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | <span data-ttu-id="e6592-134">Envia a solicitação HTTP especificada para o servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="e6592-134">Sends the specified HTTP request to the HTTP server.</span></span> <span data-ttu-id="e6592-135">Essa função requer um identificador criado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="e6592-135">This function requires a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                  |
| [<span data-ttu-id="e6592-136">**InternetErrorDlg**</span><span class="sxs-lookup"><span data-stu-id="e6592-136">**InternetErrorDlg**</span></span>](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | <span data-ttu-id="e6592-137">Exibe caixas de diálogo predefinidas para condições comuns de erro da Internet.</span><span class="sxs-lookup"><span data-stu-id="e6592-137">Displays predefined dialog boxes for common Internet error conditions.</span></span> <span data-ttu-id="e6592-138">Essa função requer o identificador usado na chamada para [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="e6592-138">This function requires the handle used in the call to [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span>                     |



 

### <a name="initiating-a-connection-to-the-www"></a><span data-ttu-id="e6592-139">Iniciando uma conexão com a WWW</span><span class="sxs-lookup"><span data-stu-id="e6592-139">Initiating a Connection to the WWW</span></span>

<span data-ttu-id="e6592-140">Para iniciar uma conexão com a WWW, o aplicativo deve chamar a função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) no [**HINTERNET**](appendix-a-hinternet-handles.md) raiz retornado por [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="e6592-140">To start a connection to the WWW, the application must call the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function on the root [**HINTERNET**](appendix-a-hinternet-handles.md) returned by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="e6592-141">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) deve estabelecer uma sessão http declarando o \_ tipo de serviço http do serviço de Internet \_ .</span><span class="sxs-lookup"><span data-stu-id="e6592-141">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) must establish an HTTP session by declaring the INTERNET\_SERVICE\_HTTP service type.</span></span> <span data-ttu-id="e6592-142">Para obter mais informações sobre como usar o [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), consulte [usando o InternetConnect](enabling-internet-functionality.md).</span><span class="sxs-lookup"><span data-stu-id="e6592-142">For more information on using [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), see [Using InternetConnect](enabling-internet-functionality.md).</span></span>

### <a name="opening-a-request"></a><span data-ttu-id="e6592-143">Abrindo uma solicitação</span><span class="sxs-lookup"><span data-stu-id="e6592-143">Opening a Request</span></span>

<span data-ttu-id="e6592-144">A função [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) abre uma solicitação HTTP e retorna um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) que pode ser usado pelas outras funções http.</span><span class="sxs-lookup"><span data-stu-id="e6592-144">The [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function opens an HTTP request and returns an [**HINTERNET**](appendix-a-hinternet-handles.md) handle that can be used by the other HTTP functions.</span></span> <span data-ttu-id="e6592-145">Ao contrário das outras funções abertas (como [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), o [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) não envia a solicitação para a Internet quando chamada.</span><span class="sxs-lookup"><span data-stu-id="e6592-145">Unlike the other open functions (such as [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) does not send the request to the Internet when called.</span></span> <span data-ttu-id="e6592-146">A função [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) envia a solicitação e estabelece uma conexão pela rede.</span><span class="sxs-lookup"><span data-stu-id="e6592-146">The [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) function sends the request and establishes a connection over the network.</span></span>

<span data-ttu-id="e6592-147">O [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usa um identificador de sessão http criado por [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e um verbo http, nome do objeto, Cadeia de caracteres de versão, referenciador, tipos de aceitação, sinalizadores e valor de contexto.</span><span class="sxs-lookup"><span data-stu-id="e6592-147">[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) takes an HTTP session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and an HTTP verb, object name, version string, referrer, accept types, flags, and context value.</span></span>

<span data-ttu-id="e6592-148">O verbo HTTP é uma cadeia de caracteres a ser usada na solicitação.</span><span class="sxs-lookup"><span data-stu-id="e6592-148">The HTTP verb is a string to be used in the request.</span></span> <span data-ttu-id="e6592-149">Os verbos HTTP comuns usados em solicitações incluem GET, PUT e POST.</span><span class="sxs-lookup"><span data-stu-id="e6592-149">Common HTTP verbs used in requests include GET, PUT, and POST.</span></span> <span data-ttu-id="e6592-150">Se esse valor for definido como **NULL**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usará o valor padrão Get.</span><span class="sxs-lookup"><span data-stu-id="e6592-150">If this value is set to **NULL**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) uses the default value GET.</span></span>

<span data-ttu-id="e6592-151">O nome do objeto é uma cadeia de caracteres que contém o nome do objeto de destino do verbo HTTP especificado.</span><span class="sxs-lookup"><span data-stu-id="e6592-151">The object name is a string that contains the name of the specified HTTP verb's target object.</span></span> <span data-ttu-id="e6592-152">Geralmente, esse é um nome de arquivo, um módulo executável ou um especificador de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e6592-152">This is generally a file name, an executable module, or a search specifier.</span></span> <span data-ttu-id="e6592-153">Se o nome do objeto fornecido for uma cadeia de caracteres vazia, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) procurará a página padrão.</span><span class="sxs-lookup"><span data-stu-id="e6592-153">If the object name supplied is an empty string, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) looks for the default page.</span></span>

<span data-ttu-id="e6592-154">A cadeia de caracteres da versão deve conter a versão HTTP.</span><span class="sxs-lookup"><span data-stu-id="e6592-154">The version string should contain the HTTP version.</span></span> <span data-ttu-id="e6592-155">Se esse parâmetro for **nulo**, a função usará "" http/1.1 "".</span><span class="sxs-lookup"><span data-stu-id="e6592-155">If this parameter is **NULL**, the function uses ""HTTP/1.1"".</span></span>

<span data-ttu-id="e6592-156">O referenciador especifica o endereço do documento do qual o nome do objeto foi obtido.</span><span class="sxs-lookup"><span data-stu-id="e6592-156">The referrer specifies the address of the document from which the object name was obtained.</span></span> <span data-ttu-id="e6592-157">Se esse parâmetro for **NULL**, nenhum referenciador será especificado.</span><span class="sxs-lookup"><span data-stu-id="e6592-157">If this parameter is **NULL**, no referrer is specified.</span></span>

<span data-ttu-id="e6592-158">A cadeia de caracteres terminada em **nulo** que contém os tipos de aceitação indica os tipos de conteúdo aceitos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e6592-158">The **null**-terminated string that contains the accept types indicates the content types accepted by the application.</span></span> <span data-ttu-id="e6592-159">Definir esse parâmetro como **NULL** indica que nenhum tipo de conteúdo é aceito pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e6592-159">Setting this parameter to **NULL** indicates that no content types are accepted by the application.</span></span> <span data-ttu-id="e6592-160">Se uma cadeia de caracteres vazia for fornecida, o aplicativo indicará que aceita somente documentos do tipo "" Text/ \* "".</span><span class="sxs-lookup"><span data-stu-id="e6592-160">If an empty string is supplied, the application indicates it accepts only documents of type ""text/\*"".</span></span> <span data-ttu-id="e6592-161">O valor "" Text/ \* "" indica documentos somente texto — não imagens ou outros arquivos binários.</span><span class="sxs-lookup"><span data-stu-id="e6592-161">The value ""text/\*"" indicates text-only documents—not pictures or other binary files.</span></span>

<span data-ttu-id="e6592-162">Os valores do sinalizador controlam o cache, os cookies e os problemas de segurança.</span><span class="sxs-lookup"><span data-stu-id="e6592-162">The flag values control caching, cookies, and security issues.</span></span> <span data-ttu-id="e6592-163">Para o Microsoft Network (MSN), o NTLM e outros tipos de autenticação, defina o sinalizador [Internet \_ Flag \_ manter \_ conexão](api-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="e6592-163">For Microsoft Network (MSN), NTLM, and other types of authentication, set the [INTERNET\_FLAG\_KEEP\_CONNECTION](api-flags.md) flag.</span></span>

<span data-ttu-id="e6592-164">Se o [sinalizador \_ \_ assíncrono de sinalizador da Internet](api-flags.md) tiver sido definido na chamada para [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), um valor de contexto diferente de zero deverá ser definido para a operação assíncrona adequada.</span><span class="sxs-lookup"><span data-stu-id="e6592-164">If the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag was set in the call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), a nonzero context value should be set for proper asynchronous operation.</span></span>

<span data-ttu-id="e6592-165">O exemplo a seguir é uma chamada de exemplo para [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="e6592-165">The following example is a sample call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a><span data-ttu-id="e6592-166">Adicionando cabeçalhos de solicitação</span><span class="sxs-lookup"><span data-stu-id="e6592-166">Adding Request Headers</span></span>

<span data-ttu-id="e6592-167">A função [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) permite que os aplicativos adicionem um ou mais cabeçalhos de solicitação à solicitação inicial.</span><span class="sxs-lookup"><span data-stu-id="e6592-167">The [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) function enables applications to add one or more request headers to the initial request.</span></span> <span data-ttu-id="e6592-168">Essa função permite que um aplicativo acrescente cabeçalhos de formato livre adicionais ao identificador de solicitação HTTP; Ele é destinado ao uso por aplicativos sofisticados que exigem controle preciso sobre a solicitação enviada ao servidor HTTP.</span><span class="sxs-lookup"><span data-stu-id="e6592-168">This function allows an application to append additional free-format headers to the HTTP request handle; it is intended for use by sophisticated applications that require precise control over the request sent to the HTTP server.</span></span>

<span data-ttu-id="e6592-169">[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) precisa de um identificador de solicitação HTTP criado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), uma cadeia de caracteres que contém os cabeçalhos, o comprimento dos cabeçalhos e os modificadores.</span><span class="sxs-lookup"><span data-stu-id="e6592-169">[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) needs an HTTP request handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), a string that contains the headers, the length of the headers, and modifiers.</span></span>

### <a name="sending-a-request"></a><span data-ttu-id="e6592-170">Enviando uma solicitação</span><span class="sxs-lookup"><span data-stu-id="e6592-170">Sending a Request</span></span>

<span data-ttu-id="e6592-171">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) estabelece uma conexão com a Internet e envia a solicitação para o site especificado.</span><span class="sxs-lookup"><span data-stu-id="e6592-171">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) establishes a connection to the Internet and sends the request to the specified site.</span></span> <span data-ttu-id="e6592-172">Essa função requer um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) criado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="e6592-172">This function requires an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="e6592-173">O [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) também pode enviar cabeçalhos adicionais ou informações opcionais.</span><span class="sxs-lookup"><span data-stu-id="e6592-173">[**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) can also send additional headers or optional information.</span></span> <span data-ttu-id="e6592-174">As informações opcionais geralmente são usadas para operações que gravam informações no servidor, como PUT e POST.</span><span class="sxs-lookup"><span data-stu-id="e6592-174">The optional information is generally used for operations that write information to the server, such as PUT and POST.</span></span>

<span data-ttu-id="e6592-175">Depois que o [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) envia a solicitação, o aplicativo pode usar as funções [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) no identificador [**HINTERNET**](appendix-a-hinternet-handles.md) criado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) para baixar os recursos do servidor.</span><span class="sxs-lookup"><span data-stu-id="e6592-175">After [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) sends the request, the application can use the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) functions on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) to download the server's resources.</span></span>

### <a name="posting-data-to-the-server"></a><span data-ttu-id="e6592-176">Postando dados no servidor</span><span class="sxs-lookup"><span data-stu-id="e6592-176">Posting Data to the Server</span></span>

<span data-ttu-id="e6592-177">Para postar dados em um servidor, o verbo HTTP na chamada para [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) deve ser post ou PUT.</span><span class="sxs-lookup"><span data-stu-id="e6592-177">To post data to a server, the HTTP verb in the call to [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) must be either POST or PUT.</span></span> <span data-ttu-id="e6592-178">O endereço do buffer que contém os dados de POSTAgem deve ser passado para o parâmetro *lpOptional* em [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="e6592-178">The address of the buffer that contains the POST data should then be passed to the *lpOptional* parameter in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="e6592-179">O parâmetro *dwOptionalLength* deve ser definido como o tamanho dos dados.</span><span class="sxs-lookup"><span data-stu-id="e6592-179">The *dwOptionalLength* parameter should be set to the size of the data.</span></span>

<span data-ttu-id="e6592-180">Você também pode usar a função [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) para postar dados em um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) enviado usando o [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).</span><span class="sxs-lookup"><span data-stu-id="e6592-180">You can also use the [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) function to post data on an [**HINTERNET**](appendix-a-hinternet-handles.md) handle sent using [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).</span></span>

### <a name="getting-information-about-a-request"></a><span data-ttu-id="e6592-181">Obtendo informações sobre uma solicitação</span><span class="sxs-lookup"><span data-stu-id="e6592-181">Getting Information About a Request</span></span>

<span data-ttu-id="e6592-182">O [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) permite que um aplicativo recupere informações sobre uma solicitação HTTP.</span><span class="sxs-lookup"><span data-stu-id="e6592-182">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) allows an application to retrieve information about an HTTP request.</span></span> <span data-ttu-id="e6592-183">A função requer um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) criado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), um valor de nível de informação e um comprimento de buffer.</span><span class="sxs-lookup"><span data-stu-id="e6592-183">The function requires an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), an information level value, and a buffer length.</span></span> <span data-ttu-id="e6592-184">O [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) também aceita um buffer que armazena as informações e um índice de cabeçalho baseado em zero que enumera vários cabeçalhos com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="e6592-184">[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) also accepts a buffer that stores the information and a zero-based header index that enumerates multiple headers with the same name.</span></span>

### <a name="downloading-resources-from-the-www"></a><span data-ttu-id="e6592-185">Baixando recursos da WWW</span><span class="sxs-lookup"><span data-stu-id="e6592-185">Downloading Resources from the WWW</span></span>

<span data-ttu-id="e6592-186">Depois de abrir uma solicitação com [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e enviá-la ao servidor [**com HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), o aplicativo poderá usar as funções [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)e [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) para baixar o recurso do servidor http.</span><span class="sxs-lookup"><span data-stu-id="e6592-186">After opening a request with [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and sending it to the server with [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), the application can use the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), and [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) functions to download the resource from the HTTP server.</span></span>

<span data-ttu-id="e6592-187">O exemplo a seguir baixa um recurso.</span><span class="sxs-lookup"><span data-stu-id="e6592-187">The following example downloads a resource.</span></span> <span data-ttu-id="e6592-188">A função aceita o identificador para a janela atual, o número de identificação de uma caixa de edição e um identificador [**HINTERNET**](appendix-a-hinternet-handles.md) criado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e enviado por [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="e6592-188">The function accepts the handle to the current window, the identification number of an edit box, and an [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and sent by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="e6592-189">Ele usa [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) para determinar o tamanho do recurso e, em seguida, baixa-o usando [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="e6592-189">It uses [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) to determine the size of the resource and then downloads it using [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span> <span data-ttu-id="e6592-190">O conteúdo é exibido na caixa de edição.</span><span class="sxs-lookup"><span data-stu-id="e6592-190">The contents are then displayed in the edit box.</span></span>


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR lpszData;    // buffer for the data
    DWORD  dwSize;       // size of the data available
    DWORD  dwDownloaded; // size of the downloaded data
    DWORD  dwSizeSum=0;  // size of the data in the textbox
    LPTSTR lpszHolding;  // buffer to merge the textbox data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            printf("InternetQueryDataAvailable failed (%d)\n", GetLastError());
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,
                                 (LPVOID)lpszData,
                                 dwSize,
                                 &dwDownloaded))
            {
                printf("InternetReadFile failed (%d)\n", GetLastError());
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the data buffer
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];

                // Check if there has been any data written
                // to the textbox.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the textbox if any
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding,
                                   dwSizeSum);

                    // Add a null terminator at the end of the
                    // textbox data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string.
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + dwDownloaded + 1;
                LPTSTR* ppszDestEnd = 0;
                size_t* pcchRemaining = 0;

                // Add the new data to the holding buffer
                HRESULT hr = StringCchCatEx(lpszHolding,
                                            cchDest,
                                            lpszData,
                                            ppszDestEnd,
                                            pcchRemaining,
                                            STRSAFE_NO_TRUNCATION);

                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the textbox.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to the
                    // textbox data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                        break;
                    else
                    {
                    //  TODO: Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    return TRUE;
}
```



> [!Note]  
> <span data-ttu-id="e6592-191">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="e6592-191">WinINet does not support server implementations.</span></span> <span data-ttu-id="e6592-192">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="e6592-192">In addition, it should not be used from a service.</span></span> <span data-ttu-id="e6592-193">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="e6592-193">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 