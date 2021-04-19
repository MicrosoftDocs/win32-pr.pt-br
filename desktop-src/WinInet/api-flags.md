---
title: Sinalizadores de API (Wininet. h)
description: Muitas das funções do WinINet aceitam uma matriz de sinalizadores como um parâmetro. Veja a seguir uma breve descrição dos sinalizadores definidos.
ms.assetid: 63027a3b-dc59-41c4-a22a-5d6e841159aa
topic_type:
- apiref
api_name:
- INTERNET_COOKIE_EVALUATE_P3P
- INTERNET_COOKIE_THIRD_PARTY
- INTERNET_FLAG_ASYNC
- INTERNET_FLAG_CACHE_ASYNC
- INTERNET_FLAG_CACHE_IF_NET_FAIL
- INTERNET_FLAG_DONT_CACHE
- INTERNET_FLAG_EXISTING_CONNECT
- INTERNET_FLAG_FORMS_SUBMIT
- INTERNET_FLAG_FROM_CACHE
- INTERNET_FLAG_FWD_BACK
- INTERNET_FLAG_HYPERLINK
- INTERNET_FLAG_IGNORE_CERT_CN_INVALID
- INTERNET_FLAG_IGNORE_CERT_DATE_INVALID
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS
- INTERNET_FLAG_KEEP_CONNECTION
- INTERNET_FLAG_MAKE_PERSISTENT
- INTERNET_FLAG_MUST_CACHE_REQUEST
- INTERNET_FLAG_NEED_FILE
- INTERNET_FLAG_NO_AUTH
- INTERNET_FLAG_NO_AUTO_REDIRECT
- INTERNET_FLAG_NO_CACHE_WRITE
- INTERNET_FLAG_NO_COOKIES
- INTERNET_FLAG_NO_UI
- INTERNET_FLAG_OFFLINE
- INTERNET_FLAG_PASSIVE
- INTERNET_FLAG_PRAGMA_NOCACHE
- INTERNET_FLAG_RAW_DATA
- INTERNET_FLAG_READ_PREFETCH
- INTERNET_FLAG_RELOAD
- INTERNET_FLAG_RESTRICTED_ZONE
- INTERNET_FLAG_RESYNCHRONIZE
- INTERNET_FLAG_SECURE
- INTERNET_FLAG_TRANSFER_ASCII
- INTERNET_FLAG_TRANSFER_BINARY
- INTERNET_NO_CALLBACK
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- WININET_API_FLAG_ASYNC
- WININET_API_FLAG_SYNC
- WININET_API_FLAG_USE_CONTEXT
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111bf418e6cf599f99c9dfa34ca0f5025a1d779
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105798240"
---
# <a name="api-flags"></a><span data-ttu-id="a772b-104">Sinalizadores de API</span><span class="sxs-lookup"><span data-stu-id="a772b-104">API Flags</span></span>

<span data-ttu-id="a772b-105">Muitas das funções do WinINet aceitam uma matriz de sinalizadores como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="a772b-105">Many of the WinINet functions accept an array of flags as a parameter.</span></span> <span data-ttu-id="a772b-106">Veja a seguir uma breve descrição dos sinalizadores definidos.</span><span class="sxs-lookup"><span data-stu-id="a772b-106">The following is a brief description of the defined flags.</span></span>

<dl> <dt>

<span data-ttu-id="a772b-107"><span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**O \_ Cookie da Internet \_ avaliar \_ P3P**</span><span class="sxs-lookup"><span data-stu-id="a772b-107"><span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**INTERNET\_COOKIE\_EVALUATE\_P3P**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-108">0x80</span><span class="sxs-lookup"><span data-stu-id="a772b-108">0x80</span></span>
</dt> <dt>



<span data-ttu-id="a772b-109">Indica que uma plataforma para o cabeçalho da proteção de privacidade (P3P) deve ser associada a um cookie.</span><span class="sxs-lookup"><span data-stu-id="a772b-109">Indicates that a Platform for Privacy Protection (P3P) header is to be associated with a cookie.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-110"><span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**COOKIE de INTERNET \_ \_ terceirizado \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-110"><span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**INTERNET\_COOKIE\_THIRD\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-111">0x10</span><span class="sxs-lookup"><span data-stu-id="a772b-111">0x10</span></span>
</dt> <dt>



<span data-ttu-id="a772b-112">Indica que um cookie de terceiros está sendo definido ou recuperado.</span><span class="sxs-lookup"><span data-stu-id="a772b-112">Indicates that a third-party cookie is being set or retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-113"><span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**sinalizador de INTERNET \_ \_ assíncrono**</span><span class="sxs-lookup"><span data-stu-id="a772b-113"><span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**INTERNET\_FLAG\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-114">0x10000000</span><span class="sxs-lookup"><span data-stu-id="a772b-114">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-115">Faz com que somente solicitações assíncronas em identificadores sejam decrescentes do identificador retornado por essa função.</span><span class="sxs-lookup"><span data-stu-id="a772b-115">Makes only asynchronous requests on handles descended from the handle returned from this function.</span></span> <span data-ttu-id="a772b-116">Somente a função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="a772b-116">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-117"><span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**CACHE de sinalizador da INTERNET \_ \_ \_ assíncrono**</span><span class="sxs-lookup"><span data-stu-id="a772b-117"><span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**INTERNET\_FLAG\_CACHE\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-118">0x00000080</span><span class="sxs-lookup"><span data-stu-id="a772b-118">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="a772b-119">Permite uma gravação de cache lenta.</span><span class="sxs-lookup"><span data-stu-id="a772b-119">Allows a lazy cache write.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-120"><span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**CACHE de sinalizador da INTERNET \_ \_ \_ se \_ net \_ falhar**</span><span class="sxs-lookup"><span data-stu-id="a772b-120"><span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**INTERNET\_FLAG\_CACHE\_IF\_NET\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-121">0x00010000</span><span class="sxs-lookup"><span data-stu-id="a772b-121">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-122">Retorna o recurso do cache se a solicitação de rede para o recurso falhar devido a um [erro \_ de \_ \_ redefinição de conexão com a Internet](wininet-errors.md) ou [erro a \_ Internet \_ não pode \_ se conectar](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="a772b-122">Returns the resource from the cache if the network request for the resource fails due to an [ERROR\_INTERNET\_CONNECTION\_RESET](wininet-errors.md) or [ERROR\_INTERNET\_CANNOT\_CONNECT](wininet-errors.md) error.</span></span> <span data-ttu-id="a772b-123">Esse sinalizador é usado pelo [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="a772b-123">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-124"><span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**sinalizador da INTERNET não \_ \_ \_ cache**</span><span class="sxs-lookup"><span data-stu-id="a772b-124"><span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**INTERNET\_FLAG\_DONT\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-125">0x04000000</span><span class="sxs-lookup"><span data-stu-id="a772b-125">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-126">Não adiciona a entidade retornada ao cache.</span><span class="sxs-lookup"><span data-stu-id="a772b-126">Does not add the returned entity to the cache.</span></span> <span data-ttu-id="a772b-127">Isso é idêntico ao valor preferencial, [Internet \_ Flag \_ sem \_ \_ gravação de cache](/windows).</span><span class="sxs-lookup"><span data-stu-id="a772b-127">This is identical to the preferred value, [INTERNET\_FLAG\_NO\_CACHE\_WRITE](/windows).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-128"><span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**conexão do sinalizador de INTERNET \_ \_ existente \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-128"><span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**INTERNET\_FLAG\_EXISTING\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-129">0x20000000</span><span class="sxs-lookup"><span data-stu-id="a772b-129">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-130">Tenta usar um objeto [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) existente se existir um com os mesmos atributos necessários para fazer a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a772b-130">Attempts to use an existing [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) object if one exists with the same attributes required to make the request.</span></span> <span data-ttu-id="a772b-131">Isso é útil apenas com as operações de FTP, pois o FTP é o único protocolo que normalmente executa várias operações durante a mesma sessão.</span><span class="sxs-lookup"><span data-stu-id="a772b-131">This is useful only with FTP operations, since FTP is the only protocol that typically performs multiple operations during the same session.</span></span> <span data-ttu-id="a772b-132">O WinINet armazena em cache um único identificador de conexão para cada identificador de [**HINTERNET**](appendix-a-hinternet-handles.md) gerado pelo [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="a772b-132">WinINet caches a single connection handle for each [**HINTERNET**](appendix-a-hinternet-handles.md) handle generated by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="a772b-133">As funções [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) e **InternetConnect** usam esse sinalizador para conexões http e FTP.</span><span class="sxs-lookup"><span data-stu-id="a772b-133">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and **InternetConnect** functions use this flag for Http and Ftp connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-134"><span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**\_envio de \_ formulários de sinalizador da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-134"><span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**INTERNET\_FLAG\_FORMS\_SUBMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-135">0x00000040</span><span class="sxs-lookup"><span data-stu-id="a772b-135">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="a772b-136">Indica que se trata de um envio de formulários.</span><span class="sxs-lookup"><span data-stu-id="a772b-136">Indicates that this is a Forms submission.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-137"><span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**\_sinalizador \_ da Internet do \_ cache**</span><span class="sxs-lookup"><span data-stu-id="a772b-137"><span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**INTERNET\_FLAG\_FROM\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-138">0x01000000</span><span class="sxs-lookup"><span data-stu-id="a772b-138">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-139">Não faz solicitações de rede.</span><span class="sxs-lookup"><span data-stu-id="a772b-139">Does not make network requests.</span></span> <span data-ttu-id="a772b-140">Todas as entidades são retornadas do cache.</span><span class="sxs-lookup"><span data-stu-id="a772b-140">All entities are returned from the cache.</span></span> <span data-ttu-id="a772b-141">Se o item solicitado não estiver no cache, um erro adequado, como o arquivo de \_ erro \_ não \_ encontrado, será retornado.</span><span class="sxs-lookup"><span data-stu-id="a772b-141">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="a772b-142">Somente a função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="a772b-142">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-143"><span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**sinalizador de INTERNET do \_ \_ FWD \_ back**</span><span class="sxs-lookup"><span data-stu-id="a772b-143"><span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**INTERNET\_FLAG\_FWD\_BACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-144">0x00000020</span><span class="sxs-lookup"><span data-stu-id="a772b-144">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="a772b-145">Indica que a função deve usar a cópia do recurso que está atualmente no cache da Internet.</span><span class="sxs-lookup"><span data-stu-id="a772b-145">Indicates that the function should use the copy of the resource that is currently in the Internet cache.</span></span> <span data-ttu-id="a772b-146">A data de validade e outras informações sobre o recurso não são verificadas.</span><span class="sxs-lookup"><span data-stu-id="a772b-146">The expiration date and other information about the resource is not checked.</span></span> <span data-ttu-id="a772b-147">Se o item solicitado não for encontrado no cache da Internet, o sistema tentará localizar o recurso na rede.</span><span class="sxs-lookup"><span data-stu-id="a772b-147">If the requested item is not found in the Internet cache, the system attempts to locate the resource on the network.</span></span> <span data-ttu-id="a772b-148">Esse valor foi introduzido no Microsoft Internet Explorer 5 e está associado às operações de botão **Avançar** e **voltar** do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a772b-148">This value was introduced in Microsoft Internet Explorer 5 and is associated with the **Forward** and **Back** button operations of Internet Explorer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-149"><span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**\_hiperlink de sinalizador da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-149"><span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**INTERNET\_FLAG\_HYPERLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-150">0x00000400</span><span class="sxs-lookup"><span data-stu-id="a772b-150">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="a772b-151">Força uma recarga se não houver tempo de expiração e nenhum horário de LastModified retornado do servidor ao determinar se deseja recarregar o item da rede.</span><span class="sxs-lookup"><span data-stu-id="a772b-151">Forces a reload if there is no Expires time and no LastModified time returned from the server when determining whether to reload the item from the network.</span></span> <span data-ttu-id="a772b-152">Esse sinalizador pode ser usado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="a772b-152">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="a772b-153">**Windows XP e Windows Server 2003 R2 e anteriores:** Também usado por [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="a772b-153">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-154"><span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**sinalizador da INTERNET \_ \_ ignorar \_ CN do certificado \_ \_ inválido**</span><span class="sxs-lookup"><span data-stu-id="a772b-154"><span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**INTERNET\_FLAG\_IGNORE\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-155">0x00001000</span><span class="sxs-lookup"><span data-stu-id="a772b-155">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-156">Desabilita a verificação de certificados baseados em SSL/PCT que são retornados do servidor em relação ao nome de host fornecido na solicitação.</span><span class="sxs-lookup"><span data-stu-id="a772b-156">Disables checking of SSL/PCT-based certificates that are returned from the server against the host name given in the request.</span></span> <span data-ttu-id="a772b-157">O WinINet usa uma verificação simples em relação a certificados por meio da comparação de nomes de host correspondentes e regras de curinga simples.</span><span class="sxs-lookup"><span data-stu-id="a772b-157">WinINet uses a simple check against certificates by comparing for matching host names and simple wildcarding rules.</span></span> <span data-ttu-id="a772b-158">Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para solicitações HTTP).</span><span class="sxs-lookup"><span data-stu-id="a772b-158">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-159"><span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**sinalizador de INTERNET \_ \_ ignorar \_ data de certificado \_ \_ inválida**</span><span class="sxs-lookup"><span data-stu-id="a772b-159"><span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**INTERNET\_FLAG\_IGNORE\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-160">0x00002000</span><span class="sxs-lookup"><span data-stu-id="a772b-160">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-161">Desabilita a verificação de certificados baseados em SSL/PCT para datas de validade adequadas.</span><span class="sxs-lookup"><span data-stu-id="a772b-161">Disables checking of SSL/PCT-based certificates for proper validity dates.</span></span> <span data-ttu-id="a772b-162">Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para solicitações HTTP).</span><span class="sxs-lookup"><span data-stu-id="a772b-162">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-163"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**sinalizador da INTERNET \_ \_ ignorar \_ redirecionamento \_ para \_ http**</span><span class="sxs-lookup"><span data-stu-id="a772b-163"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**INTERNET\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-164">0x00008000</span><span class="sxs-lookup"><span data-stu-id="a772b-164">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-165">Desabilita a detecção desse tipo especial de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="a772b-165">Disables detection of this special type of redirect.</span></span> <span data-ttu-id="a772b-166">Quando esse sinalizador é usado, o WinINet permite de forma transparente redirecionamentos de HTTPS para URLs HTTP.</span><span class="sxs-lookup"><span data-stu-id="a772b-166">When this flag is used, WinINet transparently allows redirects from HTTPS to HTTP URLs.</span></span> <span data-ttu-id="a772b-167">Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para solicitações HTTP).</span><span class="sxs-lookup"><span data-stu-id="a772b-167">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-168"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**sinalizador da INTERNET \_ \_ ignorar \_ redirecionamento \_ para \_ https**</span><span class="sxs-lookup"><span data-stu-id="a772b-168"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**INTERNET\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-169">0x00004000</span><span class="sxs-lookup"><span data-stu-id="a772b-169">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-170">Desabilita a detecção desse tipo especial de redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="a772b-170">Disables detection of this special type of redirect.</span></span> <span data-ttu-id="a772b-171">Quando esse sinalizador é usado, o WinINet permite redirecionar de forma transparente as URLs de HTTP para HTTPS.</span><span class="sxs-lookup"><span data-stu-id="a772b-171">When this flag is used, WinINet transparently allow redirects from HTTP to HTTPS URLs.</span></span> <span data-ttu-id="a772b-172">Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para solicitações HTTP).</span><span class="sxs-lookup"><span data-stu-id="a772b-172">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-173"><span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**sinalizador de INTERNET \_ \_ manter \_ conexão**</span><span class="sxs-lookup"><span data-stu-id="a772b-173"><span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**INTERNET\_FLAG\_KEEP\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-174">0x00400000</span><span class="sxs-lookup"><span data-stu-id="a772b-174">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-175">Usa semântica Keep-Alive, se disponível, para a conexão.</span><span class="sxs-lookup"><span data-stu-id="a772b-175">Uses keep-alive semantics, if available, for the connection.</span></span> <span data-ttu-id="a772b-176">Esse sinalizador é usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para solicitações HTTP).</span><span class="sxs-lookup"><span data-stu-id="a772b-176">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span> <span data-ttu-id="a772b-177">Esse sinalizador é necessário para o Microsoft Network (MSN), o NTLM e outros tipos de autenticação.</span><span class="sxs-lookup"><span data-stu-id="a772b-177">This flag is required for Microsoft Network (MSN), NTLM, and other types of authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-178"><span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**sinalizador da INTERNET \_ \_ tornar \_ persistente**</span><span class="sxs-lookup"><span data-stu-id="a772b-178"><span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**INTERNET\_FLAG\_MAKE\_PERSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-179">0x02000000</span><span class="sxs-lookup"><span data-stu-id="a772b-179">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-180">Não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="a772b-180">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-181"><span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**o \_ sinalizador da Internet \_ deve \_ armazenar a solicitação em cache \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-181"><span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**INTERNET\_FLAG\_MUST\_CACHE\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a772b-182">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="a772b-183">Idêntico ao valor preferencial, o **sinalizador de Internet \_ \_ precisa de \_ arquivo**.</span><span class="sxs-lookup"><span data-stu-id="a772b-183">Identical to the preferred value, **INTERNET\_FLAG\_NEED\_FILE**.</span></span> <span data-ttu-id="a772b-184">Faz com que um arquivo temporário seja criado se o arquivo não puder ser armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="a772b-184">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="a772b-185">Esse sinalizador pode ser usado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="a772b-185">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="a772b-186">**Windows XP e Windows Server 2003 R2 e anteriores:** Também usado por [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="a772b-186">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-187"><span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**sinalizador de INTERNET- \_ \_ \_ arquivo necessário**</span><span class="sxs-lookup"><span data-stu-id="a772b-187"><span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**INTERNET\_FLAG\_NEED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-188">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a772b-188">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="a772b-189">Faz com que um arquivo temporário seja criado se o arquivo não puder ser armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="a772b-189">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="a772b-190">Esse sinalizador pode ser usado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="a772b-190">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="a772b-191">**Windows XP e Windows Server 2003 R2 e anteriores:** Também usado por [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="a772b-191">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-192"><span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**sinalizador da INTERNET \_ \_ sem \_ autenticação**</span><span class="sxs-lookup"><span data-stu-id="a772b-192"><span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**INTERNET\_FLAG\_NO\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-193">0x00040000</span><span class="sxs-lookup"><span data-stu-id="a772b-193">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-194">O não tenta a autenticação automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a772b-194">Does not attempt authentication automatically.</span></span> <span data-ttu-id="a772b-195">Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para solicitações HTTP).</span><span class="sxs-lookup"><span data-stu-id="a772b-195">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-196"><span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**sinalizador da INTERNET \_ \_ sem \_ \_ redirecionamento automático**</span><span class="sxs-lookup"><span data-stu-id="a772b-196"><span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**INTERNET\_FLAG\_NO\_AUTO\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-197">0x00200000</span><span class="sxs-lookup"><span data-stu-id="a772b-197">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-198">O não manipula automaticamente o redirecionamento no [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="a772b-198">Does not automatically handle redirection in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="a772b-199">Esse sinalizador também pode ser usado pelo [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) para solicitações HTTP.</span><span class="sxs-lookup"><span data-stu-id="a772b-199">This flag can also be used by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) for HTTP requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-200"><span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**sinalizador da INTERNET \_ \_ sem \_ gravação de cache \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-200"><span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**INTERNET\_FLAG\_NO\_CACHE\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-201">0x04000000</span><span class="sxs-lookup"><span data-stu-id="a772b-201">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-202">Não adiciona a entidade retornada ao cache.</span><span class="sxs-lookup"><span data-stu-id="a772b-202">Does not add the returned entity to the cache.</span></span> <span data-ttu-id="a772b-203">Esse sinalizador é usado por, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="a772b-203">This flag is used by , [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="a772b-204">**Windows XP e Windows Server 2003 R2 e anteriores:** Também usado por [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="a772b-204">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-205"><span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**sinalizador da INTERNET \_ \_ sem \_ cookies**</span><span class="sxs-lookup"><span data-stu-id="a772b-205"><span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**INTERNET\_FLAG\_NO\_COOKIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-206">0x00080000</span><span class="sxs-lookup"><span data-stu-id="a772b-206">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-207">Não adiciona automaticamente cabeçalhos de cookie a solicitações e não adiciona automaticamente cookies retornados ao banco de dados de cookie.</span><span class="sxs-lookup"><span data-stu-id="a772b-207">Does not automatically add cookie headers to requests, and does not automatically add returned cookies to the cookie database.</span></span> <span data-ttu-id="a772b-208">Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (para solicitações HTTP).</span><span class="sxs-lookup"><span data-stu-id="a772b-208">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-209"><span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**\_sinalizador \_ da Internet sem \_ interface do usuário**</span><span class="sxs-lookup"><span data-stu-id="a772b-209"><span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**INTERNET\_FLAG\_NO\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-210">0x00000200</span><span class="sxs-lookup"><span data-stu-id="a772b-210">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="a772b-211">Desabilita a caixa de diálogo cookie.</span><span class="sxs-lookup"><span data-stu-id="a772b-211">Disables the cookie dialog box.</span></span> <span data-ttu-id="a772b-212">Esse sinalizador pode ser usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (somente solicitações HTTP).</span><span class="sxs-lookup"><span data-stu-id="a772b-212">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (HTTP requests only).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-213"><span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**sinalizador de INTERNET \_ \_ offline**</span><span class="sxs-lookup"><span data-stu-id="a772b-213"><span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**INTERNET\_FLAG\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-214">0x01000000</span><span class="sxs-lookup"><span data-stu-id="a772b-214">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-215">Idêntico ao **\_ sinalizador \_ da Internet do \_ cache**.</span><span class="sxs-lookup"><span data-stu-id="a772b-215">Identical to **INTERNET\_FLAG\_FROM\_CACHE**.</span></span> <span data-ttu-id="a772b-216">Não faz solicitações de rede.</span><span class="sxs-lookup"><span data-stu-id="a772b-216">Does not make network requests.</span></span> <span data-ttu-id="a772b-217">Todas as entidades são retornadas do cache.</span><span class="sxs-lookup"><span data-stu-id="a772b-217">All entities are returned from the cache.</span></span> <span data-ttu-id="a772b-218">Se o item solicitado não estiver no cache, um erro adequado, como o arquivo de \_ erro \_ não \_ encontrado, será retornado.</span><span class="sxs-lookup"><span data-stu-id="a772b-218">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="a772b-219">Somente a função [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="a772b-219">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-220"><span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**sinalizador de INTERNET \_ \_ passivo**</span><span class="sxs-lookup"><span data-stu-id="a772b-220"><span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**INTERNET\_FLAG\_PASSIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-221">0x08000000</span><span class="sxs-lookup"><span data-stu-id="a772b-221">0x08000000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-222">Usa a semântica de FTP passiva.</span><span class="sxs-lookup"><span data-stu-id="a772b-222">Uses passive FTP semantics.</span></span> <span data-ttu-id="a772b-223">Somente [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usam esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="a772b-223">Only [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) use this flag.</span></span> <span data-ttu-id="a772b-224">O [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa esse sinalizador para solicitações de FTP e o [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa esse sinalizador para arquivos e diretórios FTP.</span><span class="sxs-lookup"><span data-stu-id="a772b-224">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) uses this flag for FTP requests, and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) uses this flag for FTP files and directories.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-225"><span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**PRAGMA do sinalizador de INTERNET \_ \_ \_ NoCache**</span><span class="sxs-lookup"><span data-stu-id="a772b-225"><span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**INTERNET\_FLAG\_PRAGMA\_NOCACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-226">0x00000100</span><span class="sxs-lookup"><span data-stu-id="a772b-226">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="a772b-227">Força a solicitação a ser resolvida pelo servidor de origem, mesmo que exista uma cópia armazenada em cache no proxy.</span><span class="sxs-lookup"><span data-stu-id="a772b-227">Forces the request to be resolved by the origin server, even if a cached copy exists on the proxy.</span></span> <span data-ttu-id="a772b-228">A função [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (somente em solicitações HTTP e HTTPS) e a função [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) usam esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="a772b-228">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function (on HTTP and HTTPS requests only) and [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function use this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-229"><span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**sinalizador de INTERNET \_ \_ dados brutos \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-229"><span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**INTERNET\_FLAG\_RAW\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-230">0x40000000</span><span class="sxs-lookup"><span data-stu-id="a772b-230">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-231">Retorna os dados como uma estrutura de [**\_ \_ dados de localização do Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) ao recuperar informações do diretório FTP.</span><span class="sxs-lookup"><span data-stu-id="a772b-231">Returns the data as a [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure when retrieving FTP directory information.</span></span> <span data-ttu-id="a772b-232">Se esse sinalizador não for especificado ou se a chamada for feita por meio de um proxy CERN, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) retornará a versão HTML do diretório.</span><span class="sxs-lookup"><span data-stu-id="a772b-232">If this flag is not specified or if the call is made through a CERN proxy, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) returns the HTML version of the directory.</span></span> <span data-ttu-id="a772b-233">Somente a função [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usa esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="a772b-233">Only the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function uses this flag.</span></span>

<span data-ttu-id="a772b-234">**Windows XP e Windows Server 2003 R2 e anteriores:** Também retorna uma estrutura de [**\_ \_ dados de localização do Gopher**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) ao recuperar informações de diretório do Gopher.</span><span class="sxs-lookup"><span data-stu-id="a772b-234">**Windows XP and Windows Server 2003 R2 and earlier:** Also returns a [**GOPHER\_FIND\_DATA**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) structure when retrieving Gopher directory information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-235"><span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**\_pré-busca de \_ leitura do sinalizador da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-235"><span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**INTERNET\_FLAG\_READ\_PREFETCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-236">0x00100000</span><span class="sxs-lookup"><span data-stu-id="a772b-236">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-237">Este sinalizador está desabilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="a772b-237">This flag is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-238"><span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**recarregamento de sinalizador da INTERNET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-238"><span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**INTERNET\_FLAG\_RELOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-239">0x80000000</span><span class="sxs-lookup"><span data-stu-id="a772b-239">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-240">Força um download da listagem de arquivo, objeto ou diretório solicitada do servidor de origem, não do cache.</span><span class="sxs-lookup"><span data-stu-id="a772b-240">Forces a download of the requested file, object, or directory listing from the origin server, not from the cache.</span></span> <span data-ttu-id="a772b-241">As funções [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) usam esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="a772b-241">The [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) functions use this flag.</span></span>

<span data-ttu-id="a772b-242">**Windows XP e Windows Server 2003 R2 e anteriores:** Também usado por [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="a772b-242">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-243"><span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**\_ \_ zona restrita de sinalizador da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-243"><span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**INTERNET\_FLAG\_RESTRICTED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-244">0x00020000</span><span class="sxs-lookup"><span data-stu-id="a772b-244">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-245">Indica que o cookie que está sendo definido está associado a um site não confiável.</span><span class="sxs-lookup"><span data-stu-id="a772b-245">Indicates that the cookie being set is associated with an untrusted site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-246"><span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**sinalizador de INTERNET \_ \_ ressincronizar**</span><span class="sxs-lookup"><span data-stu-id="a772b-246"><span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**INTERNET\_FLAG\_RESYNCHRONIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-247">0x00000800</span><span class="sxs-lookup"><span data-stu-id="a772b-247">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="a772b-248">Recarregará recursos HTTP se o recurso tiver sido modificado desde a última vez que foi baixado.</span><span class="sxs-lookup"><span data-stu-id="a772b-248">Reloads HTTP resources if the resource has been modified since the last time it was downloaded.</span></span> <span data-ttu-id="a772b-249">Todos os recursos de FTP são recarregados.</span><span class="sxs-lookup"><span data-stu-id="a772b-249">All FTP resources are reloaded.</span></span> <span data-ttu-id="a772b-250">Esse sinalizador pode ser usado por [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="a772b-250">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="a772b-251">**Windows XP e Windows Server 2003 R2 e anteriores:** Também usado por [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) e [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), e os recursos de Gopher são recarregados.</span><span class="sxs-lookup"><span data-stu-id="a772b-251">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), and Gopher resources are reloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-252"><span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**sinalizador de INTERNET \_ \_ seguro**</span><span class="sxs-lookup"><span data-stu-id="a772b-252"><span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**INTERNET\_FLAG\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-253">0x00800000</span><span class="sxs-lookup"><span data-stu-id="a772b-253">0x00800000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-254">Usa semântica de transação segura.</span><span class="sxs-lookup"><span data-stu-id="a772b-254">Uses secure transaction semantics.</span></span> <span data-ttu-id="a772b-255">Isso se traduz em usar a tecnologia de comunicação protocolo SSL/privada (SSL/PCT) e só é significativo em solicitações HTTP.</span><span class="sxs-lookup"><span data-stu-id="a772b-255">This translates to using Secure Sockets Layer/Private Communications Technology (SSL/PCT) and is only meaningful in HTTP requests.</span></span> <span data-ttu-id="a772b-256">Esse sinalizador é usado por [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) e [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), mas isso será redundante se https://aparecer na URL. A função [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) usa esse sinalizador para conexões http; todos os identificadores de solicitação criados nessa conexão herdarão esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="a772b-256">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), but this is redundant if https:// appears in the URL.The [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function uses this flag for HTTP connections; all the request handles created under this connection will inherit this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-257"><span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**\_ASCII de \_ transferência de sinalizador da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-257"><span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**INTERNET\_FLAG\_TRANSFER\_ASCII**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-258">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a772b-258">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="a772b-259">Transfere o arquivo como ASCII (somente FTP).</span><span class="sxs-lookup"><span data-stu-id="a772b-259">Transfers file as ASCII (FTP only).</span></span> <span data-ttu-id="a772b-260">Esse sinalizador pode ser usado por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)e [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="a772b-260">This flag can be used by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), and [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-261"><span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**\_binário de \_ transferência de sinalizador da Internet \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-261"><span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**INTERNET\_FLAG\_TRANSFER\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-262">0x00000002</span><span class="sxs-lookup"><span data-stu-id="a772b-262">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="a772b-263">Transfere o arquivo como binário (somente FTP).</span><span class="sxs-lookup"><span data-stu-id="a772b-263">Transfers file as binary (FTP only).</span></span> <span data-ttu-id="a772b-264">Esse sinalizador pode ser usado por [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)e [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="a772b-264">This flag can be used by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), and [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-265"><span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**INTERNET \_ sem \_ retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="a772b-265"><span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**INTERNET\_NO\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a772b-266">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="a772b-267">Indica que nenhum retorno de chamada deve ser feito para essa API.</span><span class="sxs-lookup"><span data-stu-id="a772b-267">Indicates that no callbacks should be made for that API.</span></span> <span data-ttu-id="a772b-268">Isso é usado para o parâmetro *dxContext* das funções que permitem operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="a772b-268">This is used for the *dxContext* parameter of the functions that allow asynchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-269"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**opção de INTERNET \_ \_ suprimir \_ autenticação de servidor \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-269"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-270">104</span><span class="sxs-lookup"><span data-stu-id="a772b-270">104</span></span>
</dt> <dt>



<span data-ttu-id="a772b-271">Define um objeto de solicitação HTTP de modo que ele não fará logon nos servidores de origem, mas executará o logon automático em servidores proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="a772b-271">Sets an HTTP request object such that it will not logon to origin servers, but will perform automatic logon to HTTP proxy servers.</span></span> <span data-ttu-id="a772b-272">Essa opção é diferente do sinalizador de solicitação da \_ Internet \_ sem \_ autenticação, o que impede a autenticação tanto nos servidores proxy quanto nos servidores de origem.</span><span class="sxs-lookup"><span data-stu-id="a772b-272">This option differs from the Request flag INTERNET\_FLAG\_NO\_AUTH, which prevents authentication to both proxy servers and origin servers.</span></span> <span data-ttu-id="a772b-273">Definir esse modo irá suprimir o uso de qualquer material de credencial (anteriormente fornecido nome de usuário/senha ou certificado SSL de cliente) ao se comunicar com um servidor de origem.</span><span class="sxs-lookup"><span data-stu-id="a772b-273">Setting this mode will suppress the use of any credential material (either previously provided username/password or client SSL certificate) when communicating with an origin server.</span></span> <span data-ttu-id="a772b-274">No entanto, se a solicitação precisar transitar por meio de um proxy de autenticação, o WinINet ainda executará a autenticação automática para o proxy HTTP de acordo com as configurações de zona da intranet do usuário.</span><span class="sxs-lookup"><span data-stu-id="a772b-274">However, if the request must transit via an authenticating proxy, WinINet will still perform automatic authentication to the HTTP proxy per the Intranet Zone settings for the user.</span></span> <span data-ttu-id="a772b-275">A configuração de zona da intranet padrão é permitir o logon automático usando as credenciais padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="a772b-275">The default Intranet Zone setting is to permit automatic logon using the user s default credentials.</span></span> <span data-ttu-id="a772b-276">Para garantir a supressão de todas as informações de identificação, o chamador deve combinar a opção da INTERNET \_ \_ suprimir a \_ autenticação do servidor \_ com o sinalizador Internet sem sinalizador de \_ solicitação de \_ \_ cookies.</span><span class="sxs-lookup"><span data-stu-id="a772b-276">To ensure suppression of all identifying information, the caller should combine INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH with the INTERNET\_FLAG\_NO\_COOKIES request flag.</span></span> <span data-ttu-id="a772b-277">Essa opção só pode ser definida em objetos de solicitação antes de serem enviadas.</span><span class="sxs-lookup"><span data-stu-id="a772b-277">This option may only be set on request objects before they have been sent.</span></span> <span data-ttu-id="a772b-278">As tentativas de definir essa opção após a solicitação ter sido enviada retornarão \_ um \_ estado de identificador incorreto da Internet \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a772b-278">Attempts to set this option after the request has been sent will return ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE.</span></span> <span data-ttu-id="a772b-279">Nenhum buffer é necessário para essa opção.</span><span class="sxs-lookup"><span data-stu-id="a772b-279">No buffer is required for this option.</span></span> <span data-ttu-id="a772b-280">Isso é usado por InternetSetOption em identificadores retornados apenas por HttpOpenRequest.</span><span class="sxs-lookup"><span data-stu-id="a772b-280">This is used by InternetSetOption on handles returned by HttpOpenRequest only.</span></span> <span data-ttu-id="a772b-281">Versão: requer o Internet Explorer 8,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="a772b-281">Version: Requires Internet Explorer 8.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-282"><span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**sinalizador de API do WININET \_ \_ \_ assíncrono**</span><span class="sxs-lookup"><span data-stu-id="a772b-282"><span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**WININET\_API\_FLAG\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-283">0x00000001</span><span class="sxs-lookup"><span data-stu-id="a772b-283">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="a772b-284">Força operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="a772b-284">Forces asynchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-285"><span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**\_sincronização de \_ sinalizador de API do Wininet \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-285"><span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**WININET\_API\_FLAG\_SYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-286">0x00000004</span><span class="sxs-lookup"><span data-stu-id="a772b-286">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="a772b-287">Força operações síncronas.</span><span class="sxs-lookup"><span data-stu-id="a772b-287">Forces synchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a772b-288"><span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**\_contexto de \_ uso de sinalizador de API do Wininet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a772b-288"><span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**WININET\_API\_FLAG\_USE\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a772b-289">0x00000008</span><span class="sxs-lookup"><span data-stu-id="a772b-289">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="a772b-290">Força a API a usar o valor de contexto, mesmo se ele estiver definido como zero.</span><span class="sxs-lookup"><span data-stu-id="a772b-290">Forces the API to use the context value, even if it is set to zero.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a772b-291">Comentários</span><span class="sxs-lookup"><span data-stu-id="a772b-291">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a772b-292">O WinINet não oferece suporte a implementações de servidor.</span><span class="sxs-lookup"><span data-stu-id="a772b-292">WinINet does not support server implementations.</span></span> <span data-ttu-id="a772b-293">Além disso, ele não deve ser usado de um serviço.</span><span class="sxs-lookup"><span data-stu-id="a772b-293">In addition, it should not be used from a service.</span></span> <span data-ttu-id="a772b-294">Para implementações de servidor ou serviços, use [o Microsoft Windows http Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="a772b-294">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a772b-295">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a772b-295">Requirements</span></span>



| <span data-ttu-id="a772b-296">Requisito</span><span class="sxs-lookup"><span data-stu-id="a772b-296">Requirement</span></span> | <span data-ttu-id="a772b-297">Valor</span><span class="sxs-lookup"><span data-stu-id="a772b-297">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a772b-298">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a772b-298">Minimum supported client</span></span><br/> | <span data-ttu-id="a772b-299">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a772b-299">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a772b-300">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a772b-300">Minimum supported server</span></span><br/> | <span data-ttu-id="a772b-301">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a772b-301">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a772b-302">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a772b-302">Header</span></span><br/>                   | <dl> <span data-ttu-id="a772b-303"><dt>WinInet. h</dt></span><span class="sxs-lookup"><span data-stu-id="a772b-303"><dt>Wininet.h</dt></span></span> </dl> |



 

