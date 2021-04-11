---
description: Todas as configurações de IPv6 são feitas com a ferramenta de Ipv6.exe.
ms.assetid: cb701070-cb7f-472a-97c7-1de9c0ddec0f
title: Ipv6.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91e6fb0266609d22116cc72151e0db26006c415a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164467"
---
# <a name="ipv6exe"></a>Ipv6.exe

Todas as configurações de IPv6 são feitas com a ferramenta de Ipv6.exe. Essa ferramenta é usada principalmente para consultar e configurar interfaces IPv6, endereços, caches e rotas. Estes são os subcomandos IPv6:

<dl> <dt>

<span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**IPv6 se** \[ que\#\]
</dt> <dd>

Exibe informações sobre interfaces. Se um número de interface for especificado, somente as informações sobre essa interface serão exibidas. Caso contrário, as informações sobre todas as interfaces serão exibidas. A saída inclui o endereço de camada de vínculo da interface e a lista de endereços IPv6 atribuídos à interface, incluindo a MTU atual da interface e o MTU máximo (verdadeiro) ao qual a interface pode dar suporte.

\#A interface 1 é uma pseudo-interface usada para loopback. \#A interface 2 é uma pseudo interface usada para túnel configurado, túnel automático e túnel 6to4. Outras interfaces são numeradas em sequência na ordem em que são criadas. Essa ordem varia de um computador para outro.

Os endereços de camada de link no formato *AA*/ -  - *CC* - *DD* - *EE* aaaa -  são endereços Ethernet. Endereço de camada de link em *um*. *b*. *c*. o formulário *d* são interfaces 6-over-4. Para obter mais informações sobre 6-over-4, consulte RFC 2529.

As duas pseudo interfaces não usam a descoberta de vizinho IPv6.

</dd> <dt>

<span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**IPv6 IFC** se os \# \[ encaminhar \] \[ anuncia \] \[ -encaminhamentos \] \[ -anuncias \] \[ MTU \# bytes \] \[ site-identificador\]
</dt> <dd>

Controla os atributos da interface. As interfaces podem ser encaminhadas, caso em que encaminhar pacotes com endereços de destino não atribuídos à interface. As interfaces podem ser anunciadas; nesse caso, elas enviam anúncios de roteador. Esses atributos podem ser controlados de forma independente. Uma interface envia solicitações de roteador e recebe anúncios de roteador ou recebe solicitações de roteador e envia anúncios de roteador.

Como as duas pseudo interfaces não usam a descoberta de vizinho, elas não podem ser configuradas para enviar anúncios de roteador.

Os encaminhamentos podem ser abreviados como forw e anunciados como avçd.

O MTU para a interface também pode ser definido. A nova MTU deve ser menor ou igual à MTU máxima (true) do link (conforme relatado pelo IPv6 se) e maior ou igual à MTU IPv6 mínima (1280 bytes).

O identificador de site para uma interface também pode ser alterado. Os identificadores de site são usados no \_ campo ID de escopo sin6 \_ com endereços de site local.

</dd> <dt>

<span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**IFD IPv6** se\#
</dt> <dd>

Exclui uma interface. As pseudo-interfaces de loopback e de túnel não podem ser excluídas.

</dd> <dt>

<span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**NC IPv6** \[ Se o \# \[ Endereço\]\]
</dt> <dd>

Exibe o conteúdo do cache vizinho. Se um número de interface for especificado, somente o conteúdo do cache vizinho dessa interface será exibido. Caso contrário, o conteúdo de todos os caches vizinhos da interface será exibido. Se uma interface for especificada, um endereço IPv6 poderá ser especificado para exibir somente essa entrada de cache vizinho.

Para cada entrada de cache vizinho, a interface, o endereço IPv6, o endereço de camada de link e o estado de alcance são exibidos.

</dd> <dt>

<span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**NCF IPv6** \[ Se o \# \[ Endereço\]\]
</dt> <dd>

Libera as entradas de cache vizinho especificadas. Somente entradas de cache vizinho sem referências são limpas. Como as entradas do cache de rota mantêm referências a entradas de cache vizinho, o cache de rota deve ser liberado primeiro. As entradas da tabela de roteamento também podem manter referências a entradas de cache vizinho.

</dd> <dt>

<span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**IPv6 RC** \[ Se o \# Endereço\]
</dt> <dd>

Exibe o conteúdo do cache de rota. O cache de rota é o nome de implementação do IPv6 da Microsoft para o cache de destino. Se uma interface e um endereço forem especificados, a entrada de cache de rota para atingir o endereço por meio da interface será exibida. Caso contrário, todas as entradas de cache de rota serão exibidas.

Para cada entrada de cache de rota, o endereço IPv6 e a interface de próximo salto atual e o endereço vizinho são exibidos. O endereço de origem preferencial para uso com esse destino, a MTU do caminho atual para atingir esse destino por meio da interface e a determinação de se esta é uma interface específica – a entrada do cache de rota também é exibida. Qualquer endereço de atendimento (para mobilidade) para o endereço de destino também é exibido.

Um endereço de destino pode ter várias entradas de cache de rota — tanto quanto uma para cada interface de saída. No entanto, um endereço de destino pode ter no máximo uma entrada de cache de rota que não seja específica da interface. Uma interface específica – a entrada de cache de rota só será usada se o aplicativo especificar explicitamente a interface de saída.

</dd> <dt>

<span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**RCF IPv6** \[ Se o \# \[ Endereço\]\]
</dt> <dd>

Libera as entradas de cache de rota especificadas.

</dd> <dt>

<span id="ipv6_bc"></span><span id="IPV6_BC"></span>**BC IPv6**
</dt> <dd>

Exibe o conteúdo do cache de associação, que contém associações entre endereços residenciais e endereços de cuidado para IPv6 móvel.

Para cada associação, é exibido o endereço principal, o endereço de atendimento, o número de sequência de associação e o tempo de vida.

</dd> <dt>

<span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**Adu IPv6** If \# /Address \[ Lifetime VL \[ /pl \] \] \[ anycast \] \[ unicast\]
</dt> <dd>

Adiciona ou remove uma atribuição de endereço unicast ou anycast em uma interface. O endereço unicast é acionado a menos que anycast seja especificado.

O tempo de vida é infinito se não especificado. Se apenas um tempo de vida válido for especificado, o tempo de vida preferencial será igual ao tempo de vida válido. Um tempo de vida infinito pode ser especificado ou um valor finito em segundos. O tempo de vida preferencial deve ser menor ou igual ao tempo de vida válido. A especificação de um tempo de vida igual a zero faz com que o endereço seja removido.

Você pode abreviar o tempo de vida como vida útil.

Para endereços anycast, os únicos valores de tempo de vida válidos são zero e infinito.

</dd> <dt>

<span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**SPT IPv6**
</dt> <dd>

Exibe o conteúdo atual da tabela de prefixo do site.

Para cada prefixo de site, o comando exibe o prefixo, a interface à qual o prefixo do site se aplica e o tempo de vida do prefixo em segundos.

Os prefixos de site normalmente são configurados automaticamente a partir de anúncios de roteador. Eles são usados na função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) para filtrar endereços locais inadequados do site.

</dd> <dt>

<span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>prefixo de **SPU IPv6** se \# \[ tempo de vida L\]
</dt> <dd>

Adiciona, remove ou atualiza um prefixo na tabela de prefixo do site.

O prefixo e o número da interface são necessários. O tempo de vida do prefixo do site, especificado em segundos, padrão será infinito se não for especificado. Especificar um tempo de vida igual a zero exclui o prefixo do site.

Esse comando é desnecessário para a configuração normal de hosts ou roteadores.

</dd> <dt>

<span id="ipv6_rt"></span><span id="IPV6_RT"></span>**IPv6 RT**
</dt> <dd>

Exibe o conteúdo atual da tabela de roteamento.

Para cada entrada de tabela de roteamento, o comando exibe o prefixo de rota, uma interface em link ou um vizinho de próximo salto em uma interface, um valor de preferência (menor é preferencial) e um tempo de vida em segundos.

As entradas da tabela de roteamento também podem ter atributos de **publicação** e de **expiração** . Por padrão, elas envelhecem (a vida útil conta, em vez da constante restante) e não são publicadas (não são usadas na construção de anúncios de roteador).

Em hosts, as entradas da tabela de roteamento normalmente são configuradas automaticamente de anúncios de roteador.

</dd> <dt>

<span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>prefixo **RTU IPv6** se \# \[ /nexthop \] \[ tempo de vida L \] \[ preferência P \] \[ publicar \] \[ idade \] \[ SPL site-prefixo-comprimento\]
</dt> <dd>

Adiciona ou remove uma rota na tabela de roteamento. O prefixo de rota é necessário. O prefixo pode estar no link para uma interface especificada ou próximo salto, especificado com um endereço vizinho em uma interface. A rota pode ter um tempo de vida em segundos, com o infinito padrão e uma preferência, com o padrão de zero ou o mais preferencial. Especificar um tempo de vida igual a zero exclui a rota.

Se a rota for especificada como publicada, indicando que ela será usada na construção de anúncios de roteador, ela não age. O tempo de vida da rota não é contabilizado e, portanto, é efetivamente infinito, mas o valor é usado em anúncios de roteador. Opcionalmente, uma rota pode ser especificada como uma rota publicada que também expira. Por padrão, uma rota não publicada sempre é expirada.

A subopção SPL opcional pode ser usada para especificar um comprimento de prefixo de site associado à rota. O comprimento do prefixo do site é usado somente ao enviar anúncios de roteador.

O tempo de vida pode ser abreviado como vida, preferência como pref e publicar como pub.

</dd> </dl>

 

 



