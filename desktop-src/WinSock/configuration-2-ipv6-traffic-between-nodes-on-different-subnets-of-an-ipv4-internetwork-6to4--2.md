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
# <a name="configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4"></a>Configuração 2: tráfego IPv6 entre nós em sub-redes diferentes de um protocolo de rede IPv4 (6to4)

o 6to4 é um método para conectar hosts ou sites IPv6 pela infraestrutura de Internet IPv4 existente. Ele usa um prefixo de endereço exclusivo para dar aos sites IPv6 isolados seu próprio espaço de endereço IPv6. o 6to4 é como um "pseudo-ISP" que fornece conectividade IPv6. Você pode usar o 6to4 para se comunicar diretamente com outros sites 6to4. o 6to4 não exige o uso de roteadores IPv6 e seu tráfego IPv6 é encapsulado com um cabeçalho IPv4.

A ilustração a seguir mostra a configuração de dois nós em sub-redes separadas usando o 6to4 para se comunicar em um roteador IPv4.

![nós que usam o 6to4 para se comunicar em um roteador IPv4.](images/v6mig-2.png)

O principal requisito para usar o 6to4 é um endereço IPv4 roteável globalmente para seu site. Suponha que seu site consiste em uma coleção de computadores IPv6 que você gerencia (alguns executando o protocolo Microsoft IPv6 e alguns executando outras implementações de IPv6). Suponha também que todos os computadores IPv6 estejam diretamente conectados usando Ethernet ou 6 sobre 4. O endereço IPv4 roteável globalmente deve ser atribuído a um dos seus computadores que executam o protocolo IPv6 da Microsoft. Este computador será o gateway do 6to4.

Se você tiver um endereço IPv4 que faz parte do espaço de endereço privado (10.0.0.0/8, 172.16.0.0/12 ou 192.168.0.0/16) ou o espaço de endereço APIPA (endereçamento IP privado automático) de 169.254.0.0/16 usado pelo Windows 2000, ele não será roteável globalmente. Caso contrário, é provavelmente um endereço IP público e é roteável globalmente. Consulte o tópico [depuração de configuração de 6to4](#debugging-6to4-configuration) neste documento para obter mais ajuda para determinar se sua conexão de ISP oferece suporte a 6to4.

## <a name="the-6to4cfgexe-tool"></a>A ferramenta de 6to4cfg.exe

A ferramenta de 6to4cfg.exe automatiza a configuração de 6to4, descobrindo automaticamente seu endereço IPv4 roteável globalmente e criando um prefixo 6to4. Ele executa a configuração diretamente ou pode gravar um script de configuração que você pode inspecionar e executar mais tarde.

A sintaxe de comando 6to4cfg.exe básica é a seguinte.

``` syntax
6to4cfg [-r] [-s] [-u] [-R relay] [-b] [-S address] [filename]
```

<dl> <dt>

<span id="_filename_"></span><span id="_FILENAME_"></span>\[*nome do arquivo*\]
</dt> <dd>

Grava o script de configuração em um arquivo, se você especificar um nome de arquivo. O script de configuração usa Ipv6.exe.

Você pode especificar con para o nome do arquivo gravar o script de configuração na saída do console, o que é útil para ver o que 6to4cfg.exe fará em um cenário de teste.

Se você não especificar um nome de arquivo, 6to4cfg.exe atualizará diretamente a configuração de IPv6 em seu computador.

</dd> <dt>

<span id="-r"></span><span id="-R"></span>-r
</dt> <dd>

Torna-se um roteador de gateway 6to4 para sua rede local, habilitando o roteamento em todas as suas interfaces e prefixos de sub-rede atribuídos.

</dd> <dt>

<span id="-s"></span><span id="-S"></span>-s
</dt> <dd>

Habilita o endereçamento local no site do 6to4. Esse comando só é útil quando usado em conjunto com-r.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>-u
</dt> <dd>

Especifica que a configuração de 6to4 será revertida. Portanto, 6to4cfg-u reverte o efeito de 6to4cfg e 6to4cfg-r-u inverte o efeito de 6to4cfg-r e assim por diante.

</dd> <dt>

<span id="-R_relay"></span><span id="-r_relay"></span><span id="-R_RELAY"></span>-R *retransmissão*
</dt> <dd>

Especifica o nome ou endereço IPv4 de um roteador de retransmissão 6to4. O nome padrão é 6to4.ipv6.microsoft.com, o roteador de retransmissão 6to4 na Internet.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>-b
</dt> <dd>

Especifica que 6to4cfg.exe escolhe o endereço de retransmissão "melhor" em vez do primeiro.

</dd> <dt>

<span id="-S_address"></span><span id="-s_address"></span><span id="-S_ADDRESS"></span>-S *endereço*
</dt> <dd>

Especifica o endereço IPv4 local para o prefixo 6to4.

</dd> </dl>

## <a name="manual-6to4-configuration"></a>Configuração de 6to4 manual

Neste exemplo, o endereço do gateway 6to4 é 172.31.42.239. Você precisa de seu próprio endereço IPv4 roteável globalmente para usar o 6to4.

> [!Note]  
> O endereço IP 172.31.42.239 é usado apenas para fins de exemplo. Esse é um endereço privado e não é roteável globalmente na Internet.

 

O endereço IPv4 roteável globalmente de 32 bits é combinado com o prefixo de 16 bits 2002::/16 para formar um prefixo de endereço IPv6 de 48 bits para seu site. Neste exemplo, o prefixo do site 6to4 é 2002: ac1f: 2aef::/48. Observe que ac1f: 2aef é a codificação hexadecimal de 172.31.42.239 (é claro, você usará um prefixo diferente com base em seu próprio endereço IPv4 roteável globalmente). Usando o prefixo do site 6to4, você pode atribuir endereços e prefixos de sub-rede dentro de seu site.

Este exemplo pressupõe que você use a sub-rede 0 para configurar manualmente um endereço 6to4 no seu computador de gateway 6to4 e que você usa a sub-rede 1 para configurar automaticamente endereços em seu segmento de rede Ethernet. No entanto, outras opções são possíveis.

1.  Use Ipv6.exe para habilitar o 6to4 em seu computador de gateway 6to4:

    **IPv6 RTU 2002::/16 2**

    O comando **ipv6 rtu** executa uma atualização de tabela de roteamento. Ele pode ser usado para adicionar, remover ou atualizar uma rota. Nesse caso, ele está habilitando o 6to4.

    O argumento 2002::/16 é o prefixo da rota, especificando o prefixo 6to4 exclusivo.

    O argumento 2 especifica a interface no link para esse prefixo. \#A interface 2 é a "pseudo-interface" usada para túneis configurados, túnel automático e 6to4. Quando um endereço de destino IPv6 corresponde ao prefixo 2002::/16, os 32 bits que seguem o prefixo no endereço de destino são extraídos para formar um endereço de destino IPv4. O pacote é encapsulado com um cabeçalho IPv4 e enviado ao endereço de destino IPv4.

2.  Configure um endereço 6to4 em seu computador de gateway 6to4:

    **o IPv6 Adu 2/2002: ac1f: 2aef:: ac1f: 2aef**

    O comando **IPv6 Adu** executa uma atualização de endereço. Ele pode ser usado para adicionar, remover ou atualizar um endereço em uma interface. Nessa instância, ele está configurando o endereço 6to4 do computador.

    O argumento 2/2002: ac1f: 2aef:: ac1f: 2aef especifica a interface e o endereço. Ele requer a configuração do endereço 2002: ac1f: 2aef:: ac1f: 2aef na interface \# 2. O endereço é criado usando o prefixo do site 2002: ac1f: 2aef::/48, sub-rede 0 para dar um prefixo de sub-rede 2002: ac1f: 2aef::/64 e um identificador de interface de 64 bits. A Convenção demonstrada usa o endereço IPv4 do computador para o identificador de interface para endereços atribuídos à interface \# 2. Para seu uso, ac1f: 2aef deve ser substituído pela codificação hexadecimal do seu próprio endereço IPv4 roteável globalmente.

Os dois comandos anteriores são suficientes para permitir a comunicação com outros sites 6to4. Por exemplo, você pode tentar executar ping no site 6to4 da Microsoft:

**ping6 2002:836b: 9820:: 836b: 9820**

Para habilitar a comunicação com o 6bone, você deve criar um túnel configurado padrão para uma retransmissão de 6to4. Você pode usar o roteador de retransmissão 6to4 da Microsoft, 131.107.152.32:

**IPv6 RTU::/0 2/:: 131.107.152.32 pub Life 1800**

O comando **ipv6 rtu** executa uma atualização de tabela de roteamento, estabelecendo, nessa instância, uma rota padrão para a retransmissão de 6to4.

O argumento::/0 é o prefixo de rota. O prefixo de comprimento zero indica que se trata de uma rota padrão.

O argumento 2/:: 131.107.152.32 especifica o vizinho do próximo salto para esse prefixo. Ele requer que os pacotes que correspondem ao prefixo sejam encaminhados para Address:: 131.107.152.32 usando a interface \# 2. O encaminhamento de um pacote para:: 131.107.152.32 na interface \# 2 faz com que ele seja encapsulado com um cabeçalho v4 e enviado a 131.107.152.32.

O argumento pub torna essa rota publicada. Como isso só é relevante para roteadores, ele não tem efeito até que o roteamento seja habilitado. Da mesma forma, o tempo de vida de 30 minutos se refere apenas se o roteamento estiver habilitado.

Você deve ser capaz de acessar sites do 6bone, bem como sites 6to4. Você pode usar o seguinte comando para testar isso:

**ping6 3ffe: 1cff: 0: F5:: 1**

A etapa final é habilitar o roteamento em seu gateway 6to4. Este exemplo supõe que a interface \# 3 no seu computador de gateway é uma interface Ethernet e a interface \# 4 é 6-over-4. Seu computador pode numerar suas interfaces de forma diferente. Os dois comandos a seguir atribuem prefixos de sub-rede aos dois links. Os prefixos de sub-rede são derivados do prefixo 6to4 do site 2002: ac1f: 2aef::/48:

**IPv6 RTU 2002: ac1f: 2aef: 1::/64 3 pub Life 1800**

**IPv6 RTU 2002: ac1f: 2aef: 2::/64 4 pub Life 1800**

O comando **ipv6 rtu** especifica que o prefixo 2002: ac1f: 2aef: 1::/64 está no link para a interface \# 3. Ele está configurando o primeiro prefixo de sub-rede na interface Ethernet. A rota é publicada com um tempo de vida de 30 minutos.

Da mesma forma, o prefixo 2002: ac1f: 2aef: 2::/64 é configurado na interface 6-over-4.

Os próximos três comandos permitem que o computador do gateway 6to4 funcione como um roteador:

**IPv6 IFC 2 forw**

**IPv6 IFC 3 forw avçd**

**IPv6 IFC 4 forw avçd**

O comando **IPv6 IFC** controla os atributos de uma interface. Um roteador encaminha pacotes e envia anúncios de roteador. Na implementação do IPv6 da Microsoft, esses atributos por interface são controlados separadamente.

\#A interface 2 não é necessária para publicidade porque é uma pseudo interface.

Se o seu computador tiver interfaces adicionais, elas também deverão ser configuradas para serem encaminhadas e anunciadas.

Depois de executar esses comandos, o protocolo IPv6 da Microsoft configurará automaticamente os endereços nas interfaces \# 3 e \# 4 usando os respectivos prefixos de sub-rede e as duas interfaces começarão a enviar anúncios de roteador em intervalos de aproximadamente 3 a 10 minutos.

Os hosts que recebem esses anúncios de roteador serão automaticamente configurados com uma rota padrão e um endereço 6to4 derivado do prefixo de sub-rede do link. Eles terão comunicação com outros sites 6to4 e o 6bone por meio do computador do gateway.

## <a name="debugging-6to4-configuration"></a>Depurando configuração de 6to4

**Para depurar a configuração de 6to4**

1.  Verifique a conectividade IPv4 para o roteador de retransmissão 6to4:

    **6to4.ipv6.microsoft.com ping**

    Se isso falhar, você não terá conectividade de Internet global.

2.  Verifique o encapsulamento de IPv6 usando o túnel automático:

    **ping6:: 131.107.152.32**

    Se isso falhar, você poderá ter um firewall ou NAT (tradutor de endereço de rede) entre o computador e a Internet. Se isso for bem-sucedido, sua conexão com a Internet poderá dar suporte a 6to4.

3.  Verifique a exibição do comando IPv6 RT. Você deverá ver uma rota 2002::/16-> 2. Verifique a exibição do comando IPv6 If 2. Você deverá ver um endereço preferencial com um prefixo 2002::/16.

> [!Note]  
> O endereço IPv4 do roteador de retransmissão 6to4 da Microsoft de 131.107.152.32 está sujeito a alterações. Se a etapa 2 acima não funcionar, verifique a saída do comando ping na etapa 1 para verificar o endereço IPv4 do roteador de retransmissão 6to4 da Microsoft.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurações recomendadas para IPv6](recommended-configurations-2.md)
</dt> <dt>

[Sub-rede única com endereços de link local](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[Usando o IPsec entre dois hosts de link local](configuration-4-using-ipsec-between-two-local-link-hosts-2.md)
</dt> </dl>

 

 



