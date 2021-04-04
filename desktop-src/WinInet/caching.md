---
title: Caching (Internet do Windows)
description: As funções do WinINet têm suporte de cache interno simples, mas flexível.
ms.assetid: 44c268c9-a745-432a-8540-60d7e7d2cb2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e753d826ec3abe580b94158296562208dcbed44
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085063"
---
# <a name="caching-windows-internet"></a><span data-ttu-id="eee51-103">Caching (Internet do Windows)</span><span class="sxs-lookup"><span data-stu-id="eee51-103">Caching (Windows Internet)</span></span>

<span data-ttu-id="eee51-104">As funções do WinINet têm suporte de cache interno simples, mas flexível.</span><span class="sxs-lookup"><span data-stu-id="eee51-104">The WinINet functions have simple, yet flexible, built-in caching support.</span></span> <span data-ttu-id="eee51-105">Todos os dados recuperados da rede são armazenados em cache no disco rígido e recuperados para solicitações subsequentes.</span><span class="sxs-lookup"><span data-stu-id="eee51-105">Any data retrieved from the network is cached on the hard disk and retrieved for subsequent requests.</span></span> <span data-ttu-id="eee51-106">O aplicativo pode controlar o cache em cada solicitação.</span><span class="sxs-lookup"><span data-stu-id="eee51-106">The application can control the caching on each request.</span></span> <span data-ttu-id="eee51-107">Para solicitações HTTP do servidor, a maioria dos cabeçalhos recebidos também é armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-107">For http requests from the server, most headers received are also cached.</span></span> <span data-ttu-id="eee51-108">Quando uma solicitação HTTP é satisfeita no cache, os cabeçalhos armazenados em cache também são retornados ao chamador.</span><span class="sxs-lookup"><span data-stu-id="eee51-108">When an http request is satisfied from the cache, the cached headers are also returned to the caller.</span></span> <span data-ttu-id="eee51-109">Isso torna o download de dados contínuo, se os dados são provenientes do cache ou da rede.</span><span class="sxs-lookup"><span data-stu-id="eee51-109">This makes data download seamless, whether the data is coming from the cache or from the network.</span></span>

<span data-ttu-id="eee51-110">Os aplicativos devem alocar corretamente um buffer para obter os resultados desejados ao usar as funções de cache de URL persistentes.</span><span class="sxs-lookup"><span data-stu-id="eee51-110">Applications must properly allocate a buffer in order to get the desired results when using the persistent URL caching functions.</span></span> <span data-ttu-id="eee51-111">Para obter mais informações, consulte [usando buffers](appendix-b-using-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="eee51-111">For more information, see [Using Buffers](appendix-b-using-buffers.md).</span></span>

## <a name="cache-behavior-during-response-processing"></a><span data-ttu-id="eee51-112">Comportamento de cache durante o processamento de resposta</span><span class="sxs-lookup"><span data-stu-id="eee51-112">Cache Behavior During Response Processing</span></span>

<span data-ttu-id="eee51-113">O cache do WinINet é compatível com as diretivas HTTP Cache-Control descritas na RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="eee51-113">The WinINet cache is compliant with the HTTP cache-control directives described in RFC 2616.</span></span> <span data-ttu-id="eee51-114">As diretivas de controle de cache e os sinalizadores de conjunto de aplicativos determinam o que pode ser armazenado em cache; no entanto, o WinINet determina o que realmente é armazenado em cache com base no seguinte critério:</span><span class="sxs-lookup"><span data-stu-id="eee51-114">The cache-control directives and application set flags determine what may be cached; however, WinINet determines what is actually cached based on the following criterion:</span></span>

-   <span data-ttu-id="eee51-115">O WinINet apenas armazena em cache as respostas HTTP e FTP.</span><span class="sxs-lookup"><span data-stu-id="eee51-115">WinINet only caches HTTP and FTP responses.</span></span>
-   <span data-ttu-id="eee51-116">Somente as respostas bem compostas podem ser armazenadas por um cache e usadas em uma resposta a uma solicitação subsequente.</span><span class="sxs-lookup"><span data-stu-id="eee51-116">Only well behaved responses may be stored by a cache and used in a reply to a subsequent Request.</span></span> <span data-ttu-id="eee51-117">As respostas bem compostas são definidas como respostas que retornam com êxito.</span><span class="sxs-lookup"><span data-stu-id="eee51-117">Well behaved responses are defined as responses that return successfully.</span></span>
-   <span data-ttu-id="eee51-118">Por padrão, o WinINet armazenará em cache as respostas bem-sucedidas, a menos que uma diretiva de controle de cache do servidor ou um sinalizador definido pelo aplicativo denotasse especificamente que a resposta não pode ser armazenada em cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-118">By default, WinINet will cache successful responses unless either a cache-control directive from the server, or an application-defined flag specifically denote that the response may not be cached.</span></span>
-   <span data-ttu-id="eee51-119">Em geral, as respostas para o verbo GET serão armazenadas em cache se os requisitos listados acima forem atendidos.</span><span class="sxs-lookup"><span data-stu-id="eee51-119">In general, responses to the GET verb are cached if the requirements listed above are met.</span></span> <span data-ttu-id="eee51-120">As respostas aos verbos PUT e POST não são armazenadas em cache em nenhuma circunstância.</span><span class="sxs-lookup"><span data-stu-id="eee51-120">Responses to PUT and POST verbs are not cached under any circumstances.</span></span>
-   <span data-ttu-id="eee51-121">Os itens serão armazenados em cache mesmo quando o cache estiver cheio.</span><span class="sxs-lookup"><span data-stu-id="eee51-121">Items will be cached even when the cache is full.</span></span> <span data-ttu-id="eee51-122">Se um item adicionado for colocar o cache sobre o limite de tamanho, a recuperação de cache será agendada.</span><span class="sxs-lookup"><span data-stu-id="eee51-122">If an added item is puts the cache over the size limit, the cache scavenger is scheduled.</span></span> <span data-ttu-id="eee51-123">Por padrão, não há garantia de que os itens permaneçam mais de 10 minutos no cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-123">By default, items are not guaranteed to remain more than 10 minutes in the cache.</span></span> <span data-ttu-id="eee51-124">Para obter mais informações, consulte a seção [recuperação de cache](#cache-scavenger) abaixo.</span><span class="sxs-lookup"><span data-stu-id="eee51-124">For more information, see the [Cache Scavenger](#cache-scavenger) section below.</span></span>
-   <span data-ttu-id="eee51-125">O HTTPS é armazenado em cache por padrão.</span><span class="sxs-lookup"><span data-stu-id="eee51-125">Https is cached by default.</span></span> <span data-ttu-id="eee51-126">Isso é gerenciado por uma configuração global que não pode ser substituída por diretivas de cache definidas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="eee51-126">This is managed by a global setting that cannot be overridden by application-defined cache directives.</span></span> <span data-ttu-id="eee51-127">Para substituir a configuração global, selecione o miniaplicativo opções da Internet no painel de controle e vá para a guia Avançado. Marque a caixa "não salvar páginas criptografadas no disco" na seção "segurança".</span><span class="sxs-lookup"><span data-stu-id="eee51-127">To override the global setting, select the Internet Options applet in the control panel, and go to the advanced tab. Check the "Do not save encrypted pages to disk" box under the "Security" section.</span></span>

## <a name="cache-scavenger"></a><span data-ttu-id="eee51-128">Recuperação de cache</span><span class="sxs-lookup"><span data-stu-id="eee51-128">Cache Scavenger</span></span>

<span data-ttu-id="eee51-129">A recuperação de cache limpa periodicamente os itens do cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-129">The cache scavenger periodically cleans items from the cache.</span></span> <span data-ttu-id="eee51-130">Se um item for adicionado ao cache e o cache estiver cheio, o item será adicionado ao cache e a recuperação de cache será agendada.</span><span class="sxs-lookup"><span data-stu-id="eee51-130">If an item is added to the cache and the cache is full, the item is added to the cache and the cache scavenger is scheduled.</span></span> <span data-ttu-id="eee51-131">Se a recuperação do cache concluir uma rodada de eliminação e o cache não tiver atingido o limite de cache, a recuperação será agendada para outra rodada quando outro item for adicionado ao cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-131">If the cache scavenger completes a round of scavenging and the cache has not reached the cache limit, the scavenger is scheduled for another round when another item is added to the cache.</span></span> <span data-ttu-id="eee51-132">Em geral, a recuperação é agendada quando um item adicionado coloca o cache sobre seu limite de tamanho.</span><span class="sxs-lookup"><span data-stu-id="eee51-132">In general, the scavenger is scheduled when an added item puts the cache over its size limit.</span></span> <span data-ttu-id="eee51-133">Por padrão, o tempo de vida mínimo no cache é definido como 10 minutos, a menos que especificado de outra forma em uma diretiva de controle de cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-133">By default, the minimum time to live in the cache is set to 10 minutes unless otherwise specified in a cache-control directive.</span></span> <span data-ttu-id="eee51-134">Quando o cache de recuperação é iniciado, não há nenhuma garantia de que os itens mais antigos sejam os primeiros a serem excluídos do cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-134">When the cache scavenger is initiated, there is no guarantee that the oldest items are the first to be deleted from the cache.</span></span>

<span data-ttu-id="eee51-135">O cache é compartilhado entre todos os aplicativos WinINet no computador para o mesmo usuário.</span><span class="sxs-lookup"><span data-stu-id="eee51-135">The cache is shared across all WinINet applications on the computer for the same user.</span></span> <span data-ttu-id="eee51-136">A partir do Windows Vista e do Windows Server 2008, o tamanho do cache é definido como 1/32 º do tamanho do disco, com um tamanho mínimo de 8MB e um tamanho máximo de 50 MB.</span><span class="sxs-lookup"><span data-stu-id="eee51-136">Starting with Windows Vista and Windows Server 2008 the cache size is set to 1/32nd the size of the disk, with a minimum size of 8MB and a maximum size of 50MB.</span></span>

## <a name="using-flags-to-control-caching"></a><span data-ttu-id="eee51-137">Usando sinalizadores para controlar o cache</span><span class="sxs-lookup"><span data-stu-id="eee51-137">Using Flags to Control Caching</span></span>

<span data-ttu-id="eee51-138">Os sinalizadores de cache permitem que um aplicativo controle quando e como ele usa o cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-138">The caching flags allow an application to control when and how it uses the cache.</span></span> <span data-ttu-id="eee51-139">Esses sinalizadores podem ser usados sozinhos ou em combinação com o parâmetro *dwFlags* em funções que acessam informações ou recursos na Internet.</span><span class="sxs-lookup"><span data-stu-id="eee51-139">These flags can be used alone or in combination with the *dwFlags* parameter in functions that access information or resources on the Internet.</span></span> <span data-ttu-id="eee51-140">Por padrão, as funções armazenam todos os dados baixados da Internet.</span><span class="sxs-lookup"><span data-stu-id="eee51-140">By default, the functions store all data downloaded from the Internet.</span></span>

<span data-ttu-id="eee51-141">Os sinalizadores a seguir podem ser usados para controlar o cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-141">The following flags can be used to control caching.</span></span>



| <span data-ttu-id="eee51-142">Valor</span><span class="sxs-lookup"><span data-stu-id="eee51-142">Value</span></span>                                                                                                                                                  | <span data-ttu-id="eee51-143">Significado</span><span class="sxs-lookup"><span data-stu-id="eee51-143">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee51-144">**CACHE de sinalizador da INTERNET \_ \_ \_ assíncrono**</span><span class="sxs-lookup"><span data-stu-id="eee51-144">**INTERNET\_FLAG\_CACHE\_ASYNC**</span></span>](api-flags.md)                                                                            | <span data-ttu-id="eee51-145">Este sinalizador não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="eee51-145">This flag has no effect.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="eee51-146">**CACHE de sinalizador da INTERNET \_ \_ \_ se \_ net \_ falhar**</span><span class="sxs-lookup"><span data-stu-id="eee51-146">**INTERNET\_FLAG\_CACHE\_IF\_NET\_FAIL**</span></span>](api-flags.md)                                                              | <span data-ttu-id="eee51-147">Retorna o recurso do cache se a solicitação de rede para o recurso falhar devido a um [erro \_ de \_ \_ redefinição de conexão com a Internet](wininet-errors.md) ou [erro a \_ Internet \_ não pode \_ se conectar](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="eee51-147">Returns the resource from the cache if the network request for the resource fails due to an [ERROR\_INTERNET\_CONNECTION\_RESET](wininet-errors.md) or [ERROR\_INTERNET\_CANNOT\_CONNECT](wininet-errors.md) error.</span></span> <span data-ttu-id="eee51-148">Esse sinalizador é usado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="eee51-148">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>                                                                                                              |
| [<span data-ttu-id="eee51-149">**sinalizador da INTERNET não \_ \_ \_ cache**</span><span class="sxs-lookup"><span data-stu-id="eee51-149">**INTERNET\_FLAG\_DONT\_CACHE**</span></span>](api-flags.md)                                                                              | <span data-ttu-id="eee51-150">Não armazena em cache os dados, seja localmente ou em qualquer gateway.</span><span class="sxs-lookup"><span data-stu-id="eee51-150">Does not cache the data, either locally or in any gateways.</span></span> <span data-ttu-id="eee51-151">Idêntico ao valor preferencial, o [**sinalizador da Internet \_ \_ não \_ \_ grava cache**](api-flags.md).</span><span class="sxs-lookup"><span data-stu-id="eee51-151">Identical to the preferred value, [**INTERNET\_FLAG\_NO\_CACHE\_WRITE**](api-flags.md).</span></span>                                                                                                                                                                                                                                                                                 |
|                                                                                                                                                        | <span data-ttu-id="eee51-152">Indica que se trata de um envio de formulários.</span><span class="sxs-lookup"><span data-stu-id="eee51-152">Indicates that this is a Forms submission.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="eee51-153">[**Internet \_ sinalizador \_ de \_ envio de formulários de sinalizador da Internet do cache**](api-flags.md)[**\_ \_ \_**](api-flags.md)</span><span class="sxs-lookup"><span data-stu-id="eee51-153">[**INTERNET\_FLAG\_FROM\_CACHE**](api-flags.md)[**INTERNET\_FLAG\_FORMS\_SUBMIT**](api-flags.md)</span></span> | <span data-ttu-id="eee51-154">Não faz solicitações de rede.</span><span class="sxs-lookup"><span data-stu-id="eee51-154">Does not make network requests.</span></span> <span data-ttu-id="eee51-155">Todas as entidades são retornadas do cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-155">All entities are returned from the cache.</span></span> <span data-ttu-id="eee51-156">Se o item solicitado não estiver no cache, um erro adequado, como o arquivo de \_ erro \_ não \_ encontrado, será retornado.</span><span class="sxs-lookup"><span data-stu-id="eee51-156">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="eee51-157">Somente a função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="eee51-157">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>                                                                                                                                                                                                       |
| [<span data-ttu-id="eee51-158">**sinalizador de INTERNET do \_ \_ FWD \_ back**</span><span class="sxs-lookup"><span data-stu-id="eee51-158">**INTERNET\_FLAG\_FWD\_BACK**</span></span>](api-flags.md)                                                                                  | <span data-ttu-id="eee51-159">Indica que a função deve usar a cópia do recurso que está atualmente no cache da Internet.</span><span class="sxs-lookup"><span data-stu-id="eee51-159">Indicates that the function should use the copy of the resource that is currently in the Internet cache.</span></span> <span data-ttu-id="eee51-160">A data de validade e outras informações sobre o recurso não são verificadas.</span><span class="sxs-lookup"><span data-stu-id="eee51-160">The expiration date and other information about the resource is not checked.</span></span> <span data-ttu-id="eee51-161">Se o item solicitado não for encontrado no cache da Internet, o sistema tentará localizar o recurso na rede.</span><span class="sxs-lookup"><span data-stu-id="eee51-161">If the requested item is not found in the Internet cache, the system attempts to locate the resource on the network.</span></span> <span data-ttu-id="eee51-162">Esse valor foi introduzido no Microsoft Internet Explorer 5 e está associado às operações de botão **Avançar** e **voltar** do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="eee51-162">This value was introduced in Microsoft Internet Explorer 5 and is associated with the **Forward** and **Back** button operations of Internet Explorer.</span></span> |
| [<span data-ttu-id="eee51-163">**\_hiperlink de sinalizador da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="eee51-163">**INTERNET\_FLAG\_HYPERLINK**</span></span>](api-flags.md)                                                                                 | <span data-ttu-id="eee51-164">Força o aplicativo a recarregar um recurso se nenhum tempo de expiração e nenhuma hora da última modificação foi retornada quando o recurso foi armazenado no cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-164">Forces the application to reload a resource if no expire time and no last-modified time were returned when the resource was stored in the cache.</span></span>                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="eee51-165">**sinalizador da INTERNET \_ \_ tornar \_ persistente**</span><span class="sxs-lookup"><span data-stu-id="eee51-165">**INTERNET\_FLAG\_MAKE\_PERSISTENT**</span></span>](api-flags.md)                                                                    | <span data-ttu-id="eee51-166">Não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="eee51-166">No longer supported.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="eee51-167">**o \_ sinalizador da Internet \_ deve \_ armazenar a solicitação em cache \_**</span><span class="sxs-lookup"><span data-stu-id="eee51-167">**INTERNET\_FLAG\_MUST\_CACHE\_REQUEST**</span></span>](api-flags.md)                                                             | <span data-ttu-id="eee51-168">Faz com que um arquivo temporário seja criado se o arquivo não puder ser armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-168">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="eee51-169">Isso é idêntico ao valor preferencial, o [**sinalizador de Internet \_ \_ precisa de \_ arquivo**](api-flags.md).</span><span class="sxs-lookup"><span data-stu-id="eee51-169">This is identical to the preferred value, [**INTERNET\_FLAG\_NEED\_FILE**](api-flags.md).</span></span>                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="eee51-170">**sinalizador de INTERNET- \_ \_ \_ arquivo necessário**</span><span class="sxs-lookup"><span data-stu-id="eee51-170">**INTERNET\_FLAG\_NEED\_FILE**</span></span>](api-flags.md)                                                                                | <span data-ttu-id="eee51-171">Faz com que um arquivo temporário seja criado se o arquivo não puder ser armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-171">Causes a temporary file to be created if the file cannot be cached.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="eee51-172">**sinalizador da INTERNET \_ \_ sem \_ gravação de cache \_**</span><span class="sxs-lookup"><span data-stu-id="eee51-172">**INTERNET\_FLAG\_NO\_CACHE\_WRITE**</span></span>](api-flags.md)                                                                     | <span data-ttu-id="eee51-173">Rejeita qualquer tentativa da função para armazenar dados baixados da Internet no cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-173">Rejects any attempt by the function to store data downloaded from the Internet in the cache.</span></span> <span data-ttu-id="eee51-174">Esse sinalizador será necessário se o aplicativo não quiser que os recursos baixados sejam armazenados localmente.</span><span class="sxs-lookup"><span data-stu-id="eee51-174">This flag is necessary if the application does not want any downloaded resources to be stored locally.</span></span>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="eee51-175">**\_sinalizador \_ da Internet sem \_ interface do usuário**</span><span class="sxs-lookup"><span data-stu-id="eee51-175">**INTERNET\_FLAG\_NO\_UI**</span></span>](api-flags.md)                                                                                        | <span data-ttu-id="eee51-176">Desabilita a caixa de diálogo cookie.</span><span class="sxs-lookup"><span data-stu-id="eee51-176">Disables the cookie dialog box.</span></span> <span data-ttu-id="eee51-177">Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (somente solicitações HTTP).</span><span class="sxs-lookup"><span data-stu-id="eee51-177">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (HTTP requests only).</span></span>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="eee51-178">**sinalizador de INTERNET \_ \_ offline**</span><span class="sxs-lookup"><span data-stu-id="eee51-178">**INTERNET\_FLAG\_OFFLINE**</span></span>](api-flags.md)                                                                                     | <span data-ttu-id="eee51-179">Impede que o aplicativo envie solicitações para a rede.</span><span class="sxs-lookup"><span data-stu-id="eee51-179">Prevents the application from sending requests to the network.</span></span> <span data-ttu-id="eee51-180">Todas as solicitações são resolvidas usando os recursos armazenados no cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-180">All requests are resolved using the resources stored in the cache.</span></span> <span data-ttu-id="eee51-181">Se o recurso não estiver no cache, um erro adequado, como o arquivo de \_ erro \_ não \_ encontrado, será retornado.</span><span class="sxs-lookup"><span data-stu-id="eee51-181">If the resource is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span>                                                                                                                                                                                                                            |
| [<span data-ttu-id="eee51-182">**PRAGMA do sinalizador de INTERNET \_ \_ \_ NoCache**</span><span class="sxs-lookup"><span data-stu-id="eee51-182">**INTERNET\_FLAG\_PRAGMA\_NOCACHE**</span></span>](api-flags.md)                                                                      | <span data-ttu-id="eee51-183">Força a solicitação a ser resolvida pelo servidor de origem, mesmo que exista uma cópia armazenada em cache no proxy.</span><span class="sxs-lookup"><span data-stu-id="eee51-183">Forces the request to be resolved by the origin server, even if a cached copy exists on the proxy.</span></span> <span data-ttu-id="eee51-184">A função [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (somente em solicitações HTTP e HTTPS) e a função [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usam esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="eee51-184">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function (on HTTP and HTTPS requests only) and [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function use this flag.</span></span>                                                                                                                                                                                               |
| [<span data-ttu-id="eee51-185">**recarregamento de sinalizador da INTERNET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="eee51-185">**INTERNET\_FLAG\_RELOAD**</span></span>](api-flags.md)                                                                                       | <span data-ttu-id="eee51-186">Força a função a recuperar o recurso solicitado diretamente da Internet.</span><span class="sxs-lookup"><span data-stu-id="eee51-186">Forces the function to retrieve the requested resource directly from the Internet.</span></span> <span data-ttu-id="eee51-187">As informações baixadas são armazenadas no cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-187">The information that is downloaded is stored in the cache.</span></span>                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="eee51-188">**sinalizador de INTERNET \_ \_ ressincronizar**</span><span class="sxs-lookup"><span data-stu-id="eee51-188">**INTERNET\_FLAG\_RESYNCHRONIZE**</span></span>](api-flags.md)                                                                         | <span data-ttu-id="eee51-189">Faz com que um aplicativo execute um download condicional do recurso da Internet.</span><span class="sxs-lookup"><span data-stu-id="eee51-189">Causes an application to perform a conditional download of the resource from the Internet.</span></span> <span data-ttu-id="eee51-190">Se a versão armazenada no cache estiver atualizada, as informações serão baixadas do cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-190">If the version stored in the cache is current, the information is downloaded from the cache.</span></span> <span data-ttu-id="eee51-191">Caso contrário, as informações serão recarregadas do servidor.</span><span class="sxs-lookup"><span data-stu-id="eee51-191">Otherwise, the information is reloaded from the server.</span></span>                                                                                                                                                                                                                   |



 

## <a name="persistent-caching-functions"></a><span data-ttu-id="eee51-192">Funções de cache persistentes</span><span class="sxs-lookup"><span data-stu-id="eee51-192">Persistent Caching Functions</span></span>

<span data-ttu-id="eee51-193">Os clientes que precisam de serviços de cache persistentes usam as funções de cache persistentes para permitir que seus aplicativos salvem dados no sistema de arquivos local para uso posterior, como em situações em que um link de baixa largura de banda limita o acesso aos dados ou o acesso não está disponível.</span><span class="sxs-lookup"><span data-stu-id="eee51-193">Clients that need persistent caching services use the persistent caching functions to allow their applications to save data in the local file system for subsequent use, such as in situations where a low-bandwidth link limits access to the data, or the access is not available at all.</span></span>

<span data-ttu-id="eee51-194">As funções de cache fornecem cache persistente e navegação offline.</span><span class="sxs-lookup"><span data-stu-id="eee51-194">The cache functions provide persistent caching and offline browsing.</span></span> <span data-ttu-id="eee51-195">A menos que o [**sinalizador da Internet sem sinalizador de \_ \_ \_ \_ gravação de cache não**](api-flags.md) especifique explicitamente nenhum cache, as funções armazenam em cache todos os dados baixados da rede.</span><span class="sxs-lookup"><span data-stu-id="eee51-195">Unless the [**INTERNET\_FLAG\_NO\_CACHE\_WRITE**](api-flags.md) flag explicitly specifies no caching, the functions cache all data downloaded from the network.</span></span> <span data-ttu-id="eee51-196">As respostas para postar dados não são armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-196">The responses to POST data are not cached.</span></span>

## <a name="using-the-persistent-url-cache-functions"></a><span data-ttu-id="eee51-197">Usando as funções de cache de URL persistentes</span><span class="sxs-lookup"><span data-stu-id="eee51-197">Using the Persistent URL Cache Functions</span></span>

<span data-ttu-id="eee51-198">As seguintes funções de cache de URL persistentes permitem que um aplicativo acesse e manipule informações armazenadas no cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-198">The following persistent URL cache functions allow an application to access and manipulate information stored in the cache.</span></span>



| <span data-ttu-id="eee51-199">Função</span><span class="sxs-lookup"><span data-stu-id="eee51-199">Function</span></span>                                                           | <span data-ttu-id="eee51-200">Descrição</span><span class="sxs-lookup"><span data-stu-id="eee51-200">Description</span></span>                                                                                                                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eee51-201">**CommitUrlCacheEntryA**</span><span class="sxs-lookup"><span data-stu-id="eee51-201">**CommitUrlCacheEntryA**</span></span>](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya)               | <span data-ttu-id="eee51-202">Armazena em cache os dados no arquivo especificado no armazenamento de cache e associa-os à URL fornecida.</span><span class="sxs-lookup"><span data-stu-id="eee51-202">Caches data in the specified file in the cache storage and associates it with the given URL.</span></span>                                                                  |
| [<span data-ttu-id="eee51-203">**CommitUrlCacheEntryW**</span><span class="sxs-lookup"><span data-stu-id="eee51-203">**CommitUrlCacheEntryW**</span></span>](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentryw)               | <span data-ttu-id="eee51-204">Armazena em cache os dados no arquivo especificado no armazenamento de cache e associa-os à URL fornecida.</span><span class="sxs-lookup"><span data-stu-id="eee51-204">Caches data in the specified file in the cache storage and associates it with the given URL.</span></span>                                                                  |
| [<span data-ttu-id="eee51-205">**CreateUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="eee51-205">**CreateUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya)                 | <span data-ttu-id="eee51-206">Aloca o armazenamento de cache solicitado e cria um nome de arquivo local para salvar a entrada de cache que corresponde ao nome de origem.</span><span class="sxs-lookup"><span data-stu-id="eee51-206">Allocates the requested cache storage and creates a local file name for saving the cache entry that corresponds to the source name.</span></span>                           |
| [<span data-ttu-id="eee51-207">**CreateUrlCacheGroup**</span><span class="sxs-lookup"><span data-stu-id="eee51-207">**CreateUrlCacheGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup)                 | <span data-ttu-id="eee51-208">Gera uma identificação de grupo de cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-208">Generates a cache group identification.</span></span>                                                                                                                       |
| [<span data-ttu-id="eee51-209">**DeleteUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="eee51-209">**DeleteUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry)                 | <span data-ttu-id="eee51-210">Remove o arquivo associado ao nome de origem do cache, se o arquivo existir.</span><span class="sxs-lookup"><span data-stu-id="eee51-210">Removes the file associated with the source name from the cache, if the file exists.</span></span>                                                                          |
| [<span data-ttu-id="eee51-211">**DeleteUrlCacheGroup**</span><span class="sxs-lookup"><span data-stu-id="eee51-211">**DeleteUrlCacheGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-deleteurlcachegroup)                 | <span data-ttu-id="eee51-212">Libera um **GroupId** e qualquer estado associado no arquivo de índice de cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-212">Releases a **GROUPID** and any associated state in the cache index file.</span></span>                                                                                      |
| [<span data-ttu-id="eee51-213">**FindCloseUrlCache**</span><span class="sxs-lookup"><span data-stu-id="eee51-213">**FindCloseUrlCache**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache)                     | <span data-ttu-id="eee51-214">Fecha o identificador de enumeração especificado.</span><span class="sxs-lookup"><span data-stu-id="eee51-214">Closes the specified enumeration handle.</span></span>                                                                                                                      |
| [<span data-ttu-id="eee51-215">**FindFirstUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="eee51-215">**FindFirstUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya)           | <span data-ttu-id="eee51-216">Inicia a enumeração do cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-216">Begins the enumeration of the cache.</span></span>                                                                                                                          |
| [<span data-ttu-id="eee51-217">**FindFirstUrlCacheEntryEx**</span><span class="sxs-lookup"><span data-stu-id="eee51-217">**FindFirstUrlCacheEntryEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa)       | <span data-ttu-id="eee51-218">Inicia uma enumeração filtrada do cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-218">Begins a filtered enumeration of the cache.</span></span>                                                                                                                   |
| [<span data-ttu-id="eee51-219">**FindNextUrlCacheEntry**</span><span class="sxs-lookup"><span data-stu-id="eee51-219">**FindNextUrlCacheEntry**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya)             | <span data-ttu-id="eee51-220">Recupera a próxima entrada no cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-220">Retrieves the next entry in the cache.</span></span>                                                                                                                        |
| [<span data-ttu-id="eee51-221">**FindNextUrlCacheEntryEx**</span><span class="sxs-lookup"><span data-stu-id="eee51-221">**FindNextUrlCacheEntryEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa)         | <span data-ttu-id="eee51-222">Recupera a próxima entrada em uma enumeração de cache filtrada.</span><span class="sxs-lookup"><span data-stu-id="eee51-222">Retrieves the next entry in a filtered cache enumeration.</span></span>                                                                                                     |
| [<span data-ttu-id="eee51-223">**GetUrlCacheEntryInfo**</span><span class="sxs-lookup"><span data-stu-id="eee51-223">**GetUrlCacheEntryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa)               | <span data-ttu-id="eee51-224">Recupera informações sobre uma entrada de cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-224">Retrieves information about a cache entry.</span></span>                                                                                                                    |
| [<span data-ttu-id="eee51-225">**GetUrlCacheEntryInfoEx**</span><span class="sxs-lookup"><span data-stu-id="eee51-225">**GetUrlCacheEntryInfoEx**</span></span>](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoexa)           | <span data-ttu-id="eee51-226">Pesquisa a URL após a tradução de qualquer redirecionamento em cache que seria aplicado no modo offline por [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="eee51-226">Searches for the URL after translating any cached redirections that would be applied in offline mode by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span>           |
| [<span data-ttu-id="eee51-227">**ReadUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="eee51-227">**ReadUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)         | <span data-ttu-id="eee51-228">Lê os dados armazenados em cache de um fluxo que foi aberto usando [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span><span class="sxs-lookup"><span data-stu-id="eee51-228">Reads the cached data from a stream that has been opened using [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span></span>                            |
| [<span data-ttu-id="eee51-229">**RetrieveUrlCacheEntryFile**</span><span class="sxs-lookup"><span data-stu-id="eee51-229">**RetrieveUrlCacheEntryFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea)     | <span data-ttu-id="eee51-230">Recupera uma entrada de cache do cache na forma de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="eee51-230">Retrieves a cache entry from the cache in the form of a file.</span></span>                                                                                                 |
| [<span data-ttu-id="eee51-231">**RetrieveUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="eee51-231">**RetrieveUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) | <span data-ttu-id="eee51-232">Fornece a maneira mais eficiente e independente de implementação de acessar os dados de cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-232">Provides the most efficient and implementation-independent way of accessing the cache data.</span></span>                                                                   |
| [<span data-ttu-id="eee51-233">**SetUrlCacheEntryGroup**</span><span class="sxs-lookup"><span data-stu-id="eee51-233">**SetUrlCacheEntryGroup**</span></span>](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup)             | <span data-ttu-id="eee51-234">Adiciona ou remove entradas de um grupo de cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-234">Adds or removes entries from a cache group.</span></span>                                                                                                                   |
| [<span data-ttu-id="eee51-235">**SetUrlCacheEntryInfo**</span><span class="sxs-lookup"><span data-stu-id="eee51-235">**SetUrlCacheEntryInfo**</span></span>](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentryinfoa)               | <span data-ttu-id="eee51-236">Define os membros especificados da estrutura [**de \_ \_ \_ informações de entrada de cache da Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .</span><span class="sxs-lookup"><span data-stu-id="eee51-236">Sets the specified members of the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure.</span></span>                                                |
| [<span data-ttu-id="eee51-237">**UnlockUrlCacheEntryFile**</span><span class="sxs-lookup"><span data-stu-id="eee51-237">**UnlockUrlCacheEntryFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile)         | <span data-ttu-id="eee51-238">Desbloqueia a entrada de cache que foi bloqueada quando o arquivo foi recuperado para uso do cache por [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea).</span><span class="sxs-lookup"><span data-stu-id="eee51-238">Unlocks the cache entry that was locked when the file was retrieved for use from the cache by [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea).</span></span> |
| [<span data-ttu-id="eee51-239">**UnlockUrlCacheEntryStream**</span><span class="sxs-lookup"><span data-stu-id="eee51-239">**UnlockUrlCacheEntryStream**</span></span>](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream)     | <span data-ttu-id="eee51-240">Fecha o fluxo que foi recuperado usando [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span><span class="sxs-lookup"><span data-stu-id="eee51-240">Closes the stream that has been retrieved using [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama).</span></span>                                           |



 

### <a name="enumerating-the-cache"></a><span data-ttu-id="eee51-241">Enumerando o cache</span><span class="sxs-lookup"><span data-stu-id="eee51-241">Enumerating the Cache</span></span>

<span data-ttu-id="eee51-242">As funções [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) e [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) enumeram as informações armazenadas no cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-242">The [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) and [**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) functions enumerate the information stored in the cache.</span></span> <span data-ttu-id="eee51-243">[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) inicia a enumeração por meio de um padrão de pesquisa, um buffer e um tamanho de buffer para criar um identificador e retornar a primeira entrada de cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-243">[**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) starts the enumeration by taking a search pattern, a buffer, and a buffer size to create a handle and return the first cache entry.</span></span> <span data-ttu-id="eee51-244">[**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) usa o identificador criado por [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), um buffer e um tamanho de buffer para retornar a próxima entrada de cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-244">[**FindNextUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentrya) takes the handle created by [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya), a buffer, and a buffer size to return the next cache entry.</span></span>

<span data-ttu-id="eee51-245">Ambas as funções armazenam uma estrutura de informações de entrada de cache da Internet no buffer. [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)</span><span class="sxs-lookup"><span data-stu-id="eee51-245">Both functions store an [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure in the buffer.</span></span> <span data-ttu-id="eee51-246">O tamanho dessa estrutura varia para cada entrada.</span><span class="sxs-lookup"><span data-stu-id="eee51-246">The size of this structure varies for each entry.</span></span> <span data-ttu-id="eee51-247">Se o tamanho do buffer passado para uma das funções for insuficiente, a função falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um erro de \_ buffer insuficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="eee51-247">If the buffer size passed to either function is insufficient, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="eee51-248">A variável de tamanho do buffer contém o tamanho do buffer necessário para recuperar essa entrada de cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-248">The buffer size variable contains the buffer size that was needed to retrieve that cache entry.</span></span> <span data-ttu-id="eee51-249">Um buffer do tamanho indicado pela variável de tamanho do buffer deve ser alocado e a função deve ser chamada novamente com o novo buffer.</span><span class="sxs-lookup"><span data-stu-id="eee51-249">A buffer of the size indicated by the buffer size variable should be allocated, and the function should be called again with the new buffer.</span></span>

<span data-ttu-id="eee51-250">A estrutura de informações de entrada de cache da Internet contém o tamanho da estrutura, a URL das informações armazenadas em cache, o nome do arquivo local, o tipo de entrada de cache, a contagem de uso, a taxa de acesso, a hora da última modificação, a expiração, o último acesso, a hora da última sincronização, as informações do cabeçalho e a extensão do nome do arquivo [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)</span><span class="sxs-lookup"><span data-stu-id="eee51-250">The [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure contains the structure size, URL of the cached information, local file name, cache entry type, use count, hit rate, size, last modified time, expiration, last access, last synchronized time, header information, header information size, and file name extension.</span></span>

<span data-ttu-id="eee51-251">A função [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) usa um padrão de pesquisa, um buffer que armazena a estrutura de informações de entrada de cache da [**Internet \_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="eee51-251">The [**FindFirstUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentrya) function takes a search pattern, a buffer that stores the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="eee51-252">Atualmente, apenas o padrão de pesquisa padrão, que retorna todas as entradas de cache, é implementado.</span><span class="sxs-lookup"><span data-stu-id="eee51-252">Currently, only the default search pattern, which returns all cache entries, is implemented.</span></span>

<span data-ttu-id="eee51-253">Depois que o cache é enumerado, o aplicativo deve chamar [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) para fechar o identificador de enumeração de cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-253">After the cache is enumerated, the application should call [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache) to close the cache enumeration handle.</span></span>

<span data-ttu-id="eee51-254">O exemplo a seguir exibe a URL de cada entrada de cache em uma caixa de listagem, **IDC \_ cachelist**.</span><span class="sxs-lookup"><span data-stu-id="eee51-254">The following example displays each cache entry's URL in a list box, **IDC\_CacheList**.</span></span> <span data-ttu-id="eee51-255">Ele usa \_ \_ \_ o tamanho máximo das informações de entrada de cache \_ para alocar inicialmente um buffer, já que as versões anteriores da API do Wininet não enumeram o cache corretamente de outra forma.</span><span class="sxs-lookup"><span data-stu-id="eee51-255">It uses MAX\_CACHE\_ENTRY\_INFO\_SIZE to initially allocate a buffer, since early versions of the WinINet API do not enumerate the cache properly otherwise.</span></span> <span data-ttu-id="eee51-256">As versões posteriores enumeram o cache corretamente e não há nenhum limite de tamanho de cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-256">Later versions do enumerate the cache properly and there is no cache size limit.</span></span> <span data-ttu-id="eee51-257">Todos os aplicativos executados em computadores com a versão da API do WinINet do Internet Explorer 4,0 devem alocar um buffer do tamanho necessário.</span><span class="sxs-lookup"><span data-stu-id="eee51-257">All applications that run on computers with the version of the WinINet API from Internet Explorer 4.0 must allocate a buffer of the required size.</span></span> <span data-ttu-id="eee51-258">Para obter mais informações, consulte [usando buffers](appendix-b-using-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="eee51-258">For more information, see [Using Buffers](appendix-b-using-buffers.md).</span></span>


```C++
int WINAPI EnumerateCacheOld(HWND hX)
{
    DWORD dwEntrySize;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;
    DWORD MAX_CACHE_ENTRY_INFO_SIZE = 4096;
    HANDLE hCacheDir;
    int nCount=0;

    SendDlgItemMessage(hX,IDC_CacheList,LB_RESETCONTENT,0,0);
    
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
    lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
    lpCacheEntry->dwStructSize = dwEntrySize;

again:

    hCacheDir = FindFirstUrlCacheEntry(NULL,
                                       lpCacheEntry,
                                       &dwEntrySize);
    if (!hCacheDir)                                             
    {
        delete[]lpCacheEntry;
        switch(GetLastError())
        {
            case ERROR_NO_MORE_ITEMS: 
                TCHAR tempout[80];
                _stprintf_s(tempout, 
                            80,   
                            TEXT("The number of cache entries = %d \n"),
                            nCount);
                MessageBox(hX,tempout,TEXT("Cache Enumeration"),MB_OK);
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return TRUE;
                break;
            case ERROR_INSUFFICIENT_BUFFER:
                lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                                new char[dwEntrySize];
                lpCacheEntry->dwStructSize = dwEntrySize;
                goto again;
                break;
            default:
                ErrorOut( hX,GetLastError(),
                          TEXT("FindNextUrlCacheEntry Init"));
                FindCloseUrlCache(hCacheDir);
                SetCursor(LoadCursor(NULL,IDC_ARROW));
                return FALSE;
        }
    }

    SendDlgItemMessage(hX,IDC_CacheList,LB_ADDSTRING,
                       0,(LPARAM)(lpCacheEntry->lpszSourceUrlName));
    nCount++;
    delete (lpCacheEntry);

    do 
    {
        dwEntrySize = MAX_CACHE_ENTRY_INFO_SIZE;
        lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) new char[dwEntrySize];
        lpCacheEntry->dwStructSize = dwEntrySize;

retry:
        if (!FindNextUrlCacheEntry(hCacheDir,
                                   lpCacheEntry, 
                                   &dwEntrySize))
        {
            delete[]lpCacheEntry;
            switch(GetLastError())
            {
                case ERROR_NO_MORE_ITEMS: 
                    TCHAR tempout[80];
                    _stprintf_s(tempout,
                                80,
                                TEXT("The number of cache entries = %d \n"),nCount);
                    MessageBox(hX,
                               tempout,
                               TEXT("Cache Enumeration"),MB_OK);
                    FindCloseUrlCache(hCacheDir);
                    return TRUE;
                    break;
                case ERROR_INSUFFICIENT_BUFFER:
                    lpCacheEntry = 
                             (LPINTERNET_CACHE_ENTRY_INFO) 
                              new char[dwEntrySize];
                    lpCacheEntry->dwStructSize = dwEntrySize;
                    goto retry;
                    break;
                default:
                    ErrorOut(hX,
                             GetLastError(),
                             TEXT("FindNextUrlCacheEntry Init"));
                    FindCloseUrlCache(hCacheDir);
                    return FALSE;
            }
        }

        SendDlgItemMessage(hX,
                           IDC_CacheList,LB_ADDSTRING,
                           0,
                          (LPARAM)(lpCacheEntry->lpszSourceUrlName));
        nCount++;
        delete[] lpCacheEntry;        
    }  while (TRUE);

    SetCursor(LoadCursor(NULL,IDC_ARROW));
    return TRUE;        
}
```



### <a name="retrieving-cache-entry-information"></a><span data-ttu-id="eee51-259">Recuperando informações de entrada de cache</span><span class="sxs-lookup"><span data-stu-id="eee51-259">Retrieving Cache Entry Information</span></span>

<span data-ttu-id="eee51-260">A função [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) permite recuperar a estrutura [**de \_ \_ \_ informações de entrada de cache da Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) para a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="eee51-260">The [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) function lets you retrieve the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure for the specified URL.</span></span> <span data-ttu-id="eee51-261">Essa estrutura contém o tamanho da estrutura, a URL das informações armazenadas em cache, o nome do arquivo local, o tipo de entrada do cache, a contagem de uso, a taxa de acesso, a hora da última modificação, a expiração, o último acesso, a hora da última sincronização, as informações do cabeçalho, o tamanho das informações do cabeçalho e a extensão do nome</span><span class="sxs-lookup"><span data-stu-id="eee51-261">This structure contains the structure size, URL of the cached information, local file name, cache entry type, use count, hit rate, size, last modified time, expiration, last access, last synchronized time, header information, header information size, and file name extension.</span></span>

<span data-ttu-id="eee51-262">O [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) aceita uma URL, um buffer para uma estrutura de informações de entrada de cache da [**Internet \_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="eee51-262">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) accepts a URL, a buffer for an [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="eee51-263">Se a URL for encontrada, as informações serão copiadas no buffer.</span><span class="sxs-lookup"><span data-stu-id="eee51-263">If the URL is found, the information is copied into the buffer.</span></span> <span data-ttu-id="eee51-264">Caso contrário, a função falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o arquivo de erro \_ \_ não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="eee51-264">Otherwise, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="eee51-265">Se o tamanho do buffer for insuficiente para armazenar as informações de entrada de cache, a função falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará um erro de \_ buffer insuficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="eee51-265">If the buffer size is insufficient to store the cache entry information, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INSUFFICIENT\_BUFFER.</span></span> <span data-ttu-id="eee51-266">O tamanho necessário para recuperar as informações é armazenado na variável de tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="eee51-266">The size required to retrieve the information is stored in the buffer size variable.</span></span>

<span data-ttu-id="eee51-267">O [**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) não faz nenhuma análise de URL, portanto, uma URL que contém uma âncora ( \# ) não será encontrada no cache, mesmo que o recurso seja armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-267">[**GetUrlCacheEntryInfo**](/windows/desktop/api/Wininet/nf-wininet-geturlcacheentryinfoa) does not do any URL parsing, so a URL that contains an anchor (\#) will not be found in the cache, even if the resource is cached.</span></span> <span data-ttu-id="eee51-268">Por exemplo, se a URL " https://example.com/example.htm\#sample " for passada, a função retornará o \_ arquivo de erro \_ não \_ encontrado mesmo se " https://example.com/example.htm " estiver no cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-268">For example, if the URL "https://example.com/example.htm\#sample" is passed, the function returns ERROR\_FILE\_NOT\_FOUND even if "https://example.com/example.htm" is in the cache.</span></span>

<span data-ttu-id="eee51-269">O exemplo a seguir recupera as informações de entrada de cache para a URL especificada.</span><span class="sxs-lookup"><span data-stu-id="eee51-269">The following example retrieves the cache entry information for the specified URL.</span></span> <span data-ttu-id="eee51-270">Em seguida, a função exibe as informações de cabeçalho na caixa de edição **IDC \_ CacheDump** .</span><span class="sxs-lookup"><span data-stu-id="eee51-270">The function then displays the header information in the **IDC\_CacheDump** edit box.</span></span>


```C++
int WINAPI GetCacheEntryInfo(HWND hX,LPTSTR lpszUrl)
{
    DWORD dwEntrySize=0;
    LPINTERNET_CACHE_ENTRY_INFO lpCacheEntry;

    SetCursor(LoadCursor(NULL,IDC_WAIT));
    if (!GetUrlCacheEntryInfo(lpszUrl,NULL,&dwEntrySize))
    {
        if (GetLastError()!=ERROR_INSUFFICIENT_BUFFER)
        {
            ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
            lpCacheEntry = (LPINTERNET_CACHE_ENTRY_INFO) 
                            new char[dwEntrySize];
    }
    else
        return FALSE; // should not be successful w/ NULL buffer
                      // and 0 size

    if (!GetUrlCacheEntryInfo(lpszUrl,lpCacheEntry,&dwEntrySize))
    {
        ErrorOut(hX,GetLastError(),TEXT("GetUrlCacheEntryInfo"));
        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return FALSE;
    }
    else
    {
        if ((lpCacheEntry->dwHeaderInfoSize)!=0)
        {
            LPSTR(lpCacheEntry->lpHeaderInfo)
                                [lpCacheEntry->dwHeaderInfoSize]=TEXT('\0');
            SetDlgItemText(hX,IDC_Headers,
                           lpCacheEntry->lpHeaderInfo);
        }
        else
        {
            SetDlgItemText(hX,IDC_Headers,TEXT("None"));
        }

        SetCursor(LoadCursor(NULL,IDC_ARROW));
        return TRUE;
    }
        
}
```



### <a name="creating-a-cache-entry"></a><span data-ttu-id="eee51-271">Criando uma entrada de cache</span><span class="sxs-lookup"><span data-stu-id="eee51-271">Creating a Cache Entry</span></span>

<span data-ttu-id="eee51-272">Um aplicativo usa as funções [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) e [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) para criar uma entrada de cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-272">An application uses the [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) and [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) functions to create a cache entry.</span></span>

<span data-ttu-id="eee51-273">[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) aceita a URL, o tamanho de arquivo esperado e a extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="eee51-273">[**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya) accepts the URL, expected file size, and file name extension.</span></span> <span data-ttu-id="eee51-274">Em seguida, a função cria um nome de arquivo local para salvar a entrada de cache que corresponde à URL e à extensão de nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="eee51-274">The function then creates a local file name for saving the cache entry that corresponds to the URL and file name extension.</span></span>

<span data-ttu-id="eee51-275">Usando o nome do arquivo local, grave os dados no arquivo local.</span><span class="sxs-lookup"><span data-stu-id="eee51-275">Using the local file name, write the data into the local file.</span></span> <span data-ttu-id="eee51-276">Depois que os dados tiverem sido gravados no arquivo local, o aplicativo deverá chamar [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span><span class="sxs-lookup"><span data-stu-id="eee51-276">After the data has been written to the local file, the application should call [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span></span>

<span data-ttu-id="eee51-277">[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) aceita a URL, o nome do arquivo local, a expiração, a hora da última modificação, o tipo de entrada do cache, as informações do cabeçalho, o tamanho das informações do cabeçalho e a extensão do nome do arquivo</span><span class="sxs-lookup"><span data-stu-id="eee51-277">[**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya) accepts the URL, local file name, expiration, last modified time, cache entry type, header information, header information size, and file name extension.</span></span> <span data-ttu-id="eee51-278">Em seguida, a função armazena em cache os dados no arquivo especificado no armazenamento de cache e o associa à URL fornecida.</span><span class="sxs-lookup"><span data-stu-id="eee51-278">The function then caches data in the file specified in the cache storage and associates it with the given URL.</span></span>

<span data-ttu-id="eee51-279">O exemplo a seguir usa o nome do arquivo local, criado por uma chamada anterior para [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), armazenado na caixa de texto, **IDC \_ LocalFile**, para armazenar o texto da caixa de texto, **IDC \_ CacheDump**, na entrada de cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-279">The following example uses the local file name, created by a previous call to [**CreateUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-createurlcacheentrya), stored in the text box, **IDC\_LocalFile**, to store the text from the text box, **IDC\_CacheDump**, in the cache entry.</span></span> <span data-ttu-id="eee51-280">Depois que os dados tiverem sido gravados no arquivo usando **fopen**, **fprintf** e **fclose**, a entrada será confirmada usando [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span><span class="sxs-lookup"><span data-stu-id="eee51-280">After the data has been written to the file using **fopen**, **fprintf**, and **fclose**, the entry is committed using [**CommitUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-commiturlcacheentrya).</span></span>


```C++
int WINAPI CommitEntry(HWND hX)
{
    LPTSTR lpszUrl, lpszExt, lpszFileName;
    LPTSTR lpszData,lpszSize;
    DWORD dwSize;
    DWORD dwEntryType=0;
    FILE *lpfCacheEntry;
    LPFILETIME lpdtmExpire, lpdtmLastModified;
    LPSYSTEMTIME lpdtmSysTime;
    errno_t err;

    if( SendDlgItemMessage(hX,IDC_RBNormal,BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + NORMAL_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBSticky, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + STICKY_CACHE_ENTRY;
    }
    else if(SendDlgItemMessage( hX,IDC_RBSparse, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + SPARSE_CACHE_ENTRY;
    }
 

    if( SendDlgItemMessage(hX,IDC_RBCookie, BM_GETCHECK,0,0))
    {
            dwEntryType = dwEntryType + COOKIE_CACHE_ENTRY;
    }
    else if( SendDlgItemMessage(hX,IDC_RBUrl, BM_GETCHECK,0,0) )
    {
        dwEntryType = dwEntryType + URLHISTORY_CACHE_ENTRY;
    }


    if( SendDlgItemMessage(hX,IDC_RBNone, BM_GETCHECK,0,0) )
    {
        dwEntryType=0;
    }
        
    lpdtmSysTime = new SYSTEMTIME;
    lpdtmExpire = new FILETIME;
    lpdtmLastModified = new FILETIME;

    GetLocalTime(lpdtmSysTime);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmExpire);
    SystemTimeToFileTime(lpdtmSysTime,lpdtmLastModified);
    delete(lpdtmSysTime);

    lpszUrl = new TCHAR[MAX_PATH];
    lpszFileName = new TCHAR[MAX_PATH];
    lpszExt = new TCHAR[5];
    lpszSize = new TCHAR[10];

    GetDlgItemText(hX,IDC_SourceURL,lpszUrl,MAX_PATH);
    GetDlgItemText(hX,IDC_LocalFile,lpszFileName,MAX_PATH);
    GetDlgItemText(hX,IDC_FileExt,lpszExt,5);

    GetDlgItemText(hX,IDC_SizeLow,lpszSize,10);
    dwSize = (DWORD)_ttol(lpszSize);
    delete(lpszSize);

    if (dwSize==0)
    {
        if((MessageBox(hX,
                       TEXT("Incorrect File Size.\nUsing 8000 characters, Okay?\n"),
                       TEXT("Commit Entry"),MB_YESNO))
                        ==IDYES)
        {
            dwSize = 8000;
        }
        else
        {
            return FALSE;
        }
    }

    lpszData = new TCHAR[dwSize];
    GetDlgItemText(hX,IDC_CacheDump,lpszData,dwSize);
        
     err = _tfopen_s(&lpfCacheEntry,lpszFileName,_T("w"));
     if (err)
        return FALSE;
    fprintf(lpfCacheEntry,"%s",lpszData);
    fclose(lpfCacheEntry);
    delete(lpszData);

    if ( !CommitUrlCacheEntry( lpszUrl, 
                               lpszFileName, 
                               *lpdtmExpire,
                               *lpdtmLastModified, 
                               dwEntryType,
                               NULL,
                               0,
                               lpszExt,
                               0) )
    {
        ErrorOut(hX,GetLastError(),TEXT("Commit Cache Entry"));
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return FALSE;
    }
    else
    {
        delete(lpszUrl);
        delete(lpszFileName);
        delete(lpszExt);
        delete(lpdtmExpire);
        delete(lpdtmLastModified);
        return TRUE;
    }
}
```



### <a name="deleting-a-cache-entry"></a><span data-ttu-id="eee51-281">Excluindo uma entrada de cache</span><span class="sxs-lookup"><span data-stu-id="eee51-281">Deleting a Cache Entry</span></span>

<span data-ttu-id="eee51-282">A função [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) usa uma URL e remove o arquivo de cache associado a ela.</span><span class="sxs-lookup"><span data-stu-id="eee51-282">The [**DeleteUrlCacheEntry**](/windows/desktop/api/Wininet/nf-wininet-deleteurlcacheentry) function takes a URL and removes the cache file associated with it.</span></span> <span data-ttu-id="eee51-283">Se o arquivo de cache não existir, a função falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o arquivo de erro \_ \_ não \_ encontrado.</span><span class="sxs-lookup"><span data-stu-id="eee51-283">If the cache file does not exist, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_FILE\_NOT\_FOUND.</span></span> <span data-ttu-id="eee51-284">Se o arquivo de cache estiver bloqueado ou em uso no momento, a função falhará e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o acesso ao erro \_ \_ negado.</span><span class="sxs-lookup"><span data-stu-id="eee51-284">If the cache file is currently locked or in use, the function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span> <span data-ttu-id="eee51-285">O arquivo é excluído quando desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="eee51-285">The file is deleted when unlocked.</span></span>

### <a name="retrieving-cache-entry-files"></a><span data-ttu-id="eee51-286">Recuperando arquivos de entrada de cache</span><span class="sxs-lookup"><span data-stu-id="eee51-286">Retrieving Cache Entry Files</span></span>

<span data-ttu-id="eee51-287">Para aplicativos que exigem o nome de arquivo de um recurso, use as funções [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) e [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) .</span><span class="sxs-lookup"><span data-stu-id="eee51-287">For applications that require the file name of a resource, use the [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) and [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) functions.</span></span> <span data-ttu-id="eee51-288">Os aplicativos que não exigem o nome do arquivo devem usar as funções [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream)e [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) para recuperar as informações no cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-288">Applications that do not require the file name should use the [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama), [**ReadUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-readurlcacheentrystream), and [**UnlockUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentrystream) functions to retrieve the information in the cache.</span></span>

<span data-ttu-id="eee51-289">O [**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) não faz nenhuma análise de URL, portanto, uma URL que contém uma âncora ( \# ) não será encontrada no cache, mesmo que o recurso seja armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-289">[**RetrieveUrlCacheEntryStream**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentrystreama) does not do any URL parsing, so a URL that contains an anchor (\#) will not be found in the cache, even if the resource is cached.</span></span> <span data-ttu-id="eee51-290">Por exemplo, se a URL " https://example.com/example.htm\#sample " for passada, a função retornará o \_ arquivo de erro \_ não \_ encontrado mesmo se " https://example.com/example.htm " estiver no cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-290">For example, if the URL "https://example.com/example.htm\#sample" is passed, the function returns ERROR\_FILE\_NOT\_FOUND even if "https://example.com/example.htm" is in the cache.</span></span>

<span data-ttu-id="eee51-291">O [**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) aceita uma URL, um buffer que armazena a estrutura de informações de entrada de cache da [**Internet \_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) e o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="eee51-291">[**RetrieveUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-retrieveurlcacheentryfilea) accepts a URL, a buffer that stores the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure, and the buffer size.</span></span> <span data-ttu-id="eee51-292">A função é recuperada e bloqueada para o chamador.</span><span class="sxs-lookup"><span data-stu-id="eee51-292">The function is retrieved and locked for the caller.</span></span>

<span data-ttu-id="eee51-293">Depois que as informações no arquivo forem usadas, o aplicativo deverá chamar [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) para desbloquear o arquivo.</span><span class="sxs-lookup"><span data-stu-id="eee51-293">After the information in the file has been used, the application should call [**UnlockUrlCacheEntryFile**](/windows/desktop/api/Wininet/nf-wininet-unlockurlcacheentryfile) to unlock the file.</span></span>

### <a name="cache-groups"></a><span data-ttu-id="eee51-294">Grupos de cache</span><span class="sxs-lookup"><span data-stu-id="eee51-294">Cache Groups</span></span>

<span data-ttu-id="eee51-295">Para criar um grupo de cache, a função [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) deve ser chamada para gerar um **GroupId** para o grupo de cache.</span><span class="sxs-lookup"><span data-stu-id="eee51-295">To create a cache group, the [**CreateUrlCacheGroup**](/windows/desktop/api/Wininet/nf-wininet-createurlcachegroup) function must be called to generate a **GROUPID** for the cache group.</span></span> <span data-ttu-id="eee51-296">As entradas podem ser adicionadas ao grupo de cache, fornecendo a URL da entrada de cache e o \_ sinalizador adicionar do grupo de cache da Internet \_ \_ à função [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) .</span><span class="sxs-lookup"><span data-stu-id="eee51-296">Entries can be added to the cache group by supplying the cache entry's URL and the INTERNET\_CACHE\_GROUP\_ADD flag to the [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup) function.</span></span> <span data-ttu-id="eee51-297">Para remover uma entrada de cache de um grupo, passe a URL da entrada de cache e o \_ sinalizador de remoção do grupo de caches da Internet \_ \_ para [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).</span><span class="sxs-lookup"><span data-stu-id="eee51-297">To remove a cache entry from a group, pass the cache entry's URL and the INTERNET\_CACHE\_GROUP\_REMOVE flag to [**SetUrlCacheEntryGroup**](/windows/desktop/api/Wininet/nf-wininet-seturlcacheentrygroup).</span></span>

<span data-ttu-id="eee51-298">As funções [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) e [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) podem ser usadas para enumerar as entradas em um grupo de cache especificado.</span><span class="sxs-lookup"><span data-stu-id="eee51-298">The [**FindFirstUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findfirsturlcacheentryexa) and [**FindNextUrlCacheEntryEx**](/windows/desktop/api/Wininet/nf-wininet-findnexturlcacheentryexa) functions can be used to enumerate the entries in a specified cache group.</span></span> <span data-ttu-id="eee51-299">Depois que a enumeração for concluída, a função deverá chamar [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).</span><span class="sxs-lookup"><span data-stu-id="eee51-299">After the enumeration is complete, the function should call [**FindCloseUrlCache**](/windows/desktop/api/Wininet/nf-wininet-findcloseurlcache).</span></span>

## <a name="handling-structures-with-variable-size-information"></a><span data-ttu-id="eee51-300">Manipulando estruturas com informações de tamanho variável</span><span class="sxs-lookup"><span data-stu-id="eee51-300">Handling Structures with Variable Size Information</span></span>

<span data-ttu-id="eee51-301">O cache pode conter informações de tamanho variável para cada URL armazenada.</span><span class="sxs-lookup"><span data-stu-id="eee51-301">The cache can contain variable size information for each URL stored.</span></span> <span data-ttu-id="eee51-302">Isso se reflete na estrutura [**de \_ \_ \_ informações da entrada de cache da Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) .</span><span class="sxs-lookup"><span data-stu-id="eee51-302">This is reflected in the [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) structure.</span></span> <span data-ttu-id="eee51-303">Quando as funções de cache retornam essa estrutura, elas criam um buffer que sempre é o tamanho das informações de entrada de cache da Internet, além de qualquer informação de tamanho variável. [**\_ \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa)</span><span class="sxs-lookup"><span data-stu-id="eee51-303">When the cache functions return this structure, they create a buffer that is always the size of [**INTERNET\_CACHE\_ENTRY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_entry_infoa) plus any variable size information.</span></span> <span data-ttu-id="eee51-304">Se um membro de ponteiro não for **nulo**, ele apontará para a área de memória imediatamente após a estrutura.</span><span class="sxs-lookup"><span data-stu-id="eee51-304">If a pointer member is not **NULL**, it points to the memory area immediately after the structure.</span></span> <span data-ttu-id="eee51-305">Ao copiar o buffer retornado por uma função em outro buffer, os membros do ponteiro devem ser corrigidos para apontar para o local apropriado no novo buffer, como mostra o exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="eee51-305">While copying the buffer returned by a function into another buffer, the pointer members should be fixed to point to the appropriate place in the new buffer, as the following example shows.</span></span>

``` syntax
lpDstCEInfo->lpszSourceUrlName = 
    (LPINTERNET_CACHE_ENTRY_INFO) ((LPBYTE) lpSrcCEInfo + 
       ((DWORD)(lpOldCEInfo->lpszSourceUrlName) - (DWORD)lpOldCEInfo));
```

<span data-ttu-id="eee51-306">Algumas funções de cache falharão com a \_ mensagem de erro de buffer insuficiente \_ se você especificar um buffer que é muito pequeno para conter as informações de entrada de cache recuperadas pela função.</span><span class="sxs-lookup"><span data-stu-id="eee51-306">Some cache functions fail with the ERROR\_INSUFFICIENT\_BUFFER error message if you specify a buffer that is too small to contain the cache entry information retrieved by the function.</span></span> <span data-ttu-id="eee51-307">Nesse caso, a função também retorna o tamanho necessário do buffer.</span><span class="sxs-lookup"><span data-stu-id="eee51-307">In this case, the function also returns the required size of the buffer.</span></span> <span data-ttu-id="eee51-308">Em seguida, você pode alocar um buffer do tamanho apropriado e chamar a função novamente.</span><span class="sxs-lookup"><span data-stu-id="eee51-308">You can then allocate a buffer of the appropriate size and call the function again.</span></span>

> [!Note]  
> <span data-ttu-id="eee51-309">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="eee51-309">WinINet does not support server implementations.</span></span> <span data-ttu-id="eee51-310">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="eee51-310">In addition, it should not be used from a service.</span></span> <span data-ttu-id="eee51-311">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="eee51-311">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
