---
description: 6to4 é um método para conectar hosts IPv6 ou sites pela infraestrutura de Internet IPv4 existente.
ms.assetid: 3ca8518d-42f0-428c-b94c-ff244d17b314
title: 'Configuração 2: Tráfego IPv6 entre nós em sub-redes diferentes de um IPv4 Internetwork (6to4)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d976aa3ea21d990ea22f861fbf05a816866e6b0d21502211e23a0e331a2f851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112492"
---
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a>Configuração 2: Tráfego IPv6 entre nós em sub-redes diferentes de um IPv4 Internetwork (6to4)

6to4 é um método para conectar hosts IPv6 ou sites pela infraestrutura de Internet IPv4 existente. Ele usa um prefixo de endereço exclusivo para dar aos sites IPv6 isolados seu próprio espaço de endereço IPv6. 6to4 é como um "pseudo-ISP" fornecendo conectividade IPv6. Você pode usar 6to4 para se comunicar diretamente com outros 6to4 sites. 6to4 requer o uso de roteadores IPv6 e seu tráfego IPv6 é encapsulado com um header IPv4.

A ilustração a seguir mostra a configuração de dois nós em sub-redes separadas usando 6to4 para se comunicar em um roteador IPv4.

![nós que usam 6to4 para se comunicar em um roteador ipv4.](images/v6mig-2.png)

O principal requisito para usar 6to4 é um endereço IPv4 globalmente stável para seu site. Suponha que seu site consiste em uma coleção de computadores IPv6 que você gerencia (alguns executando o protocolo IPv6 da Microsoft e outros executando outras implementações de IPv6). Suponha também que todos os computadores IPv6 estão conectados diretamente usando Ethernet ou 6 sobre 4. O endereço IPv4 globalmente stável deve ser atribuído a um dos computadores que executam o protocolo IPv6 da Microsoft. Esse computador será seu gateway 6to4 dados.

Se você tiver um endereço IPv4 que faz parte do espaço de endereço privado (10.0.0.0/8, 172.16.0.0/12 ou 192.168.0.0/16) ou o espaço de endereço DE APIPA (Endereçamento IP Privado Automático) de 169.254.0.0/16 usado pelo Windows 2000, ele não é globalmente rouco. Caso contrário, provavelmente é um endereço IP público e é globalmente stável. Consulte o [tópico Depurando 6to4 configuração](#debugging-6to4-configuration) neste documento para obter mais ajuda para determinar se sua conexão ISP dá suporte a 6to4.

## <a name="the-6to4cfgexe-tool"></a>A 6to4cfg.exe de dados

A 6to4cfg.exe automatiza a configuração 6to4, descobrindo automaticamente seu endereço IPv4 globalmente stável e criando um prefixo 6to4 dados. Ele executa a configuração diretamente ou pode escrever um script de configuração que você pode inspecionar e executar mais tarde.

A sintaxe 6to4cfg.exe comando básica é a seguinte.

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span id="_filename_"></span><span id="_FILENAME_"></span>\[*Filename*\]
</dt> <dd>

Grava o script de configuração em um arquivo, se você especificar um nome de arquivo. O script de configuração usa Ipv6.exe.

Você pode especificar con para o nome do arquivo gravar o script de configuração na saída do console, o que é útil para ver o que 6to4cfg.exe fará em um cenário de teste.

Se você não especificar um nome de arquivo, 6to4cfg.exe atualizará diretamente a configuração de IPv6 em seu computador.

</dd> <dt>

<span id="-r"></span><span id="-R"></span>-r
</dt> <dd>

Torna-se 6to4 de gateway para sua rede local, habilitando o roteamento em todas as interfaces e prefixos de sub-rede atribuídos.

</dd> <dt>

<span id="-s"></span><span id="-S"></span>-s
</dt> <dd>

Habilita o endereçamento local do site 6to4 site. Esse comando só é útil quando usado em conjunto com -r.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>-u
</dt> <dd>

Especifica que a configuração 6to4 ser revertida. Portanto, 6to4cfg -u inverte o efeito de 6to4cfg e 6to4cfg -r -u inverte o efeito de 6to4cfg -r e assim por diante.

</dd> <dt>

<span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>*Retransmissão* -R
</dt> <dd>

Especifica o nome ou o endereço IPv4 de um roteador 6to4 retransmissão. O nome padrão é 6to4.ipv6.microsoft.com, o roteador 6to4 de retransmissão na Internet.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>-b
</dt> <dd>

Especifica que 6to4cfg.exe escolhe o endereço de retransmissão "melhor" em vez do primeiro.

</dd> <dt>

<span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>Endereço *-S*
</dt> <dd>

Especifica o endereço IPv4 local para o prefixo 6to4 dados.

</dd> </dl>

## <a name="manual-6to4-configuration"></a>Configuração 6to4 manual

Neste exemplo, o endereço do gateway 6to4 é 172.31.42.239. Você precisa de seu próprio endereço IPv4 globalmente 6to4.

> [!Note]  
> O endereço IP 172.31.42.239 é usado apenas para fins de exemplo. Esse é um endereço privado e não é globalmente rápido na Internet.

 

O endereço IPv4 globalmente 32 bits é combinado com o prefixo de 16 bits 2002::/16 para formar um prefixo de endereço IPv6 de 48 bits para seu site. Neste exemplo, o prefixo 6to4 site é 2002:ac1f:2aef::/48. Observe que ac1f:2aef é a codificação hexadecimal de 172.31.42.239 (é claro que você usará um prefixo diferente com base em seu próprio endereço IPv4 globalmente roucável). Usando o 6to4 do site, você pode atribuir endereços e prefixos de sub-rede dentro de seu site.

Este exemplo presume que você use a sub-rede 0 para configurar manualmente um endereço 6to4 no computador do gateway do 6to4 e que você use a sub-rede 1 para configurar automaticamente os endereços no segmento de rede Ethernet. No entanto, outras opções são possíveis.

1.  Use Ipv6.exe para habilitar 6to4 no computador 6to4 gateway:

    **ipv6 rtu 2002::/16 2**

    O **comando ipv6 rtu** executa uma atualização de tabela de roteamento. Ele pode ser usado para adicionar, remover ou atualizar uma rota. Nesse caso, ele está habilitando 6to4.

    O argumento 2002::/16 é o prefixo da rota, especificando o prefixo 6to4 exclusivo.

    O argumento 2 especifica a interface no link para esse prefixo. A Interface \# 2 é a "pseudo-interface" usada para túneis configurados, túnel automático e 6to4. Quando um endereço de destino IPv6 corresponde ao prefixo 2002::/16, os 32 bits que seguem o prefixo no endereço de destino são extraídos para formar um endereço de destino IPv4. O pacote é encapsulado com um header IPv4 e enviado para o endereço de destino IPv4.

2.  Configure um 6to4 no seu computador 6to4 gateway:

    **ipv6 adu 2/2002:ac1f:2aef::ac1f:2aef**

    O **comando adu ipv6** executa uma atualização de endereço. Ele pode ser usado para adicionar, remover ou atualizar um endereço em uma interface. Nesse caso, ele está configurando o endereço de 6to4 computador.

    O argumento 2/2002:ac1f:2aef::ac1f:2aef especifica a interface e o endereço. Ele requer a configuração do endereço 2002:ac1f:2aef::ac1f:2aef na interface \# 2. O endereço é criado usando o prefixo do site 2002:ac1f:2aef::/48, sub-rede 0 para dar um prefixo de sub-rede 2002:ac1f:2aef::/64 e um identificador de interface de 64 bits. A convenção demonstrada usa o endereço IPv4 do computador para o identificador de interface para endereços atribuídos à interface \# 2. Para seu uso, ac1f:2aef deve ser substituído pela codificação hexadecimal de seu próprio endereço IPv4 globalmente roustável.

Os dois comandos anteriores são suficientes para permitir a comunicação com outros 6to4 sites. Por exemplo, você pode tentar fazer ping no site do Microsoft 6to4:

**ping6 2002:836b:9820::836b:9820**

Para habilitar a comunicação com o 6bone, você deve criar um túnel configurado padrão para uma 6to4 retransmissão. Você pode usar o roteador de 6to4 microsoft, 131.107.152.32:

**ipv6 rtu ::/0 2/::131.107.152.32 pub life 1800**

O **comando ipv6 rtu** executa uma atualização de tabela de roteamento, estabelecendo, nesta instância, uma rota padrão para a 6to4 retransmissão.

O argumento ::/0 é o prefixo de rota. O prefixo de comprimento zero indica que é uma rota padrão.

O argumento 2/::131.107.152.32 especifica o vizinho do próximo salto para esse prefixo. Ele requer que os pacotes correspondentes ao prefixo sejam encaminhados para endereço ::131.107.152.32 usando a interface \# 2. Encaminhar um pacote para ::131.107.152.32 na interface 2 faz com que ele seja encapsulado com um header v4 e enviado para \# 131.107.152.32.

O argumento pub torna essa rota publicada. Como isso só é relevante para roteadores, ele não tem efeito até que o roteamento seja habilitado. Da mesma forma, o tempo de vida de 30 minutos pertence apenas se o roteamento estiver habilitado.

Você deve ser capaz de acessar sites de 6bones, bem como 6to4 sites. Você pode usar o seguinte comando para testar isso:

**ping6 3ffe:1cff:0:f5::1**

A etapa final é habilitar o roteamento em seu gateway 6to4 dados. Este exemplo presume que a interface 3 em seu computador gateway é uma interface Ethernet e \# a interface \# 4 é 6 sobre 4. Seu computador pode numerar suas interfaces de forma diferente. Os dois comandos a seguir atribuem prefixos de sub-rede aos dois links. Os prefixos de sub-rede são derivados do prefixo 6to4 2002:ac1f:2aef::/48 do site:

**ipv6 rtu 2002:ac1f:2aef:1::/64 3 pub life 1800**

**ipv6 rtu 2002:ac1f:2aef:2::/64 4 pub life 1800**

O **comando ipv6 rtu** especifica que o prefixo 2002:ac1f:2aef:1::/64 está no link para a interface \# 3. Ele está configurando o primeiro prefixo de sub-rede na interface Ethernet. A rota é publicada com um tempo de vida de 30 minutos.

Da mesma forma, o prefixo 2002:ac1f:2aef:2::/64 é configurado na interface 6 sobre 4.

Os três comandos a seguir permitem que o 6to4 do gateway funcione como um roteador:

**ipv6 ifc 2 forw**

**ipv6 ifc 3 forw adv**

**ipv6 ifc 4 forw adv**

O **comando ifc ipv6** controla atributos de uma interface. Um roteador encaminha pacotes e envia anúncios de roteador. Na implementação do Microsoft IPv6, esses atributos por interface são controlados separadamente.

A Interface \# 2 não é necessária para publicidade porque é uma pseudo-interface.

Se o computador tiver interfaces adicionais, eles também deverão ser configurados para serem encaminhados e anunciados.

Depois de executar esses comandos, o protocolo IPv6 da Microsoft configurará automaticamente endereços nas interfaces 3 e 4 usando os respectivos prefixos de sub-rede e as duas interfaces começarão a enviar anúncios de roteador em intervalos de aproximadamente 3 a \# \# 10 minutos.

Os hosts que recebem esses anúncios de roteador se configurarão automaticamente com uma rota padrão e um 6to4 de rede derivado do prefixo de sub-rede de seu link. Eles terão comunicação com outros sites 6to4 e o 6bone por meio do computador do gateway.

## <a name="debugging-6to4-configuration"></a>Configuração de 6to4 depuração

**Para depurar sua configuração 6to4 configuração**

1.  Verifique a conectividade IPv4 com o roteador 6to4 retransmissão:

    **ping 6to4.ipv6.microsoft.com**

    Se isso falhar, você não terá conectividade global com a Internet.

2.  Verifique o encapsulamento IPv6 usando o túnel automático:

    **ping6 ::131.107.152.32**

    Se isso falhar, você poderá ter um FIREWALL ou NAT (conversor de endereço de rede) entre o computador e a Internet. Se isso for bem-sucedido, sua conexão com a Internet poderá dar suporte 6to4.

3.  Verifique a exibição do comando ipv6 rt. Você deverá ver uma rota 2002::/16 -> 2. Verifique a exibição do comando ipv6 if 2. Você deve ver um endereço preferencial com um prefixo 2002::/16.

> [!Note]  
> O endereço IPv4 do roteador de retransmissão do Microsoft 6to4 131.107.152.32 está sujeito a alterações. Se a Etapa 2 acima não funcionar, verifique a saída do comando ping na etapa 1 para verificar o endereço IPv4 do roteador de retransmissão 6to4 Microsoft.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurações recomendadas para IPv6](recommended-configurations-2.md)
</dt> <dt>

[Sub-rede única com endereços locais de link](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[Usando o IPsec entre dois hosts de link local](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



