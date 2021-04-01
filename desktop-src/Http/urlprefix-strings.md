---
title: Cadeias de caracteres de UrlPrefix
description: Na API do servidor HTTP, um UrlPrefix é uma cadeia de caracteres Unicode de caractere largo (UTF-16) com um formato canônico que especifica uma seção do namespace da URL.
ms.assetid: 4f317bf6-ee6a-47a8-a531-78534217109d
keywords:
- API de servidor HTTP de cadeia de caracteres UrlPrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bddc484f26bc1b3de5d20196dadec9201d3ea272
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103642959"
---
# <a name="urlprefix-strings"></a><span data-ttu-id="b4cdd-104">Cadeias de caracteres de UrlPrefix</span><span class="sxs-lookup"><span data-stu-id="b4cdd-104">UrlPrefix Strings</span></span>

<span data-ttu-id="b4cdd-105">Na API do servidor HTTP, um *URLPrefix* é uma cadeia de caracteres Unicode de caractere largo (UTF-16) com um formato canônico que especifica uma seção do namespace da URL.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-105">In the HTTP Server API, a *UrlPrefix* is a wide-character (UTF-16) Unicode string with a canonical form that specifies a section of URL namespace.</span></span> <span data-ttu-id="b4cdd-106">Ele é usado para reservar uma seção do namespace de URL para uma conta de usuário ou registrar uma seção do namespace de URL para um processo.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-106">It is used to reserve a section of URL namespace for a user account or register a section of URL namespace for a process.</span></span>

## <a name="urlprefix-format"></a><span data-ttu-id="b4cdd-107">Formato UrlPrefix</span><span class="sxs-lookup"><span data-stu-id="b4cdd-107">UrlPrefix Format</span></span>

<span data-ttu-id="b4cdd-108">Um UrlPrefix tem a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="b4cdd-108">A UrlPrefix has the following syntax:</span></span>

<span data-ttu-id="b4cdd-109">"Scheme://host: Port/relativeURI"</span><span class="sxs-lookup"><span data-stu-id="b4cdd-109">"scheme://host:port/relativeURI"</span></span>

<span data-ttu-id="b4cdd-110">O esquema, o host e os elementos de porta de um UrlPrefix devem estar presentes e não vazios e devem obedecer às seguintes regras:</span><span class="sxs-lookup"><span data-stu-id="b4cdd-110">The scheme, host and port elements of a UrlPrefix must be present and non-empty, and must obey the following rules:</span></span>

<dl> <dt>

<span data-ttu-id="b4cdd-111"><span id="scheme"></span><span id="SCHEME"></span>esquema</span><span class="sxs-lookup"><span data-stu-id="b4cdd-111"><span id="scheme"></span><span id="SCHEME"></span>scheme</span></span>
</dt> <dd>

<span data-ttu-id="b4cdd-112">Deve ser http ou HTTPS, em minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-112">Must be either http or https, all in lowercase.</span></span>

</dd> <dt>

<span data-ttu-id="b4cdd-113"><span id="host"></span><span id="HOST"></span>hospedeira</span><span class="sxs-lookup"><span data-stu-id="b4cdd-113"><span id="host"></span><span id="HOST"></span>host</span></span>
</dt> <dd>

<span data-ttu-id="b4cdd-114">Deve ser um nome de domínio totalmente qualificado, uma cadeia de caracteres literal IPv4 ou IPv6 ou um curinga.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-114">Must be a fully qualified domain name, an IPv4 or IPv6 literal string, or a wildcard.</span></span> <span data-ttu-id="b4cdd-115">Ao contrário do esquema, que deve estar em letras minúsculas, a parte do host não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-115">Unlike the scheme, which must be lowercase, the host portion is case-insensitive.</span></span> <span data-ttu-id="b4cdd-116">Dependendo de como sua parte de host é especificada, um UrlPrefix se enquadra em uma das quatro categorias de roteamento a seguir, que são descritas em mais detalhes abaixo:</span><span class="sxs-lookup"><span data-stu-id="b4cdd-116">Depending on how its host portion is specified, a UrlPrefix falls into one of the following four routing categories, which are described in more detail below:</span></span>

<dl> <dd><span data-ttu-id="b4cdd-117">Curinga forte</span><span class="sxs-lookup"><span data-stu-id="b4cdd-117">Strong wildcard</span></span></dd> <dd><span data-ttu-id="b4cdd-118">Explícita</span><span class="sxs-lookup"><span data-stu-id="b4cdd-118">Explicit</span></span></dd> <dd><span data-ttu-id="b4cdd-119">Curinga fraco com limite de IP</span><span class="sxs-lookup"><span data-stu-id="b4cdd-119">IP-bound weak wildcard</span></span></dd> <dd><span data-ttu-id="b4cdd-120">Curinga fraco</span><span class="sxs-lookup"><span data-stu-id="b4cdd-120">Weak wildcard</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="b4cdd-121"><span id="port"></span><span id="PORT"></span>Porto</span><span class="sxs-lookup"><span data-stu-id="b4cdd-121"><span id="port"></span><span id="PORT"></span>port</span></span>
</dt> <dd>

<span data-ttu-id="b4cdd-122">Uma cadeia de caracteres numérica decimal que não começa com zero e que representa um número de porta TCP válido (de 1 a 65.535).</span><span class="sxs-lookup"><span data-stu-id="b4cdd-122">A decimal numeric string that does not start with zero and that represents a valid TCP port number (1 to 65,535).</span></span> <span data-ttu-id="b4cdd-123">Esse valor não pode ser um caractere curinga.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-123">This value cannot be a wildcard.</span></span>

</dd> <dt>

<span data-ttu-id="b4cdd-124"><span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI</span><span class="sxs-lookup"><span data-stu-id="b4cdd-124"><span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI</span></span>
</dt> <dd>

<span data-ttu-id="b4cdd-125">O elemento relativeURI é opcional, mas, se presente, deve ser sempre seguido por um caractere de barra ("/").</span><span class="sxs-lookup"><span data-stu-id="b4cdd-125">The relativeURI element is optional, but if present must always be followed by a slash character ("/").</span></span> <span data-ttu-id="b4cdd-126">Essa é uma cadeia de caracteres de prefixo que indica uma subárvore dentro do namespace da máquina especificado em relação ao esquema, ao host e aos valores de porta.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-126">This is a prefix string that indicates a subtree within the machine's namespace specified relative to the scheme, host and port values.</span></span> <span data-ttu-id="b4cdd-127">Ao contrário do esquema, que deve estar em letras minúsculas, a parte relativeURI não diferencia maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-127">Unlike the scheme, which must be lowercase, the relativeURI portion is case-insensitive.</span></span>

</dd> </dl>

<span data-ttu-id="b4cdd-128">Exemplos de UrlPrefixes formados corretamente são:</span><span class="sxs-lookup"><span data-stu-id="b4cdd-128">Examples of properly formed UrlPrefixes are:</span></span>

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a><span data-ttu-id="b4cdd-129">Categorias de Host-Specifier</span><span class="sxs-lookup"><span data-stu-id="b4cdd-129">Host-Specifier Categories</span></span>

<span data-ttu-id="b4cdd-130">Para flexibilidade e facilidade de uso, a API do servidor HTTP dá suporte a quatro maneiras diferentes de especificar hosts.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-130">For flexibility and ease of use, the HTTP Server API supports four different ways to specify hosts.</span></span> <span data-ttu-id="b4cdd-131">As quatro categorias de especificador de host são listadas abaixo em ordem de precedência:</span><span class="sxs-lookup"><span data-stu-id="b4cdd-131">The four host-specifier categories are listed below in order of precedence:</span></span>

<dl> <dt>

<span data-ttu-id="b4cdd-132"><span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Curinga forte (sinal de adição)</span><span class="sxs-lookup"><span data-stu-id="b4cdd-132"><span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Strong wildcard (Plus Sign)</span></span>
</dt> <dd>

<span data-ttu-id="b4cdd-133">Quando o elemento host de um UrlPrefix consiste em um único sinal de adição (+), o UrlPrefix corresponde a todos os nomes de host possíveis no contexto de seus elementos Scheme, Port e relativeURI e se enquadra na categoria curinga forte.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-133">When the host element of a UrlPrefix consists of a single plus sign (+), the UrlPrefix matches all possible host names in the context of its scheme, port and relativeURI elements, and falls into the strong wildcard category.</span></span>

<span data-ttu-id="b4cdd-134">Um curinga forte é útil quando um aplicativo precisa atender solicitações endereçadas a um ou mais relativeURIs, independentemente de como essas solicitações chegam no computador ou em qual site eles especificam em seus cabeçalhos de host.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-134">A strong wildcard is useful when an application needs to serve requests addressed to one or more relativeURIs, regardless of how those requests arrive on the machine or what site they specify in their Host headers.</span></span> <span data-ttu-id="b4cdd-135">O uso de um curinga forte nessa situação evita a necessidade de especificar uma lista completa de hosts e/ou endereços IP.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-135">Use of a strong wildcard in this situation avoids the need to specify an exhaustive list of host and/or IP-addresses.</span></span>

</dd> <dt>

<span data-ttu-id="b4cdd-136"><span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explicita</span><span class="sxs-lookup"><span data-stu-id="b4cdd-136"><span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explicit</span></span>
</dt> <dd>

<span data-ttu-id="b4cdd-137">Um nome de host explícito, como um nome de domínio totalmente qualificado no elemento de host, coloca um UrlPrefix na categoria explícita.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-137">An explicit host name such as a fully qualified domain name in the host element places a UrlPrefix in the explicit category.</span></span> <span data-ttu-id="b4cdd-138">Esse tipo de elemento de host é correspondido diretamente em relação aos cabeçalhos de host das solicitações de entrada.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-138">This kind of host element is matched directly against the Host headers of incoming requests.</span></span>

<span data-ttu-id="b4cdd-139">As especificações de host explícitas são úteis para aplicativos multissite, como servidores Web que fornecem conteúdo diferente, dependendo do site para o qual a solicitação foi direcionada.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-139">Explicit host specifications are useful for multi-site applications such as Web servers that deliver different content depending on the site to which the request was directed.</span></span>

</dd> <dt>

<span data-ttu-id="b4cdd-140"><span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>Curinga fraco com limite de IP</span><span class="sxs-lookup"><span data-stu-id="b4cdd-140"><span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>IP-bound weak wildcard</span></span>
</dt> <dd>

<span data-ttu-id="b4cdd-141">Quando um endereço IP é exibido como o elemento host, o UrlPrefix se enquadra na categoria curinga fraco com limite de IP.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-141">When an IP address appears as the host element, then the UrlPrefix falls into the IP-bound Weak Wildcard category.</span></span> <span data-ttu-id="b4cdd-142">Esse tipo de UrlPrefix corresponde a qualquer nome de host para a interface IP especificada com o esquema, a porta e a relativeURI especificados e que ainda não tenha sido correspondido por um UrlPrefix de caractere curinga forte ou explícito.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-142">This kind of UrlPrefix matches any host name for the specified IP interface with the specified scheme, port and relativeURI, and that has not already been matched by a strong-wildcard or explicit UrlPrefix.</span></span> <span data-ttu-id="b4cdd-143">O endereço IP usa uma das duas formas no elemento host:</span><span class="sxs-lookup"><span data-stu-id="b4cdd-143">The IP address takes one of two forms in the host element:</span></span>

<dl> <dt>

<span data-ttu-id="b4cdd-144"><span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>Cadeia de caracteres literal IPv4</span><span class="sxs-lookup"><span data-stu-id="b4cdd-144"><span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>IPv4 Literal String</span></span>
</dt> <dd>

<span data-ttu-id="b4cdd-145">Um literal IPv4 consiste em quatro números decimais pontilhados, cada um no intervalo de 0-255, como 192.168.0.0.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-145">An IPv4 literal consists of four dotted decimal numbers, each in the range 0-255, such as 192.168.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="b4cdd-146"><span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>Cadeia de caracteres literal do IPv6</span><span class="sxs-lookup"><span data-stu-id="b4cdd-146"><span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>IPv6 Literal String</span></span>
</dt> <dd>

<span data-ttu-id="b4cdd-147">Uma cadeia de caracteres literal do IPv6 é colocada entre colchetes e contém números hexadecimais separados por dois-pontos. por exemplo:: \[ : 1 \] ou \[ 3ffe: ffff:: 6ECB: 0101 \] .</span><span class="sxs-lookup"><span data-stu-id="b4cdd-147">An IPv6 literal string is enclosed in square brackets and contains hex numbers separated by colons; for example: \[::1\] or \[3ffe:ffff::6ECB:0101\].</span></span>

</dd> </dl>

<span data-ttu-id="b4cdd-148">Os especificadores de host fraco-curingas ligados por IP são destinados a aplicativos que variam de acordo com o conteúdo que eles atendem com base na rota tomada pelas solicitações de entrada.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-148">IP-bound weak-wildcard host specifiers are intended for applications that vary the content they serve based on the route taken by incoming requests.</span></span> <span data-ttu-id="b4cdd-149">Não confie em especificadores de host fraco-curinga com limite de IP para impor a segurança.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-149">Do not rely on IP-bound weak-wildcard host specifiers to enforce security.</span></span>

</dd> <dt>

<span data-ttu-id="b4cdd-150"><span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Caractere curinga fraco (asterisco)</span><span class="sxs-lookup"><span data-stu-id="b4cdd-150"><span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Weak wildcard (asterisk)</span></span>
</dt> <dd>

<span data-ttu-id="b4cdd-151">Quando um asterisco ( \* ) é exibido como o elemento host, o URLPrefix se enquadra na categoria curinga fraco.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-151">When an asterisk (\*) appears as the host element, then the UrlPrefix falls into the weak wildcard category.</span></span> <span data-ttu-id="b4cdd-152">Esse tipo de UrlPrefix corresponde a qualquer nome de host associado ao esquema especificado, à porta e ao relativeURI que ainda não tenha sido correspondido por um UrlPrefix de caractere curinga forte, explícito ou de IP fraco.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-152">This kind of UrlPrefix matches any host name associated with the specified scheme, port and relativeURI that has not already been matched by a strong-wildcard, explicit, or IP-bound weak-wildcard UrlPrefix.</span></span>

<span data-ttu-id="b4cdd-153">Essa especificação de host pode ser usada como um padrão catch-all em algumas circunstâncias, ou pode ser usada para especificar uma seção grande do namespace de URL sem a necessidade de usar muitos UrlPrefixes.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-153">This host specification can be used as a default catch-all in some circumstances, or can be used to specify a large section of URL namespace without having to use many UrlPrefixes.</span></span>

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a><span data-ttu-id="b4cdd-154">Detecção de conflitos de UrlPrefix durante a reserva e o registro</span><span class="sxs-lookup"><span data-stu-id="b4cdd-154">UrlPrefix Conflict Detection During Reservation and Registration</span></span>

<span data-ttu-id="b4cdd-155">Para fins de reserva e registro, as quatro categorias diferentes de UrlPrefix são tratadas separadamente, sem referência entre si.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-155">For reservation and registration purposes, the four different categories of UrlPrefix are treated separately, without reference to one another.</span></span> <span data-ttu-id="b4cdd-156">É possível registrar UrlPrefixes conflitantes, desde que estejam em categorias diferentes.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-156">It is possible to register conflicting UrlPrefixes as long as they are in different categories.</span></span> <span data-ttu-id="b4cdd-157">Somente dentro da mesma categoria, um conflito causa uma falha na tentativa de reserva.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-157">Only within the same category does a conflict cause a reservation attempt to fail.</span></span>

<span data-ttu-id="b4cdd-158">Por exemplo, seria possível reservar o UrlPrefix explícito `https://www.adatum.com:80/vroot/` e o URLPrefix curinga forte conflitante `https://+:80/vroot/` , pois eles pertencem a categorias diferentes.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-158">For example, it would be possible to reserve both the explicit UrlPrefix `https://www.adatum.com:80/vroot/` and the conflicting strong wildcard UrlPrefix `https://+:80/vroot/`, since they belong to different categories.</span></span> <span data-ttu-id="b4cdd-159">No entanto, uma tentativa subsequente de reservar https://+:80/vroot/ para um usuário diferente falhará, pois ele estaria em conflito com uma reserva existente em sua própria categoria.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-159">However, a subsequent attempt to reserve https://+:80/vroot/ to a different user would fail because it would conflict with an existing reservation in its own category.</span></span>

## <a name="routing-behavior"></a><span data-ttu-id="b4cdd-160">Comportamento de roteamento</span><span class="sxs-lookup"><span data-stu-id="b4cdd-160">Routing Behavior</span></span>

<span data-ttu-id="b4cdd-161">Ao rotear uma solicitação HTTP de entrada, a API do servidor HTTP começa com a categoria curinga forte e compara a URL de entrada com o UrlPrefixes registrado e reservado nessa categoria.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-161">When routing an incoming HTTP request, the HTTP Server API starts with the strong wildcard category and compares the incoming URL with both registered and reserved UrlPrefixes in that category.</span></span>

<span data-ttu-id="b4cdd-162">Se a URL de entrada corresponder a uma reserva, mas não a um registro, a API do servidor HTTP falhará na solicitação.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-162">If the incoming URL matches a reservation but not a registration, the HTTP Server API fails the request.</span></span> <span data-ttu-id="b4cdd-163">Isso impede que os registros de baixa prioridade sejam capazes de pegar solicitações não pretendidas para ele.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-163">This prevents a lower-priority registrations from being able to pick up requests not intended for it.</span></span> <span data-ttu-id="b4cdd-164">O status em falha é 400 ("solicitação inválida") em vez de 503 ("serviço não disponível"), pois um retorno de 503 é, às vezes, interpretado erroneamente por gateways de balanceamento de carga, indicando que o servidor estava sobrecarregado.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-164">The status on failure is 400 ("Bad Request") rather than 503 ("Service not available"), because a 503 return is sometimes mistakenly interpreted by load-balancing gateways as indicating that the server was overloaded.</span></span>

<span data-ttu-id="b4cdd-165">Se um registro correspondente for encontrado dentro da categoria, a solicitação será roteada para a fila de solicitações associada a esse registro.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-165">If a matching registration is found within the category, the request is routed to the request queue associated with that registration.</span></span> <span data-ttu-id="b4cdd-166">A solicitação é sempre roteada para a fila associada ao UrlPrefix correspondente mais longo dentro de uma categoria.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-166">The request is always routed to the queue associated with the longest matching UrlPrefix within a category.</span></span>

<span data-ttu-id="b4cdd-167">Se nenhuma correspondência for encontrada na categoria, a API do servidor HTTP prosseguirá para a categoria explícita e repetirá o mesmo procedimento.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-167">If no match is found in the category, then the HTTP Server API proceeds to the explicit category and repeats the same procedure.</span></span> <span data-ttu-id="b4cdd-168">Para resumir, a ordem na qual as categorias são examinadas é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="b4cdd-168">To summarize, the order in which the categories are examined is as follows:</span></span>

1.  <span data-ttu-id="b4cdd-169">Curinga forte</span><span class="sxs-lookup"><span data-stu-id="b4cdd-169">Strong wildcard</span></span>
2.  <span data-ttu-id="b4cdd-170">Explícita</span><span class="sxs-lookup"><span data-stu-id="b4cdd-170">Explicit</span></span>
3.  <span data-ttu-id="b4cdd-171">IP-Bound curinga fraco</span><span class="sxs-lookup"><span data-stu-id="b4cdd-171">IP-Bound weak wildcard</span></span>
4.  <span data-ttu-id="b4cdd-172">Curinga fraco</span><span class="sxs-lookup"><span data-stu-id="b4cdd-172">Weak wildcard</span></span>

<span data-ttu-id="b4cdd-173">Se nenhuma correspondência for encontrada em nenhuma das categorias, a API do servidor HTTP enviará uma resposta com um código de status de 400 para indicar que a solicitação não pode ser roteada.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-173">If no match is found in any of the categories, the HTTP Server API sends a response with a status code of 400 to indicate that the request cannot be routed.</span></span>

## <a name="longest-match-rule"></a><span data-ttu-id="b4cdd-174">Regra de correspondência mais longa</span><span class="sxs-lookup"><span data-stu-id="b4cdd-174">Longest Match Rule</span></span>

<span data-ttu-id="b4cdd-175">Em cada categoria UrlPrefix, a API do servidor HTTP roteia uma solicitação para a fila associada ao UrlPrefix correspondente mais longo.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-175">Within each UrlPrefix category, HTTP Server API routes a request to the queue associated with the longest matching UrlPrefix.</span></span> <span data-ttu-id="b4cdd-176">Por exemplo, suponha que os dois UrlPrefixes a seguir sejam registrados em filas diferentes:</span><span class="sxs-lookup"><span data-stu-id="b4cdd-176">For example, suppose the following two UrlPrefixes are registered to different queues:</span></span>

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

<span data-ttu-id="b4cdd-177">A API do servidor HTTP roteia uma solicitação de `https://www.adatum.com:80/default.htm` para Queue1 e uma solicitação de `https://www.adatum.com:80/dir/sna/snadefault.htm` para o Queue2.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-177">The HTTP Server API routes a request for `https://www.adatum.com:80/default.htm` to Queue1, and a request for `https://www.adatum.com:80/dir/sna/snadefault.htm` to Queue2.</span></span> <span data-ttu-id="b4cdd-178">Ele roteia uma solicitação de `https://www.adatum.com:80/dir/app.htm` para Queue1 porque a correspondência completa mais longa é com o `https://www.adatum.com:80/` URLPrefix, não com o `https://www.adatum.com:80/dir/sna` URLPrefix.</span><span class="sxs-lookup"><span data-stu-id="b4cdd-178">It routes a request for `https://www.adatum.com:80/dir/app.htm` to Queue1 because the longest complete match is with the `https://www.adatum.com:80/` UrlPrefix, not with the `https://www.adatum.com:80/dir/sna` UrlPrefix.</span></span>

 

 




