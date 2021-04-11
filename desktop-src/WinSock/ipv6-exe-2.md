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
# <a name="ipv6exe"></a><span data-ttu-id="668bc-103">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="668bc-103">Ipv6.exe</span></span>

<span data-ttu-id="668bc-104">Todas as configurações de IPv6 são feitas com a ferramenta de Ipv6.exe.</span><span class="sxs-lookup"><span data-stu-id="668bc-104">All IPv6 configuration is done with the Ipv6.exe tool.</span></span> <span data-ttu-id="668bc-105">Essa ferramenta é usada principalmente para consultar e configurar interfaces IPv6, endereços, caches e rotas.</span><span class="sxs-lookup"><span data-stu-id="668bc-105">This tool is primarily used for the querying and configuring of IPv6 interfaces, addresses, caches, and routes.</span></span> <span data-ttu-id="668bc-106">Estes são os subcomandos IPv6:</span><span class="sxs-lookup"><span data-stu-id="668bc-106">The following are IPv6 subcommands:</span></span>

<dl> <dt>

<span data-ttu-id="668bc-107"><span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**IPv6 se** \[ que\#\]</span><span class="sxs-lookup"><span data-stu-id="668bc-107"><span id="ipv6_if__if__"></span><span id="IPV6_IF__IF__"></span>**ipv6 if** \[if\#\]</span></span>
</dt> <dd>

<span data-ttu-id="668bc-108">Exibe informações sobre interfaces.</span><span class="sxs-lookup"><span data-stu-id="668bc-108">Displays information about interfaces.</span></span> <span data-ttu-id="668bc-109">Se um número de interface for especificado, somente as informações sobre essa interface serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="668bc-109">If an interface number is specified, only information about that interface is displayed.</span></span> <span data-ttu-id="668bc-110">Caso contrário, as informações sobre todas as interfaces serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="668bc-110">Otherwise, information about all interfaces is displayed.</span></span> <span data-ttu-id="668bc-111">A saída inclui o endereço de camada de vínculo da interface e a lista de endereços IPv6 atribuídos à interface, incluindo a MTU atual da interface e o MTU máximo (verdadeiro) ao qual a interface pode dar suporte.</span><span class="sxs-lookup"><span data-stu-id="668bc-111">The output includes the interface's link-layer address and the list of IPv6 addresses assigned to the interface, including the interface's current MTU and the maximum (true) MTU that the interface can support.</span></span>

<span data-ttu-id="668bc-112">\#A interface 1 é uma pseudo-interface usada para loopback.</span><span class="sxs-lookup"><span data-stu-id="668bc-112">Interface \#1 is a pseudo-interface used for loopback.</span></span> <span data-ttu-id="668bc-113">\#A interface 2 é uma pseudo interface usada para túnel configurado, túnel automático e túnel 6to4.</span><span class="sxs-lookup"><span data-stu-id="668bc-113">Interface \#2 is a pseudo-interface used for configured tunneling, automatic tunneling, and 6to4 tunneling.</span></span> <span data-ttu-id="668bc-114">Outras interfaces são numeradas em sequência na ordem em que são criadas.</span><span class="sxs-lookup"><span data-stu-id="668bc-114">Other interfaces are numbered sequentially in the order in which they are created.</span></span> <span data-ttu-id="668bc-115">Essa ordem varia de um computador para outro.</span><span class="sxs-lookup"><span data-stu-id="668bc-115">This order varies from one computer to another.</span></span>

<span data-ttu-id="668bc-116">Os endereços de camada de link no formato *AA*/ -  - *CC* - *DD* - *EE* aaaa -  são endereços Ethernet.</span><span class="sxs-lookup"><span data-stu-id="668bc-116">Link-layer addresses in *aa*-*bb*-*cc*-*dd*-*ee*-*ff* format are Ethernet addresses.</span></span> <span data-ttu-id="668bc-117">Endereço de camada de link em *um*. *b*. *c*. o formulário *d* são interfaces 6-over-4.</span><span class="sxs-lookup"><span data-stu-id="668bc-117">Link-layer address in *a*.*b*.*c*.*d* form are 6-over-4 interfaces.</span></span> <span data-ttu-id="668bc-118">Para obter mais informações sobre 6-over-4, consulte RFC 2529.</span><span class="sxs-lookup"><span data-stu-id="668bc-118">For more information on 6-over-4, see RFC 2529.</span></span>

<span data-ttu-id="668bc-119">As duas pseudo interfaces não usam a descoberta de vizinho IPv6.</span><span class="sxs-lookup"><span data-stu-id="668bc-119">The two pseudo-interfaces do not use IPv6 Neighbor Discovery.</span></span>

</dd> <dt>

<span data-ttu-id="668bc-120"><span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**IPv6 IFC** se os \# \[ encaminhar \] \[ anuncia \] \[ -encaminhamentos \] \[ -anuncias \] \[ MTU \# bytes \] \[ site-identificador\]</span><span class="sxs-lookup"><span data-stu-id="668bc-120"><span id="ipv6_ifc_if___forwards___advertises___-forwards___-advertises___mtu__bytes___site_site-identifier_"></span><span id="IPV6_IFC_IF___FORWARDS___ADVERTISES___-FORWARDS___-ADVERTISES___MTU__BYTES___SITE_SITE-IDENTIFIER_"></span>**ipv6 ifc** if\# \[forwards\] \[advertises\] \[-forwards\] \[-advertises\] \[mtu \#bytes\] \[site site-identifier\]</span></span>
</dt> <dd>

<span data-ttu-id="668bc-121">Controla os atributos da interface.</span><span class="sxs-lookup"><span data-stu-id="668bc-121">Controls interface attributes.</span></span> <span data-ttu-id="668bc-122">As interfaces podem ser encaminhadas, caso em que encaminhar pacotes com endereços de destino não atribuídos à interface.</span><span class="sxs-lookup"><span data-stu-id="668bc-122">Interfaces can be forwarding, in which case they forward packets with destination addresses not assigned to the interface.</span></span> <span data-ttu-id="668bc-123">As interfaces podem ser anunciadas; nesse caso, elas enviam anúncios de roteador.</span><span class="sxs-lookup"><span data-stu-id="668bc-123">Interfaces can be advertising, in which case they send router advertisements.</span></span> <span data-ttu-id="668bc-124">Esses atributos podem ser controlados de forma independente.</span><span class="sxs-lookup"><span data-stu-id="668bc-124">These attributes can be independently controlled.</span></span> <span data-ttu-id="668bc-125">Uma interface envia solicitações de roteador e recebe anúncios de roteador ou recebe solicitações de roteador e envia anúncios de roteador.</span><span class="sxs-lookup"><span data-stu-id="668bc-125">An interface either sends router solicitations and receives router advertisements, or receives router solicitations and sends router advertisements.</span></span>

<span data-ttu-id="668bc-126">Como as duas pseudo interfaces não usam a descoberta de vizinho, elas não podem ser configuradas para enviar anúncios de roteador.</span><span class="sxs-lookup"><span data-stu-id="668bc-126">Because the two pseudo-interfaces do not use Neighbor Discovery, they cannot be configured to send router advertisements.</span></span>

<span data-ttu-id="668bc-127">Os encaminhamentos podem ser abreviados como forw e anunciados como avçd.</span><span class="sxs-lookup"><span data-stu-id="668bc-127">Forwards can be abbreviated as forw, and advertised as adv.</span></span>

<span data-ttu-id="668bc-128">O MTU para a interface também pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="668bc-128">The MTU for the interface can also be set.</span></span> <span data-ttu-id="668bc-129">A nova MTU deve ser menor ou igual à MTU máxima (true) do link (conforme relatado pelo IPv6 se) e maior ou igual à MTU IPv6 mínima (1280 bytes).</span><span class="sxs-lookup"><span data-stu-id="668bc-129">The new MTU must be less than or equal to the link's maximum (true) MTU (as reported by ipv6 if) and greater than or equal to the minimum IPv6 MTU (1280 bytes).</span></span>

<span data-ttu-id="668bc-130">O identificador de site para uma interface também pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="668bc-130">The site-identifier for an interface can also be changed.</span></span> <span data-ttu-id="668bc-131">Os identificadores de site são usados no \_ campo ID de escopo sin6 \_ com endereços de site local.</span><span class="sxs-lookup"><span data-stu-id="668bc-131">Site identifiers are used in the sin6\_scope\_id field with site-local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="668bc-132"><span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**IFD IPv6** se\#</span><span class="sxs-lookup"><span data-stu-id="668bc-132"><span id="ipv6_ifd_if_"></span><span id="IPV6_IFD_IF_"></span>**ipv6 ifd** if\#</span></span>
</dt> <dd>

<span data-ttu-id="668bc-133">Exclui uma interface.</span><span class="sxs-lookup"><span data-stu-id="668bc-133">Deletes an interface.</span></span> <span data-ttu-id="668bc-134">As pseudo-interfaces de loopback e de túnel não podem ser excluídas.</span><span class="sxs-lookup"><span data-stu-id="668bc-134">The loopback and tunnel pseudo-interfaces cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="668bc-135"><span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**NC IPv6** \[ Se o \# \[ Endereço\]\]</span><span class="sxs-lookup"><span data-stu-id="668bc-135"><span id="ipv6_nc__if___address__"></span><span id="IPV6_NC__IF___ADDRESS__"></span>**ipv6 nc** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="668bc-136">Exibe o conteúdo do cache vizinho.</span><span class="sxs-lookup"><span data-stu-id="668bc-136">Displays the contents of the neighbor cache.</span></span> <span data-ttu-id="668bc-137">Se um número de interface for especificado, somente o conteúdo do cache vizinho dessa interface será exibido.</span><span class="sxs-lookup"><span data-stu-id="668bc-137">If an interface number is specified, only the contents of that interface's neighbor cache are displayed.</span></span> <span data-ttu-id="668bc-138">Caso contrário, o conteúdo de todos os caches vizinhos da interface será exibido.</span><span class="sxs-lookup"><span data-stu-id="668bc-138">Otherwise, the contents of all the interface's neighbor caches are displayed.</span></span> <span data-ttu-id="668bc-139">Se uma interface for especificada, um endereço IPv6 poderá ser especificado para exibir somente essa entrada de cache vizinho.</span><span class="sxs-lookup"><span data-stu-id="668bc-139">If an interface is specified, an IPv6 address can be specified to display only that neighbor cache entry.</span></span>

<span data-ttu-id="668bc-140">Para cada entrada de cache vizinho, a interface, o endereço IPv6, o endereço de camada de link e o estado de alcance são exibidos.</span><span class="sxs-lookup"><span data-stu-id="668bc-140">For each neighbor cache entry, the interface, IPv6 address, link-layer address, and reach state are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="668bc-141"><span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**NCF IPv6** \[ Se o \# \[ Endereço\]\]</span><span class="sxs-lookup"><span data-stu-id="668bc-141"><span id="ipv6_ncf__if___address__"></span><span id="IPV6_NCF__IF___ADDRESS__"></span>**ipv6 ncf** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="668bc-142">Libera as entradas de cache vizinho especificadas.</span><span class="sxs-lookup"><span data-stu-id="668bc-142">Flushes the specified neighbor cache entries.</span></span> <span data-ttu-id="668bc-143">Somente entradas de cache vizinho sem referências são limpas.</span><span class="sxs-lookup"><span data-stu-id="668bc-143">Only neighbor cache entries without references are purged.</span></span> <span data-ttu-id="668bc-144">Como as entradas do cache de rota mantêm referências a entradas de cache vizinho, o cache de rota deve ser liberado primeiro.</span><span class="sxs-lookup"><span data-stu-id="668bc-144">Because route cache entries hold references to neighbor cache entries, the route cache should be flushed first.</span></span> <span data-ttu-id="668bc-145">As entradas da tabela de roteamento também podem manter referências a entradas de cache vizinho.</span><span class="sxs-lookup"><span data-stu-id="668bc-145">Routing table entries can also hold references to neighbor cache entries.</span></span>

</dd> <dt>

<span data-ttu-id="668bc-146"><span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**IPv6 RC** \[ Se o \# Endereço\]</span><span class="sxs-lookup"><span data-stu-id="668bc-146"><span id="ipv6_rc__if__address_"></span><span id="IPV6_RC__IF__ADDRESS_"></span>**ipv6 rc** \[if\# address\]</span></span>
</dt> <dd>

<span data-ttu-id="668bc-147">Exibe o conteúdo do cache de rota.</span><span class="sxs-lookup"><span data-stu-id="668bc-147">Displays the contents of the route cache.</span></span> <span data-ttu-id="668bc-148">O cache de rota é o nome de implementação do IPv6 da Microsoft para o cache de destino.</span><span class="sxs-lookup"><span data-stu-id="668bc-148">The route cache is the Microsoft IPv6 implementation name for the destination cache.</span></span> <span data-ttu-id="668bc-149">Se uma interface e um endereço forem especificados, a entrada de cache de rota para atingir o endereço por meio da interface será exibida.</span><span class="sxs-lookup"><span data-stu-id="668bc-149">If an interface and address are specified, the route cache entry for reaching the address through the interface is displayed.</span></span> <span data-ttu-id="668bc-150">Caso contrário, todas as entradas de cache de rota serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="668bc-150">Otherwise, all route cache entries are displayed.</span></span>

<span data-ttu-id="668bc-151">Para cada entrada de cache de rota, o endereço IPv6 e a interface de próximo salto atual e o endereço vizinho são exibidos.</span><span class="sxs-lookup"><span data-stu-id="668bc-151">For each route cache entry, the IPv6 address and the current next-hop interface and neighbor address are displayed.</span></span> <span data-ttu-id="668bc-152">O endereço de origem preferencial para uso com esse destino, a MTU do caminho atual para atingir esse destino por meio da interface e a determinação de se esta é uma interface específica – a entrada do cache de rota também é exibida.</span><span class="sxs-lookup"><span data-stu-id="668bc-152">The preferred source address for use with this destination, the current path MTU for reaching this destination through the interface, and the determination of whether this is an interface specific–route cache entry are also displayed.</span></span> <span data-ttu-id="668bc-153">Qualquer endereço de atendimento (para mobilidade) para o endereço de destino também é exibido.</span><span class="sxs-lookup"><span data-stu-id="668bc-153">Any care-of address (for mobility) for the destination address is displayed as well.</span></span>

<span data-ttu-id="668bc-154">Um endereço de destino pode ter várias entradas de cache de rota — tanto quanto uma para cada interface de saída.</span><span class="sxs-lookup"><span data-stu-id="668bc-154">A destination address can have multiple route cache entries—as many as one for each outgoing interface.</span></span> <span data-ttu-id="668bc-155">No entanto, um endereço de destino pode ter no máximo uma entrada de cache de rota que não seja específica da interface.</span><span class="sxs-lookup"><span data-stu-id="668bc-155">However, a destination address can have a maximum of one route cache entry that is not interface-specific.</span></span> <span data-ttu-id="668bc-156">Uma interface específica – a entrada de cache de rota só será usada se o aplicativo especificar explicitamente a interface de saída.</span><span class="sxs-lookup"><span data-stu-id="668bc-156">An interface specific–route cache entry is only used if the application explicitly specifies that outgoing interface.</span></span>

</dd> <dt>

<span data-ttu-id="668bc-157"><span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**RCF IPv6** \[ Se o \# \[ Endereço\]\]</span><span class="sxs-lookup"><span data-stu-id="668bc-157"><span id="ipv6_rcf__if___address__"></span><span id="IPV6_RCF__IF___ADDRESS__"></span>**ipv6 rcf** \[if\# \[address\]\]</span></span>
</dt> <dd>

<span data-ttu-id="668bc-158">Libera as entradas de cache de rota especificadas.</span><span class="sxs-lookup"><span data-stu-id="668bc-158">Flushes the specified route cache entries.</span></span>

</dd> <dt>

<span data-ttu-id="668bc-159"><span id="ipv6_bc"></span><span id="IPV6_BC"></span>**BC IPv6**</span><span class="sxs-lookup"><span data-stu-id="668bc-159"><span id="ipv6_bc"></span><span id="IPV6_BC"></span>**ipv6 bc**</span></span>
</dt> <dd>

<span data-ttu-id="668bc-160">Exibe o conteúdo do cache de associação, que contém associações entre endereços residenciais e endereços de cuidado para IPv6 móvel.</span><span class="sxs-lookup"><span data-stu-id="668bc-160">Displays the contents of the binding cache, which holds bindings between home addresses and care-of addresses for mobile IPv6.</span></span>

<span data-ttu-id="668bc-161">Para cada associação, é exibido o endereço principal, o endereço de atendimento, o número de sequência de associação e o tempo de vida.</span><span class="sxs-lookup"><span data-stu-id="668bc-161">For each binding, the home address, care-of address, binding sequence number, and lifetime are displayed.</span></span>

</dd> <dt>

<span data-ttu-id="668bc-162"><span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**Adu IPv6** If \# /Address \[ Lifetime VL \[ /pl \] \] \[ anycast \] \[ unicast\]</span><span class="sxs-lookup"><span data-stu-id="668bc-162"><span id="ipv6_adu_if__address__lifetime_VL__PL____anycast___unicast_"></span><span id="ipv6_adu_if__address__lifetime_vl__pl____anycast___unicast_"></span><span id="IPV6_ADU_IF__ADDRESS__LIFETIME_VL__PL____ANYCAST___UNICAST_"></span>**ipv6 adu** if\#/address \[lifetime VL\[/PL\]\] \[anycast\] \[unicast\]</span></span>
</dt> <dd>

<span data-ttu-id="668bc-163">Adiciona ou remove uma atribuição de endereço unicast ou anycast em uma interface.</span><span class="sxs-lookup"><span data-stu-id="668bc-163">Adds or removes a unicast or anycast address assignment on an interface.</span></span> <span data-ttu-id="668bc-164">O endereço unicast é acionado a menos que anycast seja especificado.</span><span class="sxs-lookup"><span data-stu-id="668bc-164">The unicast address is acted upon unless anycast is specified.</span></span>

<span data-ttu-id="668bc-165">O tempo de vida é infinito se não especificado.</span><span class="sxs-lookup"><span data-stu-id="668bc-165">Lifetime is infinite if unspecified.</span></span> <span data-ttu-id="668bc-166">Se apenas um tempo de vida válido for especificado, o tempo de vida preferencial será igual ao tempo de vida válido.</span><span class="sxs-lookup"><span data-stu-id="668bc-166">If only a valid lifetime is specified, the preferred lifetime is equal to the valid lifetime.</span></span> <span data-ttu-id="668bc-167">Um tempo de vida infinito pode ser especificado ou um valor finito em segundos.</span><span class="sxs-lookup"><span data-stu-id="668bc-167">An infinite lifetime may be specified, or a finite value in seconds.</span></span> <span data-ttu-id="668bc-168">O tempo de vida preferencial deve ser menor ou igual ao tempo de vida válido.</span><span class="sxs-lookup"><span data-stu-id="668bc-168">The preferred lifetime must be less than or equal to the valid lifetime.</span></span> <span data-ttu-id="668bc-169">A especificação de um tempo de vida igual a zero faz com que o endereço seja removido.</span><span class="sxs-lookup"><span data-stu-id="668bc-169">Specifying a lifetime of zero causes the address to be removed.</span></span>

<span data-ttu-id="668bc-170">Você pode abreviar o tempo de vida como vida útil.</span><span class="sxs-lookup"><span data-stu-id="668bc-170">You can abbreviate lifetime as life.</span></span>

<span data-ttu-id="668bc-171">Para endereços anycast, os únicos valores de tempo de vida válidos são zero e infinito.</span><span class="sxs-lookup"><span data-stu-id="668bc-171">For anycast addresses, the only valid lifetime values are zero and infinite.</span></span>

</dd> <dt>

<span data-ttu-id="668bc-172"><span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**SPT IPv6**</span><span class="sxs-lookup"><span data-stu-id="668bc-172"><span id="ipv6_spt"></span><span id="IPV6_SPT"></span>**ipv6 spt**</span></span>
</dt> <dd>

<span data-ttu-id="668bc-173">Exibe o conteúdo atual da tabela de prefixo do site.</span><span class="sxs-lookup"><span data-stu-id="668bc-173">Displays the current contents of the site prefix table.</span></span>

<span data-ttu-id="668bc-174">Para cada prefixo de site, o comando exibe o prefixo, a interface à qual o prefixo do site se aplica e o tempo de vida do prefixo em segundos.</span><span class="sxs-lookup"><span data-stu-id="668bc-174">For each site prefix, the command displays the prefix, the interface to which the site prefix applies, and the prefix lifetime in seconds.</span></span>

<span data-ttu-id="668bc-175">Os prefixos de site normalmente são configurados automaticamente a partir de anúncios de roteador.</span><span class="sxs-lookup"><span data-stu-id="668bc-175">Site prefixes are normally auto-configured from router advertisements.</span></span> <span data-ttu-id="668bc-176">Eles são usados na função [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) para filtrar endereços locais inadequados do site.</span><span class="sxs-lookup"><span data-stu-id="668bc-176">They are used in the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function to filter inappropriate site-local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="668bc-177"><span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>prefixo de **SPU IPv6** se \# \[ tempo de vida L\]</span><span class="sxs-lookup"><span data-stu-id="668bc-177"><span id="ipv6_spu_prefix_if___lifetime_L_"></span><span id="ipv6_spu_prefix_if___lifetime_l_"></span><span id="IPV6_SPU_PREFIX_IF___LIFETIME_L_"></span>**ipv6 spu** prefix if\# \[lifetime L\]</span></span>
</dt> <dd>

<span data-ttu-id="668bc-178">Adiciona, remove ou atualiza um prefixo na tabela de prefixo do site.</span><span class="sxs-lookup"><span data-stu-id="668bc-178">Adds, removes, or updates a prefix in the site prefix table.</span></span>

<span data-ttu-id="668bc-179">O prefixo e o número da interface são necessários.</span><span class="sxs-lookup"><span data-stu-id="668bc-179">The prefix and interface number are required.</span></span> <span data-ttu-id="668bc-180">O tempo de vida do prefixo do site, especificado em segundos, padrão será infinito se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="668bc-180">The site prefix lifetime, specified in seconds, defaults to infinite if not specified.</span></span> <span data-ttu-id="668bc-181">Especificar um tempo de vida igual a zero exclui o prefixo do site.</span><span class="sxs-lookup"><span data-stu-id="668bc-181">Specifying a lifetime of zero deletes the site prefix.</span></span>

<span data-ttu-id="668bc-182">Esse comando é desnecessário para a configuração normal de hosts ou roteadores.</span><span class="sxs-lookup"><span data-stu-id="668bc-182">This command is unnecessary for the normal configuration of hosts or routers.</span></span>

</dd> <dt>

<span data-ttu-id="668bc-183"><span id="ipv6_rt"></span><span id="IPV6_RT"></span>**IPv6 RT**</span><span class="sxs-lookup"><span data-stu-id="668bc-183"><span id="ipv6_rt"></span><span id="IPV6_RT"></span>**ipv6 rt**</span></span>
</dt> <dd>

<span data-ttu-id="668bc-184">Exibe o conteúdo atual da tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="668bc-184">Displays the current contents of the routing table.</span></span>

<span data-ttu-id="668bc-185">Para cada entrada de tabela de roteamento, o comando exibe o prefixo de rota, uma interface em link ou um vizinho de próximo salto em uma interface, um valor de preferência (menor é preferencial) e um tempo de vida em segundos.</span><span class="sxs-lookup"><span data-stu-id="668bc-185">For each routing table entry, the command displays the route prefix, an on-link interface or a next-hop neighbor on an interface, a preference value (smaller is preferred), and a lifetime in seconds.</span></span>

<span data-ttu-id="668bc-186">As entradas da tabela de roteamento também podem ter atributos de **publicação** e de **expiração** .</span><span class="sxs-lookup"><span data-stu-id="668bc-186">Routing table entries may also have **publish** and **aging** attributes.</span></span> <span data-ttu-id="668bc-187">Por padrão, elas envelhecem (a vida útil conta, em vez da constante restante) e não são publicadas (não são usadas na construção de anúncios de roteador).</span><span class="sxs-lookup"><span data-stu-id="668bc-187">By default, they age (the lifetime counts down, rather than remaining constant) and are not published (not used in constructing router advertisements).</span></span>

<span data-ttu-id="668bc-188">Em hosts, as entradas da tabela de roteamento normalmente são configuradas automaticamente de anúncios de roteador.</span><span class="sxs-lookup"><span data-stu-id="668bc-188">On hosts, routing table entries are normally auto-configured from router advertisements.</span></span>

</dd> <dt>

<span data-ttu-id="668bc-189"><span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>prefixo **RTU IPv6** se \# \[ /nexthop \] \[ tempo de vida L \] \[ preferência P \] \[ publicar \] \[ idade \] \[ SPL site-prefixo-comprimento\]</span><span class="sxs-lookup"><span data-stu-id="668bc-189"><span id="ipv6_rtu_prefix_if___nexthop___lifetime_L___preference_P___publish___age___spl_site-prefix-length_"></span><span id="ipv6_rtu_prefix_if___nexthop___lifetime_l___preference_p___publish___age___spl_site-prefix-length_"></span><span id="IPV6_RTU_PREFIX_IF___NEXTHOP___LIFETIME_L___PREFERENCE_P___PUBLISH___AGE___SPL_SITE-PREFIX-LENGTH_"></span>**ipv6 rtu** prefix if\#\[/nexthop\] \[lifetime L\] \[preference P\] \[publish\] \[age\] \[spl site-prefix-length\]</span></span>
</dt> <dd>

<span data-ttu-id="668bc-190">Adiciona ou remove uma rota na tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="668bc-190">Adds or removes a route in the routing table.</span></span> <span data-ttu-id="668bc-191">O prefixo de rota é necessário.</span><span class="sxs-lookup"><span data-stu-id="668bc-191">The route prefix is required.</span></span> <span data-ttu-id="668bc-192">O prefixo pode estar no link para uma interface especificada ou próximo salto, especificado com um endereço vizinho em uma interface.</span><span class="sxs-lookup"><span data-stu-id="668bc-192">The prefix can be on-link to a specified interface, or next-hop, specified with a neighbor address on an interface.</span></span> <span data-ttu-id="668bc-193">A rota pode ter um tempo de vida em segundos, com o infinito padrão e uma preferência, com o padrão de zero ou o mais preferencial.</span><span class="sxs-lookup"><span data-stu-id="668bc-193">The route can have a lifetime in seconds, with the default infinite, and a preference, with the default of zero, or most preferred.</span></span> <span data-ttu-id="668bc-194">Especificar um tempo de vida igual a zero exclui a rota.</span><span class="sxs-lookup"><span data-stu-id="668bc-194">Specifying a lifetime of zero deletes the route.</span></span>

<span data-ttu-id="668bc-195">Se a rota for especificada como publicada, indicando que ela será usada na construção de anúncios de roteador, ela não age.</span><span class="sxs-lookup"><span data-stu-id="668bc-195">If the route is specified as published, indicating it will be used in constructing router advertisements, it does not age.</span></span> <span data-ttu-id="668bc-196">O tempo de vida da rota não é contabilizado e, portanto, é efetivamente infinito, mas o valor é usado em anúncios de roteador.</span><span class="sxs-lookup"><span data-stu-id="668bc-196">The route's lifetime does not count down and therefore is effectively infinite, but the value is used in router advertisements.</span></span> <span data-ttu-id="668bc-197">Opcionalmente, uma rota pode ser especificada como uma rota publicada que também expira.</span><span class="sxs-lookup"><span data-stu-id="668bc-197">Optionally, a route can be specified as a published route that also ages.</span></span> <span data-ttu-id="668bc-198">Por padrão, uma rota não publicada sempre é expirada.</span><span class="sxs-lookup"><span data-stu-id="668bc-198">A nonpublished route by default always ages.</span></span>

<span data-ttu-id="668bc-199">A subopção SPL opcional pode ser usada para especificar um comprimento de prefixo de site associado à rota.</span><span class="sxs-lookup"><span data-stu-id="668bc-199">The optional spl suboption can be used to specify a site prefix length associated with the route.</span></span> <span data-ttu-id="668bc-200">O comprimento do prefixo do site é usado somente ao enviar anúncios de roteador.</span><span class="sxs-lookup"><span data-stu-id="668bc-200">The site prefix length is used only when sending router advertisements.</span></span>

<span data-ttu-id="668bc-201">O tempo de vida pode ser abreviado como vida, preferência como pref e publicar como pub.</span><span class="sxs-lookup"><span data-stu-id="668bc-201">Lifetime can be abbreviated as life, preference as pref, and publish as pub.</span></span>

</dd> </dl>

 

 



