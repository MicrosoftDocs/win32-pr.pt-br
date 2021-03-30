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
# <a name="urlprefix-strings"></a>Cadeias de caracteres de UrlPrefix

Na API do servidor HTTP, um *URLPrefix* é uma cadeia de caracteres Unicode de caractere largo (UTF-16) com um formato canônico que especifica uma seção do namespace da URL. Ele é usado para reservar uma seção do namespace de URL para uma conta de usuário ou registrar uma seção do namespace de URL para um processo.

## <a name="urlprefix-format"></a>Formato UrlPrefix

Um UrlPrefix tem a seguinte sintaxe:

"Scheme://host: Port/relativeURI"

O esquema, o host e os elementos de porta de um UrlPrefix devem estar presentes e não vazios e devem obedecer às seguintes regras:

<dl> <dt>

<span id="scheme"></span><span id="SCHEME"></span>esquema
</dt> <dd>

Deve ser http ou HTTPS, em minúsculas.

</dd> <dt>

<span id="host"></span><span id="HOST"></span>hospedeira
</dt> <dd>

Deve ser um nome de domínio totalmente qualificado, uma cadeia de caracteres literal IPv4 ou IPv6 ou um curinga. Ao contrário do esquema, que deve estar em letras minúsculas, a parte do host não diferencia maiúsculas de minúsculas. Dependendo de como sua parte de host é especificada, um UrlPrefix se enquadra em uma das quatro categorias de roteamento a seguir, que são descritas em mais detalhes abaixo:

<dl> <dd>Curinga forte</dd> <dd>Explícita</dd> <dd>Curinga fraco com limite de IP</dd> <dd>Curinga fraco</dd> </dl> </dd> <dt>

<span id="port"></span><span id="PORT"></span>Porto
</dt> <dd>

Uma cadeia de caracteres numérica decimal que não começa com zero e que representa um número de porta TCP válido (de 1 a 65.535). Esse valor não pode ser um caractere curinga.

</dd> <dt>

<span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>relativeURI
</dt> <dd>

O elemento relativeURI é opcional, mas, se presente, deve ser sempre seguido por um caractere de barra ("/"). Essa é uma cadeia de caracteres de prefixo que indica uma subárvore dentro do namespace da máquina especificado em relação ao esquema, ao host e aos valores de porta. Ao contrário do esquema, que deve estar em letras minúsculas, a parte relativeURI não diferencia maiúsculas de minúsculas.

</dd> </dl>

Exemplos de UrlPrefixes formados corretamente são:

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a>Categorias de Host-Specifier

Para flexibilidade e facilidade de uso, a API do servidor HTTP dá suporte a quatro maneiras diferentes de especificar hosts. As quatro categorias de especificador de host são listadas abaixo em ordem de precedência:

<dl> <dt>

<span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Curinga forte (sinal de adição)
</dt> <dd>

Quando o elemento host de um UrlPrefix consiste em um único sinal de adição (+), o UrlPrefix corresponde a todos os nomes de host possíveis no contexto de seus elementos Scheme, Port e relativeURI e se enquadra na categoria curinga forte.

Um curinga forte é útil quando um aplicativo precisa atender solicitações endereçadas a um ou mais relativeURIs, independentemente de como essas solicitações chegam no computador ou em qual site eles especificam em seus cabeçalhos de host. O uso de um curinga forte nessa situação evita a necessidade de especificar uma lista completa de hosts e/ou endereços IP.

</dd> <dt>

<span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explicita
</dt> <dd>

Um nome de host explícito, como um nome de domínio totalmente qualificado no elemento de host, coloca um UrlPrefix na categoria explícita. Esse tipo de elemento de host é correspondido diretamente em relação aos cabeçalhos de host das solicitações de entrada.

As especificações de host explícitas são úteis para aplicativos multissite, como servidores Web que fornecem conteúdo diferente, dependendo do site para o qual a solicitação foi direcionada.

</dd> <dt>

<span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>Curinga fraco com limite de IP
</dt> <dd>

Quando um endereço IP é exibido como o elemento host, o UrlPrefix se enquadra na categoria curinga fraco com limite de IP. Esse tipo de UrlPrefix corresponde a qualquer nome de host para a interface IP especificada com o esquema, a porta e a relativeURI especificados e que ainda não tenha sido correspondido por um UrlPrefix de caractere curinga forte ou explícito. O endereço IP usa uma das duas formas no elemento host:

<dl> <dt>

<span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>Cadeia de caracteres literal IPv4
</dt> <dd>

Um literal IPv4 consiste em quatro números decimais pontilhados, cada um no intervalo de 0-255, como 192.168.0.0.

</dd> <dt>

<span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>Cadeia de caracteres literal do IPv6
</dt> <dd>

Uma cadeia de caracteres literal do IPv6 é colocada entre colchetes e contém números hexadecimais separados por dois-pontos. por exemplo:: \[ : 1 \] ou \[ 3ffe: ffff:: 6ECB: 0101 \] .

</dd> </dl>

Os especificadores de host fraco-curingas ligados por IP são destinados a aplicativos que variam de acordo com o conteúdo que eles atendem com base na rota tomada pelas solicitações de entrada. Não confie em especificadores de host fraco-curinga com limite de IP para impor a segurança.

</dd> <dt>

<span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Caractere curinga fraco (asterisco)
</dt> <dd>

Quando um asterisco ( \* ) é exibido como o elemento host, o URLPrefix se enquadra na categoria curinga fraco. Esse tipo de UrlPrefix corresponde a qualquer nome de host associado ao esquema especificado, à porta e ao relativeURI que ainda não tenha sido correspondido por um UrlPrefix de caractere curinga forte, explícito ou de IP fraco.

Essa especificação de host pode ser usada como um padrão catch-all em algumas circunstâncias, ou pode ser usada para especificar uma seção grande do namespace de URL sem a necessidade de usar muitos UrlPrefixes.

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a>Detecção de conflitos de UrlPrefix durante a reserva e o registro

Para fins de reserva e registro, as quatro categorias diferentes de UrlPrefix são tratadas separadamente, sem referência entre si. É possível registrar UrlPrefixes conflitantes, desde que estejam em categorias diferentes. Somente dentro da mesma categoria, um conflito causa uma falha na tentativa de reserva.

Por exemplo, seria possível reservar o UrlPrefix explícito `https://www.adatum.com:80/vroot/` e o URLPrefix curinga forte conflitante `https://+:80/vroot/` , pois eles pertencem a categorias diferentes. No entanto, uma tentativa subsequente de reservar https://+:80/vroot/ para um usuário diferente falhará, pois ele estaria em conflito com uma reserva existente em sua própria categoria.

## <a name="routing-behavior"></a>Comportamento de roteamento

Ao rotear uma solicitação HTTP de entrada, a API do servidor HTTP começa com a categoria curinga forte e compara a URL de entrada com o UrlPrefixes registrado e reservado nessa categoria.

Se a URL de entrada corresponder a uma reserva, mas não a um registro, a API do servidor HTTP falhará na solicitação. Isso impede que os registros de baixa prioridade sejam capazes de pegar solicitações não pretendidas para ele. O status em falha é 400 ("solicitação inválida") em vez de 503 ("serviço não disponível"), pois um retorno de 503 é, às vezes, interpretado erroneamente por gateways de balanceamento de carga, indicando que o servidor estava sobrecarregado.

Se um registro correspondente for encontrado dentro da categoria, a solicitação será roteada para a fila de solicitações associada a esse registro. A solicitação é sempre roteada para a fila associada ao UrlPrefix correspondente mais longo dentro de uma categoria.

Se nenhuma correspondência for encontrada na categoria, a API do servidor HTTP prosseguirá para a categoria explícita e repetirá o mesmo procedimento. Para resumir, a ordem na qual as categorias são examinadas é a seguinte:

1.  Curinga forte
2.  Explícita
3.  IP-Bound curinga fraco
4.  Curinga fraco

Se nenhuma correspondência for encontrada em nenhuma das categorias, a API do servidor HTTP enviará uma resposta com um código de status de 400 para indicar que a solicitação não pode ser roteada.

## <a name="longest-match-rule"></a>Regra de correspondência mais longa

Em cada categoria UrlPrefix, a API do servidor HTTP roteia uma solicitação para a fila associada ao UrlPrefix correspondente mais longo. Por exemplo, suponha que os dois UrlPrefixes a seguir sejam registrados em filas diferentes:

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

A API do servidor HTTP roteia uma solicitação de `https://www.adatum.com:80/default.htm` para Queue1 e uma solicitação de `https://www.adatum.com:80/dir/sna/snadefault.htm` para o Queue2. Ele roteia uma solicitação de `https://www.adatum.com:80/dir/app.htm` para Queue1 porque a correspondência completa mais longa é com o `https://www.adatum.com:80/` URLPrefix, não com o `https://www.adatum.com:80/dir/sna` URLPrefix.

 

 




