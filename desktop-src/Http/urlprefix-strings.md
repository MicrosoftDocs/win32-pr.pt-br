---
title: Cadeias de caracteres de UrlPrefix
description: Na API do Servidor HTTP, um UrlPrefix é uma cadeia de caracteres Unicode de caractere largo (UTF-16) com um formulário canônico que especifica uma seção do namespace de URL.
ms.assetid: 4f317bf6-ee6a-47a8-a531-78534217109d
keywords:
- UrlPrefix strings HTTP Server API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3fad89bf7abd52ee3681beaa8069a7f5e4ee25b482cd065f880263852690fce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047036"
---
# <a name="urlprefix-strings"></a>Cadeias de caracteres de UrlPrefix

Na API do Servidor HTTP, um *UrlPrefix* é uma cadeia de caracteres Unicode de caractere largo (UTF-16) com um formulário canônico que especifica uma seção do namespace de URL. Ele é usado para reservar uma seção do namespace de URL para uma conta de usuário ou registrar uma seção do namespace de URL para um processo.

## <a name="urlprefix-format"></a>Formato UrlPrefix

Um UrlPrefix tem a seguinte sintaxe:

"scheme://host:port/relativeURI"

Os elementos de esquema, host e porta de um UrlPrefix devem estar presentes e não vazios e devem obedecer às seguintes regras:

<dl> <dt>

<span id="scheme"></span><span id="SCHEME"></span>Esquema
</dt> <dd>

Deve ser http ou https, tudo em minúsculas.

</dd> <dt>

<span id="host"></span><span id="HOST"></span>Host
</dt> <dd>

Deve ser um nome de domínio totalmente qualificado, uma cadeia de caracteres literal IPv4 ou IPv6 ou um curinga. Ao contrário do esquema, que deve estar em minúsculas, a parte do host não faz diferença entre maiúsculas e minúsculas. Dependendo de como sua parte do host é especificada, um UrlPrefix se enquadra em uma das quatro categorias de roteamento a seguir, que são descritas mais detalhadamente abaixo:

<dl> <dd>Curinga forte</dd> <dd>Explícita</dd> <dd>Curinga fraco com limite de IP</dd> <dd>Curinga fraco</dd> </dl> </dd> <dt>

<span id="port"></span><span id="PORT"></span>Porta
</dt> <dd>

Uma cadeia de caracteres numérica decimal que não começa com zero e que representa um número de porta TCP válido (1 a 65.535). Esse valor não pode ser um curinga.

</dd> <dt>

<span id="relativeURI"></span><span id="relativeuri"></span><span id="RELATIVEURI"></span>Relativeuri
</dt> <dd>

O elemento relativeURI é opcional, mas se presente sempre deve ser seguido por um caractere de barra ("/"). Essa é uma cadeia de caracteres de prefixo que indica uma subárvore dentro do namespace do computador especificado em relação aos valores de esquema, host e porta. Ao contrário do esquema, que deve estar em minúsculas, a parte de relativeURI não faz diferença entre maiúsculas e minúsculas.

</dd> </dl>

Exemplos de UrlPrefixes corretamente formados são:

-   `https://www.adatum.com:80/vroot/`
-   `https://adatum.com:443/secure/database/`
-   `https://+:80/vroot/`

## <a name="host-specifier-categories"></a>Host-Specifier categorias

Para flexibilidade e facilidade de uso, a API do servidor HTTP dá suporte a quatro maneiras diferentes de especificar hosts. As quatro categorias de especificador de host são listadas abaixo em ordem de precedência:

<dl> <dt>

<span id="Strong_wildcard__Plus_Sign_"></span><span id="strong_wildcard__plus_sign_"></span><span id="STRONG_WILDCARD__PLUS_SIGN_"></span>Curinga forte (sinal de a mais)
</dt> <dd>

Quando o elemento host de um UrlPrefix consiste em um único sinal de mais (+), o UrlPrefix corresponde a todos os nomes de host possíveis no contexto de seus elementos de esquema, porta e relativeURI e se enquadra na categoria curinga forte.

Um curinga forte é útil quando um aplicativo precisa atender a solicitações endereçadas a um ou mais relativeURIs, independentemente de como essas solicitações chegam no computador ou de qual site eles especificam em seus headers de Host. O uso de um curinga forte nessa situação evita a necessidade de especificar uma lista completa de endereços IP e/ou host.

</dd> <dt>

<span id="Explicit"></span><span id="explicit"></span><span id="EXPLICIT"></span>Explícita
</dt> <dd>

Um nome de host explícito, como um nome de domínio totalmente qualificado no elemento host, coloca um UrlPrefix na categoria explícita. Esse tipo de elemento de host é corresponder diretamente com os headers host de solicitações de entrada.

Especificações explícitas de host são úteis para aplicativos de vários sites, como servidores Web que entregam conteúdo diferente, dependendo do site para o qual a solicitação foi direcionada.

</dd> <dt>

<span id="IP-bound_weak_wildcard"></span><span id="ip-bound_weak_wildcard"></span><span id="IP-BOUND_WEAK_WILDCARD"></span>Curinga fraco com limite de IP
</dt> <dd>

Quando um endereço IP aparece como o elemento host, o UrlPrefix se enquadra na categoria Curinga Fraca vinculada a IP. Esse tipo de UrlPrefix corresponde a qualquer nome de host para a interface IP especificada com o esquema, a porta e o relativeURI especificados e que ainda não foi corresponder a um urlPrefix forte ou explícito. O endereço IP assume uma das duas formas no elemento host:

<dl> <dt>

<span id="IPv4_Literal_String"></span><span id="ipv4_literal_string"></span><span id="IPV4_LITERAL_STRING"></span>Cadeia de caracteres literal IPv4
</dt> <dd>

Um literal IPv4 consiste em quatro números decimais pontilhados, cada um no intervalo de 0 a 255, como 192.168.0.0.

</dd> <dt>

<span id="IPv6_Literal_String"></span><span id="ipv6_literal_string"></span><span id="IPV6_LITERAL_STRING"></span>Cadeia de caracteres literal IPv6
</dt> <dd>

Uma cadeia de caracteres literal IPv6 é entre colchetes e contém números hexatórios separados por dois-pontos; por exemplo: \[ ::1 \] ou \[ 3ffe:ffff::6ECB:0101 \] .

</dd> </dl>

Especificadores de host de curinga fraco com limite de IP destinam-se a aplicativos que variam o conteúdo que eles servem com base na rota tomada por solicitações de entrada. Não confie em especificadores de host de curinga fraco com limite de IP para impor a segurança.

</dd> <dt>

<span id="Weak_wildcard__asterisk_"></span><span id="weak_wildcard__asterisk_"></span><span id="WEAK_WILDCARD__ASTERISK_"></span>Curinga fraco (asterisco)
</dt> <dd>

Quando um asterisco ( ) aparece como o \* elemento host, o UrlPrefix se enquadra na categoria curinga fraca. Esse tipo de UrlPrefix corresponde a qualquer nome de host associado ao esquema, à porta e ao relativeURI especificados que ainda não foram correspondedos por um UrlPrefix de curinga forte, explícita ou associada a IP.

Essa especificação de host pode ser usada como um catch-all padrão em algumas circunstâncias ou pode ser usada para especificar uma grande seção do namespace de URL sem precisar usar muitos UrlPrefixes.

</dd> </dl>

## <a name="urlprefix-conflict-detection-during-reservation-and-registration"></a>Detecção de conflitos UrlPrefix durante a reserva e o registro

Para fins de reserva e registro, as quatro categorias diferentes de UrlPrefix são tratadas separadamente, sem referência uma à outra. É possível registrar UrlPrefixes conflitantes, desde que eles sejam em categorias diferentes. Somente dentro da mesma categoria um conflito causa falha em uma tentativa de reserva.

Por exemplo, seria possível reservar o UrlPrefix explícito e o url curinga forte conflitante UrlPrefix, pois eles pertencem `https://www.adatum.com:80/vroot/` `https://+:80/vroot/` a categorias diferentes. No entanto, uma tentativa subsequente de reservar para um usuário diferente falharia porque entraria em conflito com uma reserva https://+:80/vroot/ existente em sua própria categoria.

## <a name="routing-behavior"></a>Comportamento de roteamento

Ao rotear uma solicitação HTTP de entrada, a API do Servidor HTTP começa com a categoria curinga forte e compara a URL de entrada com UrlPrefixes registradas e reservadas nessa categoria.

Se a URL de entrada corresponde a uma reserva, mas não a um registro, a API do servidor HTTP falha na solicitação. Isso impede que um registro de prioridade mais baixa seja capaz de pegar solicitações não destinadas a ele. O status de falha é 400 ("Solicitação Ruim") em vez de 503 ("Serviço não disponível"), porque um retorno 503 às vezes é interpretado erroneamente por gateways de balanceamento de carga como indicando que o servidor estava sobrecarregado.

Se um registro correspondente for encontrado dentro da categoria, a solicitação será roteada para a fila de solicitação associada a esse registro. A solicitação sempre é roteada para a fila associada ao UrlPrefix correspondente mais longo dentro de uma categoria.

Se nenhuma corresponder for encontrada na categoria, a API do Servidor HTTP prosseguirá para a categoria explícita e repetirá o mesmo procedimento. Para resumir, a ordem na qual as categorias são examinadas é a seguinte:

1.  Curinga forte
2.  Explícita
3.  IP-Bound curinga fraco
4.  Curinga fraco

Se nenhuma corresponder for encontrada em qualquer uma das categorias, a API do Servidor HTTP enviará uma resposta com um código de status 400 para indicar que a solicitação não pode ser roteada.

## <a name="longest-match-rule"></a>Regra de combinação mais longa

Dentro de cada categoria UrlPrefix, a API do Servidor HTTP encaminha uma solicitação para a fila associada ao UrlPrefix correspondente mais longo. Por exemplo, suponha que os dois UrlPrefixes a seguir sejam registrados em filas diferentes:

- `Queue1 https://www.adatum.com:80/`
- `Queue2 https://www.adatum.com:80/dir/sna/`

A API do Servidor HTTP encaminha uma solicitação `https://www.adatum.com:80/default.htm` para a Queue1 e uma solicitação `https://www.adatum.com:80/dir/sna/snadefault.htm` para a Queue2. Ele encaminha uma solicitação para a Queue1 porque a maior combinação completa é com `https://www.adatum.com:80/dir/app.htm` `https://www.adatum.com:80/` o UrlPrefix, não com `https://www.adatum.com:80/dir/sna` o UrlPrefix.

 

 




