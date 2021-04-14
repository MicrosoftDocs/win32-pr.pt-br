---
description: o 6to4 é um método para conectar hosts ou sites IPv6 pela infraestrutura de Internet IPv4 existente.
ms.assetid: 3ca8518d-42f0-428c-b94c-ff244d17b314
title: 'Configuração 2: tráfego IPv6 entre nós em sub-redes diferentes de um protocolo de rede IPv4 (6to4)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1abd5477005e6a1e71c13aaf19a734e9191097d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461117"
---
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a><span data-ttu-id="b4f01-103">Configuração 2: tráfego IPv6 entre nós em sub-redes diferentes de um protocolo de rede IPv4 (6to4)</span><span class="sxs-lookup"><span data-stu-id="b4f01-103">Configuration 2: IPv6 Traffic Between Nodes on Different Subnets of an IPv4 Internetwork (6to4)</span></span>

<span data-ttu-id="b4f01-104">o 6to4 é um método para conectar hosts ou sites IPv6 pela infraestrutura de Internet IPv4 existente.</span><span class="sxs-lookup"><span data-stu-id="b4f01-104">6to4 is a method for connecting IPv6 hosts or sites over the existing IPv4 Internet infrastructure.</span></span> <span data-ttu-id="b4f01-105">Ele usa um prefixo de endereço exclusivo para dar aos sites IPv6 isolados seu próprio espaço de endereço IPv6.</span><span class="sxs-lookup"><span data-stu-id="b4f01-105">It uses a unique address prefix to give isolated IPv6 sites their own IPv6 address space.</span></span> <span data-ttu-id="b4f01-106">o 6to4 é como um "pseudo-ISP" que fornece conectividade IPv6.</span><span class="sxs-lookup"><span data-stu-id="b4f01-106">6to4 is like a "pseudo-ISP" providing IPv6 connectivity.</span></span> <span data-ttu-id="b4f01-107">Você pode usar o 6to4 para se comunicar diretamente com outros sites 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-107">You can use 6to4 to communicate directly with other 6to4 sites.</span></span> <span data-ttu-id="b4f01-108">o 6to4 não exige o uso de roteadores IPv6 e seu tráfego IPv6 é encapsulado com um cabeçalho IPv4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-108">6to4 does not require the use of IPv6 routers and its IPv6 traffic is encapsulated with an IPv4 header.</span></span>

<span data-ttu-id="b4f01-109">A ilustração a seguir mostra a configuração de dois nós em sub-redes separadas usando o 6to4 para se comunicar em um roteador IPv4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-109">The following illustration shows the configuration of two nodes on separate subnets using 6to4 to communicate across an IPv4 router.</span></span>

![nós que usam o 6to4 para se comunicar em um roteador IPv4.](images/v6mig-2.png)

<span data-ttu-id="b4f01-111">O principal requisito para usar o 6to4 é um endereço IPv4 roteável globalmente para seu site.</span><span class="sxs-lookup"><span data-stu-id="b4f01-111">The main requirement for using 6to4 is one globally routable IPv4 address for your site.</span></span> <span data-ttu-id="b4f01-112">Suponha que seu site consiste em uma coleção de computadores IPv6 que você gerencia (alguns executando o protocolo Microsoft IPv6 e alguns executando outras implementações de IPv6).</span><span class="sxs-lookup"><span data-stu-id="b4f01-112">Suppose that your site consists of a collection of IPv6 computers that you manage (some running the Microsoft IPv6 protocol and some running other IPv6 implementations).</span></span> <span data-ttu-id="b4f01-113">Suponha também que todos os computadores IPv6 estejam diretamente conectados usando Ethernet ou 6 sobre 4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-113">Assume also that all IPv6 computers are directly connected using Ethernet or 6-over-4.</span></span> <span data-ttu-id="b4f01-114">O endereço IPv4 roteável globalmente deve ser atribuído a um dos seus computadores que executam o protocolo IPv6 da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b4f01-114">The globally routable IPv4 address must be assigned to one of your computers running the Microsoft IPv6 protocol.</span></span> <span data-ttu-id="b4f01-115">Este computador será o gateway do 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-115">This computer will be your 6to4 gateway.</span></span>

<span data-ttu-id="b4f01-116">Se você tiver um endereço IPv4 que faz parte do espaço de endereço privado (10.0.0.0/8, 172.16.0.0/12 ou 192.168.0.0/16) ou o espaço de endereço APIPA (endereçamento IP privado automático) de 169.254.0.0/16 usado pelo Windows 2000, ele não será roteável globalmente.</span><span class="sxs-lookup"><span data-stu-id="b4f01-116">If you have an IPv4 address that is part of the private address space (10.0.0.0/8, 172.16.0.0/12, or 192.168.0.0/16) or the Automatic Private IP Addressing (APIPA) address space of 169.254.0.0/16 used by Windows 2000, it is not globally routable.</span></span> <span data-ttu-id="b4f01-117">Caso contrário, é provavelmente um endereço IP público e é roteável globalmente.</span><span class="sxs-lookup"><span data-stu-id="b4f01-117">Otherwise, it is probably a public IP address and is globally routable.</span></span> <span data-ttu-id="b4f01-118">Consulte o tópico [depuração de configuração de 6to4](#debugging-6to4-configuration) neste documento para obter mais ajuda para determinar se sua conexão de ISP oferece suporte a 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-118">See the [Debugging 6to4 Configuration](#debugging-6to4-configuration) topic in this document for more help in determining whether your ISP connection supports 6to4.</span></span>

## <a name="the-6to4cfgexe-tool"></a><span data-ttu-id="b4f01-119">A ferramenta de 6to4cfg.exe</span><span class="sxs-lookup"><span data-stu-id="b4f01-119">The 6to4cfg.exe Tool</span></span>

<span data-ttu-id="b4f01-120">A ferramenta de 6to4cfg.exe automatiza a configuração de 6to4, descobrindo automaticamente seu endereço IPv4 roteável globalmente e criando um prefixo 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-120">The 6to4cfg.exe tool automates 6to4 configuration, automatically discovering your globally routable IPv4 address and creating a 6to4 prefix.</span></span> <span data-ttu-id="b4f01-121">Ele executa a configuração diretamente ou pode gravar um script de configuração que você pode inspecionar e executar mais tarde.</span><span class="sxs-lookup"><span data-stu-id="b4f01-121">It either performs the configuration directly, or it can write a configuration script that you can inspect and run later.</span></span>

<span data-ttu-id="b4f01-122">A sintaxe de comando 6to4cfg.exe básica é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="b4f01-122">The basic 6to4cfg.exe command syntax is as follows.</span></span>

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span data-ttu-id="b4f01-123"><span id="_filename_"></span><span id="_FILENAME_"></span>\[*nome do arquivo*\]</span><span class="sxs-lookup"><span data-stu-id="b4f01-123"><span id="_filename_"></span><span id="_FILENAME_"></span>\[*filename*\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f01-124">Grava o script de configuração em um arquivo, se você especificar um nome de arquivo.</span><span class="sxs-lookup"><span data-stu-id="b4f01-124">Writes the configuration script to a file, if you specify a file name.</span></span> <span data-ttu-id="b4f01-125">O script de configuração usa Ipv6.exe.</span><span class="sxs-lookup"><span data-stu-id="b4f01-125">The configuration script uses Ipv6.exe.</span></span>

<span data-ttu-id="b4f01-126">Você pode especificar con para o nome do arquivo gravar o script de configuração na saída do console, o que é útil para ver o que 6to4cfg.exe fará em um cenário de teste.</span><span class="sxs-lookup"><span data-stu-id="b4f01-126">You can specify con for the file name to write the configuration script to console output, which is useful for seeing what 6to4cfg.exe will do in a test scenario.</span></span>

<span data-ttu-id="b4f01-127">Se você não especificar um nome de arquivo, 6to4cfg.exe atualizará diretamente a configuração de IPv6 em seu computador.</span><span class="sxs-lookup"><span data-stu-id="b4f01-127">If you do not specify a file name, 6to4cfg.exe directly updates the IPv6 configuration on your computer.</span></span>

</dd> <dt>

<span data-ttu-id="b4f01-128"><span id="-r"></span><span id="-R"></span>-r</span><span class="sxs-lookup"><span data-stu-id="b4f01-128"><span id="-r"></span><span id="-R"></span>-r</span></span>
</dt> <dd>

<span data-ttu-id="b4f01-129">Torna-se um roteador de gateway 6to4 para sua rede local, habilitando o roteamento em todas as suas interfaces e prefixos de sub-rede atribuídos.</span><span class="sxs-lookup"><span data-stu-id="b4f01-129">Becomes a 6to4 gateway router for your local network, enabling routing on all of your interfaces and assigned subnet prefixes.</span></span>

</dd> <dt>

<span data-ttu-id="b4f01-130"><span id="-s"></span><span id="-S"></span>-s</span><span class="sxs-lookup"><span data-stu-id="b4f01-130"><span id="-s"></span><span id="-S"></span>-s</span></span>
</dt> <dd>

<span data-ttu-id="b4f01-131">Habilita o endereçamento local no site do 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-131">Enables site-local addressing in your 6to4 site.</span></span> <span data-ttu-id="b4f01-132">Esse comando só é útil quando usado em conjunto com-r.</span><span class="sxs-lookup"><span data-stu-id="b4f01-132">This command is only useful when used in conjunction with -r.</span></span>

</dd> <dt>

<span data-ttu-id="b4f01-133"><span id="-u"></span><span id="-U"></span>-u</span><span class="sxs-lookup"><span data-stu-id="b4f01-133"><span id="-u"></span><span id="-U"></span>-u</span></span>
</dt> <dd>

<span data-ttu-id="b4f01-134">Especifica que a configuração de 6to4 será revertida.</span><span class="sxs-lookup"><span data-stu-id="b4f01-134">Specifies that the 6to4 configuration be reversed.</span></span> <span data-ttu-id="b4f01-135">Portanto, 6to4cfg-u reverte o efeito de 6to4cfg e 6to4cfg-r-u inverte o efeito de 6to4cfg-r e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b4f01-135">Therefore 6to4cfg -u reverses the effect of 6to4cfg and 6to4cfg -r -u reverses the effect of 6to4cfg -r, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="b4f01-136"><span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *retransmissão*</span><span class="sxs-lookup"><span data-stu-id="b4f01-136"><span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *relay*</span></span>
</dt> <dd>

<span data-ttu-id="b4f01-137">Especifica o nome ou endereço IPv4 de um roteador de retransmissão 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-137">Specifies the name or IPv4 address of a 6to4 relay router.</span></span> <span data-ttu-id="b4f01-138">O nome padrão é 6to4.ipv6.microsoft.com, o roteador de retransmissão 6to4 na Internet.</span><span class="sxs-lookup"><span data-stu-id="b4f01-138">The default name is 6to4.ipv6.microsoft.com, the 6to4 relay router on the Internet.</span></span>

</dd> <dt>

<span data-ttu-id="b4f01-139"><span id="-b"></span><span id="-B"></span>-b</span><span class="sxs-lookup"><span data-stu-id="b4f01-139"><span id="-b"></span><span id="-B"></span>-b</span></span>
</dt> <dd>

<span data-ttu-id="b4f01-140">Especifica que 6to4cfg.exe escolhe o endereço de retransmissão "melhor" em vez do primeiro.</span><span class="sxs-lookup"><span data-stu-id="b4f01-140">Specifies that 6to4cfg.exe picks the "best" relay address instead of the first.</span></span>

</dd> <dt>

<span data-ttu-id="b4f01-141"><span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *endereço*</span><span class="sxs-lookup"><span data-stu-id="b4f01-141"><span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *address*</span></span>
</dt> <dd>

<span data-ttu-id="b4f01-142">Especifica o endereço IPv4 local para o prefixo 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-142">Specifies the local IPv4 address for the 6to4 prefix.</span></span>

</dd> </dl>

## <a name="manual-6to4-configuration"></a><span data-ttu-id="b4f01-143">Configuração de 6to4 manual</span><span class="sxs-lookup"><span data-stu-id="b4f01-143">Manual 6to4 Configuration</span></span>

<span data-ttu-id="b4f01-144">Neste exemplo, o endereço do gateway 6to4 é 172.31.42.239.</span><span class="sxs-lookup"><span data-stu-id="b4f01-144">In this example the address of the 6to4 gateway is 172.31.42.239.</span></span> <span data-ttu-id="b4f01-145">Você precisa de seu próprio endereço IPv4 roteável globalmente para usar o 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-145">You need your own globally routable IPv4 address to use 6to4.</span></span>

> [!Note]  
> <span data-ttu-id="b4f01-146">O endereço IP 172.31.42.239 é usado apenas para fins de exemplo.</span><span class="sxs-lookup"><span data-stu-id="b4f01-146">The IP address 172.31.42.239 is used for example purposes only.</span></span> <span data-ttu-id="b4f01-147">Esse é um endereço privado e não é roteável globalmente na Internet.</span><span class="sxs-lookup"><span data-stu-id="b4f01-147">This is a private address and is not globally routable on the Internet.</span></span>

 

<span data-ttu-id="b4f01-148">O endereço IPv4 roteável globalmente de 32 bits é combinado com o prefixo de 16 bits 2002::/16 para formar um prefixo de endereço IPv6 de 48 bits para seu site.</span><span class="sxs-lookup"><span data-stu-id="b4f01-148">The 32-bit globally routable IPv4 address is combined with the 16-bit prefix 2002::/16 to form a 48-bit IPv6 address prefix for your site.</span></span> <span data-ttu-id="b4f01-149">Neste exemplo, o prefixo do site 6to4 é 2002: ac1f: 2aef::/48.</span><span class="sxs-lookup"><span data-stu-id="b4f01-149">In this example, the 6to4 site prefix is 2002:ac1f:2aef::/48.</span></span> <span data-ttu-id="b4f01-150">Observe que ac1f: 2aef é a codificação hexadecimal de 172.31.42.239 (é claro, você usará um prefixo diferente com base em seu próprio endereço IPv4 roteável globalmente).</span><span class="sxs-lookup"><span data-stu-id="b4f01-150">Note that ac1f:2aef is the hexadecimal encoding of 172.31.42.239 (of course, you will use a different prefix based on your own globally routable IPv4 address).</span></span> <span data-ttu-id="b4f01-151">Usando o prefixo do site 6to4, você pode atribuir endereços e prefixos de sub-rede dentro de seu site.</span><span class="sxs-lookup"><span data-stu-id="b4f01-151">Using the 6to4 site prefix, you can assign addresses and subnet prefixes inside your site.</span></span>

<span data-ttu-id="b4f01-152">Este exemplo pressupõe que você use a sub-rede 0 para configurar manualmente um endereço 6to4 no seu computador de gateway 6to4 e que você usa a sub-rede 1 para configurar automaticamente endereços em seu segmento de rede Ethernet.</span><span class="sxs-lookup"><span data-stu-id="b4f01-152">This example assumes that you use subnet 0 for manually configuring a 6to4 address on your 6to4 gateway computer and that you use subnet 1 for automatically configuring addresses on your Ethernet network segment.</span></span> <span data-ttu-id="b4f01-153">No entanto, outras opções são possíveis.</span><span class="sxs-lookup"><span data-stu-id="b4f01-153">However, other choices are possible.</span></span>

1.  <span data-ttu-id="b4f01-154">Use Ipv6.exe para habilitar o 6to4 em seu computador de gateway 6to4:</span><span class="sxs-lookup"><span data-stu-id="b4f01-154">Use Ipv6.exe to enable 6to4 on your 6to4 gateway computer:</span></span>

    <span data-ttu-id="b4f01-155">**IPv6 RTU 2002::/16 2**</span><span class="sxs-lookup"><span data-stu-id="b4f01-155">**ipv6 rtu 2002::/16 2**</span></span>

    <span data-ttu-id="b4f01-156">O comando **ipv6 rtu** executa uma atualização de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="b4f01-156">The **ipv6 rtu** command performs a routing table update.</span></span> <span data-ttu-id="b4f01-157">Ele pode ser usado para adicionar, remover ou atualizar uma rota.</span><span class="sxs-lookup"><span data-stu-id="b4f01-157">It can be used to add, remove, or update a route.</span></span> <span data-ttu-id="b4f01-158">Nesse caso, ele está habilitando o 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-158">In this case it is enabling 6to4.</span></span>

    <span data-ttu-id="b4f01-159">O argumento 2002::/16 é o prefixo da rota, especificando o prefixo 6to4 exclusivo.</span><span class="sxs-lookup"><span data-stu-id="b4f01-159">The 2002::/16 argument is the prefix of the route, specifying the unique 6to4 prefix.</span></span>

    <span data-ttu-id="b4f01-160">O argumento 2 especifica a interface no link para esse prefixo.</span><span class="sxs-lookup"><span data-stu-id="b4f01-160">The 2 argument specifies the on-link interface for this prefix.</span></span> <span data-ttu-id="b4f01-161">\#A interface 2 é a "pseudo-interface" usada para túneis configurados, túnel automático e 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-161">Interface \#2 is the "pseudo-interface" used for configured tunnels, automatic tunneling, and 6to4.</span></span> <span data-ttu-id="b4f01-162">Quando um endereço de destino IPv6 corresponde ao prefixo 2002::/16, os 32 bits que seguem o prefixo no endereço de destino são extraídos para formar um endereço de destino IPv4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-162">When an IPv6 destination address matches the 2002::/16 prefix, the 32 bits that follow the prefix in the destination address are extracted to form an IPv4 destination address.</span></span> <span data-ttu-id="b4f01-163">O pacote é encapsulado com um cabeçalho IPv4 e enviado ao endereço de destino IPv4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-163">The packet is encapsulated with an IPv4 header and sent to the IPv4 destination address.</span></span>

2.  <span data-ttu-id="b4f01-164">Configure um endereço 6to4 em seu computador de gateway 6to4:</span><span class="sxs-lookup"><span data-stu-id="b4f01-164">Configure a 6to4 address on your 6to4 gateway computer:</span></span>

    <span data-ttu-id="b4f01-165">**o IPv6 Adu 2/2002: ac1f: 2aef:: ac1f: 2aef**</span><span class="sxs-lookup"><span data-stu-id="b4f01-165">**ipv6 adu 2/2002:ac1f:2aef::ac1f:2aef**</span></span>

    <span data-ttu-id="b4f01-166">O comando **IPv6 Adu** executa uma atualização de endereço.</span><span class="sxs-lookup"><span data-stu-id="b4f01-166">The **ipv6 adu** command performs an address update.</span></span> <span data-ttu-id="b4f01-167">Ele pode ser usado para adicionar, remover ou atualizar um endereço em uma interface.</span><span class="sxs-lookup"><span data-stu-id="b4f01-167">It can be used to add, remove, or update an address on an interface.</span></span> <span data-ttu-id="b4f01-168">Nessa instância, ele está configurando o endereço 6to4 do computador.</span><span class="sxs-lookup"><span data-stu-id="b4f01-168">In this instance, it is configuring the computer's 6to4 address.</span></span>

    <span data-ttu-id="b4f01-169">O argumento 2/2002: ac1f: 2aef:: ac1f: 2aef especifica a interface e o endereço.</span><span class="sxs-lookup"><span data-stu-id="b4f01-169">The 2/2002:ac1f:2aef::ac1f:2aef argument specifies both the interface and the address.</span></span> <span data-ttu-id="b4f01-170">Ele requer a configuração do endereço 2002: ac1f: 2aef:: ac1f: 2aef na interface \# 2.</span><span class="sxs-lookup"><span data-stu-id="b4f01-170">It requires configuring address 2002:ac1f:2aef::ac1f:2aef on interface \#2.</span></span> <span data-ttu-id="b4f01-171">O endereço é criado usando o prefixo do site 2002: ac1f: 2aef::/48, sub-rede 0 para dar um prefixo de sub-rede 2002: ac1f: 2aef::/64 e um identificador de interface de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="b4f01-171">The address is created using the site prefix 2002:ac1f:2aef::/48, subnet 0 to give a subnet prefix 2002:ac1f:2aef::/64, and a 64-bit interface identifier.</span></span> <span data-ttu-id="b4f01-172">A Convenção demonstrada usa o endereço IPv4 do computador para o identificador de interface para endereços atribuídos à interface \# 2.</span><span class="sxs-lookup"><span data-stu-id="b4f01-172">The convention demonstrated uses the computer's IPv4 address for the interface identifier for addresses assigned to interface \#2.</span></span> <span data-ttu-id="b4f01-173">Para seu uso, ac1f: 2aef deve ser substituído pela codificação hexadecimal do seu próprio endereço IPv4 roteável globalmente.</span><span class="sxs-lookup"><span data-stu-id="b4f01-173">For your use, ac1f:2aef should be replaced by the hexadecimal encoding of your own globally routable IPv4 address.</span></span>

<span data-ttu-id="b4f01-174">Os dois comandos anteriores são suficientes para permitir a comunicação com outros sites 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-174">The two preceding commands are sufficient to allow communication with other 6to4 sites.</span></span> <span data-ttu-id="b4f01-175">Por exemplo, você pode tentar executar ping no site 6to4 da Microsoft:</span><span class="sxs-lookup"><span data-stu-id="b4f01-175">For example, you can try pinging the Microsoft 6to4 site:</span></span>

<span data-ttu-id="b4f01-176">**ping6 2002:836b: 9820:: 836b: 9820**</span><span class="sxs-lookup"><span data-stu-id="b4f01-176">**ping6 2002:836b:9820::836b:9820**</span></span>

<span data-ttu-id="b4f01-177">Para habilitar a comunicação com o 6bone, você deve criar um túnel configurado padrão para uma retransmissão de 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-177">To enable communication with the 6bone, you must create a default configured tunnel to a 6to4 relay.</span></span> <span data-ttu-id="b4f01-178">Você pode usar o roteador de retransmissão 6to4 da Microsoft, 131.107.152.32:</span><span class="sxs-lookup"><span data-stu-id="b4f01-178">You can use the Microsoft 6to4 relay router, 131.107.152.32:</span></span>

<span data-ttu-id="b4f01-179">**IPv6 RTU::/0 2/:: 131.107.152.32 pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="b4f01-179">**ipv6 rtu ::/0 2/::131.107.152.32 pub life 1800**</span></span>

<span data-ttu-id="b4f01-180">O comando **ipv6 rtu** executa uma atualização de tabela de roteamento, estabelecendo, nessa instância, uma rota padrão para a retransmissão de 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-180">The **ipv6 rtu** command performs a routing table update, establishing, in this instance, a default route to the 6to4 relay.</span></span>

<span data-ttu-id="b4f01-181">O argumento::/0 é o prefixo de rota.</span><span class="sxs-lookup"><span data-stu-id="b4f01-181">The ::/0 argument is the route prefix.</span></span> <span data-ttu-id="b4f01-182">O prefixo de comprimento zero indica que se trata de uma rota padrão.</span><span class="sxs-lookup"><span data-stu-id="b4f01-182">The zero-length prefix indicates that it is a default route.</span></span>

<span data-ttu-id="b4f01-183">O argumento 2/:: 131.107.152.32 especifica o vizinho do próximo salto para esse prefixo.</span><span class="sxs-lookup"><span data-stu-id="b4f01-183">The 2/::131.107.152.32 argument specifies the next-hop neighbor for this prefix.</span></span> <span data-ttu-id="b4f01-184">Ele requer que os pacotes que correspondem ao prefixo sejam encaminhados para Address:: 131.107.152.32 usando a interface \# 2.</span><span class="sxs-lookup"><span data-stu-id="b4f01-184">It requires that packets matching the prefix are forwarded to address ::131.107.152.32 using interface \#2.</span></span> <span data-ttu-id="b4f01-185">O encaminhamento de um pacote para:: 131.107.152.32 na interface \# 2 faz com que ele seja encapsulado com um cabeçalho v4 e enviado a 131.107.152.32.</span><span class="sxs-lookup"><span data-stu-id="b4f01-185">Forwarding a packet to ::131.107.152.32 on interface \#2 causes it to be encapsulated with a v4 header and sent to 131.107.152.32.</span></span>

<span data-ttu-id="b4f01-186">O argumento pub torna essa rota publicada.</span><span class="sxs-lookup"><span data-stu-id="b4f01-186">The pub argument makes this a published route.</span></span> <span data-ttu-id="b4f01-187">Como isso só é relevante para roteadores, ele não tem efeito até que o roteamento seja habilitado.</span><span class="sxs-lookup"><span data-stu-id="b4f01-187">Because this is only relevant for routers, it has no effect until routing is enabled.</span></span> <span data-ttu-id="b4f01-188">Da mesma forma, o tempo de vida de 30 minutos se refere apenas se o roteamento estiver habilitado.</span><span class="sxs-lookup"><span data-stu-id="b4f01-188">Similarly, the 30-minute lifetime pertains only if routing is enabled.</span></span>

<span data-ttu-id="b4f01-189">Você deve ser capaz de acessar sites do 6bone, bem como sites 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-189">You should be able to access 6bone sites as well as 6to4 sites.</span></span> <span data-ttu-id="b4f01-190">Você pode usar o seguinte comando para testar isso:</span><span class="sxs-lookup"><span data-stu-id="b4f01-190">You can use the following command to test this:</span></span>

<span data-ttu-id="b4f01-191">**ping6 3ffe: 1cff: 0: F5:: 1**</span><span class="sxs-lookup"><span data-stu-id="b4f01-191">**ping6 3ffe:1cff:0:f5::1**</span></span>

<span data-ttu-id="b4f01-192">A etapa final é habilitar o roteamento em seu gateway 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-192">The final step is to enable routing on your 6to4 gateway.</span></span> <span data-ttu-id="b4f01-193">Este exemplo supõe que a interface \# 3 no seu computador de gateway é uma interface Ethernet e a interface \# 4 é 6-over-4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-193">This example assumes that interface \#3 on your gateway computer is an Ethernet interface and interface \#4 is 6-over-4.</span></span> <span data-ttu-id="b4f01-194">Seu computador pode numerar suas interfaces de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="b4f01-194">Your computer might number its interfaces differently.</span></span> <span data-ttu-id="b4f01-195">Os dois comandos a seguir atribuem prefixos de sub-rede aos dois links.</span><span class="sxs-lookup"><span data-stu-id="b4f01-195">The following two commands assign subnet prefixes to the two links.</span></span> <span data-ttu-id="b4f01-196">Os prefixos de sub-rede são derivados do prefixo 6to4 do site 2002: ac1f: 2aef::/48:</span><span class="sxs-lookup"><span data-stu-id="b4f01-196">The subnet prefixes are derived from the site's 6to4 prefix 2002:ac1f:2aef::/48:</span></span>

<span data-ttu-id="b4f01-197">**IPv6 RTU 2002: ac1f: 2aef: 1::/64 3 pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="b4f01-197">**ipv6 rtu 2002:ac1f:2aef:1::/64 3 pub life 1800**</span></span>

<span data-ttu-id="b4f01-198">**IPv6 RTU 2002: ac1f: 2aef: 2::/64 4 pub Life 1800**</span><span class="sxs-lookup"><span data-stu-id="b4f01-198">**ipv6 rtu 2002:ac1f:2aef:2::/64 4 pub life 1800**</span></span>

<span data-ttu-id="b4f01-199">O comando **ipv6 rtu** especifica que o prefixo 2002: ac1f: 2aef: 1::/64 está no link para a interface \# 3.</span><span class="sxs-lookup"><span data-stu-id="b4f01-199">The **ipv6 rtu** command specifies that the prefix 2002:ac1f:2aef:1::/64 is on-link to interface \#3.</span></span> <span data-ttu-id="b4f01-200">Ele está configurando o primeiro prefixo de sub-rede na interface Ethernet.</span><span class="sxs-lookup"><span data-stu-id="b4f01-200">It is configuring the first subnet prefix on the Ethernet interface.</span></span> <span data-ttu-id="b4f01-201">A rota é publicada com um tempo de vida de 30 minutos.</span><span class="sxs-lookup"><span data-stu-id="b4f01-201">The route is published with a lifetime of 30 minutes.</span></span>

<span data-ttu-id="b4f01-202">Da mesma forma, o prefixo 2002: ac1f: 2aef: 2::/64 é configurado na interface 6-over-4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-202">Similarly, the 2002:ac1f:2aef:2::/64 prefix is configured on the 6-over-4 interface.</span></span>

<span data-ttu-id="b4f01-203">Os próximos três comandos permitem que o computador do gateway 6to4 funcione como um roteador:</span><span class="sxs-lookup"><span data-stu-id="b4f01-203">The next three commands enable the 6to4 gateway computer to function as a router:</span></span>

<span data-ttu-id="b4f01-204">**IPv6 IFC 2 forw**</span><span class="sxs-lookup"><span data-stu-id="b4f01-204">**ipv6 ifc 2 forw**</span></span>

<span data-ttu-id="b4f01-205">**IPv6 IFC 3 forw avçd**</span><span class="sxs-lookup"><span data-stu-id="b4f01-205">**ipv6 ifc 3 forw adv**</span></span>

<span data-ttu-id="b4f01-206">**IPv6 IFC 4 forw avçd**</span><span class="sxs-lookup"><span data-stu-id="b4f01-206">**ipv6 ifc 4 forw adv**</span></span>

<span data-ttu-id="b4f01-207">O comando **IPv6 IFC** controla os atributos de uma interface.</span><span class="sxs-lookup"><span data-stu-id="b4f01-207">The **ipv6 ifc** command controls attributes of an interface.</span></span> <span data-ttu-id="b4f01-208">Um roteador encaminha pacotes e envia anúncios de roteador.</span><span class="sxs-lookup"><span data-stu-id="b4f01-208">A router forwards packets and sends router advertisements.</span></span> <span data-ttu-id="b4f01-209">Na implementação do IPv6 da Microsoft, esses atributos por interface são controlados separadamente.</span><span class="sxs-lookup"><span data-stu-id="b4f01-209">In the Microsoft IPv6 implementation, these per-interface attributes are controlled separately.</span></span>

<span data-ttu-id="b4f01-210">\#A interface 2 não é necessária para publicidade porque é uma pseudo interface.</span><span class="sxs-lookup"><span data-stu-id="b4f01-210">Interface \#2 is not needed for advertising because it is a pseudo-interface.</span></span>

<span data-ttu-id="b4f01-211">Se o seu computador tiver interfaces adicionais, elas também deverão ser configuradas para serem encaminhadas e anunciadas.</span><span class="sxs-lookup"><span data-stu-id="b4f01-211">If your computer has additional interfaces, they should also be configured to be forwarding and advertising.</span></span>

<span data-ttu-id="b4f01-212">Depois de executar esses comandos, o protocolo IPv6 da Microsoft configurará automaticamente os endereços nas interfaces \# 3 e \# 4 usando os respectivos prefixos de sub-rede e as duas interfaces começarão a enviar anúncios de roteador em intervalos de aproximadamente 3 a 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="b4f01-212">After running these commands, the Microsoft IPv6 protocol will automatically configure addresses on interfaces \#3 and \#4 using the respective subnet prefixes and the two interfaces will start sending router advertisements at approximately 3 to 10 minute intervals.</span></span>

<span data-ttu-id="b4f01-213">Os hosts que recebem esses anúncios de roteador serão automaticamente configurados com uma rota padrão e um endereço 6to4 derivado do prefixo de sub-rede do link.</span><span class="sxs-lookup"><span data-stu-id="b4f01-213">Hosts receiving these router advertisements will automatically configure themselves with a default route and a 6to4 address derived from the subnet prefix of their link.</span></span> <span data-ttu-id="b4f01-214">Eles terão comunicação com outros sites 6to4 e o 6bone por meio do computador do gateway.</span><span class="sxs-lookup"><span data-stu-id="b4f01-214">They will have communication to other 6to4 sites and the 6bone through the gateway computer.</span></span>

## <a name="debugging-6to4-configuration"></a><span data-ttu-id="b4f01-215">Depurando configuração de 6to4</span><span class="sxs-lookup"><span data-stu-id="b4f01-215">Debugging 6to4 Configuration</span></span>

<span data-ttu-id="b4f01-216">**Para depurar a configuração de 6to4**</span><span class="sxs-lookup"><span data-stu-id="b4f01-216">**To debug your 6to4 configuration**</span></span>

1.  <span data-ttu-id="b4f01-217">Verifique a conectividade IPv4 para o roteador de retransmissão 6to4:</span><span class="sxs-lookup"><span data-stu-id="b4f01-217">Check your IPv4 connectivity to the 6to4 relay router:</span></span>

    <span data-ttu-id="b4f01-218">**6to4.ipv6.microsoft.com ping**</span><span class="sxs-lookup"><span data-stu-id="b4f01-218">**ping 6to4.ipv6.microsoft.com**</span></span>

    <span data-ttu-id="b4f01-219">Se isso falhar, você não terá conectividade de Internet global.</span><span class="sxs-lookup"><span data-stu-id="b4f01-219">If this fails, then you do not have global Internet connectivity.</span></span>

2.  <span data-ttu-id="b4f01-220">Verifique o encapsulamento de IPv6 usando o túnel automático:</span><span class="sxs-lookup"><span data-stu-id="b4f01-220">Check IPv6 encapsulation by using automatic tunneling:</span></span>

    <span data-ttu-id="b4f01-221">**ping6:: 131.107.152.32**</span><span class="sxs-lookup"><span data-stu-id="b4f01-221">**ping6 ::131.107.152.32**</span></span>

    <span data-ttu-id="b4f01-222">Se isso falhar, você poderá ter um firewall ou NAT (tradutor de endereço de rede) entre o computador e a Internet.</span><span class="sxs-lookup"><span data-stu-id="b4f01-222">If this fails, then you might have a firewall or network address translator (NAT) between your computer and the Internet.</span></span> <span data-ttu-id="b4f01-223">Se isso for bem-sucedido, sua conexão com a Internet poderá dar suporte a 6to4.</span><span class="sxs-lookup"><span data-stu-id="b4f01-223">If this is successful, then your Internet connection can support 6to4.</span></span>

3.  <span data-ttu-id="b4f01-224">Verifique a exibição do comando IPv6 RT.</span><span class="sxs-lookup"><span data-stu-id="b4f01-224">Check the display of the ipv6 rt command.</span></span> <span data-ttu-id="b4f01-225">Você deverá ver uma rota 2002::/16-> 2.</span><span class="sxs-lookup"><span data-stu-id="b4f01-225">You should see a 2002::/16 -> 2 route.</span></span> <span data-ttu-id="b4f01-226">Verifique a exibição do comando IPv6 If 2.</span><span class="sxs-lookup"><span data-stu-id="b4f01-226">Check the display of the ipv6 if 2 command.</span></span> <span data-ttu-id="b4f01-227">Você deverá ver um endereço preferencial com um prefixo 2002::/16.</span><span class="sxs-lookup"><span data-stu-id="b4f01-227">You should see a preferred address with a 2002::/16 prefix.</span></span>

> [!Note]  
> <span data-ttu-id="b4f01-228">O endereço IPv4 do roteador de retransmissão 6to4 da Microsoft de 131.107.152.32 está sujeito a alterações.</span><span class="sxs-lookup"><span data-stu-id="b4f01-228">The IPv4 address of the Microsoft 6to4 relay router of 131.107.152.32 is subject to change.</span></span> <span data-ttu-id="b4f01-229">Se a etapa 2 acima não funcionar, verifique a saída do comando ping na etapa 1 para verificar o endereço IPv4 do roteador de retransmissão 6to4 da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b4f01-229">If Step 2 above does not work, check the output of the ping command in step 1 to verify the IPv4 address of the Microsoft 6to4 relay router.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b4f01-230">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b4f01-230">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4f01-231">Configurações recomendadas para IPv6</span><span class="sxs-lookup"><span data-stu-id="b4f01-231">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> <dt>

[<span data-ttu-id="b4f01-232">Sub-rede única com endereços de link local</span><span class="sxs-lookup"><span data-stu-id="b4f01-232">Single subnet with link-local addresses</span></span>](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="b4f01-233">Usando o IPsec entre dois hosts de link local</span><span class="sxs-lookup"><span data-stu-id="b4f01-233">Using IPsec between two local link hosts</span></span>](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



